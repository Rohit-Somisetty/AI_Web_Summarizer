# News Summarizer & Instagram Post Generator
A Jupyter-notebook tool that **scrapes any news article, distills the key ideas with local LLMs, and instantly formats the output as an Instagram-ready post** – emojis, hashtags, headline, everything.

---

## ✨  Key features
| Feature | What it does | Tech under the hood |
|---------|--------------|---------------------|
| One-click scraping | Pulls full article text with Selenium (undetected-chromedriver) and falls back to a plain `requests` fetch if headless Chrome fails | `undetected_chromedriver`, `selenium`, `BeautifulSoup` |
| Local-LLM summaries | Runs multiple Ollama models in parallel (default: **llama3.2**, **gemma3**, **deepseek-r1:8b**) so you can compare tones / lengths | `ollama` REST chat API |
| Format switcher | “Short”, “Bullet Points”, or “Detailed” summaries chosen from a toggle | `ipywidgets` |
| IG-post builder | Generates a punchy headline, selects context-aware emojis & hashtags, and returns a polished caption | Regular-expression helpers |
| Instant download | Saves the most-recent summary to `summary_YYYYMMDD_HHMMSS.txt` | `datetime` timestamping |
| GUI, no code needed | Every action lives behind friendly Jupyter widgets | `ipywidgets`, `IPython.display` |

---

## 🛠  Installation

> **Tested on Python 3.10+, macOS 14 & Windows 10/11**

1. **Clone** the repository  
   ```bash
   git clone https://github.com/<your-user>/<repo>.git
   cd <repo>
