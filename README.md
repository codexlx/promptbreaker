# 🛡️ PromptBreaker

**PromptBreaker** is a lightweight, automated security scanner for LLM-based applications. 
It helps developers and security researchers identify critical vulnerabilities in their AI integrations before attackers do.

## 🚀 Features
- **Context Overflow (Lost in the Middle):** Tests if your model leaks its system prompt when fed a massive junk payload.
- **IDOR Scanner:** Checks for missing authorization checks on dialogue sessions/instances.

## 📦 Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/promptbreaker.git
   cd promptbreaker
Install dependencies:
Ы
pip install -r requirements.txt

🛠️ Usage
Run a full scan against your API endpoint:
python promptbreaker.py --url "https://api.yourdomain.com/v1/chat" --token "YOUR_JWT_TOKEN" --mode all

Command Line Options:
--url: The target API endpoint.

--token: Your authorization Bearer token.

--instance: The ID of the test dialogue session (default: default_instance).

--mode: overflow, idor, or all (default: all).

## 📸 Example Output

```text
🚀 Starting PromptBreaker Scan...
Target: https://api.yourdomain.com/v1/chat

⚠️ VULNERABLE: System Prompt Leakage!
Evidence: {"visible_message": "You are a helpful assistant...", ...}

Testing IDOR on Instance IDs...

┏━━━━━━━━━━━━━┳━━━━━━━━━━━━┓
┃ Instance ID ┃ Status     ┃
┡━━━━━━━━━━━━━╇━━━━━━━━━━━━┩
│ admin       │ VULNERABLE │
│ test        │ Secure     │
└─────────────┴────────────┘
```

## ⚖️ Disclaimer
This tool is intended for educational purposes and authorized security testing only. Do not use against systems you do not own. The author is not responsible for any misuse.

🤝 Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
