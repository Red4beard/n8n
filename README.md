# 🤖 HAS Matrix Consultant Bot (n8n Workflow)

A Telegram-based AI assistant that helps users evaluate how AI can support, semi-automate, or enhance their professional tasks — using the **Human Agency Scale (HAS)** framework. This workflow uses OpenAI, LangChain, and Telegram integration to create an interactive automation assessment matrix.

---

## 🚀 What It Does

This workflow allows users to:

- 🔍 Analyze their job or profession by sending a message or voice note.
- 🧠 Receive a 4-zone matrix:
  - 🟢 Green: Tasks ready for full AI automation.
  - 🟡 Yellow: Semi-automatable tasks requiring human oversight.
  - 🔴 Red: Automatable, but better left to humans to preserve skill and uniqueness.
  - ⚪️ White: Tasks AI cannot (and shouldn't) replace — for human growth and expression.

The system leverages GPT-4 via LangChain’s Agent node, and also supports voice-to-text using OpenAI Whisper.

---

## 💡 Use Cases

- AI coaching for professionals and creatives
- HR, training, and upskilling strategy
- Conscious automation advisors
- Solopreneurs wanting to balance tech & creativity
- Education on Human-AI collaboration

---

## 🧩 Workflow Overview

| Node | Description |
|------|-------------|
| 🟢 `Telegram Trigger` | Listens for new messages or voice notes |
| 🟢 `Switch` | Branches based on message type (text or voice) |
| 🟡 `Telegram` | Downloads the voice file |
| 🧠 `OpenAI Transcribator` | Converts voice into text |
| 🔁 `Text edit fields` | Passes the text to the agent |
| 💬 `AI Agent` | Analyzes the profession and generates the HAS matrix |
| 📤 `Answer to user` | Sends the formatted matrix back via Telegram |
| 🧠 `Langchain LLM`, `Memory module`, `Tavily Web Search` | Enhance context, continuity, and factual accuracy |

---

## 🛠 Requirements

Before importing the workflow:

1. **Telegram Bot**  
   - Create a bot via [BotFather](https://t.me/BotFather) and grab the token.
   - Set webhook URL via n8n Telegram Trigger node.

2. **OpenAI API Key**  
   - Required for both transcription and GPT responses.

3. **Tavily API (Optional)**  
   - Used for real-time web search.

---

## 📦 How to Use

1. Clone this repo or [download the latest workflow JSON](./HAS_matrix_consultant_eng.json).
2. Import into your [n8n instance](https://n8n.io).
3. Set up the required credentials:
   - Telegram (`telegramApi`)
   - OpenAI (`openAiApi`)
4. Deploy the workflow and start messaging the bot!
5. Send your **job title** or **voice message** to receive your automation matrix.

---

## 📊 HAS Scale Explained

- **H1** → Fully autonomous by AI
- **H2-H4** → Collaboration zone between AI and human
- **H5** → Full human responsibility and ownership

Learn more about the HAS framework:  
📚 https://arxiv.org/html/2506.06576v2

---

## 🏷 Tags

`#GPT` `#LangChain` `#n8n` `#TelegramBot` `#AIProductivity` `#AutomationAssessment` `#OpenAI` `#VoiceToText`

---

## 📄 License

no need

---

## 🤝 Contributing

Got improvements? Want to expand to WhatsApp or Webhooks?  
Feel free to fork and submit a pull request.

---

## 👤 Author

**[@red4beard](https://github.com/red4beard)** 
