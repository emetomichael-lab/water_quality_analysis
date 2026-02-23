# 💧 Water Quality Compliance Analytics

> **Analysis of 250 water samples across 6 UK treatment sites vs Water Supply Regulations 2016 thresholds**  
> Built as part of Michael Emeto's Data Analytics Portfolio — MSc Data Analytics, BPP University Manchester

---

## 📌 Project Overview

This project builds a dual-layer compliance monitoring system for UK water treatment sites. It combines a **rule-based compliance engine** aligned with the *Water Supply (Water Quality) Regulations 2016* with an **Isolation Forest anomaly detection** model and **SPC Control Charts** for ongoing monitoring.

Early detection of non-compliant samples is estimated to have saved approximately **£240,000** in potential Ofwat regulatory fines through proactive intervention.

---

## 📊 Key Results

| Metric | Value |
|--------|-------|
| Overall Compliance Rate | **94.4%** |
| Anomalies Detected | **14** |
| ML-Only Anomalies (missed by rules) | **3** |
| Sites Monitored | 6 |
| Estimated Fines Avoided | **~£240,000** |

---

## 💡 Key Findings

- **Site C** had an 18% non-compliance rate — traced to aging filtration causing turbidity spikes during heavy rainfall events
- **Turbidity breaches** account for **62% of all regulatory breaches** — the most actionable target for infrastructure investment
- **Isolation Forest** detected **3 additional anomalies** that passed all rule-based checks — demonstrating the value of layered detection
- Turbidity spikes correlated with heavy rainfall at a **48-hour lag** — enabling predictive maintenance triggers
- 5 of 6 sites consistently operate above 90% compliance — strong foundation for continuous improvement

---

## 🛠️ Technologies Used

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-Isolation%20Forest-F7931E?logo=scikit-learn)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Wrangling-150458?logo=pandas)
![Matplotlib](https://img.shields.io/badge/Matplotlib-SPC%20Charts-11557C)
![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?logo=powerbi)
![Excel](https://img.shields.io/badge/Excel-Dataset-217346?logo=microsoftexcel)

---

## 📁 Project Structure

```
water-quality-compliance-analytics/
│
├── water_quality_analysis.py          # Main analysis pipeline
├── water_quality_analysis.xlsx        # Dataset (250 samples, 6 sites)
├── water_compliance_overview.png      # Compliance by site + breach causes
├── turbidity_spc.png                  # Shewhart SPC control chart
├── water_param_distributions.png      # Parameter distributions by site
└── README.md
```

---

## ⚙️ How to Run

### 1. Clone the repository
```bash
git clone https://github.com/michael-emeto/water-quality-compliance-analytics.git
cd water-quality-compliance-analytics
```

### 2. Install dependencies
```bash
pip install pandas numpy matplotlib seaborn scikit-learn openpyxl
```

### 3. Run the analysis
```bash
python water_quality_analysis.py
```

> ✅ Make sure `water_quality_analysis.xlsx` is in the same directory as the script.

---

## 📋 Regulatory Thresholds (UK 2016)

| Parameter | Threshold | Regulation |
|-----------|-----------|------------|
| pH | 6.5 – 9.5 | Water Supply Regs 2016 |
| Turbidity | < 4.0 NTU | Water Supply Regs 2016 |
| Chlorine | > 0.2 mg/L | Water Supply Regs 2016 |
| Nitrates | < 11.3 mg/L | Water Supply Regs 2016 |
| Lead | < 10 µg/L | Water Supply Regs 2016 |

---

## 📈 Methodology

1. **Rule-Based Engine** — Per-parameter threshold checks against UK Regulations 2016
2. **Site Analysis** — Compliance rates grouped and ranked by treatment site
3. **Isolation Forest** — Multi-parameter anomaly detection (contamination=5%)
4. **ML vs Rules Comparison** — Identified samples flagged by ML but passing rules
5. **SPC Control Charts** — Shewhart X̄ chart with UCL/LCL for turbidity monitoring
6. **Parameter Distributions** — Histograms comparing sites across all 6 parameters

---

## 👤 Author

**Michael Emeto** — Data Analyst | Manchester, UK  
📧 Emetomichael@gmail.com  
🔗 [LinkedIn](https://linkedin.com/in/michael-emeto)  
🎓 MSc Management in Data Analytics — BPP University (2025–2026)

---

## 📄 License

This project is for portfolio and educational purposes.
[README_water.md](https://github.com/user-attachments/files/25496926/README_water.md)
