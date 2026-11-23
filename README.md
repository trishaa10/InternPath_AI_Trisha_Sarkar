# InternPath AI – Smart Internship Finder for Tier-2/3 Students

**Author:** Trisha Sarkar | **Institution:** Institute of Engineering & Management (IEM), Kolkata  
**Program:** AI Careers for Women – LinkedIn & Microsoft Fellowship (2026)  
**Category:** EdTech & Workforce Development (Career Analytics & Skill-Matching)  
**UN SDG Alignment:** SDG 8 (Decent Work & Economic Growth – Target 8.6) & SDG 5 (Gender Equality)

---

## 📌 Overview
Undergraduate students across Tier-2 and Tier-3 cities in India spend **4–6 hours every week** manually scrolling fragmented WhatsApp groups, Telegram channels, campus notice boards, and generic job portals—resulting in an **84% missed-deadline rate** and **<5% application response rates** (validated via a primary student survey of $n = 45$ non-metro undergraduates).

**InternPath AI** solves this discovery gap through a transparent, zero-infrastructure analytics and generative AI workflow that transforms scattered internship postings into ranked, skill-and-location-matched opportunities complete with `<72-hour` urgent deadline alerts and verified plain-language skill-gap guidance.

---

## 🎯 Key Features
* **Multi-Channel Aggregation & Deduplication:** Standardises 1,000+ raw internship listings across portals and regional channels using **Microsoft Excel (Power Query)**.
* **Weighted Skill & Location Match Engine:** Scores student-to-role compatibility in **Python (Pandas/NLP)** using a transparent composite index:
  $$\text{Match Score (\%)} = (0.60 \times \text{Technical Skill Overlap \%}) + (0.25 \times \text{Location/Remote Tier Fit}) + (0.15 \times \text{Stipend Women-Friendly Verification Flag})$$
* **Interactive Power BI Dashboard & Deadline Alerts:** Features dynamic slicers (`Required Skill`, `Location Tier`, `Work Mode`, `Deadline Alert Status`), DAX KPI cards, and automated **`<72-hour` Urgent Deadline Alerts**.
* **Women-Centric Remote & Safety Filtering (SDG 5):** Highlights verified remote, hybrid, and stipend-backed flexible internships (`Women_Friendly_Flag`) to overcome regional travel and safety barriers.
* **Verified AI Skill-Gap Tips:** Uses structured **Copilot / ChatGPT** prompt templates to generate 3-step upskilling tips for roles scoring `50%–74%`, strictly cross-checked against Power BI dataset metrics to eliminate AI hallucinations.

---

## 🛠️ Tech Stack
| Layer | Tool / Technology | Purpose |
| :--- | :--- | :--- |
| **Data Cleaning & ETL** | Microsoft Excel (Power Query) | Deduplication (`Listing_ID` + composite keys), missing-value handling, and deadline helper columns |
| **Matching & NLP** | Python (`Pandas`, `NumPy`) | Multi-tag skill parsing, composite match scoring, and missing-skill frequency extraction |
| **BI & Visualisation** | Power BI Desktop (DAX) | Star-schema data model, interactive slicers, KPI cards, and `<72-hr` deadline countdowns |
| **Generative AI** | Microsoft Copilot / ChatGPT | Plain-language skill-gap tips & priority alerts governed by a human-in-the-loop verification log |

---

## 📂 Repository Structure
```text
InternPath_AI_Project/
├── data/
│   ├── raw_internship_listings.csv          # Anonymised multi-channel postings (1,000+ records)
│   ├── cleaned_internpath_dataset.xlsx      # Power Query standardised dataset with deadline flags
│   └── student_survey_summary_n45.csv       # Anonymised Tier-2/3 student survey responses (n = 45)
├── notebooks/
│   └── skill_location_matching.ipynb        # Python (Pandas) skill-overlap & weighted scoring script
├── dashboard/
│   └── InternPath_AI_Dashboard.pbix         # Interactive Power BI report with DAX measures & slicers
├── docs/
│   ├── InternPath_AI_Project_Report.pdf     # Full fellowship capstone documentation
│   └── verified_ai_prompt_log.md            # Structured prompt templates & dataset cross-checks
└── README.md
