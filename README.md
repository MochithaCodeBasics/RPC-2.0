<h1 style="color:blue;"><b>DS RPC 2.0 : ADEGuard – AI-Powered Adverse Drug Event Detection and Severity Mapping</b></h1>

This is the starter repository for Codebasics's Resume Project Challenge 2.0.  

This project focuses on building an AI-powered pipeline to detect **Adverse Drug Events (ADEs)** from symptom text, group them into symptom-based and age-specific clusters, and classify each event by severity.

Please **fork this repository** to get started.

---


## 📂 Data Access Instructions

This repository already contains the **VAERS dataset** from the U.S. Vaccine Adverse Event Reporting System (VAERS).

- **Raw data** is stored in the `data/raw` folder as **year-wise ZIP files**.
- Each ZIP file corresponds to a specific year and contains **three CSV files**:
  1. **VAERSDATA.csv** → Main case and patient data  
  2. **VAERSSYMPTOMS.csv** → Coded adverse event terms using the **MedDRA** (Medical Dictionary for Regulatory Activities) terminology.  
     - Each report can have up to five coded symptoms (`SYMPTOM1`–`SYMPTOM5`), representing standardized MedDRA Preferred Terms (PTs).  
  3. **VAERSVAX.csv** → Vaccine/product details  


---

## 📝 Annotation Guidelines

Before starting annotation or model training, review the **Annotation Guidelines** in the `docs/` folder.  
They explain in detail:

- **ADE annotation rules** – how to identify Adverse Drug Events in text, including what to include and what to skip.
- **DRUG annotation rules** – how to label vaccine or drug mentions exactly as reported, handle brand names, code names, and generic terms.
- **Special cases** – rules for compound symptoms, repeated mentions, death/hospitalization references, and COVID-19 mentions.
- **Span formatting** – keeping longest medically accurate terms, excluding durations, and labeling each occurrence separately.
- **Quick checklist** – a step-by-step reminder to ensure annotations are consistent and compliant.

📌 **Tip:** Following these rules strictly ensures the labels are high quality and consistent, which is critical for training the NER model effectively.

---

### 📌 Learn More
Visit the **[challenge page](https://codebasics.io/)** to learn more: **DS RPC-02**
