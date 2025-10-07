
# ✨ Blink Runtime

> A modern, sleek runtime for the Blink programming language — designed for simplicity, speed, and clarity.

---

## 📚 Table of Contents
- [Overview](#-overview)
- [Features](#-features)
- [Core Design](#-core-design)
- [Example Syntax](#-example-syntax)
- [Running Blink](#-running-blink)
- [Development Notes](#-development-notes)
- [Philosophy](#-philosophy)
- [License](#-license)

---

## 🚀 Overview

**Blink Runtime** is the execution layer for **Blink** — a structured, interpreted language built to simplify game development and rapid prototyping.  
It’s written with modularity and readability in mind, following clean design principles.

---

## 🧩 Features

✅ **Lightweight Lexer & Parser** — written in Go for performance and clarity.  
✅ **Structured Syntax** — uses `<` and `>` for section transitions.  
✅ **Hybrid Model** — interpreted scripts running on a compiled C# MonoGame engine.  
✅ **Clean API** — minimal, intuitive, and extendable for future upgrades.  
✅ **Open Development** — designed to evolve with Blink Engine.

---

## 🧠 Core Design

```text
/Blink
 ┣ 📂 lang
 ┃ ┣ 📜 lexer.go
 ┃ ┣ 📜 parser.go
 ┃ ┗ 📜 tokens.go
 ┣ 📂 runtime
 ┃ ┣ 📜 evaluator.go
 ┃ ┗ 📜 environment.go
 ┣ 📜 main.go
 ┗ 📜 README.md
```

- **Lexer** → Converts Blink code into tokens.  
- **Parser** → Translates tokens into an AST (Abstract Syntax Tree).  
- **Evaluator** → Interprets and runs the AST within an isolated runtime environment.

---

## 🧰 Example Syntax

```blink
<game>
  name: "Blink Test"
  version: 0.1
</game>

<object>
  name: "Player"
  position: (10, 5)
</object>
```

---

## ⚙️ Running Blink

```bash
go run main.go blink/test.blink
```

This executes Blink scripts using the runtime’s lexer and parser pipeline.

---

## 🛠️ Development Notes

- Written in **Go** for the language layer.  
- Connected to the **Blink Engine** (MonoGame + C#).  
- Fully open to future modules like scene rendering and prefab handling.  

---

## 🪄 Philosophy

> **Blink Runtime** is built on the idea that programming languages for games should be as creative as the games themselves.  
> No unnecessary syntax, no clutter — just clarity, logic, and flow.

---

## 🧾 License

MIT License © 2025 Fly Pixel
