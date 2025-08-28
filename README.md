# FantaAstaAI

Prompt per gestire (con AI) un'**asta di Fantacalcio Serie A 2025/2026** realistica, competitiva e *budget-safe*, usando un prompt ottimizzato e il **listone ufficiale**.

## ✨ Descrizione
Questo repo contiene:
- `prompt.md` → prompt migliorato per ChatGPT per condurre l'asta in modo credibile e fluido.

## 📦 Come usarlo con ChatGPT
1. Apri `docs/prompt.md` e copia tutto.
2. Scarica qui il listone ufficiale con tutti i giocatori della Serie A: https://www.fantacalcio.it/quotazioni-fantacalcio
3. Carica su ChatGPT **il file Excel**.
4. Incolla il prompt e inizia l'asta: il bot chiamerà **un giocatore per volta**, partendo dai portieri.
5. Durante l'asta puoi scrivere `recap` per avere il riepilogo aggiornato.

## 💸 Regole di Budget (rinforzate nel prompt)
- Ogni squadra parte con **500 crediti**.
- **Non si può mai offrire più dei crediti residui**.
- **Offerta massima consentita** = `crediti_residui - (slot_rimanenti - 1)`
  - (devi tenerti almeno 1 credito per ogni altro slot da riempire).
- Se l'offerta richiesta supera il massimo consentito, il bot **rifiuta il rilancio** e lo segnala.
- **25 giocatori totali** per rosa, con limiti per ruolo: 3P, 8D, 8C, 6A.

## 📑 Note
- I giocatori **devono** esistere nel listone Excel; niente nomi fuori lista.
- Ruoli battuti in ordine: **P → D → C → A**.
- Alcuni giocatori top non vanno via sottocosto: logiche di prezzo min. realistiche sono incluse.


