Voglio che tu gestisca un’asta di fantacalcio realistica, competitiva e completamente automatica per la stagione 2025/2026 della Serie A.
Ti fornirò un file Excel ufficiale (listone), che contiene i giocatori ammessi con squadra e ruolo corretti.
Devi usare **esclusivamente** i giocatori presenti in quel file: nessun nome al di fuori del listone, nemmeno per esempio o simulazione.
L’asta deve procedere in modo autonomo, con chiamate e rilanci automatici tra le squadre fino all’assegnazione, senza mai chiedere conferma o intervento all’utente (tranne quando richiede un recap o comandi specifici).

---

## 🎯 Regole di base

* Giocatori chiamati **uno alla volta**, in ordine casuale, solo se presenti nel listone, con dati corretti.
* Base d’asta: **1 credito** indipendentemente dalla quotazione.
* Offerta minima: **1 credito**.

---

## 👥 Partecipanti

* 10 squadre: la mia (**Paris Saint Gennar**) + 9 inventate con nomi realistici e in stile fantacalcio italiano.
* Ogni squadra parte con **500 crediti**.

---

## ⚖️ Rose da completare

* 3 Portieri (P)
* 8 Difensori (D)
* 8 Centrocampisti (C)
* 6 Attaccanti (A)
  Totale: **25 giocatori**.
* Limiti di ruolo obbligatori.
* Squadra che completa un ruolo → esclusa dalle chiamate per quel ruolo.
* Nessuna squadra può avere più di 25 giocatori.

---

## 📊 Gestione dati

* Aggiorna in tempo reale:

  * Crediti residui
  * Slot rimanenti totali
  * Slot rimanenti per ruolo
* Tabella assegnazioni:
  \| Giocatore | SquadraSerieA | Ruolo | Prezzo | Fantasquadra |
* Mantieni elenco giocatori già chiamati per evitare doppioni.

---

## 💸 Regole budget

* Mai superare il budget residuo.
* **Offerta massima consentita**:
  `crediti_residui - (slot_rimanenti - 1)`
  (così resta sempre almeno 1 credito per ogni slot rimanente).
* Se un rilancio supera il massimo → annulla e segnala.
* Se supera il limite di ruolo → annulla e segnala.

---

## 🧠 Strategie squadre

* Personalità diverse (aggressiva, impulsiva, calcolatrice, strategica).
* Distribuzione budget tipica:

  * Attacco \~35%
  * Centrocampo \~30%
  * Difesa \~25%
  * Portieri \~10%
* Nell’asta ufficiale: niente comportamenti irrealistici (no ruoli completati troppo presto senza motivo).

---

## 💬 Dialoghi e rilanci

* Botta e risposta sintetici, tono realistico e ironico da fantallenatori.
* **Rilanci automatici** fino all’assegnazione, senza mai chiedere all’utente se procedere.
* Top player (Sommer, Di Gregorio, Dimarco, Çalhanoğlu, Lautaro, ecc.) non sotto 30–50 crediti salvo mancanza di rilanci dopo 3 giri.
* Giocatori marginali possono restare invenduti anche a 1.

---

## 🔁 Logica asta

* Procedi **automaticamente**:

  * Chiamata → rilanci automatici → assegnazione → prossimo giocatore.
  * Nessuna domanda all’utente se continuare o rilanciare.
* Rispetta l’ordine ruoli: P → D → C → A.
* Recap solo su richiesta (`recap`).
* Testo breve, ritmo rapido.

---

## 🚦 Controlli prima di accettare un’offerta

1. Offerta ≤ budget residuo
2. Offerta ≤ `crediti_residui - (slot_rimanenti - 1)`
3. Non supera limiti di ruolo
4. Giocatore presente nel listone e non già assegnato

---

## 📁 Avvio asta

1. Dopo il caricamento del file Excel, conferma.
2. Estrai giocatori del primo ruolo, chiama un nome casuale valido.
3. Base 1 credito → rilanci automatici → assegnazione → prossimo nome.

---

## 📌 Comandi utente

* **recap** → riepilogo aggiornato
* **stop** → sospendi
* **riparti** → continua dall’ultimo punto

---

## 📦 Chiusura

* Quando tutte le squadre hanno 25 giocatori → tabella finale con tutti gli acquisti + riassunto strategie.

---
 
