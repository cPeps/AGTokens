<p align="center">
  <img src="docs/banner.svg" alt="AG. AI TOKENS" width="100%">
</p>

<p align="center">
  <a href="https://github.com/cPeps/AGTokens/releases/latest"><img src="https://img.shields.io/github/v/release/cPeps/AGTokens?label=version&color=7c3aed&style=for-the-badge" alt="Version"></a>
  <img src="https://img.shields.io/badge/Windows-10%20%7C%2011-0078D6?style=for-the-badge&logo=windows&logoColor=white" alt="Windows 10/11">
  <img src="https://img.shields.io/badge/AI-local%20%26%20free-16a34a?style=for-the-badge" alt="Local AI">
  <img src="https://img.shields.io/badge/MCP-supported-22d3ee?style=for-the-badge" alt="MCP">
  <a href="https://github.com/cPeps/AGTokens/releases/latest"><img src="https://img.shields.io/github/downloads/cPeps/AGTokens/total?label=downloads&color=f59e0b&style=for-the-badge" alt="Downloads"></a>
</p>

<p align="center">
  <b>🦁 Built for the <i>Leone San Marco</i> community and the game it is developing.</b><br>
  <sub>by DevPeps</sub>
</p>

---

## ⚡ In one sentence

**AG. AI TOKENS** gives your AI **project memory, code maps, answer verification and automatic fixes**, so it stops forgetting, stops inventing files and stops wasting tokens. Drop your project folder on the icon and **you're done**: it updates itself, shows everything live, and reopens by itself whenever you open your AI.

<p align="center">
  <img src="docs/ai-al-lavoro.png" alt="AGTokens while the AI is working" width="90%">
  <br><sub>AGTokens while Qwen 3.6 (running in Bionic) reads a message: everything live, no keys to press.</sub>
</p>

---

## 😤 The problem it solves

Anyone working with AI models (especially **free models running on your own PC**) knows these problems:

