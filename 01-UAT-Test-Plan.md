# UAT Test Plan – Rilascio v2.4 (Carrello e Checkout)

* *Progetto:* Swag Labs E-Commerce – Flusso Checkout
* *Ambiente di Test:* Web Staging (https://www.saucedemo.com/)
* *Browser testati:* Chrome (Desktop), Safari (Mobile)
* *Obiettivo:* Verificare che l'utente finale possa autenticarsi, gestire il carrello e completare un ordine senza errori di calcolo o blocchi funzionali prima del go-live.

## Scope del Test
* *In Scope:* Login utente, ordinamento catalogo, aggiunta/rimozione articoli dal carrello, compilazione dati spedizione, calcolo tasse (8%) e conferma ordine.
* *Out of Scope:* Recupero password, pagamenti con carte reali, gestione magazzino backend.

## Criteri di Ingresso e Uscita
* *Entry Criteria:* Ambiente di staging online; credenziali di test attive (standard_user, problem_user).
* *Exit Criteria:* 100% dei test critici (P1) eseguiti; zero difetti bloccanti (Severity: Critical) aperti; approvazione finale tramite UAT Sign-Off Report.
