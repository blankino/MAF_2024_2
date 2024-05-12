# MatProgCsom projekt 2024
Imre Balázs, Kövér Blanka, Somorjai Noémi Anna

## A játék leírása
A 2023/24-es MatProgCsom tárgy keretein belül egy logikai rejtvény megoldási folyamatát implementáltuk. A rejtvény szabályai a következők:

Töltse ki az ábrát "pókokkal" az alábbi szabályok alapján:

+ Az ábrában minden pókhálóhoz igyekszik egy pók, ami azt jelenti, hogy a vízszintesen vagy függőlegesen közvetlenül szomszédos mezőben található.

+ Pókot tartalmazó mezők nem érintkezhetnek egymással, még átlósan sem.

+ Az ábra szélén látható számok azt jelzik, hogy az adott sorban ill. oszlopban hány pók van.

A Jupyter Notebookban található egy feladvány, illetve ennek helyes kitöltése a feladat szemléltetése céljából. (Ezek offline megjelenítéséhez a Jupyter Notebookkal együtt a megfelelő képeket is le kell tölteni a projekt mappájából.)

## A program
A programmal alapvetően azt igyekeztünk szimulálni, ahogyan egy emberi játékos megoldaná a feladványt: először megpróbáljuk "kilogikázni" a következő lépést, például különböző mintázatokat keresve, ha pedig ezekkel már nem tudunk továbblépni, akkor backtrackingre támaszkodva a DFS algoritmussal keressük a megoldást.

A táblát egy $N \times N$-es NumPy array-jel reprezentáljuk, valamint eltároljuk mellé azt a két vektort, amelyek azt adják meg, hogy az egyes sorokba, illetve oszlopokba hány pókot kell még beírni. A táblázatban az alábbi jelöléseket használjuk:

+ 0: még üres mező
+ 1: kielégítetlen pókháló
+ 2: kielégített pókháló
+ 3: kielégítetlen pók
+ 4: kielégített pók
+ 9: olyan mező, ahova nem kerülhet pók
 
A terminológia szorul némi magyarázatra:

A játék szabályai előírják, hogy a helyes kitöltésben minden pókhálóhoz kell tartoznia póknak. Ha egy pókhálóra már egyértelmű, hogy melyik vele oldalszomszédos pók tartozik hozzá, akkor őt és pókját kielégítettnek nevezzük, addig pedig kielégítetlennek.

A kódot egy Jupyter Notebookban töltöttük fel. Ebben ezenkívül megtalálhatók még a további instrukciók és magyarázatok a program futtatásához, illetve számos futtatható példa, amiből egy a Restart and Run All paranccsal le is fut.
