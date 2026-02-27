# Change Log

All notable changes to the "Kode Language Support" extension will be documented in this file.

## [0.1.0] - 2026-02-27

### Added - Modern Language Features 🚀

- **Icon & Branding**
  - Professional Kode logo (SVG format)
  - Gallery banner for VS Code Marketplace
  - Enhanced publisher metadata

- **Advanced Syntax Highlighting**
  - Generics syntax with angle brackets `<T, U>`
  - Async/await keywords and async functions
  - Attributes and decorators (`#[attribute]`, `@decorator`)
  - Result and Option types highlighting
  - Type parameters and lifetime annotations
  - Macro invocations with `!` operator
  - Module path syntax with `::`
  - Range operators (`..`, `..=`, `::`)
  - Arrow operators (`->`, `=>`, `<-`)
  - Variant type suffixes (u8, i32, f64, etc.)
  - More primitive types (i8, i16, i32, i64, u8, u16, u32, u64, f32, f64, char, byte)
  - Mutability modifiers (mut, ref, ptr, &)
  - Regex strings (r"pattern")

- **Enhanced Code Snippets (60+ templates)**
  - Generic functions: `fng`
  - Async functions: `fnasync`
  - Match with guards: `matchguard`
  - Generic structs: `structg`
  - Enum with values: `enumval`
  - Trait implementation: `traitmpl`
  - Result types: `fnresult`
  - Option types: `fnoption`
  - Mutable variables: `letmut`
  - Type aliases: `typealias`
  - Destructuring: `destruct`, `destructpat`
  - Channel operations: `send`, `recv`
  - Select statements: `select`
  - Mutex operations: `mutex`
  - Defer statements: `defer`
  - Await expressions: `await`
  - Closures: `closure`
  - Higher-order functions: `hof`
  - And many more!

- **Language Configuration Enhancements**
  - Angle brackets `< >` as bracket pairs
  - Improved indentation rules for async functions
  - Support for async/await indentation
  - Block comment folding support
  - Better multi-line block support

- **Modern Kode Features Support**
  - Generics and type parameters
  - Async/concurrent programming
  - Advanced pattern matching
  - Error handling with Result types
  - Optional types with Option
  - Macros and attributes
  - Module system with advanced paths
  - First-class function types

### Changed
- Updated version to 0.1.0
- Completely revamped syntax grammar for modern language features
- Enhanced repository metadata (homepage, bugs, author)
- Improved package.json with badges and better categorization

### Improved
- Better generic type highlighting with nested generics
- More comprehensive operator support
- Improved function and method recognition
- Better string interpolation handling
- More accurate comment parsing
- Enhanced number literal support (unit suffixed numbers)

---

## [0.1.0] - 2026-02-27

### Added
- **Comprehensive Syntax Highlighting**
  - All Kode keywords: fn, let, const, if, else, while, for, do, match, struct, enum, trait, impl, import, export, etc.
  - String interpolation with `${}` syntax
  - Comment types: line (`//`), block (`/* */`), documentation (`///`)
  - All numeric formats: integers, floats, hex, binary, octal
  - Operators: arithmetic, bitwise, logical, comparison, assignment
  - Type highlighting and function recognition

- **30+ Code Snippets**
  - Function definitions and lambda functions
  - Control flow (if, while, for, do-while, match)
  - Data structures (struct, enum, trait)
  - Error handling (try-catch)
  - Module system (import, export)
  - Array operations (map, filter, reduce)
  - Concurrency (spawn, channels)
  - And more!

- **Enhanced Language Configuration**
  - Auto-closing pairs for brackets and quotes
  - Bracket matching and surrounding pairs
  - Automatic indentation rules
  - Code folding support for regions
  - On-enter rules for proper formatting

- **Package.json Improvements**
  - Proper extension metadata
  - Repository information
  - Version bump to 0.1.0
  - First-line shebang support

- **Comprehensive Documentation**
  - Detailed README with examples
  - Changelog with version history
  - Extension manifest properly configured

### Changed
- Completely rewrote syntax grammar for better accuracy
- Enhanced language configuration with professional standards
- Updated README with complete feature documentation

### Fixed
- Improved string escape sequence recognition
- Better bracket pair matching
- More accurate keyword highlighting

## [0.0.1] - Initial Release

- Initial extension setup
- Basic syntax highlighting for keywords and strings
- Basic language configuration template