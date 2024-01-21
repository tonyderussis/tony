- - -
Due tipi di schemi operativi:
1. schema a blocchi -> elimina l' aliasing (frequenza di campionamento rispettata secondo il teorema di shannon)
2. trigger: pre e post trigger, campionamento casuale

**banda passante**
studio dell' attenuazione del segnale, frequenza di taglio da prendere in considerazione è quella di -3 db. 
la funzione di trasferimento della banda passante si calcola: 
H(db) = 20 log_10 |V_out / V_in| = 10 ^-3/20 = V_out / V_in => Vout = V_in * 10 ^ -3/20

la banda passante in questo caso è in grado di creare un filtro a passa basso (idealmente )
- per ridurre l'effetto dell' ampiezza del 2% : B = 5 * f_max 
- la banda inoltre ha effetto anche sul tempo di salita che si calcola t_so = K/B, con K compreso tra 0.35 e 0.45 

**selettore di ingresso**
fa si di selezionare il tipo di corrente :
- AC -> corrente alternata fa si che la corrente passi per un condensatore che funge come filtro a passa basso 
- Dc -> corrente continua

**attenuatore tarato**
resistenza variabile per manipolare la tensione ordine di mv/div  (manopola v_div)

**0 div**
manopola per cambiare il riferimento 







