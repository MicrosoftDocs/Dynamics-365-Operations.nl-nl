---
title: Over-/ondertransacties
description: Dit onderwerp bevat informatie die u zal helpen bij het instellen van beleidsregels voor over-/ondertransacties, zodat het systeem kan bepalen hoe moet worden omgegaan met de verwerking van te veel of te weinig goederen wanneer deze worden ontvangen.
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMOverUnderTrans, ITMOverUnderToleranceTable, ITMOverUnderReasonTable, ITMOverUnderToleranceGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: c7e75e39877b36e482dd4aaa5cc7c8f84d57d81b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833732"
---
# <a name="overunder-transactions"></a>Over-/ondertransacties

[!include [banner](../../includes/banner.md)]

Wanneer de orders in een reis worden verwerkt, verwacht het systeem dat de artikelhoeveelheid die is ontvangen in het uiteindelijke doelmagazijn voor verbruik overeenkomt met de hoeveelheid die is opgegeven op de inkooporderregels die aan de reis zijn gekoppeld. Aangezien de exacte hoeveelheid op de inkooporderregels echter niet altijd in het magazijn wordt ontvangen, definieert de module **Francoprijzen** een reeks regels die worden gebruikt voor het verwerken van te veel en te weinig ontvangen goederen. Deze regels zijn vooral belangrijk omdat de oorspronkelijke inkooporder is gefactureerd en niet meer kan worden gewijzigd. Door beleidsregels voor over-/ondertransacties in te stellen, zorgt u dat het systeem kan bepalen hoe moet worden omgegaan met de verwerking van te veel of te weinig goederen wanneer deze worden ontvangen. U kunt ook handmatig over- en ondervoorraad beheren met de pagina **Over-/ondertransacties**.

## <a name="overunder-tolerances"></a>Over-/ondertoleranties

U stelt toleranties instellen voor te veel en te weinig ontvangen goederen om de over- en onderhoeveelheden of -volumes op te geven die op een reis kunnen worden verwerkt zonder dat er een fout wordt veroorzaakt. Als de reisregelontvangst buiten deze toleranties valt, moet deze worden gewijzigd en opgelost voordat de ontvangstregel kan worden gesloten voor verdere verwerking.

Als u de toleranties wilt configureren, gaat u naar **Francoprijzen \> Instellingen voor over-/onder \> Over-/ondertoleranties**. Daar kunt u tolerantierecords weergeven, bewerken, toevoegen en verwijderen. In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke record.

| Veld | Beschrijving |
|---|---|
| Rekeningcode | <p>Definieer het bereik van leveranciers op wie de tolerantie van toepassing is door een van de volgende waarden te selecteren:</p><ul><li>**Tabel**: de over-/ondertolerantie is alleen van toepassing op de leverancier die voor de rij is geselecteerd.</li><li>**Groep**: de over-/ondertolerantie is van toepassing op alle leveranciers in de leverancierstolerantiegroep die voor de rij is geselecteerd.</li><li>**Alle**: het over-/ondertolerantiepercentage wordt op alle leveranciers toegepast.</li></ul> |
| Rekeningrelatie | Selecteer de leverancier of leveranciersgroep waarop de over-/ondertolerantie van toepassing is, afhankelijk van de waarde die u hebt geselecteerd in het veld **Rekeningcode**. |
| Artikelcode | <p>Definieer het bereik van artikelen op wie de tolerantie van toepassing is door een van de volgende waarden te selecteren:</p><ul><li>**Tabel**: de over-/ondertolerantie is alleen van toepassing op het artikel dat voor de rij is geselecteerd.</li><li>**Groep**: de over-/ondertolerantie is van toepassing op alle artikelen in de artikeltolerantiegroep die voor de rij is geselecteerd.</li><li>**Alle**: het over-/ondertolerantiepercentage wordt op alle artikelen toegepast.</li></ul> |
| Artikelrelatie | Selecteer het artikel of de artikelgroep waarop de over-/ondertolerantie van toepassing is, afhankelijk van de waarde die u hebt geselecteerd in het veld **Artikelcode**. |
| Bedragtolerantie | Voer de hoeveelheidstolerantie in die op een gehele inkooporder moet worden toegepast. |
| Percentagetolerantie | Voer de percentagetolerantie in die op een afzonderlijke inkooporderregel moet worden toegepast. |

