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

**unstop Command**: Resume execution after a stop command

```blink
say("this will be executed, no problem")
stop
say("this will not be executed")
say("this will not be executed also")
unstop
say("this will get executed also")
```

**Output:**
```
this will be executed, no problem
stopped
un-stopped
this will get executed also
```

**Advanced Stop/Unstop Example:**
```blink
say("First message")
stop
say("This won't run")
unstop
say("Back to running")
say("Still running")
stop
say("Stopped again - won't run")
unstop
say("Final message after unstop")
```

**Output:**
```
First message
stopped
un-stopped
Back to running
Still running
stopped
un-stopped
Final message after unstop
```

**Important Rules:**
- ✅ **Works only at the top level** - must be at the beginning of a line in main code
- ❌ **Does NOT work inside blocks** - cannot be used inside loops, conditionals, or other blocks
- 🔄 **Multiple cycles supported** - can use stop/unstop multiple times in the same program
- 🚫 **Invalid usage examples:**
  ```blink
  loop 44 {
      say("hey")
      stop    # ❌ This will NOT work - stop doesn't work inside blocks
      say("hey")
  }
  
  if condition {
      stop    # ❌ This will NOT work - stop doesn't work inside blocks
      unstop  # ❌ This will NOT work - unstop doesn't work inside blocks
  }
  ```

**Features:**
- **stop**: Immediate program pause with "stopped" message
- **unstop**: Resume execution with "un-stopped" message
- Simple syntax: just `stop` or `unstop` on their own lines
- Perfect for debugging, testing, and controlled program flow
- Flexible execution control with multiple stop/unstop cycles
- State tracking ensures unstop only works after stop

### 💬 Interactive Input

**ask Command**: Get user input interactively from the terminal

```blink
ask("What's your name?") {
    name = answer
    say("Hello, " + name + "!")
}

ask("What's your favorite color?") {
    color = answer
    say("You chose: " + color)
}

# Improved comparisons - you can now compare without quotes!
if color == Red {
    say("Hey it's red, mine too!")
}

if color == Blue {
    say("Blue is a cool color!")
}

if color == Green {
    say("Green like nature!")
}

say("Nice to meet you, " + name + "!")
remove = name, color
```

**Terminal Output Format:**
```
What's your name?
> Jeff
Hello, Jeff!
What's your favorite color?
> Red
You chose: Red
Hey it's red, mine too!
Nice to meet you, Jeff!
```

**Enhanced Features:**
- Interactive terminal prompts with custom questions
- Automatic `answer` variable creation with user input
- **NEW**: Smart string comparisons without quotes (e.g., `color == Red`)
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

### 🪟 Window System (Game Development)

**window Command**: Create and manage GUI windows with professional text rendering and visual effects

```blink
# Define a window with all available parameters
window test {
    name: 🎮 First Test 🎮 // Custom window title (supports emojis!)
    size: 600x500 // Window size in pixels (width x height)
    resize: true // Allow user to resize window (default: true)
    triangle: true // Render a dynamic triangle that scales with window
    grid: true // Render a dynamic grid overlay that scales with window
    color: FF0000 // Background color in hex format (with or without #)
    icon: icons/game.png // Window icon file path (PNG or JPG)
    selector: true // Enable coordinate selector - right-click for coordinates
    cursor: false // Hide mouse cursor (great for games) (NEW)
    transparency: 0.9 // Window transparency 0.0-1.0 (NEW)
    always_on_top: true // Keep window above all others (NEW)
}

# Define fullscreen windows with graphics, colors, and icons
window game_fullscreen {
    name: 🎮 My Game
    size: fullscreen // Maximized window (shows taskbar)
    resize: false // Lock window size (no resizing allowed)
    triangle: true // Dynamic triangle rendering
    grid: false // No grid overlay
    color: #000080 // Dark blue background
    icon: icons/fullscreen.jpg // Custom icon for fullscreen mode
}

window game_entirescreen {
    name: 🌟 Immersive Game
    size: entirescreen // Exclusive fullscreen (hides everything)
    resize: false // Fixed size window
    triangle: false // No triangle graphics
    grid: true // Grid overlay only
    color: 800080 // Purple background (# is optional)
    icon: icons/immersive.png // Icon for immersive mode
}

# Open the window (still uses 'test' as identifier)
window open test

# Keep window open for 10 seconds
wait 10

# Close the window (still uses 'test' as identifier)
window close test
```

