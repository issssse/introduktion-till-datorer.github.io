---
title: Python som miniräknare
weight: 30
---

Du skall nu får lära dig mer om Python REPL genom att använda det som en
miniräknare.

## Starta VS Code

Starta VS Code. 

![](/images/python/vscode/vscode-start.png?width=600px)


## Öppna ett Python REPL

Använd `Ctrl+Shift+P` (Windows och Linux) eller `Cmd+Shift+P`
(macOS) för att öppna kommandopaletten. Skriv `Start REPL` i sökrutan och välj
`Python: Start REPL`.

![](/images/python/vscode/start-repl.png?width=600px)

I den nedre halvan av VS Code öppnas nu en terminal, med ett Python REPL.

![](/images/python/vscode/python-repl.png?width=600px)

## Addition

Skriv in följande vid prompten `>>>` och tryck enter. 

``` text
>>> 1 + 1
```

Svaret på denna beräknings skriv nu ut på en egen rad följt av en ny prompt
`>>>`.

```text 
>>> 1 + 1
2
>>>
```

Notera att du kan använda godtyckligt många mellanslag runt plustecknet. Alla
dessa varianter är likvärdiga.

```text
1+1
1 +1
1+ 1
1    +1
1+    1
1  +  1
```

Men, du kan inte börja med ett eller flera mellanslag. 

```text 
>>>  1 + 1
  File "<stdin>", line 1
    1+1
IndentationError: unexpected indent
>>>
```

Om du böjar med ett eller flera mellanslag klagar Python och ger felmeddelandet `IndentationError: unexpected indent`.

## Testa fler räknesätt

Nedan ser du exempel på addition, multiplikation och division. 
``` text
>>> 1 + 3
4
>>> 3*7
21
>>> 1 / 3
0.3333333333333333
>>> 1 + 2*1/3
1.6666666666666665
>>> 
```

Parenteser kan användas för att gruppera. 

```text
>>> 10 - 5 / 2
7.5
>>> (10 - 5) / 2
2.5
>>>
```

## Variabler

Värdet av en beräkning kan lagras i en variabel. I exemplet nedan lagras värdet
`5` i variabeln `a` och värdet `2` i variabeln `b`. Variablerna `a` och `b` kan
sedan användas i nya beräkningar. 


``` text
>>> a = 5
>>> b = 2
>>> (a + b) / 2
3.5
>>>
``` 

## Testa på egen hand

Testa att utföra olika beräkningar med hjälp av `+`, `-`, `*` och `/` på egen
hand. Testa även att använda dig av parenteser `(` och `)` för att gruppera. 

## Klurighet

I Python är symbolerna `+`, `-`, `*` och `/` exempel på binära aritmetiska
operatorer. Kan du lista ut vad den binära aritmetiska operatorn `%` beräknar
för något?

Låt oss testa några exempel.

``` text
>>> 1 % 3
1
>>> 2 % 3
2
>>> 3 % 3
0
>>> 4 % 3
1
>>> 5 % 3
2
>>> 6 % 3
0
>>> 7 % 3
1
>>> 
```

Några exempel till. 

``` text
>>> 1 % 2
1
>>> 2 % 2
0
>>> 3 % 2
1
>>> 4 % 2
0
>>> 
```

Vad beräknas med hjälp av operatorn `%`? 
