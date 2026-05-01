# Mining Understudied Environmental Factors of Chronic Diseases Using NLP

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![NLP](https://img.shields.io/badge/NLP-Biomedical%20Text%20Mining-green)
![NER](https://img.shields.io/badge/Task-Named%20Entity%20Recognition-orange)
![Biomedical Text Mining](https://img.shields.io/badge/Domain-Biomedical%20Literature%20Mining-brightgreen)
![Status](https://img.shields.io/badge/Status-Research%20Prototype-purple)
![License](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey)

---

## Overview

This repository presents an NLP-based research framework for mining understudied environmental factors associated with chronic diseases from large-scale biomedical literature.

Chronic diseases such as cancer, cardiovascular disease, diabetes, stroke, asthma, and lung diseases are among the major causes of global mortality. Many well-known risk factors, including smoking, obesity, hypertension, air pollution, and physical inactivity, have already been widely investigated. However, several environmental exposures may also contribute to chronic disease development but remain less studied in biomedical research.

This project uses natural language processing, biomedical named entity recognition, BIO tagging, dictionary-based annotation, relation extraction, co-occurrence analysis, and impact-score-based ranking to identify hidden or neglected environmental factors from medical literature.

---

## Paper Title

Mining Chronic Diseases Understudied Environmental Factors from Medical Literature Using Natural Language Processing

---

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

The system is designed to:

- collect biomedical literature from major scientific databases;
- preprocess abstracts while preserving biomedical terms;
- identify disease and environmental factor entities;
- extract disease–factor relationships;
- rank environmental factors using frequency and disease diversity;
- detect underrepresented but potentially important environmental exposures;
- support future public health research and disease prevention.

---

## Why This Project Matters

Most chronic disease studies focus on already established risk factors such as:

- smoking;
- obesity;
- air pollution;
- hypertension;
- physical inactivity;
- diet-related factors.

However, many environmental factors receive less attention despite possible health risks. These neglected factors may affect human health through long-term exposure, occupational contact, contaminated water, indoor air, food additives, or industrial chemicals.

This project helps researchers identify hidden environmental exposures that may deserve more scientific attention.

---

## Dataset

The study processed more than 150,000 biomedical abstracts collected from multiple scientific databases.

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

---

## Methodology

The proposed framework follows a step-by-step biomedical NLP pipeline.

```text
Biomedical Literature Collection
        ↓
Text Cleaning and Preprocessing
        ↓
Environmental Factor Dictionary Construction
        ↓
Disease Dictionary Construction
        ↓
Named Entity Recognition
        ↓
BIO Tagging
        ↓
Disease–Factor Pair Extraction
        ↓
Relation Extraction
        ↓
Co-occurrence Analysis
        ↓
Impact Score Calculation
        ↓
Understudied Factor Identification
```

---

## Text Preprocessing

Text preprocessing was performed to convert raw biomedical abstracts into a cleaner and more machine-readable format.

The preprocessing pipeline includes:

- duplicate removal;
- missing abstract removal;
- abstract quality screening;
- sentence-level filtering;
- text cleaning and normalization;
- token normalization;
- abbreviation detection and expansion;
- selective stopword handling;
- lemmatization;
- entity-preserving punctuation handling.

Special care was taken to preserve important biomedical and chemical terms such as:

- PM2.5;
- PFAS;
- chemical names;
- disease names;
- environmental exposure terms;
- multi-word factor names.

---

## Named Entity Recognition

Named Entity Recognition was used to identify domain-specific entities from biomedical text.

The system identifies two main entity types:

| Entity Type | Meaning | Example |
|---|---|---|
| DISEASE | Chronic disease entity | Cancer, asthma, diabetes, coronary heart disease |
| FACTOR | Environmental factor entity | Biosolids, radon in water, mold spores, alkylphenols |

A hybrid NER strategy was used by combining:

- dictionary-based NER;
- manual validation;
- biomedical ontology-based dictionary construction.

The environmental factor dictionary was developed using internationally recognized sources such as:

- ChEBI;
- CTD;
- MeSH;
- ENVO;
- biomedical research articles.

The dictionary contains more than 2,000 environmental and disease-related factors across different categories.

---

## Environmental Factor Categories

| Category | Approximate Number of Factors |
|---|---:|
| Air Quality and Pollution | 100+ |
| Chemical Exposures | 200+ |
| Water Contaminants | 100+ |
| Food and Dietary Factors | 150+ |
| Soil and Land Contamination | 100+ |
| Climate and Weather Factors | 100+ |
| Built Environment | 200+ |
| Occupational Exposures | 150+ |
| Radiation Exposures | 100+ |
| Biological Factors | 150+ |
| Disease-Specific Factors | 180+ |
| Total | 2000+ |

---

## BIO Tagging

BIO tagging was used to label words or tokens in the text.

BIO means:

- B = Beginning of an entity;
- I = Inside an entity;
- O = Outside any entity.

Example:

```text
Radon        B-FACTOR
in           I-FACTOR
water        I-FACTOR
is           O
linked       O
to           O
cancer       B-DISEASE
```

This method helps the system correctly identify multi-word biomedical entities.

---

## Gold Standard Validation

A gold standard corpus was created to evaluate the quality of the NER system.

The study used:

- 500 manually annotated abstracts;
- stratified random sampling by publication decade and journal category;
- manual annotation using Label Studio;
- comparison between manual annotation and dictionary-based annotation.

The validation focused on two entity classes:

- FACTOR;
- DISEASE.

---

## Relation Extraction

After entity extraction, the system identifies possible relationships between environmental factors and chronic diseases.

The relation extraction process includes:

- dictionary-based relation extraction;
- co-occurrence-based relationship detection;
- linguistic pattern matching;
- dependency-aware relation extraction;
- graph-based analysis using dependency structure;
- manual validation of extracted disease–factor pairs.

Example extracted relations:

```text
Biosolids → Cancer
Radon in Water → Cancer
Alkylphenols → Cancer
Chlorine Dioxide → Cancer
Butyl Benzyl Phthalate → Asthma
Mold Spores → Lung Disease
Sulfites → Lung Disease
```

---

## Impact Score

The study ranks environmental factors using an impact score.

```text
Impact Score = Factor Frequency × Disease Diversity
```

Where:

- Factor Frequency means how often the factor appears in the literature;
- Disease Diversity means how many different chronic diseases are associated with that factor.

This helps identify factors that may be less studied but linked to multiple disease outcomes.

---

## Model Evaluation

Five transformer-based models were used to evaluate the quality of the NER dataset and extracted entities.

| Model | Precision | Recall | F1-score |
|---|---:|---:|---:|
| PubMedBERT | 0.8663 | 0.8819 | 0.8043 |
| DistilBERT | 0.9403 | 0.9586 | 0.9484 |
| SciBERT | 0.8991 | 0.8796 | 0.8869 |
| XLM-RoBERTa | 0.8271 | 0.8058 | 0.8121 |
| BioBERT | 0.9410 | 0.9335 | 0.9289 |

The best-performing model was DistilBERT, with an F1-score of 0.9484.

BioBERT also performed strongly, with an F1-score of 0.9289.

---

## Entity and Relation Extraction Performance

| Category | Precision | Recall | F1-score |
|---|---:|---:|---:|
| Chronic Disease Entity | 86.7% | 93.2% | 89.8% |
| Environmental Risk Factor Entity | 88.6% | 93.3% | 90.9% |
| Relation Extraction | 96.0% | - | - |

---

## Key Findings

The framework identified several understudied environmental factors that may be associated with chronic diseases.

| Environmental Factor | Associated Disease | Source Type | Relationship |
|---|---|---|---|
| Biosolids | Cancer | Human-made | Positive |
| Radon in Water | Cancer | Natural / Environmental | Positive |
| Alkylphenols | Cancer | Human-made | Positive |
| Chlorine Dioxide | Cancer | Human-made | Positive |
| Butyl Benzyl Phthalate | Asthma | Human-made | Positive |
| Mold Spores | Lung Disease | Natural | Positive |
| Sulfites | Lung Disease | Human-made | Positive |

---

## Understudied Factors Explained

### Biosolids

Biosolids are organic materials recovered from sewage treatment processes and often used as fertilizer. Although they contain useful nutrients, they may also carry contaminants such as PFAS, microplastics, antibiotic resistance genes, and other harmful compounds. These contaminants may accumulate in soil and create long-term risks for food safety and human health.

### Radon in Water

Radon is a naturally occurring radioactive gas produced from uranium decay in soil, rock, and groundwater. Radon in drinking water can enter indoor air during showering, cooking, or washing. It is mainly known for lung cancer risk, but radon in water may also contribute to stomach cancer risk.

### Alkylphenols

Alkylphenols are industrial chemicals used in detergents, plastics, paints, and other products. They are considered endocrine-disrupting chemicals because they can mimic estrogen and interfere with normal hormonal processes. They may affect reproductive health, inflammation, and cancer-related risks.

### Chlorine Dioxide

Chlorine dioxide is widely used as a disinfectant in water treatment and industrial processes. Although useful for microbial control, high exposure may cause respiratory irritation, blood-related effects, organ damage, and possible cancer-related concerns through disinfection by-products.

### Butyl Benzyl Phthalate

Butyl benzyl phthalate is a plasticizer used in PVC flooring, vinyl products, adhesives, paints, toys, packaging materials, and indoor products. It can be released into the environment and indoor dust. Children and pregnant women may be more vulnerable to exposure.

### Mold Spores

Mold spores are microscopic fungal particles found in damp indoor and outdoor environments. Long-term exposure to mold spores is associated with asthma, respiratory symptoms, hypersensitivity pneumonitis, and chronic lung diseases.

### Sulfites

Sulfites are widely used as preservatives in foods, beverages, and some medications. They help maintain food color and prevent microbial growth. However, sulfites trigger asthma-like symptoms, allergic responses, respiratory problems, and other health issues in sensitive individuals.

---

## Baseline vs Candidate Factors

The study compared widely studied baseline risk factors with candidate understudied factors.

Baseline factors include:

- lead;
- tobacco;
- air pollution;
- arsenic;
- occupational exposure.

Candidate understudied factors include:

- butyl benzyl phthalate;
- biosolids;
- alkylphenols;
- mold spores;
- chlorine dioxide;
- radon in water;
- sulfites.

This comparison showed that established risk factors receive much more publication attention, while several potentially harmful exposures remain relatively underrepresented in research.

---


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

---

## Usage

### Step 1: Preprocess biomedical abstracts

```bash
python src/preprocessing.py
```

### Step 2: Build environmental factor and disease dictionaries

```bash
python src/dictionary_builder.py
```

### Step 3: Run NER tagging

```bash
python src/ner_tagger.py
```

### Step 4: Generate BIO-tagged dataset

```bash
python src/bio_tagger.py
```

### Step 5: Extract disease–factor relationships

```bash
python src/relation_extraction.py
```

### Step 6: Calculate impact scores

```bash
python src/impact_score.py
```

### Step 7: Evaluate model performance

```bash
python src/evaluation.py
```

---

## Example Output

```text
Factor: Biosolids
Associated Disease: Cancer
Relation: Positive
Source Type: Human-made
Impact Status: Understudied
```

```text
Factor: Mold Spores
Associated Disease: Lung Disease
Relation: Positive
Source Type: Natural
Impact Status: Understudied
```

```text
Factor: Butyl Benzyl Phthalate
Associated Disease: Asthma
Relation: Positive
Source Type: Human-made
Impact Status: Understudied
```

---

## Visual Workflow

```text
+-----------------------------+
| Biomedical Abstracts        |
+--------------+--------------+
               |
               v
+-----------------------------+
| Text Cleaning               |
+--------------+--------------+
               |
               v
+-----------------------------+
| Dictionary Construction     |
+--------------+--------------+
               |
               v
+-----------------------------+
| Named Entity Recognition    |
+--------------+--------------+
               |
               v
+-----------------------------+
| BIO Tagging                 |
+--------------+--------------+
               |
               v
+-----------------------------+
| Disease-Factor Extraction   |
+--------------+--------------+
               |
               v
+-----------------------------+
| Relation Extraction         |
+--------------+--------------+
               |
               v
+-----------------------------+
| Impact Score Ranking        |
+--------------+--------------+
               |
               v
+-----------------------------+
| Understudied Factor Mining  |
+-----------------------------+
```

---

## Main Contributions

This project contributes:

- a scalable NLP framework for mining biomedical literature;
- a hybrid named entity recognition pipeline;
- dictionary-based and manually validated entity extraction;
- disease–environment relation extraction;
- impact-score-based factor prioritization;
- transformer-based evaluation using PubMedBERT, DistilBERT, SciBERT, XLM-RoBERTa, and BioBERT;
- identification of neglected environmental factors linked to chronic diseases.

---

## Limitations

This study has some limitations:

- The findings depend on the quality and coverage of collected abstracts.
- Dictionary-based NER may miss new, rare, or differently written entities.
- Some disease–factor relations may require further epidemiological or experimental validation.
- Publication bias may influence which factors appear understudied.
- The study mainly focuses on abstract-level information rather than full-text analysis.

---

## Future Work

Future improvements may include:

- expanding the dictionary with more biomedical ontologies;
- mining full-text articles instead of only abstracts;
- improving relation extraction using advanced graph neural networks;
- adding temporal trend prediction;
- integrating citation-based gap analysis;
- creating an open-source web dashboard;
- continuously updating the system with new PubMed articles;
- supporting researchers in public health risk prioritization.

---

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
