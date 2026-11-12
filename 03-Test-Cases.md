# Matrice dei Test Case UAT (Execution Log)

*Legenda Stato:* ✅ PASS | ❌ FAIL | ⏸️ BLOCKED

| ID | Requisito | Titolo Test Case | Precondizioni | Step di Esecuzione | Risultato Atteso | Esito | Note / Bug ID |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| *TC-01* | US-01 | Login con utente standard valido | Essere su saucedemo.com | 1. Inserire user standard_user<br>2. Inserire password secret_sauce<br>3. Cliccare Login | Accesso riuscito e redirect alla pagina catalogo (/inventory.html). | ✅ PASS | - |
| *TC-02* | US-01 | Blocco accesso per utente sospeso | Essere su saucedemo.com | 1. Inserire user locked_out_user<br>2. Inserire password secret_sauce<br>3. Cliccare Login | L'accesso viene negato e appare il messaggio "Sorry, this user has been locked out." | ✅ PASS | - |
| *TC-03* | US-02 | Aggiunta di 2 prodotti al carrello | Loggato come standard_user | 1. Cliccare Add to cart su "Sauce Labs Backpack"<br>2. Cliccare Add to cart su "Sauce Labs Bike Light" | Entrambi i pulsanti diventano Remove e il badge del carrello mostra 2. | ❌ FAIL | Vedi *BUG-01* |
| *TC-04* | US-02 | Rimozione di un prodotto dal carrello | Almeno 2 prodotti nel carrello | 1. Aprire l'icona del carrello<br>2. Cliccare Remove su uno dei due articoli | L'articolo sparisce dalla lista e il badge del carrello si aggiorna a 1. | ✅ PASS | Funziona dentro la pagina carrello |
| *TC-05* | US-03 | Validazione campi obbligatori nel Checkout | Almeno 1 prodotto nel carrello, pagina Checkout: Your Information | 1. Lasciare vuoti Nome, Cognome e CAP<br>2. Cliccare Continue | Il sistema blocca l'avanzamento e mostra l'errore "Error: First Name is required". | ✅ PASS | - |
| *TC-06* | US-03 | Calcolo corretto Subtotale, Tasse (8%) e Totale | Prodotto da $29.99 nel carrello, dati spedizione inseriti | 1. Arrivare alla pagina Checkout: Overview<br>2. Verificare gli importi mostrati | Item total: $29.99, Tax (8%): $2.40, Total: $32.39. | ✅ PASS | Calcolo esatto al centesimo |
| *TC-07* | US-03 | Completamento ordine End-to-End | Essere su Checkout: Overview con standard_user | 1. Cliccare sul pulsante Finish | Appare la pagina di conferma con il messaggio "Thank you for your order!". | ✅ PASS | - |
| *TC-08* | US-02/03 | Test esplorativo con utente problematico (problem_user) | Essere su saucedemo.com | 1. Accedere con problem_user / secret_sauce<br>2. Provare ad aggiungere articoli al carrello e completare il checkout | Il flusso funziona senza errori grafici o blocchi nei campi del form. | ❌ FAIL | Vedi *BUG-01* + immagini prodotto errate |
