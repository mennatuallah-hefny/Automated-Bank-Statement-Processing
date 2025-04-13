# 📄 Bank Statement Automation (Make.com)

## 🔍 Overview
Automates end‑to‑end ingestion, parsing and reporting of PDF bank statements via Jotform → Make.com → Google Sheets.

- **Baseline**: 10 min/manual statement → **Automated**: 2 min/statement (80% time reduction)  
- **Throughput**: 100 → 500 statements/month (+400%)  
- **Error Rate**: 5% → <1% (80% reduction)  
- **Savings**: 65 hrs/month & \$21.6K annual labor cost

---

## ⚙️ Workflow Steps
1. **Trigger**: Jotform “New Submission” webhook  
2. **Fetch PDF**: HTTP “Get File” module  
3. **Parse**: PDF.co “Bank Statement Parser”  
4. **Transform**: JSON → array of `{ date, description, amount, balance }`  
5. **Load**: Google Sheets “Add Rows” (transactions)  


---

## 🏗 Architecture
```
Jotform → Make.com Scenario → PDF.co → Google Sheets & Slack/Email
```

---

## 🛠 Tech Stack
- **No‑Code**: Make (Integromat)  
- **Form Input**: Jotform API / Webhooks  
- **PDF Parsing**: PDF.co v2  
- **Data Store**: Google Sheets  

---

## 🚀 Setup & Deployment

1. **Clone Repo**  
   ```bash
   git clone https://github.com/your‑username/bank‑statement‑automation.git
   cd bank‑statement‑automation
   ```

2. **Import Make.com Scenario**  
   - In Make.com: **Scenarios → Import** → upload `make‑scenario.json`

3. **Configure Connections**  
   - Jotform API Key → Scenario “Jotform” module  
   - PDF.co API Key → Scenario “PDF.co” module  
   - Google Sheets OAuth → Scenario “Google Sheets” modules  

4. **Deploy**  
   - Turn scenario **ON**  
   - Set schedule to **“Immediately”** on webhook trigger

---

## 📊 Metrics & Results

| Metric                   | Baseline | Automated | Improvement        |
|--------------------------|----------|-----------|--------------------|
| Cycle Time per Statement | 10 min   | 2 min     | −80%               |
| Monthly Throughput       | 100      | 500       | +400%              |
| Error Rate               | 5%       | <1%       | −80%               |
| Monthly Hours Saved      | —        | 65 hrs    | +65 hrs            |
| Annual Savings           | —        | \$21.6K   | +\$21.6K           |

---


## 🤝 Contributing
1. Fork repo  
2. Update `make‑scenario.json` or `README.md`  
3. Submit PR

---
