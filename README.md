# Il mio ricettario

Sito statico pubblicato con GitHub Pages. Le ricette si scrivono con Pages CMS, un editor a moduli che salva i file nel repository: non serve scrivere codice.

## Messa online (una volta sola, circa 15 minuti)

1. **Crea il repository.** Su github.com: *New repository*, nome `ricettario`, visibilità *Public*, poi *Create repository*.
   Se scegli un altro nome, cambia la riga `baseurl` in `_config.yml` usando lo stesso nome.
2. **Carica i file.** Nel repository appena creato: *uploading an existing file*. Trascina **tutto il contenuto** della cartella `ricettario` (cartelle comprese, anche il file `.pages.yml`), poi *Commit changes*.
3. **Accendi il sito.** *Settings → Pages → Build and deployment*: Source *Deploy from a branch*, branch `main`, cartella `/ (root)`, *Save*.
   Dopo 1-2 minuti il sito è su `https://TUONOMEUTENTE.github.io/ricettario/`.
4. **Collega l'editor.** Vai su app.pagescms.org, *Sign in with GitHub*, installa la GitHub App autorizzandola **solo** sul repository `ricettario`, poi apri il repository.
5. **Imposta il sito.** In Pages CMS apri *Impostazioni del sito*: titolo, sottotitolo e link PayPal.me. Finché il link resta vuoto, il pulsante del caffè non compare.

## Scrivere una ricetta (sempre così, anche da telefono)

1. Apri app.pagescms.org, entra nel repository, sezione **Ricette** → *Add an entry*.
2. Compila i campi: nome, categoria, foto (la trascini o la scegli dal telefono), porzioni e tempo in minuti (solo numeri), ingredienti (uno per riga, con il pulsante *+* per aggiungerne), procedimento (un passaggio per riquadro), note.
3. *Save*. Il sito si aggiorna da solo in 1-2 minuti.

Per correggere una ricetta la riapri e salvi. Per cancellarla usi il menu della ricetta.
La ricetta "Esempio - Pasta al pomodoro" serve solo a vedere l'impaginazione: cancellala dopo aver pubblicato la prima ricetta vera.

## Struttura dei file

| Percorso | Contenuto |
|---|---|
| `_ricette/` | una ricetta per file (le crea Pages CMS) |
| `foto/` | le foto delle ricette (le carica Pages CMS) |
| `_data/sito.yml` | titolo, sottotitolo, tuo nome, link PayPal |
| `.pages.yml` | i moduli dell'editor |
| `_layouts/`, `index.html`, `assets/stile.css` | grafica e struttura del sito |
| `_config.yml` | configurazione tecnica |

## Farsi trovare su Google (una volta sola)

Il sito genera da solo la mappa delle pagine (`sitemap.xml`) e, in ogni ricetta, i dati strutturati "Recipe" che Google usa per i risultati con foto e tempi.

1. Vai su Google Search Console, aggiungi la proprietà di tipo *Prefisso URL* con l'indirizzo del sito.
2. Per la verifica scegli *File HTML*: scarica il file e caricalo nella cartella principale del repository (*Add file → Upload files*).
3. Nel menu *Sitemap* inserisci `sitemap.xml` e invia.
4. Per controllare che i dati di una ricetta siano letti bene, incolla il suo indirizzo nel Test dei risultati avanzati di Google.

Per comparire con la foto nei risultati, la ricetta deve avere la foto: per Google è un dato obbligatorio.

## Due accortezze

- **Foto**: carica solo foto tue o con licenza che ne permetta l'uso. Le ricette in sé sono difficilmente tutelabili, le foto e i testi altrui sì.
- **Peso delle foto**: GitHub Pages accetta siti fino a 1 GB. Le foto dello smartphone sono spesso di 3-5 MB l'una: ridurle a circa 1600 px di lato le rende anche più veloci da caricare.
