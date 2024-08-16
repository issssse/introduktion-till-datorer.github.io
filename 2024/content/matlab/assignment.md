---
title: Uppgifter
weight: 20
assignment: mandatory
---

## Mål

Efter att du blivit godkänd på denna uppgift kommer du att känna till hur du:

- sparar ett MATLAB-skript till en fil och kör det
- genererar listor av tal
- implementerar enkla ekvationer och använder enkla matematiska operationer
- använder enkla funktioner för att skapa nya värdelistor
- visar resultat i form av grafer på ett överskådligt sätt.

## Detta behöver du

För att genomföra uppgiften behöver du tillgång till följande.

Matlab
: MATLAB finns på PC-datorerna i salarna på ITC/Ångström (alternativt på egen dator)

Aktiverat Studentkonto
: För att kunna lämna in i Studium eller Canvas (ES) behöver du ett aktiverat Studentkonto.

## Förberedelser

De koncept som tas upp i uppgiften diskuteras på [introduktionssidan för MATLAB](../introduction/).

## Uppgift

Under utbildningens gång kommer du ofta använda Matlab för att lösa
beräkningsuppgifter. I denna uppgift kommer du att få prova på att göra några
enkla beräkningar i MATLAB, men framförallt att presentera dina resultat i form
av flera grafer på ett snyggt sätt.

### Del 1: Skapa ett nytt Matlab-skript
Börja med att skapa ett nytt MATLAB-skript. Klistra sedan in följande kod i ditt skript:

``` matlab
disp('Jag fungerar!')
```

Spara sedan skriptet till skrivbordet (eller någon annan plats på datorn) och se till att filen får namnet `abcd1234_matlab.m`,
där du ersätter `abcd1234` med användarnamnet för ditt studentkonto.

Testkör nu ditt skript. Om programmet skriver ut `Jag fungerar!` i kommandofönstret kan du gå vidare
till nästa del. Får du inte utskriften, kontrollera att:

