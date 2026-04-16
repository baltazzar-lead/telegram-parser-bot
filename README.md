Название: telegram-parser-bot


Описание (короткое): Production-ready Telegram bots for automated product parsing, inventory monitoring, and instant notifications.

markdown
# Telegram Parser Bot — Automated Product Monitoring

A suite of Telegram bots built for **Cvestok** flower marketplace that automate product parsing, inventory monitoring, and real-time notifications for florists and administrators.

## 🧠 Architecture

┌─────────────┐     ┌─────────────────┐     ┌──────────────┐
│  Web Scraper │────▶│  Python Backend │────▶│  Telegram Bot │
│ (Playwright) │     │   (Aiogram)     │     │   (Aiogram)   │
└─────────────┘     └─────────────────┘     └──────┬───────┘
                                                     │
                                                     ▼
┌─────────────┐     ┌─────────────────┐     ┌──────────────┐
│   Florists   │◀────│  Notification   │◀────│   Supabase   │
│  (Telegram)  │     │   Dispatcher    │     │   (DB)       │
└─────────────┘     └─────────────────┘     └──────────────┘

## 🛠 Tech Stack

| Component | Technology |
|:---|:---|
| **Bot Framework** | Python 3.12 + Aiogram |
| **Web Scraping** | Playwright + BeautifulSoup |
| **Database** | Supabase (PostgreSQL) |
| **Infrastructure** | Docker, Nginx, VPS |
| **Notifications** | Telegram Bot API |

## 🚀 Key Features

- **Automated product parsing:** Monitors supplier websites for new flower listings.
- **Price change alerts:** Notifies florists when competitor prices drop.
- **Inventory sync:** Updates Cvestok database with fresh stock data.
- **Instant Telegram notifications:** Florists receive real-time alerts on new deals.
- **Admin controls:** Start/stop parsing, view logs, manage sources via bot commands.

## 📁 Project Structure
telegram-parser-bot/
├── bot/
│ ├── handlers/ # Aiogram message handlers
│ ├── keyboards/ # Inline keyboards
│ └── main.py # Bot entry point
├── parser/
│ ├── scrapers/ # Playwright scrapers per source
│ ├── pipeline.py # Data processing pipeline
│ └── scheduler.py # Cron-like task scheduler
├── docker-compose.yml
└── requirements.txt

text

## 👤 Author

**Garik** — AI Automation Architect & Full-stack Developer.
- GitHub: [@baltazzar-lead](https://github.com/baltazzar-lead)

---
*Powering real-time inventory updates for Cvestok flower marketplace.*
