<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0F2027,50:203A43,100:2C5364&height=180&section=header&text=Fashion%20Deal%20Tracker&fontSize=40&fontColor=ffffff&fontAlignY=36&desc=Price%20tracking%20%26amp%3B%20Telegram%20deal%20alerts&descSize=18&descAlignY=58" alt="Fashion Deal Tracker" width="100%" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/source-private-555555?style=for-the-badge&logo=github" alt="Source private" />
  <img src="https://img.shields.io/badge/project-showcase-36BCF7?style=for-the-badge" alt="Project showcase" />
</p>

> [!NOTE]
> This repository is a **project showcase**: the source code is private. A demo is available on request.

## 🧭 Overview

A **"Keepa-style" price tracker** for a large fashion e-commerce. It scans discounted products, keeps their price history and publishes only the **real deals** to a public Telegram channel. A personal bot lets each user subscribe to specific products, brands or categories.

## ✨ Key features

- 🔎 **Smart catalog scanning** by category and brand, with batched requests (about 3 requests every 84 products)
- 📉 **Real-deal filter**: a product is published only if it is discounted both on the original price **and** against its lowest price of the last 30 days, so fake discounts are discarded
- 📢 **Public Telegram channel** for deals above a global discount threshold
- 🤖 **Personal Telegram bot** with subscriptions to products, brands and categories
- 🕒 **Price history** stored for every tracked product
- 🧯 **Rate limiting and backoff** to stay well within polite request rates

## 🏗️ How it works

```mermaid
flowchart LR
    SC[Scheduled scanner] --> F{Real-deal filter<br/>vs 30-day low}
    F -->|deal| DB[(Price history)]
    DB --> CH[Public Telegram channel]
    DB --> BOT[Personal bot<br/>subscriptions]
    F -->|fake discount| X([discarded])
```

## 🧰 Tech stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Telegram](https://img.shields.io/badge/Telegram_Bot-26A5E4?style=flat&logo=telegram&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat&logo=sqlalchemy&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)

## 📬 Contact

Built by **Salvatore Cutaia**, Computer Engineer specialized in AI agents & automations.

[![GitHub](https://img.shields.io/badge/GitHub-Salvo1583-181717?style=flat&logo=github)](https://github.com/Salvo1583)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Salvatore_Cutaia-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/salvatore-cutaia-6047b0155/)
