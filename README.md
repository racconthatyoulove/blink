# 🚀 The Blink Programming Language

> **✅ Stable Release ✅**
> 
> 🎉 **Blink is fully functional and ready to use!** 🎉
> 
> - **Complete core language** with all essential features implemented
> - **Production-ready** interpreter with robust execution
> - **Zero dependencies** - runs with just Go
> - **Clean, simple syntax** perfect for learning and scripting

## 📖 What is Blink?

Blink is a **simple, powerful programming language** designed with **clarity and ease-of-use** in mind. Built for learning, scripting, and experimentation, Blink provides clean syntax and essential programming constructs without unnecessary complexity.

### ✨ Key Highlights

- 🧠 **Beginner-Friendly**: Minimal syntax with maximum expressiveness
- ⚡ **High Performance**: Go-powered backend for fast execution
- 🔧 **Complete Core**: All essential programming features implemented
- 🎨 **Clean Design**: Simple, readable code structure
- ✅ **Production Ready**: Stable, tested, and reliable

## 🏗️ Core Language Features

### 📊 Data Types & Variables

**Numbers** (Floating-Point Precision)
- Full floating-point arithmetic (64-bit precision)
- Supports integers and decimals: `42`, `3.14159`, `-5.5`
- Perfect for mathematical calculations and precise computations

**Strings** (Text & Messages)
- Enclosed in double quotes: `"Hello, World!"`
- Perfect for user messages, data labels, and text processing
- Seamless concatenation with other types

**Booleans** (True/False Logic)
- Simple `true`/`false` values for logical operations
- Essential for conditions and program flow control
- Automatic conversion to strings for display

### 🔢 Arithmetic Operations

**Operators**: `+` (addition), `-` (subtraction), `*` (multiplication), `/` (division)

```blink
# Basic arithmetic examples
result = 10 + 5      # Addition: 15
result = 10 - 3      # Subtraction: 7
result = 4 * 6       # Multiplication: 24
result = 15 / 3      # Division: 5.0
```
**Features:**
- Full floating-point precision for accurate calculations
- Proper operator precedence (`*` and `/` before `+` and `-`)
- Perfect for mathematical computations and data processing

### 🔤 Special Features

**Flexible Variable Names**
```blink
# Variables can have numeric names
1 = "first"
2 = "second"
say("Sequence: " + 1 + ", " + 2)
```

**Mixed-Type Operations**
```blink
# Seamless string + number + boolean concatenation
name = "Alice"
age = 25
active = true
say("User: " + name + ", Age: " + age + ", Active: " + active)
```

### 💬 Comments & Documentation

**Multiple Comment Styles**
```blink
# Shell-style comments
// C-style comments

# Both styles supported for flexibility
```

### 🎯 Control Flow

**If-Else Statements**
```blink
# Simple if statement
if condition {
    # Execute if true
}

# If-else statement
if score >= 50 {
    say("Grade: A (Excellent!)")
} else {
    say("Grade: B (Could Be Better)")
}

# Another simple example
if temperature >= 0 {
    say("Above freezing")
} else {
    say("Below freezing")
}
```

**Loop Statements**
```blink
# Basic loop with automatic iteration counter
loop 3 {
    say("hello")
    say(i)  # 'i' is automatically created and incremented (0, 1, 2)
}

# Loop with variables
count = 5
loop count {
    say("Iteration: " + i)
}

# Nested loops support
loop 2 {
    say("Outer loop: " + i)
    loop 3 {
        say("  Inner loop: " + i)
    }
}
```

**Control Flow Features**
- Support for `if` statements with optional `else` blocks
- Clean, simple conditional logic with smart syntax
- Focus on single else - keep it simple and readable
- Proper block parsing with brace support
- **Loop functionality** with automatic iteration counter
- Supports both numeric literals and variables as loop counts
- Nested loops support with proper variable scoping
- Zero iteration handling (loop 0 skips execution)
- Error handling for invalid counts and negative numbers
### ⚖️ Comparison Operators

**Complete Set**: `==`, `!=`, `>`, `<`, `>=`, `<=`

```blink
# Comparison examples
result = 10 == 10    # Equality: true
result = 5 != 3      # Inequality: true
result = 7 > 5       # Greater than: true
result = 4 <= 10     # Less than or equal: true
```

**Features:**
- Works with numbers, strings, and booleans
- Returns proper boolean values
- Essential for all conditional logic

### 🔗 String Concatenation

**Smart Concatenation**: Automatically combines strings, numbers, and booleans

```blink
name = "Alice"
age = 25
active = true

say("User: " + name)                    # Display user name
say("Age: " + age + " years")           # Show age with text
say("Status: " + active)                # Boolean to text
```

### 🎯 Expression Evaluation

**Parentheses Support**: Control evaluation order for complex calculations

```blink
# Complex expressions
result = (10 + 5) * 2        # Result: 30
valid = (age >= 18) == true  # Boolean logic
final = (base + bonus) / 2   # Mathematical operations
```

### 💬 Output System

