---
title: Onderhoudsplannen
description: In dit onderwerp wordt uitgelegd wat onderhoudsplannen zijn in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5a89e85dc92d57b0a5d2fc7e7a5910c7be09387c
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875580"
---
# <a name="maintenance-plans"></a>Onderhoudsplannen


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


In een onderhoudsplan wordt vastgelegd wanneer een geplande preventieve onderhoudstaak moet worden uitgevoerd voor een activum. Onderhoudsplannen kunnen worden gekoppeld aan activa, activatypen, functionele locaties of functionele-locatietypen, maar u maakt eerst de onderhoudsplannen die in uw bedrijf moeten worden gebruikt.

Een onderhoudsplan kan meerdere onderhoudsplanregels hebben. Het type onderhoudstaak en het interval worden opgegeven op de onderhoudsplanregel. Er zijn twee typen onderhoudsplanregels:

- Tijd  
- Teller  

Onderhoudsplanregels van het type Tijd worden gebruikt voor periodiek gepland onderhoud op basis van een vast tijdsinterval. Onderhoudsplanregels van het type Teller worden gebruikt voor gepland onderhoud of reactief onderhoud op basis van registraties van activumtellers. Een onderhoudsplan kan meerdere onderhoudsplanregels van beide typen bevatten.

>[!NOTE]
>Als er geen tellerwaarden voor een tellertype voor een activum zijn geregistreerd, worden de onderhoudsplanregels genegeerd.

Eerst maakt u de onderhoudsplannen die u nodig hebt voor uw preventieve onderhoudstaken en selecteert u de activatypen, activa, functionele-locatietypen en functionele locaties die aan elk onderhoudsplan moeten worden gekoppeld. Daarna kunt u indien nodig ook onderhoudsplannen toevoegen aan een activum of een functionele locatie. U doet dat in **Alle activa** > selecteer activum > sneltabblad **Onderhoudsplannen voor activa**, of **Alle functionele locaties** > selecteer functionele locatie > sneltabblad **Onderhoudsplannen**.

Als u een onderhoudsplan toevoegt aan activatypen of functionele-locatietypen, betekent dit dat het activum of de functionele locatie automatisch wordt toegevoegd aan het onderhoudsplan wanneer u nieuwe activa of functionele locaties met deze activatypen of functionele-locatietypen maakt. De begindatum van de relatie met een onderhoudsplan is de huidige datum, die mogelijk moet worden gecorrigeerd.

## <a name="set-up-maintenance-plans"></a>Onderhoudsplannen instellen

In deze sectie wordt beschreven hoe u onderhoudsplanregels instelt en vindt u voorbeelden van hoe deze kunnen worden gebruikt.

1. Klik op **Activabeheer** > **Instellen** > **Preventief onderhoud** > **Onderhoudsplannen**.

2. Klik op **Nieuw** om een nieuwe sequentie te maken.

3. Geef een id op in het veld **Onderhoudssequentie** en een naam in het veld **Naam**.

4. Voer in het veld **Planningsdatum** de begindatum in waarop de planning voor het onderhoudsplan kan plaatsvinden. Op tijd gebaseerde onderhoudsplanregels kunnen andere planningsdatums hebben.

5. Selecteer Ja in de wisselknop **Actief** om het onderhoudsplan te activeren.

>[!NOTE]
>Als u een onderhoudsplan uitschakelt, worden er geen planningsberichten in het onderhoudsschema gemaakt wanneer u een onderhoudsplantaak plant.

6. De velden **Tolerantiedagen voor** en **Tolerantiedagen na** zijn gerelateerd aan de onderhoudsplanregels waarin het selectievakje **Overlappende onderhoudstaken onderdrukken** is ingeschakeld (zie stap 17). De Tolerantie-velden worden gebruikt om het interval in dagen te verlengen waarin - als meerdere onderhoudsplannen elkaar overlappen - de meest uitgebreide/grootste taak wordt gemaakt als een onderhoudsplanningsregel tijdens de planning van het onderhoudsplan en vaker voorkomende overlappende taken tijdens de planning van het onderhoudsplan achterwege worden gelaten. Voeg het aantal dagen in het veld **Tolerantiedagen voor** in, bijvoorbeeld 2.

