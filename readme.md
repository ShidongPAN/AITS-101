# AITS-101: Government AI Transparency Statements in Australia

AITS-101 is a curated dataset of **101 publicly available AI Transparency Statements (AITS)** collected from **Australian Government agencies**. The dataset supports research on public-sector AI transparency, regulatory disclosure, document analysis, and AI governance. It was introduced in the paper *The Creation and Analysis of Government AI Transparency Statements in Australia*. 

The dataset was constructed as the **first systematic corpus of government AI transparency statements**, with the goal of enabling stylometric, quantitative, and qualitative analyses of how AI transparency requirements are documented and operationalised in practice.

## Overview

Australia’s **Policy for the Responsible Use of AI in Government** requires non-corporate Commonwealth entities to publish AI Transparency Statements on their public websites. These statements are intended to explain how AI systems are used in practice. AITS-101 compiles these disclosures into a reusable research dataset.

Basic dataset statistics:

- **101** AI Transparency Statements


## What is included

This repository contains the AITS-101 dataset and supporting resources for reproducing the analyses in the paper. Depending on the release version, the repository may include:

- raw source metadata for collected AITS
- preprocessed plain-text versions of statements
- taxonomy of AITS composition
- L1 annotation based on the AITS taxonomy

## Repository structure

```text
AITS-101/
├── README.md
├── LICENSE
├── data/
│   ├── raw/
│   ├── processed/
│   ├── annotations/
│   └── metadata/
├── taxonomy/
│   └── annotation_taxonomy.xlsx
└── paper/
```


## Preprocessing

Collected statements appeared in heterogeneous formats, including **HTML webpages, PDFs, DOCX files, and statements embedded within broader policy documents**. To enable consistent analysis, all AITS were converted into plain text.

Notably, the numbering ranges from 1 to 104 but is **non-consecutive**: AITS entries are absent for IDs 18, 20, and 85.

## Annotation scheme

The annotation scheme was developed through an iterative top-down process, starting from official AITS requirements and refining categories based on observations from the corpus. The final scheme contains **10 L1 categories**. Notably, even though we provide L2 annotation, we did not perform and provide any L2 annotation in the current stage.

### Level-1 annotation categories

1. **Definition of AI**  
   Statements describing the meaning, scope, or boundaries of AI as used by the agency.

2. **General introduction**  
   Introductory or contextual content providing an overview of the AI Transparency Statement. 

3. **Intention of AI**  
  The intentions behind why the agency uses AI or is considering its adoption.

4. **AI usage patterns**  
   The classification of AI use according to usage patterns, as defined by the Attachment A - Classification system for AI use.

5. **AI usage domains**  
   Classification of AI use according to usage domains, as defined by the Attachment A - Classification system for AI use.

6. **Impact to the public**  
   Classification of use where the public may directly interact with, or be significantly impacted by, AI or its outputs without human review.

7. **Monitoring measures**  
   Measures to monitor the effectiveness of deployed AI systems and protect the public against negative impacts.

8. **Compliance with AI regulations and policies**  
   Mentions of specific compliance or applicable legislation and regulations.

9. **Update**  
   Statements about the AITS update, such as the publish date or the update frequency. 

10. **Contact**  
    Contact Information, such as the email address for public enquiries.

The paper notes that these categories were annotated over **2,923 sentences**, and that **“EMPTY”** is treated as a valid value for sentences without semantic meaning. 

## Why this dataset is useful

AITS-101 supports research in:

- AI governance and transparency
- public-sector AI adoption
- policy and regulatory disclosure analysis
- NLP for long-form institutional documents
- readability and plain-language assessment
- comparative studies with privacy policies and related disclosures

The paper uses the dataset for three complementary forms of analysis:

- **stylometric analysis**
- **quantitative composition analysis using a fine-grained annotation taxonomy**
- **qualitative analysis of recurring disclosure patterns** 

## Main findings reported in the paper

Using AITS-101, the paper reports several key findings:

- AITS are relatively short, with a mean of **554 words** and a median around **498 words**
- AITS are structurally simpler than privacy policies
- the median Flesch Reading Ease Test score (readability) is **14.16**, suggesting that these documents remain difficult for the general public to understand
- only **40.59%** of AITS explicitly define AI


## License

This dataset is licensed under the Creative Commons Attribution 4.0 International License (CC-BY-4.0).

The dataset is compiled from publicly available AI Transparency Statements published by Australian Government entities. 
Users are responsible for ensuring that their use of the dataset also complies with any applicable terms, copyright rules, and source-specific conditions associated with the original materials.

## Citation

If you use this dataset, please cite the corresponding paper:

```text
@article{pan2026creation,
  title={The Creation and Analysis of Government AI Transparency Statements in Australia},
  author={Pan, Shidong and Gong, Haochen and Xia, Boming and Sun, Xiaoyu and Xu, Xiwei and Zhu, Liming},
  journal={arXiv preprint arXiv:2604.26075},
  year={2026}
}
```
