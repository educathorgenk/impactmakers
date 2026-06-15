# Podiumtechnieker 

## Introductie @showdialog
Vandaag worden jullie **podiumtechniekers op een festival**!  
Jullie zorgen voor:
- een **welkomstboodschap** voor bezoekers  
- de **verlichting (RGB)**  
- de **rookmachine (ventilator)**  

Stap voor stap maken jullie een echte festivalervaring! 🎪✨
*Gebruik zeker de hints als je vastzit.*

## Stap 1: sluit de drukknop aan
Gebruik de kabels op tafel en verbind je drukknop:

- Verbind **één uiteinde** van de kabel met **P1**
- Verbind het **andere uiteinde** van de kabel met **DK**

## Stap 2: gebruik pinnen
We gaan controleren of de drukknop wordt gedrukt.

Voeg een ``||logic:als <waar> anders||`` blok toe in de ``||basic: de hele tijd||``.
Plaats een ``||logic:<0 = 0>||``  blok in het ``||logic:<waar>||`` gedeelte van de ``||logic:als <waar> anders||`` blok.
Gebruik de ``||pins: Lees digitaal pin [P0]||`` blok in het eerste gedeelte van de ``||logic:<0 = 0>||`` vergelijking.
Vergelijk nu de waarde van ``||pins: Lees digitaal pin [P1]||`` blok of deze gelijk is aan **1**.

```blocks
basic.forever(function () {
// @highlight
    if (pins.digitalReadPin(DigitalPin.P1) == 1) {
       
    }else{}
})
```
## Step 3:Toon tekst bij indrukken
Voeg een ``||basic: toon tekens||`` blok toe in het **"als"-gedeelte** van de ``||logic:als <waar> anders||`` blok.
**Schrijf een leuke boodschap voor de festivalbezoekers.** Voeg een ``||basic: wis scherm||`` toe in het **"anders"-gedeelte** van de ``||logic:als <waar> anders||`` blok.

```blocks
basic.forever(function () {
    if (pins.digitalReadPin(DigitalPin.P1) == 1) {
    // @highlight
        basic.showString("Hallo!")
    }else{
     basic.clearScreen()
    }
})
```
## Step 4: download naar de micro:bit
Klik op **Download**-knop linksonderaan.  
Druk op de drukknop en kijk wat er gebeurt.





```validation.global
# BlocksExistValidator
```