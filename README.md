# Electronische-fakkel

Een electronische fakkel voor een fakkeloptocht.

## Benodigde materialen & gereedschap

* Arduino micro of Arduino nano (makkelijk aan te sluiten vanwege de USB connector) optioneel kan een andere Arduino ook of een ESP8266 of ESP32 maar dan moet je meer solderen.
* (Optioneel) Elektrolytische condensator van 470 uF of meer (10V of meer)
* 8 x 32 pixel flexibel ws2812 matrix
  Verkrijgbaar bij o.a. de volgende webshops:
  * https://nl.aliexpress.com/item/33025679652.html
  * https://www.hobbyelectronica.nl/product/8x32-rgb-ws2812b-led-flex-module/?gclid=EAIaIQobChMI5fu85tn_7wIVhaZ3Ch3kEw4IEAQYAiABEgJ_G_D_BwE
  * https://nl.grandado.com/products/ws2812b-led-digitale-flexibele-dc5v-individueel-adresseerbare-panel-licht-ws2812-8x8-16x16-8x32-module-matrix-scherm?variant=32322300903477
  * https://www.amazon.nl/dp/B07KT1H481
  * https://www.tinytronics.nl/shop/nl/diversen/led-matrix/ws2812b-digitale-5050-rgb-led-matrix-32x8-flexibel
* Powerbank met USB aansluiting
* USB kabel die past op de Arduino micro of nano

* Soldeergereedschap (soldeerbout met medium of kleine punt en soldeer)
* ducttape
* dun draad met vaste kern of een stukje (dun) touw

## Instructies

Desoldeer de aansluiting voor data output (de mannelijke connector) van het scherm maar bewaar de connector, die wordt in de volgende stap hergebruikt. In plaats van desolderen kan je deze ook vlak bij het scherm losknippen.
![Aansluitingen scherm](/MatrixAansluiting.jpg)

Soldeer de net verkregen connector aan de Arduino:
* Rode draad op de 5V aansluiting.
* Zwarte of witte draad op GND.
* Groene draad op pin 6 (bij een ESP8266 of ESP32 sluit je de groene draad aan op pin 13 - D3).

Soldeer eventueel de elektrolytische condensator op de losse rode en witte of rode en zwarte draad die van het scherm afkomt (in de afbeelding "Increase Voltage Wire genoemd). 

LET OP, de condensator heeft een witte streep of aanduiding die de negatieve kant aangeeft. Deze dient op de witte of zwarte draad aangesloten te worden, de andere kant van de condensator is voor de rode draad. Controleer of je de polariteit goed hebt aangesloten en isoleer de aansluitingen met ducttape.

Sluit de Arduino aan op de computer en upload de sketch (fakkel.ino).

Maak van het scherm een rolletje (niet te strak) en plak met ducttape eventueel de arduino en de condensator aan de binnenkant vast. Een deel van het scherm zal hierdoor niet zichtbaar zijn maar dat maakt niet uit voor het effect. Bind tussen de LEDs een touwtje of draadje zodat het scherm een rolletje blijft.

Plak het geheel met ducttape vast op een (bamboe)stokje. Zorg dat de stok niet te zwaar of stevig is om inbeslagname te voorkomen anders kunnen de instanties de stok zien als een slagwapen.

![Fakkel](/Fakkel.gif)

## Optionele houder

Optioneel kan je een houder printen, door in het midden een bout en een moer met hotglue vast te zetten kan je ze op elkaar vastdraaien, in de rand kan je dan de matrix vastklemmen. Tip: plak de matrix in de onderste (die met het doorlopende gat) houder vast met wat stukjes ducttape, de uiteinden overlappen een paar millimeter zodat het een geheel wordt.

In de onderste houder kan je vervolgens iets maken om de fakkel op vast te zetten.

<img src="https://github.com/DigitaalProtesteren/Electronische-fakkel/Fakkelhouder.jpg" alt="Fakkelhouder" width="250"/>

## Optionele batterij
In plaats van een powerbank kan je ook een IKEA batterij en een DC/DC omvormer gebruiken, bijvoorbeeld de Braunit:
 * https://www.ikea.com/nl/nl/p/braunit-batterijpakket-10433258/

In combinatie met een goedkope DC/DC omvormer, bijvoorbeeld verkrijgbaar bij de volgende webshops:
 * https://nl.aliexpress.com/item/32880983608.html
 * https://www.hobbyelectronica.nl/product/lm2596s-dc-dc-regelbare-step-down/
 * https://www.amazon.nl/Allayu-converter-Step-Down-Verstelbare-Converter/dp/B09GY1GZHK/ref=sr_1_3_sspa
 * https://www.tinytronics.nl/shop/nl/power/spanningsconverters/buck-(step-down)-converters/mini-dc-dc-verstelbare-step-down-buck-converter-0.5a-mp2307

Voor de batterij kan je een houder printen, op Thingsverse is een mooie houder te vinden (https://cdn.thingiverse.com/assets/b0/ff/df/dc/c7/Battery_constraint.stl). Je kan de print na 1-1,5 cm afbreken. In plaats van de officiële connector (https://nl.aliexpress.com/item/4000332107587.html) kan je ook gewoon twee stukjes metaal pakken die tussen de contacten van de batterij passen:
 * Knip twee stukje metaal uit van ongeveer 10 x 5 mm.
 * Vouw de stukjes over de lengte in een hoek van 90 graden.
 * Knip uit de houder het plastic weg wat voor de batterijcontacten zit, laat de zijkanten zitten.
 * Soldeer aan beide stukjes metaal een draadje.
 * Plaats de batterij in de houder en plaats de stukjes metaal zodanig dat ze contact maken met de uiterste twee contacten van de batterij.
 * Lijm de stukjes metaal vast met hotglue (let op dat je geen lijm op de batterij krijgt).

![Batterijhouder](/Batterijhouder.jpg)
