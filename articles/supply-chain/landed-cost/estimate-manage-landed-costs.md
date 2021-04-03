---
title: Francoprijzen ramen en beheren
description: U kunt via de automatische kosteninstellingen een raming voor de francoprijzen bepalen. In dit onderwerp wordt uitgelegd hoe u verschillende scenario's kunt definiëren om een nauwkeurigere raming te leveren.
author: sherry-zheng
manager: tfehr
ms.date: 01/26/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMCostTemplateTable, ITM CostEstimateDialog, ITMCostEstimateTable, SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-26
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: cbd652f2b29f7a78ad9e4e1d3dda4a3ef8a9f3f3
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501265"
---
# <a name="estimate-and-manage-landed-costs"></a>Francoprijzen ramen en beheren

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

U kunt via de [automatische kosteninstellingen](auto-cost-setup.md) een raming voor de francoprijzen bepalen. Daarnaast kunt u verschillende scenario's definiëren om een nauwkeurigere raming te leveren. Deze scenario's worden opgeslagen. Daarom kunt u ze later bekijken en ze vergelijken met de werkelijke gegevens in een rapport. U kunt de artikelprijs ook bijwerken.

## <a name="set-up-cost-estimates"></a>Kostenramingen instellen

### <a name="set-up-cost-templates"></a>Kostensjablonen instellen

Met kostensjablonen kunt u standaardinstellingen opgeven die gebruikers die de raming krijgen, mogelijk niet weten. Met sjablonen kunt u de complexiteit in het ramingsproces verminderen door de selecties die gebruikers moeten opgeven, te minimaliseren om een juiste raming te krijgen. Als u het standaardkostenmodel gebruikt, kunt u kostensjablonen gebruiken terwijl u de kosten van goederen instelt.

Als u kostensjablonen wilt instellen, gaat u naar **Francoprijzen \> Kostprijsberekening instellen \> Kostensjablonen**. Op de pagina **Kostensjablonen** worden in het lijstdeelvenster aan de linkerkant alle huidige kostensjablonen weergegeven. U kunt de knoppen in het actiedeelvenster gebruiken om sjablonen te maken, te verwijderen en te bewerken.

In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke sjabloon.

| Veld | Beschrijving |
|---|---|
| Kostensjabloon | Een unieke naam invoeren voor de kostensjabloon. Met de naam wordt meestal de factor of kostenvermenigvuldiger voor de sjabloon beschreven. |
| Beschrijving | Voer een omschrijving van de kostensjabloon in. |
| Verzendbedrijf | Selecteer het expeditiebedrijf dat moet worden toegepast wanneer de sjabloon wordt gebruikt. |
| Leveringsmethode | Hier kunt u de leveringsmodus selecteren, zoals zee of lucht, die moet worden toegepast wanneer de sjabloon wordt gebruikt. Via dit veld kunt u de automatische kosten bepalen die zijn gekoppeld aan de goederen in een kostenraming. |
| Type verzendcontainer | Selecteer het type verzendcontainer dat moet worden toegepast wanneer de sjabloon wordt gebruikt. Via dit veld kunt u de automatische kosten bepalen die zijn gekoppeld aan de goederen in een kostenraming. |
| Douane-expediteur | Selecteer de douane-expediteur (leverancier) die moet worden toegepast wanneer de sjabloon wordt gebruikt. Met dit veld kunt u de automatische kosten bepalen die zijn gekoppeld aan de kostenraming. |
| Factor | Voer de vermenigvuldiger (percentage) in die automatisch moet worden toegepast op de kostenraming wanneer de sjabloon wordt gebruikt. Voer bijvoorbeeld *1,10* in om 10 procent op te tellen bij de berekende kostenraming. |

### <a name="create-a-cost-estimate"></a>Een kostenraming maken

Gebruik het dialoogvenster **Kostenraming** om een nieuwe kostenraming te genereren op basis van een geselecteerde kostensjabloon, een geselecteerde set artikelen en andere details van een kostprijsraming. Deze instellingen worden vervolgens gebruikt om de geschatte francoprijzen van goederen te bepalen. Deze kostenramingen worden voornamelijk gebruikt om met standaardkostenartikelen te werken. Als u de geschatte francoprijzen toevoegt aan de standaardkosten van goederen in de voorraad, moet u kleinere afwijkingstransacties krijgen wanneer de goederen worden toegevoegd aan een reis, omdat de standaardkosten de ramingen van deze francoprijzen weerspiegelen.