**All Window Options Example:**
```blink
# Create windows with different graphics, colors, icons, and advanced features
window game_window {
    name: 🎮🌈 Game Window
    size: 800x600 // Specific pixel dimensions
    resize: true // User can resize this window
    triangle: true // Render dynamic triangle that scales with window
    grid: true // Render grid overlay behind triangle
    color: #FF6B6B // Light red background
    icon: icons/game.png // Game controller icon
    cursor: false // Hide cursor for immersive gaming
    selector: true // Enable coordinate selection
}

window overlay_window {
    name: 🌟 Transparent Overlay
    size: 600x400 // Fixed dimensions
    resize: false // User cannot resize this window
    triangle: false // No triangle
    grid: true // Grid overlay only
    color: 0066CC // Blue background
    icon: icons/overlay.png // Overlay icon
    transparency: 0.7 // Semi-transparent overlay
    always_on_top: true // Stay above other windows
}

window graphics_demo {
    name: 🔺💚 Graphics Demo
    size: 500x300 // Simple window
    resize: true // Resizable
    triangle: true // Triangle graphics
    grid: false // No grid overlay
    color: 00AA00 // Green background
    icon: icons/triangle.png // Triangle icon
}

window settings_panel {
    name: ⚙️ Settings Panel
    size: 400x300 // Simple window
    resize: true // Resizable
    triangle: false // No triangle
    grid: false // No grid
    color: #800080 // Purple background
    icon: icons/settings.png // Settings gear icon
}

# Open different types of windows
window open game_window       // Opens game window with custom icon
say("Game window opened! Custom game controller icon in taskbar.")

window open editor_window     // Opens editor window with editor icon
say("Editor window opened! Text editor icon visible.")

window open graphics_demo     // Opens graphics demo with triangle icon
say("Graphics demo opened! Triangle icon matches the content.")

window open settings_panel    // Opens settings with gear icon
say("Settings panel opened! Gear icon for easy identification.")

wait 5

# Close all windows
window close game_window
window close editor_window
window close graphics_demo
window close settings_panel
```

**Default Behavior:**
```blink
# Window without custom parameters uses defaults
window simple {
    // No name parameter - will use "simple" as window title
    // No size parameter - will use 400x300 as default size
    // No resize parameter - will default to true (resizable)
    // No triangle parameter - will default to false (no triangle)
    // No grid parameter - will default to false (no grid)
    // No color parameter - will default to black (000000)
    // No icon parameter - will use default system icon
}

window open simple    // Opens 400x300 resizable black window titled "simple"

# You can specify individual parameters
window custom_name {
    name: My Custom Window // Custom name, default size/resize/graphics/color/icon
}

window custom_triangle {
    triangle: true // Default size and name, but with triangle graphics
}

window custom_grid {
    grid: true // Default size and name, but with grid overlay
}

window custom_color {
    color: #FF0000 // Red background, default everything else
}

window custom_icon {
    icon: icons/my_app.png // Custom icon, default everything else
}

window custom_both_graphics {
    triangle: true // Triangle graphics
    grid: true // Grid overlay behind triangle
    color: 0066FF // Blue background
    icon: icons/graphics.jpg // Custom icon for graphics window
}

window custom_size {
    size: 1024x768 // Custom size, uses "custom_size" as title
}
```

### 📝 Text Rendering System (NEW)

**pop Elements**: Add professional text rendering to your windows with TrueType font support

#### ✨ Multiple Pop Elements Support (FIXED)

You can now add **multiple text elements** to a single window! Each pop element renders independently with its own position, size, and content.

