---
Title: Färganalys
Description: Color analysis
Template: analysis
---

Laddningstider
==========================

Det som denna analys går ut på är att utvärdera tre hemsidor i aspekten laddningstider. De hemsidorna som jag tänker analysera är M3, Feber.se och Sweclockers. De här hemsidorna är tre olika tekniknyhetssidor, som har som mål att få besökarna att läsa artiklar på deras hemsidor.

<div class="container">
    <a href="https://m3.idg.se/">
        <img class="card one-third" src="..//assets/img/m3.png?q=10">
    </a>
    <a href="https://www.feber.se/">
        <img class="card one-third" src="..//assets/img/feber.jpg?q=10"></a>
    <a href="https://www.sweclockers.com/">
        <img class="card one-third" src="..//assets/img/sweclockers.png?q=10">
    </a>
</div>

De verktygen som jag använder mig av för att samla "laddningsdatan" är pagespeed insights. Med detta verktyg får man tillgång till många olika typer av laddningsdata. Med resultatet från denna webbsida kommer jag sedan att jämföra de olika webbplatserna

M3
--------------
<img src="..//assets/img/m3-shot.png?w=100&h=300&q=10">

Resultatet efter att använt mig av pagespeed insights samt dignostikverktyget i firefox är följande:

<iframe class="one-page-data" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vSy9X1M5fS6tCIs7CH-Z5N0u1GRpgk545M8jc5UdH9RPHk_DndowmBFWTLynE4KZLaYVSAsNHlipof8/pubhtml?gid=1744635118&amp;single=true&amp;widget=true&amp;headers=false"></iframe>

Resultatet som ges är att hemsidan får bättre resultat på datorn i jämförelse med mobilen. Detta är inte oväntat då hårdvaran på en dator är oftast snabbare än på en mobiltelefon. Den Cumulativa layoutshiften gör så att M3 inte får godkänt på PageSpeed Insights då den överskrider gränsvärdet. Det värdet innebär att det är saker på sidan som laddas in och gör att sidan rör på sig. M3 ligger ganska högt över gränsvärdet med ett värde på 0,57 på mobil och 0,32 på dator vilket är något som bör förbättras. Resterande värden tester klarar hemsidan av.

När det kommer till laddningstiden på hemsidan var denna inte enkel att läsa av. Eftersom att sidan använder sig av mycket annonser laddas de in under körning av webbplatsen. Detta gör så att sidan aldrig laddas in helt. Det värden jag använder mig av är därför från när sidan laddats in och det pausas innan fler bilder laddas in. Storleken på hemsidan är nästan 200 mb stor där de mesa datan som laddas är från bilder samt videos. De inladdade resurserna är dock endast ca 800 kb stor vilket betyder att hemsidan laddar mycket data under användning. Detta kan vara en anledning till det låga betyget på Cumulativ layout shift (CLS).

Feber
--------------
<img src="..//assets/img/feber-shot.png?w=100&h=300&q=10">

Resultatet efter att använt mig av pagespeed insights samt dignostikverktyget i firefox är följande:

<iframe class="one-page-data" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vSy9X1M5fS6tCIs7CH-Z5N0u1GRpgk545M8jc5UdH9RPHk_DndowmBFWTLynE4KZLaYVSAsNHlipof8/pubhtml?gid=595024197&amp;single=true&amp;widget=true&amp;headers=false"></iframe>


Feber.se resultat får också underkänt på pagespeed insight. Hemsidan har ett för högt värde på Cumulativ layout shift och detta är anledningen till betyget. Utöver detta uppmärksammas det att prestandan på mobila enheter är låg där den får ett betyg på 47/100, mot 73/100 på dator. Largest Contentful Paint är även något som Feber.se får dålig betyg i vilket betyder att det tar lång tid innan hemsidan renderas.

Hemsidan laddas i snitt in på 5,46 s med ca 108,94 kb av resurser. Hemsidans totala storlek är 1,58mb.

Feber
--------------
<img src="..//assets/img/sweclockers-shot.png?w=100&h=300&q=10">

Resultatet efter att använt mig av pagespeed insights samt dignostikverktyget i firefox är följande:

<iframe class="one-page-data" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vSy9X1M5fS6tCIs7CH-Z5N0u1GRpgk545M8jc5UdH9RPHk_DndowmBFWTLynE4KZLaYVSAsNHlipof8/pubhtml?gid=309040085&amp;single=true&amp;widget=true&amp;headers=false"></iframe>

Sweclockers är den första hemsidan som testats med godkänt betyg där hemsidan går igenom på mobila enheter men inte på dator. Återigen är det den Cumulativa layout shiften som gör att hemsidan får underkänt på dator. Prestandan som hemsidan på mobila enheter är dock låg där den får ett betyg på 36/100. På dator har hemsidan 81/100 i betyg i prestanda.

Sammanfattning
---------------
Efter att analyserat de tre hemsidorna kan man enkelt dra slutsatsen att de alla har problem med den Cumulativa Layout Shiften. Detta beror förmodligen på att de laddar in mycket reklam på hemsidan som får sidan att bli längre och kortare. Utöver detta kan man se att eftersom att Sweclockers hemsida hanterar mindre data får den även kortast laddningstid. På sweclockers hemsida är nästan alla resurser inladdade på deras startsida vilket förmodligen bidrar till mindre "layoutshifting". De tre hemsidorna har alla sämre betyg på mobilen än på dator och det är ett område de alla bör se över.

Det går att tydligt se en relation mellan tiden för att ladda in en hemsida och storleken på webbsidan. Alla webbplatserna försörjer sig på annonsintäkter och det är en stor del av deras webbplatser. Detta gör att det konstant är mycket data som laddas in och hemsidan blir aldrig klar. På M3 kan man se att dessa filer är väldigt stora och skulle fördelaktigt komprimeras till mindre.

<iframe class="all-page-data" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vSy9X1M5fS6tCIs7CH-Z5N0u1GRpgk545M8jc5UdH9RPHk_DndowmBFWTLynE4KZLaYVSAsNHlipof8/pubhtml?widget=true&amp;headers=false"></iframe>

Vinnare
-------------------

<img src="..//assets/img/podium.png?w=100&h=300&q=10" width="200px">


1. Sweclockers
2. M3
3. Feber

Vad jag anser som Bra
----------------------
Enligt PubNub:s artikel om hur snabbt realtid uppfattas allt som är under 100ms som att det sker direkt. 1 sekund är snabbt nog för att en normal användare ska känna att det flyter på okej när man interagerar med informationen. Allt som överstiger tio sekunder gör att vi som användare tappar intresset. Med denna fakta skulle jag anse att en laddningstid som inte överskrider 3s är en bra laddningstid. Jag uppfattar inte den stora skillnaden i laddningstiden som jag fick i mina tester på de olika hemsidorna. Det som tar tid att ladda in förmodar jag är reklamen. De tre sidorna tycker jag laddar in bra nog för att jag ska stanna kvar på sidorna och läsa deras artiklar. Sweclockers kan ha ett övertag när det kommer till laddningstiderna men jag tycker att M3 och Feber också är klart godkända. Det viktigaste är att det första som man ser är inladdat när man kommer in på sidan och det uppfattas det som att det är på de tre hemsidorna jag jämfört.

Skribent
--------------------
Albin Stegler

Referenser
---------------------
https://www.pubnub.com/blog/how-fast-is-realtime-human-perception-and-technology/
