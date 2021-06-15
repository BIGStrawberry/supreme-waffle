# supreme-waffle


# opdracht 1 - Interpreter
Als eerste opdracht gaan we een interpreter bouwen. De basisfunctionaliteit die we willen hebben is: we implementeren één of meerdere functies in een zelf-gekozen of zelfontworpen programmeertaal. De interpreter moet dus minimaal:
* één functie per file kunnen supporten (mag ook meer)
* de interpreter moet de inputs van de functie kunnen meegeven (mag op de commandline, maar mag ook met een GUI)
* een functie moet een andere functie kunnen callen (die in een andere file mag staan die de interpreter dan ook moet kunnen inladen)
* de interpreter moet het resultaat van de functie kunnen weergeven7

## Must-haves
Er zijn drie categoriën van must-haves. 
Criteria zijn eisen die wij stellen aan de stijl en manier van programmeren.
Functionaliteiten zijn dingen die de interpreter moet kunnen.
Inleveritems gaat over hoe en wat er precies moet worden ingeleverd.

### Criteria
* De code is goed becommentariëerd.
* Er is een duidelijke README (zie ook Inleveritems).
* De code is geschreven in functionele programmeerstijl.
* De gekozen of ontworpen programmeertaal is Turingcompleet. Turing-compleetheid is aantoonbaar door aan te tonen dat de programmeertaal een Turing machine of Minsky (Register) machine kan implementeren, maar dit is vaak lastig. Je kan ook laten zien dat de programmeertaal in kwestie op zijn minst dezelfde functionaliteit kan bieden als een andere Turing-complete taal (zoals Brainfuck).
* Deze taal moet minstens of loops of goto-statments, of lambda-calculus ondersteunen.
* De taal mag géén Python, Brainfuck, C++ , of Assembler zijn.
* De code moet classes bevatten (voor bijvoorbeeld de Tokens en de AST), met inheritance.
* Object-printing functions voor elke class (via __str__)
* De code moet minstens één zelf-geschreven decorator (met -syntax) bevatten en gebruiken.
* Alle functions moeten type-annotated zijn (volgens het formaat in Hoofdstuk 4.4), zowel in commentaar (Haskell-type notatie) en in de functie zelf (Python-type notatie).
* Het gebruik van minstens 3 hogere-orde functies zoals: map, foldr, foldl, zipWith, zip, of andere (bijv. zelf-bedachte) hogere-orde functies. NB: de meeste standaard
11 hogere-orde functies zijn in Python geïmplementeerd en hoeven niet zelf geschreven te worden. Map zit bijvoorbeeld standaard zonder verdere imports in Python. foldl
heet reduce in Python en zit in de functools library voor hogere-orde functies.

### Functionaliteiten
* De interpreter moet minstens één functie per file kunnen supporten (mag ook meer)
* De interpreter moet de inputs van de functie kunnen meegeven (mag op de commandline, maar mag ook met een GUI).
* Een functie moet een andere functie kunnen aanroepen (als die in een andere file mag staan dan moet de interpreter die ook automatisch kunnen inladen)
* De interpreter moet het resultaat van de functie kunnen weergeven.

### Inleveritems en -format
Ingeleverd moeten worden:
* De code van de interpreter
* Voorbeeldcode van je eigen programmeertaal, die in ieder geval de functies zoals beschreven in Paragraaf 3.1 implementeren.
* Een README met waar aan welke criteria en functionaliteiten voldaan zijn, hoe het programma gebruikt kan worden, welke libraries het programma nodig heeft (liefst zo min mogelijk), en waarom de taal Turing-compleet is. (Het format is te vinden op https://docs.google.com/document/d/1X2lwEG-WXpHfp3GCPB6YgpgzUGDOO3Gjpec5NIg3imA/).
* Een duidelijke argumentatie waarom de taal Turing-compleet is.
* Een video van 8 à 15 minuten waarin je a) de structuur taal die je ontworpen hebt of gebruikt kort toelicht b) de structuur van de code van de interpreter toelicht c)
kort laat zien hoe de interpreter gebruikt wordt.


## Should/Could-haves
Voor alles boven de 5.5 wil je graag extra functionaliteiten inbouwen. Hieronder staat een niet-uitputtende lijst van mogelijke extra functionaliteiten, met een maximum aantal
punten. NB: je krijgt dus niet automatisch het maximum; meestal niet zelfs.

* ≤2pt: Error-messaging - er is niets irritanter dan code die niet werkt met een stel vage foutmeldingen (ik zeg “segmentation fault”) die je geen hint geven waar de fout eigenlijk zit. Help een programmeur uit de brand, en schrijf een goede error-handler waarmee een programmeur uit de voeten kan.

* ≤4pt: Visualisatie kan erg interessant zijn, zeker als je bijvoorbeeld een editor hebt waarbij
je de staat van het programma kan zien, of zelfs breakpunten kan zetten. Zie bijvoorbeeld de assembler-tool van Lennart Jenssen die vorig jaar is gemaakt: https:
//github.com/Lennart99/ASM-interpreter.