**🚀 Performance Improvements:**
- **Fixed rendering issue**: Multiple pop elements now display correctly without overwriting each other
- **Optimized texture management**: Individual textures for each text element instead of full-screen overlays
- **Eliminated lag and glitching**: Smooth rendering performance even with many text elements
- **Proper positioning**: Each text element renders at its exact specified coordinates

```blink
window textDemo {
    name: 📝 Text Rendering Demo
    size: 1200x800
    color: #001122
    
    pop title {
        text("BLINK TEXT SYSTEM")
        size = 50
        middle = x(600), y(150)
    }
    
    pop subtitle {
        text("Professional TrueType Font Rendering")
        size = 25
        middle = x(600), y(200)
    }
    
    pop alphabet {
        text("A, B, C, D, E, F, G, H, I, J, K, L, M, N, O, P, Q, R, S, T, U, V, W, X, Y, Z")
        size = 15
        middle = x(600), y(300)
    }
    
    pop numbers {
        text("0, 1, 2, 3, 4, 5, 6, 7, 8, 9")
        size = 20
        middle = x(600), y(350)
    }
    
    pop symbols {
        text("! @ # $ % ^ & * ( ) - = + [ ] { } | \\ : ; \" ' < > ? / . ,")
        size = 12
        middle = x(600), y(400)
    }
    
    pop math {
        text("Math: 2 + 3 = 5, 10 - 4 = 6, 3 * 7 = 21, 15 / 3 = 5")
        size = 18
        middle = x(600), y(450)
    }
}

window open textDemo
wait 8
window close textDemo
```

#### 🎯 Multiple Pop Elements Example

```blink
window multiTextDemo {
    name: 🎨 Multiple Text Elements
    size: 1000x600
    color: #112233
    
    # Header section
    pop header {
        text("MULTIPLE TEXT DEMO")
        size = 35
        middle = x(500), y(80)
    }
    
    # Left column
    pop leftTitle {
        text("Left Column")
        size = 20
        middle = x(250), y(150)
    }
    
    pop leftContent {
        text("This text appears on the left side")
        size = 12
        middle = x(250), y(200)
    }
    
    # Right column
    pop rightTitle {
        text("Right Column")
        size = 20
        middle = x(750), y(150)
    }
    
    pop rightContent {
        text("This text appears on the right side")
        size = 12
        middle = x(750), y(200)
    }
    
    # Center content
    pop centerInfo {
        text("All text elements render simultaneously!")
        size = 16
        middle = x(500), y(300)
    }
    
    # Footer
    pop footer {
        text("Footer: Multiple pop elements working perfectly")
        size = 10
        middle = x(500), y(500)
    }
}

window open multiTextDemo
wait 10
window close multiTextDemo
```

#### Text Element Parameters

| Parameter | Type | Description | Example |
|-----------|------|-------------|---------|
| `text()` | String | Text content to display | `text("Hello World")` |
| `size` | Number | Text size (1-100 scale) | `size = 25` |
| `middle` | Coordinates | Center position of text | `middle = x(400), y(300)` |

#### Supported Characters

**Complete ASCII Character Set:**
- **Letters**: A-Z, a-z (uppercase and lowercase)
- **Numbers**: 0-9 (all digits)
- **Punctuation**: `. , ! ? : ; " ' ` (common punctuation)
- **Math Symbols**: `+ - * / = < > ( ) [ ] { }` (mathematical operations)
- **Special Characters**: `@ # $ % ^ & _ | \ ~ ` (programming symbols)
- **Spaces**: Full space and formatting support

**Font Features:**
- **TrueType Rendering**: Professional, smooth text rendering
- **Scalable**: Text scales smoothly from size 1 to 100
- **Anti-aliased**: Smooth edges for professional appearance
- **Centered Positioning**: Text centers perfectly at specified coordinates
- **Window Scaling**: Text scales proportionally when window is resized

### 📏 Complete Window Parameters Reference

