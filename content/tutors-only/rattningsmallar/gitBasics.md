---
title: Git och Github (Basics)
weight: 70
---

Git och Github (basics)-uppgiften går ut på att skapa ett git-repo, hantera historiken för enskilda filer, lägga till filer, committa och publicera repot på Github.

### För att eleven ska bli godkänd krävs
*Mer detaljerad information om punkterna finns efter listan, tillsammans med en
beskrivning på hur en kontroll kan utföras.*

1. Repot/Mappen samt tar-filen innehåller elevens student-ID på formen `abcd1234-git-test`.
2. Det existerar ett git-repo i mappen
   - Kontrollera detta mha. `git status`
3. Mappen innehåller samtliga förväntade filer och inga extra filer: `color.txt` och `food.txt`.
4. Commit-historik
   + I samtliga *log*-meddelanden ska elevens ID och studentmail stå som author.
   + Samtliga specificerade *commits* ska finnas närvarande i git log, helst
     i samma ordning som exemplet nedan.
   + Det ska finnas minst fem commits 

***
`OBS!` **Om commit-historiken innehåller alla obligatoriska commits _och_ flertalet
andra commits blir eleven godkänd OM det går se att denne utfört uppgiften på det
sätt som förväntats.**
***

## Detaljerad beskrivning
### 1. Klona repot
Börja med att klona repot med `git clone <länk>` 
<br/>
### 2. git-repo existerar
För att testa huruvida ett git-repo existerar kan du använda kommandot
`git status`. Om ett repo **existerar** får du följande meddelande:

``` shell
On branch master
nothing to commit, working directory clean
```

Om ett repo **inte existerar** får du följande meddelande:

``` shell
fatal: Not a git repository (or any parent up to mount point /home/kira)
Stopping at filesystem boundary (GIT_DISCOVERY_ACROSS_FILESYSTEM not set).
```
### 3. Mappen innehåller samtliga förväntade filer.
Mappen ska innehålla dessa filer och endast dessa filer:

``` text
.
├── color.txt
└── food.txt
```
### 4. Kontrollera innehållet i filerna.
Detta gör du enklast med kommandot `cat`. Så:
```shell
cat color.txt
My favorite color is Red.
```
samt 
```shell
cat food.txt
My favorite food is Kebabpizza.
```

### 5. Kontrollera sedan commit historiken.
Detta gör du enklast med kommandot `git log`. Så:
```shell
git log

commit 594cdc385692762e68e4a9672d4fae2a78c37d92 (HEAD -> master)
Author: kamar535 <karl.marklund@it.uu.se>
Date:   Fri Aug 20 19:49:08 2021 +0200

    So sweet

commit 62e83492a0d72c1721ae519a0079e4c6a7b36411
Author: kamar535 <karl.marklund@it.uu.se>
Date:   Fri Aug 20 19:47:27 2021 +0200

    Waffles are better

commit 11ee6f0d222e2b3123762781e7e5e662ae6536f7
Author: kamar535 <karl.marklund@it.uu.se>
Date:   Fri Aug 20 19:45:32 2021 +0200

    Pizza is the best

commit 88606137bc39ffe8d4529dbc934172f95e70e754 (HEAD -> master)
Author: kamar535 <karl.marklund@it.uu.se>
Date:   Fri Aug 20 19:40:34 2021 +0200

    Sorry brown, you and me forever

commit dca4e654d3cf6ffdb9ab4ce0a76633332a101a55 (HEAD -> master)
Author: Adam Andersson <abcd1234@beurling.it.uu.se>
Date:   Fri Aug 20 18:03:44 2021 +0200

    I now like orange better

commit c7762ffaa1d9cb6d32b0e33340542c63efc2fed0
Author: Adam Andersson <abcd1234@beurling.it.uu.se>
Date:   Fri Aug 20 17:42:20 2021 +0200

    I like brown
```

Det skall finnas **minst 5 commits**. Helst i ordning. Finns det fler där de obligatoriska commitsen finns med är det fortfarande godkänt! 

***
`OBS!` **Om du ser färre commits än 5, prova att trycka på pilen nedåt på tangentbordet. Finns det färre commits än 5 är det underkänt.**
***