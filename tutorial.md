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

Voeg een ``||logic:als <waar> dan, anders||`` blok toe in de ``||basic: de hele tijd||``.
Plaats een ``||logic:<0 = 0>||``  blok in het ``||logic:<waar>||`` gedeelte van de ``||logic:als <waar> dan, anders||`` blok.
Gebruik de ``||pins: Lees digitaal pin [P0]||`` blok in het eerste gedeelte van de ``||logic:<0 = 0>||`` vergelijking.
Vergelijk nu de waarde van ``||pins: Lees digitaal pin [P1]||`` blok of deze gelijk is aan **1**.

```blocks
basic.forever(function () {
// @highlight
    if (pins.digitalReadPin(DigitalPin.P1) == 1) {
       
    }else{}
})
```
## Stap 3:Toon tekst bij indrukken
Voeg een ``||basic: toon tekens||`` blok toe in het **"als"-gedeelte** van de ``||logic:als <waar> dan, anders||`` blok.
**Schrijf een leuke boodschap voor de festivalbezoekers.** Voeg een ``||basic: wis scherm||`` toe in het **"anders"-gedeelte** van de ``||logic:als <waar> dan, anders||`` blok.

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
## Stap 4: download naar de micro:bit
Klik op **Download**-knop linksonderaan.  
Druk op de drukknop en kijk wat er gebeurt.

## Goed gedaan! @showdialog

### Sfeerverlichting

In deze opdracht stuur je een **RGB LED** aan met de **micro:bit**.  
Je laat de LED wisselen tussen **rood**, **groen** en **blauw**. 🌈

## Stap 1: Sluit de kabels aan

Verbind de kabels op de juiste plaats:

- **R** gaat naar **P2**
- **G** gaat naar **P8**
- **B** gaat naar **P12**

Controleer goed of elke kabel juist zit.

## Stap 2: Wat heb je aangesloten?

Je hebt een **RGB LED** aangesloten.

Een RGB LED heeft drie kleuren:

- **R** = rood
- **G** = groen
- **B** = blauw

Door de juiste pinnen aan (hoog) en uit (laag) te zetten, kies je de kleur.

## Stap 3: Programmeer rood licht

Gebruik de blok `||pins:schrijf digitaal pin [P0] naar [0]||`. Voeg deze voor elke pin toe aan de ``||basic: de hele tijd||`` blok.

Stel de pinnen zo in:

- **P2** naar **0**
- **P8** naar **1**
- **P12** naar **1**

Download het programma naar je micro:bit.

```blocks
   // @highlight
basic.forever(function () {
    pins.digitalWritePin(DigitalPin.P2, 0)
    pins.digitalWritePin(DigitalPin.P8, 1)
    pins.digitalWritePin(DigitalPin.P12, 1)
})
```

## Stap 4: Programmeer groen licht
Pas de waarden aan:

- **P2** naar **1**
- **P8** naar **0**
- **P12** naar **1**

Download het programma naar je micro:bit.

```blocks
basic.forever(function () {
    pins.digitalWritePin(DigitalPin.P2, 1)
    pins.digitalWritePin(DigitalPin.P8, 0)
    pins.digitalWritePin(DigitalPin.P12, 1)
})
```
## Stap 5: Programmeer blauw licht
Pas de waarden aan:

- **P2** naar **1**
- **P8** naar **1**
- **P12** naar **0**

Download het programma naar je micro:bit.

```blocks
basic.forever(function () {
    pins.digitalWritePin(DigitalPin.P2, 1)
    pins.digitalWritePin(DigitalPin.P8, 1)
    pins.digitalWritePin(DigitalPin.P12, 0)
})
```
## Stap 6: Maak een lichtshow

Laat de kleuren nu na elkaar verschijnen.
Gebruik tussen elke kleur het blok ``||basic:pauzeer (ms)||``.
Zo blijft elke kleur even zichtbaar.

```blocks
basic.forever(function () {
    pins.digitalWritePin(DigitalPin.P2, 0)
    pins.digitalWritePin(DigitalPin.P8, 1)
    pins.digitalWritePin(DigitalPin.P12, 1)
    basic.pause(500)

    pins.digitalWritePin(DigitalPin.P2, 1)
    pins.digitalWritePin(DigitalPin.P8, 0)
    pins.digitalWritePin(DigitalPin.P12, 1)
    basic.pause(500)

    pins.digitalWritePin(DigitalPin.P2, 1)
    pins.digitalWritePin(DigitalPin.P8, 1)
    pins.digitalWritePin(DigitalPin.P12, 0)
    basic.pause(500)
})
```


```validation.global
# BlocksExistValidator
```