
# Conversation Summarization & Information Extraction

This notebook demonstrates two key tasks using **Groq API (LLaMA-3.1-8b-instant)** and supporting Python utilities.

---

## 📌 Task 1: Conversation Summarization & Truncation
- Implements **chat history tracking** with summarization and truncation.  
- **Summarization** occurs after every fixed number of turns (`k=3`).  
- **Truncation strategies**:
  - By maximum number of turns (e.g., `max_turns=4`)  
  - By maximum number of characters (e.g., `max_chars=3000`)  

### 🔹 Demo:
1. Truncation by turns  
2. Truncation by characters  

This ensures efficient context management in long conversations.

---

## 📌 Task 2: JSON Schema Classification & Information Extraction
This task extracts **structured details** from unstructured free-text chats.  
Details include:  
- `name`  
- `email`  
- `phone`  
- `location`  
- `age`

### 🔹 Workflow:
1. Uses **Groq API with JSON Schema tools** for structured outputs.  
2. Validates extracted data against the schema:  
   - ✅ **Present keys** → Correctly extracted fields  
   - ⚠️ **Missing keys** → Expected but not found  
   - ❌ **Extra keys** → Not part of schema  
3. **Fallback Regex Extraction** is applied if API call fails.  

### 🔹 Demos:
Five sample chats are tested:
1. **Complete details** (all fields present)  
2. **Partial details** (some fields missing)  
3. **No details** (empty extraction)  
4. **Invalid details** (skips invalid values)  
5. **Some details** (only name + location)

Each demo shows both the **extracted JSON** and the **validation results**.

---

## ⚙️ Tech Stack
- **Python**  
- **Groq API** (`LLaMA-3.1-8b-instant`)  
- **OpenAI client libraries**  
- **Regex (for fallback extraction)**  
- **JSON Schema validation**  

---

## 📈 Insights
- Task 1 provides an **efficient way to handle long chat conversations** by summarizing and truncating context.  
- Task 2 ensures **structured data extraction from unstructured chats**, useful for automating workflows like **E-KYC, chatbots, or CRM data entry**.  

---

## 🚀 Future Scope
- Extend schema to support more fields.  
- Improve regex fallback to handle edge cases.  
- Deploy as a **REST API service** for real-world integration.  

---

👉 This project is a step toward **automated summarization, data extraction, and validation pipelines** in AI-driven applications.
