# Riconoscimento delle Emozioni tramite Segnali EEG

## Descrizione del Progetto
Questo progetto si concentra sull'identificazione delle emozioni umane attraverso l'analisi dei segnali **EEG (Elettroencefalogramma)**. Utilizzando tecniche avanzate di **machine learning** e **pre-processing dei segnali**, l'obiettivo è migliorare la precisione nella classificazione delle emozioni. Il sistema sviluppato può avere applicazioni nel settore medico, nel miglioramento delle interfacce cervello-computer (BCI) e nella realizzazione di strumenti per la regolazione emotiva.

## Autori
- **De Martino Angela**
- **Spagna Zito Marika**

**Supervisori:**
- **Prof. Michele Nappi**
- **Dott.ssa Chiara Pero**

## Dataset Utilizzato
Il dataset impiegato per l'analisi è **[SEED-IV](https://bcmi.sjtu.edu.cn/~seed/seed-iv.html) (Stress and Emotion in Everyday Decision-making - Interactive Version)**. 
Il dataset include:
- Registrazioni EEG da **15 soggetti**.
- **62 canali EEG**.
- Movimenti oculari raccolti tramite occhiali di tracciamento.
- Stimoli video per indurre specifiche emozioni (felicità, tristezza, paura, neutralità).

## Struttura del Progetto
### 1. Pre-processing dei dati
- **Filtro Notch a 50Hz** per rimuovere interferenze.
- **Filtri passa-banda (1-35Hz)** per isolare le frequenze EEG rilevanti.
- **Trasformata di Wavelet** per il miglioramento del segnale.
- **PCA (Principal Component Analysis)** per la riduzione della dimensionalità.

### 2. Estrazione delle Caratteristiche
- Media, deviazione standard, entropia di Shannon, energia e altre metriche.
- Analisi della distribuzione delle caratteristiche estratte per identificare pattern ricorrenti.

### 3. Fusione con i Movimenti Oculari
- Unione delle caratteristiche EEG e movimenti oculari tramite **feature level fusion**.
- Analisi della correlazione tra movimenti oculari ed emozioni classificate.

### 4. Classificazione
- Algoritmi utilizzati:
  - XGBoost
  - SVM
  - Random Forest
  - Logistic Regression
  - Naive Bayes
  - AdaBoost
- Valutazione tramite **matrici di confusione**, **accuratezza** e altre metriche.

## Tecnologie Utilizzate
- **Linguaggi**: Python
- **Librerie principali**: Scikit-learn, Numpy, Pandas, Seaborn, Optuna
- **Ambiente di sviluppo**: Google Colab
- **Frameworks aggiuntivi**: TensorFlow/Keras per possibili miglioramenti futuri con reti neurali.

## Risultati Principali
I modelli sono stati valutati su tre protocolli differenti:
| Protocollo          | Accuratezza Massima |
|--------------------|-------------------|
| **Subject-Dependent** | 78% |
| **Subject-Independent** | 92% |
| **Subject-Biased** | 85% |

**XGBoost** si è rivelato il miglior modello con un'accuratezza media **superiore al 90%** nei protocolli più performanti.

## Possibili Sviluppi Futuri
- Esplorazione di **tecniche di deep learning** per l'analisi EEG.
- Test su **dataset aggiuntivi** per validazione e generalizzazione.
- Ottimizzazione delle tecniche di **fusione multimodale** per una classificazione più precisa.
- Implementazione di **reti neurali convoluzionali (CNN)** o **LSTM** per migliorare l'analisi temporale dei segnali EEG.
- **Applicazioni reali**: supporto nella diagnosi di disturbi neurologici e miglioramento delle interfacce BCI.

## Citazioni e Riferimenti
Per un elenco completo delle fonti utilizzate, fare riferimento alla bibliografia inclusa nel documento principale.

---
**Università degli Studi di Salerno - Dipartimento di Informatica**
