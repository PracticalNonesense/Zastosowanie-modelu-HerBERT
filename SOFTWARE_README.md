This readme file was generated on [2026-06-10] by Kacper Wójcik

GENERAL INFORMATION

- Project name: Zastosowanie-modelu-HerBERT
- Version: 2.0
- Short description: A multi-task NLP project that fine-tunes the Polish HerBERT model to jointly classify sentiment and sarcasm in social media comments written in Polish.

PROJECT OVERVIEW

- Full description: This project implements a multi-task transformer-based classifier for Polish social media comments, using the allegro/herbert-base-cased model as a shared encoder with two task-specific heads: one for sentiment (e.g., positive / neutral / negative) and one for sarcasm (binary). The software loads labeled comment data from Excel files, performs preprocessing and train–test splits, tokenizes using Hugging Face tokenizers, and trains a custom PyTorch module via the Hugging Face Trainer API. It then evaluates the model with accuracy, macro F1, and confusion matrices, and exposes helper functions to run inference on new comments, returning both sentiment and sarcasm probabilities in a tabular form.
- Date of creation: (2025-06-15 - 2026-04-22)
- Project Organization: Python source code file(s) or notebook with training, evaluation and inference logic, no pre-compiled binaries, informal tests embedded as evaluation and sample inference, Excel datasets komentarze.xlsx and sarkazm.xlsx, no dedicated build scripts, documentation mainly as inline comments and a short overview, static resources limited to Excel data and saved model directories such as ./herbert_sentiment_model and ./herbert_sentiment_final
- Software project size: 320KB (uncompressed)


INSTALLATION

- Step by step instructions: step by step instructions: install Python 3.10+ or a recent 3.x, create and activate a virtual environment, install dependencies with pip (torch, transformers, datasets, pandas, numpy, scikit-learn, matplotlib, seaborn, openpyxl, safetensors), create a Komentarze directory and place komentarze.xlsx and sarkazm.xlsx inside it, save the main training/evaluation script (e.g. main.py) in the project root with correct paths, optionally copy a pre-trained model directory such as ./herbert_sentiment_final into the project, run training and evaluation with python main.py
- System requirements: Linux, macOS or Windows 10/11, CPU with at least 8 GB RAM recommended, optional CUDA-capable GPU for faster training, approximately 1–2 GB free disk space for models, checkpoints and data
- Required libraries, packages, modules: torch, transformers, datasets, pandas, numpy, scikit-learn, matplotlib, seaborn, openpyxl, safetensors
- Setup requirements: optional configuration of paths for komentarze.xlsx sarkazm.xlsx, optional environment variables or small config module for MODEL_NAME, data paths and output directories, no mandatory environment variables beyond standard Python and CUDA configuration
- Known issues: slow training on CPU compared to GPU, possible version-related warnings about unexpected keys in state_dict when loading checkpoints if transformers or torch versions change, need to retrain or carefully manage label encodings if sentiment classes in the Excel files are modified, occasional confusion for users when paths to Excel files or model directories are misconfigured


USAGE

- Step by step instructions: <run python main.py to launch training and evaluation, wait for training epochs to complete and metrics to be printed, inspect evaluation loss, accuracy, macro F1 and classification report in the console, view the confusion matrix displayed with matplotlib, use the predict_sentiment_sarcasm helper in Python to pass a list of new comment strings, receive a pandas DataFrame with predicted sentiment label, sarcasm label, confidence for sarcasm and per-class probabilities, optionally run the same flow inside a Jupyter or Colab notebook and add custom cells for additional plots or exports

- Usage examples: training and evaluation via python main.py, inference in a notebook cell calling predict_sentiment_sarcasm(["Ten filmik serio poprawił mi humor, obejrzałem już trzy razy.", "No jasne, bo nic tak nie rozwiązuje problemów jak wojna w komentarzach."]), manual inspection of the resulting DataFrame with predicted sentiment and sarcasm for each example

- Known limitations: performance and behavior tied to the specific training data from komentarze.xlsx and sarkazm.xlsx so domain shift may reduce quality, sarcasm detection remains imperfect on highly subtle or context-heavy irony, mixed-language or very slang-heavy comments may be classified less reliably, no full automated test-suite beyond evaluation metrics and manual examples


LICENSE

-  Software License: Apache License, Version 2.0
-  Preferred citation: Wojcik, K.(2026). Application of the multi-task HerBERT model
for sentiment and sarcasm classification in Polish-language social media content



CONTACT INFORMATION

Author/Principal Investigator Information
Name: Kacper Wójcik
ORCID: 0009-0009-5551-3640
Institution: University of Economics in Katowice
Address: Będzin, Poland
Email: wojcik.kacperr@gmail.com