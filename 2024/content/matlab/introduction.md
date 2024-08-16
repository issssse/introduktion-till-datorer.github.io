---
title: Introduktion
weight: 10
---

På denna sida hittar du en kort introduktion till MATLAB. 

{{% notice style="warning" title="Testa själv i MATLAB" %}}

Det är **starkt** rekommenderat att du startar MATLAB och själv testar de kommandon och exempel
som ges i texten samtidigt som du läser.

{{% /notice %}}


## Vad är MATLAB?

MATLAB kan kort sagt beskrivas som en avancerad grafräknare vilken kan programmeras att
göra det du vill. Till exempel är det väldigt lätt att rita upp
grafer och utföra beräkningar på stora ekvationssystem (större än
det är möjligt att lösa för hand). Ett kortare urval av enklare saker MATLAB
kan användas till är:

- Utföra beräkningar
- Läsa eller spara från/till en fil
- Skapa bilder, grafik och diagram
- Skapa grafiska användargränssnitt

MATLAB har dessutom mängder av användbara inbyggda kommandon och funktioner. Det finns även tilläggspaket, så kallade *toolboxes*, som utökar programmets funktionalitet. 

MATLAB finns installerat på PC-datorerna i datorsalarna på ITC och Ångström. Det går även att installera MATLAB på [egen dator](https://teknat.uu.se/student/stod-och-service/matlab/); nedladdnings- och installationstiden kan dock vara lång, så för denna modul i Introduktion i datorer rekommenderas datorerna i universitetets datorsalar, där MATLAB redan finns installerat.

Det är också möjligt att använda [MATLAB i webbläsaren](https://matlab.mathworks.com/) om man har ett konto hos Mathworks. En lokal installation kan dock vara att föredra i de flesta fall.

## Hur fungerar MATLAB?
Det grafiska gränssnittet för MATLAB har ett antal olika sektioner dedikerade till olika uppgifter. De viktigaste av dessa
är markerade i bilden nedan. Allmän information om hur MATLAB fungerar och vad de olika delarna av användargränssnittet gör följer i texten nedan.

{{< figure src="/images/matlab/program.png" title="Användargränssnittet i MATLAB." >}}

### Kommandofönstret
Kommandofönstret kan bland annat användas
för att direkt utföra beräkningar eller exekvera uttryck. Kommandon eller
uttryck som skrivs i kommandofönstret körs direkt när du trycker på returknappen ( `ENTER` ) på tangentbordet.

{{< figure src="/images/matlab/commandwindow.gif" title="Kommandon som exekveras i MATLAB:s kommandofönster." >}}

{{% notice style="warning" title="Spara ditt arbete!" %}}

Tänk på att de kommandon du skriver i kommandofönstret inte sparas. Skriv dina kommandon i ett skript (se nedan) om du vill kunna köra dem vid ett senare tillfälle!  

{{% /notice %}}

### Skript och datafiler
I ett så kallat *skript* kan man, kort sagt, köra många kommandon i följd och spara denna följd för senare bruk. Skript kan skapas genom att i övre vänstra hörnet trycka på `New Script` (det går också bra att trycka på `New` och sedan `Script` i rutan som dyker upp). 

MATLAB-skript har filändelsen `.m` och den kod du ska skriva i uppgiften till denna modul och många andra uppgifter under din utbildning ska lämnas in just som skript, då alla kommandon som behöver köras kan sparas i en och samma fil. Skriptet kan sedan skickas till en lärare eller studiekamrat som då kan köra din kod på sin dator. Koden i ett skript exekveras **uppifrån och ned**, alltså som om MATLAB läser och kör koden i skriptet rad för rad. 

Skript kan startas från bland annat kommandofönstret efter att de sparats och namngivits med knappen `Save`, som är synlig då ett skript har skapats och `EDITOR`-fliken längst upp är aktiv.

{{% notice style="info" title="Filtyper" %}}

Man kan även spara värden på variabler utan koden som generar dem i en fil, som då får filändelse `.mat`. Denna funktionalitet kommer vi inte använda i denna modul. Inga `.mat`-filer ska lämnas in!

{{% /notice %}}

### Filredigerare
Skript redigeras enklast i filredigeraren. Det finns även en uppsättning knappar som hör till filredigeraren; dessa nås genom att i menyraden klicka på fliken `EDITOR`, vilket gjorts i bilden nedan: 

{{< figure src="/images/matlab/editor.png" title="Den övre delen av MATLAB-fönstret, där knappar associerade med filredigeraren visas." >}}

Här finns en grön knapp kallad `Run` med vilken man kan köra det skript som är aktivt i filredigeraren. Det finns även verktyg för felsökning och formatering av kod här.

### Arbetsmapp

För att ditt skript ska kunna köras måste MATLAB hänvisas till den mapp där
skriptet finns. Denna mapp kallas *arbetsmappen* och behöver alltså ställas in.
Som synes i bilden ovan ligger skriptet `decorated_plot.m` i vår nuvarande
arbetsmapp och går därför att köra om man matar in `decorated_plot` i kommandofönstret.

Om du försöker köra ett skript som **inte** ligger i arbetsmappen kommer denna ruta att dyka upp:

{{< figure src="/images/matlab/felarbetsmapp.png" title="Fönstret som dyker upp då fel arbetsmapp är inställd." >}}

Trycker du på `Change Folder` kommer arbetsmappen automatiskt att bytas till den där skriptet du försöker köra ligger. Trycker du på `Add to Path` kommer ditt skript istället att läggas till i din nuvarande arbetsmapp.



#### Sökväg till arbetsmappen

Detta fält visar sökvägen till arbetsmappen. 

{{< figure src="/images/matlab/path.png" title="Sökvägen för arbetsmappen." >}}

Härifrån kan man
navigera till andra mappar, men också söka efter filer. För att
navigera i mappstrukturen, använder du de små pilarna bredvid mappnamnen, eller
klickar i den tomma ytan bredvid sökvägen för att manuellt skriva in en
sökväg.

För att söka efter filer, klickar du på knappen med förstoringsglaset längst
till höger.

Det finns även sökvägshistorik om du klickar på den lilla pilen till vänster
om förstoringsglaset. 

### Variabelfönstret

Tal, listor och annan data sparas i så kallade *variabler*. Att använda variabler istället för statiska värden gör att man i sin kod lätt kan ändra vilka värden
man räknar med. Variabelfönstret visar namnen på de variabler som finns tillgängliga samt deras innehåll. 

{{< figure src="/images/matlab/workspace.png" title="Variabelfönstret till höger med alla sparade variabler." >}}

Det är bra att titta i variabelfönstret om man inte vet vilka variabler man har skapat tidigare, eller för att ta reda på hur ett skript beter sig genom att se hur variablernas värden ändras då man kör sitt skript.

## Lathund i MATLAB

I denna sektion beskrivs grundläggande kommandon/funktioner i MATLAB. Testa
gärna dessa kommandon i kommandofönstret samtidigt som du läser!

{{% notice style="info" title="Skriv inte samma sak flera gånger i onödan!" %}}

Genom att trycka på uppåtpilen ( `↑` ) på tangentbordet återfås tidigare skrivna kommandon. Du behöver då inte skriva om ett kommando om du vill köra det flera gånger. 

{{% /notice %}}

### Kommentarer

Kommentarer i MATLAB-skript föregås av `%` och har grön färg i filredigeraren. Kommentarer är bra för att berätta vad
olika delar av kod betyder och/eller gör, dels för utomstående som läser din kod, men även för dig själv då du vid ett senare tillfälle försöker minnas hur din kod fungerar eller varför du gjorde på ett visst sätt.

``` matlab
% Detta är en kommentar i MATLAB
```

### Enkla tal

Enkla tal kan bestå av *heltal* eller *flyttal*. Såhär sparar du ett tal i en
variabel:

``` matlab
% Heltal
A = 42
% flyttal
B = 1.234
```
### Listor

En *lista* kan beskrivas som en uppsättning tal och är synonymt med *vektor* eller *array* (vilket ord som används beror på sammanhanget). För att spara tal i en lista kan man skriva på två olika sätt:

``` matlab
% Med kommatecken
C = [1, 2, 3, 4]
% Utan kommatecken
D = [1 2 3 4]
```


Det finns ett enkelt sätt att skapa listor utan att behöva skriva varje
tal för hand:

``` matlab
% Skapa en lista med talen [1, 2, 3, 4, 5]
E = 1:1:5
% Skapa en lista med talen [1, 3, 5, 7, 9]
F = 1:2:10
```

Denna typ av listor kan även kallas *radvektor*, då alla listans värden står på en rad.
I MATLAB kan man även skapa listor som kallas *kolumnvektor*, där alla värden
står i en kolumn. Detta används dock främst vid *matrisberäkningar*, och är lite
överkurs:

``` matlab
% Kolumnvektor, separera tal med ;
G = [1; 2; 3; 4]
```

### Dölja utskrift av variabler och uttryck

Som du kanske märkt (om du testat kommandona själv) skrivs resultatet ut varje
gång ett kommando eller uttryck körs. Detta går att "stänga av" genom att avsluta
uttrycket/kommandot med semikolon ( `;` ). Testa exempelvis följande:

``` matlab
% Med utskrift
A = 42
% Utan utskrift
B = 42;
```

{{% notice style="info" title="Skriv endast ut sådant som är viktigt!" %}}

Att dölja utskrifter kan vara en bra idé om man har många kommandon som ska köras i ett skript; alla variabeltilldelningar är inte relevanta att visa för användaren!

{{% /notice %}}

### Matematiska operationer och funktioner
För att kunna utföra beräkningar behövs matematiska operationer/funktioner. Ett urval av dessa återfinns nedan.

#### Operationer på enkla tal

``` matlab
% Vi börjar med att skapa en variabel a med värde 8
a = 8;

% Addition
b = a + 10  % blir 18
c = a + b   % blir 8 + 18 = 26

% Subtraktion
d = c - 8   % blir 18
e = d - a   % blir 18 - 8 = 10

% Multiplikation
f = a * 2   % blir 16
g = a * a   % blir 8 * 8 = 64

% Division
h = g / 2   % blir 32
i = h / a   % blir 32 / 8 = 4

% Exponenter
j = a ^ 2   % blir 64
k = a ^ a   % blir 8 ^ 8 = 16777216
```

De flesta operationer/funktioner har inte lika kort notation som de ovan. Exempel på
detta är kvadratroten, vilken anropas genom sitt funktionsnamn `sqrt`:

``` matlab
% Vi börjar med att skapa en variabel, a
a = 64;

b = sqrt(100) % blir 10
c = sqrt(a)   % blir 8
```

#### Operationer på listor

För att snabbt utföra många beräkningar kan man använda listor. Många av
exemplen från [enkla tal](#enkla-tal-1) ovan går att använda på samma sätt när det gäller listor,
men i vissa fall måste en punkt ( `.` ) skrivas ut före den matematiska
operanden (se Exponenter i exemplet nedan). Detta beror på att MATLAB arbetar
med så kallade *matrisberäkningar* och i vissa fall förväntar sig två matriser
och inte enkla tal. Punkten ser till att den önskade operationen utförs *elementvis*.

``` matlab
% Vi börjar med att skapa en lista a med värdena 1, 2 och 3
a = [1, 2, 3];

% Addition
b = a + 10  % blir [11, 12, 13]
c = a + b   % blir [1+11, 2+12, 3+13] = [12, 14, 16]

% Subtraktion
d = c - 8   % blir [4, 6, 8]
e = d - a   % blir [4-1, 6-2, 8-3] = [3, 4, 5]

% Multiplikation - Notera .* för g
f = a * 2   % blir [2, 4, 6]
g = a .* a   % blir [1*1, 2*2, 3*3] = [1, 4, 9]

% Division - Notera ./ för i
h = g / 2   % blir [0.5000, 2.0000, 4.5000]
i = a ./ a   % blir [1/1, 2/2, 3/3] = [1.000, 1.000, 1.0000]

% Exponenter - Notera .^ för både j och k
j = a .^ 2   % blir [1, 4, 9]
k = a .^ a   % blir [1^1, 2^2, 3^3]  = [1, 4, 27]

l = sqrt(j)   % blir [1, 2, 3]
```

### Egna funktioner

I framtida kurser, speciellt beräkningsvetenskap kommer ni bli ombedda att skriva och kalla på 
funktioner i MATLAB. En funktion kan kort beskrivas som en "maskin" som tar en given input och 
omvandlar detta till en output, med hjälp av matematiska formler och parametervärden. 

Funktioner deklareras på följande sätt:

``` matlab

%% Beräkna en cirkels omkrets:


function Omkrets = Cirkel(r)

Omkrets = pi*2*r

disp(Omkrets)

end

```

### Hjälp med funktioner/kommandon

Det är inte alltid så lätt att komma ihåg hur alla funktioner ska skrivas in. Som tur är
finns ett hjälpsystem i MATLAB för just sådana tillfällen! För att ta reda på
hur en funktion ska skrivas och fungerar kan du använda
`help`-kommandot. Skriv helt enkelt `help <funktionsnamn>` i kommandofönstret.
Exempelvis för funktionen `sqrt`:

``` matlab
help sqrt
```

vilket ger utskriften:

{{< figure src="/images/matlab/help_sqrt.png" class="small" >}}

Det går även att lägga till hjälptext till dina egna funktioner, vilket är en väldigt bra idé. Särskilt om 
någon annan ska använda dina funktioner eller du arbetar med ett stort projekt. Hjälptexten för dina egna funktioner
placeras direkt efter deklarationen, så här:

``` matlab
function Omkrets = Cirkel(r)
% Cirkel - beräknar omkretsen för en cirkel med radie r
%   Exempel: Cirkel(20) - ger omkretsen på en cirkel med radien 20 cm

Omkrets = pi*2*r

disp(Omkrets)

end

```

### Grafer

MATLAB gör det väldigt enkelt att snabbt rita upp en graf över en uppsättning
tal. För att rita upp en enkel graf i MATLAB används den inbyggda funktionen
`plot`:

``` matlab
plot(x,y)
```
Där `x` samt `y` är listor med värden för \\(x\\)- respektive \\(y\\)-axeln.

Exemplet nedan ritar upp en
förenklad graf över funktionen \\(y = x^2\\), där vi redan räknat ut en lista `y` för givna
`x`:

``` matlab
% Position på x-axeln
x = [1 2 3 4 5]
% Värden på y-axeln
y = [1 4 9 16 25]

% Rita ut graf för x/y-värden
plot(x,y)
```
Detta resulterar i följande graf:

{{< figure src="/images/matlab/x2plot.png" title="Förenklad graf för y=x^2." >}}

Det går även att ändra hur grafen ska se ut, lägga till titel och namn på axlar:

``` matlab
x = [1 2 3 4 5]
y = [1 4 9 16 25]

% Rita samma graf, men med röd linje
plot(x,y,'r')

% Sätt titel på grafen
title('Graf över x^2')

% Sätt namn på x- och y-axel
xlabel('x-axel')
ylabel('y-axel')
```

{{< figure src="/images/matlab/x2plot_decorated.png" title="Dekorerad graf för y=x^2." >}}

#### Flera linjer i grafen

Det går även ha flera grafer i samma fönster. För att göra detta
använder vi `hold`-kommandot. Vi skapar två grafer, en linjär och
den kvadratiska från ovan:


``` matlab
x = [1 2 3 4 5]
y1 = [1 2 3 4 5]
y2 = [1 4 9 16 25]

% Sätt hold till ON för att spara
% alla grafer vi ritar ut
hold on

% Rita  grafen för y1 (linjär)
plot(x,y1)

% Rita grafen för y2 (kvadratisk)
plot(x,y2)

% Sätt titel på grafen
title('Två linjer i en graf')

% Sätt namn på x- och y-axel
xlabel('x-axel')
ylabel('y-axel')

% Stäng av hold när vi är klara
hold off
```

{{< figure src="/images/matlab/dual_line_plot.png" title="Graf för två funktioner." >}}

#### Flera grafer i ett rutnät

Utöver att ha flera linjer i samma graf går det att placera flera grafer bredvid varandra i ett rutnät. För detta
använder vi kommandot `subplot` . Detta kommando behöver veta hur många rader och
kolumner du vill ha i rutnätet som kommer skapas. Du behöver också för varje graf ange vilken position i rutnätet du vill att grafen i fråga ska ha. Denna position fungerar ungefär som ett index, den första positionen i rutnätet är alltså 1, den andra 2 och så vidare.

Kommandot används alltså genom att ange: `subplot(antal_rader, antal_kolumner, position)` (för varje graf du vill ha med). Ett exempel följer nedan:


``` matlab
x = [1 2 3 4 5]
y1 = [1 2 3 4 5]
y2 = [1 4 9 16 25]

% En rad, två kolumner. Nästa graf på första platsen:
subplot(1,2,1)
plot(x,y1, 'g') % Rita grafen på plats 1 och gör linjen grön
title('Första grafen') % Titel på första grafen

% En rad, två kolumner. Nästa graf på andra platsen:
subplot(1,2,2)
plot(x,y2, 'r') % Rita grafen på plats 2 och gör linjen röd
title('Andra grafen') % Titel på andra grafen

% Sätt namn på x- och y-axel för andra grafen
xlabel('x-axel')
ylabel('y-axel')
```

{{< figure src="/images/matlab/subplot.png" title="Flera grafer med olika konfiguration." >}}

### Skriva ut text i kommandofönstret

För att skriva ut text i kommandofönstret används funktionen `disp`. Notera att text
som ska skrivas ut måste omslutas av `'`-tecken:

``` matlab
disp('Hallå från kommandofönstret!') % Skriver ut texten till kommandofönstret
```

### Rensa gamla variabler/historik

Ibland kan man behöva rensa gamla variabler från minnet. Detta kan du göra via kommandot
`clear`. För att rensa all historik skriver du:
``` matlab
clear all
```

För att rensa enskilda/specifika variabler skriver du variabelnamnet istället för `all`.
Du kan även rensa flera variabler på samma gång:
``` matlab
% Vi skapar några variabler först
a = 1
b = 2
c = 3

% Sedan rensar vi a och c från minnet, men sparar b
clear a c
```

För att rensa kommandofönstrets historik skriver du:
``` matlab
clc
```



## Spara skript

Eftersom det är jobbigt att behöva skriva alla kommandon varje gång är det bra att kunna
spara dem i en fil som ett MATLAB-skript. Det är även bra om man har kod som fungerar
bra och man vill spara för framtiden.

Kom ihåg att koden i ett skript exekveras **uppifrån och ned**, alltså som om MATLAB läser koden i skriptet rad för rad. 

Börja med att skapa en ny fil genom att klicka på `New Script` längst till vänster i
menyraden. Detta öppnar en tom fil i tilredigeraren. Kopiera sedan koden nedan och
klistra in i filen:

``` matlab
x = 2016;
y = 1953; %  Ändra till året du föddes

disp('Hej, jag heter Tintin!') % Ändra Tintin till dit namn
disp('Min ålder är: ')
disp(x-y)
```

Justera enligt kommentarer. Tryck därefter på diskett-ikonen ( `Save` ) i menyraden och spara
filen som `test.m` i din arbetsmapp (den är förvald som destination). Filen kommer nu
synas i arbetsmapp-fönstret i MATLAB.

Skriv nu namnet på filen ( `test` ) i kommandofönstret för att köra ditt skript!

{{< figure src="/images/matlab/savefile.gif" title="Spara en skriptfil i MATLAB." >}}

## Gör uppgifterna!
Du har nu gått igenom det material som krävs för att göra [uppgifterna](../assignment) som ska lämnas in!

Om du är intresserad och vill lära dig mer om vad som kan göras i MATLAB finns här nedan mer avancerade exempel ([överkurs](../extra)) som du kan gå igenom om du är klar med alla andra uppgifter och känner att du har tid. Dessa saker (och mycket mer) kommer gås igenom i kommande kurser. 

{{% notice style="info" title="Fråga dina handledare!" %}}

Fråga gärna dina handledare vad de har använt MATLAB till under deras studietid och om de har några tips att dela med sig av!

{{% /notice %}}

