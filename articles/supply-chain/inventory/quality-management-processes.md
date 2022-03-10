---
title: Overzicht van het beheer van kwaliteit en niet-conformeringen
description: In dit onderwerp worden de functies voor kwaliteits- en niet-conformeringsbeheer in Microsoft Dynamics 365 Supply Chain Management beschreven en wordt uitgelegd hoe u hiermee de productkwaliteit in uw toeleveringsketen kunt verbeteren.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling, InventNonConformanceHistory, InventNonConformanceTable, InventQualityOrderLineResults, InventQualityOrderTable, InventTestCorrection, InventTestDiagnosticType, InventTestInstrument, InventTestReportSetup, InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "11574"
- intro-internal
ms.assetid: 5ac8a059-5cb4-4cb5-ba14-b944bd08dae9
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1bb4bcb7f554c22b4e1ab1b41867bd2d3dcca4d4
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985504"
---
# <a name="quality-and-nonconformance-management-overview"></a>Overzicht van het beheer van kwaliteit en niet-conformeringen

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de functies voor kwaliteits- en niet-conformeringsbeheer in Microsoft Dynamics 365 Supply Chain Management beschreven en wordt uitgelegd hoe u hiermee de productkwaliteit in uw toeleveringsketen kunt verbeteren.

Kwaliteitscontrole omvat het testen van producten en het beheren van materialen die niet overeenkomen. Kwaliteitsbeheerprocessen helpen om een hoog productkwaliteitsniveau in uw leveringsketen te garanderen. Deze processen helpen om de leveringsketenprocessen te optimaliseren en klanttevredenheid te verhogen. Kwaliteitsbeheer kan u helpen keerpunttijden te beheren wanneer u te maken hebt met niet-overeenkomende producten, ongeacht punt van oorsprong van deze producten. U kunt diagnoseresultaten koppelen aan correctietaken. Het systeem kan taken inplannen om problemen te corrigeren, en zo helpen voorkomen dat deze problemen zich in de toekomst opnieuw voordoen. Met kwaliteitsbeheer ook kunt u problemen (inclusief interne problemen) volgen op probleemtype en oplossingen identificeren als korte-termijnoplossingen of lange-termijnoplossingen. De statistieken over Key Performance Indicators (KPI's) bevatten inzicht in niet-conformeringsproblemen die eerder zijn opgetreden en de oplossingen die zijn toegepast om ze te corrigeren. U kunt de historische gegevens gebruiken om de efficiëntie van kwaliteitsmetingen te controleren die eerder zijn genomen en overeenkomende stappen in de toekomst te definiëren.

Kwaliteitsbeheer kan u helpen keerpunttijden te beheren wanneer u te maken hebt met niet-overeenkomende producten, ongeacht hun punt van oorsprong. Omdat typen diagnoses aan correctierapportage zijn gekoppeld, kan Supply Chain Management taken plannen om problemen te corrigeren en te voorkomen dat deze worden herhaald.

Naast functionaliteit voor het beheer van niet-conformering omvat het kwaliteitsbeheer functionaliteit voor het bijhouden van problemen op probleemtype (zelfs wanneer het om interne problemen gaat) en om oplossingen als kortetermijn- of langetermijnoplossingen te identificeren. De statistieken over Key Performance Indicators (KPI´s) bieden inzicht in de geschiedenis van eerdere niet-conformeringsproblemen en de oplossingen die zijn gebruikt om ze te corrigeren. U kunt de historische gegevens gebruiken om de efficiëntie van eerdere kwaliteitsmetingen te controleren en passende stappen voor de toekomst te definiëren.

Wanneer u een kwaliteitskoppeling opzet, kan Supply Chain Management kwaliteitsorders genereren voor verschillende bedrijfsprocessen, gebeurtenissen en voorwaarden. De kwaliteitskoppeling kan betrekking hebben op een specifiek artikel, een specifieke groep artikelen of alle artikelen.

## <a name="examples-of-the-use-of-quality-management"></a>Voorbeelden van het gebruik van kwaliteitsbeheer

Kwaliteitsbeheer is flexibel en kan op verschillende manieren worden geïmplementeerd om aan de vereisten van specifieke niveaus van toeleveringsactiviteiten te voldoen. In de volgende voorbeelden worden mogelijke toepassingen van deze functies beschreven:

- Start automatisch een kwaliteitscontroleproces op basis van vooraf gedefinieerde criteria (bijvoorbeeld bij magazijnregistratie van een inkooporder van een specifieke leverancier).
- Blokkeer voorraad tijdens inspectie om te voorkomen dat niet-goedgekeurde voorraad wordt gebruikt (volledig blokkeren van inkooporderhoeveelheden).
- Gebruik artikelbemonstering als onderdeel van een kwaliteitskoppeling om te definiëren hoeveel fysieke actuele voorraad moet worden geïnspecteerd. Bemonstering kan worden gebaseerd op een vaste hoeveelheid, een percentage of een volledige nummerplaat.
- Maak kwaliteitsorders voor gedeeltelijke ontvangsten. Als u een kwaliteitsorder wilt maken die is gebaseerd op de hoeveelheid die fysiek is ontvangen met een order, moet u het selectievakje **Per bijgewerkte hoeveelheid** op de pagina **Artikelbemonstering** inschakelen.
- Maak testtypen die minimum-, maximum- en doeltestwaarden bevatten en voer vergelijkende kwalitatieve en kwantitatieve testen met vooraf gedefinieerde validatieresultaten uit.
- Geef een acceptabel kwaliteitsniveau op om kwaliteitsmetingstoleranties te beheren.
- Geef op welke resources een inspectiebewerking nodig hebben, zoals een testgebied en testinstrumenten.

> [!NOTE]
> De functie _Kwaliteitsbeheer voor magazijnprocessen_ vergroot de mogelijkheden van kwaliteitsbeheer. Als u deze functie gebruikt, raadpleegt u [Kwaliteitsbeheer voor magazijnprocessen](quality-management-for-warehouses-processes.md) voor voorbeelden van hoe kwaliteitsbeheer werkt wanneer deze optie is ingeschakeld.

## <a name="controlling-the-quality-management-process"></a>Het kwaliteitsbeheerproces controleren

Hieronder staan enkele manieren waarop u het kwaliteitsbeheerproces kunt controleren:

- Maak kwaliteitsorders die zijn gebaseerd op triggerpunten, zoals 'bij productontvangst' voor inkomende bewerkingen of 'bij ophalen product' voor uitgaande bewerkingen.
- Documenteer testresultaten en bepaal of de resultaten voldoen aan de vastgestelde testcriteria en acceptabele kwaliteitsniveaus.
- Gebruik documentbeheer voor gedetailleerde productspecificaties en gebruikerspecifieke notities als onderdeel van rapportage tijdens het inspectieproces.
- Beheer niet-overeenkomende producten en stem die producten af met aanvullende niet-conformeringsinformatie om de oorspronkelijke oorzaak van een probleem op te sporen.
- Documenteer de kosten om een niet-conformering te beheren. Deze kosten kunnen bestaan uit de artikelen (zoals reserveonderdelen), diverse kosten en de arbeidsuren die nodig zijn om de niet-conformering te corrigeren.
- Plan foutcorrectieprocessen door gebruik te maken van correctieafhandeling die is gekoppeld aan kwaliteitsorders.

[![Proces voor kwaliteitsbeheer.](media/quality-management-process-diagram.png)](media/quality-management-process-diagram.png)

## <a name="product-testing-and-quality-orders"></a>Producten testen en kwaliteitsorders

Het testen van producten wordt doorgaans geschaard onder kwaliteitscontroles en brengt het gebruik van kwaliteitsorders met zich mee. Met de functionaliteit voor kwaliteitscontrole kunt u het volgende doen:

- Bepalen welke tests voor materiaal moeten worden uitgevoerd. Tot deze tests behoren de kwaliteitsspecificaties, het desbetreffende testprogramma, de documenten waarin de test wordt beschreven, een bemonsteringsplan en de acceptabele kwaliteitsniveaus.
- Een kwaliteitsorder maken waarin wordt aangegeven welke testen voor een order (zoals een inkoop- of productieorder) of voorraadhoeveelheid moeten worden uitgevoerd. U kunt handmatig een kwaliteitsorder maken of een kwaliteitsorder automatisch op basis van de kwaliteitsrichtlijnen laten genereren.
- Definieer de kwaliteitsrichtlijnen met betrekking tot inkoop, quarantaine, productie of verkooporders in elk bedrijfsproces, zodat er automatisch een kwaliteitsorder kan worden gegenereerd waarin de testvereisten voor inkomend en uitgaand materiaal worden aangegeven.
- Leg de testresultaten in een kwaliteitsorder vast, valideer de testresultaten ten opzichte van de acceptabele kwaliteitsniveaus en druk een analysecertificaat met de testresultaten af.

## <a name="nonconformance"></a>Niet-conformering

Een niet-conformering beschrijft een artikel met een kwaliteitsprobleem. Via het niet-conformeringsproces kunt u een niet-conformeringsorder maken waarin een hoeveelheid niet-overeenkomende materialen wordt beschreven in termen van de bron van het probleem, het type probleem en begeleidende notities. U kunt een classificatie van probleemtypen definiëren om de analyse van niet-conformeringmateriaal te vergemakkelijken. U kunt een niet-conformeringslabel en een niet-conformeringsrapport ook afdrukken als richtlijn voor beschikking van niet-conformeringsmateriaal. Het label en rapport kunnen bijvoorbeeld de toestand **Onbruikbaar** of **Beperkt gebruik** aangeven.

De volgende tabel bevat de zes standaard niet-conformeringstypen en beschrijft de informatie die voor elk type moet worden geregistreerd.

| Niet-conformeringstype | Brongegevens |
|---|---|
| Klant | Het klantrekeningnummer, verkoopordernummer of een partijnummer van een verkoopordertransactie. De niet-conformering kan bijvoorbeeld zijn gerelateerd aan een specifieke verkooporderzending of aan klantfeedback over de kwaliteit van een product. |
| Serviceaanvraag | Het klantrekeningnummer, verkoopordernummer of een partijnummer van een verkoopordertransactie. De niet-conformering kan bijvoorbeeld zijn gerelateerd aan een specifieke verkooporderzending of aan een klacht van een klant over de kwaliteit van een artikel. |
| Leverancier | Het leveranciersrekeningnummer, inkoopordernummer of een partijnummer van een inkoopordertransactie. De niet-conformering kan bijvoorbeeld zijn gerelateerd aan een inkooporderontvangst of aan de ontevredenheid van een leverancier over een geleverd onderdeel. |
| Productie | Het productieordernummer of partijnummer van een productieordertransactie. De niet-conformering kan bijvoorbeeld zijn gerelateerd aan een specifieke batch die is geproduceerd. |
| Intern | Het kwaliteitsordernummer of partijnummer van een kwaliteitsordertransactie. De niet-conformering kan bijvoorbeeld zijn gerelateerd aan de testen die zijn uitgevoerd als onderdeel van een kwaliteitsorder of aan de twijfel van een werknemer over de kwaliteit van een product. |
| Productie van coproducten | niet-conformering van de co-productproductieorder die is gerelateerd aan batchproductieorders. |

Niet-conformeringen worden gekoppeld aan een probleemtype. Probleemtypen worden gedefinieerd op de pagina **Probleemtypen**, waar u kunt instellen welke probleemtypen aan elk niet-conformeringstype kunnen worden gekoppeld. De probleemtypen voor niet-conformeringen van het type **Serviceaanvraag** kunnen bijvoorbeeld een classificatie van klachten van klanten weerspiegelen, terwijl de probleemtypen voor niet-conformeringen van het type **Intern** een classificatie van defectcodes kunnen vertegenwoordigen.

Wanneer u een nieuwe niet-conformering maak, selecteert u het niet-conformeringstype en probleemtype. De oorspronkelijke goedkeuringsstatus is **Nieuw**, wat een actieaanvraag vertegenwoordigt. De volgende stap is het wijzigen van de goedkeuringsstatus in **Goedgekeurd** of **Geweigerd** om aan te geven dat u al dan niet actie onderneemt voor de niet-conformering. U kunt een niet-conformering ook sluiten (door een afzonderlijk selectievakje te selecteren) om aan te geven dat u deze hebt voltooid, of u kunt een niet-conformering opnieuw openen om aan te geven dat verdere actie is vereist.

U kunt opmerkingen invoeren voor een niet-conformering door een document te koppelen. Het is daarom een goed idee om een uniek documenttype voor niet-conformeringen te definiëren door de pagina **Documenttype** te gebruiken. U kunt de pagina **Rapport instellen** gebruiken om te definiëren of opmerkingen voor dit documenttype moeten worden afgedrukt op het niet-conformeringsrapport en niet-conformeringslabel. Het niet-conformeringsrapport en niet-conformeringslabel zijn handig voor materiaalbeschikking. U kunt rapporten en labels genereren op basis van selectiecriteria, zoals het niet-conformeringsnummer, artikel, de klant, leverancier of status, die aan een niet-conformering zijn gekoppeld. Deze criteria omvatten het niet-conformeringsnummer, artikel, de klant, leverancier en status.

Het niet-conformeringsrapport geeft het niet-conformeringsnummer, artikel en probleemtype weer. Afhankelijk van uw rapportinstellingenbeleid kan het rapport ook gerelateerde notities over de niet-conformering weergeven. Het niet-conformeringlabel toont vergelijkbare informatie en omvat ook de quarantainezone en het type (zoals **Beperkt gebruik** of **Onbruikbaar**) die u hebt toegewezen aan de niet-conformering om de beschikking van het defecte materiaal te begeleiden.

## <a name="approved-nonconformance"></a>Goedgekeurde niet-conformering

U kunt desgewenst een of meer gerelateerde bewerkingen voor een goedgekeurde niet-conformering definiëren. Een gerelateerde bewerking beschrijft het werk dat moet worden uitgevoerd en bevat een lijst van de kwaliteitsbewerkingen die u hebt gedefinieerd en de beschrijvende tekst over de reden voor het werk. Nadat u een bewerking hebt gedefinieerd, kunt u desgewenst de diverse kosten, artikelen en arbeidsuren definiëren die nodig zijn om het werk uit te voeren. De berekende kosten worden weergegeven voor de gerelateerde bewerking en de totale berekende kosten worden weergegeven voor de niet-conformering. De berekende kosten en de bijbehorende details (over artikelen, arbeidsuren en diverse kosten) zijn referentiegegevens en worden alleen gebruikt in de functie voor kwaliteitsbeheer.

U kunt zo nodig een kwaliteitsorder maken voor een niet-conformering door eerst een aanvraag uit te voeren voor kwaliteitsorders en vervolgens de nieuwe kwaliteitsorder te maken. Met een kwaliteitsorder kan bijvoorbeeld worden aangegeven dat het defecte materiaal moet worden getest (of opnieuw moet worden getest). In de nieuwe kwaliteitsorder wordt de koppeling met de oorspronkelijke niet-conformering aangegeven.

U kunt desgewenst niet-conformeringen aan elkaar koppelen of een nieuwe niet-conformering maken op basis van een bestaande niet-conformering. Met de koppeling kan bijvoorbeeld het verband tussen kwaliteitsproblemen worden aangegeven.

## <a name="correction-handling"></a>Afhandeling van correcties

Op de pagina **Correcties** kunt u een lijst van niet-conformeringen maken die moeten worden gecorrigeerd. Elk correctieartikel wordt gekoppeld aan het type diagnose waardoor het probleem werd gevonden. De pagina **Correcties** bevat ook informatie over wie een corrigerende actie moet uitvoeren en wanneer. U kunt de details van het probleem en de vereiste corrigerende actie beschrijven, door een document aan de correctie te koppelen. Nadat de niet-conformering is geadresseerd of gecorrigeerd, "sluit" u het correctieartikel door de optie **Voltooid** te selecteren. U kunt ook aangeven dat de oplossing een kortetermijnoplossing was.

Het is daarom een goed idee om een uniek documenttype voor correcties te definiëren door de pagina **Documenttype** te gebruiken. U kunt de pagina **Rapport instellen** gebruiken om te definiëren of opmerkingen voor dit documenttype moeten worden afgedrukt op het correctierapport. Op een afgedrukt correctierapport wordt informatie weergegeven over de niet-conformering en de gerelateerde niet-conformeringsnotities. Het rapport bevat ook correctiegegevens, zoals het type diagnose en de gerelateerde correctienotities.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Beheer van kwaliteit en niet-conformeringen inschakelen](enable-quality-management.md)
- [Voorraadblokkering](inventory-blocking.md)
- [Quarantaineorders](quarantine-orders.md)
- [De kwaliteit van goederen inspecteren](tasks/inspect-quality-goods.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
