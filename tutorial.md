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

## Goed gedaan @showdialog

### sfeerverlichting
In deze opdracht leer je hoe je een RGB-LED kan aansturen met de micro:bit.
Je laat de LED van kleur veranderen: rood → blauw → groen.
Zo ontdek je hoe je met code verschillende kleuren kan maken. 🌈

## Stap 1: Sluit de kabels aan

Verbind de kabels correct:

- **R** gaat naar **P2**
- **G** gaat naar **P8**
- **B** gaat naar **P12**

## Stap 2: Wat heb je aangesloten?

Je hebt een **RGB LED** aangesloten.
Een RGB LED is een lampje met drie kleuren:

- **R** = rood
- **G** = groen
- **B** = blauw

## Stap 3: Programmeer rood licht

Gebruik de blokken uit ``||pins: schrijf digitaal pin [P0]||``:

- schrijf digitaal pin **P2** naar **0**
- schrijf digitaal pin **P8** naar **1**
- schrijf digitaal pin **P12** naar **1**

Download het programma

```blocks
basic.forever(function () {
    pins.digitalWritePin(DigitalPin.P2, 0)
    pins.digitalWritePin(DigitalPin.P8, 1)
    pins.digitalWritePin(DigitalPin.P12, 1)
})
```

## Stap 4: Programmeer groen licht

Gebruik de blokken uit ``||pins: schrijf digitaal pin [P0]||``:

- schrijf digitaal pin **P2** naar **1**
- schrijf digitaal pin **P8** naar **0**
- schrijf digitaal pin **P12** naar **1**

Download het programma

```blocks
basic.forever(function () {
    pins.digitalWritePin(DigitalPin.P2, 1)
    pins.digitalWritePin(DigitalPin.P8, 0)
    pins.digitalWritePin(DigitalPin.P12, 1)
})
```

## Stap 5: Programmeer blauw licht

Gebruik de blokken uit ``||pins: schrijf digitaal pin [P0]||``:

- schrijf digitaal pin **P2** naar **1**
- schrijf digitaal pin **P8** naar **1**
- schrijf digitaal pin **P12** naar **0**

Download het programma

```blocks
basic.forever(function () {
    pins.digitalWritePin(DigitalPin.P2, 1)
    pins.digitalWritePin(DigitalPin.P8, 1)
    pins.digitalWritePin(DigitalPin.P12, 0)
})
```

## Stap 6: Maak een lichtshow

Laat nu meerdere kleuren na elkaar verschijnen.  

Gebruik telkens een blok `||basic:pauzeer (ms)||` tussen twee kleuren.
Zo krijgt je podiumlicht tijd om van kleur te veranderen.

🎬 Test je programma.  
Je RGB LED maakt nu een kleine lichtshow.

```blocks
// @highlight
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