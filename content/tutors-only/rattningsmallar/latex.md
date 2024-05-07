---
title: LaTeX
weight: 40
---

LaTeX-uppgiften går ut på att skapa ett enklare dokument med de element som
visas i referensdokumentet.


### För att eleven ska bli godkänd krävs:

1. Filnamnet ska innehålla studentkontots användarnamn
2. Ordningen för sidans innehåll spelar ingen större roll
3. Sidan ska se ut ungefär som [referensdokumentet](#referensdokument)
4. Titel:
    + Titeln ska vara studentkontots användarnamn
    + Författare ska vara studentens *faktiska* namn
    + Om studenten bytt plats på studentkonto och namn är det OK
5. "Innehåll" *ska* stå på svenska
    + Detta visar att `usepackage` har använts
6. Innehållsförteckningen ska innehålla fyra rubriker. Dessa måste inte vara exakt namngivna (eller i samma ordning) som i dokumentet.
7. En *numrerad* lista (vad punkterna heter spelar mindre roll)
8. En ekvation (volymen av ett klot)
9. En bild med
    + figurtext. Detta visar att `\label` har använts.
    + bildhänvisning i texten. Detta visar att `\ref`har använts (den måste inte vara klickbar).
10. En enkel textrad/ett citat (vad som står spelar ingen roll). En referens (d.v.s. |1| ) **ska** vara med
     + Citationstecken. Dubbla citationstecken ska användas och de ska skapas enligt instruktionerna med ''(två stycken ' ). Skulle någon göra engelska varianten och använda vänster- för att börja ett citat och högercitationstecken för att avsluta så är detta OK. 
     + Detta visar att `\cite` har använts
12. En referenslista innehållande författare, titel och årtal (påhittade artiklar är tillåtna)


### Referensdokument

{{< figure src="/images/latex/latex-final-uppg.png" title="Referensbild för dokumentet" class="border" >}}
