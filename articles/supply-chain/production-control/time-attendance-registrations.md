---
title: Overzicht van Tijd- en aanwezigheidsregistratie
description: Tijdregistratiewerknemers kunnen uiteenlopende typen tijdregistraties invoeren, zoals inklokken, uitklokken, registratie van indirecte activiteiten en verzuimregistratie. Dit onderwerp beschrijft registraties, hun berekening, goedkeuring en het gebruik van de workflow om structuur en automatische goedkeuring aan het proces van het goedkeuren van urenstaten toe te voegen.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, JmgCalcApprovePickDialog, JmgGroupApprove, JmgGroupCalc, JmgGroupSigningTable, JmgRegistration, JmgTimeCalcParmeters, WorkflowTableListPageRnr, JmgRegistrationSetup, JmgStampTrans, JmgStampJournalTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 53351
ms.assetid: 885b0cdf-53d7-4cb4-92fe-da1b9e32b39f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b6fa5715a04aa8077651f5c6e29e6bca83d763c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425488"
---
# <a name="time-and-attendance-registration-overview"></a>Overzicht van Tijd- en aanwezigheidsregistratie

[!include [banner](../includes/banner.md)]

Tijdregistratiewerknemers kunnen uiteenlopende typen tijdregistraties invoeren, zoals inklokken, uitklokken, registratie van indirecte activiteiten en verzuimregistratie. Dit onderwerp beschrijft registraties, hun berekening, goedkeuring en het gebruik van de workflow om structuur en automatische goedkeuring aan het proces van het goedkeuren van urenstaten toe te voegen. 

<a name="registrations"></a>Registraties
-------------

In bedrijven die Tijd en aanwezigheid gebruiken, moeten werknemers de tijd registreren die ze aan het werk besteden evenals hun aanwezigheid. Sommige bedrijven vereisen misschien alleen dat werknemers het in- en uitklokken registreren. In andere bedrijven moeten de werknemers misschien ook het tijdverbruik voor de werkelijke activiteiten registreren evenals de pauzes die ze hebben genomen. De beoogde gebruikers van Tijd en aanwezigheid zijn:
-   Werknemers die verplicht zijn om tijd en aanwezigheid periodiek te registreren, bijvoorbeeld dagelijks, wekelijks of om de twee weken.
-   Supervisors, managers en medewerkers van de salarisadministratie die registraties van werknemers berekenen, goedkeuren en overboeken voor verdere verwerking.

| **Opmerking**                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Als u Tijd en aanwezigheid tegelijk uitvoert met Uitvoering fabricage, worden alle registraties voor projecten, projectactiviteiten, verzuimcodes, indirecte activiteiten, overwerk en flextijd geregistreerd en gebruikt om salaris in beide modules te berekenen. |

## <a name="time-registrations-workers"></a> Tijdregistratiemedewerkers
Om tijd en afwezigheid te registreren moeten werknemers als tijdregistratiewerknemers worden ingesteld in het bedrijf waarin ze werken.

Na instelling kunnen werknemers verschillende typen registraties invoeren.

-   In- en uitklokken wanneer hij aankomt of vertrekt.
-   Tijd- en artikelverbruik voor productietaken.
-   Gebruikte tijd voor een machine op de werkvloer, als de machine als bron is gedefinieerd.

| **Opmerking**                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aan een werknemer kunnen automatisch de tijdregistraties worden toegewezen die voor een bepaalde machine op de werkvloer zijn gemaakt, als de werknemer ervoor kiest als assistent van de machine te werken wanneer hij of zij de productietaak start. |

-   Tijdregistraties voor projecten en projectactiviteiten.
-   Bijzondere kosten en artikelverbruik voor een project registreren via de respectieve projectjournalen voor bijzondere kosten en projectartikeljournalen.
-   Gepland verzuim.
-   Verzuim wanneer hij/zij te laat begint of eerder vertrekt dan gepland.
-   Werkpauzen, ofwel automatisch door het systeem berekend of handmatig geregistreerd.
-   Indirecte activiteiten, wat niet-productieve activiteiten van een werknemer tijdens een werkdag zijn. Voorbeelden van deze activiteiten zijn bijeenkomsten of de reiniging van de werkruimte.
-   Overtijd, wat kan worden geregistreerd als extra uren, flextijd of overwerk.

## <a name="adding-clock-out-registrations"></a>Uitklokregistraties toevoegen
Als werknemers aan het einde van hun werkdag vergeten uit te klokken, kan de ontbrekende registratie worden toegevoegd met een batchtaak. Het systeem vergelijkt de inkloktijd en de uitkloktijd volgens het gekoppelde profiel van de werknemer, en voegt automatisch de ontbrekende uitklokregistratie in die past bij de eindtijd van het profiel. Zowel in- als uitklokregistraties zijn essentieel voor de berekening en goedkeuring van tijdregistraties voordat ze naar salaris kunnen worden overgeboekt.

## <a name="calculating-registrations"></a>Geregistreerde gegevens berekenen
Wanneer een registratiewerknemer aan een berekeningsgroep wordt toegewezen die meestal is gerelateerd aan een specifiek team, ploegendienst of werkgroep. De supervisor of teammanager valideert meestal de registraties die door werknemers zijn gemaakt, en zijn daarom ook de verantwoordelijke persoon voor de berekening voor de respectieve berekeningsgroepen op een dagelijkse basis. Als onderdeel van het berekeningsproces kan de teammanager of supervisor:
-   Foutieve registraties corrigeren. Bijvoorbeeld, schakelcodes wijzigen en feedback op productietaken aanpassen.
-   Ontbrekende registraties toevoegen. Bijvoorbeeld: uitklokregistraties maken en verzuimtransacties maken.
-   Onjuiste registraties verwijderen.

