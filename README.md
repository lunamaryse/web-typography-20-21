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

# Logboek

### Dinsdag 2 maart
Ik heb de code doorgenomen en alles via github klaargezet. Ik heb de "lines" ook in de JS gezet zodat ik weet wat ik moet aanroepen in de CSS.

### Vrijdag 5 maart

We hebben een interview gehad met Darice. We begrijpen nu beter hoe het is om doof te zijn en over hoe je dan dingen ervaart. Ook zijn we er achter gekomen wat voor films Darice leuk vind en wat ze belangrijk vind bij het lezen van ondertiteling.

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
Ik ben gaan experimenteren met fonts en het vormgeven van de geluiden. 

### Maandag 8 maart 
Vandaag liep ik heel erg vast. De ondertiteling was ineens niet meer zichtbaar, ik was niet tevreden met de vormgegeven geluiden en ik wilde totaal wat anders. Ik heb toen besloten om weer helemaal fris te starten in een nieuw repository.