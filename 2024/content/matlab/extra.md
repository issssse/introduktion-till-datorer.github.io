---
title: Överkurs
weight: 30
---

Denna del är helt frivillig men tar upp några koncept som du kommer stöta på
senare under din utbildning. Om du redan nu är intresserad av att lära dig mer
om MATLAB kan detta vara något för dig. 

## Kontrollsatser

Generellt sätt finns det två former av kontrollsatser i de flesta imperativa programmeringspråk (Java, Python m.fl) - loopar (används vid upprepningar) samt statements (sortering). I MATLAB förekommer for och while - loopar samt if, elif och else - statements. Observera att do - while loopar ej används samt else if , även om elif är samma sak som else-if.

Liksom andra programmeringspråk förekommer även s.k "nested-loops", vilket innebär att man har flera loopar efter varandra som gör flera separata  beräkningar. Ett exempel kan vara att man har en given lista, där alla jämna tal ska skrivas ut samt deras placering i listan.
Här nedan följer ett par exempel (med kod) på vilka situationer ni kommer att bemöta i framtida matlab-kurser.


### Exempel 1 - Utskrift av alla tal mellan 1 och 10 (for-loop)

I detta exempel ska vi beräkna hur man kan m.h.a en for-loop skriva ut alla heltal mellan 1 och 10.

Nyckeln till att lösa uppgiften är att dels veta vilket tal som har vilken index-värde (position)
samt att man inkrementerar det föregångna talet för att få fram nästa tal.

```matlab

%% Skriva ut alla tal mellan 1 och 10:

for i= 0:9 % i är våra index (börjar med 0)
    a = i + 1; % a är våra tal (1-10)
    disp(a)   
end

```

### Exempel 2 - Jämföra flera tal med varandra (statements)

``` matlab

%% Variabeldeklaration
a = 3
b = 9
c = 10
d = 2

ab = a*b
cd = c*d


%% Statements och jämförelse
if ab > cd
    disp("ab is greater")
    
else
    disp("cd is greater")
end

```

### Exempel 3 - Utskrift av alla jämna tal från en given lista (for-loop samt statements)

``` matlab

%% Skriva ut alla jämna tal från en lista:

lista = [1 9 3 15 17 7 10 18 22 48] %vår lista

for i= 1:length(lista) % i är våra index (börjar med 0)
      
    if mod(lista(i),2) == 0 % villkor för jämna tal
        
        disp("talen är:" + lista(i)) %Utskrift
        
    else
        i = i + 1 %loopa vidare till nästa tal
        
    end
end

```


## Symbolhantering
MATLAB kan även hantera så kallad *symbolisk* matematik. Det vill säga matematiska
uttryck och ekvationer som innehåller symboler och ej resulterar i en
numerisk lösning. Via symbolhanteringen i MATLAB kan man exempelvis
beräkna derivatan av en funktion som en formel.

### Exempel: Derivera en enkel funktion
Låt oss ta en enkel ekvation, \\(F(x) = 5x^2 - 2x\\), och utnyttja symbolhantering i MATLAB för att hitta dess derivata:

``` matlab
% Först säger vi att vi vill använda
% x för symbolisk matematik
syms x

% Sedan sparar vi funktionen vi vill
% derivera i en variabel, F
F = 5*(x^2) - 2*x;

% Därefter använder vi symbolhantering
% för att derivera funktionen:

diff(F,x) % Derivatan av funktionen F med avseende på x

```

{{< figure src="/images/matlab/symbolics.gif" title="Symbolisk derivata i MATLAB." >}}

{{% notice style="info" title="Tillägspaket krävs" %}}