| Parameter | Type | Default | Description | Example |
|-----------|------|---------|-------------|---------|
| `name` | String | window identifier | Display name in title bar | `name: 🎮 My Game 🎮` |
| `size` | String | `400x300` | Window dimensions or fullscreen | `size: 1920x1080` |
| `resize` | Boolean | `true` | Allow user to resize window | `resize: false` |
| `color` | Hex Color | `#000000` | Background color | `color: #ff3300` |
| `icon` | File Path | system default | Window icon (PNG/JPG) | `icon: icons/app.png` |
| `triangle` | Boolean | `false` | Show animated triangle | `triangle: true` |
| `grid` | Boolean | `false` | Show grid overlay | `grid: true` |
| `selector` | Boolean | `false` | Enable coordinate selector | `selector: true` |
| `cursor` | Boolean | `true` | Show mouse cursor | `cursor: false` |
| `transparency` | Float | `1.0` | Window transparency (0.0-1.0) | `transparency: 0.8` |
| `always_on_top` | Boolean | `false` | Keep window above others | `always_on_top: true` |

### 🎨 Size Options

- **Specific Dimensions**: `800x600`, `1920x1080`, `1100x700`
- **Fullscreen**: `fullscreen` (maximized with taskbar visible)
- **Entirescreen**: `entirescreen` (exclusive fullscreen, hides everything)

### 🎯 Coordinate System

- **Origin**: Top-left corner (0, 0)
- **X-axis**: Left to right (positive direction)
- **Y-axis**: Top to bottom (positive direction)
- **Text Positioning**: `middle = x(xPos), y(yPos)` centers text at coordinates
- **Coordinate Selector**: Right-click when `selector: true` to get pixel coordinates

### 🎨 Color Format

