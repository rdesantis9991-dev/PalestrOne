# Palestra 3.0 per iPhone

L'app è fatta da questi file, da tenere insieme nella stessa cartella:
`index.html`, `sw.js`, `manifest.json`, `icon-180.png`, `icon-192.png`, `icon-512.png`.

## Novità della versione 3.0
Pensate per l'app installata con Sideloadly (nella versione web l'app funziona come prima):
- **Avviso a fine recupero** anche con lo schermo bloccato o se stai usando un'altra app: arriva una notifica e il telefono vibra, anche in silenzioso. La prima volta che inizi un allenamento l'app chiede il permesso per le notifiche: rispondi **Consenti**.
- **Il timer di recupero ti dice cosa viene dopo** ("Squat · serie 2/3", "Poi: Lat machine") e **non si perde** se l'app viene chiusa.
- **Promemoria allenamento** (👤 → Notifiche): scegli giorni e ora, la notifica ti dice quale scheda tocca. Se quel giorno ti sei già allenato non arriva.
- **Schermo sempre acceso** con il sistema nativo dell'iPhone, più affidabile.
- **Backup automatico** nella cartella "Palestra": la trovi nell'app File (Sul mio iPhone → Palestra) e sul PC con iTunes (icona dell'iPhone → Condivisione file → Palestra). Un file sempre aggiornato più una copia per ognuna delle ultime 6 settimane. Se i dati dell'app sparissero, all'apertura l'app propone di ripristinarli da lì.
- **Esporta backup** apre il foglio di condivisione di iOS (Salva su File, AirDrop, Mail…).
- **Vibrazioni** quando spunti una serie, a fine recupero, quando salvi e quando fai un record.

## Aggiornare alla 3.0
1. Su GitHub, nel repository della palestra: **Add file → Upload files**, trascina **`index.html` e `sw.js`** di questa cartella e fai **Commit changes**.
2. Apri `.github/workflows/build-ios.yml`, clicca la **matita**, seleziona tutto il testo (**Ctrl + A**), incolla il contenuto del file `build-ios.yml` di questa cartella e fai **Commit changes**.
3. Quando in **Actions** compare la spunta verde, scarica il nuovo **Palestra.ipa** da **Releases** e installalo con Sideloadly. Se avevi già l'app, schede e allenamenti restano.

## Aggiornare dalla versione 1 alla 2
1. Nel repository `palestra` su GitHub ricarica **tutti i file**, sostituendo i vecchi. C'è anche una nuova icona.
2. Sull'iPhone apri l'app con internet attivo, chiudila e riaprila: compare la versione 2.0.

**Schede e allenamenti già salvati restano.** Per sicurezza, prima di aggiornare fai un backup dalla vecchia app (scheda Backup → Esporta).

## La prima cosa da fare
Tocca **👤 in alto a destra** e inserisci **peso, altezza, età e sesso**. Servono per stimare le calorie.
Lì puoi anche cambiare gli obiettivi giornalieri. Quelli predefiniti sono:
- 400 kcal attive;
- 30 minuti di esercizio;
- 4 allenamenti a settimana.

## Le sezioni
- **Oggi**
  - i tre anelli: Movimento (kcal attive), Esercizio (minuti) e allenamenti della settimana;
  - la prossima scheda da fare;
  - i pulsanti per far partire un'attività cardio;
  - il grafico della settimana e le ultime attività.
- **Schede**: crei e modifichi le schede. Mentre scrivi il nome di un esercizio l'app ti suggerisce quelli più comuni. Dal menu ••• puoi **duplicare** una scheda.
- **Storico**: un calendario del mese, con un pallino arancione per i pesi e uno verde per il cardio. Tocca un giorno per vedere cosa hai fatto, tocca un'attività per il dettaglio, dove puoi anche modificarla o eliminarla.
- **Progressi**
  - **Pesi**: grafico per esercizio (carico massimo, 1RM stimato, volume), record personali e serie per gruppo muscolare negli ultimi 7 giorni;
  - **Cardio**: kcal o minuti per settimana e statistiche di ogni attività (km, miglior ritmo, vittorie/pareggi/sconfitte);
  - **Corpo**: andamento del peso, indice di massa corporea e kcal che bruci a riposo.

## Cardio e sport
- In **Oggi** tocca un'attività (Corsa, Calcio, Tennis…) oppure **Altre** per vedere tutta la lista, circa 20 attività.
- Parte il **cronometro**. Puoi andare in pausa, riprendere, oppure ridurre la schermata con ⌄ e usare l'app normalmente.
- Quando tocchi **Termina** puoi:
  - controllare l'orario di inizio e di fine;
  - inserire i km (corsa, camminata, bici, nuoto, escursionismo) e vedere il ritmo;
  - scegliere l'intensità;
  - per gli sport, segnare l'esito e il risultato (es. "6-4 7-5").
- **Registra un'attività già fatta**: per esempio la partita di ieri sera. Scegli l'attività e scrivi data, inizio e fine.
- Il cronometro continua anche se chiudi l'app: si basa sull'orario di inizio.

## Come vengono stimate le kcal
**kcal = MET × metabolismo a riposo × ore**
- **MET**: indica quanto è impegnativa un'attività rispetto allo stare fermi. I valori vengono dal *Compendium of Physical Activities*.
- Per corsa, camminata e bici, se inserisci i km l'app calcola la velocità e usa il MET corrispondente.
- **Metabolismo a riposo**: viene calcolato con la formula di Mifflin-St Jeor, partendo dal tuo profilo.
- **kcal attive**: quelle in più rispetto a stare fermo. Sono le stesse "calorie attive" dell'app Fitness di Apple.
- Anche gli allenamenti con i pesi ora registrano inizio e fine, quindi hanno durata e kcal. L'intensità si imposta nel profilo.
- **È una stima**: l'errore tipico è intorno al ±20%.

## Durante l'allenamento con i pesi
- In alto vedi durata, kcal e serie fatte.
- Quando superi il tuo carico massimo su un esercizio compare **★ Record**.
- Con **Schermo sempre acceso**, attivo di default, l'iPhone non si blocca mentre ti alleni.
- Il bip a fine recupero si disattiva dal profilo. Non si sente con il silenzioso attivo.

## Da sapere
- I dati sono **solo sul telefono**. Ogni tanto fai **👤 → Esporta backup** e salvalo in File o iCloud Drive.
- **Indietro**: scorri dal bordo sinistro dello schermo.

## App vera per iPhone (con Sideloadly)
GitHub può trasformare l'app in un'app installabile (Palestra.ipa), che si affianca all'app Musica senza sostituirla.
1. **Una volta sola**: nel repository della palestra su GitHub clicca **Add file → Create new file**. Come nome scrivi `.github/workflows/build-ios.yml`, incolla tutto il contenuto del file `build-ios.yml` di questa cartella, poi **Commit changes**.
2. Dopo 5–10 minuti (scheda **Actions**, spunta verde) apri **Releases** nella colonna destra del repository e scarica **Palestra.ipa**.
3. Installala con **Sideloadly** come l'app Musica. Il rinnovo automatico ogni 7 giorni vale per entrambe.
- **Per portare i dati**: nella versione web fai **👤 → Esporta backup** e salvalo in File; poi nell'app nuova importalo dalla stessa sezione.
