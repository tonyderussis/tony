
- paradigma **request response** è un paradigma di comunicazione, il client fa una domanda al server e il server non risponde, è una comunicazione sincrona, questo è un oaradigma sincrono perchè c'è sincronia tra fare una domanda e ricevere una risposta. 
- abbiamo un host (id: indirizzo ip), porta (numero esadecimale)
-  il protocollo http
- oggi è sbagliato mandare utente e password, nella parte di autority
- autority devono viaggiare in chiaro, per riuscire ad indirizzare
- IL SERVER WEB: contiene l'informazione e deve essere pronto a fornire l'informazione
- Il client consuma il servizio: vuol dire chiedere un' informazione e serve a fare un' analisi 
- URI/URL -> identificativo univoco il documento deve avere l'identificativo 
- http è il protocollo più diffuso,  è una delle tecnologie fondamentali in termini di robustezza
- machine to machine 
- protocollo mqtt con un paradigma publish subscribe 
- http rispecchia request response 
- metodi che mi permettono di far comunicare due entità nello stesso livello 
- metodi principali dell' http: 
	- get 
	- post 
	- put
	- delete 
- ogni protocollo ha un header, http body (informazione reale)
- get /doc/ test.html http/1.1
   host: www.test101.com parte che manca dell' uri 

- put vuo dire aggiorna una risorsa già esistente nel server -> ha un comportamento molto simile al post (eventualmente crea)
- post -> crea documento se devo aggiornare -> put 
- con la put deve inviare il documento da aggiornare nel body 
- il server in questo caso ha la possibilità di aggiornare il body nella response 
- delete cancella un documento, meglio una risorsa nel server
differenza tra client(browswer) - webserver e client(device) - webserver ?
uno fa comunicazione con il web l'altro con la macchina 
![[Pasted image 20230420151320.png]]

- se dovessi aggiornare la configurazione -> put 
- il server web va su un dispositivo iot quindi deve **deve essere leggero** 
**proprietà dell' http**

- **addresability**
	ogni risorsa deve avere un identificativo esempio www.example (indirizzo ip)
- **cacheability**
	utilizza un altro server in modo da fare accesso rapido proxy server e nel caso in cui non ci sia la richiesta nella cache, viene copiata. 
	last modified : mi permette di verificare quando è stato modificato
	cache cambiare con proxy
- **statelessness** 
	risorse computazionali per tenere traccia di tutte le macchine a stati. 
	"io sono smemorato"

---
rest -> serve per realizzare servizi web attraverso dei vincoli 