Omdat de geregistreerde tijd bij het werktijdprofiel van de werknemer moet passen vóór het berekenen van de registraties, moet u het werktijdprofiel voor elke werknemer overschrijven die een uitzondering op zijn standaardwerktijdprofiel heeft. In het geval dat het werknemersprofiel dagploeg is, en de werknemer heeft toegestemd om een nachtshift te werken zonder betaling voor overtijd, moet de supervisor of teammanager het standaardprofiel van de werknemer vervangen om de werktijd volgens het standaardnachttarief en niet als overtijd te berekenen. De berekening geeft ook een fout weer als een verzuimregistratie ontbreekt. Deze moet voor het berekenen worden toegevoegd.

## <a name="approving-registrations"></a>Geregistreerde gegevens goedkeuren
Net zoals u een berekeningsgroep aan een tijdregistratiewerknemer toewijst, moet u ook een goedkeuringsgroep toewijzen. Gewoonlijk is de groep specifiek voor een team, ploeg of werkgroep. U moet de tijdregistraties goedkeuren die correct zijn berekend - dit betekent dat een berekening zonder fouten wordt uitgevoerd - voordat de salarisposten kunnen worden gegenereerd die vervolgens naar een salarissysteem kunnen worden overgeboekt. De salarismedewerker zal meestal de goedkeuring van registraties doen. Vóór de goedkeuring kan hij:
-   Salarisovereenkomsten voor afzonderlijke werknemers overschrijven.
-   Handmatige premies toevoegen.
-   Extra informatie invoeren over verzuimregistraties.

| **Opmerking**                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Als er voor specifieke werknemers overuren zijn berekend, kunnen deze overuren worden toegewezen aan specifieke taken gedurende de dag. Dit is van toepassing als taakkosten worden berekend op basis van het salaris van de werknemer. |

## <a name="approving-registrations-using-workflow"></a> Geregistreerde gegevens goedkeuren via een workflow
U kunt een workflow voor het goedkeuringsproces instellen waarmee geregistreerde gegevens die voldoen aan de regels die in de workflow zijn ingesteld, automatisch worden goedgekeurd. Alleen afwijkingen hoeven handmatig worden verwerkt. Als de goedkeuringsworkflow is geactiveerd, kan de teammanager of supervisor de berekende registraties ter goedkeuring indienen. Via het workflowproces worden de toepasselijke goedkeuringen en taken gemaakt en vervolgens toegewezen aan de juiste gebruikers en rollen die in de workflow zijn opgegeven. Er zijn twee workflowgoedkeuringen voor tijd en aanwezigheid.

| Werkstroom                                  | Doel                                                                                                   | Registratietype                                                                                                                                                                                                                                     |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Totaal aantal dagen tijd en aanwezigheid            | De workflow valideert geregistreerde gegevens door deze bijvoorbeeld te vergelijken met het verwachte aantal werkuren voor de dag. |                                                                                                                                                                                                                                                       |
| Journaalregistratie van tijd en aanwezigheid. | De workflow valideert elk registratietype voor de datum van de registratie.                           | Tijd en aanwezigheid • Inklokken • Uitklokken • Verzuim • Pauze • Schakelcode • Project • Projectactiviteit • Productietaken voor indirecte activiteiten • Wachttijd vóór • Instellen • Proces • Overlapping • Transport • Wachttijd na • Assistentie beginnen • Assistentie eindigen |



## <a name="transferring-approved-registrations"></a>Goedgekeurde registraties overboeken
Na goedkeuring van de registraties kunnen ze worden overgeboekt naar een periodieke salaristaak. Overgeboekte geregistreerde gegevens worden geboekt naar de activiteit of taak waarmee deze zijn verbonden, bijvoorbeeld een productieorder of project. Salaristransacties worden gegenereerd voor iedere werknemer op basis van de geregistreerde gegevens.  

## <a name="reversing-transferred-registrations"></a>Overgeboekte registraties omkeren
Het terugboeken van transacties kan plaatsvinden tot het moment waarop de betalingsoverboeking van de salarisperiode wordt uitgevoerd. Dit betekent dat de salarisgegevens zijn overgebracht naar een extern bestand. Wanneer geregistreerde gegevens worden teruggeboekt, worden al deze gegevens teruggenomen en worden eventuele transacties die naar productieorders of projecten zijn geboekt, ongedaan gemaakt en geneutraliseerd.

| **Opmerking**                                                 |
|----------------------------------------------------------|
| Het externe bestand kan worden geïmporteerd in de salarisadministratie. |

## <a name="registrations-in-electronic-timecards"></a>Registraties met elektronische prikkaarten
Werknemers met taken waarvoor directe feedback niet vereist is, zoals het geval is bij productietaken, maar die werken aan projectactiviteiten, kunnen de elektronische prikkaart gebruiken. De elektronische prikkaarten bieden de flexibiliteit om op elk moment registraties in te voeren en op de beste manier voor uw bedrijfsplan - dagelijks, wekelijks, of wanneer een werknemer opnieuw in het kantoor is na weg te zijn geweest. Om elektronische prikkaarten of deze werknemers te gebruiken, moet u Prikkaart gebruiken in de werknemersdetails opgeven. De werknemer kan met elektronische prikkaarten het volgende registreren:

-   Datum
-   Registratietype
-   Taakreferentie, zoals project, productieorder of indirecte activiteit
-   Taaknummer
-   Tijdverbruik
-   Bijzondere projectkosten
-   Projectartikelen






[!INCLUDE[footer-include](../../includes/footer-banner.md)]