# Annotated Bibliography: Patient- and Data-Oriented Healthcare NLP

A companion resource to the tutorial *Healthcare NLP: where are we and what is next?* presented at LREC 2026.  
Materials: <https://github.com/4dpicture/HealthNLP>
Tutorial description: <https://arxiv.org/abs/2512.08617>


## Introduction: core papers

[Wu et al. (2022)](https://doi.org/10.1038/s41746-022-00730-6) survey clinical NLP projects in the United Kingdom between 2007 and 2022. They show that clinical NLP publications double every five years.

[Locke et al. (2021)](https://doi.org/10.1016/j.tacc.2021.02.007) provide an introductory and practical review of NLP in medicine. They cover tasks from information extraction to clinical decision support and make the topic accessible to a clinical audience.

[Spasic & Nenadic (2020)](https://doi.org/10.2196/17984) is a data-centric systematic review of clinical text datasets used in machine learning between 2010 and 2016. They provide an overview of corpora and annotation practices across specialties.

[Elvas et al. (2025)](https://doi.org/10.1016/j.ijmedinf.2025.105728) carry out a scoping review of NLP in medical text processing (2019–2023). They cover tasks from classification to information extraction and report work in multiple languages beyond English.

[Maddox et al. (2025)](https://doi.org/10.1056/NEJMsb2503956) summarise the progress generative AI has made in healthcare and the challenges that remain, as assessed by a National Academy of Medicine workshop of experts.



## Data layer

### Annotation

[Gurulingappa et al. (2012)](https://doi.org/10.1016/j.jbi.2012.04.008) set a good example of a text annotation process in the healthcare domain: they developed a benchmark corpus of nearly 3,000 case reports manually annotated with drugs and adverse effects, showing that guideline development should be a cyclic process guided by inter-annotator agreement until convergence.

An instance of a sophisticated guideline is proposed by [Schulz et al. (2023)](https://ceur-ws.org/Vol-3603/icbo2023_proceedings.pdf) to use the semantic standards SNOMED CT and HL7 FHIR. They design a hierarchical annotation schema with *core* and *sub*-concepts based on ontological principles, enriched with A-Box and T-Box annotations using symbolic and neural reasoning.

NER: [Yada et al. (2020)](https://aclanthology.org/2020.lrec-1.424/) aimed at a versatile annotation guideline using critical lung disease data. Their design avoids heavy medical-knowledge requirements by focusing on linguistic patterns, annotating entity types including diseases, anatomical entities, features, temporal expressions, medicines, and clinical context.

[Xia & Yetisgen-Yildiz (2012)](https://aclweb.org/anthology/W12-2404) discuss the challenges and strategies of clinical corpus annotation, emphasising the importance of involving NLP researchers early alongside clinical experts.

Non-English examples:
* [SemClinBr by Oliveira et al. (2022)](https://doi.org/10.1186/s13326-022-00264-6) for Portuguese electronic health records: a multi-institutional, multi-specialty semantically annotated corpus.
* [Codiesp by Miranda-Escalada et al. (2020)](https://ceur-ws.org/Vol-2696/) for Spanish clinical coding systems of medical documents, presented at the CodiEsp track of CLEF eHealth 2020.
* [CARDIO:DE by Richter-Pechanski et al. (2023)](https://doi.org/10.1038/s41597-023-02050-0), a distributable German clinical corpus of cardiovascular routine doctor's letters.
* [Becker et al. (2025)](https://doi.org/10.1016/j.ijmedinf.2025.106009) extend CARDIO:DE with additional annotation guidelines and an evaluation of NLP approaches for clinical applications.



### Ethical Concerns

[Suster et al. (2017)](https://aclanthology.org/W17-1602/) provide a short review of ethical challenges in clinical NLP, discussing data sanitisation, consent, secure access, and sources of less sensitive data; they also encourage reporting of model bias to avoid socially harmful impact.

[Benton et al. (2017)](https://aclanthology.org/W17-1612/) outline ethical research protocols for social media health research, emphasising the roles of Institutional Review Boards (IRBs), informed consent, de-identification, and the risks of data linking.

[Lewis et al. (2017)](https://aclanthology.org/W17-1607/) address the integration of personal data protection with open science in research ethics, offering practical guidance for the NLP community.

[Bear Don't Walk et al. (2022)](https://doi.org/10.1093/jamiaopen/ooac039) present a scoping review of ethics considerations in clinical NLP, analysing 22 papers through the lens of bias and fairness, with attention to the ML development pipeline (design, data, algorithm, critique).

[Khattak et al. (2023)](https://doi.org/10.47992/IJAHCA.2581.6373.0083) discuss ethical considerations and challenges in deploying NLP systems in healthcare. They cover data privacy, security, model bias, medical liability, explainability, and transparency.

[Fu et al. (2023)](https://doi.org/10.1111/cts.13459) conduct a scoping review of recommended practices and ethical considerations for NLP-assisted observational research, emphasising the WHO's six principles for ethical AI use in health: protecting autonomy, promoting human well-being, ensuring transparency, fostering accountability, ensuring inclusiveness, and promoting sustainability.

[Bak et al. (2025)](https://doi.org/10.2196/65566) report on the embedded ethics review of our EU-funded 4D PICTURE project on cancer patient quality-of-life support, introducing ideas such as an embedded ethicist position, psychological safety in research teams, and anticipating techno-moral change.



### Health Data Governance

[Jones et al. (2020)](https://doi.org/10.2196/16760) conduct a UK network study on developing data governance standards for reusing clinical free text in health research. They identify barriers around authoritative guidance, public transparency, de-identification efficacy, and the use of accredited data safe havens.

[Di Iorio et al. (2021)](https://doi.org/10.1136/medethics-2020-107011) survey data protection and governance in health information systems across 15 centres in 10 European countries. They find high variability in privacy practices and proposing a Privacy and Ethics Impact and Performance Assessment (PEIPA) methodology.

[Wang et al. (2022)](https://doi.org/10.2196/32361) describe the big data platform of West China Hospital (online since 2020). They cover more than 12 million patients, 75 million visits, and 8,475 data variables. This is an example of large-scale clinical data governance in practice.

[Lopez-Perez et al. (2023)](https://doi.org/10.1007/978-3-031-49068-2_32) present a Rare Cancer Data Ecosystem for the European healthcare setting, using emerging interoperability technologies and AI to improve data quality and organisation for rare cancer patient care.

[Arigbabu et al. (2024)](https://doi.org/10.9734/ajrcos/2024/v17i3418) study data governance in AI-enabled healthcare via a survey of 843 users. They find a positive link between awareness of AI projects and trust in healthcare providers, and stress the importance of transparent communication about data use.

Promising technical approaches for safer data access include **federated learning** ([Xu et al., 2021](https://doi.org/10.1007/s41666-020-00082-4); [Nguyen et al., 2022](https://doi.org/10.1145/3501296); [Antunes et al., 2022](https://doi.org/10.1145/3501813)) and **access-level control** ([Abouelmehdi et al., 2018](https://doi.org/10.1186/s40537-017-0110-7); [Xiang & Cai, 2021](https://doi.org/10.1155/2021/9980551)).



### Use of Synthetic Data

[El Emam et al. (2024)](https://doi.org/10.1038/s41598-024-57207-7) evaluate the replicability of analyses using synthetic health data, a useful reference for the methodology of tabular synthetic data generation in the health domain.

[Belkadi et al. (2023)](https://openreview.net/forum?id=yYIL3uhQ8i) introduce LT3 (Label-To-Text Transformer), a model that generates synthetic medical prescriptions conditioned on label vocabularies, enabling NER training without access to real patient data. Models trained on the synthetic data achieve 96–98% F1 on the n2c2-2018 medication extraction task.

[Ren et al. (2025)](https://doi.org/10.3389/fdgth.2025.1497130) present **Synthetic4Health**, a pipeline for generating annotated synthetic clinical letters from structured knowledge, evaluated for lexical similarity, utility (train-on-synthetic, test-on-real), and diversity.

[Kattenberg (2025)](https://theses.liacs.nl/3496) generates a synthetic Dutch medical dataset of episode descriptions using a fine-tuned GPT-2 model conditioned on ICPC class labels. He demonstrates reasonable classification accuracy but reduced diversity compared to real data.

[Belkadi et al. (2025)](https://doi.org/10.1109/ICHI64508.2025) introduce **MLM4SynMed**, using masked language modelling to generate synthetic free-text medical records, extending synthetic data generation to a more challenging and heterogeneous text type.



## NLP layer

### Classification and Prediction Models

[Beeksma et al. (2019)](https://doi.org/10.1186/s12911-019-0775-2) use an LSTM recurrent neural network on electronic medical records to predict life expectancy, demonstrating that sequential models can assist clinicians in timely end-of-life conversations based on prognostication.

[Shmatko et al. (2025)](https://doi.org/10.1038/s41586-025-09529-3) present **Delphi**, a transformer-based generative model trained on large-scale UK Biobank health records to learn long-term disease progression trajectories, enabling multi-disease risk prediction over decades and capturing comorbidity patterns.

[Liang et al. (2025)](https://doi.org/10.1016/j.tjog.2025.02.006) fine-tune Llama-2-13B with AI-generated medical diagnoses for ICD coding in gynaecologic oncology, showing a practical route to using LLMs for clinical classification with limited real labelled data.



### Entity Recognition and De-identification

[Belkadi et al. (2023)](https://doi.org/10.1109/BigData59044.2023.10386154) compare pre-trained encoder-based language models (BERT, BioBERT, ClinicalBERT) fine-tuned for drug and adverse drug effect entity recognition. They find that domain-specific models achieve similar F1 (0.84) to general BERT despite higher precision.

[Romero et al. (2025)](https://aclanthology.org/2025.cl4health-1.26/) investigate ensemble learning over eight diverse encoder-based models (including RoBERTa-L, BioMedRoBERTa, and PubMedBERT) for medication extraction. Their non-BIO word-level ensemble reaches a macro-F1 of 0.8821, while BIO-aware max-logit voting reaches 0.8232.

[Magge et al. (2021)](https://doi.org/10.1093/jamia/ocab114) present **DeepADEMiner**, a deep learning pharmacovigilance pipeline for extracting and normalising adverse drug event mentions from Twitter, combining NER with entity normalisation to a medical ontology.

[Dirkson et al. (2022)](https://doi.org/10.1038/s41598-022-13894-8) show that automated NLP extraction from online patient forums (GIST Support International on Facebook) can complement pharmacovigilance data for rare cancers, identifying drug–side-effect relations not yet in official databases.

[Wang et al. (2025)](https://aclanthology.org/2025.findings-naacl.239/) introduce **GPT-NER**, a few-shot NER approach using generative LLMs. It cannot beat a fine-tuned model when labelled data is plentiful, but significantly outperforms supervised models when training data is extremely scarce.



### Biomedical Entity Linking

[Liu et al. (2021)](https://aclanthology.org/2021.naacl-main.334/) propose **SapBERT** (Self-Alignment Pretraining for Biomedical Entity Representations), which uses contrastive learning on UMLS synonyms to bring synonym embeddings closer together than non-synonyms, establishing a strong baseline for biomedical entity linking.

[Hartendorp et al. (2024)](https://aclanthology.org/2024.cl4health-1.31/) adapt SapBERT for Dutch by fine-tuning on an automatically generated Wikipedia corpus, then apply it to a Dutch cancer patient forum (kanker.nl), reporting that NER errors are currently a larger bottleneck than the linker itself.

[Mazzucato et al. (2026)](https://doi.org/10.64898/2026.01.22.26344605) explore both NER and entity linking with decoder-only LLMs (GPT-4o) in a cross-lingual setting (Dutch and Italian EHRs, CLEF eHealth data), endorsing the potential of generative LLMs for multilingual healthcare data harmonisation.



### Relation Extraction

*(Left out from the tutorial)*



### Sentiment Analysis

[Mæhlum et al. (2024)](https://aclanthology.org/2024.cl4health-1.2/) introduce the **Norwegian Patient Comment corpus (NorPaC)** for sentiment analysis of patient feedback and evaluate Norwegian language models on the task, including zero-shot settings.

[Rønningstadal et al. (2025)](https://aclanthology.org/2025.nodalida-1.58/) explore within- and cross-domain training for Norwegian patient feedback sentiment. They find that fine-tuned BERT and T5 models outperform zero- and few-shot LLMs on four-way sentiment, and that out-of-domain data (NoReC) can improve in-domain results when in-domain data is limited.

[Storset et al. (2026)](https://aclanthology.org/2026.healing-1/) extend NorPaC with aspect categories aligned to patient-centred care quality dimensions and their associated sentiment labels. They find that joint training on aspect extraction and sentiment outperforms a pipeline approach.

[Lal et al. (2024)](https://aclanthology.org/2024.cl4health-1.9/) conduct emotion and sentiment analysis of 1,500 Reddit posts about cancer stages and treatments, using pre-trained BERT-like and lexicon-based models. They highlight the challenges of contradictory emotions and posts requiring additional context.



### Summarization, Simplification, and Translation

*(Left out from the tutorial)*



### Explainable NLP

*(Left out from the tutorial)*



## Patient layer

### Privacy

De-identification is a key prerequisite for releasing clinical NLP data. [Shaji et al. (2024)](https://arxiv.org/abs/2405.12630) de-identify clinical texts using biomedical BERT variants with comprehensive risk assessment, contributing to the MORMOR-KARL shared task at LEGAL 2026.

Patients' attitudes towards health data sharing are explored by [Subramanian et al. (2024)](https://doi.org/10.2196/51439), who find that HIPAA does not fully prevent data breaches and explore industry-standard alternatives. [O'Herrin et al. (2004)](https://doi.org/10.1097/01.sla.0000128307.98274.dc) report that HIPAA increases workload and dropout rates for medical records research.



### Public and Patient Involvement and Engagement (PPIE)

[Moschogianis et al. (2025)](https://doi.org/10.21203/rs.3.rs-7264851/v1) study the feasibility and added value of electronic patient-generated data (questionnaires) for people with musculoskeletal conditions, demonstrating how patient-reported data can feed into NLP workflows.

The **iPOF project** (investigative research into the experiences of online forum users) illustrates ethical NLP on mental health forum data (patient support groups). It developed a comprehensive ethics framework drawing on UK Government Data Ethics, BPS Internet-Mediated Research guidelines, and NHS Trust approval, published at <https://www.lancaster.ac.uk/health-and-medicine/research/>.



### Analysis of patient narratives

[Han et al. (2026)](https://aclanthology.org/2026.cl4health-1.8/) extract metaphors from Dutch cancer patients' interviews and forum data using LLMs combined with human-in-the-loop validation. They connect to the broader **Metaphor Menu** project (<https://wp.lancs.ac.uk/melc/>) that develops multilingual conversation tools for cancer patients.

[Lal et al. (2024)](https://aclanthology.org/2024.cl4health-1.9/) analyse cancer narratives from Reddit to understand the emotional content around stages and treatments, providing insights into how patients articulate their health experiences in informal language.

[Lal et al. (2025)](https://aclanthology.org/2025.coling-demos.3/) present **LENS** (Learning Entities from Narratives of Skin Cancer), a system demonstration for extracting medical entities from cancer patient narratives in social media.



### Shared Decision Making (SDM)

[Oueslati et al. (2026)](https://doi.org/10.1016/j.pec.2025.108623) study shared decision making with ethnic minorities in oncology through interviews, identifying language barriers and the need for culturally tailored information. They point to NLP tasks such as simplification, translation, and metaphor integration as important research directions.

[Kidanemariam et al. (2024)](https://doi.org/10.1016/j.pec.2024.108189) analyse clinical consultations in diabetes care using qualitative methods, showing how patients and clinicians collaborate to make care fit individual preferences and values. This forms a basis for designing conversational NLP tools that support person-centred SDM.




