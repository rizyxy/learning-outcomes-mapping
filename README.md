# Mapping Learning Outcomes to SFIA Using Natural Language Processing (NLP)
### *Automated Curriculum Alignment for Information Systems Education*

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![NLP](https://img.shields.io/badge/NLP-Natural%20Language%20Processing-blueviolet)
![Framework](https://img.shields.io/badge/SFIA-Version%209-lightgrey)

## 📌 Project Overview
Aligning academic curricula with industry standards is essential for graduate employability. This project automates the mapping of **Course Learning Outcomes (CLO)** from the Universitas Airlangga Information Systems program to the **Skills Framework for the Information Age (SFIA)**. 

By leveraging various NLP techniques, we developed a system that identifies educational gaps and skill alignments, significantly reducing the manual effort required by academic committees.

### Key Highlights:
* **Automated Mapping Pipeline:** Developed a workflow to link unstructured textual learning outcomes to standardized global competency frameworks.
* **Skill Extraction & Enrichment:** Integrated **SkillNER** for entity recognition and **Query Expansion (QE)** to improve document matching through synonyms and hyponyms.
* **Comparative Analysis:** Evaluated multiple vectorization techniques including **TF-IDF**, **DistilBERT**, and **RoBERTa**.
* **Expert Validation:** Benchmarked system performance against a "Ground Truth" established by academic experts using Precision, Recall, and F1-Score.

---

## 🛠️ Methodology

The research follows a structured 5-step computational pipeline:

1.  **Data Extraction:** Scraped 37 core course syllabi and cleaned raw text using Regular Expressions (Regex).
2.  **Skill Extraction:** Utilized **SkillNER** to isolate specific technical competencies and professional roles within the curriculum.
3.  **Data Augmentation:** Applied **Query Expansion** strategies to enrich the textual data, increasing the semantic overlap between academic terms and SFIA definitions.
4.  **Feature Engineering:** Converted text into numerical vectors using both statistical (TF-IDF) and transformer-based (BERT) embedding methods.
5.  **Similarity Mapping:** Calculated alignment using **Cosine Similarity**, identifying matches between Learning Outcomes and the 196 skills defined in SFIA 9.

---

## 🚀 Key Findings

* **Top Performance:** The combination of **NLP Preprocessing + TF-IDF** achieved the best balance of precision and recall, yielding an **F1-Score of 41.17%**.
* **Transformer Insights:** While **DistilBERT** and **RoBERTa** models demonstrated exceptional Recall (100%), they tended to "over-map" generic terms, highlighting the effectiveness of TF-IDF for specific technical terminology.
* **Curriculum Gaps:** Successfully identified the top 10 most prominent skills in the curriculum, such as *Financial Analysis*, *Animation Development*, and *Accessibility & Inclusion*.

---
