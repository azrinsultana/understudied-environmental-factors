

---

## Overview

This repository presents an NLP-based research framework for mining understudied environmental factors associated with chronic diseases from large-scale biomedical literature.

Chronic diseases such as cancer, cardiovascular disease, diabetes, stroke, asthma, and lung diseases are among the major causes of global mortality. Many well-known risk factors, including smoking, obesity, hypertension, air pollution, and physical inactivity, have already been widely investigated. However, several environmental exposures may also contribute to chronic disease development but remain less studied in biomedical research.

This project uses natural language processing, biomedical named entity recognition, BIO tagging, dictionary-based annotation, relation extraction, co-occurrence analysis, and impact-score-based ranking to identify hidden or neglected environmental factors from medical literature.



## Authors

Azrin Sultana  
American International University-Bangladesh, Dhaka, Bangladesh  
Email: 25-93678-1@student.aiub.edu  

MD. MAZID-UL-HAQUE  
American International University-Bangladesh, Dhaka, Bangladesh  
Email: mazid@aiub.edu  

Dip Nandi  
American International University-Bangladesh, Dhaka, Bangladesh  
Email: dip.nandi@aiub.edu  

---

## Research Aim

The main aim of this study is to develop a systematic NLP framework that can automatically identify understudied environmental factors linked with chronic diseases from large-scale biomedical abstracts.


Data sources include:

- PubMed;
- ScienceDirect;
- EMBASE;
- Web of Science;
- IEEE Xplore;
- Google Scholar.

Each article record includes bibliographic and textual information.

| Attribute | Description |
|---|---|
| PMID | Unique biomedical article identifier |
| Title | Title of the research article |
| Abstract | Main text used for NLP processing |
| Authors | Author names |
| Affiliation | Institutional information |
| Country | Country associated with the publication |
| Journal | Journal name |
| Year | Publication year |
| URL | Article access link |




## Requirements

Example Python libraries used in this project:

```text
pandas
numpy
scikit-learn
nltk
spacy
transformers
torch
matplotlib
seaborn
networkx
tqdm
biopython
label-studio
```

## Citation

If you use this work, please cite:

```bibtex
@article{sultana2026mining,
  title={Mining Chronic Diseases Understudied Environmental Factors from Medical Literature Using Natural Language Processing},
  author={Sultana, Azrin and Nandi, Dip},
  journal={International Journal of Modern Education and Computer Science},
  year={2026},
  note={Manuscript}
}
```

---

## Keywords

```text
Biomedical NLP
Chronic Disease
Environmental Risk Factors
Named Entity Recognition
BIO Tagging
Relation Extraction
PubMed Mining
Medical Literature Mining
Disease-Factor Association
Understudied Factors
Public Health Informatics
Environmental Exposure
Transformer Models
BioBERT
DistilBERT
```

---

## License

This work is licensed under the Creative Commons Attribution 4.0 International License.

You are free to share and adapt the material with proper attribution.

---

## Acknowledgement

This project supports the use of natural language processing, biomedical text mining, and public health informatics to uncover overlooked environmental exposures that may contribute to chronic disease burden.

The framework can help researchers, healthcare professionals, and policymakers identify neglected environmental risk factors and prioritize future investigation.
