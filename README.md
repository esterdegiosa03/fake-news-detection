## Fake News Detection con ML & NLP

Questo progetto esplora diverse tecniche di Machine Learning, NLP tradizionale e Deep Learning (incluso BERT) per la classificazione automatica di notizie come *fake* o *real* usando il dataset **WELFake\_Dataset.csv**.

---

### Requisiti principali

```bash
pip install pandas numpy matplotlib seaborn scikit-learn torch transformers wordcloud
```

---

### Dataset
Il dataset usato per questo progetto è disponibile su [Kaggle](https://www.kaggle.com/datasets/saurabhshahane/fake-news-classification).


---

### Panoramica

1. **Caricamento & Pulizia Dati**

   * Lettura CSV.
   * Selezione colonne (`title`, `text`, `label`).
   * Rimozione valori mancanti e duplicati.
   * Fusione `title` + `text` in `full_text`.
   * Pulizia testo (lowercase, rimozione spazi multipli).

2. **Trasformazione Testo**

   * TF-IDF Vectorization (uni-grammi e bi-grammi, max 5000 features).

3. **Split Train/Test**

   * 80% train / 20% test mantenendo distribuzione delle classi.

---

### Modelli implementati

| Modello                                     | Ottimizzazione               |
| ------------------------------------------- | ---------------------------- |
| Logistic Regression                         | GridSearchCV                 |
| Random Forest                               | RandomizedSearchCV           |
| SVM Lineare (LinearSVC)                     | GridSearchCV                 |
| Rete Neurale (MLPClassifier)                | Con scaling + early stopping |
| Ensemble (VotingClassifier con soft voting) | Sui migliori modelli         |
| BERT (transformers)                         | Fine-tuning (accennato)      |

---

### Valutazione

* Accuracy, Precision, Recall, F1-score
* Matrici di confusione
* ROC Curve multiple
* Importanza delle parole (feature importance da RF con wordcloud)

---

### Confronto modelli

Al termine vengono stampati e ordinati:

* Metriche complete per ogni modello (Accuracy, Precision, Recall, F1)
* Confronto visivo tramite grafici
* Performance ensemble vs modelli singoli

---

### Come eseguire

Assicurarsi che il file `WELFake_Dataset.csv` sia nella cartella `data/`.
Poi eseguire lo script Python:

```bash
python fake_news_classification.py
```

---

### Librerie principali

* `pandas`, `numpy` → gestione e analisi dati
* `matplotlib`, `seaborn`, `wordcloud` → grafici e visualizzazione
* `scikit-learn` → modelli ML tradizionali, tuning, metriche
* `torch`, `transformers` → modelli deep learning (BERT)
