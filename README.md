# quizzer
A lightweight, standalone web application for practicing exam quizzes using YAML-formatted databases. Designed to be private, portable, and easy to use for students and educators.

## ✨ Key Features

- **Zero Installation:** A single-page application (SPA) that runs directly in any modern web browser.
- **Flexible Data Input:**
    - **Drag & Drop:** Drop your `.yaml` file directly onto the interface.
    - **File Upload:** Browse and select your local quiz files.
    - **Live Paste:** Paste YAML text directly into the app to start immediately.
- **Customizable Quiz Logic:** - Toggle between **Sequential** (order by ID) and **Random** (shuffled) modes.
- **Integrated Live Editor:** Modify, fix, or update your quiz data during the session without losing progress.
- **Export & Portability:** Download your corrected YAML files or copy the updated text to your clipboard.
- **AI-Ready Prompt:** Includes a built-in generator to help you convert raw study notes into valid YAML using AI tools (ChatGPT, Gemini, etc.).
- **Modern UI:** A clean, card-based interface with CSS variables for easy personal theming.

## 🛠️ How to Use

1. **Download** the `index.html` file from this repository.
2. **Open** it in your preferred browser (Chrome, Firefox, Safari, Edge).
3. **Load** your quiz data and start practicing. No internet connection is required after the initial library load.

## 📊 Data Structure (YAML)

The application expects the following YAML format:

```yaml
- id: 1
  domanda: "What is the main advantage of this app?"
  opzioni:
    a: "It requires a server"
    b: "It is standalone and private"
    c: "It only works with JSON"
  risposta_corretta: "b"
```

## 🔒 Privacy & Security

100% Local Processing: Your quiz files are never uploaded to a server. All parsing and logic happen within your browser's memory.

No Data Collection: The app does not use cookies or tracking scripts.

## 📋 Roadmap & TODOs

[ ] Fully Offline Integration: Embed the js-yaml library directly into the HTML file to remove the external CDN dependency (currently loaded via Cloudflare).

[ ] Answer notes: add a "note" field into the .yaml structure to manage notes for every question.

[ ] Dark Mode: Add a toggle for low-light study sessions.

## ⚖️ License

This project is licensed under the Affero GNU General Public License v3.0 (GPLv3).

Note: This project uses the js-yaml library, which is included under the MIT License.

## 👤 Author

Simone Di Marco (assisted by Gemini AI)

GitHub: @simodimarco
