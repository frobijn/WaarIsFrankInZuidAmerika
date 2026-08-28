# Bewerking foto's algemeen

## Downloaden:
- Siril, en installeren
- AstroWizard, is al applicatie.exe
- GraXpert, en installeren.

## Verzamel foto's
- Maak een werkdirectory
- Kopieer alle *.NEF naar een subdirectory *Raw*
- Bekijk de *Raw* foto's:
    - Met satellieten of andere verstoringen: weghalen.

## Stacking met Siril
- Open Siril (1.4) en kies de werkdirectory via het home icon links boven
- Rechter hoofdscherm, tab *Conversion*:
    - Selecteer de bestanden in *Raw* en klik *Add*
    - Vul een *Sequence name* in
    - Converteer de bestanden. Dit levert *.fit op in de werkdirectory.
    - Siril zal vanaf nu de geconverteerde bestanden gebruiken.

Als Siril afgesloten wordt, dan na opnieuw opstarten:

- Rechter hoofdscherm, tab *Sequence*:
    - Search sequence. De enig aanwezige sequence wordt gevonden.

Volgende stap is image alignment:

- Rechter hoofdscherm, tab *Registration*:
    - *Go register*

Volgende stap is stacking:

- Rechter hoofdscherm, tab *Stacking*:
    - *Start stacking*
    - Het resultaat is een bestand r_*Sequence name*_stacked.fits


## Image processing met AstroWizard

- Open AstroWizard
- Laad het r_*Sequence name*_stacked.fits bestand. Staat op z'n kop; laat dat zo.
- Vink *Image looks all one colour?* aan. Wacht tot het plaatje wijzigt.
- Next step: cropping and framing
    - Flip V (en wacht)
    - Gebruik Shave om randen weg te halen
- Volgende stappen volgen:
    - Gebruik stretch wizard - geeft vreemde kleuren, komt later. Kan ook resultaat behouden.
    - Noise reduction kan vreemd uitpakken als er alleen sterren in beeld zijn.
    - Kleur correctie: indien nodig, kan zijn als stretch wizard gebruikt is.

## Meteoren

- Haal de foto's met meteoren uit de set met Raw, zet ze apart in bijv *Meteoren*.
- Converteer *Raw* en *Meteoren* in aparte sequences / werkdirectories.
- Stack *Raw* op de gewone manier (*Sum stacking*)
- Stack *Meteoren* met *pixel maximum stacking*

- Zet de twee resulterende *_stacked.fits in een nieuwe werkdirectory
- Converteer ze / maak er een *.seq file voor.
- Registreer de files
- Stack beide met *pixel maximum stacking*

- Resulterende image behandelen met AstroWizard.