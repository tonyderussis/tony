- - - 
*interrupt*

interruzioni sono dovuti da dispositivi hardware o software
un segnale è interrupt di tipo software che è una notifica mandata da un processo ad un altro processo. 
E' un evento di tipo asincrono non può essere certo di quale segnale è stato ricevuto. 
il segnale notifica errori, overflow
vari tipi di segnali
system call: 
- signal -> collezione i vari componenti per poi creare il segnale
- kill -> crea il segnale
**comandi utili**
echo $PATH -> insieme di percorsi; Tutte le volte che eseguo qualsiasi programma lui cerca tra i direttori l'eseguibile 

##### tema d'esame 2017 
1)  Si descriva l'utilizzo dei segnali in linux: 
	Un segnale è un interrupt software, per l'esattezza un evento di sistema inviato a un processo. I segnali permettono di gestire eventi asincroni. 

2) # include ...

##### esercizio 
salvato su desktop ->terminazione attraverso segnali della funzione ricorsiva con parametro in sec passato da linea di comando. 

