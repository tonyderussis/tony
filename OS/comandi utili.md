- - -
 *utilizzo di cp*
 - andare nella directory in cui si vuole copiare il file 
 - dal punto di vista di struttura: cp ../../path_di_sorgente  ./ (directory corrente)
 - less -N filename.txt fa si di darti il numero di righe e visulizza il file 
 - more filename.txt ti fa vedere il file 
 - cat filename.txt ti fa vedere il file 

*utilizzo diff*
- nota le differenze tra due file

*path assoluto e path relativo*
- path assoluto -> utilizza in scala gerarchica le directory 
- path relativo->  invece utilizza :
	[..] -> per specificare la directory padre della directory corrente (figlio)
	[.] ->  la directory stessa 

*cp e rm -r*
- si usano per le directories se si vuole copiarle o rimuoverle tutte 

*pwd*
ti printa tutto il percorso che hai fatto fino alla directory in cui sei 

*wc*
ti conta il numero di parole che sono presenti in un file (byte)

*chmod*

modifica i vari permessi in all, user, groups, è in divisione ottale. 

*ls -l*
mostra un elenco dettagliato dei file presenti in quella directory.
seconda colonna indica il numero di link che ci sono di quel file/ directory 

esempio di output di creazione : 

totale 28  
-rw-r--r-- 1 antonioderussis antonioderussis  439 28 ott 15.50 heart.py  
-rw-r--r-- 1 antonioderussis antonioderussis    0 28 ott 15.46 lab01e04in.copy  
-rw-r--r-- 2 antonioderussis antonioderussis 5202 28 ott 15.47 lab01e04in.hl  
lrwxrwxrwx 1 antonioderussis antonioderussis   14 28 ott 16.32 lab01e04in.sl -> lab01e04in.txt  
-rw-r--r-- 2 antonioderussis antonioderussis 5202 28 ott 15.47 lab01e04in.txt  
-rw-r--r-- 1 antonioderussis antonioderussis 5202 28 ott 16.30 labe01e04in.copy

diff file_in.txt file.copy manca la new line alla fine con gli altri invece non ci sono differenze 