**say() Function**: Universal output for debugging and user feedback

```blink
say("Program Started!")                 # Simple messages
say("User " + name + " logged in")      # Dynamic content
say("Values: " + x + ", " + y)          # Debug information
say("Result: " + final_result)          # Program results
```

### ⏱️ Timing Control

**wait Command**: Pause execution for precise timing control

```blink
say("This message appears immediately")
wait 1.5
say("This message appears after 1.5 seconds")

# Examples with different durations
wait 0.5    # Wait half a second
wait 2.0    # Wait 2 seconds  
wait 1.322  # Wait 1.322 seconds (precise timing)
```

**Features:**
- Supports decimal precision for exact timing
- Perfect for creating delays, countdowns, and timed sequences
- Simple syntax: `wait <duration>` where duration is in seconds
- Execution pauses at the wait command before continuing

### 🛑 Program Control

**stop Command**: Immediately halt program execution

```blink
say("this will run with no problem at all")
stop
say("this will not be runned")
x = "hello"
say("this will also not run")
```

**Output:**
```
this will run with no problem at all
stopped
```

**Important Rules:**
- ✅ **Works only at the top level** - must be at the beginning of a line in main code
- ❌ **Does NOT work inside blocks** - cannot be used inside loops, conditionals, or other blocks
- 🚫 **Invalid usage examples:**
  ```blink
  loop 44 {
      say("hey")
      stop    # ❌ This will NOT work - stop doesn't work inside blocks
      say("hey")
  }
  
  if condition {
      stop    # ❌ This will NOT work - stop doesn't work inside blocks
  }
  ```

**Features:**
- Immediate program termination with "stopped" message
- Simple syntax: just `stop` on its own line
- Perfect for debugging, testing, and controlled program termination
- All code after `stop` is completely ignored and never executed

### 💬 Interactive Input

**ask Command**: Get user input interactively from the terminal

```blink
ask("What's your name?") {
    name = answer
    say("Hello, " + name + "!")
}

ask("What's your age?") {
    age = answer
    say("You are " + age + " years old.")
}

say("Nice to meet you, " + name + "!")
remove = name, age
```

**Terminal Output Format:**
```
What's your name?
> Jeff
Hello, Jeff!
What's your age?
> 25
You are 25 years old.
Nice to meet you, Jeff!
```

**Features:**
- Interactive terminal prompts with custom questions
- Automatic `answer` variable creation with user input
- Clean formatting with question on one line, input on next with ">" prompt
- Block execution after receiving input
- Works seamlessly with loops, conditionals, and other language features
- Perfect for creating interactive programs and user-driven applications

### 🎲 Random Selection

**random Command**: Randomly select one option from a list of choices

```blink
random(apple, banana, cherry, grape) {
    fruit = chosen
    say("Randomly selected: " + fruit)
}

random(1, 2, 3, 4, 5, a, 6, b, c, %, **, 444a) {
    result = chosen
    say("Random choice: " + result)
    wait 2
    remove = result
}

say("The fruit was: " + fruit)
remove = fruit
```

**Example Output:**
```
Randomly selected: banana
Random choice: **
The fruit was: banana
```

**Features:**
- Random selection from any number of options
- Supports numbers, letters, symbols, and combinations
- Equal probability for all options regardless of type
- Automatic `chosen` variable creation with selected option
- Block execution after random selection
- Perfect for games, decision making, and randomized content
- Works seamlessly with loops, conditionals, and other language features

### 🛡️ Variable Management & Protection

**Variable Overwrite Protection**: Prevents accidental variable reassignment with helpful guidance

```blink
x = "hello"
y = "sir"
say(x + " " + y)

# Trying to overwrite existing variables will show helpful error:
# x = "new value"  # Error with instructions on how to remove first
```

**remove Command**: Clean variable removal for intentional reassignment

```blink
# Remove single or multiple variables
remove = x
remove = x, y, z

# After removal, variables can be reassigned
x = "heyyyy"
y = "woow"
say(x + " " + y)
```

**Features:**
- **Smart Protection**: Prevents accidental variable overwrites
- **Helpful Errors**: Clear instructions on how to remove variables
- **Batch Removal**: Remove multiple variables in one command
- **Extensible Design**: Built to support future features like windows
- **User-Friendly**: Provides feedback on successful removals

### 🎯 Practical Examples

**If-Else Logic Example**
```blink
score = 85

if score >= 80 {
    say("Grade: A (Great job!)")
} else {
    say("Grade: B (Keep practicing!)")
}
```

**Simple Conditional Example**
```blink
temperature = -5

if temperature >= 0 {
    say("Temperature is above freezing")
} else {
    say("Temperature is below freezing")
}
```

**Complex Expression Example**
```blink
# Parentheses and complex expressions
num1 = 15
num2 = 20
result = (num1 + 5) == num2
say("Mathematical check: (15 + 5) == 20 is " + result)
```

**Timed Sequence Example**
```blink
# Countdown with timing control
say("Starting countdown...")
wait 1.0
say("3...")
wait 1.0
say("2...")
wait 1.0
say("1...")
wait 1.0
say("Go!")
```