Als u het dialoogvenster **Kostenraming** wilt openen, gaat u naar **Francoprijzen \> Periodieke taken \> Kostenraming**. Stel vervolgens de velden in volgens de beschrijving in de volgende subsecties. Selecteer tot slot **OK** om de raming te maken. De pagina **Kostenraming** (**Francoprijzen \> Query's \> Kostenramingen**) wordt geopend en toont de nieuwe raming, zoals verderop in dit onderwerp wordt beschreven.

### <a name="settings-on-the-parameters-tab"></a>Instellingen op het tabblad Parameters

In de volgende tabel worden de velden beschreven die beschikbaar zijn op het tabblad **Parameters** van het dialoogvenster **Kostenraming**.


| Veld | Beschrijving |
|---|---|
| Kostensjabloon | Selecteer een kostensjabloon. De instellingen die aan de geselecteerde sjabloon zijn gekoppeld, worden gebruikt om de automatische kosten te bepalen die worden toegepast. |
| Ramingsdatum | Standaard is dit veld ingesteld op de datum van vandaag, maar u kunt de waarde wijzigen. De opgegeven datum wordt gebruikt om de juiste verkoopprijzen, inkoopprijzen, automatische kosten en de wisselkoers te selecteren als er een verzendtarief wordt gebruikt. |
| Afmeting | De kosten kunnen afhankelijk zijn van een meting. Wanneer er bijvoorbeeld vrachtkosten worden gebruikt, zijn volumeprijzen mogelijk van toepassing. Als de kosten afhankelijk zijn van een meting, voert u de waarde van die meting in. Anders is het raadzaam dit veld op *1* in te stellen, tenzij u er zeker van bent dat er geen verdeling plaatsvindt via een meting. Voer een decimale waarde in. De eenheid is de eenheid die is gedefinieerd in de toepasselijke record voor automatische kosten. |
| Reissjabloon | Selecteer een [trajectsjabloon](multi-leg-journey-setup.md). Dit veld wordt gebruikt om de juiste automatische kosten te bepalen die moeten worden toegepast. |
| Vertrekhaven | De haven van waaruit de artikelen worden verzonden. Dit veld wordt ingesteld op basis van de geselecteerde reissjabloon. |
| Aankomsthaven | De haven waarnaar de artikelen worden verzonden. Dit veld wordt ingesteld op basis van de geselecteerde reissjabloon. |
| Valuta | Selecteer de valuta waarin de artikelen worden ingekocht. |
| Containers | Geef het aantal containers op als er doorgaans meerdere containers worden gebruikt. Het systeem gebruikt vervolgens kosten voor meerdere containers wanneer het de kosten raamt. |
| Folio's | Als er doorgaans meerdere folio's worden gebruikt, geeft u de hoeveelheid op. (De hoeveelheid is doorgaans *1*.) |
| Locatie | Geef de locatie op waar de goederen moeten worden afgeleverd. |

### <a name="settings-on-the-items-tab"></a>Instellingen op het tabblad Artikelen

Op het tabblad **Artikelen** kunt u net zoveel artikelen aan de raming toevoegen als u nodig hebt. Gebruik de werkbalk om artikelen aan het raster toe te voegen of artikelen te verwijderen. Selecteer **Voorraad \> Dimensies weergeven** op de werkbalk om een dialoogvenster te openen waarin u dimensiekolommen aan het raster kunt toevoegen of kolommen kunt verwijderen.

In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elk artikel.

| Veld | Beschrijving |
|---|---|
| artikelnummer | Selecteer het artikel waarvoor u de prijs wilt bepalen. (Als het artikel nog niet in het systeem bestaat, kunt u een artikel maken, dit eventueel koppelen aan een kostprijsgroep voor een artikel voor de reis en de prijs vervolgens leeg laten of de prijs maken of wijzigen.) |
| Leverancier | Selecteer de leverancier die u wilt gebruiken om dit artikel te ramen. Als er een standaardleverancier aan het artikel is toegewezen, wordt dit veld automatisch ingesteld. |
| Hoeveelheid | Selecteer de hoeveelheid die u wilt inkopen. |
| Kostprijs | De prijsregels van het systeem worden gebruikt om een beginprijs te zoeken, maar u kunt deze prijs zo nodig overschrijven. |
| Verkoopprijs | De verwachte verkoopprijs van de goederen invoeren. |
| Afmeting | Voer een decimale waarde in voor de meting van de goederen. De eenheid is de eenheid die is ingesteld voor het toepasselijke vrijgegeven product. |
| Gewicht/volume van artikel bijwerken | Schakel dit selectievakje in om het gewicht of volume van het vrijgegeven product bij te werken, zodat dit overeenkomt met de **Meting** die voor deze rij is ingevoerd. |
| (Overige dimensies) | Afhankelijk van de dimensies die u hebt geselecteerd om weer te geven, kunt u aanvullende kolommen met informatie over elk artikel zien. |

Als u de details van het volume en/of het gewicht van een artikel wilt weergeven of aanpassen, selecteert u het artikel in het raster en gebruikt u vervolgens de velden onder aan de pagina.

## <a name="manage-estimated-costs"></a>Kostenramingen beheren

Als u de gemaakte kostenramingen wilt weergeven en bewerken, gaat u naar **Francoprijzen \> Query's \> Kostenramingen**. Op de pagina **Kostenramingen** worden in het lijstdeelvenster aan de linkerkant alle huidige kostenramingen weergegeven. U kunt de knoppen in het actievenster gebruiken om te werken met een geselecteerde raming. U kunt geen nieuwe kostenraming maken op de pagina **Kostenramingen**. Gebruik in plaats daarvan het dialoogvenster **Kostenraming** (**Francoprijzen \> Periodieke taken \> Kostenramingen**), zoals eerder in dit onderwerp is beschreven.

Op de pagina **Kostenramingen** wordt weergegeven hoe elke kostenraming is afgeleid. In dit rapport worden ook de geraamde francoprijzen voor elk artikel weergegeven. U kunt een kostenraming wijzigen door de kostprijs en/of valuta te wijzigen die aan de verschillende goederen zijn gekoppeld. U kunt de gekoppelde kosten van de reis ook wijzigen op zowel het niveau van de reis als van de container. Wanneer u deze pagina gebruikt om de kosten te wijzigen, wordt u gevraagd de ramingen voor de artikelen in de kostenraming opnieuw te berekenen. Wanneer u gereed bent, kunt u de ramingen gebruiken om de kostprijs van de artikelen in de kostensjabloon bij te werken.

### <a name="information-on-the-header"></a>Informatie in de koptekst

Boven aan de pagina **Kostenramingen** ziet u de instellingen die zijn gebruikt om de geselecteerde kostenraming te genereren, zoals is beschreven in de vorige sectie. 

### <a name="settings-and-buttons-on-the-lines-fasttab"></a>Instellingen en knoppen op het sneltabblad Regels

Op het sneltabblad **Regels** wordt elk artikel vermeld dat in de huidige raming is meegenomen. In de volgende tabel wordt het veld beschreven dat beschikbaar is voor elke rij.

| Veld | Beschrijving |
|---|---|
| Leverancier | De leveranciersrekening die aan het artikel is gekoppeld. |
| artikelnummer | Het artikelnummer. |
| Hoeveelheid | Het aantal artikelen dat wordt gebruikt om de kosten te bepalen. |
| Kostprijs | De kostprijs volgens de handelsovereenkomst. Deze waarde wordt weergegeven in de lokale valuta. |
| Afmeting | De afzonderlijke meting. De eenheid is de eenheid die is gedefinieerd voor het toepasselijke vrijgegeven product. |
| Geraamde francokosten | De geraamde francoprijzen voor de totale hoeveelheid. |
| Per eenheid | De geraamde francoprijzen gedeeld door de hoeveelheid. |
| (Overige dimensies) | Afhankelijk van de dimensies die u hebt geselecteerd om weer te geven, kunt u aanvullende kolommen met informatie over elk artikel zien. |

In de volgende tabel worden de knoppen beschreven die op de werkbalk op het sneltabblad **Regels** beschikbaar zijn.

| Knop | Beschrijving |
|---|---|
| Toevoegen | Voeg artikelen aan de kostenraming toe. Nadat u artikelen hebt toegevoegd, moet u **Opnieuw berekenen** selecteren in het actiedeelvenster. |
| Wissen | Verwijder artikelen uit de kostenraming. Nadat u artikelen hebt verwijderd, moet u **Opnieuw berekenen** selecteren in het actiedeelvenster. |
| Reiskosten | Open een pagina waarin u diverse typen kosten voor het artikel kunt weergeven en bewerken. |
| Voorraad \> Dimensies weergeven | Open een dialoogvenster waarin u dimensiekolommen aan het raster kunt toevoegen of kolommen kunt verwijderen. |

### <a name="settings-on-the-general-fasttab"></a>Instellingen op het sneltabblad Algemeen

Het sneltabblad **Algemeen** toont details over het artikel dat nu is geselecteerd op het sneltabblad **Regels**. Veel van deze informatie wordt herhaald vanuit het sneltabblad **Regels** en kan op beide plaatsen worden bewerkt. Hier zijn echter ook aanvullende gegevens beschikbaar. De waarden van de extra velden zijn gebaseerd op de instellingen van het toepasselijke vrijgegeven product.

### <a name="settings-on-the-dimension-fasttab"></a>Instellingen op het sneltabblad Dimensie

Het sneltabblad **Dimensie** toont waarden voor alle beschikbare voorraaddimensies voor het artikel dat is geselecteerd op het sneltabblad **Regels**, ongeacht de dimensies die u hebt gekozen om hier te worden weergegeven. Waarden die hier worden weergegeven, zijn afkomstig van de toepasselijke kostenramingssjabloon. Deze zijn optioneel in de kostenramingssjabloon.

### <a name="buttons-on-the-action-pane"></a>Knoppen in het actiedeelvenster

Met de knoppen in het actiedeelvenster van de pagina **Kostenramingen** kunt u werken met de geselecteerde kostenraming. In de volgende tabel wordt beschreven welke knoppen beschikbaar zijn.

| Actie | Beschrijving |
|---|---|
| Kostenquery | Alle kosten voor de reis weergeven. U kunt desgewenst kosten weergeven op het niveau van het afzonderlijke artikel. |
| Standaardkosten bijwerken | <p>Werk de standaardkosten bij met de standaardversie van kostprijsberekening die is gedefinieerd op de pagina **Parameters voor francoprijzen**. U kunt deze versie overschrijven.</p><p>**Opmerking:** als een artikel verschillende artikeldimensies heeft (bijvoorbeeld verschillende grootten, kleuren en configuraties), maar deze dimensies niet zijn geselecteerd voor de raming, wordt voor elke combinatie een prijs in behandeling genomen.</p><p>**Belangrijk:** de prijsuitsplitsing wordt gemaakt en wordt gebruikt om de standaardkostenafwijking per francoprijs te bepalen.</p> |
| Reiskosten | Bekijk en bewerk reiskosten voor alle goederen in de zending. |
| Opnieuw berekenen | Werk de geschatte francoprijzen bij nadat de reiskosten zijn bijgewerkt, toegevoegd of verwijderd. |
| Vergrendeld | Vergrendel de kostenramingsrecord, zodat er geen wijzigingen meer kunnen worden aangebracht. |

## <a name="item-cost-price-update"></a>Update van kostprijs voor artikel

Met de periodieke taak **Artikelkostprijs bijwerken** worden alle kostenramingen bijgewerkt die overeenkomen met de filters die u tijdens het uitvoeren van de taak hebt ingesteld. Het effect is vergelijkbaar met de selectie van de optie **Standaardkosten bijwerken** in het actiedeelvenster voor één raming. In dit geval is de update echter van toepassing op alle overeenkomende ramingen.

Volg deze stappen om de periodieke taak uit te voeren.

1. Ga naar **Francoprijzen \> Periodieke taken \> Artikelkostprijs bijwerken**.
1. Stel in het dialoogvenster **Kostprijs bijwerken vanuit raming** de volgende velden in om het bereik van de update te beperken:

    - **Versie**: werk alleen ramingen bij die de opgegeven versie van de kostprijsberekening gebruiken.
    - **Site**: werk alleen ramingen bij die de opgegeven site gebruiken.
    - **Kostensjabloon**: werk alleen ramingen bij die de opgegeven sjabloon gebruiken.
    - **Aankomsthaven**: werk alleen ramingen bij die de opgegeven aankomsthaven gebruiken.
    - **Ramingsdatum**: werk alleen de ramingen met de opgegeven datum bij.

1. Stel de opties op het sneltabblad **Op te nemen records** en **Op de achtergrond uitvoeren** zoals gebruikelijk voor periodieke taken in.
1. Selecteer **OK** om de taak uit te voeren.

> [!NOTE]
> Deze periodieke taak wordt alleen uitgevoerd als de volgende informatie beschikbaar is:
>
> - Voor elk relevant product moeten de **Brutodiepte**, **Brutobreedte** en **Brutohoogte** zijn gedefinieerd.
> - Voor elke relevante leverancier moet een **Vertrekhaven** zijn gedefinieerd.
