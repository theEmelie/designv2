Laddningstid
=======================

Denna rapport handlar om att se hur snabbt hemsidor laddas.

Urval
-----------------------
Jag valde att analysera SEB, Nordea och Handelsbanken. Dom är alla populära banker, och tänkte att det
kan vara intressant då många personer använder deras hemsidor.

Metod
-----------------------
Jag använder verktyget [PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/) för att analysera laddningstiderna på dom olika webbplatserna. Jag använder även DevTools för att kolla det genomsnittiga hastigheten på webbplatserna. Jag har också gjort en kalkylark där jag jämför dom olika värdena på hemsidorna. [Google Kalkylark](https://docs.google.com/spreadsheets/d/e/2PACX-1vTOBlrCau4biA0JKBfIxVAbP9rxj0wE6Mq0m5IFuSqd7aTwPW8IIPd86wNwBqMmAHE-Vowha5TvqNoZ/pubhtml).


Resultat
-----------------------
Jag började med att analysera [SEB](https://seb.se/)
[FIGURE src="image/rapport/seb.png" alt="seb" width="200" height="300"]
Resultatet på deras hemsida när jag mäter laddningstiden är 31 på datorn, och 24 på mobilen. Alla resultaten är antigen i det gula eller röda på datorn. Och på mobilen är allt i det röda.
När jag mäter med DevTools får jag fram att det tar ungefär 3-5 sekunder att ladda hela sidan när cache minnet är rensat, den är cirka 1.1 MB stor och använder totalt 40 resurser.
För att göra hemsidan snabbare kan dom bl.a. aktivera textkomprimering (skulle spara cirka 4.5 sekunder), skjuta upp CSS som inte används (skulle spara cirka 2.55 sekunder) och ta bort resurser som blockerar renderingen (skulle spara cirka 2.52 sekunder).

Sedan analyserade jag [Nordea](https://www.nordea.se/)
[FIGURE src="image/rapport/nordea.png" alt="nordea" width="200" height="300"] Resultatet på deras hemsida när jag mäter laddningstiden är 54 på datorn, och 72 på mobilen. De mesta utav resultaten är i det gula, endast hastighetsindexen (hur snabbt sidan har fyllts med synligt innehåll) och första CPU-inaktivitet är i det röda. När jag mäter med DevTools får jag fram att det tar ungefär 3 sekunder att ladda hela sidan när cache minnet är rensat, den är cirka 1.2 MB stor och använder totalt 51 resurser. För att göra hemsidan snabbare kan dom bl.a. minska svarstiderna från servern (skulle spara cirka 1.64 sekunder), skjuta upp CSSen (skulle spara cirka 1.59 sekunder) och skicka bilder i morderna bildformat (skulle spara cirka 1.2 sekunder).

Sist analyserade jag [Handelsbanken](https://www.handelsbanken.se/)
[FIGURE src="image/rapport/handelsbanken.png" alt="handelsbanken" width="200" height="300"]
Resultatet på deras hemsida när jag mäter laddningstiden är 73 på datorn, och 66 på mobilen. På både datorn och mobilen är deras första uppritning av innehåll i det gröna. med bara 4ms skillnad. Även hastighetsindexen är i det gröna på datorn.
När jag mäter med DevTools får jag fram att det tar cirka 2-3 sekunder att ladda hemsidan när cache minnet är rensat, det är cirka 1 MB stor och använder totalt 37 resurser. För att göra hemsidan snabbare kan dom bl.a. skicka bilder i moderna bilformat (skulle spara cirka 0.9 sekunder), koda bilder effektivt (skulle spara cirka 0.75 sekunder) och ta bort resurser som blockerar renderingen (skulle spara cirka 0.66 sekunder).


Analys
-----------------------
Det vanligaste förbättringsåtergärderna för hemsidorna är att koda bilerna mer effektivt och skjuta upp CSS som inte används. Även att minifiera CSS och JavaScript.

Om man ska jämföra webbplatserna med varandra kan man enkelt säga att Handelsbanken har bäst mätvärden och vinner över SEB och Nordea. Det enda som är värre i Handelsbankens mätning är deras inmatningslatens som är 290 ms, medans den är 80 ms hos Nordea och 230 ms hos SEB. Nordeas tid till interaktivt tillstånd är också nästan 1 sekund snabbare än Handelsbanken, men med restan utav värderna är Handelsbanken bättre. Även deras laddningstid är snabbare, den har minst storlek och minst resurser som hjälper att ladda hemsidan snabbare.


Övrigt
-----------------------
Jag tycker inte att laddningstiden på en hemsida ska överskrida 3 sekunder. En snabb hemsida tycker jag ska ladda på ungefär 1.5-2 sekunder. Men är det mer än 3 sekunder anser jag den som långsam. SEB klarar inte mitt gränsvärde på 3 sekunder, ibland när jag laddade om sidan kunde det vara så illa att det tog 14 sekunder!? Deras hemsida är alldeles för långsam, jag tror att en del utav det har med att göra att dom har stora bilder på framsidan. Nordea ligger på gränsen, tog oftast runt 3 sekunder att ladda klart hela hemsidan, vilket ändå är bra med tanke på att dom har några stora bilder på hemsidan och även mycket annat som händer. Handelsbanken är snabb, tog oftast inte mer än 2 sekunder att ladda allt, dom har inte så stora bilder på deras framsida. Men dom har en video så jag tycker att dom har lyckats bra.


<b>Skrivet utav: Emelie Åslund</b>
