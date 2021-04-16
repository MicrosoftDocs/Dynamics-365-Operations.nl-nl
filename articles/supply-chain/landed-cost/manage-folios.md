---
title: Folio's beheren
description: In dit onderwerp wordt beschreven hoe u met folio's werkt. Een folio bestaan uit goederen van één leverancier voor één entiteit of bedrijf per zending. De goederen in een folio kunnen zich in één container bevinden of zijn verdeeld over meerdere containers.
author: sherry-zheng
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMFolioTable, ITMFolioTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 99159d2197648b8f17a719b74c8cd6ea4bffe550
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833828"
---
# <a name="manage-folios"></a>Folio's beheren

[!include [banner](../../includes/banner.md)]

Een folio wordt vaak bepaald door douanevoorschriften. De folio kan bestaan uit goederen van één leverancier voor één entiteit of bedrijf per zending. De goederen in een folio kunnen zich in één container bevinden of zijn verdeeld over meerdere containers.

U opent de pagina **Alle folio's** door naar **Francoprijzen \> Folio's \> Alle folio's** te gaan. Op deze pagina wordt een lijst met alle huidige folio's weergegeven. U kunt de knoppen in het actievenster gebruiken om folio's te maken, te verwijderen en met folio's te werken. Selecteer een folio in de lijst om de details weer te geven op de pagina **Folio's**.

## <a name="action-pane"></a>Actievenster

