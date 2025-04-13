# 📄 Bank Statement Automation (Make.com)

<div>
    <a href="https://www.loom.com/share/8bd9b5b732684dc6bf86994538a896a7">
      <p>Bank Statement Automation - Watch Video</p>
    </a>
    <a href="https://www.loom.com/share/8bd9b5b732684dc6bf86994538a896a7">
      <img style="max-width:300px;" src="https://cdn.loom.com/sessions/thumbnails/8bd9b5b732684dc6bf86994538a896a7-fc45dbaa07b0e082-full-play.gif">
    </a>
  </div>


## 🔍 Overview

This scenario automates the ingestion, parsing, and reporting of PDF bank statements using Jotform → Make.com → Google Sheets.

> ⚠️ **Note**: All metrics below are based on realistic assumptions, except for the automated processing time, which was precisely measured at **37 seconds per PDF**.

- **Processing Time**: 10 min (manual, estimated) → 37 sec (automated, measured) — **93.8% time reduction**
- **Monthly Throughput**: 100 → 500 statements (estimated) — **+400% increase**
- **Error Rate**: 1% (manual, estimated) → <0.05% (automated, estimated) — **95% reduction**
- **Labor Savings**: 65 hrs/month (estimated) — **$14.1K annual savings**

---

## ⚙️ Workflow Steps

1. **Trigger**: Jotform “New Submission” webhook
2. **Fetch PDF**: HTTP “Get File” module
3. **Parse**: PDF.co “Bank Statement Parser”
4. **Transform**: JSON → array of `{ date, description, amount, balance }`
5. **Load**:
   - Google Sheets “Add Rows” (transactions)
   - Google Sheets “Update Cell” (daily totals)
6. **Notify**: Slack/Email summary with link & error flags
7. **Log**: start/end timestamps + error count to Make Data Store

---

## 🏗 Architecture

```
Jotform → Make.com Scenario → PDF.co → Google Sheets & Slack/Email
```

---

## 🏛 Tech Stack

- **No–Code**: Make (Integromat)
- **Form Input**: Jotform API / Webhooks
- **PDF Parsing**: PDF.co v2
- **Data Store**: Google Sheets

---

## 🚀 Setup & Deployment

1. **Clone Repo**
   ```bash
   git clone https://github.com/your-username/bank-statement-automation.git
   cd bank-statement-automation
   ```

2. **Import Make.com Scenario**
   - In Make.com: **Scenarios → Import** → upload `make-scenario.json`

3. **Configure Connections**
   - Jotform API Key → Scenario “Jotform” module
   - PDF.co API Key → Scenario “PDF.co” module
   - Google Sheets OAuth → Scenario “Google Sheets” modules

4. **Deploy**
   - Turn scenario **ON**
   - Set schedule to **“Immediately”** on webhook trigger

---

## 📊 Metrics & Results

| Metric                   | Manual (Estimated) | Automated (Measured/Estimated) | Improvement        |
|--------------------------|--------------------|-------------------------------|--------------------|
| Processing Time per PDF  | 10 min             | 37 sec (measured)             | –93.8%             |
| Monthly Throughput       | 100                | 500 (estimated)               | +400%              |
| Error Rate               | 1% (estimated)     | <0.05% (estimated)            | –95%               |
| Monthly Hours Saved      | —                  | 65 hrs (estimated)            | +65 hrs            |
| Annual Labor Savings     | —                  | $14.1K (estimated)            | +$14.1K            |

> 💡 **Annual labor cost savings** estimated using:
> - 0.157 hrs saved per PDF
> - 500 PDFs/month
> - $15/hr data entry wage
> - 12 months

---

## 📚 Metric Justifications & Sources

### ⏱ Processing Time

- **Manual Estimate**: 10 minutes per PDF is a conservative estimate based on typical manual data entry tasks.
- **Automated Measurement**: 37 seconds per PDF was measured during scenario execution.

### 📈 Monthly Throughput

- **Estimate**: Increasing from 100 to 500 statements per month assumes the automation allows for processing more statements due to reduced time per statement.

### ❌ Error Rate

- **Manual Estimate**: 1% error rate is a commonly accepted average for manual data entry tasks. citeturn0search4
- **Automated Estimate**: <0.05% error rate is based on the high accuracy rates of automated data entry systems, which typically boast accuracy rates of 99.959% to 99.99%. citeturn0search1

### 💰 Labor Savings

- **Calculation**:
  - Time saved per PDF: 10 min (manual) – 37 sec (automated) = 9.38 min ≈ 0.157 hrs
  - Monthly savings: 0.157 hrs × 500 PDFs = 78.5 hrs
  - Annual savings: 78.5 hrs/month × $15/hr × 12 months = $14,130


---

## 🤝 Contributing

1. Fork repo
2. Update `make-scenario.json` or `README.md`
3. Submit PR

---

