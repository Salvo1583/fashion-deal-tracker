<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0F2027,50:203A43,100:2C5364&height=180&section=header&text=Fashion%20Deal%20Tracker&fontSize=40&fontColor=ffffff&fontAlignY=36&desc=Monitoraggio%20prezzi%20e%20offerte%20su%20Telegram&descSize=18&descAlignY=58" alt="Fashion Deal Tracker" width="100%" />
</p>

<p align="center"><a href="README.md">🇬🇧 English</a> · <b>🇮🇹 Italiano</b></p>

<p align="center">
  <img src="https://img.shields.io/badge/codice-privato-555555?style=for-the-badge&logo=github" alt="Codice privato" />
  <img src="https://img.shields.io/badge/vetrina-progetto-36BCF7?style=for-the-badge" alt="Vetrina del progetto" />
</p>

> [!NOTE]
> Questo repository è una **vetrina del progetto**: il codice sorgente è privato. Una demo è disponibile su richiesta.

## 🧭 Panoramica

Un **tracker dei prezzi "stile Keepa"** per un grande e-commerce di moda. Scansiona i prodotti scontati, ne conserva lo storico dei prezzi e pubblica solo le **offerte vere** su un canale Telegram pubblico. Un bot personale permette a ogni utente di iscriversi a prodotti, marche o categorie specifiche.

## ✨ Funzionalità principali

- 🔎 **Scansione intelligente del catalogo** per categoria e marca, con richieste raggruppate (circa 3 richieste ogni 84 prodotti)
- 📉 **Filtro "offerta vera"**: un prodotto viene pubblicato solo se è scontato sia sul prezzo originale **sia** rispetto al prezzo minimo degli ultimi 30 giorni, così gli sconti finti vengono scartati
- 📢 **Canale Telegram pubblico** per le offerte sopra una soglia di sconto
- 🤖 **Bot Telegram personale** con iscrizioni a prodotti, marche e categorie
- 🕒 **Storico dei prezzi** per ogni prodotto monitorato
- 🧯 **Limiti di frequenza e pause** per mantenere un ritmo di richieste rispettoso

## 🏗️ Come funziona

```mermaid
flowchart LR
    SC[Scansione programmata] --> F{Filtro offerta vera<br/>vs minimo 30 giorni}
    F -->|offerta| DB[(Storico prezzi)]
    DB --> CH[Canale Telegram pubblico]
    DB --> BOT[Bot personale<br/>iscrizioni]
    F -->|sconto finto| X([scartato])
```

## 🧰 Tecnologie

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Telegram](https://img.shields.io/badge/Telegram_Bot-26A5E4?style=flat&logo=telegram&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat&logo=sqlalchemy&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)

## 📬 Contatti

Realizzato da **Salvatore Cutaia**, ingegnere informatico specializzato in agenti AI e automazioni.

[![GitHub](https://img.shields.io/badge/GitHub-Salvo1583-181717?style=flat&logo=github)](https://github.com/Salvo1583)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Salvatore_Cutaia-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/salvatore-cutaia-6047b0155/)
[![Website](https://img.shields.io/badge/Website-neuralform.it-111111?style=flat&logo=googlechrome&logoColor=white)](https://neuralform.it/)
