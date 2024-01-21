- - -

#### es1
leggere un file in grado di stampare i numeri pari e numeri dispari: 
- numeri pari -> fprintf(stdout, "%d", odd);
- numeri dispari -> fprintf(stdout, "%d", even);
- nuovo tipo di redirezione è il stderr


**Pipe**
la comunicazione tra due processi attraverso le pipe avviene tramite "|" 
ridirezione fa in modo di far eseguire più processi in terminali diversi. Così facendo possiamo avere:
- stdin -> 0 (terminale) 
- stdout -> 1 (terminale)
- stderr -> 2 (terminale) 
#### es2
**comandi utili in pipe**
- grep -> filtra 
- aprire le carte e contare con le pipe diventa -> *ls xxx | wc* 
- conta tutti i processi con il nome root -> *ps aux | grep "root" | wc*


**comando ps**
- *ps -U* ispeziona tutti gli id user e mi restituisce id del processo 
- *aux*-> visualizza in maniera dettagliata tutti i processi degli utenti. 

---
#### es3

- scrivere un programma in grado di sincronizzare sia padre che figlio attraverso i segnali 
- piccolo reminder sul tipo di segnale tipi di segnali di base kill -> crea un segnale, signal prepara il segnale
- ricordiamo inoltre che il segnale è un' interruzione di un evento a causa di un evento straordinario. Viene infatti definito come interrupt software.
*dal punto di vista di codice ho fatto le seguenti cose:*

- creazione del set di segnali con la system call signal(SIGUSR1, signalHandler)
- il mio signalHandler fa si di ricevere il segnale in maniera sincrona e ritornare
- per ogni fork che creo mando un segnale con la system call kill(pid, SIGUSR1). 
- faccio sleep per non far andare il programma in crash
- utilizzo pause per far si di sospendere il processo fino a quando non arriva un segnale
child = pause-> sleep -> kill 
father = sleep-> kill ->pause 

*prima di ogni kill faccio una dormita* 





