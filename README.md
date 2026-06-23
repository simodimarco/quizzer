# quizzer

**Your private, local-first companion for exam preparation.**

`quizzer` is a lightweight, standalone web application that transforms your study notes into interactive quizzes or flashcards. Designed for students and educators, it prioritizes privacy and portability by performing all data processing locally in your browser.

## ✨ Core Capabilities

### 🔒 Privacy First
- **100% Local Processing:** Your data never leaves your device. No servers, no databases, no cloud uploads.
- **No Tracking:** The app does not use cookies or tracking scripts.

### 🎓 Dual Study Modes
The app automatically switches modes based on your data structure:
- **Quiz Mode:** Multiple-choice questions with instant feedback and score tracking.
- **Flashcard Mode:** 3D flipping cards for active recall (perfect for definitions and terminology).

### 🔄 Seamless Data Flow
- **Flexible Input:** Drag & drop `.yaml` files, upload them, or paste YAML text directly into the app.
- **Integrated Live Editor:** Fix typos or update questions on the fly without restarting your session.
- **Easy Export:** Download your modified quiz data back to a YAML file or copy it to your clipboard.

### 📱 PWA Experience
`quizzer` is a Progressive Web App (PWA), meaning you can "install" it on your desktop or mobile device for a native app experience and use it offline.
See your browser specific documentation to know how to install it as a webapp.

## 🚀 Getting Started

### Download from code repository
1. **Download** the `quizzer.html` file from this repository.
2. **Open** it in any modern web browser (Chrome, Firefox, Safari, Edge).
3. **Load Data:** Drag a `.yaml` file onto the screen or use the upload button.
4. **(Optional) Install:** Click the "Install" icon in your browser's address bar to add `quizzer` to your home screen/applications.

### Direct access on web
This app is also hosted on github pages, yo can just open it from the following link:
[https://simodimarco.github.io/quizzer/quizzer.html](https://simodimarco.github.io/quizzer/quizzer.html)

## 📊 Data Schema (The "Database")

The application uses YAML format for input data for its simplicity and human as well as machine readability.

### 📝 The Quiz Pattern
Include an `opzioni` block to trigger **Quiz Mode**.

```yaml
- id: 1
  domanda: "What is the main advantage of this app?"
  opzioni:
    a: "It requires a server"
    b: "It is standalone and private"
    c: "It only works with JSON"
  risposta_corretta: "b"
  note: "you know that by reading README.md file in github repository."
```

### 🗂️ The Flashcard Pattern
Omit `opzioni` and provide a `risposta` to trigger **Flashcard Mode**.

```yaml
- id: 1
  domanda: "What is a Progressive Web App?"
  risposta: "A type of application software delivered through the web, built using common web technologies including HTML, CSS, and JavaScript."
```

### Field Definitions
| Field | Requirement | Description |
| :--- | :--- | :--- |
| `id` | Required | A unique identifier for the question. |
| `domanda` | Required | The question or prompt text. |
| `opzioni` | Optional | A map of choices (a, b, c, d). Triggers Quiz Mode. |
| `risposta_corretta`| Required (Quiz) | The key of the correct option (e.g., "a"). |
| `risposta` | Required (Flash) | The answer text. Triggers Flashcard Mode. |
| `note` | Optional (Quiz) | A short comment on the question that will be shown once you answer |

## 🤖 AI-Powered Workflow

Converting raw notes to YAML manually can be tedious and you might not even know what YAML is. Doesen't matter, `quizzer` includes a built-in **AI Prompt**:

1. Open the app and locate the **AI Prompt** section.
2. Copy the prompt provided.
3. Paste it into an LLM (like Gemini or ChatGPT) along with your raw study notes.
4. Copy the resulting YAML and paste it directly into `quizzer`.

**Notice:** AI models and interface change everyday, the prompt suggested might not fit your favorite AI model, check its prompt design guidelines to be shure to obtain a good output. Coding agents can do a great work at it but be aware that very large file may exceed the context window of the model and return unpredictable results. As always, check what AI does!

## 🛠️ Power User Features

- **Study Logic:** Toggle between **Sequential** (follow ID order) and **Random** (shuffle questions) modes to test your knowledge.
- **Live Tweaks:** Use the editor to refine your questions based on your performance during a session.
- **Portability:** Since it's a single HTML file, you can carry your entire study tool on a USB drive or email it to classmates.

## ⚙️ Technical Architecture

- **Frontend:** Vanilla HTML5, CSS3 (Custom Variables), and ES6+ JavaScript.
- **Parsing:** Powered by `js-yaml` for robust YAML processing.
- **PWA:** Implemented via `manifest.json` and `sw.js` (Service Worker) for offline caching and installation.

## 🗺️ Roadmap & TODOs

- [ ] **Fully Offline Integration:** Embed `js-yaml` directly into the HTML to remove the CDN dependency.
- [ ] **Dark Mode:** Implement a theme with a toggle for low-light study sessions.

## ⚖️ License & Credits

This project is licensed under the **Affero GNU General Public License v3.0 (AGPLv3)**.

- **js-yaml:** Included under the MIT License.
- **Author:** Simone Di Marco
- **GitHub:** [@simodimarco](https://github.com/simodimarco)
