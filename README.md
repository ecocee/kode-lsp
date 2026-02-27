# Kode Language Support for VS Code

Professional, modern language support for the **Kode programming language** - a contemporary, expressive systems programming language with advanced features.

## ✨ Features

### 🎨 Advanced Syntax Highlighting

**Modern Language Constructs:**
- ✅ Generics with type parameters: `Container<T>`
- ✅ Async/await for concurrent programming
- ✅ Result and Option types for error handling
- ✅ Attributes and decorators: `#[attr]`, `@decorator`
- ✅ Macros with `!` operator: `println!()`
- ✅ Module paths with `::` syntax
- ✅ Operator varieties: `->`, `=>`, `<-`, `..`, `..=`
- ✅ Comprehensive type system including all numeric suffixes

**Complete Keyword Support:**
- Control flow: `if`, `else`, `while`, `for`, `do`, `match`, `yield`
- Declarations: `func`, `let`, `const`, `struct`, `enum`, `trait`, `impl`
- Async/Concurrency: `async`, `await`, `defer`, `spawn`, `send`, `receive`
- Access modifiers: `pub`, `priv`, `internal`, `protected`
- Type system: `type`, `alias`, `typeof`, `where`
- And 40+ more keywords

**String Handling:**
- Standard strings: `"Hello, World!"`
- Single quotes: `'c'`
- Template strings: `` `template` ``
- String interpolation: `"Hello, ${name}!"`
- Regex strings: `r"pattern"`

**Comment Types:**
- Line comments: `// comment`
- Block comments: `/* comment */`
- Documentation comments: `/// doc comment`

**Numeric Literals:**
- Decimals: `42`, `3.14`
- Hexadecimal: `0xFF`
- Binary: `0b1010`
- Octal: `0o755`
- Type suffixes: `42u32`, `3.14f64`

### 📝 60+ Code Snippets

**Modern Feature Snippets:**
| Prefix | Template | Usage |
|--------|----------|-------|
| `funcg` | Generic function | Parametric functions |
| `funcasync` | Async function | Concurrent operations |
| `structg` | Generic struct | Parametric types |
| `enumval` | Enum with values | Associated types |
| `traitmpl` | Trait implementation | Polymorphism |
| `funcresult` | Result-returning func | Error handling |
| `funcoption` | Option-returning func | Optional values |
| `matchguard` | Match with guards | Conditional patterns |
| `destructpat` | Destructuring pattern | Pattern matching |
| `letmut` | Mutable variable | Mutable binding |
| `typealias` | Type alias | Type definitions |
| `closure` | Closure definition | Higher-order functions |
| `hof` | Higher-order function | Function composition |
| `funcresult` | Result type template | Error handling |
| `select` | Channel select | Concurrent selection |
| `mutex` | Mutex operations | Thread safety |
| `defer` | Defer statement | Resource cleanup |
| `await` | Await expression | Async/await |
| `macro` | Macro invocation | Metaprogramming |
| `attr` | Attribute | Apply attribute |

Plus 40+ additional snippets for all language features!

### 🔧 Smart Language Configuration

- **Auto-closing pairs**: Brackets, quotes, angle brackets
- **Bracket matching**: Navigate and select matching pairs
- **Smart indentation**: Automatic indentation for blocks and async code
- **Code folding**: Collapse/expand `//region` blocks
- **Multi-line support**: Proper formatting for block comments
- **Word recognition**: Accurate identifier handling

### 🎯 Modern Language Features

**Type System:**
- Statically-typed with inference
- Generics: `Container<T, U>`
- Type parameters and constraints
- Primitive types: int, i8-i64, uint, u8-u64, float, f32, f64, bool, string, char, byte
- Complex types: arrays, tuples, structs, enums, traits

**Advanced Control Flow:**
- Pattern matching with guards
- Destructuring assignments
- Multiple return values
- Match expressions as values

**Error Handling:**
- Result types: `Result<T, E>`
- Option types: `Option<T>`
- Try-catch blocks
- Error propagation

**Concurrency:**
- Goroutines with `spawn`
- Channels for communication
- Select statements
- Mutex synchronization
- Defer for cleanup

**Functional Features:**
- First-class functions
- Closures and lambdas
- Higher-order functions
- Map, filter, reduce
- Composition patterns

**Modern Syntax:**
- Async/await support
- Macros and code generation
- Attributes and decorators
- Module system
- Visibility modifiers

## 📥 Installation

### From VS Code Marketplace
1. Open VS Code Extension Marketplace
2. Search for "Kode Language"
3. Click Install

### Manual Installation
```bash
# Clone or download the extension
git clone https://github.com/ecocee/kode-vscode
# Copy to extensions folder
cp -r kode-vscode ~/.vscode/extensions/
# Restart VS Code
```

## 🚀 Quick Start

### Create a Kode File
```bash
# Create new file
touch app.kode
```

### Hello World
```kode
func main() {
    let name = "World"
    print("Hello, ${name}!")
}
```

### Generic Function
```kode
func first<T>(arr: [T]) -> Option<T> {
    if (len(arr) > 0) {
        return Option.Some(arr[0])
    }
    return Option.None
}
```

### Async Operations
```kode
async func fetchData() -> Result<string, Error> {
    let response = await fetchFromServer("https://api.example.com")
    return Result.Success(response)
}
```

### Pattern Matching
```kode
match (result) {
    Result.Success(value) if value > 0 => print("Positive: ${value}"),
    Result.Success(value) => print("Non-positive: ${value}"),
    Result.Error(err) => print("Error: ${err}")
}
```

