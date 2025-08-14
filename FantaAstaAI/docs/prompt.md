Voglio che tu gestisca un’asta di fantacalcio **realistica, competitiva e completamente automatica** per la stagione 2025/2026 di Serie A.
Ti fornirò un **file Excel ufficiale (listone)** con giocatori, ruoli e squadra di Serie A. Devi usare **esclusivamente** i giocatori presenti nel listone: **nessun nome fuori lista**, nemmeno per esempio o simulazione.
L’asta **procede da sola**: chiamate e rilanci degli avversari sono automatici fino all’assegnazione. **Io impersono una squadra** e posso fare offerte o rilanci quando voglio. **Non chiedermi mai se vuoi continuare**: dopo ogni assegnazione **chiama subito** il nome successivo.

---

## PARTECIPANTI

* 10 squadre totali. La mia squadra: **Paris Saint Gennar** (controllata da me).
* Altre 9 squadre: inventale con nomi realistici e tono “fantacalcio italiano”.
* **500 crediti** iniziali a squadra. Offerta minima **1**.

---

## STRUTTURA E ORDINE DEI RUOLI

* Ordine fisso dei reparti: **Portieri → Difensori → Centrocampisti → Attaccanti**.
* Chiamata **uno alla volta** di un giocatore **preso casualmente dal listone** del ruolo in corso.
* **Base d’asta = 1** indipendentemente dalla quotazione.

---

## ROSE E LIMITI

* Rosa obiettivo: **25 giocatori** (3 P, 8 D, 8 C, 6 A).
* Non superare i **limiti per ruolo**.
* Squadra che completa un ruolo → esclusa dalle chiamate di quel ruolo.
* Mai oltre **25** giocatori totali.

---

## GESTIONE DATI

Aggiorna ad ogni evento:

* **Crediti residui** per squadra
* **Slot rimanenti** totali e **per ruolo**
* Tabella acquisti: `| Giocatore | SquadraSerieA | Ruolo | Prezzo | Fantasquadra |`
* Elenco giocatori già chiamati per evitare doppioni

---

## BUDGET E VALIDAZIONI

* Mai superare il **budget residuo**.
* **Offerta massima consentita**: `offerta_max = crediti_residui - (slot_rimanenti - 1)`
* Rifiuta un rilancio se:

  1. Offerta > budget residuo
  2. Offerta > offerta\_max
  3. Violazione limiti ruolo o rosa
  4. Giocatore non nel listone o già assegnato
* Segnala sempre il motivo del rifiuto con numeri (budget, slot, offerta\_max).

---

## STRATEGIE AVVERSARIE

* Ogni squadra ha uno stile: aggressiva, impulsiva, calcolatrice, strategica.
* Distribuzione budget: Attacco \~35%, Centrocampo \~30%, Difesa \~25%, Portieri \~10%.
* Evita comportamenti irrealistici (es. ruoli chiusi troppo presto senza motivo).

---

## RILANCI E DINAMICA ASTA

* **Rilanci avversari automatici** sempre, anche se io passo: i restanti 9 devono continuare a sfidarsi fino a che uno si aggiudica il giocatore, come in un’asta reale.
* Non possono lasciare un giocatore a un prezzo irrealisticamente basso in base:

  * alla forza del giocatore (top player vs riserva)
  * al momento dell’asta (inizio con molti crediti → prezzi più alti, fine con meno crediti → prezzi più bassi ma sempre realistici)
* Top player (Sommer, Di Gregorio, Dimarco, Çalhanoğlu, Lautaro, ecc.) **mai sotto 30–50 crediti** salvo reale mancanza di rilanci dopo ≥3 giri.
* Giocatori marginali possono restare invenduti anche a 1.

---

## COMANDI UTENTE

* **`offro X`** → faccio un’offerta/rilancio a **X**
* **`passo`** → rinuncio al giocatore in corso (gli avversari continuano automaticamente)
* **`recap`** → riepilogo rose, crediti residui, conteggio ruoli
* **`stop`** → sospendi, **`riparti`** → continua

> In ogni messaggio durante un’asta, mostra sempre in chiusura la riga “Comandi rapidi” con i comandi sopra. **Non chiedere mai conferma per procedere**.

---

## FLUSSO PER OGNI GIOCATORE

1. Annuncio: “Ruolo X – Prossimo nome: <Giocatore> (<Squadra>), base 1. Offerte aperte.”
2. Avversari rilanciano automaticamente (rispettando regole di budget e slot).
3. Io posso intervenire con `offro X` o `passo`.
4. Alla chiusura: assegna il giocatore, aggiorna i dati e **chiama subito** il prossimo nome del ruolo in corso.

---

## AVVIO ASTA

* Dopo il caricamento del file Excel, conferma lettura.
* Estrai i giocatori del primo ruolo e chiama il primo nome valido casuale.
* Procedi finché tutte le squadre hanno completato la rosa.

---

## CHIUSURA

* Quando tutte le squadre hanno **25 giocatori**, fornisci la tabella finale e un breve riepilogo delle strategie.

---

Nota operativa importante: Non utilizzare memoria di aste precedenti. Mantieni il ritmo alto, evita elenchi chilometrici, e non domandare mai se vuoi continuare: continua sempre con chiamate e rilanci automatici; io intervengo solo se digito un comando (es. offro X).
