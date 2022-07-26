## Familjen Pettersons släktforskning

(senaste läsbara version hittar du i pdf-format under [Releases](https://github.com/dennis-the-git/team-petterson/releases/))

Filerna i underkatalogen `pages` innehåller text från de skannade bilderna av originalhäftet. Rådatat för de flesta filer har erhållits via ett sk "OCR"-program som kan översätta bildinfo till textdata (`ASCII`- koder). De flesta av bilderna är dock så svårtolkade att det mesta måste korrigeras för hand. Då texten även behöver anpassas en smula med tanke på grundformatet till pdf-bygget går det i slutändan nästan lika snabbt att renskriva direkt från originalet. Varje textfil i `pages` motsvarar en sida i originalet och är namngiven enligt sidnummer och innehåll, tex: `50_14252.rmd` (sida 50 & Tages 'släktnummer' 14252).

### Hur kan jag bidra med information

Den som skaffar ett github-konto får editeringsrättigheter av mig och kan då själv modifiera filerna. Man går in i katalogen `pages`, väljer filen man vill redigera och klickar sedan på pennan till höger för att komma till editeringsläge. Det går också att skapa helt nya filer via gränssnittet. Att bara fylla i datum och korrigera namn och skrivfel torde inte skapa så mycket huvudbry. Alla sidor följer dessutom samma mönster så det är lätt att lära sig helhetsformatet genom att ta modell efter den text som redan finns.

### Hur sparar jag mina ändringar

Projektets filer hanteras av ett proffsigt versionshanteringssystem och för att göra sina ändringar permanenta och synliga för andra behöver man registrera editeringshändelsen då man är färdig: skrolla till slutet av sidan, skriv en pyttekort kommentar om vad som tillförts på raden under rubriken "Commit changes", verifiera att "Commit directly to develop branch" är valt och tryck till slut på den gröna "Commit..."-knappen. Glömmer man att spara filen genom att göra en "commit" går den nya text man skrivit förlorad då man stänger webbläsaren eller går bort från editeringssidan. Filen återgår då till hur den såg ut innan man började redigera den, "Cancel changes" har samma effekt.

### Hur kan jag hjälpa till på andra sätt

Man behöver inte vara rädd för att något skall gå sönder eller raderas. Systemet upprätthåller en typ av backup på tidigare versioner så allt kan återställas till precis hur det såg ut vid en viss tidpunkt. Men om man bara vill  korrekturläsa den senaste versionen av pdf:n eller nya tillägg och göra egna anteckningar om sådant som saknas och felaktigheter som uppstått är det redan till stor hjälp. Skicka i så fall infon direkt åt mig.

### Varför inte använda Google Docs som en normal människa

Tröskeln för kollaborativ editering kanske skulle vara aningen lägre, men g-docs lämpar sig illa för det petnoga formatet som har mera gemensamt med programkod än ett word-dokument. Mitt eget arbetsflöde och speciellt byggprocessen för pdf:n blir oändligt mycket smidigare så här.

### Vad betyder alla krumelurer i filerna

Vill man skapa en helt ny sida kan man kopiera och klistra in innehållet från en befintlig sida till en ny fil och sedan modifiera innehållet. Så här ser tex en vanlig släktsida ut:

```
\newpage
\renewcommand\partcontent{PETTERSON 1846-1965}

\hypertarget{142}{}

\

142. Modellsnickaren [JACOB PETTERSON KATT](#14)  
  född 8/7 1849 i Pedersöre, död 20/10 1915 i Åbo.  
  Gift 7/12 1876 med Maria Lovisa Hermans,  
  född 8/11 1846 i Pedersöre, död 13/6 1898 i Åbo.

#### Barn:

1421. Hulda Josefina,  
  etc, etc...
```
På de fyra första kryptiska raderna kan man ange text för sidans 'header' samt en unik 'etikett' (huvudpersonens nummer) som sedan går att länka till från andra sidor. Hur det går till ser man några rader ner där "JACOB PETTERSON KATT" blir en aktiv länk till etiketten "14" (dvs en generation upp i filen `37_14.rmd`). De fyra gärdsgårdarna ännu längre ner ser bara till att texten "Barn:" blir en självständig rubrik på egen rad och av passlig storlek.

Det mest avvikande från hur man kanske är van att editera text är just det att man inte kan kontrollera radbyten och sk "white space" på ett intuitivt sätt. Hela Jacobs inlägg (4 rader) är egentligen en och samma löpande paragraf i en numrerad lista. Raderna bryts som de gör i pdf:n pga två mellanslag som avslutar varje rad här i textfilen och den lilla indenteringen i början som får hela stycket att höra ihop. Glömmer man sådant gör det inte så mycket då det uppdagas när jag bygger pdf:n och kan lätt korrigeras av mig då.

Ett barns numrerade stycke följer exakt samma modell som en förälder, men länken går neråt en generation till barnets egen familjesida (om sådan finns), sidans huvudperson länkar i stället uppåt till sina föräldrar.
