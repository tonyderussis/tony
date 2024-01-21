---

**Comparatori di soglia**
i comparatori funzionano attraverso un ingresso analogico e un' uscita binario legata al valore logico alto oppure basso (1/0) -> tale stato dipende dal confronto con il valore soglia se l'ingresso I > S => U = H se invece I < S => U = L

Comparatore con AO 
- il guadagno ad anello è molto alto 
- l'escursione della tensione di uscita è limitata da VuH = Val + e da vuL = Val-
- la zona lineare della tensione di uscita è data VU = vd* Ad 
- l'amplificatore operazionale ad anello aperto può essere utilizzato come comparatore 
- differenza tra comparatore non invertente e invertente sta nel fatto che quello non invertente il segnale analogico commuta al fronte del segnale analogico, caso speculare per quanto riguarda quello invertente; Inoltre i morsetti per il non invertente il + verso l'alto e il - verso il basso con tensione di source

Effetti del rumore
- per ridurre tali effetti si mettono due tensioni di soglia così facendo si fa commutare il segnale solo quando passa in una di esse. 
- le tensioni vs1 e vs2 dipendono dalle tensioni di uscita e dal rapporto di **reazione positiva **
- - - 

**Trigger di Schmitt**
tensioni e correnti sono meno critiche rispetto ad un opamp e inoltre sono più veloci 

generatori di onda quadra -> il condensatore viene caricato e scaricato esponenzialmente 
filtro passa basso all'ingresso la tensione cresce decresce in base all'ingresso 
![[Pasted image 20230331172845.png]]
segnale funziona come opamp invertente 
il condensatore si scarica e carica in base alle tensioni soglia viste prima
la corrente presente sulla resistenza deve essere vicina tra ioh o iol senno non rispetta il vincolo legato alla resistenza.

**Oscillatori**
oscillatore ad anello: 
- formato da un numero dispari di inverter genera un onda quadra di periodo T = N(tpdlh + tpdHl)
- criterio di Barkhausen AB = -1; oscillatori -> uscita anche se I = 0 quindi c'è oscillazione 
- ![[Pasted image 20230331175210.png]]

Struttura : 
- guadagno A è costante
- guadagno di reazione B dipende dalla frequenza
- per far partite l'oscillazione AB = -1

Oscillatore di pierce 

Rf -> forza tensione di ingresso e di uscita di essere uguali 
R2 -> la resistenza protegge il quarzo 
b(f0) >0 cosi si ha un guadagno negativo 

Effetto rs -> filta armoniche dal segnale digitale -> sinusoide 
sintesi con pll -> f clock = N x f riferimento 

![[Pasted image 20230331180505.png]]

rilevatore di fase identifica quando l'oscillatore è troppo veloce e la logica si base sul confronto tra seganali up e down in quanto a deve essere in anticipo rispetto a b in caso contrario resetta finchè non funziona (formato da due flip flop di tipo d) 


pompa di carica : generatore di tensione controllato da due interruttori serve per regolare l'oscillatore in caso in cui sia troppo lento (chiudo l' interruttore up) troppo veloce scarico la corrente (chiudo interruttore down ) se chiudo tutte e due si scarica il condensatore. 
- - - 
#domandesucomparatori 
1. quali parametri descrivono un comparatore soglia ? 
 - i parametri che descrivono tale comparatore sono gli stati delle uscite in quanto possono essere di soglia alto oppure basso, in quanto in ingresso prendono un segnale analogico e in uscita uno digitale e quindi se sono entro qualche soglia rappresentano il valore logico alto oppure basso. 
 2. per quale motivo i comparatori sono in isteresi? per il fatto di associare il giusto valore solo in casi esterni al segnale di ingresso in quanto ci può essere molto rumore. 
 3. 