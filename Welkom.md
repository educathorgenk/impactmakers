# Verwelkom de festival bezoekers

## Introductie @showdialog
In deze tutorial leer je hoe je een welkomstbericht toont op de micro:bit wanneer je op een drukknop drukt die verbonden is met pin P1.
Gebruik het lamp-icoontje om tips te krijgen over de code blokken in de tutorial.

## Stap 1: sluit de drukknop aan
Gebruik de kabels op tafel en verbind je drukknop:

- Verbind **één uiteinde** van de kabel met **P1**
- Verbind het **andere uiteinde** van de kabel met **DK**

## Stap 2: gebruik pinnen

We gaan controleren of er op pin P1 wordt gedrukt.

Voeg een ``||logic:als, anders||`` blok toe in de ``||basic: de hele tijd||``.
Plaats een ``||logic:0 = 0||``  blok in de``||logic:als, anders||`` blok
Gebruik de ``||pins: Lees digitaal pin||`` blok in het eerste gedeelte van de vergelijking.
Vergelijk nu of deze gelijk is aan 1.

```blocks
basic.forever(function () {
    if (pins.digitalReadPin(DigitalPin.P1) == 1) {
       
    }else{}
})
```

## Step 3:Toon tekst bij indrukken
Voeg een ``||basic: toon tekens||`` blok toe binnen het ``||logic:als, anders||`` blok.
Schrijf een leuke boodschap voor de festivalbezoekers. Voeg een ``||basic: wis scherm||`` toe in het anders-gedeelte.

```blocks
basic.forever(function () {
    if (pins.digitalReadPin(DigitalPin.P1) == 1) {
        basic.showString("Hallo!")
    }else{
     basic.clearScreen()
    }
})
```

👉 De tekst verschijnt nu wanneer je op de knop drukt


## Step 4: test je programma
Druk op de knop en kijk wat er gebeurt:

- De boodschap verschijnt op de LED display
- Laat je los, dan stopt het bericht

## Step 5: download naar de micro:bit
Sluit je micro:bit aan en klik op **Download**.  
Test nu met de echte knop.

## Goed gedaan!
Je hebt een drukknop aangesloten en gebruikt om een bericht te tonen op de micro:bit 🎉