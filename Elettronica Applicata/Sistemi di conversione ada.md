
**filtro di ricostruzione**
riconvertire il segnale impulsivo in analogico 
il filtro deve fare attenzione alla ricostruzione 

**quantizzazione**
dobbiamo mappare in valori discreti di 2^n, solitamente questa operazione è quella di assocciare tutti i valori nell'intervallo in centro 
a->d
ciascuno di questi valori analogici vengono assocciati al range dell' intervallo digitale. 
Ciascuno di questi intervalli facciamo corrispondere un codice nella rappresentazione in binario 
**errore di quantizzazione**
come lo associamo?
per i valori che si trovano a sx e dx si ha effettivamente l'errore a differenza del centro che è zero
l'errore di quantizzazione è compreso tra -s.
Caratteristica di conversione 
![[Pasted image 20230509163915.png]]

processo di quantizzazione 
processo ideale sommando l'errore di quantizzazione 
trattandolo come un rumore possiamo calcolare la varianza 

**potenza del rumore di quantizzazione**
![[Pasted image 20230509164259.png]]

**rapporto segale / rumore**
![[Pasted image 20230509164657.png]]

supponiamo di avere un' ampiezza s, i valori digitali andranno tra 0 e il numero di codici dispoinibili.
come se avessi fisso sempre a zero. 
Dimezzando l'ampiezza del segnale perdo un bit di precisione, nel caso di 4 perdo 2 bit di precisione. 
Io devo cercare che il mio segnale occupi tutto il range a disposizione sennò ho una perdità.

![[Pasted image 20230509165506.png]]
in A = S ho un ampiezza più grande quindi alcuni valori saranno fuori tra 0 e S, saranno infatti convertiti fino al val max. importante ad operare in ampiezza pari alla dinamica del sistema di conversione. 
La parte di condizionamento.

![[Pasted image 20230509165721.png]]
se il seganle ha ampiezza piccola l'amplificatore fa si in modo da rientrare nella dinamica S in modo da impedire il sovraccarico 
il filtro anti- aliasing limita le code del segnale in modo da non disturbare il segnale
nel sistema di acquisione in S/H campiona il segnale è lo rende constante 
ADC invece fa la vera e propria conversione
il MUX viene utilizzato per i canali da convertire sono tanti quindi indirizza in un solo  segnale analogico. 
