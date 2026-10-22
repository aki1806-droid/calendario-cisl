# Sito del Calendario dei diritti 2027 · CISL FP

Pagine pensate per il telefono, raggiunte dai QR code dell'ultima pagina del calendario:
- `contatti/` → scelta del territorio, poi `contatti/padova-rovigo/` e `contatti/verona/` (sedi, telefoni, email, team con filtro per settore, "Salva nei contatti")
- `iscriviti/` → scelta del territorio, poi la pagina di iscrizione del sito territoriale
- `contratti/` → Sanità, Funzioni Locali, Funzioni Centrali: a chi si applicano, novità, pulsante per scaricare il testo
- `index.html` → pagina di ingresso

Per aggiungere un altro territorio: copia la cartella `contatti/verona/`, modifica i dati e aggiungi una scheda nelle pagine `contatti/index.html` e `iscriviti/index.html`.

## Pubblicare su GitHub Pages
1. Crea un nuovo repository pubblico, chiamato esattamente `calendario-cisl` (tutto minuscolo: è l indirizzo contenuto nei QR del calendario).
2. Carica tutto il contenuto di questa cartella (index.html, contatti/, contratti/, assets/).
3. Vai su Settings → Pages → Build and deployment → Source: "Deploy from a branch" → branch `main`, cartella `/ (root)` → Save.
4. Dopo un minuto il sito è online su `https://aki1806-droid.github.io/calendario-cisl/`.
   - Contatti: `https://aki1806-droid.github.io/calendario-cisl/contatti/`
   - Contratti: `https://aki1806-droid.github.io/calendario-cisl/contratti/`

## Collegare i contratti su Google Drive
Apri `contratti/index.html` e in alto, nel blocco CONFIGURAZIONE, incolla i link dei tre PDF:
```
const DRIVE = { sanita: "https://drive.google.com/...", locali: "...", centrali: "...", cartella: "..." };
```
Su Drive imposta la condivisione dei file su "Chiunque abbia il link può visualizzare".
Finché un link è vuoto, il pulsante mostra "Disponibile a breve".

## Aggiornare i contatti
In `contatti/padova-rovigo/index.html` e `contatti/verona/index.html`, in fondo, ci sono gli elenchi SEGRETERIA e TEAM: basta modificare nome, ruolo, settori, telefono ed email.
