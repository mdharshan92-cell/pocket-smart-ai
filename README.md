# Pocket Smart AI 📱💻

[![License: MIT](https://shields.io)](https://opensource.org)
[![PRs Welcome](https://shields.io)](http://makeapullrequest.com)

**Pocket Smart AI** is a lightweight, local-first intelligent assistant designed to bring advanced coding capabilities and AI-driven automation directly to your mobile environment or compact hardware (like Termux, Raspberry Pi, or local emulators). Write, debug, and review code entirely offline or through lightweight API wrappers.

---

## ✨ Core Features

* **Local-First Coding:** Run compact GGUF models directly on your hardware without relying on an active internet connection.
* **Smart Code Refactoring:** Inline syntax highlighting, error checking, and boilerplate generation for major programming languages.
* **Terminal Integration:** Built to interface seamlessly with Termux, ADB interfaces, and terminal text editors (like Vim, Nano, or Acode).
* **Privacy by Default:** Zero tracking or external data logging—your prompts and code never leave your physical device.

---

## 🚀 Getting Started

### Prerequisites
Before setting up the project, ensure your environment meets the minimum requirements:
* **Python** ≥ 3.9
* **Termux** (if deploying on Android) or **Raspberry Pi OS / Linux**
* **Git** installed on your terminal

### 🛠️ Installation

1. **Clone the Repository:**
   ```bash
   git clone https://github.com
   cd pocket-smart-ai
   ```

2. **Set Up a Virtual Environment & Dependencies:**
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
   ```

3. **Configure the AI Model:**
   Download a lightweight GGUF coding model (e.g., Qwen-Coder or Llama-3-Instruct-8B-GGUF) and place it inside the `/models` directory:
   ```bash
   mkdir models
   curl -L -o models/coding-model.gguf <your-preferred-model-download-url>
   ```

---

## 💻 Usage

To launch the interactive coding assistant, execute the main entry file:

```bash
python main.py --model ./models/coding-model.gguf
```

### Available CLI Commands

| Command | Action | Example |
| :--- | :--- | :--- |
| `/explain` | Breaks down the logic of a code snippet | `/explain def hello(): print("world")` |
| `/refactor` | Optimizes code for cleanliness and speed | `/refactor < paste code here >` |
| `/review` | Checks code snippets for security vulnerabilities | `/review code.py` |
| `/exit` | Gracefully closes the interactive CLI environment | `/exit` |

---

## 📁 Project Structure

```text
pocket-smart-ai/
├── data/              # Context vectors & local knowledge base
├── models/            # Stored local LLM files (.gguf)
├── src/               # Core execution scripts
│   ├── agent.py       # Logic for AI agent execution
│   └── utils.py       # Terminal UI helpers and text formatters
├── main.py            # CLI application entry point
├── requirements.txt   # Project dependencies
└── README.md          # Project documentation
```

---

## 🤝 Contributing

We welcome community contributions to expand capabilities, patch bugs, and optimize local inference! 

1. **Fork** the repository.
2. Create a new feature branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. **Push** to the branch (`git push origin feature/AmazingFeature`).
5. Open a **Pull Request**.

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.
