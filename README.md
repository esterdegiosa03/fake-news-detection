# Simulatore Little Man Computer (LMC) e Assembler

## Ester De Giosa SM3201572

## Descrizione
Questo progetto implementa un simulatore per il Little Man Computer (LMC) insieme a un Assembler che converte il codice Assembly in memoria eseguibile dal simulatore.


Il progetto include i seguenti file principali:
- **assemble.py**: Contiene la classe `Assembler`, che traduce il codice Assembly in memoria eseguibile per LMC.
- **lmc.py**: Contiene la classe `LMC`, che simula l'esecuzione del programma. Esegue le istruzioni in memoria, simula l'esecuzione di un programma e visualizza l'output.
- **main.py**: Il file principale che esegue il programma LMC, eseguendo i passaggi di assemblaggio e simulazione.
- **filename.lmc** (esempio): file di esempio scritti in Assembly per LMC.


## Istruzioni

## **Configurazione dei parametri**:
   Prima di eseguire il programma, è necessario configurare alcuni parametri nel file `main.py`. Di seguito sono spiegati i principali parametri da modificare:

   - **`file_name`**: il percorso del file contenente il programma scritto in linguaggio Assembly. Ad esempio, `file_name = "squares.lmc"`.
   Modificare la stringa `squares.lmc` in main.py con il nome del file assembly da usare.
   - **`input_queue`**: un elenco di valori che il programma utilizza come input. Ad esempio, `[5, 10]`.
   Modificare la lista `lmc.input_queue` in main.py con la lista di valori da usare.
       

## **Esecuzione del programma**:  
   Una volta configurati i parametri, è possibile eseguire il programma  con il comando seguente:

   ```bash
   python main.py
```

## **Output**:
Al termine dell'esecuzione, l'output finale verrà visualizzato nel terminale.