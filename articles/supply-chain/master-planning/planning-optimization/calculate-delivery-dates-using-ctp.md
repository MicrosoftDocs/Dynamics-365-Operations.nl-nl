---
title: Leveringsdatums van verkooporders berekenen met behulp van CTP
description: Met de Capable-to-promise- of CTP-functionaliteit kunt u klanten realistische datums geven voor de datums waarop u specifieke goederen kunt leveren. In dit artikel wordt beschreven hoe u CTP kunt instellen en gebruiken voor elke planningsengine (Planningsoptimalisatie en de ingebouwde engine).
author: t-benebo
ms.date: 07/20/2022
ms.topic: article
ms.search.form: SalesAvailableDlvDates, SalesTable, CustParameters, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-07-20
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 9a2d8a66fe7e68ebd5729a401af3f0efe04051b1
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229933"
---
# <a name="calculate-sales-order-delivery-dates-using-ctp"></a>Leveringsdatums van verkooporders berekenen met behulp van CTP

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Met de Capable-to-promise- of CTP-functionaliteit kunt u klanten realistische datums geven voor de datums waarop u specifieke goederen kunt leveren. Voor elke verkoopregel kunt u een datum leveren die rekening houdt met bestaande voorraad, productiecapaciteit en transporttijden.

CTP vergroot de de [available-to-promise-](../../sales-marketing/delivery-dates-available-promise-calculations.md) of ATP-functionaliteit door rekening te houden met capaciteitsgegevens. Hoewel ATP alleen rekening houdt met de beschikbaarheid van materialen en uitgaat van onbeperkte capaciteitsbronnen, houdt CTP rekening met de beschikbaarheid van zowel materialen als capaciteit. Daarom biedt CTP een realistischer beeld van de vraag of binnen een bepaald tijdsbestek aan vraag kan worden voldaan.

CTP werkt iets anders, afhankelijk van van de engine die voor hoofdplanning wordt gebruikt (Planningsoptimalisatie of de ingebouwde engine). In dit artikel wordt beschreven hoe dit voor elke engine kan worden ingesteld. CTP voor Planningsoptimalisatie ondersteunt momenteel alleen een subset van de CTP-scenario's die worden ondersteund door de ingebouwde engine.

## <a name="turn-on-ctp-for-planning-optimization"></a>CTP voor Planningsoptimalisatie inschakelen

CTP voor de ingebouwde hoofdplanning-engine is altijd beschikbaar. Als u echter CTP wilt gebruiken voor Planningsoptimalisatie, moet deze functie zijn ingeschakeld voor het systeem. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en in te schakelen. Schakel in de werkruimte **Functiebeheer** de functie als volgt in:

- **Module:** *Hoofdplanning*
- **Naam functie:** *(preview) CTP voor Planningsoptimalisatie*

## <a name="how-ctp-compares-to-atp"></a>Hoe verhoudt CTP zich met ATP

CTP en ATP zijn vergelijkbaar, maar met CTP kan vaak een nauwkeuriger resultaat worden verkregen, zoals het onderstaande voorbeeld laat zien.

Artikel A is een artikel dat bestaat uit artikelen B en C, en de beschikbare hoeveelheid van artikel A is 0 (nul). Als u een ATP-controle uitvoert waarbij alleen materialen in overweging worden genomen, zal de ATP-hoeveelheid ook 0 (nul) zijn. Als u echter een CTP-controle uitvoert, controleert het systeem de beschikbaarheid van de artikelen B en C, controleert het systeem de resources die nodig zijn om deze om te zetten in artikel A en berekent het systeem hoeveel artikelen A er kunnen worden gemaakt. Bovendien kan de CTP-berekening de resources en materialen controleren die nodig zijn om meer van artikelen B en C te maken en om ze te gebruiken om meer van artikel A te maken.

Een CTP-berekening waarin zowel materialen als resources worden meegenomen, kan een grotere hoeveelheid tonen dan een berekening die alleen materialen controleert, met name wanneer het artikel dat wordt gecontroleerd een artikel voor assembleren-naar order is. Met andere woorden, de CTP-functionaliteit is gebaseerd op de explosiefunctie en kan worden uitgevoerd voor een geselecteerde verkooporderregel om de verwachte leveringsdatum te berekenen.

## <a name="how-ctp-differs-depending-on-the-master-planning-engine-that-you-use"></a>De manier waarop CTP verschilt, afhankelijk van de gebruikte engine voor hoofdplanning

In de volgende tabel worden de verschillen tussen CTP voor Planningsoptimalisatie en CTP voor de ingebouwde hoofdplanning-engine samengevat.

