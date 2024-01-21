- - -
- Exec -> nuovo programma e permette al padre e al figlio di far eseguire programmi diversi. 
- Fork -> permette la clonazione di un processo, identico.

Una volta clonato il processo padre e figlio eseguono codici differenti perché è inutile avere stessi processi che eseguono lo stesso codice.
Padre e figlio eseguono codici differenti -> esempio shell diventa padre del comando stesso.
richiede l'utilizzo dell' exec -> ha molte versioni

*exec*
sostituisce il processo con un nuovo programma, il nuovo programma viene eseguito con un programma standard ma sostituisce il processo corrente con un processo che esegue un programma. 

![[Pasted image 20231113145544.png]]


dal punto di vista utente ha 6 versioni:
- exec(l/v) -> lista/vettore di argomenti
- exec(l/v)p -> lista/vettore di path
- exec(l/v)e -> lista/vettore di environment

valore di ritorno -> fa la copia della fork

pipe -> out generato dal comando sinistra viene manipolato da quello di destra esempio: 
ps -aux | grep 2471

esempio con execlp -> in questo caso utilizziamo le fork e nel caso in cui ci sia il figlio chiama ricorsivamente echo ma il padre continua. 

*system*
esempio stesso programma dell 'exec non abbiamo solo un end ma tanti end quanti sono le system



