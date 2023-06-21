Il codice è strutturato nel seguente modo:
- un file .ipynb denominato "EEG_Preprocessing.ipynb" nel quale effettuiamo il preprocessing
- 3 file .ipynb in cui alleniamo i modelli secondo i 3 protocolli descritti nel paper, denominati: "EEG_SubjectDependent.ipynb", "EEG_SubjectIndependent.ipynb","EEG_SubjectBiased.ipynb".

Il file 'EEG_Preprocessing' si occupa di caricare i dati dal dataset SJTU Emotion EEG Dataset for Four Emotions (SEED-IV) e presenti nella cartella "eeg_raw_data" per quanto riguarda i segnali EEG e  "eye_feature_smooth" per i movimenti oculari. 

Questo file deve essere eseguito prima degli altri tre file e memorizza i segnali EEG in un file denominato "preprocessed_data.csv" e i segnali eeg combinati con i movimenti oculari denominato "combinated_data.csv" presenti nella cartella "biometria_progetto". 

Nel file "EEG_SubjectBiased.ipynb" c'è in più la creazione dello studio Optuna che calcola tutte le possibili combinazioni di iperparametri e salva il modello migliore in base a quelli calcolati in una cartella apposita chiamata " Modelli" in "materiale_SubjectBiased". Una volta ottenuta la miglior configurazione viene importato il modello e su di esso effettuiamo il lavoro. 
 
In questa cartella "materiale_SubjectBiased" inoltre sono memorizzate anche le metriche e le matrici di confusione più precisamente nel percorso. 

Infine per ogni protocollo implementato sono state salvate in appositi file (chiamati "requirements_SI.txt", "requirements_SD.txt", "requirements_SB.txt") i rispettivi requirements che tengono traccia delle librerie installate insieme alle loro versioni specifiche. 

References:
If you use SEED-VIG in your research, please cite our following paper:
Wei-Long Zheng, Wei Liu, Yifei Lu, Bao-Liang Lu, and Andrzej Cichocki, EmotionMeter: A Multimodal Framework for Recognizing Human Emotions. IEEE Transactions on Cybernetics, 2018.










