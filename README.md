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
- **Labor Savings**: 78 hrs/month (estimated) — **$14,040 annual savings**

---

## ⚙️ Workflow Steps

1. **Trigger**: Jotform “New Submission” webhook
2. **Fetch & Parse PDF**: PDF.co “AI Invoice Parser”
3. **Load**: Google Sheets “Add Rows” (transactions)

---

## 🏗 Architecture

```
Jotform → Make.com Scenario → PDF.co → Google Sheets
```

---

## 🏛 Tech Stack

- **No–Code**: Make (Integromat)
- **Form Input**: Jotform API 
- **PDF Parsing**: PDF.co 
- **Data Store**: Google Sheets

---

## 🚀 Setup & Deployment

1. **Clone Repo**
   ```bash
   git clone https://github.com/your-username/bank-statement-automation.git
   cd bank-statement-automation
   ```

2. **Import Make.com Scenario**
   - In Make.com: **Scenarios → Create a new scenario → Import** → upload `Bank Statement Automation.json`

3. **Configure Connections**
   - Jotform API Key → [Connect Jotform to Make](https://apps.make.com/jotform)
   - PDF.co API Key → [Connect PDF.co to Make](https://apps.make.com/pdfco)
   - Google Sheets OAuth → [Connect PDF.co to Make](https://apps.make.com/google-sheets)

4. **Deploy**
   - Turn scenario **ON**

---

## 📊 Metrics & Results

| Metric                   | Manual (Estimated) | Automated (Measured/Estimated) | Improvement       |
|--------------------------|--------------------|-------------------------------|--------------------|
| Processing Time per PDF  | 10 min             | 37 sec (measured)             | –93.8%             |
| Monthly Throughput       | 100                | 500 (estimated)               | +400%              |
| Error Rate               | 1% (estimated)     | <0.05% (estimated)            | –95%               |
| Monthly Hours Saved      | —                  | 78 hrs (calculated)           | +78 hrs            |
| Annual Labor Savings     | —                  | $14,040 (calculated)          | +$14,040           |

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

- **Manual Estimate**: 1% error rate is a commonly accepted average for manual data entry tasks. 
- **Automated Estimate**: <0.05% error rate is based on the high accuracy rates of automated data entry systems, which typically boast accuracy rates of 99.959% to 99.99%.

### 💰 Labor Savings

- **Calculation**:
  - Time saved per PDF: 10 min (manual) – 37 sec (automated) = 9.23 min ≈ 0.156 hrs
  - Monthly savings: 0.156 hrs × 500 PDFs = 78 hrs
  - Annual savings: 78 hrs/month × $15/hr × 12 months = $14,040


---

## 🤝 Contributing

1. Fork repo
2. Update `make-scenario.json` or `README.md`
3. Submit PR

---

