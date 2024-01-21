- - -
**Processi concorrenti**
- indipendenti -> sono processi atomici
- concorrenti -> sono processi al contrario che per essere eseguiti deve esserci scambio di dati
scambio tra informazione avviene attraverso IPC 

*modelli di comunicazione:*
- **memoria condivisa**
![[Pasted image 20240111014626.png]]
file sono mappati in memoria in modo che ogni processo associa una porzione di memoria.
- Ogni processo accede alla sua zona di memoria sullo stesso file. 
- Ricorda si condivide il puntatore al file prima di ogni fork o exec. 

- **scambio di messaggi**
La comunicazione attraverso i messaggi avviene attraverso l' instaurazione di un canale. 
Questo canale richiede la chiamata alla system call e di conseguenza c'è bisogno del kernel. Questo tipo di modello va bene se si vuole fare uno scambio leggero di dati perché è molto lento. 

![[Pasted image 20240111015400.png]]



**Canali di comunicazione**
diretta oppure indiretta (mail box)
sincronizzazione: limitata 
capacità: limitata 

vari tipi di comunicazione di processi, vedremo le pipe e i processi. 
semafori -> meccanismo di sincronizzazione. 
Le pipe -> sono la più comune tipo di comunicazione tra processi. 
Le pipe sono uno pseudo-file -> tubo di comunicazione che vivono in memoria. E' un tipo di comunicazione diretto ed ha capacità limitata 
Normalmente rappresentazione tra un processo p1 (produttore [scrive]) -> tube -> p2(consumatore [legge]). 
Descrittore che descrive il lettore e scrittore. 
pipe sono half duplex -> sono simplex per risolvere il problema di sincronizzazione. 
Gli pseudo file sono condivisi quando si fa una fork. 
il procedimento di comunicazione sarà fare una pipe poi una fork

**meccanismo**
System call: pipe riceve riceve un descrittore di dimensione 2:
descrittore 0 ->lettura
descrittore 1-> scrittura 

Come si mette in pratica?
operazione fondamentale è la pipe:
se facciamo una pipe nel processo stesso non serve a nulla. 
Fare la pipe e subito dopo fare la fork, in questo modo crea un secondo processo che condividono gli stessi descrittori:
- esempio: padre-> scrive & figlio-> legge ; il figlio-> scrive & il padre-> legge
la configurazione standard è quello di avere un' unica scrittura e un' unica lettura. 
il figlio eredita i descrittori del padre

Di solito l'operazione di:
- write è atomica (nulla o niente), se la pipe è parzialmente piena potrei scrivere solo una parte. se la pipe vuota la scrivo in maniera atomica.Se la pipe è piena si blocca. PIPE_BUF definisce il numero di carattere scrivibile automaticamente. 

- read (bloccante) si blocca se la pipe è vuota, normalmente la read ritorna a 0 se la pipe è stata chiusa dall'altra estremità. Quindi è necessario che tutte le estremità siano chiusi.

quindi se devo utilizzare la scrittura devo bloccare l'estremo che non utilizzo di lettura e viceversa.

se devo leggere e scrivere-> non blocco la pipe 
**esercizio**
su slide 23

Come si fa a definire la dimensione delle pipe. 

le pipe sono dei canali di comunicazione non strutturati (sequenza di byte), per averla strutturata avere un protocollo di comunicazione 