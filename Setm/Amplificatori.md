- - -

*amplificatori*
blocco funzionale si basa su segnale di ingresso moltiplicato per una costante.
utilizzo:
- applicato all'inizio della catena di acquisizione per rendere il segnale più dinamico e renderlo immune ai rumori. 
- fornisce potenza necessaria per pilotare gli attuatori (amplificatori di potenza)
	[y(t) = Ax(t)]
	
bottle-neck : 
*comportamento in ingresso*
-  caso ideale di tensione e trans-conduttanza: nella porta di ingresso dell'amplificatore assorbe tensione. Porta di ingresso si comporta come circuito aperto. 
- caso ideale di corrente e trans-resistenza: nella porta di ingresso dell'amplificatore assorbe corrente.Porta di ingresso si comporta come cortocircuito.
*comportamento in uscita*
- caso non ideale di tensione e trans-conduttanza: la tensione in uscita dipende dalla corrente al carico 
- caso non ideale di corrente e trans-resistenza: la corrente in uscita dipende dalla tensione sul carico

*calcolo resistenze di ingresso e di uscita*
- in ingresso: Rin = vin / i_t con i_t -> corrisponde alla corrente di test applicata in ingresso
- in uscita: $Rout =\frac{vout}{i_t}$
- con i_t -> corrisponde alla corrente di test una volta tolto il generatori indipendenti 

*considerazioni su idealità e non idealità*
calcolo della tensione di uscita: 
- ideale: tensione di uscita uguale alla tensione di ingresso moltiplicata per una costante
- non ideale: tensione di uscita uguale al partitore di tensione applicata alla resistenza in parallelo con il generatore pilotato moltiplicato per la costante.

*come evitare effetti di carico ingresso/uscita*
Amplificatore tensione: 
- ingresso: $Rs << Rin$ 
- uscita: $Rl >>Rout$

Amplificatore corrente: 
- ingresso: $Rs >> Rin$ 
- uscita: $Rl <<Rout$

Amplificatore trans-conduttanza: 
- ingresso: $Rs << Rin$ 
- - uscita: $Rl <<Rout$

Amplificatore trans-resistenza: 
- ingresso: $Rs >> Rin$ 
- - uscita: $Rl >>Rout$




 