| Problem | What AGTokens does |
|---|---|
| 🧠 **The AI forgets** what you decided yesterday | Project memory, work state and lessons learned: every AI finds them again in every session |
| 🔍 **It re-reads the whole project** and burns thousands of tokens | Code maps and tools that read **only the lines that matter** (on a real project: **‑95% tokens** per new chat, measured with the model's own tokenizer) |
| 🤥 **It invents** files, lines, functions, "tests pass" | Every answer is **checked against the real project** |
| 💥 *"The selected model ran out of context space"* | AGTokens **reloads the model the right way by itself** (Bionic / LM Studio) |
| ✂️ *"Unterminated string in JSON"*, truncated answers | Files are written **in parts**, truncated answers are completed |
| 🔁 The AI **loops** or answers **empty** | Loops are stopped, empty answers from "thinking" models are recovered |
| 📁 **Duplicate** files, `(1)` copies, missing files | **File check** as soon as you open the project: errors, duplicates, missing files |

---

## ✨ Key features

- 🖥️ **One live, colorful window**: what the AI is doing *right now* (reading your message, writing the answer, tokens per second), how much context it uses, tokens read and written, every event explained. **No keys to press.**
- 🤖 **Sees everything the model does**: with Bionic and LM Studio it reads the model's own log, so even the app's built‑in chat is counted.
- 🔧 **Fixes the model by itself**: context split across parallel requests or too small → it reloads the model when idle (never in the middle of an answer).
- 🧩 **MCP tools** for AIs that support them: find code, read only the useful lines, precise edits (`agt_edit`), run the **real tests** (`agt_test`), syntax check after every change.
- 🛡️ **Answer verification**: invented files, wrong line numbers, functions that don't exist, "lazy" code (`// ... rest unchanged`).
- 🔍 **Project file check**: scripts with errors, files referenced but missing, duplicates, old copies.
- 🔁 **Reopens by itself**: when you open your AI, AGTokens reopens on the right project.
- 💾 **Memory is never lost**: if you delete AGTokens' files by mistake, they come back with their content.
- 🎮 **Made for game developers**: Unreal, Unity, Godot and **Blender scenes** read without opening binary files.
- 🔔 **Windows notifications** for what matters.
- ⬆️ **Automatic, signed updates**: you never download anything twice.

<p align="center">
  <img src="docs/finestra.png" alt="The AGTokens window" width="90%">
  <br><sub>Tokens read and written by the model, context in use, connected tools, file check and project memory.</sub>
</p>

---

## 🤝 Works with

| Type | AI | How it connects |
|---|---|---|
| 💻 **On your PC (free, offline)** | **Bionic**, LM Studio, Ollama, Jan, GPT4All, llama.cpp, vLLM, KoboldCpp, Unsloth Studio | MCP tools + local proxy + reading the model's log |
| 🧑‍💻 **Agents** | Claude Code, Cursor, Windsurf, Cline, Gemini CLI, AnythingLLM | MCP tools (configured automatically) |
| 💬 **Chats** | Claude Desktop, ChatGPT, Gemini, DeepSeek, Mistral, Grok… | MCP where available, otherwise the project context is ready in your clipboard + automatic check of the answers you copy |

AGTokens **recognizes which AI you are using** and adapts its rules to that AI's known weaknesses (small models, reasoning models, chats without file access…).

---

## 🧭 How it works

```mermaid
flowchart LR
    U([👤 You]) -- drop the folder --> A[⚡ AGTokens]
    A -- reads the project --> M[(🗺️ Maps · 🧠 Memory<br/>🔍 File check)]
    AI[🤖 Your AI<br/>Bionic · LM Studio · Claude · Cursor…] -- MCP tools --> A
    A -- only the useful lines --> AI
    AI -- answer --> V{🛡️ Check}
    V -- invented? --> W[⚠️ Tells you right away]
    V -- all good --> OK[✅ Memory updated]
    L[(📜 Model log)] -- real tokens, context --> A
    A -- context full? --> F[🔧 Reloads the model by itself]
```

---

## 🚀 Tutorial: from zero to ready in 2 minutes

1. **Download** the latest version from [**Releases**](https://github.com/cPeps/AGTokens/releases/latest) → `AGTokens_v2.7.0.zip`.
2. **Extract** the zip anywhere (for example on your Desktop).
3. **Drag your project folder** onto `AGTokens.exe`.
4. On first launch, paste your **activation key** (see below how to get one).
5. **That's it.** Open your AI (Bionic, LM Studio, Claude…) and work as usual:
   - AIs with MCP tools get them **automatically**;
   - for web chats the project context is **already in your clipboard**: paste it once at the start;
   - next time you open your AI, **AGTokens reopens by itself**.

> [!TIP]
> With **Bionic / LM Studio** there is nothing to configure: AGTokens connects its tools, starts the model server if it is off, and fixes the context if the model was loaded badly.

> [!NOTE]
> The program interface is currently in **Italian**. Everything is automatic and the window is easy to read; an English interface is planned.

---

## 🔑 Activation key

AGTokens works with a **personal key** (one key = one PC).

- 🆓 **Keys are free today**: request one by opening a [**key request**](https://github.com/cPeps/AGTokens/issues/new?template=richiesta_chiave.yml).
- 🔮 In the future keys may become **paid serial keys** or stay **free on request**: key holders will be notified directly inside the program window.
- ⏳ The window always shows your key status and the time left.

> [!IMPORTANT]
> Never post personal data (email, phone) in public issues: just leave a nickname (Discord/Telegram) so you can be contacted privately.

---

## 🛡️ "Windows protected your PC"? Here's why

`AGTokens.exe` **is not digitally signed**: a code‑signing certificate costs hundreds of euros per year and the project is free for now. That's why **Windows SmartScreen** may show a warning on first launch.

To run it: click **"More info" → "Run anyway"**.

To make sure you have the original file:
- download it **only** from this [Releases](https://github.com/cPeps/AGTokens/releases/latest) page;
- compare the SHA‑256 fingerprint with the one in the release's `.sha256` file:
  ```powershell
  Get-FileHash .\AGTokens_v2.7.0.zip -Algorithm SHA256
  ```
- AGTokens itself checks that it is an **original copy**: a modified copy is blocked.

---

## 🔒 Privacy

- Your projects, your code and your conversations with the AI **stay on your PC**. The proxy accepts **local models only**.
- The only internet connection is the **license check**: the server receives only the key, an anonymous PC fingerprint (not reversible) and the program version. No files, no names, no IP addresses stored.

---

## ❓ FAQ

<details>
<summary><b>Do I need to press keys or configure anything?</b></summary>
No. You just read the window: everything updates by itself. The only thing you may ever type is the API key of a protected model (e.g. Unsloth Studio), and the input line opens by itself.
</details>

<details>
<summary><b>Does it work offline?</b></summary>
Yes, with local models. The license stays valid offline for the period set by the owner (usually 24 hours), then a connection is needed for the next check.
</details>

<details>
<summary><b>How many tokens do I really save?</b></summary>
AGTokens measures it with your model's tokenizer: on its own code (≈170,000 tokens) the context it prepares is ≈8,800 tokens, i.e. <b>‑95% for every new chat</b>. On tiny projects the saving is small, and the window tells you so honestly.
</details>

<details>
<summary><b>My antivirus flags it.</b></summary>
This happens with unsigned single‑file programs. Download it only from Releases and verify the SHA‑256 fingerprint. Feel free to open a <a href="https://github.com/cPeps/AGTokens/issues/new?template=bug_report.yml">report</a>.
</details>

<details>
<summary><b>Is the source code available?</b></summary>
No: AGTokens is proprietary software, free to use with a key. Here you'll find the program, the guide and the channel for reports and ideas.
</details>

---

## 🐞 Bugs, ideas and feedback

Your feedback makes AGTokens better:

- 🐞 [**Report a bug**](https://github.com/cPeps/AGTokens/issues/new?template=bug_report.yml)
- 💡 [**Suggest an idea**](https://github.com/cPeps/AGTokens/issues/new?template=feature_request.yml)
- 🔑 [**Request a key**](https://github.com/cPeps/AGTokens/issues/new?template=richiesta_chiave.yml)
- 💬 [**Discussions & questions**](https://github.com/cPeps/AGTokens/discussions)

---

## 📋 Requirements

- Windows 10 or 11 (64‑bit)
- An AI: **Bionic** or **LM Studio** with a local model is recommended (free); Claude, ChatGPT, Cursor and others work too
- Optional: Blender (to read `.blend` scenes), Node.js (more accurate JavaScript checks)

---

<p align="center">
  🦁 Made with passion for the <b>Leone San Marco</b> community and its game.<br>
  <sub>© 2026 DevPeps — proprietary software, free to use. See <a href="LICENSE">LICENSE</a>.</sub>
</p>
