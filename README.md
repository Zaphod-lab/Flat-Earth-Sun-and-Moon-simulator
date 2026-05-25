# Simulatore Sole e Luna Terra Piatta 🌍🌒

Una suite di tre applicazioni web interattive progettate a scopo didattico e scientifico. Il progetto permette di simulare, analizzare e verificare visivamente le geometrie dei corpi celesti in relazione al modello della Terra piatta (Proiezione di Gleason) e di confrontarle matematicamente con la realtà del modello sferico.

L'obiettivo è dimostrare i paradossi geometrici del modello planare attraverso l'uso di trigonometria sferica, raycasting 3D e calcoli empirici verificabili.

## 🚀 Le Applicazioni

Il progetto si compone di tre file HTML indipendenti e monolitici (senza dipendenze esterne):

### 1. Simulatore Sole: La Prospettiva (`index.html`)
Permette di osservare il ciclo giorno/notte e il movimento del Sole sopra la mappa di Gleason. Evidenzia il paradosso della **dimensione apparente**: in un modello piatto con un "Sole locale", per mantenere un diametro visivo costante all'orizzonte (come avviene nella realtà), il Sole dovrebbe violare le leggi della prospettiva variando drasticamente le sue dimensioni durante il giorno.

### 2. Simulatore Luna: La Parallasse (`indexluna.html`)
Un motore di rendering 3D (software raycasting) che si concentra sulla faccia visibile della Luna. Mostra in tempo reale come due osservatori in posizioni diverse del mondo (Osservatore A e B) vedrebbero una "Luna vicina". Dimostra visivamente che una Luna locale mostrerebbe porzioni e rotazioni di superficie completamente diverse a seconda dell'osservatore, smontando geometricamente questa ipotesi.

### 3. La Prova dell'Azimut: Il Fallimento Geometrico (`indexazimut.html`)
Il simulatore più tecnico. Calcola la vera posizione del Sole (Punto Sub-solare) basata su dati astronomici (Data e Ora UTC). Usa la **trigonometria sferica** per calcolare l'Azimut e l'Elevazione esatti che una bussola reale segnerebbe per due osservatori.
*   **Il Paradosso:** Tracciando questi angoli reali sulla mappa piatta, le linee di vista non convergono mai sul Sole.
*   **Il Confronto:** Mostra un rendering 3D affiancato del Globo terrestre, dove le stesse linee convergono invece perfettamente, provando che la realtà osservabile è compatibile solo con una superficie sferica.

## 🛠️ Tecnologie Utilizzate
- **HTML5 / CSS3**: Interfaccia utente moderna e responsiva.
- **Vanilla JavaScript**: Tutta la logica matematica, orbitale e astronomica è scritta in puro JS. Nessun framework o libreria esterna.
- **Canvas API**: Utilizzata massicciamente per i rendering grafici 2D (mappe di Gleason) e 3D pixel-per-pixel (Luna e Globo sferico).

## ⚙️ Come si usa
Il software è interamente *Client-Side*. Non serve alcun server, database o installazione.

1.  Clona o scarica il repository.
2.  Assicurati che i file immagine (`Terra piatta.jpeg`, `Luna.jpg`, `Terra_sferica.jpg`) siano nella stessa cartella dei file HTML.
3.  Apri `index.html`, `indexluna.html` o `indexazimut.html` con un qualsiasi browser moderno (Chrome, Firefox, Safari, Edge).
4.  Inserisci le tue coordinate, modifica l'ora o utilizza i **Preset** (es. Equinozio, Solstizio) per vedere la simulazione in azione.

## 🔍 Trasparenza e Verificabilità
Tutti i calcoli azimutali e le formule sferiche utilizzate (visibili in chiaro nell'interfaccia dell'app *Azimut*) producono dati esatti. Qualsiasi utente è invitato a confrontare i valori di Azimut ed Elevazione restituiti dal simulatore con quelli di siti professionali e terzi, come [SunCalc.org](https://www.suncalc.org/).

## 📝 Licenza
Progetto open-source a scopo didattico. Sentiti libero di biforcare (fork) il codice, modificarlo e utilizzarlo per scopi educativi o di debunking scientifico.