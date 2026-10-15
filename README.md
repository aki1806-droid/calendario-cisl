# Sito del Calendario dei diritti 2027 · CISL FP Padova Rovigo

Due pagine pensate per il telefono, raggiunte dai QR code dell'ultima pagina del calendario:
- `contatti/` → sedi, telefoni, email, segreteria e team (con filtro per settore e "Salva nei contatti")
- `contratti/` → Sanità, Funzioni Locali, Funzioni Centrali: a chi si applicano, novità, pulsante per scaricare il testo
- `index.html` → pagina di ingresso con i collegamenti

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
In `contatti/index.html`, in fondo, ci sono gli elenchi SEGRETERIA e TEAM: basta modificare nome, ruolo, settori, telefono ed email.
