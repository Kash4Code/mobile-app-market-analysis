# Cross-Platform Mobile App Market Analysis

An end-to-end data analytics project examining **18,000+ free mobile applications** across the **Google Play Store** and **Apple App Store** to identify market trends, evaluate user engagement metrics, and formulate data-driven monetization strategies.

---

## 📌 Business Problem & Key Objectives

For developers aiming to launch free apps funded by in-app ads, identifying profitable, low-competition market niches is crucial. 

This project aims to:
1. **Clean & Standardize** multi-platform app datasets across distinct app store environments.
2. **Analyze User Engagement** across 30+ app categories.
3. **Recommend Strategic Growth Niches** that offer high cross-platform audience reach and strong revenue potential.

---

## 📊 Key Insights & Business Outcomes

* **Data Integrity Restored:** Processed 18,000+ app records, stripping non-ASCII artifacts and removing 1,100+ duplicate app listings.
* **Target Niche Identification:** **Books & Reference** and **Weather** categories demonstrated high average install counts alongside moderate competition, making them primary candidates for ad-supported free models.
* **Strategic Roadmap:** Proposed a three-phase deployment model starting with a minimal functional release on Android to test engagement, followed by cross-platform rollout on iOS.

---

## 🛠️ Tools & Technologies Used

* **Language:** Python 3.x
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn
* **Environment:** Jupyter Notebook / VS Code

---

## 📁 Repository Structure

```text
├── data/               # Raw and processed app store datasets
├── notebooks/          # Exploratory Data Analysis & cleaning steps
├── visuals/            # Exported charts and summary graphs
├── .gitignore          # Files Git should ignore
├── README.md           # Documentation
└── requirements.txt    # Project dependencies
```

---

## 🚀 How to Run the Project Locally

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/mobile-app-market-analysis.git](https://github.com/your-username/mobile-app-market-analysis.git)
   cd mobile-app-market-analysis
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the analysis:**
   Open `notebooks/app_analysis.ipynb` in Jupyter Notebook or VS Code and execute all cells.