## <a name="overunder-reasons"></a>Over-/onderredenen

Wanneer een onder- of overhoeveelheid is gekoppeld aan een reisregel die is ontvangen, moet u mogelijk de reden voor de over- of onderhoeveelheid aangeven. In dit geval kunt u de reden voor te veel of te weinig geleverd op de ontvangstregel selecteren wanneer de goederen worden ontvangen.

Als u redenen voor over- en onderleveringen wilt instellen, gaat u naar **Francoprijzen \> Instellingen voor over-/onder \> Redenen voor over-/onder**. Hier kunt u de beschikbare redenen voor te veel en te weinig geleverd weergeven, bewerken, toevoegen en verwijderen. In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke reden.

| Veld | Beschrijving |
|---|---|
| Over-/onderreden | Voer een unieke naam invoeren voor de reden voor de over- of ondertransactie. |
| Beschrijving | Voer een beschrijving van de over-/onderredencode in. |
| Mutatie | Selecteer het mutatiejournaal dat is gekoppeld aan de over-/onderreden. Dit veld bevat alle beschikbare journalen waar het journaaltype *Mutatie* aan is gekoppeld op de pagina **Voorraadjournaalnamen** (**Voorraadbeheer instellen \> Journaalnamen \> Voorraad**). |

## <a name="item-overunder-tolerance-groups"></a>Over-/ondertolerantiegroepen voor artikelen

Artikelen met vergelijkbare toleranties kunnen worden gegroepeerd. Op deze manier kunt u de over-/ondertolerantie voor alle artikelen in die groep tegelijk instellen.

Als u Tolerantiegroepen voor te veel of te weinig geleverde artikelen wilt instellen, gaat u naar **Francoprijzen \> Instellingen voor over-/onder \> Over-/ondertolerantiegroepen voor artikelen**. Daar kunt u records voor over-/ondertolerantiegroepen weergeven, bewerken, toevoegen en verwijderen. In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke record.

| Veld | Beschrijving |
|---|---|
| Over-/ondertolerantiegroep | Voer een unieke naam voor de groep in. Kies een naam die de tolerantie omschrijft, bijvoorbeeld *1% var.*. |
| Beschrijving | Voer een omschrijving in van de groep. |

## <a name="vendor-overunder-tolerance-groups"></a>Over-/ondertolerantiegroepen voor leveranciers

U kunt leveranciers die regelmatig te veel of te weinig leveren groeperen. Vervolgens kunt u de over-/ondertolerantie per groep instellen.

Als u Tolerantiegroepen voor te veel of te weinig leverende leveranciers wilt instellen, gaat u naar **Francoprijzen \> Instellingen voor over-/onder \> Over-/ondertolerantiegroepen voor leveranciers**. Daar kunt u records voor over-/ondertolerantiegroepen weergeven, bewerken, toevoegen en verwijderen. In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke record.

| Veld | Beschrijving |
|---|---|
| Over-/ondergroepen | Voer een unieke naam voor de groep in. Kies een naam die het type leveranciers beschrijft dat bij de groep hoort. |
| Beschrijving | Voer een omschrijving in van de groep. |

## <a name="view-and-process-overunder-transactions"></a>Over-/ondertransacties weergeven en verwerken

Over- en ondertransacties worden gegenereerd wanneer de hoeveelheid goederen die wordt weggezet, niet gelijk is aan de geïnitialiseerde hoeveelheid. De hoeveelheid in het ontvangstjournaal moet alleen worden bijgewerkt met de hoeveelheid die is weggezet.