### Concurrency
```kode
func main() {
    let channel = make(Channel<string>)
    
    spawn {
        send(channel, "Hello from worker!")
    }
    
    let msg = receive(channel)
    print(msg)
}
```

### Generics and Traits
```kode
trait Drawable {
    func draw() -> void
}

struct Circle<T: Drawable> {
    shape: T
}

impl<T: Drawable> Circle<T> {
    func display() -> void {
        this.shape.draw()
    }
}
```

## ⌨️ Keyboard Shortcuts

| Action | Shortcut |
|--------|----------|
| Show Snippets | `Ctrl+Space` |
| Format Document | `Shift+Alt+F` |
| Go to Line | `Ctrl+G` |
| Toggle Line Comment | `Ctrl+/` |
| Go to Bracket | `Ctrl+Shift+\` |
| Find & Replace | `Ctrl+H` |

## 🎨 Supported Features by Category

### ✅ Fully Supported
- Complete syntax highlighting
- All 60+ code snippets
- Smart indentation
- Bracket matching and auto-closing
- Generic type highlighting
- Async/await syntax
- Pattern matching
- Error handling (Result/Option)
- String interpolation
- Numeric literals (all formats)
- Comments (all types)
- Attributes and decorators
- Macro invocations

### 🔄 Extensible
- Custom color schemes
- Additional snippets
- Language extensions

### 🔮 Planned
- Language Server Protocol (LSP) for:
  - Code completion
  - Go to definition
  - Hover information
  - Diagnostics
- Debugging support
- Code formatting provider
- Task provider for Kode compiler

## 📚 Examples

### Working with Result Types
```kode
func divide(a: int, b: int) -> Result<int, string> {
    if (b == 0) {
        return Result.Error("Division by zero")
    }
    return Result.Success(a / b)
}

func main() {
    match (divide(10, 2)) {
        Result.Success(val) => print("Result: ${val}"),
        Result.Error(msg) => print("Error: ${msg}")
    }
}
```

### Higher-Order Functions with Generics
```kode
func map<T, U>(arr: [T], f: (T) -> U) -> [U] {
    let result: [U] = []
    for (item in arr) {
        push(result, f(item))
    }
    return result
}

func main() {
    let nums = [1, 2, 3, 4, 5]
    let squared = map(nums, func(x) { return x * x })
    print(squared)  // [1, 4, 9, 16, 25]
}
```

### Struct with Generic Methods
```kode
struct Container<T> {
    value: T
}

impl<T> Container<T> {
    func new(val: T) -> Container<T> {
        return Container { value: val }
    }
    
    func get() -> T { return this.value }
    func set(val: T) -> void { this.value = val }
}
```

## 🔧 Settings & Configuration

### Recommended VS Code Settings
```json
{
    "[kode]": {
        "editor.defaultFormatter": "kode-lang.kode",
        "editor.formatOnSave": true,
        "editor.tabSize": 4,
        "editor.insertSpaces": true,
        "editor.rulers": [80, 120]
    }
}
```

## 📖 Resources

- **Kode Language Docs**: [syntax.md](../docs/syntax.md)
- **Kode Language Wiki**: [wiki.md](../docs/wiki.md)
- **GitHub Repository**: [github.com/ecocee/kode](https://github.com/ecocee/kode)
- **Issue Tracker**: [GitHub Issues](https://github.com/ecocee/kode/issues)

## 🐛 Troubleshooting

### Syntax highlighting not working
- Ensure file has `.kode` extension
- Reload VS Code: `Ctrl+Shift+P` → "Reload Window"
- Check language is set to "Kode" (bottom right)

### Snippets not showing
- Press `Ctrl+Space` to trigger suggestions
- Ensure IntelliSense is enabled in settings
- Check snippet trigger words in settings

### Indentation issues
- Verify `editor.tabSize` setting
- Set `editor.insertSpaces` to `true`
- Check `editor.autoIndent` is enabled

### Generic syntax not highlighting
- Ensure `<` and `>` are recognized as brackets
- Reload VS Code if theme was changed
- Check for conflicts with other extensions

## 🤝 Contributing

Found a bug or want to suggest a feature?

1. Check [existing issues](https://github.com/ecocee/kode/issues)
2. Create a [new issue](https://github.com/ecocee/kode/issues/new)
3. Submit pull requests welcome!

## 📄 License

MIT License - See LICENSE file for details

## 🎉 Release Notes

### Version 0.1.0 (2026-02-27)
- ✅ Added professional Kode logo and branding
- ✅ Advanced syntax highlighting for modern features
- ✅ 60+ code snippets including generics, async/await
- ✅ Support for attributes, decorators, and macros
- ✅ Enhanced language configuration
- ✅ Better generic type support
- ✅ Improved async/concurrency highlighting

### Version 0.1.0 (2026-02-27)
- Initial release with comprehensive syntax highlighting
- 30+ basic snippets
- Language configuration setup

---

**Modern, Fast, Expressive - Build Great Code with Kode! 🚀**

Made with ❤️ for the Kode Programming Language Community


## Working with Markdown

You can author your README using Visual Studio Code. Here are some useful editor keyboard shortcuts:

* Split the editor (`Cmd+\` on macOS or `Ctrl+\` on Windows and Linux).
* Toggle preview (`Shift+Cmd+V` on macOS or `Shift+Ctrl+V` on Windows and Linux).
* Press `Ctrl+Space` (Windows, Linux, macOS) to see a list of Markdown snippets.

## For more information

* [Visual Studio Code's Markdown Support](http://code.visualstudio.com/docs/languages/markdown)
* [Markdown Syntax Reference](https://help.github.com/articles/markdown-basics/)

**Enjoy!**
