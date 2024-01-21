---
- [ ] *guardare i bistabili e verilog su t420*
- [ ] la parte prima sui registri pure si trova su t420

**Contatori**
- contatore asincrono: i clock sono collegati a catena (ripple adder)
	i ritardi si accumulano in cascata il singolo ritardo di ciascun flip flop ha un ritardo di propagazione pari a T_pd quindi all' uscita m si avrà un ritardo pari a MT
- contatore con flip flop di tipo jk con il valore j = 0 e k = 0 il flip flop si congela il clock fa commutare in fronte di discesa 
- quando il clock fa commutare in fronte di discesa si ha un negative edge trigger 

**differenze tra contatori sincroni e asincroni**
- asincroni hanno un ritardo variabili e possiamo avere anomalie sui transistor 
- sincroni tutte le uscite di flip flop commutano sullo stesso segnale di clock esempio di contatore sincrono jk q4 commuterà quando q1,q2,q3 avranno uscite a 0 

- - - 
**Macchine a stati finiti**

- le uscite dipende dagli stati e dagli ingressi -> esempio la lavatrice 
- lo stato può essere cidificato in due bit si fa riferimento alla macchina di huffman se non c'è un cambio di stato i bit rimangono invarianti 
- per commutare da uno stato all' altro si fa utilizzo di un half adder dove passa il riporto più lo stato -> come ingresso il bit meno significativo 
- mealy -> dipende dagli ingressi 
- moore dipende dallo stato
- rete di uscita metto counter in parallelo 2 segnali che implementano un decoder 
- - -

**ritardi: tempi di setup e di hold**

- frequenza massima è legata al tempo di setup dei flip flop (sono i vincoli per definire le prestazioni di un circuito)
- tempo di setup -> deve rimanere stabile prima del fronte di clock 
- tempo di hold-> deve rimanere stabile per questo tempo dopo il fronte del clock 
- ritardo del clock -> ritardo legato dopo il fronte del clock 
- ritardo della logica combinatoria da tenere in considerazione 
- il ritardo di propagazione ci serve per stabilire il periodo di clock 
- **per calcolare il periodo minimo di clock ta = tempo di clock + tempo massimo della logica combinatoria + il tempo di setup  < periodo di clock** -> per far funzionare il tutto 
- il periodo di clock deve contenere di più rispetto a tutti i ritardi presenti come quello di clock di setup e della logica combinatoria 
- il tempo di hold limita il ritardo della locica combinatoria 
- **tempo di hold deve essere > del tempo di clock + il tempo minimo della logica combinatoria**
- come ridurre i ritardi fare più livelli di porte 
- le prestazioni sono ridotte dai ritardi 
- - - 

esercizio b3.3 vedere slide
**domande di repilogo**

![[Pasted image 20230325150300.png]]


- quanti flip flop servono per realizzare un contatore mod 17? 5 