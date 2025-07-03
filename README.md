# Simulatore Little Man Computer (LMC) e Assembler

Questo progetto implementa un simulatore per il **Little Man Computer (LMC)** insieme a un **Assembler** che converte il codice Assembly in memoria eseguibile dal simulatore. L'MC è un modello didattico di un computer per comprendere i principi base di architettura e esecuzione di istruzioni.

## Descrizione

- **Assembler**: Traduci il codice Assembly in memoria eseguibile per LMC.
- **LMC**: Simula un computer con un set limitato di istruzioni per eseguire programmi di esempio scritti in Assembly.

Il progetto include:
1. Un **Assembler** che converte le istruzioni Assembly in formato eseguibile.
2. Un **simulatore LMC** che esegue le istruzioni in memoria, simula l'esecuzione di un programma e visualizza l'output.

## Istruzioni

### Requisiti
- Python 3.x

### Installazione

1. **Clona il repository**:
    ```bash
    git clone https://github.com/tuo-username/lmc-simulator.git
    cd lmc-simulator
    ```

2. **Esegui il programma**:
    Puoi eseguire il programma direttamente con Python:

    ```bash
    python main.py
    ```

    Assicurati che il file `multiplication.lmc` (o qualsiasi altro file di codice Assembly) sia presente nella stessa cartella del progetto o aggiorna il percorso nel codice.

### Struttura del Progetto

Il progetto contiene i seguenti file principali:

- **assembler.py**: Contiene la classe `Assembler`, che traduce il codice Assembly in memoria eseguibile.
- **lmc.py**: Contiene la classe `LMC`, che simula l'esecuzione del programma.
- **main.py**: Il file principale che esegue il programma LMC, eseguendo i passaggi di assemblaggio e simulazione.
- **multiplication.lmc** (esempio): Un file di esempio scritto in Assembly per LMC (assicurati che sia presente per eseguire il programma).

### Come funziona

1. **Assembler**:
   - Carica e parse le etichette (labels) nel codice Assembly.
   - Traduci le istruzioni in memoria eseguibile.
   - La memoria è una lista di 100 celle dove ogni cella può contenere un valore che rappresenta un'istruzione o un dato.

2. **LMC**:
   - Simula un computer con un accumulatore, un contatore di programma (PC) e le code di input e output.
   - Le istruzioni che il programma può eseguire includono ADD, SUB, LDA, STA, BRA, BRZ, BRP, INP, OUT e HLT.
   - Le istruzioni vengono eseguite ciclicamente finché non si incontra un'istruzione **HLT** (ferma l'esecuzione).

### Esecuzione di un programma

1. Scrivi un programma Assembly per LMC e salvalo con estensione `.lmc` (ad esempio `multiplication.lmc`).
2. Esegui il programma tramite il file `main.py`.
3. Durante l'esecuzione, l'MC simulerà l'elaborazione e visualizzerà l'output.

### Esempio di programma Assembly

```assembly
INP
STA 99
INP
LDA 99
MUL 99
OUT
HLT
