# IOC Collector (Flask CTI Project)

This is an **ongoing personal Cyber Threat Intelligence (CTI) project** where I built a Python-based Flask web application to **collect, normalize, and display Indicators of Compromise (IOCs)** from multiple open-source threat feeds.  

The goal is to get hands-on experience with **threat feed ingestion, IOC enrichment, and visualization** in a practical way.

---

## ✨ Features
- Pulls IOCs from public feeds:
  - [URLhaus](https://urlhaus.abuse.ch/) (malicious URLs)  
  - [Feodo Tracker](https://feodotracker.abuse.ch/) (C2 IPs)  
  - [OpenPhish](https://openphish.com/) (phishing URLs)  
- Normalizes and stores IOCs in a **SQLite database**
- Classifies IOCs as IP, Domain, URL, or Hash
- Deduplicates entries and updates `last_seen`, `confidence`, and `tags`
- Simple **Flask web UI**:
  - Search and filter by type, source, and confidence  
  - View in a clean Bootstrap table  
  - Export current filtered results to **CSV**

---

## 🚀 Getting Started

### Requirements
- Python 3.9+
- Flask
- Requests

### Installation
```bash
git clone https://github.com/yourusername/ioc-collector.git
cd ioc-collector
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
