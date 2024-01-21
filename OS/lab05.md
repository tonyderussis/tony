- - -
#### es1
prendere esercizio 1 lab 4 e fare in modo di fare il trasferimento delle stringhe attraverso una pipe ma sapendo che le misure delle stringhe non si sanno a priori passarle in input la lunghezza della stringa. 

utilizzi la funzione di libreria pipe(fd):  int fd[2] che è il vettore di interi: 
fd[0] descrittore per la lettura della pipe
fd[1] descrittore per la scrittura della pipe

---
#### es2 
scrivere un programma di sincronizzazione attraverso le pipe in modo da fare una sincronizzazione tra padre e figlio e per far terminare il figlio. 
di fatto utilizzare i vincoli sulle operazioni di scrittura e lettura in quanto sono operazioni bloccanti. 

- - -
#### es3 
espressioni regolari per cercare file 
- find \\".* \\.exe" -executable -size +1k -> cerca file eseguibili maggiori di 1024 bytes
- find \\ ".* \\.c" -size +100c -> file in c maggiori di 100 bytes
- find / -type f -regextype posix-extended -regex "(.*A.*a.*)|(.*a.*A.*)" -exec tail -n 3 '{}' \\;-> questo tipo di espressione regolare ricerca tramite l'espressione regolare estesa qualsiasi file con a-A oppure A-a in mezzo alla parola in modo poi tramite una exec estrare le ultime 3 riche dei file. 
- find / -mindepth 3 -maxdepth 5 -user antonioderussis -size +250c -type f -exec wc -c(l -> conta le righe) '{}' \;  -> trova tutti i file con livello di profondità da 3 a 5 con dimensione pari a o superiore di 250 bytes a livello utente e conta i caratteri 
- comando per compressare i file -exec tar -zcvf {}.tar.gz '{}' / ;
- find / -type d -name "bin" -exec ls -l '{}' \\; -> cerca la directories di nome bin. 
- type f-> file 
- type d -> le directories. 
- cercare tutti gli user eccetto il mio che possiedono i file in c -> find / -type f ! -user antonioderussis -regex ".* \\.c" -print
- trovare i file e cambiare i permessi -> find / -type f -minddepth 0 -exec chmod +x '{}' \\; 

- - - 
#### es4 
- per ordinare in maniera decrescente numberly -> sort -r -k1,1 -n lab05e04in.txt
	-r decrescente e -n in maniera numerica. 
- ordinare la matricola in modo che la cifra finale sia 2 oppure 4 -> grep -E "[0-9]* (2)\>" -E "[0-9]* (2)\>" 
- scrivere gli studenti che non hanno ancora frequentato che sono iscritti al ITCH e ordinarli per matricola decrescente-> fare attraverso le pipe come segue
	grep "ITCH" | grep "da frequentare" | sort -r -k1,1 -n
- per selezionare un nome che abbia due AxxA -> fare grep -e "A..A"
- grep -v -> selezione tutto eccetto la corrispondenza evidenziata dalla regex 
- grep -e "A..A" lab05e04in.txt | grep -v "\\<A" | grep -v "A\\>"  
- cut -c 1,1-6 lab05e04in.txt | tr -d 0 | tr 8 1 | sort | uniq -c -> seleziona la prima colonna cancella 0 sostituisce 8 con 1 mette in ordine e unifica 