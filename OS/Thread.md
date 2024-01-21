- - - 

thread molto più veloci dei processi inoltre si risparmia memoria grazie alla non presenza della gerarchia padre figlio, come abbiamo visto nei processi
*livelli di kernel*

**kernel livello kernel**
- kernel manipola tanti processi quanti sono i thread -> devono essere utilizzati attraverso la system call. 
- dato che il kernel si occupa della gestione dei thread e dei processi, lo fa attraverso una tabella di thread e di processi. 
- gestione può essere lenta ed abbiamo un numero massimo di thread. 
**User-level thread**
il pacchetto che gestisce il thread viene messo nello spazio utente così da alleggerire il kernel. 
i vantaggi posso implementare i thread in tutti i kernel anche se non lo sopportano. 
non richiedono modifiche dal sistema operativo. 
il sistema non sa che esistono i thread quindi potrebbe bloccare dei thread perché non ha priorità. 
**implementazione ibrida**
c'è un connubio tra livello user e livello kernel, quindi può essere utilizzato come pacchetto da inviare al kernel. 

*Coesistenza tra processi e thread*
esistono i segnali -> esempio se un processo riceve un segnale quale thread lo riceve
quale è la relazione tra i thread e processi con i segnali. 
il comportamento di un processo alla ricezione di un segnale specifico è condiviso tra tutti i thread 
quando utilizzo la fork -> duplica solo thread che richiamano la fork
nel processo originario stanno facendo dei processi critici, il processo duplicato può essere in uno stato non corretto. 
la exec -> thread sostituisce il nuovo programma un processo, tutti gli altri thread spariscono nonostante stavano eseguendo alcuni processi. 

#### libreria Pthread

abbiamo problema di tempistiche nell'esempio di threadcr.c in quanto potrebbe che ogni assegnazione di i non sia corretta, per risolvere questo problema facciamo un altro vettore dove salviamo i vari i e li passiamo alla funzione puntatore a void il puntatore del singolo elemento del vettore di indici. 
