# Simulatore Little Man Computer (LMC) e Assembler

## Descrizione
Questo progetto implementa un simulatore per il Little Man Computer (LMC) insieme a un Assembler che converte il codice Assembly in memoria eseguibile dal simulatore.


Il progetto include i seguenti file principali:
- **assembler**: Contiene la classe `Assembler`, che traduce il codice Assembly in memoria eseguibile per LMC.
- **LMC**: Contiene la classe `LMC`, che simula l'esecuzione del programma.Esegue le istruzioni in memoria, simula l'esecuzione di un programma e visualizza l'output.
- **main.py**: Il file principale che esegue il programma LMC, eseguendo i passaggi di assemblaggio e simulazione.
- **filename.lmc** (esempio): file di esempio scritti in Assembly per LMC.


## Istruzioni

**Configurazione dei parametri**:
   I parametri di ingresso devono essere inseriti direttamente nel file `main.py` per velocizzare l'esecuzione. In particolare, è necessario configurare le seguenti variabili:

   - **`nome`**: il percorso del file contenente il programma scritto in linguaggio Assembly. Ad esempio, `program.lmc`.
   - **`input_queue`**: una lista di valori che saranno utilizzati come input per il programma. Ad esempio, `[5, 10]`.

   Esempio di configurazione in `main.py`:

   ```python
   nome = "squares.lmc"         # Percorso del file Assembly
   input_queue = [5, 8]
   ```        # Lista dei valori di input

**Compilazione del programma**:  
   Una volta configurato il file `main.py`, si esegua il programma utilizzando il seguente comando:

   ```bash
   python main.py
```

**Output**:
Al termine dell'esecuzione, l'output finale verrà visualizzato nel terminale. Inoltre, sarà possibile vedere lo stato finale dell'LMC:
- La memoria dell'LMC.
- Il valore dell'accumulatore.
- Il valore del Program Counter (PC).
- La coda di input e output.
- Il flag.
