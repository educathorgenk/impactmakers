# Podiumtechnieker 

## Introductie @showdialog
Vandaag worden jullie **podiumtechniekers op een festival**!  
Jullie zorgen voor:
- een **welkomstboodschap** voor bezoekers  
- de **verlichting (RGB)**  
- de **rookmachine (ventilator)**  

Met de **micro:bit** bouwen jullie zelf de techniek achter het podium.  
Stap voor stap maken jullie een echte festivalervaring! 🎪✨

*Gebruik zeker de hints als je vastzit.*
![hints-icoon](/static/hint.png)

## Stap 1: sluit de drukknop aan
Gebruik de kabels op tafel en verbind je drukknop:

- Verbind **één uiteinde** van de kabel met **P1**
- Verbind het **andere uiteinde** van de kabel met **DK**

## Stap 2: gebruik pinnen
We gaan controleren of er op pin P1 wordt gedrukt.

Voeg een ``||logic:als, anders||`` blok toe in de ``||basic: de hele tijd||``.
Plaats een ``||logic:0 = 0||``  blok in de ``||logic:als, anders||`` blok
Gebruik de ``||pins: Lees digitaal pin||`` blok in het eerste gedeelte van de vergelijking.
Vergelijk nu of deze gelijk is aan 1.

```blocks
basic.forever(function () {
    if (pins.digitalReadPin(DigitalPin.P1) == 1) {
       
    }else{}
})
```