| Element | Planningsoptimalisatie | Ingebouwde hoofdplanning-engine |
|---|---|---|
| Instelling voor **Controle leveringsdatum** voor orders, orderregels en producten | *CTP voor Planningsoptimalisatie* | *CTP* |
| Berekeningstijd | De berekening wordt geactiveerd door een dynamisch plan uit te voeren als een geplande taak. | De berekening wordt onmiddellijk geactiveerd, telkens wanneer u een verkooporderregel invoert of bijwerkt. |
| Waarde van veld **Status CTP voor Planningsoptimalisatie** | <p>Er wordt een waarde *Niet gereed* getoond voor orders en orderregels waar het dynamische plan niet is uitgevoerd sinds de orders en regels zijn aangemaakt of voor het laatst zijn bijgewerkt.</p><p>Er wordt een waarde *Gereed* getoond voor orders en regels waarbij CTP is gebruikt om bevestigde leveringsdatums te berekenen door het dynamische plan uit te voeren.</p> | Er wordt altijd een waarde *Gereed* getoond. |

## <a name="set-default-delivery-date-control-methods"></a><a name="default-methods"></a>Standaardmethode om de leveringsdatum te controleren instellen

Het systeem kan een van verschillende methoden gebruiken om voor elke order en orderregel de verwachte leveringsdatum te berekenen. U moet de controlemethode voor leveringsdatums instellen die u het meest wilt gebruiken als de algemene standaardmethode. U kunt ook individuele overschrijvingen voor elk product instellen. Later kunt u de standaardmethoden voor elke order en/of orderregel naar wens overschrijven.

### <a name="set-the-global-default-delivery-date-control"></a><a name="global-default"></a>Algemene standaardmethode om de leveringsdatum te controleren instellen

De standaardmethode voor controle van de leveringsdatum wordt toegepast op alle nieuwe orderregels waarvoor geen overschrijving van toepassing is. Volg deze stappen om er één te selecteren.

1. Ga naar **Klanten \> Instellen \> Parameters van module Klanten**.
1. Selecteer op het tabblad **Zendingen** op het sneltabblad **Leveringscontrole** in het veld **Controle leveringsdatum** de methode die u wilt gebruiken als standaardmethode voor uw bedrijf:

    - *Geen*: geen leveringsdatums berekenen.
    - *Verkooplevertijd*: de verkooplevertijd is de tijd tussen het maken van de verkooporder en de zending van de artikelen. De berekening van de leveringsdatum is gebaseerd op een standaardaantal dagen waarbij geen rekening wordt gehouden met beschikbaarheid van voorraad, bekende vraag of gepland aanbod.
    - *ATP*: ATP is de hoeveelheid van een artikel, die beschikbaar is en aan een klant kan worden beloofd op een specifieke datum. Bij de ATP-berekening worden niet-toegezegde voorraad, levertijden, geplande ontvangsten en uitgiften gebruikt.
    - *ATP + uitgiftemarge*: de verzenddatum is gelijk aan de ATP-datum plus de uitgiftemarge voor het artikel. De uitgiftemarge is de tijd die nodig is voor het voorbereiden van artikelen voor verzending.
    - *CTP* : gebruik de CTP-berekening die wordt geleverd door de ingebouwde hoofdplanning-engine. Als u Planningsoptimalisatie gebruikt, is de controlemethode voor de *CTP*-leveringsdatum niet toegestaan en wordt bij het uitvoeren van de berekening een foutbericht weergegeven als deze methode is geselecteerd.
    - *CTP voor planningsoptimalisatie*: gebruik de CTP-berekening die wordt geleverd door Planningsoptimalisatie. Deze optie heeft geen effect als u de ingebouwde hoofdplanning-engine gebruikt.

### <a name="set-delivery-date-control-overrides-for-individual-products"></a>Overschrijvingen voor controle van leveringsdatums instellen voor afzonderlijke producten

