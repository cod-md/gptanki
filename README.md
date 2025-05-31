# GPTAnki ✨

**Transform your content into Anki flashcards with AI-powered prompt engineering!**

**Live Demo:** [https://cod-md.github.io/gptanki](https://cod-md.github.io/gptanki)

GPTAnki is a user-friendly web application designed to streamline the creation of Anki flashcards. It intelligently generates structured prompts for you to use with your preferred Large Language Models (LLMs) like ChatGPT, Claude, Gemini, etc. Once your AI generates the flashcard content based on these prompts, GPTAnki helps you parse, validate, and convert it into a CSV file, ready for import into Anki.

## 🚀 Key Features

* **🧠 AI-Optimized Prompts:** Generates tailored instructional prompts for LLMs to create high-quality flashcards.
* **✌️ Dual Modes:**
    * **Generate Mode:** Create new flashcards from your raw text material using AI.
    * **Extract Mode:** Parse and convert already structured flashcard text (e.g., from a previous AI generation or your own notes) into CSV.
* **🃏 Multiple Card Types:** Supports:
    * Multiple Choice Questions (MCQ)
    * Basic (Question/Answer)
    * Cloze Deletion
* **⚙️ Customizable Card Generation:**
    * **Number of Cards:** Specify 50, 100, or a custom number of cards for the AI to generate.
    * **Difficulty Level(s):** For **Generate Mode** (especially MCQs), select one or more Bloom's Taxonomy levels (1-6) to guide the AI in creating questions of specific cognitive complexity.
* **📖 Dynamic Format Guides:** Provides clear, copyable instructions and format examples that adapt to your selected options (mode, card type, number, difficulty). These are crucial for guiding the AI.
* **✅ Real-time Input Validation:** (For Extract Mode or when pasting AI output) Helps ensure the pasted text adheres to the expected format before generating the CSV.
* **📊 Statistics:** Shows the number of valid cards and average options for MCQs.
* **📄 CSV Export:** Directly download a `.csv` file formatted for easy Anki import.
* **✨ Clean & Responsive UI:** Modern, intuitive interface that works well on desktop and mobile devices.

## 🛠️ How to Use GPTAnki

The workflow involves using GPTAnki to prepare a prompt, using that prompt with an external AI, and then using GPTAnki again to process the AI's output.

1.  **Go to GPTAnki:** Open [https://cod-md.github.io/gptanki](https://cod-md.github.io/gptanki) in your browser.
2.  **Select Mode:**
    * `✨ Generate`: If you have raw text (e.g., lecture notes, a chapter from a book) and want an AI to create flashcards from it.
    * `🔍 Extract`: If you already have text formatted as flashcards (e.g., you manually wrote them in the specified format, or an AI has already generated them).
3.  **Select Card Type:** Choose from Multiple Choice, Basic, or Cloze Deletion.
4.  **Configure Options (Mainly for Generate Mode):**
    * **Number of Cards:** Select 50, 100, or enter a custom quantity. This tells the AI prompt how many cards to aim for.
    * **Difficulty Level(s):** If in **Generate Mode**, you can select one or multiple difficulty levels (1-6). This is particularly useful for MCQs to target specific Bloom's Taxonomy cognitive levels. This option is hidden in Extract Mode.
5.  **Copy the Format Guide:**
    * A "Format Guide" box will appear, tailored to your selections.
    * Click the "Copy" button within this guide. **This text is your prompt for the AI.**
6.  **Use Your Preferred AI Model (e.g., ChatGPT, Claude, Gemini):**
    * Open your AI tool.
    * Paste the copied guide text.
    * Below the pasted guide, add your source material (the text you want to turn into flashcards).
    * Submit this combined text to the AI.
7.  **Get AI Output & Paste into GPTAnki:**
    * The AI will (hopefully) generate flashcard content according to the format specified in the guide.
    * Copy the AI-generated flashcard text.
    * Paste this text into the main textarea in GPTAnki (labeled "Content for ... Generation" or "Multiple-Choice Questions (to Extract)", etc.).
8.  **Validate & Generate CSV:**
    * GPTAnki will attempt to validate the pasted text.
    * If valid, click the "Generate CSV" button.
9.  **Download & Import:**
    * A "Download CSV" button will appear. Click it to save the file.
    * Import this CSV file into your Anki application.

## 📝 Format Guide Details

The dynamic "Format Guide" is a core feature. It provides instructions like:
*"Make **50** MCQs on the provided material following Bloom's taxonomy **level 1, 3**."* (This text changes based on your selections).

It also includes strict formatting rules and examples for the AI to follow, such as:

* **MCQ Example:** `What is the capital of France?|Paris|London|Berlin|Madrid|Rome|Tokyo|A`
* **Basic Example:** `What is the largest planet?|Jupiter`
* **Cloze Example:** `The powerhouse of the cell is the {{c1::mitochondria}}.`

**Always copy and use the provided guide with your AI for best results.**

## 💻 Technology Stack

* **Frontend:** HTML5, CSS3, JavaScript (Vanilla JS)
* **Design:** Modern, responsive design with custom CSS variables for theming.
* **AI Interaction:** GPTAnki itself does not perform AI processing. It generates structured prompts for users to use with external Large Language Models (LLMs).

## 🔮 Future Ideas

* Direct integration with LLM APIs (e.g., OpenAI API) to automate the AI generation step.
* Support for more Anki card fields and note types.
* User accounts and cloud storage for prompts/card sets.
* Advanced formatting options (Markdown, HTML in cards).
* Community-shared prompt templates.

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Please feel free to check the [issues page](https://github.com/cod-md/gptanki/issues) (if you create one for this repo).

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

## 📜 License

This project is licensed under the MIT License. (You can add a `LICENSE.md` file with the MIT license text if you wish).

---

Made with ❤️ for efficient learning!