Het actievenster van de pagina's **Alle folio's** en **Folio's** bieden knoppen die u kunt gebruiken om met een geselecteerde folio te werken. Met elke knop voert u één actie uit. Het actievenster bevat ook tabbladen die elk op hun beurt een reeks verwante knoppen bieden. Behalve daar waar aangegeven, zijn alle knoppen en tabbladen die in de volgende subsecties worden beschreven, beschikbaar in de lijstweergave (dat wil zeggen op de pagina **Alle folio's**) en in de gedetailleerde weergave (dat wil zeggen op de pagina **Folio's**).

### <a name="buttons-that-appear-directly-on-the-action-pane"></a>Knoppen die rechtstreeks in het actievenster worden weergegeven

In de volgende tabel wordt de knoppen beschreven die rechtstreeks in het actievenster beschikbaar zijn.

| Knop | Beschrijving |
|---|---|
| Nieuw | Maak een folio. |
| Delete | Verwijder het geopende of geselecteerde folio. |
| Reiskosten | Open de pagina **Transportkosten**, waar u kosten op folioniveau kunt weergeven en toevoegen aan alle goederen in het transport. Wanneer foliokosten handmatig aan het transport worden toegevoegd, worden ze automatisch toegevoegd aan de querypagina voor kosten en verdeeld over elk artikel volgens de methode die is opgegeven op de pagina **Transportkosten**. |

### <a name="buttons-on-the-manage-tab"></a>Knoppen op het tabblad Beheren

In de volgende tabel worden de knoppen beschreven die op het tabblad **Beheren** van het actievenster beschikbaar zijn.

| Knop | Beschrijving |
|---|---|
| Ontvangstlijst boeken | Boek een ontvangstlijst voor alle inkooporderregels in het folio. Als er zendingen naar meerdere bedrijven worden gebruikt, wordt er een nieuw dialoogvenster voor het boeken van een ontvangstlijst geopend voor elk bedrijf. |
| Productontvangstbon boeken | Boek een productontvangstbon voor alle inkooporderregels in het folio. Als er transporten naar meerdere bedrijven worden gebruikt, wordt er een nieuw dialoogvenster voor het boeken van productontvangsten geopend voor elk bedrijf. |
| Factuur boeken | Boek een factuur voor alle inkooporderregels in het folio. Als er transporten naar meerdere bedrijven worden gebruikt, wordt er een nieuw dialoogvenster voor het boeken van facturen geopend voor elk bedrijf. |
| Verzenden overboekingsorders | Boek een overboekingsorder voor alle overboekingsorderregels die betrekking hebben op het huidige folio in de gerelateerde zending. |
| overboekingsorder ontvangen | Boek een overboekingsorderontvangst voor alle overboekingsorderregels die betrekking hebben op het huidige folio in de gerelateerde zending. |
| Goederen in transit ontvangen | Ontvang alle orderregels die in transit zijn in het folio. |
| Documenten ontvangen | Stel de instelling van de optie **Documenten ontvangen** in op *Ja*. Met deze knop kunt u het artikel en/of de inkoopregel vergrendelen zodat deze niet verder kan worden bijgewerkt. |
| Automatisch kosten zoeken | Zoek relevante transportkosten. Als deze kosten al zijn gevonden of bijgewerkt, ontvangt u het volgende bericht: 'Er bestaan niet-gefactureerde kostenregels. Wilt u deze overschrijven?' Houd er rekening mee dat transportkosten die aan het folio zijn gekoppeld en die zijn gefactureerd, niet worden overschreven. |
| Ontvangstjournaal maken | Genereer een ontvangstjournaal voor organisaties met behulp van geavanceerde magazijnfuncties. U kunt **Hoeveelheid initialiseren** (aanbevolen), **Maken van goederen in transit** en/of **Maken op basis van inkooporders** selecteren. De laatste optie is afhankelijk van of de verwerking van goederen in transit wordt gebruikt. |
| Kosten toerekenen | Kosten toerekenen voor een kostentype waarvoor een grootboekrekening is opgegeven voor de afschrijving. Deze knop wordt meestal gebruikt wanneer de voorraad in transit is of wanneer goederen zijn ontvangen en gefactureerd. |

### <a name="buttons-on-the-general-tab"></a>Knoppen op het tabblad Algemeen

In de volgende tabel worden de knoppen beschreven die op het tabblad **Algemeen** van het actievenster beschikbaar zijn.

| Knop | Beschrijving |
|---|---|
| Ontvangstlijst | Boek een ontvangstlijst voor alle inkooporderregels in het folio. Als er transporten naar meerdere bedrijven worden gebruikt, wordt er een nieuw dialoogvenster voor het boeken van ontvangstlijsten geopend voor elk bedrijf. |
| Ontvangst van producten | Bekijk de productontvangstrecord als deze wordt gebruikt. |
| Artikelontvangst | Bekijk het artikelontvangstjournaal, als het is gebruikt. |
| Vraag naar kostenposten | Open de querypagina voor kosten om alle kosten van een transport weer te geven, inclusief de container, folio en inkooporder. U kunt de exacte weergave van de pagina aanpassen met de actie Weergeven. Op de querypagina voor kosten kunt u alle gebieden weergeven, plus het artikel en de kostentypecode. Als u deze artikelen verwijdert, kunt u de pagina aanpassen door kosten te groeperen. Deze mogelijkheid kan handig zijn als u afmetingen en kleuren gebruikt. U kunt de dimensies wijzigen die op de pagina worden weergegeven. Op de pagina **Kosten** worden alleen kostentypecodes weergegeven waarbij de vermelding **Dr** op het tabblad **Boeking** is ingesteld *Artikel*. |

## <a name="header-view"></a>Weergave headers

Als u de weergave **Header** wilt openen, opent u een folio en selecteert u vervolgens het tabblad **Header** in de rechterbovenhoek van de folioheader.

### <a name="settings-on-the-general-fasttab"></a>Instellingen op het sneltabblad Algemeen

In de volgende tabel worden de velden beschreven die beschikbaar zijn op het sneltabblad **Algemeen** van de weergave **Header** van een folio.

| Veld | Beschrijving |
|---|---|
| Folio | De naam van het folio. Deze naam wordt automatisch gegenereerd wanneer het folio wordt gemaakt.|
| Reis | Het transport dat aan het folio is gekoppeld. |
| Douanemakelaar | Selecteer de douanemakelaar voor het folio. Douanemakelaars worden gedefinieerd voor de leverancier. Op deze manier kunnen gemaakte kosten automatisch worden bepaald. |
| Interne (lucht)vrachtbrief | Geef de luchtvrachtbrief of vrachtbrief op die van toepassing is op het folio. |
| Bedrijf | De rechtspersoon (bedrijf) die aan het folio is gekoppeld. |
| Vrachtcontrolenummer | Dit veld wordt in sommige landen of regio's door door douaneafdelingen gebruikt. |
| Afmeting | Met dit veld kunt u een meting opgeven in de module **Francoprijzen**. Metingen worden vaak gebruikt door organisaties die niet het individuele volume of gewicht van de goederen weten, maar die een nauwkeurigere verdeling vereisen dan met de opties Bedrag en Hoeveelheid mogelijk is. De expediteur verstrekt het gewicht of de kubieke meting en u kunt deze instellen op het niveau van een artikel of de inkooporder. Dit kan automatisch worden bijgewerkt als de parameter is geselecteerd of handmatig wordt ingevoerd. |
| Maateenheid | De eenheid die van toepassing is op de opgegeven meting. |
| Aantal dozen | Het aantal kartonnen dozen in het folio. Dit veld kan automatisch worden bijgewerkt, afhankelijk van de parameterselectie. |
| Leverancier | Selecteer de leverancier die aan het folio is gekoppeld. Dit veld is alleen bedoeld voor informatieve doeleinden. Dit heeft geen invloed op de functionaliteit. |
| Naam | De naam van de geselecteerde leveranciersrekening. |
| Opmerkingen | Voer eventuele aanvullende informatie in die betrekking heeft op het folio. |
| Beschrijving van goederen | Selecteer een omschrijving van de goederen om het folio te identificeren. Zie [Beschrijving van goederen](shipping-information-setup.md#description-of-goods) voor meer informatie. |
| Waarderingsdatum | Dit veld heeft betrekking op pagina voor de invoerpagina voor invoerrechten. In de module **Francoprijzen** wordt de wisselkoers van de douane gebruikt voor de datum die u hier in stelt. De standaardwaarde is de datum op de invoerpagina voor invoerrechten. |
| Douane-id | Voer de douane-id in. De douaneafdelingen in landen of regio's verstrekken deze id. |
| Tariefcode | Voer een tariefcode in die u aan het folio wilt koppelen. Deze code is meestal vereist (en gedefinieerd) door het land of de regio waarnaar u goederen verzend. |

### <a name="settings-on-the-delivery-fasttab"></a>Instellingen op het sneltabblad Levering

In de volgende tabel worden de instellingen beschreven die beschikbaar zijn op het sneltabblad **Levering** van de weergave **Header** van een folio.

| Veld | Beschrijving |
|---|---|
| Foliodatum | Selecteer een datum die u aan het folio wilt koppelen. De standaardwaarde is de aanmaakdatum van het transport. |
| ETA in haven | De geschatte aankomsttijd(ETA, Time of Arrival) in de bestemmingshaven ('naar haven'). |
| Geraamde leveringsdatum | Meestal is dit de datum waarop de goederen moeten binnenkomen in het magazijn. Dit veld wordt niet gebruikt bij de berekening van de geschatte leveringsdatum. (In plaats daarvan wordt de door traceringsbeheer geschatte leveringsdatum gebruikt.) Als u dit veld zo wilt instellen dat de waarde overeenkomt met de door traceringsbeheer geschatte leveringsdatum, gebruikt u het [Traceringsbeheercentrum](delivery-information-setup.md#tracking-control-center). |
| Oorspronkelijke documenten ontvangen | De datum waarop de oorspronkelijke documenten zijn ontvangen. |
| Aanbevolen door makelaar | De datum waarop de tussenpersoon is geadviseerd. |
| Oorspronkelijke vrachtbrief verzonden | De datum waarop de oorspronkelijke vrachtbrief is verzonden. |
| Goederen vrijgegeven | De datum waarop de goederen zijn vrijgegeven. |
| Klantafspraak | De afspraakdatum van de klant. |
| Afgeleverd in magazijn | De datum waarop goederen zijn afgeleverd bij het magazijn. |
| Verificatiedatum | De verificatiedatum. |
| Leveringsinstructies | De datum waarop de leveringsinstructies zijn ontvangen. |
| Vertrekhaven | De haven van waaruit de reis vertrekt. |
| Aankomsthaven | De haven waarin de reis aankomt. De container kan een andere haven hebben, omdat het schip mogelijk meerdere havens aandoet. |

### <a name="settings-on-the-export-fasttab"></a>Instellingen op het sneltabblad Exporteren

In de volgende tabel worden de instellingen beschreven die beschikbaar zijn op het sneltabblad **Exporteren** van de weergave **Header** van een folio.

| Veld | Beschrijving |
|---|---|
| Exporteur | De exporteur kan op het folio worden opgeslagen. In internationale handel stuurt u mogelijk een inkooporder naar het ene bedrijf, maar ontvangt u de goederen van een ander bedrijf. De douane vereist tracering en documentatie. De naam en het adres van de exporteur kunnen hier worden opgeslagen. |
| Naam | De naam van de geselecteerde exporteur. |

## <a name="lines-view"></a>Regelweergave

Als u de weergave **Regels** wilt openen, opent u een folio en selecteert u vervolgens het tabblad **Regels** in de rechterbovenhoek van de folioheader.

### <a name="information-on-the-folio-fasttab"></a>Informatie op het sneltabblad Folio

Het sneltabblad **Folio** in de weergave **Regels** bevat informatie over het folio. De meeste informatie wordt ook weergegeven in de weergave **Header**, zoals eerder in dit onderwerp is beschreven.

### <a name="information-and-buttons-on-the-lines-fasttab"></a>Informatie en knoppen op het sneltabblad Regels

Op het sneltabblad **Regels** in de weergave **Regels** worden details weergegeven over elke volledige of gedeeltelijke inkooporderregel die in het huidige folio is opgenomen.

In de volgende tabel worden de knoppen beschreven die op het sneltabblad **Regels** in de weergave **Regels** beschikbaar zijn.

| Knop | Beschrijving |
|---|---|
| Wissen | Verwijder de geselecteerde inkooporderregel uit de reis. |
| Voorraad \> Transacties | Hiermee geeft u de voorraadtransacties weer voor de geselecteerde inkooporderregel. Als u goederen in transit gebruikt, worden de oorspronkelijke order en de orders voor goederen in transit ook weergegeven. |
| Voorraad \> Dimensies weergeven | Hiermee opent u een dialoogvenster waarin u de voorraaddimensies kunt selecteren die worden weergegeven voor de transacties die u bekijkt. |
| Vernieuwen | Hiermee werkt u informatie bij die betrekking heeft op het regelbedrag, het gewicht of het volume van de geselecteerde inkooporderregel. |

### <a name="information-on-the-lines-details-fasttab"></a>Informatie op het sneltabblad Regeldetails

Op het sneltabblad **Regeldetails** in de weergave **Regels** worden details weergegeven over de inkooporderregel die op dat moment is geselecteerd op het sneltabblad **Regels**.
