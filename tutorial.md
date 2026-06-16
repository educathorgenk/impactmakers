# Podiumtechnieker 

## Introductie @showdialog
Vandaag worden jullie **podiumtechniekers op een festival**!  
Jullie zorgen voor:
- een **welkomstboodschap** voor bezoekers  
- de **verlichting (RGB)**  
- de **rookmachine (ventilator)**  

Stap voor stap maken jullie een echte festivalervaring! 🎪✨
Gebruik zeker de hints als je vastzit.

*16-06-26, V2.0.0*

## Stap 1: Sluit de drukknop aan
Gebruik de kabels op tafel en verbind je drukknop:

- Verbind **één uiteinde** van de kabel met **P1**
- Verbind het **andere uiteinde** van de kabel met **DK**

## Stap 2: Gebruik pinnen
We gaan controleren of de drukknop wordt gedrukt.

1. Voeg een ``||logic:als <waar> dan, anders||`` blok toe in de ``||basic: de hele tijd||``.
2. Plaats een ``||logic:<0 = 0>||``  blok in het ``||logic:<waar>||`` gedeelte van de ``||logic:als <waar> dan, anders||`` blok.
3. Gebruik de ``||pins: Lees digitaal pin [P0]||`` blok in het eerste gedeelte van de ``||logic:<0 = 0>||``-vergelijking.
4. Vergelijk nu de waarde van **pin P1** of deze gelijk is aan **1**.

```blocks
basic.forever(function () {
// @highlight
    if (pins.digitalReadPin(DigitalPin.P1) == 1) {
       
    }else{}
})
```
## Stap 3: Toon tekst bij indrukken
1. Voeg een ``||basic: toon tekens||`` blok toe in het **"als"-gedeelte** van de ``||logic:als <waar> dan, anders||`` blok.
2. **Schrijf een leuke boodschap voor de festivalbezoekers.** 
3. Voeg een ``||basic: wis scherm||`` toe in het **"anders"-gedeelte** van de ``||logic:als <waar> dan, anders||`` blok.

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
## Stap 4: Download naar de micro:bit
Klik op de **Download**-knop linksonderaan.  
Druk op de drukknop en kijk wat er gebeurt.

## Goed gedaan! @showdialog

### Sfeerverlichting

In deze opdracht stuur je een **RGB LED** aan met de **micro:bit**.  
Je laat de LED wisselen tussen 🔴 **rood**, 🟢 **groen** en 🔵 **blauw**.

## Stap 1: Sluit de kabels aan

Verbind de kabels op de juiste plaats:

- 🔴 **R** gaat naar **P2**
- 🟢 **G** gaat naar **P8**
- 🔵 **B** gaat naar **P12**

Controleer goed of elke kabel juist zit.

## Stap 2: Wat heb je aangesloten?
Je hebt een **RGB LED** aangesloten.
Een RGB LED heeft drie kleuren:
- **R** = rood
- **G** = groen
- **B** = blauw

Door de juiste pinnen aan (hoog) en uit (laag) te zetten, kies je de kleur.

## Stap 3: Programmeer 🔴 rood licht

Gebruik de blok ``||pins:schrijf digitaal pin [P0] naar [0]||``. Voeg deze voor **elke pin** toe aan de ``||basic: de hele tijd||`` blok.

Stel de pinnen zo in:

- 🔴 **P2** naar **0**
- 🟢 **P8** naar **1**
- 🔵 **P12** naar **1**

Download het programma naar je micro:bit.

```blocks
   // @highlight
basic.forever(function () {
    pins.digitalWritePin(DigitalPin.P2, 0)
    pins.digitalWritePin(DigitalPin.P8, 1)
    pins.digitalWritePin(DigitalPin.P12, 1)
})
```

## Stap 4: Programmeer 🟢 groen licht
Pas de waarden aan zodat het licht 🟢 groen is:

- 🔴 **P2** naar **1**
- 🟢 **P8** naar **0**
- 🔵 **P12** naar **1**

Download het programma naar je micro:bit.

```blocks
basic.forever(function () {
    pins.digitalWritePin(DigitalPin.P2, 1)
    pins.digitalWritePin(DigitalPin.P8, 0)
    pins.digitalWritePin(DigitalPin.P12, 1)
})
```
## Stap 5: Programmeer 🔵 blauw licht
Pas de waarden aan zodat het licht 🔵 blauw is:

- 🔴 **P2** naar **1**
- 🟢 **P8** naar **1**
- 🔵 **P12** naar **0**

Download het programma naar je micro:bit.

```blocks
basic.forever(function () {
    pins.digitalWritePin(DigitalPin.P2, 1)
    pins.digitalWritePin(DigitalPin.P8, 1)
    pins.digitalWritePin(DigitalPin.P12, 0)
})
```
## Stap 6: Maak een lichtshow

Laat de kleuren nu na elkaar verschijnen 🔴🟢🔵.
Gebruik tussen elke kleur een ``||basic:pauzeer (ms)||``-blok.
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

## Goed gedaan! @showdialog

# Rookmachine bedienen
In deze opdracht gebruik je een **drukknop** om een **ventilator** te sturen.

*Denk even terug aan de eerste opdracht: toen liet je een boodschap op het scherm verschijnen door op de drukknop te drukken.*

## Stap 1: Sluit alles aan
Controleer de aansluitingen en verbind als volgt:
- Drukknop (DK) → **P1**
- Ventilator (VEN) → **P0**

✅ Controleer of alles stevig en juist verbonden is.

## Stap 2: Wat ga je doen?
Je gaat controleren of de knop wordt ingedrukt.
- Knop ingedrukt = waarde van de pin is **1**
- Knop niet ingedrukt = waarde van de pin is **0**

Met een ``||logic:als <waar> dan, anders||`` blok laat je de ventilator reageren.

## Stap 3: Bouw je programma
1. Neem een ``||logic:als <waar> dan, anders||`` blok  
2. Plaats een ``||logic:<0 = 0>||``  blok in het ``||logic:<waar>||`` gedeelte van de ``||logic:als <waar> dan, anders||`` blok.
3. Gebruik de ``||pins: Lees digitaal pin [P0]||`` blok in het eerste gedeelte van de ``||logic:<0 = 0>||``-vergelijking.

```blocks
basic.forever(function () {
// @highlight
    if (pins.digitalReadPin(DigitalPin.P1) == 1) {
 
    } else {

    }
})
```

## Stap 4: Ventilator aan of uit
### ALS knop ingedrukt (P1 = 1)
- zet **P0** naar **1** *(hint: ``||pins:schrijf digitaal pin||``)*

👉 Ventilator **aan**

### ANDERS
- zet **P0** naar **0**  

👉 Ventilator **uit**

```blocks
basic.forever(function () {
// @highlight
    if (pins.digitalReadPin(DigitalPin.P1) == 1) {
        pins.digitalWritePin(DigitalPin.P0, 1)
    } else {
        pins.digitalWritePin(DigitalPin.P0, 0)
    }
})
```

```validation.global
# BlocksExistValidator
```