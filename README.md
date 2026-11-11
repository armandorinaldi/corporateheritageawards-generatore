# Generatore badge, cavalieri e basette – Corporate Heritage Awards 2026

Pagina statica: un solo `index.html`, senza dipendenze esterne. Genera in PDF vettoriale i **badge** dei partecipanti, i **cavalieri** da tavolo e le **basette** dei premi, fedeli al design Figma. I font (Anton, Playfair Display, Spline Sans, licenza SIL OFL) sono incorporati.

## Pubblicazione su GitHub Pages
1. Crea un repository e carica i file di questa cartella.
2. **Settings → Pages → Build and deployment**: Source = *Deploy from a branch*, Branch = `main` / `(root)` → Save.
3. Dopo un minuto la pagina è online su `https://<utente>.github.io/<repository>/`.

Funziona anche aprendo `index.html` in locale con doppio clic, anche offline.

## Badge
- **Badge singolo**: scegli il ruolo (GUEST, SPEAKER, PRESS, STAFF), compila Nome, Cognome e Azienda, poi *Scarica questo badge*. Il file si chiama "Nome Cognome.pdf".
- **In serie**: importa un CSV o un file Excel con le colonne `Nome`, `Cognome`, `Azienda`, `Ruolo` (modello: `modello-badge-cha2026.csv`). Di default ottieni uno ZIP con un PDF per persona; gli omonimi diventano "Nome Cognome (2).pdf". In alternativa puoi scaricare un unico PDF con un badge per pagina.
- **Formato**: con crocini la pagina è di 348,66 × 470,55 pt, come l'export di Figma. Senza crocini è di 331 × 453 pt, con l'abbondanza inclusa.

## Cavalieri
- Scheda **Cavalieri** in alto. Si modifica un solo lato, mostrato in orizzontale e leggibile. In stampa il contenuto viene ripetuto capovolto sull'altro lato.
- Campi: Azienda, Titolo progetto, Categoria. Import da CSV/Excel con le stesse colonne (modello: `modello-cavalieri-cha2026.csv`).
- **Export**: un A4 verticale per cavaliere, impaginato come nel file Figma, con entrambi i lati, crocini di taglio per il formato 200 × 287 mm e abbondanza. I file si chiamano con il nome dell'azienda, in uno ZIP oppure in un unico PDF.

## Basette premi
- Scheda **Basette**. I tipi sono tre:
  - **Vincitore** e **Menzione**: 250 × 30 mm, su fondo oro, con la riga "Vincitore - Categoria" o "Menzione - Categoria".
  - **Nomination**: 200 × 30 mm, su fondo trasparente, con la sola categoria.
- Il PDF contiene **solo la grafica blu**: testi convertiti in tracciati e logo, su fondo trasparente e nel formato esatto della basetta. Il fondo oro o trasparente che vedi nell'anteprima serve solo come riferimento.
- Import da CSV/Excel con le colonne `Nome`, `Categoria`, `Tipo` (modello: `modello-basette-cha2026.csv`). I file si chiamano "Nome - Tipo.pdf".
- I nomi troppo lunghi si riducono per stare su una riga.

Testi lunghi: vanno a capo (massimo 2 righe) e si riducono in automatico.

## Modificare il design
I colori dei ruoli sono nell'oggetto `ROLES` in `index.html`; la geometria dei cavalieri è nelle costanti `CP` e `C_BANDS`.
