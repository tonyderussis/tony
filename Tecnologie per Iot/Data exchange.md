dati eterogenei -> stessi input stessi output
- per far comunicare più dispositivi -> insieme di sistemi eterogenei nel web, data format -> sistemi che permettono di codificare e decodificare i dati
- data type astratti per l' hardware e il software, non deve avere nessun tipo di legame
- deve essere un sistema indipendente da ciò che c'è nell' hardware ed è fondamentale per avere dei meccanismi in modo da codificare e decodificare l'informazione (stiamo dando una lingua comune per comunicare)
- **Markup language** : famiglia di dataformat, ma non è adatto al mondo iot (si usano per la possibilità di integrare altri sistemi)
	- è un sistema che attraverso i tag mi fanno capire come adattare l'informazione 
	- la notazione descrive come presentare il documento 
	- il makup language sono una famiglia come ad esempio xml, html che sono figli di sgml (definisce delle regole generali)

- **Html** il file che scriviamo in html, poi viene fatto il render dal browser
	- nel mondo iot non va bene perché c'è spreco in quanto aggiungiamo al nostro sistema dei bit in più (tag) 
- **xml** -> è una lingua che abilita che abilità la descrizione di un linguaggio di tipo markup (nasce da sgml)
	- non è ottimizzato perché mi serve memoria, e mi serve un servizio di banda per scaricare i bit
	- sono human & machine readable 
	- un file xml deve includere dichiarazione, istruzioni da processare, commenti
	- dtd->descrizione della grammatica del linguaggio 
 - **json** -> linguaggio per alcuni aspetti simili a xml
	- il linguaggio ricorda un dizionario ma non lo è 
	- è un set di coppie chiave : valore, le chiavi devono essere delle stringhe tra " ". 
	- la chiave deve essere univoca 
	- esempio con la chiave temp per essere univoco devo fare una lista di tutte le temperature
	- nel caso in cui volessi mandare numeri esadecimali od ottale in json li scrivo come stringa
	- http://jsonlint.com/ -> idee per json 
	- definire i documenti: standardizzare l'organizzazione del documente stesso.
	- SenML: sensor markup language -> nasce come xml, però poi si è standardizzato anche per json 
	- funziona come un json, inizio a definire delle parole chiave ma riduco tutto al minimo. 
	- bn:  
	- e: vettore e mi dice quali sono le grandezze che sto inviando. 
	- t: timestamp è il numero di secondi dopo il gg/mm/1970
	- ci deve essere: chi manda l'informazione, cosa sto mandando, unità di misura, il valore e il tempo.
	- 