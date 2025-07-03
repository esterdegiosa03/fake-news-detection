### README.md


# Rendering 3D Scene in formato PPM

## Ester De Giosa SM3201572

## Descrizione
Questo progetto implementa un renderer 3D in C che carica una scena da un file, calcola l'intersezione tra raggi e sfere e poi genera un'immagine in formato PPM. La scena è composta da sfere e un viewport, e il programma calcola il colore dei pixel in base agli oggetti che intersecano i raggi proiettati dalla telecamera.

Il progetto include i seguenti file principali:
- **main.c**: Funzione principale che gestisce il flusso di esecuzione.
- **scene.c**: Gestisce il caricamento della scena, l'intersezione dei raggi con le sfere e il calcolo della direzione dei raggi.
- **ppm.c**: Gestisce la scrittura dell'immagine in formato PPM.
- **vec3.c**: Funzioni utili per la gestione dei vettori 3D.
- **scene.h, ppm.h, vec3.h**: Header files per le funzioni dichiarate nei rispettivi file `.c`.
- **Makefile**: Gestisce la compilazione del progetto


### **Strutture**
- **`Vec3`**:  
  Rappresenta un vettore tridimensionale o un punto nello spazio. Utilizzato per calcoli matematici relativi a direzioni e posizioni.

- **`Color`**:  
  Struttura utilizzata per rappresentare un colore in formato RGB.

- **`Sphere`**:  
  Struttura utilizzata per rappresentare una sfera nella scena. Contiene centro, raggio e colore.

- **`Scene`**:  
  Struttura utilizzata per contenere la descrizione completa della scena: viewport, colore di sfondo, il numero delle sfere, e l'elenco delle sfere.


---

## **Istruzioni**

## **Compilazione**
Per compilare il progetto, si esegue:

```bash
make
```

Questo comando genererà un eseguibile chiamato `raytracer`.

## **Esecuzione**  
Per eseguire il programma, si usa:
```bash
./raytracer <scene_file> <output_image> <width> <height>
```

### Parametri:
* **scene\_file**: Il percorso del file di scena (es. `scene.txt`).
* **output\_image**: Il nome del file di output in formato PPM (es. `output.ppm`).
* **width**: La larghezza dell'immagine (es. `800`).
* **height**: L'altezza dell'immagine (es. `600`).

### Esempio di utilizzo:
```bash
./raytracer scene.txt output.ppm 800 600
```
Questo comando carica la scena da `scene.txt`, renderizza l'immagine di dimensione `800x600` e la salva nel file `output.ppm`.

## Come Funziona

1. Il programma carica la scena da un file di configurazione.
2. Calcola i raggi per ciascun pixel dell'immagine in base alla posizione della telecamera e della scena.
3. Verifica se i raggi intersecano delle sfere. Se sì, assegna il colore della sfera al pixel.
4. Se non c'è intersezione, assegna il colore di sfondo al pixel.
5. Salva l'immagine risultante in formato PPM.

## **Visualizzazione**  
   Per visualizzare l'immagine, aprire la cartella in cui è stato generato il file PPM e aprirlo con un visualizzatore di immagini.

## **Pulizia**  
   Per rimuovere i file oggetto generati durante la compilazione, eseguire:
   ```bash
   make clean
```