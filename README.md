# Web Typography, 2020/2021

Als je doof bent, of als je om een andere reden geen geluid kunt horen, dan mis je veel informatie als je een film kijkt. Knisperende voetstappen, langzaam aanzwellende muziek, nerveus getik op een deur, je hoort het natuurlijk allemaal niet. Nu bestaat er zoiets als *closed caption*, wat een type ondertiteling is waarbij ook dingen als omgevingsgeluiden en de muziek beschreven worden. Hierdoor krijgt een kijker die informatie wel binnen.

Alleen wordt die auditieve informatie nogal neutraal beschreven. Het geluid van huilend persoon zou bijvoorbeeld beschreven kunnen worden als *snikgeluid op de achtergrond*. En iemand die lacht zou geschreven kunnen worden als *iemand lacht.* Heel neutraal, bijna zakelijk, en bovendien allebei in precies hetzelfde neutrale lettertype. Terwijl het toch echt over twee heel verschillende emoties gaat. 

Dat kan visueel sterker. 

En dat gaan jullie doen.

## Leerdoelen

- Je kan de kennis over vormgeving die je hebt opgedaan tijdens de minor technisch toepassen met behulp van CSS
- Je kan verborgen nuance uit een audiotrack overtuigend vertalen naar visuele (typografische) beelden
- Je kan je typografische keuzes onderbouwen.
- Je hebt de exclusive design principles gebruikt.

## Oplevering

Je levert een werkende versie op, gemaakt met HTML, CSS en JavaScript. Deze staat op Github. In een duidelijke readme documenteer en onderbouw je je ontwerpkeuzes. Je developmentgeschiedenis is terug te vinden op GitHub.

Je levert ook een *screen recording* met audio op van je fragment. Dit is een video van de definitieve versie, gemaakt van jouw browserscherm.

De beoordeling is mondeling en volgt [de rubric uit het beoordelingsformulier](web-typografie-beoordeling.pdf).

## Typografische restricties

Je *moet* een van deze twee opties kiezen, en je keuze moet je onderbouwen. In je readme staat een uitleg over je overwegingen om de ene of de andere restrictie te kiezen.

### Optie 1: Systeemfont

De eerste optie is dat je gebruik maakt van het zogenaamde *systeemfont* van degene die naar jouw werk kijkt. Dit font verschilt per operating system, en het verschilt soms zelfs per versie van het operating system. Het is ook aan te passen door de gebruiker zelf. 

Je hebt dus geen controle over welk lettertype er precies gebruikt wordt. Het levert dus een onzeker, en beperkt typografisch palet op. Je hebt geen *light* versies, of *extrabold*. En ook geen serif en sans-serif versie van dezelfde familie. In dit geval heb je alleen de beschikking over normal, **bold** en _italic_. Dit heeft natuurlijk ook zijn voordelen!

### Optie 2: Brenner