Wanneer de ontvangst van reisregels wordt verwerkt, kunnen er over-/ondertoleranties worden ingesteld voor een leverancier. De artikelen worden vervolgens gecontroleerd en gevalideerd. De tolerantie kan worden ingesteld als een percentage, een lokale hoeveelheid of beide.

Als een ontvangen artikel binnen de tolerantie valt, wordt een mutatiejournaal gegenereerd. U kunt dit journaal opgeven op de pagina met reisparameters. Bovendien wordt een over-/ondertransactie gemaakt. De orderwaarde is bijvoorbeeld niet € 100, de ontvangstwaarde is € 99 en deze waarden voldoen aan de tolerantieregels. In dit geval wordt een negatief mutatiejournaal voor de minder ontvangen hoeveelheid gemaakt.

Als een artikel dat wordt ontvangen buiten de tolerantie valt, wordt een over-/ondertransactie gegenereerd voor het hoeveelheidsverschil.

Als u over-/ondertransacties wilt weergeven en verwerken, gaat u naar **Francoprijzen \> Query's \> Over-/ondertransacties**. Daar wordt een over-/ondertransactie gekoppeld aan alle artikelen in een reis waarvan te veel of te weinig zijn ontvangen. We raden u aan om de pagina **Over-/ondertransacties** te gebruiken om alle over-/ondertransacties op te lossen die aan reizen zijn gekoppeld. Het is ook raadzaam om **geen** mutatie- of tellingsjournalen te gebruiken om magazijntransacties met een onderlevering handmatig op te lossen. In plaats daarvan moet u de pagina **Over-/ondertransacties** gebruiken om de magazijnhoeveelheden voor onderleveringen te beheren.

### <a name="upper-overview-tab"></a>Bovenste tabblad Overzicht

Als u over-/ondertransacties wilt weergeven, selecteert u het tabblad **Overzicht** in het bovenste gedeelte van de pagina **Over-/ondertransacties**. In de volgende tabel worden de velden beschreven die in het raster beschikbaar zijn.

| Veld | Beschrijving |
|---|---|
| Over-/ondertransactienummer | De unieke naam van de over-/ondertransactierecord die automatisch werd gemaakt toen het ontvangstjournaal werd verwerkt. |
| Reis | De reis waar de inkoopregel aan was gekoppeld. |
| Verzendcontainer | De container waar de inkoopregel aan was gekoppeld. |
| Ontvangstjournaal | Het ontvangstjournaal waaruit de over-/onderregel is gegenereerd. |
| Verwijzing | Een verwijzing naar de inkooporder of de overboekingsorder die aan de over-/ondertransactie is gekoppeld. |
| Nummer | De inkooporder waarnaar in de over-/ondertransactie wordt verwezen. |
| Leverancier | De leverancier waar de over- of onderinformatie betrekking op heeft. |
| Nummer van goederen in transit | Het nummer van de goederen in transit, indien van toepassing. |
| artikelnummer | Het artikelnummer waar de over- of onderinformatie betrekking op heeft. |
| Oorspronkelijke hoeveelheid | De oorspronkelijke hoeveelheid van de inkooporderregel die aan de zending is gekoppeld. |
| Ontvangen hoeveelheid | De werkelijk ontvangen hoeveelheid. |
| Verschil | Het verschil tussen de verwachte ontvangstjournaalhoeveelheid en de hoeveelheid die in het ontvangstjournaal is geboekt. Een negatieve waarde geeft te veel geleverde goederen aan. |
| Resterende hoeveelheid | De hoeveelheid die overblijft op de ontvangstjournaalregel. |
| Meer-/minderlevering | Een waarde die aangeeft of de ontvangen hoeveelheid een over- of een onderhoeveelheid is. |
| Status | De status van de over-/ondertransactie. Afhankelijk van de instellingen op de pagina **[Francoprijsparameters](landed-cost-parameters.md)** kan er automatisch een mutatiejournaal voor de te veel geleverde hoeveelheid worden gemaakt en het journaal worden geboekt. In dit geval heeft de over-/ondertransactie de status *Voltooid*. Als een actie is vereist om de goederen uit het onderleveringsmagazijn te muteren, heeft de record de status *Onderhanden*. |
| Over-/onderreden | De reden die is gekoppeld aan de over-/ondertransactie. |
| Overige voorraaddimensies | U kunt indien nodig kolommen voor extra dimensies in het raster weergeven. Deze dimensies zijn batchnummer, voorraadstatus en magazijn. Selecteer in het actievenster de optie **Voorraad \> Dimensies weergeven** om een dialoogvenster te openen waarin u de dimensies kunt selecteren die u wilt opnemen. |

