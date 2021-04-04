---
title: containers beheren
description: In dit onderwerp wordt beschreven hoe u met containers werkt. containers worden gebruikt om goederen te groeperen die fysiek zijn gegroepeerd. Ze worden ook gebruikt wanneer kosten alleen over deze goederen moeten worden gedeeld, meestal omdat ze fysiek zijn gegroepeerd.
author: sherry-zheng
manager: tfehr
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: e75deb5f4acd647408e93957bb99f04f548108f6
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501337"
---
# <a name="manage-shipping-containers"></a>containers beheren

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

containers worden gebruikt om goederen te groeperen die fysiek zijn gegroepeerd. Ze worden ook gebruikt wanneer kosten alleen over deze goederen moeten worden gedeeld, meestal omdat ze fysiek zijn gegroepeerd.

Als u goederen wilt weergeven en verwerken via de pagina voor containers, gaat u naar **Francoprijzen \> containers \> Alle containers**. Op de pagina **Alle containers** wordt een lijst weergegeven met alle beschikbare containers. U kunt de knoppen in het actievenster gebruiken om containers te maken, te verwijderen en met containers te werken. Selecteer een container in de lijst om de details van de container weer te geven op de pagina **containers**.

In het bovenste gedeelte van de pagina met gegevens over de container worden de container en de informatie over kostprijsberekening weergegeven. In de sectie **Regels** worden de folio's, artikelen en inkooporders of transferorders weergegeven die aan de container zijn gekoppeld.

## <a name="action-pane"></a>Actievenster

Het actievenster van de pagina's **Alle containers** en **containers** bevat knoppen waarmee u met een geselecteerde container kunt werken. Met elke knop voert u één actie uit. Het actievenster bevat ook tabbladen die elk op hun beurt een reeks verwante knoppen bieden. Behalve daar waar aangegeven, zijn alle knoppen en tabbladen die in de volgende subsecties worden beschreven, beschikbaar in de lijstweergave (dat wil zeggen op de pagina **Alle container**) en in de gedetailleerde weergave (dat wil zeggen op de pagina **containers**).

### <a name="buttons-on-the-manage-tab"></a>Knoppen op het tabblad Beheren

In de volgende tabel worden de knoppen beschreven die op het tabblad **Beheren** van het actievenster beschikbaar zijn.

| Knop | Omschrijvingen |
|---|---|
| Ontvangstlijst boeken | Boek een ontvangstlijst of bekijk de productontvangstlijst voor alle inkooporderregels in de container. Als er zendingen naar meerdere bedrijven worden gebruikt, wordt er een nieuw dialoogvenster voor het boeken van een ontvangstlijst geopend voor elk bedrijf. |
| Productontvangstbon boeken | Boek een productontvangst voor alle inkooporderregels in de container. |
| Factuur boeken | Boek een factuur voor alle inkooporderregels in de container. Als er zendingen naar meerdere bedrijven worden gebruikt, wordt er een nieuw dialoogvenster voor het boeken van facturen geopend voor elk bedrijf. |
| Verzenden transferorders | Boek een transferorderzending voor alle transferorderregels in de container. Alleen de regels in de container van het type transferorder worden in het dialoogvenster weergegeven. |
| Transferorder ontvangen | Boek een transferorderontvangst voor alle transferorderregels in de container. Goederen in een container of transport kunt u het eenvoudigst ontvangen in het dialoogvenster Ontvangen en is een van de drie beschikbare opties. U kunt ook goederen ontvangen via ontvangstjournaals of verwerking via mobiele apparaten. |
| Ontvangstjournaal maken | U kunt een ontvangstjournaal genereren voor organisaties met behulp van geavanceerde magazijnfuncties. De opties zijn _Hoeveelheid initialiseren_ (aanbevolen) en _Maken van goederen in transit_ of _Maken op basis van inkooporders_. De laatste twee opties zijn afhankelijk van of de verwerking van goederen in transit wordt gebruikt. |
| Naam wijzigen | Open een dialoogvenster waarin u de naam van een geselecteerde container kunt wijzigen. |
| Trajectsjabloon wijzigen | Wijzig de trajectsjabloon. Nadat u de trajectsjabloon hebt gewijzigd, moet u mogelijk opnieuw de optie **Automatische kosten zoeken** selecteren of handmatig weer kosten toevoegen, omdat de verzendkosten worden verwijderd. |
| Converteren naar verhuur | Zet een geselecteerde container om in een huurcontainer voor verzending. |