Je kan er ook voor kiezen om gebruik te maken van de complete Brenner familie. Dit is een zeer uitgebreid en uiterst flexibel font. [Hier kan je je verdiepen in dit font](https://www.typotheque.com/blog/brenner_an_unusual_typeface_family_with_distinct_voices). Als je kiest voor dit font dan heb je de beschikking over een *sans serif*, een *condensed*, een *serif*, een *monotype*, een *slab*, een *display* en een *script* versie. En veel van deze versies hebben varianten van *light* tot *bold*, en allemaal zowel *bold* als *italic*.

Met Brenner zijn er natuurlijk veel en veel meer mogelijkheden dan met systeemfonts. Dat kan zowel een voordeel als een nadeel zijn. 

Voor een overzicht, zie [de brenner.pdf](brenner.pdf).

## Het fragment

Ik heb een fragment voorbereid. Het gaat om twee scenes uit *Blade Runner 2049*. De captions staan in de HTML, en ze verschijnen in sync met de video. [Kijk maar](closed-captions/index.html).

### De captions

De captions staan in de html, in het bestand index.html. Je kan aan elke paragraaf eventueel een of meer classes toevoegen. Bijvoorbeeld `voice1` of `voice2 soft`. Classes voeg je handmatig toe in de html.

Met JavaScript worden er een paar dingen extra gedaan: 

- er wordt aan elke paragraaf een unieke class toegevoegd (`p0`, `p1`, etc)
- Elk woord wordt in een aparte `span` gezet. Hierdoor kan je elk woord apart stylen, en eventueel ook [na elkaar laten verschijnen](https://github.com/cmda-minor-vid/web-typography-18-19/blob/master/closed-captions/css.css#L41).

### Tijdens het afspelen

Tijdens het afspeelen wordt er een class `on` op de caption gezet als hij moet verschijnen, en een class `off` als hij klaar is. *Zowel class `on` als class `off` blijft op de caption staan!*

De timimg van de captions kan je aanpassen in [closed-captions/captions.js](closed-captions/captions.js).

Er verschijnen ook classes op de body op momenten dat er geluiden worden afgespeeld, zoals `sound1` en `sound2`. Je kan geluiden toevoegen in [closed-captions/sounds.js](closed-captions/sounds.js).

*let op,* de geluiden zijn niet compleet, dit zal je zelf moeten aanvullen.

## Een eigen fragment (afgeraden, uitgebreide onderbouwing is nodig)

Je kan er ook voor kiezen om een eigen, *beter* fragment te gebruiken. Dit wordt afgeraden. De tijd die je besteedt aan het zoeken naar dat fragment kan je beter besteden aan het werken aan de opdracht. Bovendien blijkt dat er vaak fragmenten worden gekozen die niet goed voldoen aan de opdracht. Als je een ander fragment kiest dan *moet* je dit goed onderbouwd voorleggen aan je docent. De deadline hiervoor is vrijdagochtend in de eerste week.

### Waar moet je op letten bij het kiezen van een eigen fragment.
Lees de opdracht nog eens goed door. Waar gaat het ook al weer precies om? 

Voor een goede onderbouwing van je keuze voor een ander fragment moet je deze vragen in elk geval beantwoorden:

- Welke informatie zit er in de audio die echt niet zichtbaar is?
- Welke rol speelt de audio in het fragment?
- Werkt de scene nog zonder geluid?
- Waarom is dit fragment beter dan het aangeboden fragment?

Je kan dan de nodige HTML en JavaScript genereren door gebruik te maken van [caption generator](https://cmda-minor-vid.github.io/web-typography-18-19/generator/) (in Google Chrome). 

Als je de closed captions wil bewerken dan kan je een tool zoals [Amber Script](https://www.amberscript.com/en) gebruiken. Daar kan je exporteren als `.srt`, en die kan je weer door de generator halen.

# Proces Webtypografie
Luna de Fauw
500771577
Webtypografie
Vasilis van Gemert
Minor Visual Interface Design

Dove mensen missen veel informatie tijdens het kijken van een film. Zij horen geen achtergrondmuziek of geluiden. Het was aan mij om het fragment van Bladerunner 2049 op zo'n manier vorm te geven, dat geluid te "zien" is. Dit doe ik gericht op een specifieke gebruiker, Darice. Op 5 maart heb ik haar met mijn groepje geinterviewd (zie logboek "vrijdag 5 maart").

## Logboek

### Dinsdag 2 maart
Ik heb de code doorgenomen en alles via github klaargezet. Ik heb de "lines" ook in de JS gezet zodat ik weet wat ik moet aanroepen in de CSS.

Deze week zijn we gestart met een hoorcollege van Vasilis. Hij heeft ons meer verteld over de Exclusive Design prinicpes die we kunnen gebruiken voor ons design. Na het hoorcollege heb ik het bestand van GitHub geforked en heb ik alles op de juiste manier geïnstalleerd. Daarna had ik met mijn team een videocall om vragen voor Darice te verzinnen. Na de videocall ben ik vast begonnen met de vormgeving van de ondertiteling, het iframe en de achtergrond. Hier was ik vrijdag echter nog niet ver genoeg mee om het aan Darice te laten zien.

### Vrijdag 5 maart

We hebben een interview gehad met Darice. We begrijpen nu beter hoe het voor haar is om doof te zijn en over hoe zij dingen ervaart. Ook zijn we er achter gekomen wat voor films Darice leuk vind en wat ze belangrijk vind bij het lezen van ondertiteling. Zie hieronder de vragen en antwoorden;

**_Ben je altijd al doof geweest?_**

Nee ik was altijd slechthorend, in 2007 doof. Weet wat ik mis, ben niet opgegroei met gebarentaal. Ik gebruikt gesprokentaal. 

**_Hoe was de eerste keer dat je een film keek zonder geluid?_**

Ik miste de ervaring van de muziek/achtergrondgeluid die bij een film hoort. Als je niks hoort, wordt een groot deel van de spanning in een film weggenomen. Ik ga bijna nooit meer naar de bioscoop. Ik ga alleen als er een goede actiefilm uitkomt (zoals Marvel). Doordat het geluid zo hard is in de bioscoop, hoor ik soms klanken.

**_Wat zijn je hobbies?_**

Alles wat internet is, html, css, webblog, nieuwsblog, netflix kijken (Friends) en ik houd van boeken lezen.
	
**_Ben je een rustig of druk persoon?_**

Ik houd van minimalisme. Soms vind ik kleuren en drukte mooi, als het maar strak gedaan is.
	
**_Ben je snel afgeleid, zo ja waardoor?_**

Ja met films kijken wel, als er teveel op het scherm gebeurt word ik afgeleid van het verhaal. 

**_Welke dingen vallen extra op in het leven als je doof bent_**

Als je doof bent merk je pas hoe lastig het is om gesprekken te volgen. We leven in een wereld die ontoegankelijk is voor dove mensen.

**_Hoe zie jij de opdracht het liefst uitgevoerd?_**

Ik vind het leuk als er wordt gespeeld met lettertype, achtergrond en kleuren. Het is prettig als het een geheel is.

**_Vind je het fijn om te kunnen zien wie aan het woord is?_**

Subtiele verschillen in tekst zoals; italic, sans serif/serif, monospace voor aparte stemmen. De ondertiteling en achtergrond moeten niet erg afleiden van de film.

**_Heb je irritaties bij het kijken van films?_**

Ja, de ondertiteling is soms erg slap. Het verdwijnt bijvoorbeeld heel snel terwijl de tekst lang is, op deze manier kan ik niet alles lezen. Ik vind het fijn als omschreven wordt wat voor soort muziek op de achtergrond is, dat zet de sfeer van de film. In sommige ondertiteling staat alleen "muziek", hier kan ik me erg aan irriteren. Als er twee talen gesproken worden, zeg dan bijvoorbeeld wat er in het Spaans wordt gesproken en niet “er wordt Spaans gesproken”.

**_Heb je liever NL of EN ondertiteling?_**

Ik kijk films en series altijd in de originele taal, de ondertiteling moet dezelfde taal zijn.

**_Welke fontsize werkt voor jou het beste?_**

Rond de 16/18px, hangt af van het lettertype.

**_Wat vind je van de film "Bladerunner 2049"?_**

Ik houd totaal niet van post-apocalyptische films, de wereld is al erg genoeg.

**_Denk je dat de ondertiteling het fragment interessanter zou kunnen maken?_**

Met geluiden in combinatie met kleur en goede omschrijving van de muziek kan ondertiteling de film zeker interessant maken.

**_Heb je nog tips voor ons?_** 

Check de kleurtoegankelijkheid van voor- en achtergrond, er moet een goed contrast zijn. Ik wil geen moeite hoeven doen om de ondertiteling te lezen.

### Zaterdag 6 maart
Vandaag ben ik gaan experimenteren met fonts en het vormgeven van de geluiden. 

### Maandag 8 maart 
Vandaag liep ik heel erg vast. De ondertiteling was ineens niet meer zichtbaar, en ik kon er maar niet achter komen waarom. Ik was bovendien ook niet tevreden met de vormgeving van de geluiden en ik wilde totaal wat anders gaan doen. Ik heb toen besloten om weer helemaal opnieuw te starten in een nieuw repository.

### Dinsdag 9 maart - Donderdag 11 maart
Animatie sprint: Ik heb deze week als een gek gewerkt aan het visualiseren van de geluiden (animaties).
Ondertiteling: Deze week heb ik ook het grootste gedeelte van de ondertiteling vormgegeven.


### Vrijdag 12 maart 
Vandaag heb ik mijn eerste ontwerp aan Darice en aan Vasilis laten zien, zij hadden hier de volgende feedback op.

#### Feedback Darice
Bij de herhaling zou ik graag wat duidelijker willen zien dat er herhaald wordt. Ik vind het ook fijn als geluiden beschreven worden. Het is dat ik dit stukje nu uit mijn hoofd ken, maar anders zou ik niet weten wat voor geluiden er op de achtergrond te horen zijn. 

#### Feedback Vasilis
Je zou bij de pieptoon een andere achtergrond kunnen kiezen, dat zou duidelijker zijn. Als het stil is, zou ik de animated gif stoppen. De hele video hoor je een soort ruis en op dat moment is het stil, het zou logisch zijn als de achtergrond dan ook "stil" is.

#### Inspiratie van anderen
- 1x,2x,3x bij herhaling van "within cells interlinked" laten zien of in laten faden.

### Dinsdag 15 maart - Donderdag 18 maart
Deze week heb ik mijn werk aangepast aan de hand van de feedback van Darice en Vasilis. Ik heb de achtergronden aangepast en ik heb de geluiden omschreven. 

## Eindproduct

### Font
Ik heb gekozen voor het Brenner font. Met dit font kan je namelijk zelf bepalen wat de gebruiker te zien gaat krijgen. Je kan op deze manier vaststellen hoe het ontwerp er uit komt te zien. Bij het systeemfont is dat niet het geval. Je weet niet wat de gebruiker op welke manier te zien krijgt, ik zou niet weten wat voor voordelen dat zou kunnen hebben.

#### Brenner Mono Italic
Ik heb Brenner Mono Italic gebruikt voor de ondertiteling van de baseline tester. Hij praat erg monotoom en klinkt als een computer. Op Wikipedia zag ik dat monospace-lettertypes vooral worden gebruikt voor het maken en bekijken van programmeercode. Programmeren staat natuurlijk in relatie met computers, daarom vond ik het een goed font voor de ondertiteling van de baseline tester. Ik heb ervoor gekozen om de tekst in felgroen weer te geven. Net als deze kleur, is de stem erg storend en fel. Door de kleur en het font van de ondertiteling kan de baseline tester makkelijk onderscheiden worden van de rest van de stemmen.

#### Brenner Sans Normal
De ondertiteling van officer K is wit en niet zo speciaal. Aangezien de andere teksten felgekleurd zijn, maakt dit hem juist uniek. De ondertiteling van de computer/baseline tester is al erg fel en kan best storend zijn, daarom heb ik ervoor gekozen om officer K een rustige ondertiteling te geven. Bovendien praat hij op een rustige toon.


#### Brenner Sans Normal
De stem van de boze officer die Officer K beledigd wordt in het rood benadrukt. Ik heb voor rood gekozen omdat hij iets gemeens zegt, namelijk; "fuck off skin-job". Rood wordt vaak geassocieerd met haat. Hij praat op een erg boze toon, maar hij fluisterd. Daarom heb ik zijn ondertiteling een kleinere fontsize gegeven.

#### Brenner Sans Condensed Normal
Voor de laatste stem heb ik het bovenstaande lettertype gekozen. Ik vind dat de persoon een beetje beknepen praat, vandaar condensed. Ik heb zijn ondertiteling een oranje kleur gegeven, om hem te onderscheiden van de rest.

#### Beschrijving geluiden
De beschrijvingen van de geluiden heb ik dezelfde kleur gegeven als de achtergrondkleur die in beeld komt tijdens het geluid. Zo vormen tekst en achtegrond samen "het geluid". De hoge piep op het einde wordt gecombineerd met een irritant blauwe achtergrond en de beschrijving van het geluid in een kleur blauw die amper te lezen is in combinatie met de zwarte achtergrond. Je zou er koppijn van krijgen. Net als je koppijn krijgt van de piep. 

### Animaties
Ik heb verschillende animaties en achtergronden vormgegeven, om de geluiden te laten zien.

#### Buzzer
Het eerste geluid van de video klinkt als een soort alarm/buzzer. Het klinkt alsof er een deur geopend wordt en er daarom een alarm afgaat. Ik associeer een alarm met de kleur rood. Daarom heb ik ervoor gekozen om de achtergrond tijdens dit geluid rood te maken.

#### Sirene
Het tweede geluid is een soort sirene. Bij een sirene hoor je vaak verschillende toonhoogtes. In dit geval twee. Daarom laat ik twee verschillende kleuren in beeld komen als dit geluid te horen is.

#### Low tone en high beep
In het fragment hoor je tot drie keer toe een lage toon met daarna een hoge piep. De lage toon wil ik benadrukken door het scherm heen en weer te schudden. Het lage geluid doet het scherm "trillen". De hoge piep wordt benadrukt door de knalgroene kleur die in beeld komt. Deze kleur is net zo fel en irritant als het geluid. 

#### High beep
Vanaf het moment dat je bij officer K over zijn schouder meekijkt tijdens de baseline test, hoor je een hele irritante piep steeds harder en feller worden. De iframe wordt steeds groter naarmate de piep harder wordt. Als de piep stopt, wordt de iframe weer klein. 

#### Tense music
Bij de tweede baseline test hoor je spannende achtergrond muziek. De tonen van de muziek gaan langzaam omhoog en omloog. Het iframe beweegt net als de geluiden langzaam heen en weer.

### Achtergrond
Voor de achtergrond heb ik gebruik gemaakt van animated gifs. 

#### Binary code
De eerste animated gif (groene cijfertjes) start als de baseline test begint. Als de baseline test begint de computer met het processen van data. En dit is nou net waar binaire codes voor gebruikt worden. De achtergrond staat dus voor de data die wordt waargenomen als Officer K de baseline test ondergaat.

#### Blue error screen
De tweede animated gif is felblauw en beweegt heel snel en druk. Het is irritant en fel, net als de pieptoon. De gif komt langzaam in beeld en wordt ook steeds feller, net als de piep.

#### Red error screen
Bij de tweede baseline test laat ik een rood storend beeld zien, dit staat voor een error. De tweede keer dat officer K de baseline test doet, toont hij namelijk emotie, en dat hoort niet. 

## Exclusive design principles

### Ignore conventions
Ik negeer standaard conventies en ga compleet mijn eigen gang in dit ontwerp. Bijna alle streamingdiensten houden zich aan dezelfde conventies. Donkere achtergrond, het frame staat stil, witte ondertiteling. Van deze conventies trek ik me niks aan. Ik laat het beeld lekker heen en weer schudden. Ik maak de achtergrond afleidend. En de ondertiteling komt in alle vormen en kleuren.

### Prioritise identity
Darice vind het fijn als geluiden duidelijk omschreven worden. Ook houd ze van subtiele verschillen in tekst zoals; italic, sans serif/serif, monospace voor aparte stemmen. De ondertiteling en achtergrond moeten niet erg afleiden van de film. Darice houdt totaal niet van post-apocaliptische films als Bladerunner 2049. 

Ik onderscheid mijzelf van anderen door geluiden duidelijk in beeld te laten zien. Ik ben niet vies van expirementeren en heb er daarom toch voor gekozen om niet helemaal naar Darice te luisteren. De achtergrond is bijvoorbeeld afleidend, maar geeft extra sfeer aan het fragment.

Door een beetje rekening te houden met de identiteit van de film, van Darice en van mij. Ben ik tot een mooi eindproduct gekomen, waar we denk ik allebei tevreden over zijn.

### Study situation
Ten eerste heb ik de film gekeken om me in te kunnen leven in het fragment. Ten tweede heb ik veel gegoogled, vragen gesteld aan May en aan klasgenoten. Op deze manier heb ik op een slimme wijze meer kunnen leren over vormgeven in CSS.

### Add nonsense 
Nonsense was vooral nuttig bij de eerste feedbacksessie. We kregen van Vasilis de tip om vooral lekker out of the box te gaan. Op deze manier konden we meer feedback krijgen van Darice dan bij een "braaf ontwerp".