- - -
transistor mos: 
- NMOS 
- MMOS 

**nmos**
- Ha tre terminali. 
- Nel gate la corrente è 0.
- corrente di source è opposta a quella di gate. 
- la corrente scorre tra drain e source. 
Nel terminale di gate non passa corrente perché è un terminale isolante. 
Tra il terminale source e gate NON può passare corrente. 

**pmos**
In questo caso rispetto al nmos la corrente tra drain e source scorre in senso opposto. 

**tensioni di controllo**
*nmos*: $V_gs$ e $V_ds$  tensioni presenti rispettivamente nella porta gate source e porta drain source. 
*pmos*: $V_sg$ e $V_sd$  tensioni presenti rispettivamente nella porta source gate e porta source drain.

**andamenti della corrente**
*nmos*
gli andamenti della corrente sono influenzati dalla tensione.
- se $V_GS$ è minore della tensione di soglia la corrente sarà 0.
- se $V_GS$ è maggiore della tensione di soglia e inoltre $V_ds$ è più piccola della differenza tra $V_gs$ con la tensione di soglia )=> la formula per calcolare la corrente
	$i_d = B V_ds *(V_gs - V_th - V_ds/2)$  
- nella rappresentazione grafica delle correnti, la loro pendenza dipende dalla resistenza di on controllata dalla tensione di gate.
-  se $V_GS$ è maggiore della tensione di soglia e inoltre $V_ds$ è più grande della differenza tra $V_gs$ con la tensione di soglia )=> la formula per calcolare la corrente
	$f$
- in questo la regione di saturazione mantiene invariato lo stato della corrente
- la corrente che c'è nella porta di uscita è pilotata dalla tensione nella porta di ingresso. (Amplificatore di transconduttanza )

*pmos* 
il comportamento uguale al nmos con la differenza che la resistenza e tensione di soglia sono diverse. 

**Esempio circuito con nmos**
notazione $v_GS$ -> tensione totale 
notazione $V_GS$ -> tensione in continua 
$v_GS$ = $V_in + V_GS$ -> tensione presente in ingresso 

*q saturazione:* 
- VGS > VTH 
- Vds> Vgs - Vth 
La tensione di gate (/drain) va ad oscillare nel punto q 

**rappresentazione lineare del mos**
approssimazione tramite serie di taylor. 

sistema con ingresso e uscita. 
ingresso -> componente di polarizzazione data dalle tensione in dc del circuito + variazione
uscita -> $f(x)$ può essere scomposta con una parte continua (polarizzazione) e una non continua (variazione).
linearizzando si ha $f(xi) + (df/dxin) * x_in(t) +o(x_in)$ -> $(df/dxin) = alpha$ (adimensionale) mi caratterizza ingresso uscita e mi indica la variazione del mio sistema. 
come vediamo è riconducibile alle costanti di un generatore pilotato. 

**circuito equivalente piccolo segnale: nmos**
corrente entrante nel drain e uscente nel source e l'intensità della transconduttanza, un altro contributo e vuol dire che la corrente di drain è data ro = 1/go. 
come si comporta il circuito -> se hai una corrente di segnale ids. 
E un circuito che vale solo per i segnali.

controllare le correnti 
![[Pasted image 20231115163429.png]]


**circuito equivalente piccolo segnale: pmos**

controllare le correnti 
![[Pasted image 20231115163554.png]]


*limiti di validità e dinamica*
la corrente sarà proporzionale alla tensione con relazione lineare 
andando avanti con la tangente del punto di lavoro, la corrente può andare in negativa mentre il mos impone il vincolo di corrente =0, questo implica un modello di validità. 
è presente un errore di distorsione (differenza tra il quadrato e la tangente). Questo errore è direttamente proporzionale alla grandezza del segnale. 
![[Pasted image 20231115164126.png]]

**effetti reattivi del transistore mos**
in alta frequenza non posso vedere la porta di ingresso come circuito aperto, anzi diventa un corto circuito. Il problema è la presenza della capacità $C_gs$. 