- du vet hur ett skript [körs](../introduction/#filredigerare) 
- du har valt rätt arbetsmapp i [sökfältet](../introduction/#sökfältet-sökväg-till-arbetsmappen)
- programmet du sparat syns i [arbetsmapp-fönstret](../introduction/#arbetsmapp)
- programfilen inte är tom.

### Del 2: Generera en lista med tal
För denna uppgift behöver vi en lista med tal vi kan utgå från. Då det är jobbigt att skriva alla dessa för hand används lämpligen "snabbversionen" för att skapa en lista av många tal:

För vår uppgift vill vi ha en lista `x1` som innehåller gradtal mellan 0 och 360, med intervall om 20 grader. Den färdiga listan ska alltså innehålla talen 0, 20, 40, 60, ..., 340, 360.

{{% notice style="info" title="Kom ihåg!" %}}

Om du har glömt hur man gör en lista på ett snabbt sätt kan du läsa avsnittet [Listor](../introduction/#listor) på introduktionssidan.

{{% /notice %}}


### Del 3: Matematiska operationer på listor
För att vi ska kunna använda dessa tal på det sätt vi vill måste vi omvandla våra gradtal i listan `x1` till radianer och spara resultatet i en ny lista som vi väljer att kalla `x2`. Detta gör vi via denna formel:

$$x_2 = \frac{x_1}{360} \cdot 2 \cdot \pi$$

Implementera denna formel i ditt skript. 

{{% notice style="info" title="Kom ihåg!" %}}

Variabeln \\(\pi\\) finns inbyggd i MATLAB och heter `pi`.

{{% /notice %}}

Om du skrivit rätt kommer talen i den nya listan se ut så här om du skriver ut dess innehåll i kommandofönstret:  
`x2 = [0, 0.3491, 0.6981, ..., 5.9341, 6.2832]`

### Del 4: Använda enklare funktioner
Vi ska nu använda vår lista `x2` i tre olika sinusfunktioner. Detta kommer skapa tre nya listor, vilka vi senare kan plotta. För att skapa sinusfunktioner använder du funktionen `sin` som finns inbyggd i Matlab. Om du är osäker på hur den fungerar kan du skriva `help sin` i kommandofönstret.

Gör tre nya listor `y1`, `y2` och `y3`, där respektive lista är definierad som
$$y_1 = \sin(x_2)$$
$$y_2 = \sin(2 \cdot x_2)$$
$$y_3 = \sin(3 \cdot x_2)$$



### Del 5: Visa resultatet i form av grafer
Våra listor `y1`, `y2` och `y3` (som alla är funktioner av `x2`) ska nu representeras som tre grafer. 

{{% notice style="info" title="Kom ihåg!" %}}

Information om hur detta fungerar
hittar du under sektionen [Grafer](../introduction/#grafer) på introduktionssidan.

{{% /notice %}}

 Om vi ritar upp graferna med kommandot

``` matlab
plot(x2,y1 , x2,y2 , x2,y3)
```
så får vi denna graf:

{{< figure width="800" src="/images/matlab/uppgift-plot.png" class="medium" title="En inte så överskådlig graf med alla tre listor." >}}

Men detta är inte särskilt snyggt!

**Din sista uppgift är därför att se till att grafen som ditt skript skapar istället får detta utseende:**

{{< figure width="800" src="/images/matlab/uppgift-plot-final.png" class="medium" title="Den önskade grafen, där man lätt kan urskilja de tre listornas grafer." label="finalgraph" >}}

### Slutgiltigt skript

När du är klar med skriptet ska det kunna köras. För att du ska bli godkänd ska skriptet utföra följande när det körs: 

+ Din utskrift ( `Jag fungerar!` ) ska skrivas ut i kommandofönstret  
+ Den färdiga, tredelade grafen ska visas och se ut som på den sista bilden.


## Fördjupningsuppgifter:

### Del 1: Mjukstart - Matriser och ekvationssystem

Antag att en 3x3 matris A, där A = 
[1 4 6; 9 2 4; 15 7 8] och en 1x3 matris B, där B = [6 9 4]. Bestäm värderna på konstanterna i matris x (x1, x2 och x3) om Ax = B. Finns det några heltal för x1, x2 och x3 som uppfyller ovanstående kriterium?

### Del 2: Iterationer och serier

Antag att du har en talserie (X) med 25 stycken tal, där de första 2 talen x1 = 2.4 och x2 = 0.96.

Talen följer följande serie:

$$y_3 = 3_x_2 - 4_x_1$$
$$y_4 = 3_x_3 - 4_x_2$$
$$y_n = 3_x_n-1 - 4_x_n-2$$

a) Beräkna m.h.a kontrollsatser vilket värde tal nr 20 har.

b) Vilka av talen är mindre än 5? Gör detta m.h.a kontrollsatser och skriv dessa tal i en lista. 

### Del 3: Fallskärm och integraler

En 100 kg fallskärmsdykare hoppar med en initialhastighet v, med en decceleration på g m/s^2. 

Sträckan som fallskärmhopparen färdas, kan beskrivas med följande formel:

$$s(t) = gm(1-e^{-ct/m})/c$$ , där 

g = 9.82 m/s^2
m är massan
c = 8 (konstant)

a) Beräkna hur långt fallskärmshopparen har färdats mellan 15 och 20 sekunder.

b) Efter hur lång tid är fallskärmshopparen nere på marken, om man antar att flygsträckan är 2500 m? 

## Inlämning

Du skall nu lämna in filen `abcd1234_matlab.m` där du ersatt `abcd1234` med
användarnamnet på ditt Studentkonto.

- Kontrollera att filen faktiskt har ändelsen `.m` . Filer med ändelsen `.mat`
eller något annat kommer ej att godtas och resultera i en komplettering.
- Ladda upp filen på anvisad plats i Studium (UU) eller Canvas (ES/SLU).


