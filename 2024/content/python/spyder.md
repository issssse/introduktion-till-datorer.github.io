---
title: Anaconda och Spyder
weight: 10
---

Ett enkelt sätt att komma igång med Python är att använda [Anaconda][anaconda]
och [Spyder][spyder] vilka redan finns tillgängliga på datorer i datorsalarna på Campus
[Ångströmlaboratiet][ångström]. 

Det är starkt rekommenderat att du [installerar Anaconda][download] som
inkluderar Spyder på din egen dator.

Instruktionerna på dessa sidor kommer visa hur du använder Anaconda och Spyder på en dator
i datorsal på Campus Ångström. Om du installerar och kör Anaconda på din egen
dator bör du kunna följa alla instruktioner utom de som rör hur du startar
Anaconda och Spyder.

[ångström]: https://angstrom.uu.se/
[anaconda]: https://www.anaconda.com/
[spyder]: https://www.spyder-ide.org/
[download]: https://www.anaconda.com/download/

## Logga in på en dator i datorsal

[Logga in][login] på en dator i en datorsal på Campus Ångström. 

[login]: computer-rooms/#logga-in-p%C3%A5-dator-i-datorsal-p%C3%A5-campus-%C3%A5ngstr%C3%B6m

## Starta Anaconda Navigator

Skriv in `anaconda` i sökrutan i aktivitetsfältet (1).

![](/images/python/spyder/search-anaconda-navigator.png)

Om Anaconda Navigator finns installerat dyker **Anaconda Navigator App** upp 
bland resultaten (2) och du kan nu starta detta program. 

## Software Center (ZENworks)

Om det inte går att starta Spyder från sökrutan i aktivitetsfältet behöver du
installera Anaconda med hjälp av Software Center (ZenWorks). 

Någonstans på skrivbordet hittar du **Software center (Zenworks)**.


![](/images/linux/software-center-icon.png)

Dubbelklicka på ikonen för **Software center (Zenworks)**. Nu öppnas ett nytt
fönster med tillgänglig mjukvara. 

![](/images/linux/software-center.png)

Den mjukvara som du hittar här kan redan vara installerad på den dator du
sitter vid. Om ett program inte redan är installerad kommer det att installeras första gången du
försöker använda programmet. 

Leta reda på Anaconda och dubbelklicka på ikonen för att installera programmet. 


## Anaconda Navigator

Första gången du startar Anaconda Navigator möts du av följande ruta där du får
valet att skapa ett Anaconda Cloud account. 

![](/images/python/spyder/cloud-login.png)

Om du inte vill skapa ett Anaconda Cloud account stänger du helt enkelt denna
ruta. Efter att du stängt denna får du se en lista med program som finns
tillgängliga i Anaconda Navigator. 

![](/images/python/spyder/navigator.png)

## Starta Spyder

Leta reda på Spyder och tryck på **Launch**. 

![](/images/python/spyder/launch-spyder.png)

Så här ser Spyder ut första gången du startar programmet. 

![](/images/python/spyder/spyder-first-launch.png)

![](/images/python/spyder/spyder-first-launch.png)

## Python Console och prompten

Nere till höger i Spyder hittar du **Python Console** vilket är ett Python REPL. 

![](/images/python/spyder/python-console.png)

I Python Console används `In [1]:` som prompt. Här kan du skriva in Pythonkod en
rad i taget och resultatet skriv sedan automatiskt ut på en egen rad. 

Skriv in `1+1` vid prompten och tryck enter. Resultatet `2` visas nu på nästa rad med prefixet `Out[1]`. 

En ny prompt `In [2]:` visas nu. Skriv in `3*3 + 5` och tryck enter. Resultatet
`14` visas nu på nästa rad med prefixet `Out[2]`.  

![](/images/python/spyder/console-first-try.png)

Prompten visar en siffra som räknar antal kommandon du utfört. Samma siffra
används även av det efterföljande resultatprefixet. 

## Förenklad prompt 

I alla kommande exempel kommer den förenklade prompten `>>>` användas och
resultatprefixet kommer utelämnas. Följande exempel i Python Console:

``` text
In [1]: 1+1
Out[1]: 2

In [2]: 
```

, kommer i alla kommande exempel att se ut så här: 

``` text
>>> 1+1
2
>>> 
```

Den första raden: 

``` text
>>> 1+1
```

, betyder inte att du skall skriva skriva in `>>> 1+1` i Python Console. Det
betyder att du skall skriva in `1+1` efter prompten i Python Console. 

En rad med endast `>>>`: 

``` text 
>>>
```` 

, betyder att en ny prompt kommer visas här i Python Console. 