---
title: Logga in
weight: 10
---

Här hittar du information om hur du loggar in på Universitetets Linux-system
från någon av datorsalarna för studenter på campus Ångströmlaboratoriet


## Windows i alla salar

I alla datorsalar för studenter på campus Ångströmlaboratiet finns det datorer
med Windows. 

{{< figure 
    width="555px" 
    src="/images/2025/windows/student-pc.jpg" 
    title="Arbetsplats med dator som kör Windows." 
>}}

## Linux med ThinLinc

På campus Ångströmlaboratoriet finns ett antal stora datorer ([servrar][server]) som kör
Linux någonstans i en källare. Som student kommer du inte i fysik kontakt med
dessa servrar. Istället loggar du in mot dessa servrar från Windows och får upp
skrivbordsmiljön för Linux på samma skärm som Windows. Systemet som används
för detta heter [ThinLinc][thinlinc]. 

[server]: https://sv.wikipedia.org/wiki/Server

[thinlinc]: https://en.wikipedia.org/wiki/ThinLinc

- För att komma åt Linux-systemet måste du först logga in i Windows och från
Windows använda ThinLinc Client för att logga in mot en Linux-server.

## Logga in i Windows

För att logga in i Windows anger du användarnamnet för ditt **studentkonto** på
formen `abcd1234` och **Lösenord A**.

![](/images/2025/windows/login.jpg?width=444px)

## Skrivbordet (Windows)

När du loggat in i Windows ser du **Skrivbordet**. 

![](/images/2025/windows/desktop.png)


## Aktivitetsfältet (taskbar)

Längst ner på skrivbordet hittar du **Aktivitetsfältet (taskbar)**. 

![](/images/2025/windows/taskbar.png)

## Starta ThinLinc

I **Aktivitetsfältet** hittar du en sökruta. Skriv in **ThinLinc** i sökrutan (1). 

![](/images/2025/linux/start-thinlinc.png?width=500px)

Bland sökresultaten skall du nu hitta **ThinLinc Client** (2). När du klickar på **ThinLinc Client** (2) dyker ett fönster upp där du kan logga in i Linux-systemet. 

- I fältet **Server** skall det stå `thinlinc.student.it.uu.se`.
- I fältet **Username** skriver du användarnamnet för ditt **studentkonto** på
formen `abcd1234`.
- I fältet **Password** skriver du ditt **Lösenord A**.


![](/images/2024/linux/thinlinc-login.png?width=500px)

Klicka på **Connect** för att logga in. Första gången du gör det kan du mötas av
följande meddelande. 

![](/images/2024/linux/trust-this-host.png?width=500px)

Om du ser meddelandet ovan, klicka på **Continue**. 

## Skrivbordet (Linux)

Om du lyckas logga in öppnas ett nytt fönster med skrivbordsmiljön för Linux.
Detta fönster kan du maximera eller ändra storlek på, precis som för vilket
annat fönster som helst i Windows. I fönstret i Windows ser du alltså
skrivbordet för Linux som i själva verket körs på en server någon annanstans.

![](/images/2024/linux/linux-desktop.png)