Colors support hex format with or without `#`:
- `color: #ff0000` (Red)
- `color: #00ff00` (Green)
- `color: #0000ff` (Blue)
- `color: ff3300` (Orange - # optional)
- `color: #ffffff` (White)
- `color: #000000` (Black)
```

**Features:**
- **GUI Window Creation**: Real graphical windows that appear on your desktop
- **Custom Window Titles**: Set beautiful display names with `name:` parameter
- **Custom Window Sizes**: Set initial window dimensions with `size:` parameter
- **Resize Control**: Lock or allow window resizing with `resize:` parameter
- **Dynamic Graphics**: Render interactive graphics with `triangle:` and `grid:` parameters
- **Custom Background Colors**: Set any background color with `color:` parameter
- **Custom Window Icons**: Set window icons with `icon:` parameter
- **Coordinate Selector**: Right-click coordinate detection with `selector:` parameter
- **Cursor Control**: Show/hide mouse cursor with `cursor:` parameter (NEW)
- **Window Transparency**: Adjustable transparency with `transparency:` parameter (NEW)
- **Always On Top**: Keep window above others with `always_on_top:` parameter (NEW)
- **Grid Overlay System**: Dynamic grid that scales with window size
- **Fullscreen Modes**: Support for both fullscreen and entirescreen modes
- **Emoji Support**: Use emojis and special characters in window titles
- **Flexible Naming**: Commands use simple identifiers, display shows custom names
- **Size Formats**: 
  - **Pixel dimensions**: "widthxheight" format (e.g., "800x600", "1024x768")
  - **fullscreen**: Maximized window that shows taskbar/dock
  - **entirescreen**: Exclusive fullscreen that hides everything (press ESC to exit)
- **Resize Options**: 
  - **resize: true**: Allow user to resize window (default behavior)
  - **resize: false**: Lock window to fixed size, prevent resizing
- **Graphics Options**: 
  - **triangle: true**: Render a colorful triangle that dynamically scales with window size
  - **triangle: false**: No triangle graphics (default behavior)
  - **grid: true**: Render a semi-transparent grid overlay that scales with window size
  - **grid: false**: No grid overlay (default behavior)
- **Color Options**: 
  - **color: RRGGBB**: Set background color using 6-digit hex format (e.g., "FF0000" for red)
  - **color: #RRGGBB**: Hex format with optional # prefix (e.g., "#00FF00" for green)
  - **Default**: Black background (000000) if no color specified
- **Icon Options**: 
  - **icon: path/to/file.png**: Set window icon using PNG image file
  - **icon: path/to/file.jpg**: Set window icon using JPG/JPEG image file
  - **Relative paths**: Icons relative to blink/ directory (e.g., "icons/game.png")
  - **Automatic loading**: Images are loaded and processed automatically
  - **Default**: System default icon if no icon specified
- **Cursor Options**: 
  - **cursor: true**: Show mouse cursor when over window (default behavior) (NEW)
  - **cursor: false**: Hide mouse cursor when over window (perfect for games) (NEW)
- **Transparency Options**: 
  - **transparency: 1.0**: Fully opaque window (default behavior) (NEW)
  - **transparency: 0.5**: 50% transparent window (NEW)
  - **transparency: 0.0**: Fully transparent window (invisible) (NEW)
  - **Range**: Values automatically clamped between 0.0 and 1.0 (NEW)
- **Always On Top Options**: 
  - **always_on_top: false**: Normal window behavior (default) (NEW)
  - **always_on_top: true**: Keep window above all other windows (NEW)
- **Coordinate Selector Options**: 
  - **selector: false**: No coordinate detection (default behavior)
  - **selector: true**: Enable right-click coordinate detection
- **Layered Rendering**: Proper rendering order - background color → grid → triangle → future graphics
- **Smart Defaults**: 400x300 pixels if no size specified, identifier as title if no name, resizable by default, no graphics by default, black background by default, system icon by default
- **Automatic Centering**: Normal windows automatically center on screen based on their size
- **Dynamic Scaling**: All graphics automatically resize and maintain proportions when window is resized
- **Transparency Support**: Grid uses semi-transparent rendering for professional overlay effect (NEW)
- **Window Lifecycle Management**: Open and close windows programmatically
- **Professional Window Behavior**: Proper rendering and user experience with OpenGL graphics
- **Game Development Ready**: Perfect foundation for building games with layered graphics rendering and full window control
- **Multiple Windows**: Support for creating and managing multiple windows with different sizes, modes, resize settings, and graphics combinations
- **Error Handling**: Prevents opening undefined windows or duplicate operations
- **Cross-Platform**: Works on Windows, macOS, and Linux with OpenGL support
- **Future Extensible**: Ready for more graphics layers, input handling, and game objects

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
- ✅ **Smart string comparisons without quotes (NEW)**
- ✅ **Clean terminal formatting for user interaction**
- ✅ **Random selection with `random` command**
- ✅ **Equal probability distribution for all options**
- ✅ **GUI Window System for game development**
- ✅ **Custom window titles with emoji support**
- ✅ **Custom window sizes with flexible dimensions**
- ✅ **Window resize control (lock or allow resizing)**
- ✅ **Dynamic triangle graphics with automatic scaling**
- ✅ **Dynamic grid overlay system with transparency**
- ✅ **Custom background colors with hex support**
- ✅ **Custom window icons with PNG/JPG support**
- ✅ **Coordinate selector with right-click detection**
- ✅ **Cursor control for immersive gaming (NEW)**
- ✅ **Window transparency for modern UI effects (NEW)**
- ✅ **Always on top functionality for overlays (NEW)**
- ✅ **Layered graphics rendering system**
- ✅ **Fullscreen and entirescreen modes for immersive experiences**
- ✅ **Flexible window naming system**
- ✅ **Real graphical windows with OpenGL rendering**
- ✅ **Automatic window centering based on size**
- ✅ **Window lifecycle management (open/close)**
- ✅ **Program control with `stop` and `unstop` commands**
- ✅ **Flexible execution pause and resume for debugging**
- ✅ **Multiple stop/unstop cycles support**
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
- **game_dev.blink**: Game development features and window system examples
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