### <a name="buttons-on-the-general-tab"></a>Knoppen op het tabblad Algemeen

In de volgende tabel worden de knoppen beschreven die op het tabblad **Algemeen** van het actievenster beschikbaar zijn.

| Knop | Omschrijvingen |
|---|---|
| Ontvangstlijst | Boek een ontvangstlijst voor alle inkooporderregels in de container. Als er transporten naar meerdere bedrijven worden gebruikt, wordt er een nieuw dialoogvenster voor het boeken van ontvangstlijsten geopend voor elk bedrijf. |
| Productontvangst | Bekijk de productontvangstrecord als deze wordt gebruikt. Het proces voor productontvangsten wordt alleen gebruikt als voor de goederen niet de functionaliteit goederen in transit wordt gebruikt. |
| Artikelontvangst | Bekijk het artikelontvangstjournaal voor de container, als dat journaal wordt gebruikt. |
| Etappes | Etappes worden gebruikt om afzonderlijke delen van een traject te identificeren. Aan elke etappe kunnen doorlooptijden worden gekoppeld om zendingen beter te kunnen traceren. Zie [Instellen van trajecten met meerdere etappes](multi-leg-journey-setup.md) voor meer informatie. |
| Tracering | Bekijk de tracering van zendingen of werk ze bij. |
| Orders voor goederen in transit | U kunt de pagina **Goederen in transit** rechtstreeks vanuit de container openen. Op deze pagina worden alleen de records voor goederen in transit voor de geselecteerde container weergegeven. |

## <a name="header-view"></a>Weergave headers

Als u de weergave **Header** wilt openen, opent u een container en selecteert u vervolgens het tabblad **Header** in de rechterbovenhoek van de header van de container.

### <a name="settings-on-the-general-fasttab"></a>Instellingen op het sneltabblad Algemeen

In de volgende tabel worden de instellingen beschreven die beschikbaar zijn op het sneltabblad **Algemeen** van de weergave **Header** van een container.

