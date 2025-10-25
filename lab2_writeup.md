# Lab 2 Write-Up: Note Taking App

## 📝 Project Overview

This lab focused on building a simple yet functional note-taking application. The goal was to implement a feature that allows users to generate structured notes based on a topic or keywords using an AI model. The app also supports multilingual note generation.

---

## 🚀 Features Implemented

- Generate notes from a topic or keyword using an LLM
- Output notes in structured JSON format with:
  - `Title`: A short, descriptive title
  - `Notes`: Detailed explanation
  - `Tags`: A list of relevant tags
- Language translation for multilingual support
- Creates simple ASCII art based on a keyword or concept
  - Art is constrained to 8 lines tall and 30 characters wide
  - Each line is wrapped in square brackets and centered
  - No text or explanation—just pure ASCII visuals
- Error handling for invalid or malformed responses

---

## 🛠️ Development Steps

1. **Set Up Project Environment**
   - Initialized a Python project with virtual environment
   - Installed required dependencies (e.g., `openai`, `json`, `flask` or `streamlit` for UI)

2. **Created the Note Generation Function**
   - Wrote `generate_notes(topic, lang="English")` to interact with the LLM
   - Ensured the model returns a valid JSON structure
   - Handled edge cases like malformed JSON or missing fields

3. **Created the Note Translation Function**
   - Wrote `translate_text(text, target_language)` to interact with the LLM
   - Ensured the model returns a with target language
   - 
4. **Added ASCII Art Generator**
   - Created `generate_ascii_art(text)` function
   - Prompt enforces formatting rules: ASCII-only, bracketed lines, no extra text
   - Integrated into UI with preview area
   - 
5. **Tested and Debugged**
   - Tested with various topics and languages
   - Simulated malformed responses to test error handling
   - Verified JSON parsing and tag formatting

---

## 🧩 Challenges Faced

- Ensuring the LLM always returns a valid JSON object
- Handling unexpected outputs like Markdown code blocks (` ```json `)
- Managing multilingual output formatting
- Designing a clean and intuitive UI for note display

---

## 💡 Lessons Learned

- Prompt engineering is crucial for consistent LLM responses
- Always validate and sanitize external model outputs
- Good error handling improves user experience significantly
- UI/UX design plays a big role in usability, even for simple apps

---

## ✅ Next Steps

- Add persistent storage to add and generate notes in Vercel if I have funding (e.g., SQLite or Supabase)
- Implement user authentication
- Add export options (PDF, Markdown)

---

## 🙌 Acknowledgments

Thanks to my instructor for the guidance and feedback throughout this lab. Also, shoutout to the AI assistant that helped me refine my code and documentation!
