# Comment Moderation With LLM-Powered Classification

This project uses a Generative AI model via Groq API to analyze user comments and classify them as offensive or non-offensive. It appends structured fields to each comment and saves the results to a new CSV.

---

## Classification Components

1. **LLM (Large Language Model)**:
   - Classifies each comment using deepseek-r1-distill-llama-70b.
   - Returns:
     - is_offensive: true/false
     - offense_type: e.g., hate speech, harassment, profanity, toxicity, none
     - explanation: short natural reason

2. **CSV Integration**:
   - Input: comments.csv with a column named comment_text
   - Output: output_file.csv with three additional columns:
     - is_offensive
     - offense_type
     - explanation

---

## Folder Structure

- main.ipynb
- comments.csv
- output_file.csv
- .env
- README.md

---

## Setup Instructions

1. Clone the repository:
```bash
git clone https://github.com/your-username/comment-moderation-ai.git
cd comment-moderation-ai
```

2. Create virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Set up .env file:
```bash
GROQ_API_KEY=your_actual_groq_api_key_here
```
