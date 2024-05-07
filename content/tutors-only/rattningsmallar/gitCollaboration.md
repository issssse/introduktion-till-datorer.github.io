---
title: Git och Github (Collaboration)
weight: 100
---

Git och Github (Collaboration)-uppgiften går ut på att skapa nya grenar (branches), hantera merge-konflikter och sammarbeta med andra kring samma projekt.

**Exempel-länk för korrekt repo (för två personer i gruppen) finns här: [GitHub länk](https://github.com/KianRafi1/test-oliver-kian).**

### För att eleven ska bli godkänd krävs
*Mer detaljerad information om punkterna finns efter listan, tillsammans med en
beskrivning hur en kontroll kan utföras.*

1. Repot/Mappen innehåller elevernas student-ID på formen `abcd1234-abcd1234-git-collaboration` eller `abcd1234-abcd1234-abcd1234-git-collaboration` om det finns tre medlemmar.
2. Det existerar ett git-repo i mappen
   - Kontrollera detta med kommandot `git status`
3. Mappen innehåller samtliga förväntade filer och inga extra filer: `members.txt`, `myList.txt`.
4. Commit-historik
   + I samtliga *log*-meddelanden ska elevernas ID och studentmail stå som author.
   + Samtliga specificerade *commits* ska finnas närvarande i git log, helst i samma ordning som exemplet nedan.
   + Det ska finnas en merge i commit-historiken med meddelandet *"Fixat merge konflikt"*. 

## Detaljerad beskrivning
### 1. Klona repot
Börja med att klona repot `git clone <länk>`.
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
### 3. Mappen innehåller samtliga förväntade filer
Mappen ska innehålla dessa filer och endast dessa filer:

``` text
.
├── members.txt
├── myList.txt
```
### 4. I branch *master* (eller *main*), kontrollera textfilerna
Kontrollera textfilen `members.txt` med kommandot `cat`, så:
```shell
cat members.txt

Användare på GitHub: ArneAnka
Namn: Arne Andersson
Epost: arne.andersson.1234@student.uu.se

Användare på GitHub: brittan
Namn: Britta Bengtsson
Epost: britta.bengtsson.1234@student.uu.se
```
Ungefär så skall det se ut. Om det finns 3 gruppmedlemmar skall det se ut såhär:
```shell
Användare på GitHub: ArneAnka
Namn: Arne Andersson
Epost: arne.andersson.1234@student.uu.se

Användare på GitHub: brittan
Namn: Britta Bengtsson
Epost: britta.bengtsson.1234@student.uu.se

Användare på GitHub: Carro99
Namn: Carolina Collberg
Epost: carolina.collberg.1234@student.uu.se
```
Kontrollera sedan textfilen `myList.txt`, så:
```shell
cat myList.txt

1. First
2. Third
3. Second
```

Om det finns 3 gruppmedlemmar skall det se ut såhär:
```shell
1. First
2. Third
3. Second
4. Fourth
```
### 5. Commit-historik
För samtliga commits ska studentens ID och mailadress vara satta som author.

#### master (eller main)
För att kontrollera commit-historiken, använd kommandot:
``` shell
git log
```

De commits som ska finnas närvarande, och **endast** i denna ordning, är:  

***
`OBS!` **Notera att det måste finnas en commit som är en merge. Detta kan du
se på att en extra rad med titel _merge_ finns i log-meddelandet (se första
posten i exemplet nedan).**
***

``` shell
commit b1ffa2242b8fb6ef6e836bb7734e6b834e0b5c67 (HEAD -> master, origin/master)
Merge: e0c8100 4ce6237
Author: kr4ften <oliver.kr4ft@gmail.com>
Date:   Sat Sep 4 19:30:48 2021 +0200

    Fixat merge konflikt

commit e0c8100ed3cfea0bd7446135b940872d5425e7dd
Author: kr4ften <oliver.kr4ft@gmail.com>
Date:   Sat Sep 4 19:26:24 2021 +0200

    Third - added

commit 4ce623750b5277c6af7062669adb67e08a26121f
Author: kr4ften <oliver.kr4ft@gmail.com>
Date:   Sat Sep 4 19:25:04 2021 +0200

    Second - added

commit 4ff53783cd658ec9ebe9553b5bad8670a2bacdf4
Author: KianRafi1 <73444377+KianRafi1@users.noreply.github.com>
Date:   Sat Sep 4 19:24:34 2021 +0200

    First - added

commit 1626ee30900e40b2709eb6078c7ff305359bc7d8
Author: Oliver Kraft <oliver@kraften.net>
Date:   Sat Sep 4 19:10:54 2021 +0200

    Person B added members.txt

commit f35bdc2aa1259ee14c4488deea9a74e5e23de0b3
Author: KianRafi1 <73444377+KianRafi1@users.noreply.github.com>
Date:   Sat Sep 4 19:05:59 2021 +0200

    Person A added members.txt

```
***
`OBS!` **De två första commiten ("*Person A added members.txt*" samt "*Person B added members.txt*") kan ha andra meddelanden.**
***

Detta är ett exempel på commit-historiken för två personer. För tre personer borde det finnas en till commit med valfritt meddelande, dock **max ett**.

Kontrollera också att meddelandet "*Fixat merge konflikt*" finns med samt en *Merge:* ovanför *Author* i samma log. Exempelvis så här:

```shell
commit b1ffa2242b8fb6ef6e836bb7734e6b834e0b5c67 (HEAD -> master, origin/master)
Merge: e0c8100 4ce6237
Author: kr4ften <oliver.kr4ft@gmail.com>
Date:   Sat Sep 4 19:30:48 2021 +0200

    Fixat merge konflikt
```