
### HELLO
```kode
// The first Kode program
print("hello world")

```

### TOUR
```kode
// A quick tour of Kode v0.1
const GREETING = "Hello"
const PI = 3.14159

fn area(r: float) -> float => PI * r * r

fn describe(n: int) -> string {
    if n % 2 == 0 {
        return "even"
    } else if n < 0 {
        return "negative odd"
    }
    return "odd"
}

fn shout(s: string) -> string => s + "!"

name = "Asha"
print(shout("${GREETING}, ${name}"))
print("area:", area(2.0))

total = 0
for i in 1..=5 {
    total += i
}
print("sum 1..5 =", total)

n = 0
while n < 6 {
    n += 1
    if n == 2 {
        continue
    }
    if n == 5 {
        break
    }
    print(n, describe(n))
}

ready = n > 3 and not (total == 0)
print("ready:", ready, "len:", len(name), "int(3.9):", int(3.9), "float(2):", float(2))
assert(total == 15)

```

### BANK
```kode
// Classes, maps, lists, enums, match and errors in one program
enum Kind { Deposit, Withdraw }

class Account {
    owner: string
    balance: int = 0
    history: [string] = []

    fn apply(kind: Kind, amount: int) {
        match kind {
            Kind.Deposit => {
                balance += amount
            }
            Kind.Withdraw => {
                if amount > balance {
                    throw Error(message: "insufficient funds for ${owner}", code: 402)
                }
                balance -= amount
            }
        }
        history.add("${amount}")
    }
}

accounts = {"asha": Account(owner: "Asha"), "ravi": Account(owner: "Ravi", balance: 50)}

accounts["asha"].apply(Kind.Deposit, 100)
accounts["ravi"].apply(Kind.Withdraw, 20)

accounts["ravi"].apply(Kind.Withdraw, 500) catch e {
    print("failed:", e.message, e.code)
}

for name, acct in accounts {
    print(name, acct.balance, len(acct.history))
}

```

### FIB
```kode
// Recursion, integers and a loop
fn fib(n: int) -> int {
    if n < 2 {
        return n
    }
    return fib(n - 1) + fib(n - 2)
}

for i in 0..10 {
    print("fib(${i}) =", fib(i))
}

```

### API
```kode
// A small JSON API in the style of Express / FastAPI.
// Run it with: kode run examples/api.kode -- 8080
// Then: curl localhost:8080/users/7

fn list_users(req: Request) -> Response {
    limit = "10"
    if req.query.has("limit") {
        limit = req.query["limit"]
    }
    out = json_obj()
    out["count"] = json_int(2)
    out["limit"] = json_string(limit)
    return Response.json(json_map(out))
}

fn get_user(req: Request) -> Response {
    user = json_obj()
    user["id"] = json_int(req.params["id"].to_int())
    user["name"] = json_string("Asha")
    return Response.json(json_map(user))
}

fn create_user(req: Request) -> Response {
    doc = req.json()
    return Response(status: 201, body: doc.encode(), content_type: "application/json")
}

fn health(req: Request) -> Response {
    return Response.text("ok")
}

routes = Router()
routes.get("/users", list_users)
routes.get("/users/:id", get_user)
routes.post("/users", create_user)
routes.get("/health", health)

port = 8080
if args().len() > 0 {
    port = args()[0].to_int()
}

serve(port, routes)

```
