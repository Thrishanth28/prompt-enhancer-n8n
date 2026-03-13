# prompt-enhancer-n8n
🤖 AI Prompt Enhancer — n8n Workflow

Transform any basic, rough prompt into a professional, structured, and optimized AI prompt automatically using two AI agents powered by Google Gemini.


📸 Workflow Preview
Show Image i the before or after this file

✨ What It Does
Most people write basic prompts like:

❌ "write me a blog about coffee"
❌ "make a marketing email"
❌ "explain machine learning"

This workflow automatically converts them into professional, detailed prompts with:

✅ A clear Role, Task, Context
✅ Step-by-step Instructions
✅ Output Format & Tone
✅ Constraints & Goal


🔁 How The Flow Works
Chat Trigger
    ↓
🤖 The Decider  (Gemini + Memory)
    → Analyzes your basic prompt
    → Outputs a structured JSON plan
    ↓
⚙️ Parse Decider JSON  (Code Node)
    → Cleans and extracts the JSON safely
    ↓
⚙️ Build Answerer Prompt  (Code Node)
    → Formats the plan as a user message
    ↓
🤖 The Answerer  (Gemini + Memory)
    → Writes the final professional prompt

🧩 Nodes Used
NodePurposeChat TriggerAccepts user's basic prompt via chatThe DeciderAI agent that analyzes and plans the prompt structureParse Decider JSONCode node that safely parses the JSON outputBuild Answerer PromptCode node that formats the plan as inputThe AnswererAI agent that writes the final professional promptGoogle Gemini Chat ModelLLM for The DeciderGoogle Gemini Chat Model1LLM for The AnswererWindow Buffer Memory (Decider)Keeps conversation context for The DeciderWindow Buffer Memory (Answerer)Keeps conversation context for The Answerer

🚀 How To Use
1. Import the Workflow

Open n8n
Click "Add Workflow" → "Import from file"
Upload prompt_enhancer_n8n_fixed.json

2. Get Your Free Gemini API Key

Go to aistudio.google.com
Click "Get API Key" → "Create API Key"
Copy the key

3. Add Your API Key in n8n

Click on Google Gemini Chat Model node
Go to Credentials → Create New
Paste your Gemini API Key → Save
Repeat for Google Gemini Chat Model1

4. Activate & Chat

Click "Save" then "Activate"
Open the Chat panel
Type any basic prompt and hit send!


💡 Example
Input:
write a blog about coffee
Output:
# ROLE
You are an expert content writer and food & beverage journalist
with deep knowledge of coffee culture, brewing methods, and industry trends.

# TASK
Write an engaging, informative blog post about coffee that educates
and entertains readers while covering its history, culture, and brewing tips.

# CONTEXT
- Audience: Coffee enthusiasts and general readers aged 20-45
- Purpose: To inform, engage, and drive blog traffic
- Background: Coffee is one of the world's most consumed beverages
  with a rich cultural history across multiple continents.

# INSTRUCTIONS
- Start with an attention-grabbing introduction
- Cover the history and origin of coffee
- Include at least 3 brewing methods with tips
- Use subheadings for easy reading
- Add a compelling conclusion with a call to action

# OUTPUT FORMAT
- Format: Paragraphs with subheadings
- Length: Long (1000-1500 words)
- Tone: Engaging and informative

# CONSTRAINTS
- Avoid overly technical jargon
- Always cite interesting facts to back up claims

# GOAL
Deliver a well-structured, SEO-friendly blog post that keeps readers
engaged from start to finish and positions the author as an expert.

🛠️ Built With

n8n — Workflow automation
Google Gemini — AI language model (Free API)
Window Buffer Memory — Conversation context


📁 Files
📦 prompt-enhancer-n8n
 ┣ 📄 prompt_enhancer_n8n_fixed.json   ← Import this into n8n
 ┣ 🖼️ workflow_preview.png             ← Workflow screenshot
 ┗ 📄 README.md                        ← You are here

🙌 Contributing
Feel free to fork this repo, improve the prompts, or add new models!
Pull requests are welcome.

📜 License
MIT License — free to use and modify.
