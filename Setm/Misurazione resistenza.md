- - -

r = v/i -> nel caso in cui la corrente è più grande si ha una resistenza più piccola

effetto sistematico ? (se è trascurabile oppure no) nel caso in cui incertezza non mi da 0 1 % devo modificare r 
incertezza dato dal rapporto. 

**incertezza di tipo deterministico (di misura)**
epsilon(r) = epsilon(v) + epsilon(i)
![[Pasted image 20231025182322.png]]


**incertezza probabilistica della grandezza**
u_r(r) = sqrt(u_r(v)^2 + u_r(i)^2)
![[Pasted image 20231025182356.png]]

**effetto di carico strumentale**
si tiene conto di questo effetto in quanto la resistenza presente dentro l'amperometro è elevata ma non a infinito quindi bisogna tener conto delle probabili perdite e incertezze

due tipi di misurazione: 


- **voltmetro a monte (rispetto all'amperometro)**
resistenze grandi -> misurate con voltmetro a monte
mettendo una resistenza molto grande (mettere il voltmetro a monte) con una resistenza molto piccola. Si misurano la tensione misurata è data dalla somma tra quella dell'amperometro con quella del dipolo. 
r = (V + Va) / I = R + Ra

incertezza strumentale in valore assoluto in questo caso è dato da:
![[Pasted image 20231025190249.png]]

incertezza in valore assoluto: 
![[Pasted image 20231025190321.png]]



 
- **voltmetro a valle (rispetto all'amperometro )** 
resistenze piccole -> misurate con voltmetro a valle
in questo caso l amperometro misurerà una corrente pari a i + iv (la somma della corrente che passa tra il dipolo e quella nel voltmetro)
quindi la resistenza sarà r = v/ (i + iv) sostituendo avrò una resistenza equivalente a R // Rv
incertezza in valore assoluto del voltometro in questo caso è data: 
![[Pasted image 20231025184724.png]]

invece relativa è data: 
![[Pasted image 20231025184809.png]]
in questo caso basta dividere per r e si ha un'incertezza in cui non prende in considerazione R al denominatore in quanto ha resistività molto piccola rispetto alla resistenza Rv (del voltmetro).

**correzione dell'effetto di carico strumentale**
valutazione se l'incertezza legata al carico è trascurabile oppure no. 
si fa in base al confronto di R(resistenza misurata) con sqrt(Ra * Rv); 
- se R < sqrt(Ra * Rv) -> il voltmetro conviene metterlo a valle 
- se R > sqrt(Ra * Rv) -> il voltometro conviene metterlo a monte

nel caso in cui l'incertezza di misurazione non è trascurabile bisogna calcolarsi la resistenza quanto segue: 
- voltmetro a valle : 

![[Pasted image 20231025205705.png]]

- voltmetro a monte: 

![[Pasted image 20231025205749.png]]











