- - -

**processi sequenziale e concorrenti**

sequenziale:  processo uno alla volta 
concorrenti:  più processi alla volta

ps -> per visualizzare i processi 

il processo può essere manipolato attraverso le system call esempio pid, getpid, fork... 
pid -> process identifier 
è un numero intero non negativo 

getpid -> identifica il processo chiamante 
il pid del processo è univoco -> posso utilizzare il pid per fare una determinato processo 
per gestire e distinguere
alcuni tipi di pid sono riservati :
- pid 0 -> scheduler gestisce i multitasking 
- pid 1 -> processo di init, eseguito alla fine del bootstrap, viene eseguito a livello utente, e diventa genitore di tutti i processi orfani 

**identificatore di un processo**

getppid -> da il pid padre 
getupid -> da il pid dell'user 
wait(unsigned int )
sleep (unsigned int )
**come creare un processo**

si può creare un processo tramite la system call fork
fork -> ritorna due volte: una volta per il padre e una per il figlio 

processo zombie -> si aspetta che i processi genitori riconoscano gli altri processi, se l'attesa non viene effettuata lascia il figlio e rilascia una  pcb (rimane pendente nell'eventuale attesa che il genitore lo raccolga) e deve fare una wait.
Non è un comportamento deterministico perché il processo fa la fork il padre 5 figlio 2, e il figlio viene processato in esecuzione core più lento ma continua ad aspettare il wait. 
dipende come il sistema operativo assegni i vari processi. 

processo orfano-> figlio rimane senza il padre e viene rimane init -> avviene quando il figlio aspetta il padre ma nel mentre termina, pid stampato del figlio è 1. 

cfg -> control fork graph 

**risorse**
pcb -> process controll block
condividono il codice sorgente, tutti i descrittori del file 

come si termina un processo -> return, exit 
**system call wait e waitpid**
il processo padre che attende la terminazione di un processo di uno dei figli:
- sincrono 
- asincrono 
wait -> join di padre e figlio che genera un figlio 
waitpid -> aspetta un figlio specifico 

terminazione del processo figlio avviene tramite una system call wait:
in cui il kernel invia un segnale sigchld al padre che si occuperà in maniera sincrona oppure asincrona la terminazione del figlio. 

i processi orfani per non rimanere tali vengono ereditati da init (1) oppure da un custom utente
nel caso quest'ultimi vengano ereditati dal processo init() non diventeranno mai zombie. 

#### aspetti teorici su processi 
![[Pasted image 20231110120018.png]]

i processi sono evidenziati da stati: 
- ready 
- running 
- waiting 
- new 
- terminated 

**evoluzione temporale di un processo**
![[Pasted image 20231110120850.png]]

**rappresentazione diagramma a stati**
![[Pasted image 20231110121014.png]]

