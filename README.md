# VerseSync

Align multi-lingual worship lyrics and export them ready-to-use into ProPresenter, FreeShow, and other presentation software.

## What is VerseSync?

VerseSync is a simple, powerful tool for creating bilingual or multilingual worship slides. It's a single HTML file that runs entirely in your web browser—no installation, no server, no dependencies required. Just open `index.html` in any modern browser and start creating beautiful, aligned lyrics for your church presentations.

Whether you're leading worship in multiple languages, need transliterations for pronunciation, or want to include translations for your congregation, VerseSync makes it easy to prepare professional-looking slides quickly.

**[Try VerseSync Live](https://jeff.github.io/versesync/)** — No download required, works directly in your browser!

## Key Features

- **Easy 3-Step Workflow**: Paste, align, and export your lyrics in minutes.
- **Multi-Language Support**: Handle primary lyrics, transliterations, and translations side-by-side.
- **Auto-Translate**: Powered by AI (Hugging Face's NLLB-200 model) to automatically translate lyrics between supported languages.
- **Drag-and-Drop Alignment**: Visually align lines across languages with an intuitive editor.
- **Multiple Export Formats**: Generate files for ProPresenter, FreeShow, OpenLyrics-compatible software, plain text, or print-ready PDFs.
- **ProPresenter Integration**: Native .pro files with proper slide layouts and group colors.
- **Free and Open Source**: No cost, no ads, no tracking—just pure functionality.

## Getting Started

1. **Download**: Grab the `index.html` file from this repository.
2. **Open**: Double-click the file or drag it into your web browser.
3. **Use**: Follow the on-screen steps to create your slides.

That's it! No setup required. The app works offline once loaded (except for auto-translate, which downloads a model on first use).

## Step-by-Step Guide

### Step 1: Paste Your Lyrics

- **Enter Song Details**: Add the song title and artist (optional).
- **Choose Languages**: Select your primary language from the dropdown. If using translations or transliterations, choose those too.
- **Paste Lyrics**: Copy and paste your lyrics into the text areas.
  - **Primary Lyrics**: Your main language.
  - **Transliteration** (optional): Phonetic spelling to help with pronunciation.
  - **Translation** (optional): Another language version.
- **Toggle Options**: Use the buttons to enable/disable transliteration and translation fields as needed.
- **Auto-Translate**: If you have primary lyrics but no translation, click "Auto-Translate" to generate one using AI. (Note: This requires an internet connection and downloads a ~630MB model on first use.)
- **Tips**:
  - Separate song sections (verses, choruses) with blank lines.
  - Use labels like `[Verse 1]`, `[Chorus]`, `[Bridge]` at the start of sections—these are automatically detected.
  - The app shows live stats on how many sections are detected in each language.

### Step 2: Align Slides

- **Review the Table**: Each row represents one slide. Columns show the primary lyrics, transliteration, and translation.
- **Edit Alignment**:
  - **Drag Rows**: Click and drag to reorder slides.
  - **Insert Rows**: Add blank slides above or below the selected row.
  - **Delete Rows**: Remove unwanted slides.
  - **Split Rows**: Divide a slide with many lines into two.
  - **Merge Rows**: Combine two slides into one.
  - **Edit Labels**: Click on section labels to rename them.
- **Preview**: Click any row to see a live preview of how the slide will look, including line counts and layout.
- **Tips**:
  - Use blank rows to offset languages if they don't align perfectly.
  - The preview shows the slide layout but not final styling—that's handled by your presentation software.

### Step 3: Export

- **Choose Format**: Select from the available export options.
- **Download**: Click the button to save the file to your computer.
- **Import**: Open the downloaded file in your presentation software.

## Export Formats Explained

| Format | File Extension | Description | Best For |
|--------|----------------|-------------|----------|
| **ProPresenter** | `.pro` | Native binary format for ProPresenter 7+. Includes slide layouts, group colors, and stacked text elements. | ProPresenter users |
| **FreeShow** | `.show` | JSON format with text items for each language. | FreeShow users |
| **OpenLyrics XML** | `.xml` | Standard XML format supported by EasyWorship, MediaShout, OpenLP, and others. | Universal compatibility |
| **Plain Text** | `.txt` | Simple interleaved text file. | Backup or manual editing |
| **Print / PDF** | — | Browser-based print dialog for formatted lyrics sheets. | Physical handouts or quick previews |

## Supported Languages

VerseSync supports a wide range of languages for input and auto-translation:

- English
- Spanish
- Chinese (Simplified & Traditional)
- Korean
- Portuguese (and Brazilian variant)
- French
- German
- Tagalog
- Vietnamese
- Hindi
- Malayalam
- Telugu
- Tamil
- Arabic
- Russian
- Japanese
- Indonesian
- Swahili
- Italian
- And more via the "Other" option

Auto-translation uses BCP-47 language codes and covers most major languages. If a language isn't listed, select "Other" and enter the lyrics manually.

## ProPresenter Slide Layout

When exporting to ProPresenter, slides use the "VB Bilingual" theme geometry at 1920×1080 resolution:

- **Primary Language**: White text at the bottom of the slide.
- **Transliteration** (if enabled): Lavender text in the middle.
- **Translation** (if enabled): Gold text at the top.

Text appearance (fonts, sizes, shadows) is controlled by your ProPresenter theme. VerseSync focuses on content and layout.

Groups are automatically created based on section labels:
- Chorus: Light blue
- Verse: Dark blue
- Other: Gray

## Usage Tips and Best Practices

- **Blank Lines Matter**: Always separate sections with blank lines to create individual slides.
- **Labels Help**: Use `[Chorus]`, `[Verse 2]`, etc., for better organization in ProPresenter.
- **Auto-Translate Caveats**: AI translation is helpful but not perfect—always review and edit for accuracy.
- **Browser Compatibility**: Works best in modern browsers like Chrome, Firefox, or Safari. Enable JavaScript.
- **Offline Use**: Once loaded, the app works offline. Auto-translate needs internet for the model download.
- **File Safety**: Downloaded files are safe and contain only your lyrics data.
- **Large Songs**: For very long songs, split into multiple exports if needed.

## Browser Requirements

- Modern web browser with JavaScript enabled.
- For auto-translate: Internet connection and ~630MB free space for the AI model (cached locally).
- No special hardware required—runs on any computer.

## Troubleshooting

- **App Won't Load?** Ensure JavaScript is enabled in your browser settings.
- **Auto-Translate Fails?** Check your internet connection. The model downloads once and is cached.
- **Export Doesn't Work?** Try a different browser or check for popup blockers.
- **Slides Look Wrong?** Double-check blank lines and alignment in Step 2.
- **ProPresenter Import Issues?** Ensure you're using ProPresenter 7 or later.

If you run into issues, try refreshing the page or reopening the HTML file.

## Tech Stack

- **Frontend**: Pure HTML, CSS, and JavaScript—no frameworks.
- **Auto-Translate**: Hugging Face Transformers.js with NLLB-200-distilled-600M model.
- **ProPresenter Export**: Custom binary format generation (inspired by VerseFlow).
- **File Generation**: Browser-native Blob and download APIs.

## Related Projects

- [VerseFlow](https://github.com/your-org/verseflow) — Python tool for batch-converting ProPresenter libraries. VerseSync borrows its PP7 binary logic.
- [VerseBridge](https://versebridge.app/studio) — The original inspiration for VerseSync's workflow and features.

## Contributing

Found a bug or have a feature request? Open an issue on GitHub. Pull requests welcome!

## License

[Add license info here, e.g., MIT License]

---

Enjoy creating multilingual worship experiences with VerseSync! 🎶
