- - -

**comando find**
fa in modo di ricercare all' interno del disk e si utilizzano le espressioni regolari
esempio trovare tutti i file .txt si utilizza 
- find .* /.txt
- per analizzare dei file in un server apache si utilizza awk

espressione regolare -> modo semplice per rappresentare le stringhe 

automa non deterministico -> quando scrivo l'espressione regolare si crea questo tipo di automa
automa deterministico -> fa in modo di trovare la parola 

esempio -> le lettere mi rappresenta una sequenza di lettere
 l'*asterisco* indica 0 più ripetizioni. 

   altri tipi di caratteri: 
   - [] -> chiamata classi rappresentano un unico carattere in quell' insieme.
   - Esempio [a-z] caratteri che vanno dalla a minuscola alla z.
   - esempio se io scrivo questa espressione [_a-z A-Z]  [a-z A-Z 0-9] questo rappresenta una variabile
   - nelle espressioni regolari di tipo esteso c'è | (or) -> or esempio (a|b)
   - il simbolo + -> indica 1 o più ripetizione
   - il ? rende tutto opzionale
   - ^ -> rappresenta la negazione
   - per uno specifico numero di ripetizione -> {n} n volte ripetute. 
   - {n1, n2} -> indica l'elemento è presente da n1 a n2 volte
   - . -> qualsiasi carattere 

esempio ricerca espressione palindroma:
find (.)(.).\\ 2\\ 1 espressione palindroma di 5 caratteri in cui in 3 posizione ci può essere qualsiasi carattere

#### comando find
se metto find . [ opzioni ]] [ azioni ]]

esempi find . -name "* . txt"
find . -name ".???"
*? -> il punto interrogativo in questo caso indica qualsiasi carattere*

- find  . -regex ".* \\\ .txt" 
- comando "-mindepth" fa una ricerca ricorsiva sul mio albero da grado 1
- find . -name "* .txt" -mindepth 2 -> fa una ricerca dal livello 2 del mio albero di directory 
- ricorda che la ricerca è sempre ricorsiva
con il find devo matchare tutto il path e non solo il file 

*opzione exec*
fa uno specifico comando dopo aver trovato il file con il comando find 
es: find . -mindepth 2 -name "* .txt" -exec ls -l \{} \; 
posso anche mettere un -delete alla fine per cancellare i find

