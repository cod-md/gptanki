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
    * Follow the instructions in the "Importing to Anki" section below.

---

## 📥 Importing to Anki

Once you have your `.csv` file from GPTAnki, here's how to import it into Anki:

1.  **Open Anki** desktop application.
2.  Go to **File > Import...**
3.  **Select the `.csv` file** you downloaded from GPTAnki.
4.  **Anki Import Dialog:** This is where you configure how Anki reads your file.
    * **Note Type:**
        * For **Basic Cards**, select Anki's built-in `Basic` note type.
        * For **Cloze Deletion Cards**, select Anki's built-in `Cloze` note type.
        * For **Multiple Choice Questions (MCQs):**
            * Using a specialized MCQ note type is **highly recommended** for the best functionality and display.
            * You can download a compatible MCQ note type template here:
                [**MCQ Note Type Demo.apkg**](https://github.com/muctebanesiri/anki-multiple-choise-question-template/blob/main/Files/MCQ%20Notetype%20Demo.apkg)
            * **To install this note type:**
                1.  Download the `.apkg` file from the link above.
                2.  In Anki, go to `File > Import...` and select the downloaded `.apkg` file. Click "Import".
                3.  This will add the note type (likely named "MCQ-Format" or similar, as shown in the demo) to your Anki collection.
            * After installation, **select this specific MCQ note type** (e.g., "MCQ-Format") in the current CSV import dialog.
    * **Fields separated by:** **IMPORTANT: Select `Comma` from the dropdown menu.** GPTAnki outputs standard comma-separated CSV files.
    * **Allow HTML in fields:** Ensure this option is **checked**. This allows for any potential formatting your cards might contain.
    * **Field Mapping:**
        * Anki will show how columns from your CSV (Field 1, Field 2, etc.) map to the fields of your chosen Anki Note Type.
        * For the **recommended MCQ Note Type** (from the link above), the CSV generated by GPTAnki has 10 columns. These should typically map as follows:
            1.  Field 1 (CSV) → `Question` (Anki Note Field)
            2.  Field 2 (CSV) → `Option A`
            3.  Field 3 (CSV) → `Option B`
            4.  Field 4 (CSV) → `Option C`
            5.  Field 5 (CSV) → `Option D`
            6.  Field 6 (CSV) → `Option E`
            7.  Field 7 (CSV) → `Option F`
            8.  Field 8 (CSV) → `AdditionalInfo` (or similar field for explanations/extra details)
            9.  Field 9 (CSV) → `Tags`
            10. Field 10 (CSV) → `Correct Answer` (this field in the note type usually stores the letter like A, B, C)
        * Verify that the mapping is correct. If Anki doesn't map them automatically, you can click on each Anki field and change which CSV field it maps to. The order listed above is how GPTAnki structures its MCQ CSV output.
    * Review the import preview at the bottom of the dialog to ensure your cards look as expected before finalizing the import.
5.  Click **Import**.

After importing, you can find your new cards in the deck specified during the import process (or your default deck if none was chosen).

---

## 📝 Format Guide Details

The dynamic "Format Guide" is a core feature. It provides instructions like:
*"Make **50** MCQs on the provided material following Bloom's taxonomy **levels 1, 3**."* (This text changes based on your selections).

It also includes strict formatting rules and examples for the AI to follow, such as:

* **MCQ Example:** `What is the capital of France?|Paris|London|Berlin|Madrid|Rome|Tokyo|A`
* **Basic Example:** `What is the largest planet?|Jupiter`
* **Cloze Example:** `The powerhouse of the cell is the {{c1::mitochondria}}.`

**Always copy and use the provided guide with your AI for best results.**

---

## 💻 Technology Stack

* **Frontend:** HTML5, CSS3, JavaScript (Vanilla JS)
* **Design:** Modern, responsive design with custom CSS variables for theming.
* **AI Interaction:** GPTAnki itself does not perform AI processing. It generates structured prompts for users to use with external Large Language Models (LLMs).

---

## 🔮 Future Ideas

* Direct integration with LLM APIs (e.g., OpenAI API) to automate the AI generation step.
* Support for more Anki card fields and note types.
* User accounts and cloud storage for prompts/card sets.
* Advanced formatting options (Markdown, HTML in cards).
* Community-shared prompt templates.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Please feel free to check the [issues page](https://github.com/cod-md/gptanki/issues) (if you create one for this repo).

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

---

## 📜 License

This project is licensed under the MIT License. (You can add a `LICENSE.md` file with the MIT license text if you wish).

---

Made with ❤️ for efficient learning!
