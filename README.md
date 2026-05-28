Devke SoC Correctie Zendure

De automatisering Devke SoC Correctie Zendure bewaakt de laagste laadstatus (SoC) van alle beschikbare Zendure AC-batterijen en grijpt in wanneer het systeem onder een veilige ondergrens dreigt te komen.

De basis van de logica is een dynamische sensor (Zendure Laagste SoC) die automatisch de laagste beschikbare SoC bepaalt uit alle herkende batterijen. Het aantal batterijen is daarbij volledig flexibel. Nieuwe batterijen worden automatisch meegenomen en ontbrekende of tijdelijk niet-beschikbare batterijen worden uitgesloten zonder invloed op de berekening.

Werking van de bescherming

Wanneer de laagste SoC onder de ingestelde minimumgrens komt, activeert de automatisering een beschermingsmechanisme. Dit gebeurt ook als het systeem op dat moment handmatig is ingesteld.

In dat geval:

- wordt de huidige modus (bijvoorbeeld Handmatig) tijdelijk opgeslagen
- wordt de bestaande configuratie van het systeem bewaard
- schakelt de automatisering het systeem naar een gecontroleerde handmatige beschermingsmodus
- wordt een vast laadvermogen ingesteld om verdere daling van de SoC te voorkomen

Hierdoor kan de SoC-protectie ook ingrijpen wanneer je zelf bewust handmatig aan het sturen bent, omdat de prioriteit altijd veiligheid van de batterijstatus is.

Herstel van de situatie

Zodra alle batterijen weer boven de doelgrens komen:

- wordt de oorspronkelijke modus hersteld (bijvoorbeeld terug naar Handmatig of Automatisch zoals opgeslagen)
- wordt de vorige synchronisatie- of laadstatus teruggezet -
- en neemt het systeem weer normale aansturing over zonder verdere interventie

Robuustheid

De automatisering is ontworpen om robuust te functioneren bij:

Home Assistant herstarts
tijdelijke onbeschikbaarheid van individuele batterijen
wisselende aantallen batterijen
dynamische SoC-waarden tijdens correcties of herkalibratie

De laagste SoC wordt altijd opnieuw berekend zodra data weer beschikbaar is, waardoor de bescherming zichzelf automatisch herstelt zonder handmatige acties.
