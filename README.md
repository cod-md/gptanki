# GPTAnki ✨

**Quickly create Anki flashcards using AI-powered prompts!**

**Live Demo:** [https://cod-md.github.io/gptanki](https://cod-md.github.io/gptanki)

GPTAnki simplifies Anki flashcard creation. It generates structured prompts for your preferred Large Language Model (LLM, e.g., ChatGPT, Claude, Gemini). You then use this prompt with your LLM and source text. Finally, paste the AI's output back into GPTAnki to parse, validate, and download an Anki-ready CSV file.

https://raw.githubusercontent.com/cod-md/gptanki/refs/heads/main/Screenrecorder-2025-05-31-23-17-42-572%7E2.mp4

## 🚀 Key Features

* **AI-Optimized Prompts:** Generates tailored prompts for LLMs.
* **Dual Modes:**
    * **Generate:** Create new cards from raw text via an AI.
    * **Extract:** Convert pre-formatted card text to CSV.
* **Card Types:** Supports Multiple Choice (MCQ), Basic (Q/A), and Cloze Deletion.
* **Customization:**
    * **Number of Cards:** 50, 100, or custom.
    * **Difficulty Level(s):** For "Generate MCQs," select Bloom's Taxonomy levels (1-6, multi-select) to guide AI.
* **Dynamic Format Guides:** Provides copyable instructions for your AI, adapting to your selections.
* **Input Validation & CSV Export:** Ensures data integrity before creating the CSV.
* **Responsive UI:** Clean interface for desktop and mobile.

## 🛠️ How to Use GPTAnki

1.  **In GPTAnki ([https://cod-md.github.io/gptanki](https://cod-md.github.io/gptanki)):**
    * Select **Mode** (Generate/Extract).
    * Select **Card Type** (MCQ, Basic, Cloze).
    * Configure **Options** (Number of Cards, Difficulty Level if generating).
2.  **Copy the "Format Guide":** This text is your prompt for the AI.
3.  **In your LLM (e.g., ChatGPT):**
    * Paste the copied Format Guide.
    * Add your source material/text below the guide.
    * Run the AI to generate flashcard content.
4.  **Back in GPTAnki:**
    * Copy the AI's generated flashcard text.
    * Paste it into GPTAnki's main textarea.
    * The tool will attempt to validate the input.
    * Click "Generate CSV".
5.  **Download the CSV** and import it into Anki (see next section).

---

## 📥 Importing to Anki

1.  **Open Anki** (desktop), go to **File > Import...**, and select your CSV.
2.  In the Anki Import Dialog:
    * **Note Type:**
        * **Basic/Cloze:** Use Anki's built-in `Basic` or `Cloze` types.
        * **MCQs:** Highly recommended: Download and import this [MCQ Note Type (.apkg)](https://github.com/muctebanesiri/anki-multiple-choise-question-template/blob/main/Files/MCQ%20Notetype%20Demo.apkg) into Anki first. Then select it here (e.g., "MCQ-Format").
    * **Fields separated by:** **Crucially, select `Comma`**.
    * **Allow HTML in fields:** Check this option.
    * **Field Mapping:** Ensure CSV columns map correctly to your Anki Note Type's fields. For the recommended MCQ type, GPTAnki's 10-column CSV should map like: 1.Question, 2.OptA, ..., 8.AdditionalInfo, 9.Tags, 10.CorrectAnswerLetter.
    * Review the preview.
3.  Click **Import**.

---

## 📝 Format Guide Details

The "Format Guide" box is key. It provides dynamic, copyable instructions (e.g., *"Make **50** MCQs on the provided material following Bloom's taxonomy **levels 1, 3**."*) tailored to your settings. **Use this guide as the prompt for your AI** to ensure correctly formatted output for GPTAnki to parse. It also includes specific formatting examples for the AI.

---

## 💻 Technology

* **Frontend:** HTML, CSS, JavaScript.
* **AI Interaction:** GPTAnki generates prompts for *external* LLMs; it does not include a built-in AI.

---

## 🔮 Future Ideas

* Possible direct LLM API integration.
* More card types and advanced formatting.

---

## 🤝 Contributing

Issues and Pull Requests are welcome!

---

## 📜 License

MIT License. (Consider adding a `LICENSE.md` file to your repository).

---

Made with ❤️ for efficient learning!
