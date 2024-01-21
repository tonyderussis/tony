kernel è il nucleo del sistema operativo

tipi di kernel 3 tipi: 
- kernel monolitico 
-  micro-kernel 
- kernel ibrido 



*kernel monolitico* 
kernel ha un unica funzione che comprende tutto, vantaggio molto veloce, le funzionalità sono a livello utente 
kernel ibridi 
hanno più funzionalità ed è un misto dei due precedenti


che cos'è una system call 
è una funzione all'interno del kernel, fornisce un servizio così come una funzione. 
le system call sono predefinite e il numero è pre-indicato
sono molto semplici e forniscono funzioni e numero identificativi.

il sistema operativo funziona in modo che nel momento di una system call permette di entrare in modalità protetta settando il bit = 0, resettando il bit a 1 ritorna in modalità user. 

- fork -> processo padre aspetta figlio poi lavorano in parallelo, bipartizione del flusso operativo del padre; il padre si dirama in padre e figlio. 

- exec -> processo padre e figlio si scambiano 

cp copiare direttori oppure file  
ls . . -> direttorio padre, mi riferisco al direttorio corrente " . ", di fatto corrisponde a ls ./.. mi sto riferendo all DIRECTORY corrente 
come copiare un file tar -> cp ./../../usr/bin/tar ./../../var/
![[Pasted image 20231006143416.png]]


programma concorrente o parallelo che fa si di eseguire programmi paralleli e le loro temporizzazioni possono essere rappresentati da un grafo di precedenza, se le operazioni sono atomiche non devo preoccuparmi delle temporizzazioni, alcune operazioni sembrano atomiche ma non lo sono esempio 
x++ -> processo che sposta nel registro il dato [processo non atomico]
le operazioni non atomiche implicano la sincronizzazione

***thread*** 
fanno si di essere nello stesso processo ed eseguire con una temporizzazione sincrona/ asincrona le varie operazioni 

***pipe***
processi diversi legati tra di loro attraverso un flusso di dati che può essere half/full duplex 

***deadlock***
insieme di entità che aspettano un evento, può essere causata solo da un' altra entità dell' insieme

**livelock**
di base le entità sono bloccate e non fanno nessuno processo. esempio di due persone nello stesso corridoio e cercano di passare ma non procedono. 
avviene il polling quando uno dei due cerca di verificare il processo dell'altro 

**starvation**
ad una entità viene continuamente rifiutato l'accesso ad una risorsa che serve per il suo processo. 
deadlock => starvation ma non il reciproco. 

hypervision -> gestire delle macchine guest e disporle all' host, come avere più sistemi operativi in una unica macchina .
tipi di hypervision : 
- tipo 1 o nativo -> direttamente incluso nell'hardware 
- tipo 2 -> incluso nel sistema operativo