**Variable Management Example**
```blink
# Create variables
x = "hello"
y = "sir"
say(x + " " + y)

# Remove and reassign
remove = x, y
x = "heyyyy"
y = "woow"
say(x + " " + y)

# Output:
# hello sir
# Removed variables: x, y
# heyyyy woow
```

**Loop Examples**
```blink
# Simple counting loop
loop 5 {
    say("Count: " + i)
}
# Output: Count: 0, Count: 1, Count: 2, Count: 3, Count: 4

# Loop with conditional logic
loop 3 {
    if i >= 2 {
        say("High iteration: " + i)
    } else {
        say("Low iteration: " + i)
    }
}

# Variable-controlled loop
max_iterations = 4
loop max_iterations {
    say("Processing item " + i)
}
```

**Interactive Program Example**
```blink
# Interactive greeting program
ask("What's your name?") {
    name = answer
    say("Hello, " + name + "!")
}

ask("How old are you?") {
    age = answer
    if age >= 18 {
        say("You're an adult!")
    } else {
        say("You're still young!")
    }
}

say("Nice chatting with you, " + name + "!")
remove = name, age
```

**Random Game Example**
```blink
# Simple random game
say("Welcome to the Random Adventure!")

random(forest, cave, mountain, beach) {
    location = chosen
    say("You find yourself in a " + location)
}

random(treasure, monster, friend, nothing) {
    encounter = chosen
    if encounter == treasure {
        say("You found a treasure chest!")
    } else {
        say("You encountered: " + encounter)
    }
}

say("Your adventure in the " + location + " is complete!")
remove = location, encounter
```

## 🎯 Language Philosophy

**Simplicity First**
- No complex syntax - just essential features
- Easy to learn, powerful to use

**What Blink Does Well**
- ✅ Variables and data types (numbers, strings, booleans)
- ✅ Variable overwrite protection with helpful error messages
- ✅ Clean variable removal with `remove` command
- ✅ Arithmetic operations with full precision
- ✅ String concatenation and mixed-type operations
- ✅ Comparison operators (all 6 types)
- ✅ Simple if-else statements with clean syntax
- ✅ Single else blocks for clear, readable logic
- ✅ **Loop statements with automatic iteration counter**
- ✅ **Nested loops with proper variable scoping**
- ✅ **Interactive input with `ask` command**
- ✅ **Clean terminal formatting for user interaction**
- ✅ **Random selection with `random` command**
- ✅ **Equal probability distribution for all options**
- ✅ **Program control with `stop` command**
- ✅ **Immediate execution termination for debugging**
- ✅ Parentheses and expression evaluation
- ✅ Flexible variable naming (including numeric names)
- ✅ Dual comment styles (# and //)
- ✅ Robust output with `say()` function
- ✅ Precise timing control with `wait` command

**What Blink Doesn't Do**
- ❌ No else-if statements (by design - keep it simple)
- ❌ No complex nested conditionals (focus on clarity)
- ❌ No functions (keep it simple)
- ❌ No complex data structures (arrays, objects)

Blink is perfect for **learning programming concepts**, **simple calculations**, **data processing**, and **scripting tasks** where clarity and simplicity matter most.

## 🚀 Getting Started

### 📋 Requirements
- Go 1.21 or higher
- Any text editor or IDE
- Terminal/Command prompt access

### 🏃 Running Blink Programs

```bash
# Command format
go run ./Blink/main.go <your_file>.blink

# Example
go run ./Blink/main.go ./Blink/blink/test.blink
```

**File Extension**: `.blink` (recommended for syntax highlighting)

### 📚 Learning Resources
- **test.blink**: Complete language documentation with examples
- **This README**: Comprehensive feature overview

## 🏆 Why Choose Blink?

### ✨ Developer Experience
- 🧠 **Learning-Focused**: Gentle learning curve for new programmers
- 📖 **Readable**: Clean, intuitive syntax that's easy to understand
- 🚀 **Productive**: Get programs up and running quickly
- 🔧 **Flexible**: Powerful enough for complex applications
- 🛡️ **Reliable**: Robust error handling and type safety

### 💻 Programming Focus
- ⚡ **Performance**: Fast execution for smooth program operation
- 🎨 **Expressiveness**: Natural syntax for clear logic
- 🔄 **Iteration**: Quick compile-test cycles for rapid development
- 📚 **Learning**: Perfect for education and experimentation
- 🌟 **Innovation**: Modern language features with classic simplicity

## 🎊 Conclusion

**Blink** represents a modern approach to programming language design - combining the **simplicity** of scripting languages with the **power** and **performance** needed for real applications.

Whether you're a **beginner** taking your first steps into programming or an **experienced developer** looking for a clean, efficient language for prototyping and development, Blink provides the perfect balance of **accessibility** and **capability**.

🌟 **Start your programming journey with Blink today!** 🌟

**Happy Coding! 💻✨**

---

*Blink Programming Language - Making coding accessible and enjoyable for everyone.*
