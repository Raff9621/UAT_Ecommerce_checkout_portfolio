# Business Requirements & Acceptance Criteria

## US-01: Autenticazione Utente
*Come* cliente registrato, *voglio* accedere con username e password *per* visualizzare il catalogo prodotti.
* *AC 1.1:* Dato un utente con credenziali valide, quando effettua il login, allora viene reindirizzato alla pagina /inventory.html.
* *AC 1.2:* Dato un utente bloccato (locked_out_user), quando tenta l'accesso, allora visualizza un messaggio di errore chiaro e non accede al catalogo.

## US-02: Gestione Carrello
*Come* acquirente, *voglio* aggiungere e rimuovere articoli dal carrello *per* modificare il mio ordine prima dell'acquisto.
* *AC 2.1:* Quando aggiungo 2 prodotti, il badge sull'icona del carrello mostra il numero 2.
* *AC 2.2:* Quando rimuovo 1 prodotto, il badge si aggiorna dinamicamente a 1.

## US-03: Checkout e Calcolo Totale
*Come* acquirente, *voglio* inserire i dati di spedizione e vedere il riepilogo con subtotale, tasse (8%) e totale finale *per* verificare l'importo prima di confermare.
* *AC 3.1:* Il totale finale deve corrispondere esattamente alla somma dei prezzi dei singoli articoli più l'8% di tasse.
* *AC 3.2:* Se lascio vuoto un campo obbligatorio (Nome, Cognome o CAP), il sistema blocca l'avanzamento e mostra un avviso.
