- - -
partendo da un file testuale fa in modo di selezionare determinate righe e colonne
si riesce a fare diversi 
- cat -> stampa file 
- wc -> conta il numero di parole di un file 

**grep e sort**

#### comando cut
con il programma cut -> selezione determinati colonne del file
con il comando wget scarico determinate risorse da internet in locale 

posso fare ad esempio una selezione dalla colonna 2 alla colonna 5. 
esempio cut -c 1, 2-5 -> selezione la colonna
il comando cut -d ' ' -> fa uno spazio delimitatore
il comando cut -d ' ' 2,4 selezione le colonne 2 e 4 +
cut -f -> solo i caratteri 

#### comando tr 
esempio posso usare tr per fare manipolazione di caratteri in pipe esempio 
echo alla | tr a-z A-Z -> trasforma da minuscolo a maiuscolo
tr -s " "-> elimina le ripetizione, posso anche usarla per sostituire anche caratteri 
tr -d -> elimina i caratteri associati alle regex

#### comando uniq
comando uniq -> compatta le ripetizione all'interno di un file

uniq -c ti mette i nomi compattati senza ripetizione con di fianco il numero di ripetizione di ciascun nome. 
sort nome del file mette in ordine il contenuto del file


dirname -> mi da la direttoria principale 
basename-> invece fa in modo di togliere il path della directory 

posso anche fare delle variabili all'interno della shell facendo a = $(....) nome del file. 

#### comando sort
*sort*
facendo sort -k2,2 nomefile -> fa un sort partendo dalla colonna 2 fino alla colonna 2 
ad esempio a parità di cognome posso aggiungere il sort di un' altra colonna. 
sort -k2,2r -k3,3  nomefile
in questi casi faccio sorting alfabetico se invece faccio un sorting numerico -> metto un n vicino all ' upper bound della colonna ' 
#### comando head
comando head -> mi fa vedere i primi n del file -> head -n 3 
cat file1.txt file2.txt -> concatena il file 1 e il file 2 

*grep*
cerco all'interno del file una determinata espressione regolare
egrep -e "\<B" seleziona tutte le parole che inizia con la parola B

egrep -e "^[1-9][0-9]* [02468]\>" -e "^[02468]\>" example txt -> mi matcha tutte le matricole tra di numero pari 
egrep -B 2 -A 1 -e "^002" -> fa una espressione regolare in grado di valutare ad esempio due istanti prima dell'attacco e una dopo l'attacco

il $ fa in modo di non prendere il numero con la virgola nella ricerca 

**esempio** 
comando di espressione regolare in grado di ordinare tutti i voti sufficienti 
egrep -e "30.0$" -e "2[0-9 ]\ .[0-9] $" -e "1[89]\.[0-9] $" -e "17\.[5-9] $" example.txt | sort -k4,4rn | head -n 1 | cut -d " " -f2 > file.txt
 output nel file.txt BIANCHI
 