7. Als u een waarde in **Tolerantiedagen voor** hebt ingevoerd, voegt u ook het aantal dagen in het veld **Tolerantiedagen na** in, bijvoorbeeld 2.

>[!NOTE]
>Het voorbeeld dat in deze en de vorige stap wordt beschreven, betekent dat als meerdere onderhoudsplanregels elkaar overlappen en **Overlappende onderhoudstaken onderdrukken** voor een of meer regels is geselecteerd, de periode voor het weglaten van onderhoudsschemaregels wordt verlengd tot in totaal vijf dagen (de verwachte begindatum op de onderhoudsschemaregel *en* twee dagen vóór *en* twee dagen na die datum).

8. De velden in de groep **Details** op het sneltabblad **Details** bevatten het aantal onderhoudsplanregels dat is ingesteld in het onderhoudsplan en het aantal activa en functionele locaties voor het onderhoudsplan.

9. Klik op het sneltabblad **Regels** op **Tijdregel toevoegen** of **Activatellerregel toevoegen** als u een nieuwe onderhoudsplanregel wilt maken.

10. Voeg een beschrijving van de regel in het veld **Werkorderbeschrijving** in. De beschrijving wordt overgebracht naar gerelateerde werkorders.

11. Selecteer in het veld **Type onderhoudstaak** het taaktype waaraan de onderhoudsplanregel is gerelateerd.

12. Selecteer in de velden **Variant van type onderhoudstaak** en **Handel** de variant en handel voor het type onderhoudstaak.

13. In de velden **Voltooien binnen dagen** en **Voltooien binnen uren** kunt u de verwachte einddatum in dagen of uren invoegen. De verwachte einddatum wordt ingevoegd ten opzichte van de verwachte begindatum. Deze wordt berekend wanneer de onderhoudsschemaregels worden gemaakt. Zo kunt u 7 in het veld **Voltooien binnen dagen** invoeren als u wilt aangeven dat de betreffende taak binnen een week vanaf de verwachte begindatum moet worden voltooid.

