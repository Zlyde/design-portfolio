Laddningstid
=======================

Detta är en rapport som jämför och analyserar laddningstiden hos tre olika sidor, prestandan hos sidorna
på mobil och dator, och eventuella åtgärder som gjorts/kan göras för att öka hastigheten.

Urval
-----------------------

Jag har valt tre olika bloggar för att jämföra. Detta urval gjorde jag för att se om åtgärder gjorts för att öka
laddningshastigheter för dessa bloggar. Första sidan är en mode-blogg, andra bloggen handlar om trädgård,
och tredje är en blogg för fans av Margit Sandemos verk "Sagan om Isfolket".

https://annawii.se/

https://gardener.blogg.se/index.html

https://isfolket.blogg.se/

<div class="landingpage">
    <h1>Länkar till hemsidorna:</h1>
    <div class="box1">
        <a href="https://annawii.se/" target="_blank">
            <picture>
                <source media="(min-width: 668px)" srcset="%base_url%/image/annawii.png">
                <img src="%base_url%/image/annawii.png&w=667" alt="anna">
            </picture>
        </a>
    </div>
    <div class="box1">
        <a href="https://gardener.blogg.se/index.html" target="_blank">
            <picture>
                <source media="(min-width: 668px)" srcset="%base_url%/image/gardener.png">
                <img src="%base_url%/image/gardener.png&w=667" alt="garden">
            </picture>
        </a>
    </div>
    <div class="box1">
        <a href="https://isfolket.blogg.se/" target="_blank">
            <picture>
                <source media="(min-width: 668px)" srcset="%base_url%/image/isfolket.png">
                <img src="%base_url%/image/isfolket.png&w=667" alt="isfolk">
            </picture>
        </a>
    </div>
</div>

<br>
Metod
-----------------------

Jag använde Google's verktyg "https://pagespeed.web.dev/" för att analysera resultaten av hastighetsmätningar på sidorna.
Sedan skapade jag ett spreadsheet i Google Docs som jag presenterar nedan.

Resultat
-----------------------

Nedan följer resultaten jag noterade under undersökningen. Första bilden är spreadsheet av datan från mätverktyget pagespeed,
och andra bilden är datan jag mätte från fliken Network i devtools i webbläsaren. Dessa resultat är genomsnittet av tre
separata mätningar av varje sida.

<h4>Prestanda Google Pagespeed</h4>
<div class="embed-container">
    <iframe style="clip-path: inset(0 0 50% 0)" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vTKB-YunmUDJ6X3slmevdIi7BS5Rn6tG5IR3e9YmH8VtE5wJnXrJuvLJhOpuCGNBHBD9KmYecg8lwTb/pubhtml?widget=true&amp;headers=false"></iframe>
</div>

<h4>Laddningstid Devtools Network</h4>
<div class="embed-container">
    <iframe style="clip-path: inset(0 0 50% 0)" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vREx6Y1ISCWllfRVdhEtpc-1A1v2SN9FwnUL1BDD_x_ffprSd_3p4CGwOx1IWbhb-pX5_Wus9oeNlzK/pubhtml?widget=true&amp;headers=false"></iframe>
</div>

Analys
-----------------------

Sammanfattningen av resultaten är att ingen av hemsidorna från urvalet är särskilt optimerade för mobil prestanda. Bloggen om Isfolket fick bäst betyg 38 enligt
verktyget pagespeed för mobil, där de andra sidorna låg väldigt lågt. För dator däremot hade de två andra sidorna betydligt högre betyg med annawii på betyget 73.

När vi tittar på datan från Network-fliken i Devtools ser vi att annawii.se har bäst laddningstid, och vi ser även att laddningstiden blir längre ju fler resurser
som laddas in, dock är storleken på gardener.blogg.se störst även fast isfolket.blogg.se laddar längst. När jag analyserade närmare såg jag att isfolket laddade
in klipp från youtube som tog lång tid att ladda, vilket påverkade resultatet stort. Gardener har även en widget som saktade ned laddningstiden. Det som tog
lång tid för alla tre sidor var inladdning av bilder. Enlig pagespeed fanns det även js-filer för varje sida, samt CSS på isfolket, som inte används, reducerar
man dessa filer förbättras också laddningstiden.

Bilder, JavaScript-filer och widgets är vanliga anledningar till nedsaktning av laddningshastigeter, förbättring av dessa är ett enkelt sätt att sänka laddningstiden.

Enligt dessa resultat rangordnar jag sidorna enligt nedan:

1 - annawii.se

2 - isfolket.blogg.se

3 - gardener.blogg.se

Från data jag samlat samt referenser anser jag att en laddningstid på ca. 2 sekunder är ett godkänt resultat. Två av dessa tre sidor laddade på mindre än 2 sekunder,
medan den enda anledningen till varför den sista, isfolket.blogg.se, inte gjorde det var för att det fanns problem med att ladda in youtube som embed.

Referenser
-----------------------

https://moz.com/learn/seo/page-speed

https://developers.google.com/search/blog/2018/01/using-page-speed-in-mobile-search

Övrigt
-----------------------

Anton Lindahl, anlm19