# hlt-internship-deliverables
This repo contains deliverable example scripts and instructions for accessing trained for models for Amber Converse's HLT internship.

## 1. Web Scraping
The first section of deliverables is related to web scraping. These scripts are available in directory 1_web_scraping. Available in this directory are the scraping templates for HTML and PDF scraping and a sample finished script that I completed for scraping FLACSO.

## 2. Annotated UN Corpus
The second section is for the annotated UN Corpus. This data is available in the directory 2_annotated_un_corpus. Available in this directory is data_master.csv. data_master.csv contains the sentences in all languages used for training the models and labels for binary classification, multi-class classification, and a binary vector for multi-label classification (not used).

Each row in data_master.csv represents a single annotated document. The first 20 columns contain the language data for that sentence, in the native language and in all translations from multiple directions. The last 6 columns contain the annotations. The columns MatConf, MatCoop, VerConf, and VerCoop in combination form a binary label vector. Each of these columns is either a 0 or a 1, 0 meaning this sentence does not meet the category, and 1 meaning it does. Relevant is a binary label, 0 for irrelevant, 1 for relevant. QuadClass represents the QuadClass category of the sentence in numerical rather than binary format, 0 corresponds to irrelevant, 1 to Material Conflict, 2 to Material Cooperation, 3 to Verbal Conflict, and 4 to Verbal Cooperation. Note that this column cannot represent sentences with multiple labels, so if a sentence has multiple labels, the value for this column is -1 for invalid. If using this column as labels for multi-class training, any sentence with a -1 in this column should be excluded.

## 3. Pre-Trained ConfliBERT Spanish v2
The third section is for pre-trained ConfliBERT models. These models are not hosted on this repo, but can be accessed via Hugging Face API at the following paths:
* ConfliBERT-Spanish-mBERT-Cased: TBA
* ConfliBERT-Spanish-mBERT-Uncased: TBA

## 4. Fine-Tuned Models
The fourth section contains fine-tuned ConfliBERT model trained on the annotated UN Parallel Corpus and the annotated LEOKA Corpus. Only the highest performing models are made available. These models are not hosted on this repo, but can be accessed via Hugging Face API at the following paths:
* Relevant vs. Irrelevant to PLOVER Binary Classification:
  * ConfliBERT-English-Scr-Unc-Binary: TBA
  * ConfliBERT-Spanish-BETO-Case-Binary: TBA
  * ConfliBERT-Arabic-AraBERT-Unc-Binary: TBA
* QuadClass Multi-Class Classification:
  * ConfliBERT-English-Scr-Case-Quad: TBA
  * ConfliBERT-Spanish-mBERT-Unc-Quad: TBA
  * ConfliBERT-Arabic-mBERT-Unc-Quad: TBA
* LEOKA Multi-Label Classification:
  * ConfliBERT-English-Scr-Unc-LEOKA-ML: TBA
  * BERT-base-Unc-LEOKA-ML: TBA
