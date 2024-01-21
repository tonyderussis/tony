file system contiene tutti i file, directory ecc.. 

impiego di file binari per una maggiore portabilità nel sistema: 
- compattezza 
- modificabilità 
- facilità di posizionarsi 

serializzazione -> si riesce a ricostruire o trasmettere un file come un' unica entità 


impiego della fat -> esempi: usb.
tema di esame sul file system

- es1
con metodo fat allocare 3 file 
file1 2.4
file2 1.6
file3 3.9 

posso allocare il file1 2,3,4, file 2 4,5 il file 3 non è allocabile 

tipi di allocazione concatenata, indicizzata vedere pdf su blocco 3 c'è la soluzione 

- es2
cosa si intende directory block

directory block -> blocco dove indicizza le directory entry 
directory entry -> filename + # i_node 
data blocco -> blocco per dati file 
i-node -> almeno 1 per ogni file che ha puntatori blocchi dati e altre informazioni. 

permessi/ diritti -> chmod e vari comandi figli con ch

softlink -> file che contiene il puntatore che contiene file originario 
hardlink -> puntatore dalla directory entry all 'i-node 
ln [-s] file [link]

cp s1 s2 
rem s 