### <a name="upper-general-tab"></a>Bovenste tabblad Algemeen

Als u meer informatie wilt weergeven over de regel die op het bovenste tabblad **Overzicht** is geselecteerd, selecteert u het tabblad **Algemeen** in het bovenste gedeelte van de pagina **Over-/onder transacties**. De informatie op dit tabblad bevat de waarden voor alle beschikbare dimensies. Deze informatie wordt gehaald uit de oorspronkelijke inkooporder.

### <a name="lower-overview-tab"></a>Onderste tabblad Overzicht

Als u het documenttype wilt weergeven voor de rij die op het bovenste tabblad **Overzicht** is geselecteerd, selecteert u het tabblad **Overzicht** in het onderste gedeelte van de pagina **Over-/onder transacties**. In de volgende tabel worden de velden beschreven die beschikbaar zijn.

| Veld | Beschrijving |
|---|---|
| Nieuw documenttype | Dit veld is ingesteld op *Verplaatsingsjournaal* of *Inkooporder*, afhankelijk van de actie die wordt weergegeven op de geselecteerde over-/ondertransactieregel. |
| Nummer | Een verwijzing en koppeling naar de inkooporder of het mutatiejournaal dat aan de geselecteerde over-/ondertransactieregel is gekoppeld. |
| Over-/onderreden | De reden die is gekoppeld aan de geselecteerde over-/ondertransactieregel. |
| Hoeveelheid | De hoeveelheid die u hebt geselecteerd voor de inkooporder of het mutatiejournaal dat aan de geselecteerde over-/ondertransactieregel is gekoppeld. |

### <a name="lower-general-tab"></a>Onderste tabblad Algemeen

Als u het over-/ondertransactienummer, de partij-ID en het dimensienummer wilt weergeven die zijn gekoppeld aan de geselecteerde over-/ondertransactieregel, selecteert u het tabblad **Algemeen** onderaan de pagina **Over-/ondertransacties**. 

### <a name="process-overunder-transactions"></a>Over-/ondertransacties verwerken

Het actievenster op de pagina **Over-/onder transacties** bevat de volgende opdrachten voor het verwerken van de transacties die op de pagina zijn geselecteerd. Met elke opdracht kunt u kiezen hoe elke transactie moet worden verwerkt.

- **Maken \> Mutatie**: mutatiejournaal voor de geselecteerde transactie maken en boeken. Voor ondertransacties wordt automatisch een mutatiejournaal gemaakt en geboekt voor het verschil tussen de verwachte en de werkelijk ontvangen hoeveelheid. Selecteer deze opdracht voor overtransacties als u wilt dat de leverancier het kostenverschil realiseert.
- **Maken \> Inkooporder**: een inkooporder maken voor het verschil tussen de verwachte en de werkelijk ontvangen hoeveelheid van de geselecteerde transactie. Selecteer deze opdracht voor overtransacties als uw organisatie het kostenverschil zal realiseren.
- **Maken \> Transfer naar bestemming**: deze opdracht geldt alleen voor overboekingsorders. Selecteer deze opdracht als u de over- of onderhoeveelheid naar het doelmagazijn wilt over brengen.
- **Maken \> Transfer naar oorsprong**: deze opdracht geldt alleen voor overboekingsorders. Selecteer deze opdracht als u de over- of onderhoeveelheid naar het magazijn van herkomst wilt over brengen.