För att utnyttja symbolhanteringen i MATLAB behövs tilläggspaketet
*Symbolic Math Toolbox*. Mer information om detta samt tillhörande exempelfiler hittar du [här](http://se.mathworks.com/help/symbolic/index.html).

{{% /notice %}}

## Matriser & matrisekvationer

Matriser och matrisoperationer är något de flesta av er aldrig stött på tidigare och inget
vi kommer fokusera på i denna modul. Att arbeta med matriser i MATLAB är dock väldigt smidigt och är något du garanterat kommer att göra i framtida kurser. Här kommer därför ett litet smakprov av matriser och några tillämpningar i MATLAB:

### Exempel 1: Symboliska uttryck

Uttrycket

$$2x\_1+3x\_2-4x\_3,$$

där \\(x_1\\), \\(x_2\\) och \\(x_3\\) är okända variabler, kan skrivas på matrisform som

$$\begin{bmatrix}2 & 3 & -4 \end{bmatrix} \begin{bmatrix}x\_1 \\\ x\_2 \\\ x\_3 \end{bmatrix}.$$

Detta kan implementeras i MATLAB på följande vis:

```matlab
% Definiera koefficientmatrisen
A = [2, 3, -4];

% Definiera x1, x2 och x3 som symboler
syms x1 x2 x3

% Vår x-vektor
x = [x1; x2; x3];

% Visa det symboliska uttrycket i kommandofönstret
A*x
```
På detta sätt kan koefficienterna i matrisen `A` lätt ändras. Variablerna \\(x_1\\), \\(x_2\\) och \\(x_3\\) kan från kommandofönstret tilldelas värden och värdet för hela uttrycket kan då evalueras:

```matlab
% Evaluera ett symboliskt uttryck
subs(A*x)
```
det symboliska uttrycket `A*x` kan även deriveras; exempelvis kommer `diff(A*x,x1)` derivera uttrycket med avseende på \\(x_1\\).


### Exempel 2: Lösning av linjära ekvationssystem
Med matriser kan vi beskriva både vänsterled och högerled för hela ekvationssystem.

Det linjära ekvationssystemet

$$2x\_1+3x\_2 = 10$$
$$4x\_1+5x\_2 = 12$$

kan skrivas på matrisform som

$$\begin{bmatrix}2 & 3 \\\ 4 & 5 \end{bmatrix} \begin{bmatrix}x\_1 \\\ x\_2 \end{bmatrix} = \begin{bmatrix}10 \\\ 12 \end{bmatrix}.$$

Med hjälp av operatorn `\` (*backslash*, inte snedstreck som ger division) kan ekvationssystem likt det ovan lösas. Detta är som sagt *överkurs* och teorin bakom kommer att gås igenom **grundligt i kommande kurser**, men om du vill veta mer om hur MATLAB beräknar lösningen kan du kolla upp `\` i MATLAB-dokumentationen.

Lösning av ekvationssystemet

``` matlab
% Definiera vår koefficientmatris
A = [2, 3;
     4, 5];

% Definiera högerledet som en matris 
B = [10; 12]; 

% Ekvationssystem på denna form (A*x = B) kan lösas genom
x = A\B
```

Vilket ger utskriften:

``` matlab
x =

    -7
     8
```

Alltså är \\(x_1 = -7\\) och \\(x_2 = 8\\) lösningen på ekvationssystemet.

Allt detta går så klart att applicera på betydligt större ekvationssystem som annars hade tagit orimligt lång tid (eller varit omöjliga) att beräkna för hand!

Om du vill lära dig mer om matriser kan du besöka http://sv.wikipedia.org/wiki/Matris.



## Integraler och integralberäkning

I många fall kommer ni att stöta på problem som har med tillämpningar att göra, och integraler är inget undantag.
För att ni ska beräkna generella integraler på MATLAB, behövs egentligen 2 saker: En given funktion (med variabelvärden) samt den inbyggda funktionen `integral`.


### Exempel 1: Beräkna arean under en kurva

I detta exempel har vi en kurva som har funktionen f(x) = ax^5 + bx^2 + 4. Ett antagande görs, där konstanterna a och b har värdena 3 resp 5.
Frågan som ska besvaras är hur stor arean under kurvan kommer att bli mellan x = 4 och x = 6.

Det fiffiga med integralberäkning på MATLAB är att man inte behöver manuellt hitta den primitiva funktionen till den givna funktionen utan, den inbyggda funktionen
`integral` gör jobbet åt en.

Arean under kurvan beräknas på följande sätt:


 ``` matlab
 
a = 3
b = 5
x1 = 4
x2 = 6

function = @(x) ax^5 + bx^2 + 4

inteG = integral(function,x1,x2)
disp("Integralvärde:" , inteG)

```

I detta fall evalueras integralen mellan  `x1 = 4` och `x2 = 6`, som i sin tur är beroende av givna x-värden. Därför
lägger man till `@(x)` framför sin funktion. Den inbyggda funtionen `integral()` måste minst innehålla 3 st parametrar, där den
första parametern är funktionen och de två sista är integrationsgränserna.

### Exempel 2: Beräkna en rakets höjd m.h.a en egen funktion

I detta exempel får du lära dig om hur man gör en integralberäkning, då man skriver en egen funktion och tillämpar den på ett problem.
Det viktiga med denna uppgift är koddispositionen d.v.s var den deklarerade funktionen och integralfunktionen ska vara.

``` matlab
%% Integralberakning
t1 = 0;
t2 = 100;
q = integral(@Raket,t1,t2)
disp(" Strackan:" + q)

%% Funktion med parametervarden (deklarerad)
function Stracka = Raket(t, a,b)
a = 4;
b = 3;

strackan = 2*sqrt(b.^2 - (b.^2*t.^2/a.^2))

end

```

Här måste man vara observant på att integralfunktionen ALLTID hamnar ovanför den deklarerade funktionen.
Den givna matematiska uttrycket deklareras inuti den egna funktionen inklusive alla konstanter. En annan
viktig sak som måste poängteras är att integralen integreras med avseende på den givna funktionen och INTE en
enskild variabel.


## Kort om Numeriska metoder

Förutom praktisk programmering och torrexekvering kommer ni att bemöta teorin bakom viktiga numeriska metoder för att lösa diverse problem. De numeriska metoder som är viktiga att lära sig i den kommande kursen Beräkningsvetenskap 1 är:

- Newton-raphsons metod (eller Newtons metod)
- Minsta kvadratmetoden
- Trapetsmetoden
- Simpsons metod
- Richardson-extrapolationmetoden
- Bisektionsmetoden


