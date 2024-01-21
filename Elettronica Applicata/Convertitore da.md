data la retta ideale e la retta reale si confrontano le due rette si fa un approssimazione, spostando questo punto da dx a sx abbiamo una variazione, 
![[Pasted image 20230509172553.png]]
avendo Ad e Ad' è un errore di non linearità non differenziale.
se questo errore tende ad essere più grnade di un gradino (LSB), nel bit meno significativo perchè ci dice che noi saliamo o scendiamo di un gradino. Quindi posso avere dei comportamenti anomali, se questo errore è molto grande si ha un errore di non monoticità, se è più grande di gradino, quindi si avrà un cambio di pensenza. 
![[Pasted image 20230509172855.png]]
ed è dovuto che da qualche parte della caratteristica ed è più grnde di lsb , in questo caso è più grande di due volte. Ad un errore di non linearità differenziale, non neccessariamente corrisponde un errore di non linearità. 

**tempo di assetto**
ci sarà un tempo minimo per far salire l'uscita che è data dal rapporto tra dv e dt , un volta raggiunta la tensione max, ci possono essere delle variazioni che possono causare delle oscillazioni. 
Il tempo di assetto.Quando le oscillazioni stanno a metà di lsb. parametro dinamico che caratterizza il suo setting time.

![[Pasted image 20230509180938.png]]
**Glitch**
variazioni di bit di ingresso per la quale non tutti i bit non cambiano allo stesso tempo, e possono manifestarsi delle variazioni di tensione che possono avere ampiezza molto grandi. 
![[Pasted image 20230509181001.png]]
QUESTO PASSAGGIO FA CAMBIARE TUTTI BIT, se cambiano tutti i bit significativi posso passare in 0000 e mi troverei in un valore digitale che corrisponde alla tensione minima, questi ritardi dati dalla differenza di lsb delle due tensioni possono così causare i cosidetti glitch. 

**Alcuni schemi di convertitori ad**
possono classificare con:
- grandezze pesate -> binario 
- grandezze uniforme -> con pochi bit
![[Pasted image 20230509182044.png]]
questi convertitori a grandezze pesate si hanno resistenze con valori molto molto diverse.Si oreferisce avere resistenze simili si sfrutta la rete a scala che è una particolare rete che tiene conto di due valori di resistenza in modo di avere uno doppio dell'altro. Serie di interruttore pilotati dall'ingresso che selezionano. Grandezze analogiche sommate tra di loro che sono delle correnti. Al bit più significativo corrente grande, bit meno significativo corrente piccole; e si sommano se il bit è 1 oopure 0.
Amplificatore di transresistenze-> corrente in ingresso in resistenza. 

**Grandezze uniforme**
bit che mi danno lo stesso contributo uguale a tutti gli altri bit di ingresso, se dovessi convertire in 9d : 000111111111, così determinano le correnti che sono uguali e vengono sommate.

**Grandezze pesate**
bit del numero che voglio convertire ho delle grandezze pesate che da binario in decimale, 
esempio 9d = 1001 => 2^n_bit *  1 

in pratica come si realizzano questi circuiti?
in pratica chiudero gli interruttori che dove ci sono i bit ad uno -> gli interruttori sono 16 quindi chiudo 9 interruttori e li lascio aperti 7. 
nel caso di grandezze pesate le resistenze non sono uguali ma sono pesate con potenze di 2. A parità di numero di bit che voglio convertire abrò meno resistenze.
rete di scala dividi in 2 in 2 le resistenze per avere diverse correnti.

si possono avere anche reti di capacita -> in questo caso non si fa passare corrente, quando le capacità vengono caricate ad una tensione quindi il transitorio di carica si ha un consumo transitorio 

gli errori sono dovuti alla non idealità dei circuiti, ci saranno nelle variazione di corrente nel valore ideale invece di salire, e salgono in un gradino, e fanno si di non essere allineata dalla caratteristica ideale. 
l'amplificatore operazionale introdice delle non linearità che sono non lineare.



