This readme file was generated on [2026-06-10] by Kacper Wójcik

GENERAL INFORMATION

Title of Dataset: sarkazm, komentarze

Author/Principal Investigator Information
Name: Kacper Wójcik
ORCID: 0009-0009-5551-3640
Institution: University of Economics in Katowice
Address: Będzin, Poland
Email: wojcik.kacperr@gmail.com


- Date of data collection: [2025-07-15] - [2026-04-22]
- Geographic location of data collection: Poland

SHARING/ACCESS INFORMATION

- Licenses/restrictions placed on the data: Apache License, Version 2.0
- Was data derived from another source?
	- If yes, list source(s): www.Facebook.com, www.Instagram.com, www.x.com
- Recommended citation for this dataset: Wojcik, K.(2026). Application of the multi-task HerBERT model
for sentiment and sarcasm classification in Polish-language social media content



DATA & FILE OVERVIEW

File List: sarkazm.xlsx, komentarze.xlsx

- Relationship between files, if important: sarkazm.xlsx contains comments on social media with visible sarcasm, komentarze.xlsx contains comments on social media with no sarcasm

METHODOLOGICAL INFORMATION

Description of methods used for collection/generation of data:
Includes copying public data posted by users on platforms www.Facebook.com, www.Instagram.com, www.x.com

Methods for processing the data:
Data was collected on social media platforms www.Facebook.com, www.Instagram.com, www.x.com

Instrument- or software-specific information needed to interpret the data:
Code written in python 3, includes libraries such as: os, pandas, numpy, torch, torch.nn, torch.nn.functiona, datasets, transformers, sklearn.model_selection, sklearn.preprocessing, sklearn.metrics, seaborn, matplotlib.pyplot, json, safetensors.torch, time.

- People involved with sample collection, processing, analysis and/or submission:
Data was sourced from widely accesible publications made by people on social media platforms.


DATA-SPECIFIC INFORMATION FOR: [komentarze.xlsx]

- Number of variables: 8 variables
- Number of cases/rows: 1577 rows
- Variable List: Treść: text content of a social media comment in Polish, Sentyment: sentiment label for the comment with values Pozytywny, Neutralny, Negatywny, Data_utworzenia: comment creation date in format yyyy-mm-dd, Platforma: social media platform where the comment appeared (e.g. Facebook, TikTok, X/Twitter, Instagram, LinkedIn), Użytkownik: user identifier or username associated with the comment (may be anonymized or synthetic), Hashtag: hashtag or set of hashtags linked to the comment (real or synthetic tags used for training), Kraj: country associated with the comment or its context, most commonly Polska, Sarkazm: binary sarcasm label where 0 means non-sarcastic and 1 means sarcastic,
- Specialized formats or other abbreviations used: date yyyy-mm-dd

DATA-SPECIFIC INFORMATION FOR: [sarkazm.xlsx]

- Number of variables: 8 variables
- Number of cases/rows: 709 rows
- Variable List: Treść: text content of a Polish social media comment curated primarily for sarcasm-related training, Sentyment: sentiment label for the comment with values Pozytywny, Neutralny, Negatywny, Data_utworzenia: comment creation date in format yyyy-mm-dd, Platforma: social media platform of origin or simulated origin (e.g. Facebook, TikTok, X/Twitter, Instagram, LinkedIn), Użytkownik: user identifier or synthetic username used for the comment, Hashtag: hashtag or synthetic training tag connected with the comment, Kraj: country information for the comment context, typically Polska, Sarkazm: binary sarcasm annotation where 0 denotes non-sarcastic content and 1 denotes sarcastic content
- Specialized formats or other abbreviations used: date yyyy-mm-dd