* ≤2pt: Het is makkelijk om een Turing-complete taal te maken - zelfs Brainfuck is Turing complete (https://softwareengineering.stackexchange.com/questions/315919/how-is-brainfuck-turing-complete). Advanced language feautures boven bare-bone Turing-compleetheid (en function calls) leveren extra punten op.

* ≤1.5pt: Het maken van een eigen programmeertaal is uitdagend, en levert sowieso 0.5 extra punt op. Wij kunnen nog 1 vol punt toekennen voor bijzonder creatieve dingen.



# opdracht 2  - Compiler
In de tweede opdracht starten we met het werk dat in Opdracht 1 al gedaan is. Met name, de lexer en de parser kunnen volledig worden hergebruikt. Dit betekent natuurlijk niet
dat je je lexer en parser precies zo moet laten als het was - voel je vrij om alle gewenste aanpassingen te maken. Net als vorige opdracht, zijn er weer must-have and should-have criteria en functionaliteiten

## Must-haves
De must-have criteria zijn grotendeels identiek aan de criteria van de eerste opdracht. De functionaliteit is uiteraard wel anders.

### Criteria
* De code is goed becommentariëerd.
* Er is een duidelijke README (zie ook Inleveritems).
* De code is geschreven in functionele programmeerstijl.
* De gekozen of ontworpen programmeertaal is Turingcompleet. Turing-compleetheid is aantoonbaar door aan te tonen dat de programmeertaal een Turing machine of Minsky (Register) machine kan implementeren, maar dit is vaak lastig. Je kan ook laten zien dat de programmeertaal in kwestie op zijn minst dezelfde functionaliteit kan bieden als een andere Turing-complete taal (zoals Brainfuck). Dit mag gekopiëerd zijn uit de eerste opdracht.
* Deze taal moet minstens of loops of goto-statments, of lambda-calculus ondersteunen. Indien je hieraan voldeed in de eerste opdracht voldoe je hier uiteraard ook aan bij
de tweede opdracht.
* De taal mag géén Python, Brainfuck, C++ , of Assembler zijn.
* De code moet classes bevatten (voor bijvoorbeeld de Tokens en de AST), met inheritance. Indien je hieraan voldeed in de eerste opdracht voldoe je hier uiteraard ook direct aan bij de tweede opdracht.
* Object-printing functions voor elke class (via __str__)

!! Naast de code voor de compiler dient er een unit-test te zijn - geschreven in C++ - waarmee de compiler wordt getest. Dat wil zeggen, de output van de compiler moet
meegecompileerd worden met deze unit-test en draaien op de Arduino. De unit-test toont aan dat de gecompilede code correct functioneert.

### Functionaliteiten
* De compiler dient functies om te kunnen zetten naar één of meerdere Assembler voor de Cortex-m0.
* Er is een unit-test, geschreven in C++ .
* * Er is een make-file die de (zelf-geschreven) compiler aanroept op de source-bestanden (in de gekozen programmeertaal) die deze source-bestanden compileert naar .asmfiles. De make-file zorgt er vervolgens voor dat deze .asm-files door middel van een standaard-compiler (zoals gcc of g++) worden meegecompileerd met de unit-tests tot een executable die vervolgens wordt uitgevoerd op een Arduino Due.
* De source-bestanden bevatten in ieder geval de equilavente code voor de voorbeelden uit Paragraaf 3.1, en nog minstens één eigen bedacht voorbeeld. Voor al deze source
files zijn er unit tests.
* De unittests testen de code afdoende, en tonen daarmee aan dat de compiler goed werkt. De test moet dus uitputtend genoeg zijn, en eventuele randgevallen (en mogelijke slechte invoer) testen.

### Inleveritems
De code van de compiler
* De unit-test code in C++ , hierbij mag je gebruik maken van een unit-test library, maar dat hoeft niet (je mag het ook gewoon zelf in platte C++ -code schrijven).
* De source files in je eigen gekozen programmeertaal
* De makefile die de de source files d.m.v. je eigen compiler compileert naar .asm-files, en deze samen met de unittest compileert en draait op de Arduino Due.
* Een README met waar aan welke criteria en functionaliteiten voldaan zijn, hoe het programma gebruikt kan worden, welke libraries het programma nodig heeft (liefst
zo min mogelijk).
* Een duidelijke argumentatie waarom de taal Turing-compleet is, if and only if dit was afgekeurd bij opdracht 1.
* Een video van 8 à 15 minuten waarin je a) de structuur van de code van de compiler toelicht b) uitlegt hoe de source voorbeelden vertaald worden naar .asm-files, en welke strategie je daarvoor gekozen hebt c) een demo, gebruik makend van je unittests.

### Should/Could-haves
* max 2pt Het showen van aanvullende functionaliteit door middel van unit-tests.
* max 1pt Extra nieuwe functionaliteit, bovenop wat je bij opdracht 1 al had.
* max 1.5pt Het genereren van commentaar in de .asm-files waardoor het voor de programmeur makkelijk terug te zoeken valt hoe zijn code wordt gecompileerd
* max 4pt Optimalisatie van de compiler; uiteraard moet de code altijd werkend gecompileerd worden. Alle trucs die je echter toepast om de compiler efficiënter met registers om te laten gaan, of compactere code laten opleveren, leveren – mits goed gedocumenteerd in de README file – extra punten up. Het is hierbij handig om deze optimalisaties
aan en uit te kunnen zetten, zodat het verschil duidelijk getoond kan worden (bijv. in de video).
* max 1pt Uitbreiding van de error-handler van opdracht 1 naar de compiler

# Beoordeling
Bij de opdrachten zullen wij op een aantal dingen letten. Ten eerste, zitten bij beide opdrachten een stel must-haves; dit zijn eisen aan de code en functionaliteiten die goed moeten zijn wil je een voldoende kunnen halen. Voldoen aan de must-haves levert dus een 5,5 op. Voor alle overige punten kun je extra functionaliteiten implementeren die in de Should/Could-haves staan. Je mag ook zelf functionaliteiten voorstellen, maar die moeten dan wel even worden afgestemd met de docent om het maximaal haalbare aantal punten vast te stellen. Wij waarderen doorzettingsvermogen en creativiteit.
