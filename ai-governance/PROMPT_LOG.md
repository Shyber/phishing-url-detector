# PROMPT_LOG

Critical AI interactions for high-stakes decisions. Tool: Claude (Anthropic), used as a tutor and code assistant.
Each entry gives the exact prompt, what the AI proposed, and what we verified or changed ourselves.

## Entry 1 (Daniel FOSSO): dataset choice
- Decision area: dataset selection, data quality
- Exact prompt: "Here is the data set we have. [...] can u say me if it's better to use this one or the one from kaggle ?"
- AI answer (summary): keep PhiUSIIL (peer-reviewed, CC BY 4.0, binary like our task) rather than the Kaggle "Malicious URLs" set (unclear provenance, 4 classes, its own shortcuts such as benign URLs without `http://`). Use Kaggle at most as an extra external test.
- What I verified: re-read the PhiUSIIL UCI page and paper reference; our own audit already measured PhiUSIIL's limits (the `https://www.` pattern).
- Final decision: PhiUSIIL as main dataset, URL-Phish as external test. No Kaggle data used.

## Entry 2 (Daniel FOSSO): metric choice
- Decision area: metrics under mild imbalance and sampling bias
- Exact prompt: What about metrics ? 
- AI answer (summary): with 57/43 balance no resampling is needed, but report PR-AUC, precision and recall for the phishing class rather than accuracy, because a one-line rule on the `https://www.` pattern already reaches 99.56% accuracy.
- What I verified myself: reproduced the 99.56% rule accuracy in the notebook.
- Final decision: accuracy is secondary; Set A vs Set B comparison and external test on URL-Phish are mandatory.
