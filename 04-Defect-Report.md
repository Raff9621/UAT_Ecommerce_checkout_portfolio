# Defect Report #01: Mancato aggiornamento del badge carrello dopo l'aggiunta prodotti

* *ID Difetto:* BUG-01
* *Progetto:* Swag Labs E-Commerce v2.4
* *Modulo:* Catalogo / Carrello (/inventory.html)
* *Severità:* Major (Blocca una funzionalità chiave dell'utente)
* *Priorità:* Alta
* *Autore (Tester):* [Tuo Nome / Portfolio UAT]
* *Ambiente:* Chrome 120 (Desktop) – Staging (https://www.saucedemo.com/)

---

## 1. Descrizione del Problema
Quando l'utente clicca sul pulsante "Add to cart" per aggiungere uno o più articoli dalla pagina del catalogo, il sistema registra l'azione a livello di backend ma *l'icona del carrello in alto a destra non mostra il contatore numerico (badge)* in tempo reale, inducendo l'utente a pensare che l'operazione sia fallita.

## 2. Passi per Riprodurre il Bug (Steps to Reproduce)
1. Aprire il browser e accedere a https://www.saucedemo.com/.
2. Eseguire il login con credenziali valide (es. standard_user o problem_user).
3. Dalla pagina del catalogo (/inventory.html), cliccare sul pulsante *"Add to cart"* del prodotto "Sauce Labs Backpack".
4. *Osservare l'icona del carrello* nell'angolo in alto a destra.

## 3. Risultato Atteso vs. Risultato Effettivo
* *Risultato Atteso:* Il pulsante diventa "Remove" e sull'icona del carrello compare immediatamente il badge numerico rosso con il valore "1".
* *Risultato Effettivo:* Il pulsante cambia stato in "Remove", ma il badge numerico sul carrello *rimane vuoto o non si aggiorna*, costringendo l'utente ad entrare nella pagina del carrello per verificare se l'articolo è stato aggiunto.

## 4. Evidenze (Screenshot / Log)
(Qui in un contesto reale inseriresti uno screenshot o una breve registrazione video della schermata)
> [Inserire qui l'immagine o il link allo screenshot del carrello vuoto nonostante il prodotto aggiunto]

---