U kunt overschrijvingen toewijzen voor specifieke producten waarbij u een andere controlemethode voor leveringsdatums wilt gebruiken dan de methode die is ingesteld als algemene standaardmethode.

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Selecteer het product dat u wilt instellen.
1. Selecteer in het actievenster op het tabblad **Voorraadbeheer** in de groep **Orderinstellingen** de optie **Standaardorderinstellingen**.
1. Op de pagina **Standaardorderinstellingen** stelt u op het sneltabblad **Verkooporder** de optie **Leveringscontrole overschrijven** in op *Ja*.
1. Selecteer in het veld **Controle leveringsdatum** de methode die u voor het geselecteerde product wilt gebruiken. Dezelfde opties die worden beschreven in het gedeelte [Algemene standaardmethode om de leveringsdatum te controleren instellen](#global-default) zijn beschikbaar.

## <a name="schedule-ctp-for-planning-optimization-calculations"></a><a name="batch-job"></a>CTP voor planningsoptimalisatieberekeningen plannen

Wanneer u CTP gebruikt voor Planningsoptimalisatie, moet u een dynamisch plan uitvoeren om het systeem te activeren voor het uitvoeren van de CTP-berekeningen en vervolgens de bevestigde verzend- en ontvangstdatums instellen voor alle relevante orders. Het plan moet alle artikelen bevatten waarop bevestigde verzend- en ontvangstdatums vereist zijn. (Wanneer u CTP gebruikt voor de ingebouwde planning engine, worden de CTP-berekeningen onmiddellijk lokaal uitgevoerd. Daarom hoeft u geen dynamisch plan uit te voeren om de CTP-resultaten te bekijken.)

Om er zeker van te zijn dat de datums op tijd beschikbaar zijn voor alle gebruikers, wordt het aanbevolen om batchtaken in te stellen om de relevante plannen regelmatig uit te voeren. Met een batchtaak die bijvoorbeeld is ingesteld om elke 30 minuten een dynamisch plan uit te voeren, worden de bevestigde verzend- en ontvangstdatums elke 30 minuten ingesteld. Daarom moeten gebruikers die orders invoeren en importeren, maximaal 30 minuten wachten om de bevestigde verzend- en ontvangstdatums op te halen.

Voer de volgende stappen uit om een batchtaak in te stellen voor het uitvoeren van een dynamisch plan volgens een regelmatig schema.

1. Ga naar **Hoofdplanning \> Hoofdplanning \> Uitvoeren \> Hoofdplanning**.
1. Stel in het dialoogvenster **Hoofdplanning** op het sneltabblad **Parameters** het veld **Hoofdplan** in op het dynamische plan dat u wilt uitvoeren.
1. Stel op het sneltabblad **Op de achtergrond uitvoeren** de optie **Batchverwerking** in op *Ja*.
1. Selecteer **Terugkeerpatroon** en stel de planning naar wens in.
1. Selecteer **OK** om de planning op te slaan.
1. Selecteer **OK** om de batchtaak aan te maken en het dialoogvenster te sluiten.

## <a name="use-ctp-for-built-in-master-planning"></a>CTP gebruiken voor de ingebouwde hoofdplanning

### <a name="create-a-new-order-by-using-ctp-for-built-in-master-planning"></a>Een nieuwe order aanmaken met behulp van CTP voor de ingebouwde hoofdplanning

Telkens wanneer u een nieuwe verkooporder of orderregel toevoegt, wijst het systeem een standaardmethode voor het controleren van de leveringsdatum toe. De header van de order begint altijd met de algemene standaardmethode. Als een overschrijving is toegewezen aan een besteld artikel, gebruikt de nieuwe orderregel die overschrijving. Anders wordt voor de nieuwe orderregel ook de algemene standaardmethode gebruikt. Daarom moeten de standaardmethoden zo worden ingesteld dat ze overeenkomen met de controlemethode voor leveringsdatum die u het meest wilt gebruiken. Nadat u een order hebt aangemaakt, kunt u de standaardmethode waar nodig overschrijven op het niveau van de header van de order en/of orderregel. Raadpleeg [Standaardmethodes om de leveringsdatum te controleren, instellen](#default-methods) en [Bestaande verkooporders wijzigen voor gebruik van CTP](#change-orders) voor meer informatie.

### <a name="view-confirmed-delivery-dates-when-you-use-ctp-for-built-in-master-planning"></a>Bevestigde leveringsdatums bekijken wanneer u CTP gebruikt voor ingebouwde hoofdplanning

Als u de ingebouwde hoofdplanning-engine gebruikt, worden CTP-berekeningen toegepast op orders en/of orderregels waarbij het veld **Controle leveringsdatum** is ingesteld op *CTP*.

Voor verkoopregels die gebruikmaken van CTP voor ingebouwde hoofdplanning stelt het systeem automatisch de velden **Bevestigde verzenddatum** en **Bevestigde ontvangstdatum** automatisch bijgewerkt telkens wanneer u een verkoopregel opslaat. Als u later een relevante wijziging aan een verkoopregel aanbrengt (bijvoorbeeld door de hoeveelheid of locatie te wijzigen), worden de datums onmiddellijk opnieuw berekend.

- Als u de bevestigde leveringsdatums voor een verkooporderregel wilt weergeven, opent u de verkooporder en selecteert u de verkoopregel. Controleer vervolgens op het sneltabblad **Regeldetails** op het tabblad **Levering** de waarden voor **Bevestigde verzenddatum** en **Bevestigde ontvangstdatum**.
- Als u de bevestigde leveringsdatums voor een volledige order wilt weergeven, opent u de verkooporder en selecteert u de weergave **Header**. Controleer vervolgens op het sneltabblad **Levering** de waarden voor **Bevestigde verzenddatum** en **Bevestigde ontvangstdatum**.

## <a name="use-ctp-for-planning-optimization"></a>CTP voor Planningsoptimalisatie gebruiken

### <a name="create-a-new-order-by-using-ctp-for-planning-optimization"></a>Een nieuwe order aanmaken met behulp van CTP voor Planningsoptimalisatie

Telkens wanneer u een nieuwe verkooporder of orderregel toevoegt, wijst het systeem een standaardmethode voor het controleren van de leveringsdatum toe. De header van de order begint altijd met de algemene standaardmethode. Als een overschrijving is toegewezen aan een besteld artikel, gebruikt de nieuwe orderregel die overschrijving. Anders wordt voor de nieuwe orderregel ook de algemene standaardmethode gebruikt. Daarom moeten de standaardmethoden zo worden ingesteld dat ze overeenkomen met de controlemethode voor leveringsdatum die u het meest wilt gebruiken. Nadat u een order hebt aangemaakt, kunt u de standaardmethode waar nodig overschrijven op het niveau van de header van de order en/of orderregel. Raadpleeg [Standaardmethodes om de leveringsdatum te controleren, instellen](#default-methods) en [Bestaande verkooporders wijzigen voor gebruik van CTP](#change-orders) voor meer informatie.

### <a name="view-confirmed-delivery-dates-when-using-ctp-for-planning-optimization"></a>Bevestigde leveringsdatums bekijken bij gebruik van CTP voor Planningsoptimalisatie

Als u Planningsoptimalisatie gebruikt, worden CTP-berekeningen toegepast op orders en/of orderregels waarbij het veld **Controle leveringsdatum** is ingesteld op *CTP voor Planningsoptimalisatie*.

Voor verkoopregels die gebruikmaken van CTP voor Planningsoptimalisatie zijn de velden **Bevestigde verzenddatum** en **Bevestigde ontvangstdatum** leeg totdat u het juiste dynamische plan hebt uitgevoerd (meestal via een periodieke batchtaak). Deze worden vervolgens automatisch ingesteld. Raadpleeg [CTP voor planningsoptimalisatieberekeningen plannen](#batch-job) voor meer informatie.

Met het veld **Status CTP voor Planningsoptimalisatie** wordt aangegeven of er nog bevestigde datums zijn berekend voor elke regel die gebruikmaakt van CTP voor Planningsoptimalisatie. Het veld bevat de waarde *Niet gereed* voor regels en orders waar de bevestigde leveringsdatums nog niet zijn berekend of niet meer geldig zijn vanwege andere wijzigingen. Het geeft een waarde *Gereed* aan voor regels en orders die zijn berekend. U kunt de status voor elke regel en voor de gehele order weergeven.

- Als u de status voor een verkooporderregel wilt weergeven, opent u de verkooporder en selecteert u de verkoopregel. Controleer vervolgens op het sneltabblad **Regeldetails** op het tabblad **Levering** de waarde van **Status CTP voor planningsoptimalisatie**. De velden **Bevestigde verzenddatum** en **Bevestigde ontvangstdatum** voor de regel worden ook weergegeven op dit tabblad nadat deze zijn berekend.
- Als u de status voor een volledige order wilt weergeven, opent u de verkooporder en selecteert u de weergave **Header**. Controleer vervolgens op het sneltabblad **Levering** de waarde van **Status CTP voor planningsoptimalisatie**. De **Bevestigde verzenddatum** en **Bevestigde ontvangstdatum** voor de order worden ook weergegeven op dit tabblad nadat deze zijn berekend.

<!-- KFM: The following text may be untrue and needs to be reviewed with the PM for next revision:

The sales orders that are *Ready* or *Not ready* are shown in the **All sales orders** list page. You can check the sales order that are *Ready* or *Not ready* from the sales order list page by filtering on this new status field.

-->

> [!NOTE]
> - Als u een verkooporderregel bij werkt nadat via CTP voor planningsoptimalisatie bevestigde datums zijn berekend, worden deze datums gewist totdat het toepasselijke dynamische plan de volgende keer wordt uitgevoerd.
> - Als u een gerelateerde instelling bewerkt die van invloed kan zijn op bestaande bevestigde datums (bijvoorbeeld door doorlooptijden, reserveringen of markeringen te wijzigen), moet u de bevestigde datums voor de relevante bestaande orders leeg maken. Door deze actie wordt de status van elke relevante regel gewijzigd in *Niet gereed*. Door deze wijziging kan het systeem de bevestigde datums opnieuw berekenen als het het dynamische plan de volgende keer wordt uitgevoerd.

## <a name="change-existing-sales-orders-so-that-they-use-ctp"></a><a name="change-orders"></a>Bestaande verkooporders wijzigen zodat deze gebruikmaken van CTP

U kunt op elk gewenst moment de waarde van **Controle leveringsdatum** voor elke openstaande order wijzigen. U kunt de waarde naar wens wijzigen op header-niveau en/of voor elke regel.

### <a name="change-to-ctp-at-the-order-header-level"></a>Wijzigen in CTP op het niveau van de header van de order

<!-- KFM: Would be nice to mention how changing this setting on the header affects the individual lines. -->

Als u een order wilt wijzigen zodat CTP wordt gebruikt op header-niveau, voert u de volgende stappen uit.

1. Ga naar **Klanten \> Orders \> Alle verkooporders**.
1. Open de verkooporder die u wilt instellen of maak een nieuwe aan.
1. Selecteer **Header** op de pagina **Details verkooporder** om de header-informatie te openen.
1. Stel op het sneltabblad **Levering** het veld **Controle leveringsdatum** in op een van de volgende waarden, afhankelijk van de planning-engine die u gebruikt:

    - *CTP* : gebruik de CTP-berekening die wordt geleverd door de ingebouwde hoofdplanning-engine. Als u Planningsoptimalisatie gebruikt, is de controlemethode voor de leveringsdatum *CTP* niet toegestaan. Als u deze waarde selecteert, treedt er daarom een fout op bij het uitvoeren van de berekening.
    - *CTP voor planningsoptimalisatie*: gebruik de CTP-berekening die wordt geleverd door Planningsoptimalisatie. Deze instelling heeft geen effect als u de ingebouwde hoofdplanning-engine gebruikt.

<!-- KFM: Additional dialogs are shown here. Review these with the PM and expand this procedure at next revision. -->
1. Selecteer **OK** om de wijzigingen toe te passen.

### <a name="change-to-ctp-at-the-order-line-level"></a>Wijzigen naar CTP op het niveau van de orderregel

Als u een orderregel hebt aangemaakt met behulp van een andere controlemethode voor leveringsdatums, kunt u op elk moment naar CTP wijzigen. Wijzigingen die u aanbrengt op regelniveau hebben geen invloed op andere regels. Deze kunnen er echter toe leiden dat de algehele leveringsdatums van de order naar voren of naar achteren worden verplaatst, afhankelijk van hoe elke bijgewerkte regelberekening wijzigt. <!-- KFM: Confirm this intro at next revision -->

Als u een order wilt wijzigen zodat CTP voor de ingebouwde hoofdplanning wordt gebruikt op regelniveau, voert u de volgende stappen uit.

1. Ga naar **Klanten \> Orders \> Alle verkooporders**.
1. Open de verkooporder die u wilt instellen of maak een nieuwe aan.
1. Selecteer op de pagina **Details verkooporder** op het sneltabblad **Verkooporderregel** de verkooporderregel die u wilt instellen.
1. Stel op het sneltabblad **Regeldetails** op het tabblad **Levering** het veld **Controle leveringsdatum** in op een van de volgende waarden, afhankelijk van de planning-engine die u gebruikt:

    - *CTP* : gebruik de CTP-berekening die wordt geleverd door de ingebouwde hoofdplanning-engine. Als u Planningsoptimalisatie gebruikt, is de controlemethode voor de leveringsdatum *CTP* niet toegestaan. Als u deze waarde selecteert, treedt er daarom een fout op bij het uitvoeren van de berekening.
    - *CTP voor planningsoptimalisatie*: gebruik de CTP-berekening die wordt geleverd door Planningsoptimalisatie. Deze instelling heeft geen effect als u de ingebouwde hoofdplanning-engine gebruikt.

    Het dialoogvenster **Beschikbare verzend- en ontvangstdatums** wordt weergegeven en geeft de beschikbare verzend- en ontvangstdatums weer. Dit dialoogvenster werkt op dezelfde manier voor orderregels als voor de order-header, zoals is beschreven in het vorige gedeelte.

1. Selecteer **Opslaan** in het actievenster.
