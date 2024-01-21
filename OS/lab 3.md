- - -

**es. 1**
dopo la creazione dell' albero di processi spiegare cosa fa in fase di stampa 
- fuori dal ciclo for si crea una fork() quindi crea un processo, poi si creano altri processi all'interno del ciclo for. si creano 2^3 processi (discutibile). 
- albero di processi: p1 - p2 - p3- p4 
						    /\\
						p5	p6
- stampa del programma:
exec with i=0  
exec with i=0  
system with i=0  
system with i=0  
exec with i=1  
exec with i=1  
system with i=1  
system with i=1


**es2**

processi che si creano sono 6: 
- ogni processo figlio dopo aver eseguito la exec (crea un nuovo programma) termina: $i*i$
- il processo padre invece continua fino alla fine: $i+i$ 


