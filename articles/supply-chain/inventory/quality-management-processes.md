---
title: Processen voor kwaliteitsbeheer
description: Dit artikel biedt informatie over het kwaliteitsbeheerproces voor niet-overeenkomende producten. Het beschrijft hoe u kwaliteitscontrolefunctionaliteit kunt gebruiken, hoe u niet-conformeringen definieert en beheert, en hoe u omgaat met correcties.
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemSampling, InventNonConformanceHistory, InventNonConformanceTable, InventQualityOrderLineResults, InventQualityOrderTable, InventTestCorrection, InventTestDiagnosticType, InventTestInstrument, InventTestReportSetup, InventTestTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 11574
ms.assetid: 5ac8a059-5cb4-4cb5-ba14-b944bd08dae9
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22372bd2d42b526d10e39174e7fb5ec5281d1b73
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572783"
---
# <a name="quality-management-processes"></a>Processen voor kwaliteitsbeheer

[!include [banner](../includes/banner.md)]

Dit artikel biedt informatie over het kwaliteitsbeheerproces voor niet-overeenkomende producten. Het beschrijft hoe u kwaliteitscontrolefunctionaliteit kunt gebruiken, hoe u niet-conformeringen definieert en beheert, en hoe u omgaat met correcties.

Kwaliteitscontrole omvat het testen van producten en het beheren van materialen die niet overeenkomen. Kwaliteitsbeheerprocessen helpen om een hoog productkwaliteitsniveau in uw leveringsketen te garanderen. Deze processen helpen om de leveringsketenprocessen te optimaliseren en klanttevredenheid te verhogen. Kwaliteitsbeheer kan u helpen keerpunttijden te beheren wanneer u te maken hebt met niet-overeenkomende producten, ongeacht punt van oorsprong van deze producten. U kunt diagnoseresultaten koppelen aan correctietaken. Het systeem kan taken inplannen om problemen te corrigeren, en zo helpen voorkomen dat deze problemen zich in de toekomst opnieuw voordoen. Met kwaliteitsbeheer ook kunt u problemen (inclusief interne problemen) volgen op probleemtype en oplossingen identificeren als korte-termijnoplossingen of lange-termijnoplossingen. De statistieken over Key Performance Indicators (KPI's) bevatten inzicht in niet-conformeringsproblemen die eerder zijn opgetreden en de oplossingen die zijn toegepast om ze te corrigeren. U kunt de historische gegevens gebruiken om de efficiëntie van kwaliteitsmetingen te controleren die eerder zijn genomen en overeenkomende stappen in de toekomst te definiëren.

## <a name="controlling-the-quality-management-process"></a>Het kwaliteitsbeheerproces controleren
Hieronder staan enkele manieren waarop u het kwaliteitsbeheerproces kunt controleren:

-   Maak kwaliteitsorders die zijn gebaseerd op triggerpunten zoals "bij productontvangst" voor inkomende bewerkingen of "bij ophalen product" voor uitgaande bewerkingen.
-   Documenteer testresultaten en bepaal of de resultaten voldoen aan de vastgestelde testcriteria en acceptabele kwaliteitsniveaus.
-   Gebruik documentbeheer voor gedetailleerde productspecificaties en gebruikerspecifieke notities als onderdeel van rapportage tijdens het inspectieproces.
-   Beheer niet-overeenkomende producten en correleer deze producten met aanvullende niet-conformeringsinformatie om de oorspronkelijke oorzaak van een probleem op te sporen.
-   Documenteer de kosten om een niet-conformering te beheren. Deze kosten kunnen bestaan uit de artikelen (zoals reserveonderdelen), diverse kosten en de arbeidsuren die nodig zijn om de niet-conformering te corrigeren.
-   Plan foutcorrectieprocessen door gebruik te maken van correctieafhandeling die is gekoppeld aan kwaliteitsorders.

[![Proces voor kwaliteitsbeheer](./media/quality-management-process-diagram.png)](./media/quality-management-process-diagram.png)  

## <a name="product-testing-and-quality-orders"></a>Producten testen en kwaliteitsorders
Het testen van producten wordt doorgaans geschaard onder kwaliteitscontroles en brengt het gebruik van kwaliteitsorders met zich mee. Met de functionaliteit voor kwaliteitscontrole kunt u het volgende doen:

-   Bepalen welke tests voor materiaal moeten worden uitgevoerd. Tot deze tests behoren de kwaliteitsspecificaties, het desbetreffende testprogramma, de documenten waarin de test wordt beschreven, een bemonsteringsplan en de acceptabele kwaliteitsniveaus.
-   Een kwaliteitsorder maken waarin wordt aangegeven welke testen voor een order (zoals een inkoop- of productieorder) of voorraadhoeveelheid moeten worden uitgevoerd. U kunt een kwaliteitsorder handmatig maken of een kwaliteitsorder automatisch op basis van de kwaliteitsrichtlijnen laten genereren.
-   De kwaliteitsrichtlijnen met betrekking tot inkoop, quarantaine, productie of verkooporders in elk bedrijfsproces definiëren voor het automatisch genereren van een kwaliteitsorder waarin de testvereisten voor inkomend en uitgaand materiaal worden aangegeven.
-   De testresultaten in een kwaliteitsorder registreren, de testresultaten ten opzichte van de acceptabele kwaliteitsniveaus valideren en een analysecertificaat met de testresultaten afdrukken.

## <a name="nonconformance"></a>Non-conformiteit
Een non-conformering beschrijft een artikel met een kwaliteitsprobleem. Via het niet-conformeringsproces kunt u een non-conformeringsorder maken waarin een hoeveelheid niet-overeenkomende materialen wordt beschreven in termen van de bron van het probleem, het type probleem en begeleidende notities. U kunt een classificatie van probleemtypen definiëren om de analyse van niet-conformeringmateriaal te vergemakkelijken. U kunt een niet-conformeringslabel en een niet-conformeringsrapport ook afdrukken als richtlijn voor beschikking van niet-conformeringsmateriaal. Het label en rapport kunnen bijvoorbeeld de toestand **Onbruikbaar** of **Beperkt gebruik** aangeven.

De volgende tabel bevat de zes standaard niet-conformeringstypen en beschrijft de informatie die voor elk type moet worden geregistreerd.

| Non-conformiteitstype   | Brongegevens                                                                                                                                                                                                                          |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Klant              | Het klantrekeningnummer, verkoopordernummer of een partijnummer van een verkoopordertransactie. De niet-conformering kan bijvoorbeeld zijn gerelateerd aan een specifieke verkooporderzending of aan klantfeedback over de kwaliteit van een product.       |
| Serviceaanvraag       | Het klantrekeningnummer, verkoopordernummer of een partijnummer van een verkoopordertransactie. De niet-conformering kan bijvoorbeeld zijn gerelateerd aan een specifieke verkooporderzending of aan een klacht van een klant over de kwaliteit van een artikel.     |
| Leverancier                | Het leveranciersrekeningnummer, inkoopordernummer of een partijnummer van een inkoopordertransactie. De niet-conformering kan bijvoorbeeld zijn gerelateerd aan een inkooporderontvangst of aan de ontevredenheid van een leverancier over een geleverd onderdeel. |
| Productie            | Het productieordernummer of partijnummer van een productieordertransactie. De niet-conformering kan bijvoorbeeld zijn gerelateerd aan een specifieke batch die is geproduceerd.                                                                      |
| Intern              | Het kwaliteitsordernummer of partijnummer van een kwaliteitsordertransactie. De niet-conformering kan bijvoorbeeld zijn gerelateerd aan de testen die zijn uitgevoerd als onderdeel van een kwaliteitsorder of aan de twijfel van een werknemer over de kwaliteit van een product.     |
| Productie van coproducten | niet-conformering van de co-productproductieorder die is gerelateerd aan batchproductieorders.                                                                                                                                                    |

Niet-conformeringen worden gekoppeld aan een probleemtype. Probleemtypen worden gedefinieerd op de pagina **Probleemtypen**, waar u kunt instellen welke probleemtypen aan elk niet-conformeringstype kunnen worden gekoppeld. De probleemtypen voor niet-conformeringen van de **Serviceaanvraag** kunnen bijvoorbeeld een classificatie van klachten van klanten weerspiegelen, terwijl de probleemtypen voor een niet-conformeringen van het type **Intern**een classificatie van defectcodes kunnen vertegenwoordigen.

Wanneer u een nieuwe niet-conformering maak, selecteert u het niet-conformeringstype en probleemtype. De oorspronkelijke goedkeuringsstatus is **Nieuw**, wat een actieaanvraag vertegenwoordigt. De volgende stap is het wijzigen van de goedkeuringsstatus in **Goedgekeurd** of **Geweigerd** om aan te geven dat u al dan niet actie onderneemt voor de niet-conformering. U kunt een niet-conformering ook sluiten (door een afzonderlijk selectievakje te selecteren) om aan te geven dat u deze hebt voltooid, of u kunt een niet-conformering opnieuw openen om aan te geven dat verdere actie is vereist.

U kunt opmerkingen invoeren voor een niet-conformering door een document te koppelen. Het is daarom een goed idee om een uniek documenttype voor niet-conformeringen te definiëren door de pagina **Documenttype** te gebruiken. U kunt de pagina **Rapport instellen** gebruiken om te definiëren of opmerkingen voor dit documenttype moeten worden afgedrukt op het niet-conformeringsrapport en niet-conformeringslabel. Het niet-conformeringsrapport en niet-conformeringslabel zijn handig voor materiaalbeschikking. U kunt rapporten en labels genereren op basis van selectiecriteria, zoals het niet-conformeringsnummer, artikel, de klant, leverancier of status, die aan een niet-conformering zijn gekoppeld. Deze criteria omvatten het niet-conformeringsnummer, artikel, de klant, leverancier en status.

Het niet-conformeringsrapport geeft het niet-conformeringsnummer, artikel en probleemtype weer. Afhankelijk van uw rapportinstellingenbeleid kan het rapport ook gerelateerde notities over de niet-conformering weergeven. Het niet-conformeringlabel toont vergelijkbare informatie en omvat ook de quarantainezone en het type (zoals **Beperkt gebruik** of **Onbruikbaar**) die u hebt toegewezen aan de niet-conformering om de beschikking van het defecte materiaal te begeleiden.

## <a name="approved-nonconformance"></a>Goedgekeurde niet-conformering
U kunt desgewenst een of meer gerelateerde bewerkingen voor een goedgekeurde non-conformiteit definiëren. Een gerelateerde bewerking beschrijft het werk dat moet worden uitgevoerd en bevat een lijst van de kwaliteitsbewerkingen die u hebt gedefinieerd en de beschrijvende tekst over de reden voor het werk. Nadat u een bewerking hebt gedefinieerd, kunt u desgewenst de diverse kosten, artikelen en arbeidsuren definiëren die nodig zijn om het werk uit te voeren. De berekende kosten worden weergegeven voor de gerelateerde bewerking en de totale berekende kosten worden weergegeven voor de non-conformiteit. De berekende kosten en de bijbehorende details (over artikelen, arbeidsuren en diverse kosten) zijn referentiegegevens en worden alleen gebruikt in de functie voor kwaliteitsbeheer.

U kunt zo nodig een kwaliteitsorder maken voor een niet-conformering door eerst een aanvraag uit te voeren voor kwaliteitsorders en vervolgens de nieuwe kwaliteitsorder te maken. Met een kwaliteitsorder kan bijvoorbeeld worden aangegeven dat het defecte materiaal moet worden getest (of opnieuw moet worden getest). In de nieuwe kwaliteitsorder wordt de koppeling met de oorspronkelijke non-conformiteit aangegeven.

U kunt desgewenst niet-conformeringen aan elkaar koppelen of een nieuwe niet-conformering maken op basis van een bestaande niet-conformering. Met de koppeling kan bijvoorbeeld het verband tussen kwaliteitsproblemen worden aangegeven.

## <a name="correction-handling"></a>Afhandeling van correcties
Op de pagina **Correcties** kunt u een lijst van niet-conformeringen maken die moeten worden gecorrigeerd. Elk correctieartikel wordt gekoppeld aan het type diagnose waardoor het probleem werd gevonden. De pagina **Correcties** bevat ook informatie over wie een corrigerende actie moet uitvoeren en wanneer. U kunt de details van het probleem en de vereiste corrigerende actie beschrijven, door een document aan de correctie te koppelen. Nadat de niet-conformering is geadresseerd of gecorrigeerd, "sluit" u het correctieartikel door de optie **Voltooid** te selecteren. U kunt ook aangeven dat de oplossing een kortetermijnoplossing was.

Het is daarom een goed idee om een uniek documenttype voor correcties te definiëren door de pagina **Documenttype** te gebruiken. U kunt de pagina **Rapport instellen** gebruiken om te definiëren of opmerkingen voor dit documenttype moeten worden afgedrukt op het correctierapport. Op een afgedrukt correctierapport wordt informatie weergegeven over de niet-conformering en de gerelateerde niet-conformeringsnotities. Het rapport bevat ook correctiegegevens, zoals het type diagnose en de gerelateerde correctienotities.

<a name="additional-resources"></a>Aanvullende resources
--------

[Kwaliteitsbeheer inschakelen](enable-quality-management.md)

[Niet-conformeringsbeheer inschakelen](enable-nonconformance-management.md)

[Voorraadblokkering](inventory-blocking.md)

[Quarantaineorders](quarantine-orders.md)

[Kwaliteitsorders instellen (Taakbegeleiding)](tasks/set-up-quality-orders.md)

[De kwaliteit van goederen controleren (Taakbegeleiding)](tasks/inspect-quality-goods.md)
