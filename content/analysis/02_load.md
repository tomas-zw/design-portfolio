---
Title: Load
Description: Utvärdera laddningstid och användbarhet (kmom05)
Template: index 
---

Webbplatsers laddningstid och användbarhet.
=======================

Laddningstid och användbarhet på tre webbsidor dokumenteras och analyseras.

Urval
-----------------------

Att komma på vad man ska laga till middag är inte lätt så jag har valt tre 
webbplatser med recept och mat-inspiration.  
Jag valde dom tre översta resultaten vid en google sökning på "recept".

[koket.se](https://www.koket.se/)  
[mathem.se](https://www.mathem.se/recept)  
[arla.se](https://www.arla.se/recept/)

Metod
-----------------------

Google Pagespeed används för att mäta sidorna både på både Mobile och Desktop.  
Webbläsarens dev-tools används för att mäta laddningstid, sidans totala storlek 
och antalet resurser som laddas in.  
För varje sida görs tre mätningar med dev-tools och medelvärdet används.

Resultat
-----------------------
### [koket.se](https://www.koket.se/)  
<picture class="load-img">
        <source media="(min-width: 701px)" srcset="%base_url%/image/koket-se.png?w=1020">
        <source media="(min-width: 368px)" srcset="%base_url%/image/koket-se.png?w=700">
        <img src="%base_url%/image/koket-se.png?w=367" alt="koket.se">
    </picture>

Det första man möts av är en väldigt stor reklambanner och då gör att i alla fall jag vill lämna sidan så fort som jag bara kan.  

Hastigheten på desktop sidan fungerar överlag bra, en liten förbättring det är att ta bort resurser som blockerar renderingen.  
På mobilsidan är det väldigt mycket långsammare och det är en stor förbättring att reducera javaskript som inte används och att även ta bort resurser som blockerar renderingen.
***

### [mathem.se](https://www.mathem.se/recept)  
<picture class="load-img">
        <source media="(min-width: 701px)" srcset="%base_url%/image/mathem-se.png?w=1020">
        <source media="(min-width: 368px)" srcset="%base_url%/image/mathem-se.png?w=700">
        <img src="%base_url%/image/mathem-se.png?w=367" alt="mathem.se">
    </picture>

Tog lite längre tid att ladda in men å andra sidan så möts man av det är man är där för, recept och mat förslag inte bara massa reklam. 

Hastigheten på desktop hade drastiskt kunnat reduceras med hjälp av att använda bilder med rätt storlek och att skickar bilderna i ett modernare bildformat till dem webbläsarna som stöder det.  
På mobilsidan hade samma förbättringar och att även reducera javaskript som inte används reducerat laddningstiderna avsevärt.
***


### [arla.se](https://www.arla.se/recept/)  
<picture class="load-img">
        <source media="(min-width: 701px)" srcset="%base_url%/image/arla-se.png?w=1020">
        <source media="(min-width: 368px)" srcset="%base_url%/image/arla-se.png?w=700">
        <img src="%base_url%/image/arla-se.png?w=367" alt="arla.se">
    </picture>

Denna sidan var helt klart långsammast med att ladda in . Men när den börjar laddats in så är det ingen reklam och man ser recepten direkt.  

Det första man möts av i några sekunder är en helt vit skärm. så en stor förbättring är att minska serverns första svarstid sen finns det jättemycket förbättringar att göra med bilderna som visas på sidan. Bland annat skicka bilderna ett modernare bildformat, skjuta upp inläsningen av bilder som inte visas på skärmen och även att använda bilder med rätt storlek.  
På mobilsidan förstår jag inte riktigt vad det är som har hänt, av någon anledning skickar den mer än 4 gånger så mycket data som på desktop och den största delen är bilderna (t.ex en liten bild på en lasagne på 3.2 MB!). Så en massiv förbättring är att använda bilder med rätt storlek och att skjuta upp inläsningen och bilder som inte visas på skärmen samt skickar dem i ett modernare bildformat till de webbläsare som stöder det. Att reducera JavaScipt som inte används är också en förbättring 
som kan göras.

***

### Sammanfattning

<div class="embed-container">
<iframe class="google-sheet" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vQ4xbCuCfT4BoDnBqTJpxAh19o64MXV8RiBHPIeGLpqF-bQ3iUUI1BKXyFQtDHVqW7B1qA4uDcA3Z8V/pubhtml?gid=0&amp;single=true&amp;widget=true&amp;headers=false"></iframe>
</div>

**koket.se** hamnar i mitten av de 3 testade sidorna när det kommer till laddningstid och mängd data som laddas. En förbättring är att reducera javaskript som inte används.

**Mathem.se** är den snabbaste sidan när det kommer till laddningstid. På desktop vyn är den sidan som skickar mest data och den skickar även mer data på mobil mobil vyn än desktop vyn. En stor förbättring hadde varit att använda bilder med rätt storlek och att reducera javaskript som inte har använts är en annan förbättring.

**Arla.se** är den långsammaste sidan när det  kommer till laddningstid. Fast på desktop så är den sidan som laddar minst mängd data.  
Men på mobil vyn händer något konstigt och mängden data mer än fyrdubblas. Att reducera javaskript som inte används är en förbättring men den absolut största förbättringen hade varit att skicka bilderna i rätt storlek.

Den generella förbättringen på alla 3 sidorna är att reducera mängden javaskript som inte används och på 2/3 sidor är bilderna alldeles för stora.

Sidorna rankat baserat på speed index samt mängd data som laddas ner.
1. koket.se
2. mathem.se
3. arla.se

I praktiken känns **koket.se** och **mathem.se** lika snabba att använda på både desktop och mobil. **Arla.se** på desktop ligger inte långt efter men på mobil är det en helt annan sak för mängden data är på tok för stor.

jag anser att det viktiga innehållet på en sida bör visas inom 2 sekunder och att det ska gå att interagera med sidan 1 till 2 sekunder efter det. På desktop uppfyller alla 3 sidorna mina krav Och på mobil vy klarar både **koket.se** och **mathem.se** kraven. Upplevelsen med **arla.se** på mobil vy är inte så dåliga som resultaten från mätningarna visar. Den är långsammare men det stora problemet är att mängden data som skickas är så onödigt stor att jag hade undvikit den.


Övrigt
-----------------------

Skrivet av Tomas Zwolinski.