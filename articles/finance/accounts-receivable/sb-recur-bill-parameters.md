---
title: Terugkerende contractfactureringsparameters
description: In dit onderwerp wordt uitgelegd hoe u de standaardwaarden kunt instellen voor factureringsplanningen die worden gemaakt in Terugkerende contractfacturering. Daarnaast wordt uitgelegd hoe u factureringsplanningsgroepen maakt.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 4c52095aa49962cbfc577faf71ab0d71929a386b
ms.sourcegitcommit: 836695c0e95d366ba993f34eee30f57191f356d8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/21/2022
ms.locfileid: "8629407"
---
# <a name="recurring-contract-billing-parameters"></a>Terugkerende contractfactureringsparameters

Op de pagina **Terugkerende contractfactureringsparameters** stelt u de standaardwaarden in voor factureringsplanningen die worden gemaakt in Terugkerende contractfacturering. Deze standaardwaarden worden in eerste instantie gebruikt voor alle factureringsplanningen die u maakt. U kunt echter de waarden voor elke factureringsplanning wijzigen al naar gelang uw behoeften.

## <a name="general-tab"></a>Tabblad Algemeen

1. Selecteer op de pagina **Terugkerende contractfactureringsparameters** op het tabblad **Algemeen** in het veld **Factureringsplanningsgroep** een factureringsplanningsgroep. Raadpleeg het gedeelte [Factureringsplanningsgroepen](#set-up-billing-schedule-groups) verderop in dit onderwerp voor informatie over het instellen van factureringsplanningsgroepen.
2. Selecteer in het veld **Beëindigingstype** hoe de eindfactuur wordt berekend wanneer een factureringsplanningen wordt beëindigd:

    - **Planning aanpassen**: kap het factureringsschema af op de einddatum, stel de status van het schema in op **Laatste facturering** en pas de bijbehorende uitstelplanning aan door het bedrag terug te boeken dat niet meer hoeft te worden toegerekend. Als de begindatum van de facturering na de beëindigingsdatum valt, worden de resterende factureringsperioden verwijderd.
    - **Resterend factuurbedrag**: voeg alle resterende bedragen voor de factureringsplanning toe aan de beëindigingsperiode, wijzig de status van de planning in **Laatste facturering** en werk de uitstelplanning bij. Als de begindatum van de facturering na de datum van beëindiging valt, wordt het totaalbedrag van alle resterende factureringsperioden opgeteld bij de factureringsperiode en worden de resterende factureringsperioden verwijderd.
    - **Geen correctie**: beëindig de factureringsplanning op de opgegeven beëindigingsdatum. De factureringsplanning wordt niet gecorrigeerd.

3. Selecteer in het veld **Uniek planningstype** de waarde **Geen**, om op te geven dat klanten moeten worden beperkt tot één factureringsplanning. Selecteer **Per klant** of **Per eindgebruiker** om op te geven dat klanten alleen een unieke planning kunnen hebben.
4. Stel de optie **Uitlijnen met maand** in op **Ja** om de detailregels van de factureringsplanning uit te lijnen met het einde van de maand, wanneer een factureringsplanning wordt gemaakt of bijgewerkt. Stel het in op **Nee** om incrementele datums te gebruiken.
5. Stel de optie **Gedeeltelijke perioden evenredig verdelen** in op **Ja** om factureringsbedragen toe te wijzen op basis van het aantal dagen in de periode. Stel het in op **Nee** als u in elke factureringsperiode hetzelfde bedrag wilt hebben, ongeacht het aantal dagen.
6. Als u de optie **Gedeeltelijke perioden evenredig verdelen** instelt op **Ja**, stelt u het veld **Methode voor betaling pro rata** in op **Dagelijks** om de bedragen te verdelen op basis van het aantal dagen in de periode. Stel dit in op **Maandelijks** om elke maand hetzelfde bedrag te hebben.
7. Geef op of nieuwe factureringsplanningen standaard in de wacht staan.

    > [!NOTE]
    > Als u de wachtstand wilt verwijderen voor een factureringsplanning, moet de gebruiker deel uitmaken van een gebruikersgroep. Selecteer de optie **Verwijderen van blokkering voor gebruikersgroep overschrijven** om een gebruikersgroep te configureren waarin de optie **Blokkering verwijderen toestaan** is ingeschakeld.

8. Selecteer in het veld **Type factuurtransactie** het standaardtype factuurtransactie voor nieuwe factureringsplanningen.
9. Stel de optie **Uitstel afstemmen op facturering** in op **Ja** om de bijbehorende uitstelplanning zo uit te lijnen dat dezelfde datums worden gebruikt als voor de factureringsplanning. Stel het in op **Nee** als u andere datums wilt gebruiken.
10. Als u de functie voor opbrengstsplitsing gebruikt, stelt u de optie **Opbrengstsplitsing automatisch maken** in op **Ja** wanneer artikelen worden toegevoegd aan een factureringsplanning. Het selectievakje **Gesplitste opbrengst** wordt automatisch ingeschakeld op de factureringsplanningsregel als het artikel is geconfigureerd als een artikel voor opbrengstsplitsing. Stel de optie in op **Nee** als u handmatig het selectievakje **Gesplitste opbrengst** wilt inschakelen.
11. U stelt als volgt de velden voor het maken van verkooporders in:

    - U kunt facturen consolideren per periode, klant of artikel. U kunt elke combinatie van **Ja** en **Nee** instellen. Facturen kunnen ook per artikelgroep worden opgesplitst.
    - De volgende boekingsopties zijn beschikbaar voor facturen:

        - **Verkooporder maken**: alleen de verkooporder wordt gemaakt.
        - **Boekingsfactuur tonen**: de verkooporder wordt gefactureerd en een pagina wordt geopend waarop u de factuur handmatig kunt boeken.
        - **Vrije-tekstfactuur maken**: selecteer deze optie als u vrije-tekstfacturen gebruikt.
        - **Factuur automatisch boeken**: de verkooporder wordt gefactureerd en automatisch geboekt.

    - Stel de optie **Factureringsdatums toevoegen aan artikelomschrijving** in op **Ja** om een beschrijving toe te voegen die de begindatum en einddatum van de facturering bevat.
    - Stel de optie **Nulverbruik uitsluiten** in op **Ja** om factureringsplanningsregels zonder verbruik uit te sluiten. Stel deze optie in op **Nee** om die regels op te nemen in de verkooporder.
    - Stel de optie **Onderliggende artikelen niet afdrukken** in op **Ja** als u de onderliggende artikelen van een opbrengstsplitsing niet op de verkooporder wilt afdrukken. Alleen het hoofdartikel wordt op de factuur getoond. Als het nettobedrag van de (verborgen) onderliggende artikelen een bedrag anders dan nul is, geeft het nettobedrag van de bovenliggende regel een overzicht van de onderliggende regels weer. Stel de optie in op **Nee** om alle onderliggende artikelen onder het bovenliggende artikel op de verkoopfactuur af te drukken.

12. U stelt als volgt de velden voor ondersteuning en verlenging in:

    - Stel de optie voor **Ondersteuning en verlenging automatisch inschakelen** in op **Ja** om de ondersteunings- en verlengingsfunctie automatisch te gebruiken voor een verkooporder.
    - Selecteer in het veld **Ondersteunings- en verlengingsniveau** het standaardniveau voor ondersteuning en vernieuwing.
    - Selecteer in het veld **Ondersteunings- en verlengingshoeveelheid** de hoeveelheid in voor ondersteuning en vernieuwing.
    - Geef in het veld **Standaard begindatum voor ondersteuning en verlenging** de datum op die u wilt gebruiken als standaardbegindatum voor ondersteuning en verlenging:

        - **Transactiedatum**: gebruik de transactiedatum als begindatum.
        - **Begin van huidige maand**: gebruik de eerste van de huidige maand als begindatum.
        - **Begin van volgende maand**: gebruik de eerste van de volgende maand als begindatum. Als de transactiedatum de eerste dag van de maand is, wordt de eerste dag van de huidige maand gebruikt.
        - **Regel van 15**: gebruik de eerste van de huidige maand als begindatum als de transactiedatum tussen de eerste en de vijftiende ligt. Als de transactiedatum op de zestiende of een latere datum valt, gebruikt u de eerste van de volgende maand als begindatum.

    - Stel de optie **Korting opnemen in berekening** in op **Ja** om het kortingsbedrag op te nemen in het ondersteunings- of verlengingsbedrag. Stel deze optie in op **Nee** om het kortingsbedrag niet op te nemen.
    - Selecteer in de velden **Ondersteuningsfrequentie** en **Vernieuwingsfrequentie** de frequentie die moet worden gebruikt wanneer ondersteunings- en verlengingsartikelen worden toegevoegd aan een factureringsplanning: **Dagelijks**, **Maandelijks**, **Driemaandelijks**, **Halfjaarlijks** of **Jaarlijks**.
    - Stel de optie **Uitlijnen op artikelgroep** in op **Ja** om de begin- en einddatums van nieuwe artikelen af te stemmen op bestaande artikelen, op basis van de artikelgroep.
    - Stel de optie **Afstemmen op volgende niet-gefactureerde periode** in op **Ja** om de afstemmingsdatum voor een vernieuwingsartikel te bepalen op basis van de datum van de volgende niet-gefactureerd periode na het begin van de verlenging.
    - Stel de optie **Serienummer kopiëren** in op **Ja** om het serienummer van het artikel van de oorspronkelijke verkooporderregel naar de bijbehorende factureringsplanningsregel te kopiëren.

13. Als u escalatie gebruikt op de factureringsplanning, selecteert u de methode die wordt gebruikt voor de berekening van de consumentenprijsindex.
14. Stel de optie **Prijswijziging bijhouden** instellen op **Ja** als u een registratie van prijswijzigingen op factureringsplanningsregels wilt. Als een factureringsplanningsregel handmatig wordt gewijzigd van standaard naar vast en als een nieuwe prijs is ingevoerd, wordt controle-informatie bijgeboekt op de factureringsplanningsregel. Stel de optie in op **Nee** als u deze wijzigingen niet wilt bijhouden.
15. Geef op of records standaard op begindatum of einddatum worden gefilterd op de pagina **Factuur genereren**.
16. Als u de functie **Niet-gefactureerde opbrengst** gebruikt, geeft u de gebruikte opties op:

    - Stel de optie **Algemene journalen automatisch boeken** in op **Ja** in als u wilt dat het algemene journaal tegelijkertijd wordt gemaakt en geboekt. Stel deze optie in op **Nee** als u het algemene journaal wilt maken en dit vervolgens handmatig boeken.
    - Selecteer in het veld **Standaardjournaalnaam** de standaardjournaalnaam in die u wilt gebruiken wanneer het algemene journaal wordt gemaakt.
    - Selecteer in het veld **Methode korte termijn voor niet-gefactureerd** de methode voor niet-gefactureerd korte termijn in, als u dit gebruikt. Als u **Geen** selecteert, wordt de functie voor korte termijn niet gebruikt voor niet-gefactureerde opbrengst. Selecteer **Voortschrijdende perioden** om altijd 12 maanden te gebruiken, of **Vast jaar** om het resterende boekjaar te gebruiken.

17. Geef de opties op die worden gebruikt wanneer een factureringsplanning en de bijbehorende regels worden beëindigd:

    - **Credit uitgeven**: stel een creditnota op als een factureringsplanning of een factureringsplanningsregel wordt beëindigd.
    - **Creditcorrectie**: maak een creditcorrectie voor een factureringsplanning wanneer een regel wordt beëindigd. De creditcorrectie wordt weergegeven in een toekomstige factureringsperiode voor de factureringsplanning. Met de creditcorrectie wordt het factuurbedrag voor de volgende factureringsperiode bijgewerkt, totdat de creditering is toegepast op de factureringsplanning.
    - **Geen creditering**: voer geen creditcorrectie uit of stel geen creditnota op als een factureringsplanning of een factureringsplanningsregel wordt beëindigd. Deze optie is alleen beschikbaar wanneer u de optie **Geen correctie** gebruikt om een factureringsplanning te beëindigen.

## <a name="sequence-number-tab"></a>Tabblad Volgnummer

Op het tabblad **Volgnummer** op de pagina **Terugkerende contractfactureringsparameters** stelt u de standaardwaarde in voor factureringsplanningsnummers. De standaardwaarden worden ingesteld op de pagina **Nummerreeksen** (**Organisatiebeheer \> Nummerreeksen \> Nummerreeksen**).

## <a name="set-up-billing-schedule-groups"></a>Factureringsplanningsgroepen configureren

Op de pagina **Factureringsplanningsgroepen** kunt u een factureringsplanningsgroep maken voor het factureren van terugkerende contracten. Wanneer een nieuwe factureringsplanning wordt gemaakt en een factureringsplanningsgroep wordt toegepast, worden de waarden die zijn gedefinieerd op de pagina **Factureringsplanningsgroep** ingevoerd als standaardwaarden voor de factureringsplanning. U kunt de standaardwaarden wijzigen voor de factureringsplanning die u maakt. U kunt meerdere factureringsplanningsgroepen instellen en vervolgens een van deze groepen toewijzen als de standaard factureringsplanningsgroep op de pagina **Terugkerende contractfactureringsparameters**.

Ga als volgt te werk om een factureringsplanningsgroep te maken voor terugkerende contractfacturering.

1. Selecteer op de pagina **Factureringsplanningsgroep** de optie **Nieuw** om een factureringsplanningsgroep te maken.
2. Geef in het veld **Factureringsplanningsgroep** een unieke id op.
3. Voer in het veld **Beschrijving** een beschrijving in.
4. Geef in het veld **Factureringsfrequentie** op hoe vaak de factureringsplanning naar een klant moet worden gefactureerd: **Eenmalig**, **Dagelijks**, **Maandelijks**, **Driemaandelijks**, **Halfjaarlijks** of **Jaarlijks**.
5. Voer in het veld **Factureringsinterval** een interval voor de facturering in. Stel bijvoorbeeld het veld **Factureringsfrequentie** in op **Maandelijks** en het veld **Factureringsinterval** op **2** om elke tweede maand te factureren.
6. Selecteer in het veld **Prijsbepalingsmethode** de standaardprijsbepalingsmethode in voor artikelen op de factureringsplanning:

    - **Standaard**: bereken de eenheidsprijs op basis van de totale ingevoerde hoeveelheid en gebruik de standaardprijsstelling van de pagina **Vrijgegeven producten** in Productgegevensbeheer.
    - **Vast**: pas een vaste prijs toe die wordt ingevoerd op de factureringsplanningsregel.
    - **Niveau** : Bereken de eenheidsprijs door een vaste hoeveelheid te gebruiken voor verschillende prijsklassen. Elk niveau moet worden ingevuld voordat u naar de volgende prijsklasse doorgaat.
    - **Vast niveau** : Bereken de eenheidsprijs door een vaste hoeveelheid en bedragen voor totaalprijzen te gebruiken voor verschillende prijsklassen. De prijs die in een factureringsperiode in rekening wordt gebracht, gebruikt de totaalprijs die overeenkomt met het niveau waarop de factureringshoeveelheid bestaat.

7. Selecteer in het veld **Artikeltype** het type artikel voor de factureringsgroep:

    - **Standaard**: selecteer deze waarde als de hoeveelheid statisch is.
    - **Gebruik**: selecteer deze waarde voor artikelen van het type Gemeten of Verbruik. Als u deze waarde selecteert, stelt u het veld **Metingoptie** in op **Lezen** om de waarde voor een factureringsperiode in te voeren (lezen) op een meter of apparaat. De waarde van het verbruik wordt berekend op basis van de vorige factureringsperiode en de huidige meting die u invoert.
    - **Mijlpaal**: selecteer deze waarde als u gebruik wilt maken van de functie Facturering van mijlpalen. Als u deze waarde selecteert, selecteert u in het veld **Mijlpaalsjabloon** de sjabloon voor mijlpalen, als u er een gebruikt.
    - **Verbruik**: selecteer deze waarde om de waarde in te voeren die wordt verbruikt voor een factureringsperiode.

8. Stel de optie **Afzonderlijk factureren** in op **Ja** om een combinatie van geconsolideerde facturen en afzonderlijke facturen voor dezelfde klant te maken. Stel dat een klant vijf factureringsplanningen heeft. Drie daarvan worden geconsolideerd op één factuur, maar voor elk van de andere twee is een aparte factuur vereist. Stel de optie op **Nee** in als u één geconsolideerde factuur voor de klant wilt maken.
9. Stel de optie **Automatisch verlengen** in op **Ja** als u automatisch de planning voor terugkerende facturen wilt verlengen voor de volgende factureringsperiode wanneer de factuur wordt gemaakt. Stel deze optie in op **Nee** om de factureringsplanning handmatig te verlengen. Geef in het veld **Regels die per verlenging worden toegevoegd** op hoeveel regels u wilt toevoegen bij elke verlenging.
10. Stel de optie **Escalatie** in op **Ja** om *escalaties* (prijsverhogingen) toe te passen op de factureringsplanningen die aan deze factureringsplanningsgroep zijn gekoppeld.