| Veld | Beschrijving |
|---|---|
| container | De naam van de container. |
| Reis | De reis die aan de container is gekoppeld. |
| Type container | Voer het type container in. Dit veld moet worden ingesteld. U kunt het veld gebruiken om bijvoorbeeld de vrachtkosten bepalen door de automatische kosten te selecteren die zijn gekoppeld aan het type container. |
| Vaartuig | Voer een vaartuig in of selecteer een vaartuig. Als het vaartuig niet als waarde wordt vermeld, kunt u de vaartuig-id als vrije tekst invoeren. In dat geval wordt de hoofdtabel niet bijgewerkt, zodat de vaartuig-id later in dit veld kan worden geselecteerd. Zie [Vaartuigen](shipping-information-setup.md#vessels) voor meer informatie. |
| Eenheidstype | Eenheidstypen worden gebruikt als extra manier om containers te groeperen en te identificeren. Deze worden weergegeven en geselecteerd op de pagina containers. Zie [Eenheidstypen instellen](shipping-container-setup.md#unit-types) voor meer informatie. |
| Koelingstype | Koelingstypen worden gebruikt als extra manier om containers te groeperen en te identificeren, gewoonlijk koelcontainers. Deze worden weergegeven en geselecteerd op de pagina containers. Zie [Koelingstypen instellen](shipping-container-setup.md#refrigeration-types) voor meer informatie. |
| Afmeting | Met dit veld kunt u een meting opgeven in de module **Francoprijzen**. Metingen worden vaak gebruikt door organisaties die niet het individuele volume of gewicht van de goederen weten, maar die een nauwkeurigere verdeling vereisen dan met de opties Bedrag en Hoeveelheid mogelijk is. De expediteur verstrekt het gewicht in kilogrammen of de kubieke meting en u kunt deze instellen op het niveau van een artikel of de inkooporder. Dit kan automatisch worden bijgewerkt als de parameter is geselecteerd of handmatig wordt ingevoerd. |
| Maateenheid | De maateenheid die van toepassing is op de waarde in het veld **Meting**. |
| Werkelijk gewicht | U kunt het werkelijke gewicht van de doos of de container registreren. Deze waarde kan worden gebruikt voor verificatie met het maximumgewicht dat is toegestaan bij het instellen van een container. |
| Aantal dozen | Het aantal kartonnen dozen wordt automatisch bijgewerkt als de parameter wordt geselecteerd. |
| Beschrijving van goederen | U kunt een beschrijving van goederen selecteren in de header van de container of in de folioheader. Deze beschrijving wordt gebruikt om u te helpen bij het identificeren van een reis, container of folio van goederen. Zie [Beschrijving van goederen](shipping-information-setup.md#description-of-goods) voor meer informatie. |
| Interne (lucht)vrachtbrief | U kunt het luchtvrachtbrief of vrachtbrief voor de container opgeven. |
| Opmerkingen | Aanvullende informatie die betrekking heeft op de container. |
| Retourneerbaar | Een waarde die aangeeft of de container na de reis kan worden geretourneerd. |
| Reisstatus | De status van het traject dat is gekoppeld aan de container. |
| Status inkooporder | De status van de inkooporder die is gekoppeld aan de container. |

### <a name="settings-on-the-delivery-fasttab"></a>Instellingen op het sneltabblad Levering

In de volgende tabel worden de instellingen beschreven die beschikbaar zijn op het sneltabblad **Levering** van de weergave **Header** van een container.

| Veld | Beschrijving |
|---|---|
| Aanmaakdatum en -tijd | De datum en het tijdstip waarop de container is gemaakt. |
| Datum af-fabriek | Deze datum wordt meestal aan de fabriek/leverancier verstrekt om aan te geven wanneer u verwacht dat de goederen het bedrijfsgebouw verlaten. Wanneer u werkt met een fabriek in Azië, is deze datum vaak vereist in plaats van de datum waarop u de goederen verwacht. (Bij een lokale levering is daarentegen de datum verplicht waarop u de goederen verwacht.) Dit veld kan worden ingevuld vanuit de inkooporderregels in de lijst met containers. U kunt de datum ook handmatig hier invoeren. |
| Verzenddatum | Deze datum kan worden afgedrukt op het inkooporderdocument. Via dit document wordt de fabriek/leverancier geïnformeerd over de datum waarop de goederen in de haven moeten worden geleverd. Dit veld is alleen bedoeld voor informatieve doeleinden. De datum wordt niet gebruikt om de verwachte leveringsdatum van de goederen in de container te schatten. U kunt dit veld zo instellen dat het automatisch wordt bijgewerkt wanneer de pagina voor traceringsbeheer wordt bijgewerkt. |
| Datum in winkel | De vroegste datum waarop de goederen van de inkooporders die aan de reis zijn gekoppeld, beschikbaar zijn voor verkoop.|
| Geraamde leveringsdatum | Meestal is dit de datum waarop de goederen moeten binnenkomen in het magazijn. Dit veld is alleen bedoeld voor informatieve doeleinden. Het veld wordt niet gebruikt om de hoofdplanning te berekenen van de inkooporderregels in de container. De verwachte leveringsdatum op de inkooporderregels wordt bijgewerkt via traceringsbeheer. U kunt dit veld zo instellen dat het wordt bijgewerkt wanneer de pagina voor traceringsbeheer wordt bijgewerkt. |
| Vertrekdatum | Gewoonlijk is dit de datum waarop het vliegtuig of het vaartuig daadwerkelijk de overzeese haven verlaat. |
| ETA in haven | De geschatte aankomstdatum in de bestemmingshaven ('naar haven'). |
| Oorspronkelijke documenten ontvangen | Optioneel: de datum waarop de oorspronkelijke documenten zijn ontvangen. |
| Aanbevolen door makelaar | Optioneel: de datum waarop de tussenpersoon is geadviseerd. |
| Oorspronkelijke vrachtbrief verzonden | Optioneel: de datum bijwerken waarop de oorspronkelijke vrachtbrief is verzonden. |
| Goederen vrijgegeven | Optioneel: de datum bijwerken waarop de goederen zijn vrijgegeven. |
| Klantafspraak | Optioneel: de datum van de afspraak met de klant bijwerken. |
| Afgeleverd in magazijn | Optioneel: de datum bijwerken waarop goederen zijn afgeleverd bij het magazijn. |
| Verificatiedatum | Optioneel: de verificatiedatum bijwerken. |
| Leveringsinstructies | Optioneel: de datum van de leveringsinstructies bijwerken. |
| Vertrekhaven | De haven van waaruit de artikelen worden verzonden. |
| Aankomsthaven | De haven waarnaar de artikelen worden verzonden. |
| Lokale doorstuurder | Dit veld is alleen bedoeld voor informatieve doeleinden. De lokale expediteur kan worden geselecteerd in de leverancierstabel. |
| Datum van lokaal transport | Voer de datum in waarop het lokale transport wordt geboekt. Dit veld kan het magazijn helpen bij het plannen. |
| Tijd van lokaal transport | Geef het tijdvak op. Dit veld kan het magazijn helpen bij het plannen. |
| Trajectsjabloon | De trajectsjabloon die voor de reis is opgegeven. De trajectsjabloon bevat de details van de havens 'naar' en 'van' en de doorlooptijden die zijn gekoppeld aan het traceringsbeheer van de container. |

### <a name="settings-on-the-other-fasttab"></a>Instellingen op het sneltabblad Overige

In de volgende tabel worden de instellingen beschreven die beschikbaar zijn op het sneltabblad **Overige** van de weergave **Header** van een container.

| Veld | Beschrijving |
|---|---|
| Verhuur | Een waarde die aangeeft of de container een huurcontainer is. Huurkosten kunnen gekoppeld zijn aan huurcontainers. |
| Geconverteerd naar verhuur | Een waarde die aangeeft of de container is omgezet naar een huurcontainer. Huurkosten kunnen gekoppeld zijn aan huurcontainers. |
| Oorspronkelijke reis | Als de container is verplaatst naar een nieuwe reis, de oorspronkelijke reis. |
| Gebruikt | Gebruik deze optie om vast te leggen of er een huurcontainer voor verzending is gebruikt. Deze gegevens dienen alleen ter informatie. |
| Verwachte laaddatum | De datum waarop de container naar verwachting wordt geladen met goederen. |
| Ons serienummer | Voer het serienummer in dat in uw bedrijf intern voor de container gebruikt. |
| Serienummer expeditiebedrijf | Voer het serienummer in dat het expeditiebedrijf of de agent heeft opgegeven voor de container. |
| Datum waarop onderzoekscertificaat is toegepast | De datum waarop een onderzoek is aangevraagd voor de container. |
| Datum waarop onderzoekscertificaat is ontvangen | De datum waarop het onderzoekscertificaat is ontvangen. |
| Vervaldatum van onderzoekscertificaat | De datum waarop het onderzoekscertificaat verloopt. |
| Nummer onderzoekscertificaat | Het certificaatnummer van het certificaat dat is afgegeven na een onderzoek. |

## <a name="lines-view"></a>Regelweergave

Als u de weergave **Regels** wilt openen, opent u een container en selecteert u vervolgens het tabblad **Regels** in de rechterbovenhoek van de header van de container.

### <a name="information-on-the-shipping-container-fasttab"></a>Informatie op het sneltabblad container

Het sneltabblad **container** in de weergave **Regels** bevat informatie over het folio. De meeste informatie wordt ook weergegeven in de weergave **Header**, zoals eerder in dit onderwerp is beschreven.

### <a name="information-and-buttons-on-the-lines-fasttab"></a>Informatie en knoppen op het sneltabblad Regels

Op het sneltabblad **Regels** in de weergave **Regels** worden details weergegeven over elke volledige of gedeeltelijke inkooporderregel die in het huidige container is opgenomen.

In de volgende tabel worden de knoppen beschreven die op het sneltabblad **Regels** in de weergave **Regels** beschikbaar zijn.

| Knop | Beschrijving |
|---|---|
| Wissen | Verwijder de geselecteerde inkooporderregel uit de reis. |
| Voorraad \> Transacties | Hiermee geeft u de voorraadtransacties weer voor de geselecteerde inkooporderregel. Als u goederen in transit gebruikt, worden de oorspronkelijke order en de orders voor goederen in transit ook weergegeven. |
| Voorraad \> Dimensies weergeven | Hiermee opent u een dialoogvenster waarin u de voorraaddimensies kunt selecteren die worden weergegeven voor de transacties die u bekijkt. |
| Vernieuwen | Hiermee werkt u informatie bij die betrekking heeft op het regelbedrag, het gewicht of het volume van de geselecteerde inkooporderregel. |

### <a name="information-on-the-lines-details-fasttab"></a>Informatie op het sneltabblad Regeldetails

Op het sneltabblad **Regeldetails** in de weergave **Regels** worden details weergegeven over de inkooporderregel die op dat moment is geselecteerd op het sneltabblad **Regels**.