14. Selecteer in het veld **Intervaltype** het type interval dat moet worden gebruikt op de onderhoudsplanregel, bijvoorbeeld Herhaald… of Eenmaal… Raadpleeg de onderstaande tabel [Overzicht van intervaltypen](## Interval types overview) voor een beschrijving van de relatie tussen de interval- en regeltypen.

15. Het veld **Periode** heeft alleen betrekking op tijdregeltypen. Selecteer het periodetype dat aan de periodefrequentie is gekoppeld.

16. Geef in het veld **Periodefrequentie** op hoe dikwijls de regel moet worden gebruikt voor de planning van preventieve onderhoudstaken. Voorbeeld: stel, u hebt een regel van het type Teller gemaakt en de teller is de productiehoeveelheid. Als u dan het getal 20000 in dit veld invoert, worden er tijdens de planning van preventief onderhoud automatisch nieuwe onderhoudssequentieregels gemaakt wanneer u naar verwachting nog 20.000 artikelen gaat produceren.

17. Het selectievakje **Overlappende onderhoudstaken onderdrukken** is gekoppeld aan zowel tijd- als tellerregeltypen. Schakel het selectievakje in als u vermeldingen in het onderhoudsschema wilt verwijderen die op dezelfde datum zijn gemaakt. Dit is relevant als u bijvoorbeeld een regel voor inspectie na 1 maand, een regel voor inspectie na 6 maanden en een regel voor inspectie na 1 jaar hebt gemaakt. Tijdens de inspectie na 1 jaar wilt u dat alleen die inspectie wordt uitgevoerd, niet de andere twee, die volgens het tijdsbestek mogelijk ook uitgevoerd moeten worden. Om dit voorbeeld correct in te stellen, stelt u de regel voor inspectie na 1 jaar in als de eerste regel, de regel voor inspectie na 6 maanden als de tweede regel en de regel voor inspectie na 1 maand als de derde regel. Schakel het selectievakje **Overlappende onderhoudstaken onderdrukken** in voor de regels voor inspectie na 1 maand en 6 maanden. Op deze manier zorgt u ervoor dat de inspecties na 1 en 6 maanden worden genegeerd wanneer u de markering van 1 jaar is bereikt en dat er alleen een onderhoudsschemaregel wordt gemaakt voor de regel voor inspectie na 1 jaar.

>[!NOTE]
>In het voorbeeld dat in deze stap is beschreven, ziet u dat de meest uitgebreide taak, de taak die de meeste taken bevat en die niet zo vaak wordt uitgevoerd, altijd als eerste regel moet worden ingevoegd. De taken die vaker voorkomen, worden vervolgens als afzonderlijke regels ingevoegd in volgorde van frequentie, waarbij de meest frequente taak onderaan de lijst wordt geplaatst.

18. Het veld **Teller** heeft alleen betrekking op tellerregeltypen. Selecteer het tellertype dat op de regel moet worden gebruikt. Als een tellertype niet actief is op een gekoppeld activum, wordt de onderhoudsplanregel weggelaten.

19. Het veld **Time fence voor activumteller in dagen** heeft alleen betrekking op tellerregeltypen. Voeg een numerieke waarde in om aan te geven hoeveel dagen vóór tellerregistraties worden gecontroleerd wanneer de planning van het onderhoudsplan wordt uitgevoerd. Dit betekent hoe ver terug gegevens (bestaande tellerregistraties) worden gebruikt als basis voor het berekenen van de trend die bepaalt hoeveel onderhoudsschemaregels er worden gemaakt.

>*Voorbeeld*: als wordt verwacht dat tellerregistraties eenmaal per maand worden gemaakt, zou u in dit veld de waarde 365 kunnen invoegen omdat de planning voor het onderhoudsplan altijd wordt gebaseerd op de laatste 12 maanden. Dat betekent dat onderhoudsschemaregels op basis van de trend van het afgelopen jaar worden gemaakt. Als u daarentegen de waarde 10 in dit veld invoert, verwacht u dat er vaker tellerregistraties worden gemaakt, bijvoorbeeld dagelijks. Dit betekent dat bij het plannen van het onderhoudsplan de registraties voor de afgelopen 10 dagen worden gebruikt als basis voor de planning van onderhoudsschemaregels.

20. Het veld **Plandatum** heeft alleen betrekking op tijdregeltypen. Als de onderhoudsplanregel een andere planningsdatum heeft dan het hele onderhoudsplan, selecteert u een datum in het veld **Planningsdatum** op de regel.

21. In het veld **Serviceniveau** kunt u op de regel van het onderhoudsplan het serviceniveau van een werkorder selecteren als een verdere beperking. Deze kan worden gebruikt als serviceniveau voor werkorders.

22. Schakel het selectievakje **Automatisch maken** in als u wilt dat er bij het plannen van onderhoudsplannen automatisch een werkorder wordt gemaakt op basis van de geselecteerde onderhoudsplanregel.

23. Als u het selectievakje **Automatisch maken** hebt ingeschakeld, kunt u in het veld **Werkordertype** een werkordertype voor de automatisch gemaakte werkorder selecteren. Als u het selectievakje **Automatisch maken** hebt ingeschakeld en u in dit veld geen werkordertype selecteert, wordt het werkordertype gebruikt dat is geselecteerd in **Activabeheer** > **Instellen** > **Parameters voor Activabeheer** > koppeling **Werkorders** > veld **Type preventieve werkorder**.

24. Gebruik de velden **Seizoen van** en **Seizoen tot** om een herhaaldelijke tijdgebaseerde onderhoudsplanregel te maken binnen een periode van twaalf maanden. *Voorbeeld* : apparatuur die wordt gebruikt voor het onderhoud van groenvoorzieningen moet elk voorjaar binnen een vooraf gedefinieerde periode worden nagekeken. Voeg in het veld **Seizoen van** de begindatum in van de periode die moet worden herhaald.

25. Voeg in het veld **Seizoen tot** de einddatum in van de periode die moet worden herhaald.

26. In het veld **Resulterende periode** wordt de huidige periode weergegeven die moet worden herhaald. Wanneer de huidige periode is verstreken en u een nieuw jaar start, wordt de periode die in dit veld wordt weergegeven, bijgewerkt met de volgende periode in de sequentie voor herhalen.

27. Selecteer op het sneltabblad **Activa** de activa die moeten worden gerelateerd aan het onderhoudsplan.

28. Selecteer op het sneltabblad **Activatypen** de activatypen die moeten worden gerelateerd aan het onderhoudsplan.

29. Selecteer op het sneltabblad **Functionele locaties** de functionele locaties die moeten worden gerelateerd aan het onderhoudsplan. Indien nodig kunt u de instelling specifieker maken door een specifiek activatype, een fabrikant en een model te selecteren.

30. Selecteer op het sneltabblad **Functionele-locatietypen** de functionele-locatietypen die moeten worden gerelateerd aan het onderhoudsplan.

>[!NOTE]
>Wanneer werkorders handmatig worden gemaakt voor activa die onder een leveranciersgarantie vallen, wordt er een dialoogvenster weergegeven om de gebruiker te informeren over de garantie. Het maken van de werkorder kan dan worden geannuleerd. De controle op een garantierelatie wordt achterwege gelaten voor werkorders die automatisch worden gemaakt.

## <a name="interval-types-overview"></a>Overzicht van intervaltypen

| Intervaltype en beschrijving                                                                                                                                                                                                                                                                                                                                                                                                       | Regeltype: Tijd                                                                                                                                                                                                                                                                                                                                                           | Regeltype: Teller                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Intervaltype: Herhaald vanaf planningsdatum** De telling begint op de gebruikte planningsdatum en wanneer u onderhoudsplannen plant, worden onderhoudsschemaregels gemaakt voor wanneer het interval naar verwachting wordt bereikt.                                                                                                                                                                                                                | De **Planningsdatum** op de onderhoudsplanregel wordt gebruikt. Als er geen planningsdatum is geselecteerd op de regel, wordt de **Planningsdatum** voor het onderhoudsplan gebruikt. Voorbeeld: als de waarde 3 in het veld **Periodefrequentie** is ingevoerd en Jaar is geselecteerd in het veld **Periode**, wordt er een nieuwe onderhoudsschemaregel gemaakt die om de 3 jaar wordt gemaakt.                             | De **Planningsdatum** voor het onderhoudsplan wordt gebruikt. Als de teller wordt vervangen, wordt de laatste vervangingsdatum als planningsdatum gebruikt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Intervaltype : Herhaald vanaf begindatum** De telling begint op de begindatum van de activumrelatie. De datum wordt geselecteerd in de detailweergave **Alle activa** > sneltabblad **Onderhoudsplannen voor activa** > veld **Begindatum**, of in de detailweergave **Alle functionele locaties** > sneltabblad **Onderhoudsplannen** > veld **Begindatum**. Wanneer u onderhoudsplannen plant, wordt er een onderhoudsschemaregel gemaakt wanneer het interval is bereikt. | De begindatum van de regel in het onderhoudsplan voor het activum of de functionele locatie wordt gebruikt. Als dat veld leeg is, wordt de **Planningsdatum** voor het onderhoudsplan gebruikt.                                                                                                                                                                                                 | De begindatum van de regel in het onderhoudsplan voor het activum of de functionele locatie wordt gebruikt. Als dat veld leeg is, wordt de **Planningsdatum** voor het onderhoudsplan gebruikt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Intervaltype: Herhaald vanaf laatste werkorder** De telling begint bij de werkelijke einddatum en -tijd van de laatste werkorder die is voltooid voor het activum *en* de combinatie van de variant van het type onderhoudstaak en handel. Deze datum en tijd worden weergegeven in het veld **Werkelijke einddatum** in de detailweergave **Alle werkorders**.                                                                                                                                 | De werkelijke einddatum en -tijd van de werkorder die is voltooid voor het activum *en* de combinatie van de variant van het type onderhoudstaak/Handel wordt gebruikt. Als er geen voltooide werkorder is gevonden, wordt in plaats daarvan een van de datums gebruikt die is gebruikt in het intervaltype Herhaald vanaf begindatum.                                                                                             | De werkelijke einddatum en -tijd van de werkorder die is voltooid voor het activum *en* de combinatie van de variant van het type onderhoudstaak/Handel wordt gebruikt. Als de einddatum en -tijd in de werkorder niet zijn ingevuld, wordt in plaats daarvan een van de datums gebruikt die is gebruikt in het intervaltype Herhaald vanaf begindatum.                                                                                                                                                                                                                                                                                                                                                                           |
| **Intervaltype: Eenmaal vanaf planningsdatum** Zie bovenstaande beschrijving van het intervaltype Herhaald vanaf planningsdatum. Het enige verschil is dat dit intervaltype maar één keer mag worden gebruikt.                                                                                                                                                                                                                                                   | Zie bovenstaande beschrijving van het intervaltype Herhaald vanaf planningsdatum. Dit interval wordt meestal gebruikt voor een eenmalige onderhouds- of servicetaak.                                                                                                                                                                                                                             | Zie bovenstaande beschrijving van het intervaltype Herhaald vanaf planningsdatum. Dit interval wordt meestal gebruikt voor een eenmalige onderhouds- of servicetaak. **Opmerking 1:** dit intervaltype is alleen relevant als de teller wordt vervangen wanneer u een onderhouds- of servicetaak uitvoert. Als een teller om welke reden dan ook wordt vervangen vóór het einde van het geplande interval, wordt er een nieuwe tijd voor de taak berekend vanaf het moment dat de teller wordt vervangen. **Opmerking 2:** als de teller wordt vervangen tijdens het voltooien van de onderhouds- of servicetaak, werkt dit intervaltype als bovenstaand intervaltype Herhaald vanaf planningsdatum.                                             |
| **Intervaltype: Eenmaal vanaf begindatum** Zie bovenstaande beschrijving van het intervaltype Herhaald vanaf begindatum. Het enige verschil is dat dit intervaltype maar één keer mag worden gebruikt.                                                                                                                                                                                                                                                 | Zie bovenstaande beschrijving van het intervaltype Herhaald vanaf begindatum. Dit interval wordt meestal gebruikt voor een eenmalige onderhouds- of servicetaak.                                                                                                                                                                                                                            | Zie bovenstaande beschrijving van het intervaltype Herhaald vanaf begindatum. Dit interval wordt meestal gebruikt voor een eenmalige onderhouds- of servicetaak. Bovenstaande **opmerking 1** is ook van toepassing op dit intervaltype. **Opmerking 3:** als de teller wordt vervangen tijdens het voltooien van de onderhouds- of servicetaak, werkt dit intervaltype als bovenstaand intervaltype Herhaald vanaf begindatum.                                                                                                                                                                                                                                                                                                |
| **Intervaltype: Eenmaal bereikt boven** Dit intervaltype heeft alleen betrekking op tellers en wordt gebruikt om een bovenlimiet aan te geven die op de regel van het onderhoudsplan is ingesteld. Onderhoudsschemaregels krijgen de verwachte begindatum en -tijd van de tellerregistratie. Dat betekent dat deze vermeldingen worden gemaakt met een verwachte begindatum die gelijk is aan of vóór de systeemdatum ligt.                                                | N.v.t.                                                                                                                                                                                                                                                                                                                                                                       | Het tellerinterval geeft een bovenlimiet aan. Als deze limiet wordt overschreden wanneer u een tellerregistratie maakt, wordt er een onderhoudsschemaregel gemaakt wanneer u preventief onderhoud plant.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Intervaltype: Eenmaal bereikt onder** Dit intervaltype heeft alleen betrekking op tellers en wordt gebruikt om een onderlimiet aan te geven die op de regel van het onderhoudsplan is ingesteld. Onderhoudsschemaregels krijgen de verwachte begindatum en -tijd van de tellerregistratie. Dat betekent dat deze vermeldingen worden gemaakt met een verwachte begindatum die gelijk is aan of vóór de systeemdatum ligt.                                                 | N.v.t.                                                                                                                                                                                                                                                                                                                                                                       | Het tellerinterval geeft een onderlimiet aan. Als deze limiet wordt gepasseerd wanneer u een tellerregistratie maakt, wordt er een onderhoudsschemaregel gemaakt wanneer u preventief onderhoud plant.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Intervaltype: Gekoppeld vanaf begindatum** (slechts eenmaal) Een onderhoudsplan kan meer regels met dit intervaltype bevatten. Deze regels zijn gekoppeld. Normaal gesproken maakt u een onderhoudsplan dat alleen regels van dit intervaltype bevat. Onderhoudsschemaregels worden gemaakt door de regel in het onderhoudsplan te identificeren die de eerste verwachte begindatum en -tijd bevat.                                                                                                                                                                                                                                                                                                                                                                                           | Zie bovenstaande beschrijving van het intervaltype Eenmaal vanaf begindatum. Voorbeeld: u maakt twee regels in een onderhoudsplan voor een servicetaak voor een auto: een tijdregel met een periode van 1 jaar en een tellerregel met een limiet van 25.000 km. Er wordt een onderhoudsschemaregel gemaakt voor de limiet die het eerst wordt bereikt. Voor dit regeltype maakt u de regel met de periode van 1 jaar.                                                                                                                                                                                   | Zie bovenstaande beschrijving van het intervaltype Eenmaal vanaf begindatum. Voorbeeld: u maakt twee regels in een onderhoudsplan voor een servicetaak voor een auto: een tijdregel met een periode van 1 jaar en een tellerregel met een limiet van 25.000 km. Er wordt een onderhoudsschemaregel gemaakt voor de limiet die het eerst wordt bereikt. Voor dit regeltype maakt u de regel met de limiet van 25,000 km. Voorbeeld van het maken van twee tellerregels: u kunt ook een onderhoudsplan instellen met twee gekoppelde tellerregels. De eerste regel heeft een limiet van 10.000 geproduceerde artikelen en de tweede regel heeft betrekking op de machine of de werkplaats waarvoor service moet worden verricht na 3000 uur.                                                                                                                                                           |
| **Intervaltype: Gekoppeld vanuit laatste werkorder** (herhaald na elke voltooide werkorder) Een onderhoudsplan kan meer regels met dit intervaltype bevatten. Deze regels zijn gekoppeld. Normaal gesproken maakt u een onderhoudsplan dat alleen regels van dit intervaltype bevat. Onderhoudsschemaregels worden gemaakt door de regel in het onderhoudsplan te identificeren die de eerste verwachte begindatum en -tijd bevat.                                                                                                                                                                                                                                                                                                                                                             | Dit intervaltype werkt in principe net als het hierboven beschreven type Gekoppeld vanaf begindatum. Het enige verschil is de datum waarop het intervaltype is gebaseerd. De datum die wordt gebruikt, is de werkelijke datum en tijd op de laatste werkorder die is voltooid voor het activum *en* de combinatie van de variant van het type onderhoudstaak/Handel                                                                                                                                                                                                                                                           | Dit intervaltype werkt in principe net als het hierboven beschreven type Gekoppeld vanaf begindatum. Het enige verschil is de datum waarop het intervaltype is gebaseerd. De datum die wordt gebruikt, is de werkelijke datum en tijd op de laatste werkorder die is voltooid voor het activum *en* de combinatie van de variant van het type onderhoudstaak/Handel                                                                                                                   |


>[!NOTE]
>Wanneer er onderhoudsschemaregels worden gemaakt voor tijdregels in onderhoudsplannen, is de verwachte tijd altijd het begin van de dag. Voor tellerregels in onderhoudsplannen kan de verwachte tijd elk tijdstip van de dag zijn.

Hieronder vindt u voorbeelden van instellingen van tijd- en tellerregels in onderhoudsplannen:

**Voorbeeld 1: tijdregel in onderhoudsplan:** een smeertaak kan worden ingesteld om te worden uitgevoerd met een vast interval, bijvoorbeeld eenmaal per week. Selecteer hiertoe de optie Herhaald vanaf planningsdatum in het veld **Intervaltype**, zoals in onderstaande afbeelding wordt weergegeven.

![Figuur 2](media/02-preventive-maintenance.png)

**Voorbeeld 2: tijdregel in onderhoudsplan:** een inspectietaak kan zo worden ingesteld dat deze ongeveer eenmaal per week wordt uitgevoerd. Selecteer hiertoe de optie Herhaald vanaf laatste werkorder in het veld **Intervaltype**, zoals in onderstaande afbeelding wordt weergegeven.

![Figuur 3](media/03-preventive-maintenance.png)

**Voorbeeld 3: tellerregel in onderhoudsplan:** Een afbeelding van een urenteller waarbij er telkens na 250 uur een nieuwe onderhoudsschemaregel wordt gemaakt. Het intervaltype voor deze tellerregel is Herhaald vanaf begindatum. De begindatum is de begindatum van de betreffende activa in de detailweergave **Alle activa** > sneltabblad **Onderhoudsplannen voor activa** > veld **Begindatum**, of in de detailweergave **Functionele locatie** > sneltabblad **Onderhoudsplannen** > veld **Begindatum**. Dit is een voorbeeld van *preventief* onderhoudsplan omdat de onderhoudsschemaregel automatisch wordt gemaakt wanneer de drempelwaarde (+ 250) is bereikt. In onderstaande afbeelding ziet u een grafisch voorbeeld.

![Figuur 4](media/04-preventive-maintenance.png)


**Voorbeeld 4: tellerregel in onderhoudsplan:** Een grafische illustratie van een tellerwaarde die afneemt en die de remblokslijtage meet. Er wordt een onderhoudsschemaregel gemaakt wanneer er een tellerwaarde van minder dan 20 mm voor de remblok wordt geregistreerd. Het intervaltype voor deze tellerregel is Eenmaal bereikt onder of Eenmaal vanaf laatste begindatum. Dit is een voorbeeld van een *reactief* onderhoudsplan omdat de onderhoudsschemaregel pas wordt gemaakt wanneer een meting onder de 20 mm wordt geregistreerd. In onderstaande afbeelding ziet u een grafisch voorbeeld.

![Figuur 5](media/05-preventive-maintenance.png)


**Voorbeeld 5: op teller gebaseerde onderhoudsplanregel:** een grafische afbeelding van een teller met een drempel van -18 °Celsius. Er wordt een onderhoudsschemaregel gemaakt wanneer een tellerwaarde boven -18 °Celsius wordt geregistreerd. Het intervaltype voor deze tellerregel is Eenmaal bereikt boven. Dit is een voorbeeld van een *reactief* onderhoudsplan omdat de onderhoudsschemaregel pas wordt gemaakt wanneer een meting hoger dan -18 ° Celsius wordt geregistreerd. In onderstaande afbeelding ziet u een grafisch voorbeeld.

![Figuur 6](media/06-preventive-maintenance.png)

- Wanneer u een nieuw activum maakt en dat activum gebruikmaakt van een activatype dat is gerelateerd aan een onderhoudsplan, wordt het onderhoudsplan automatisch ingevoegd in **Alle objecten** > sneltabblad **Onderhoudsplannen voor activa**. Bovendien worden in de **Standaardinstellingen voor activatypen** de bijbehorende onderhoudsplannen automatisch op het sneltabblad **Onderhoudsplannen** ingevoegd.  
- Als u activatypen of functionele-locatietypen toevoegt aan of verwijdert uit **Onderhoudsplannen**, wordt deze wijziging alleen doorgevoerd voor nieuwe activa die zijn gemaakt nadat u de wijziging hebt aangebracht.  
- Als u activa of functionele locaties toevoegt aan of verwijdert uit **Onderhoudsplannen**, wordt deze wijziging automatisch bijgewerkt in **Alle activa** > tabblad **Onderhoudsplannen voor activa**, of in **Alle functionele locaties** > sneltabblad **Onderhoudsplannen**.  


![Figuur 7](media/07-preventive-maintenance.png)


## <a name="add-a-maintenance-plan-to-an-asset"></a>Een onderhoudsplan toevoegen aan een activum

1. Klik op **Activabeheer** > **Algemeen** > **Activa** > **Alle activa** of **Actieve activa**.

2. Selecteer het activum waarvoor u een onderhoudsplan wilt instellen en klik op **Bewerken**.

3. Selecteer op het sneltabblad **Onderhoudsplannen voor activa** de optie **Regel toevoegen** om een onderhoudsplan toe te voegen aan het activum.

4. Selecteer in het veld **Onderhoudsplan** het relevante onderhoudsplan.

5. Selecteer in het veld **Begindatum** de datum vanaf wanneer de planning van preventieve onderhoudstaken kan plaatsvinden. 

6. Klik op **Opslaan**. Het veld **Actief** wordt automatisch bijgewerkt.


![Figuur 8](media/08-preventive-maintenance.png)

