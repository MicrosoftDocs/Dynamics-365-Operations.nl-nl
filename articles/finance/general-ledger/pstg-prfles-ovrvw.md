---
title: Overzicht van boekingsprofielen
description: In dit artikel wordt uitgelegd hoe boekingsprofielen worden gebruikt in Microsoft Dynamics 365-toepassingen.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemSetup, CustPosting, VendPosting, InventPosting, AssetPosting, ProjPosting, AssetLeasePostingAccounts, ProjCategory, ITMCostTypeTable, ProdGroup, WrkCtrTable, WrkCtrResourceGroup
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 91078352b6376ee99e7d9ce4546ed200cb80a25a
ms.sourcegitcommit: 6b209919de39c15e0ebe4abc9cbcd30618f2af0b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135838"
---
# <a name="posting-profiles-overview"></a>Overzicht van boekingsprofielen

In apps voor financiën en bedrijfsactiviteiten wordt de term *boekingsprofielen* gebruikt om de configuraties te beschrijven die bepalen hoe subgrootboekrekeningen worden geconverteerd naar hoofdrekeningen, zodat ze kunnen worden gebruikt in transacties die naar het grootboek worden geboekt. Deze bepalen bijvoorbeeld hoe de klant wordt geconverteerd naar een hoofdrekening in Klanten wanneer een factuur wordt geboekt.

Sommige modules en functies hebben een pagina met de woorden 'boekingsprofiel' in de naam (bijvoorbeeld **Klantboekingsprofiel** of **Leveranciersboekingsprofiel**). Bovendien bevatten sommige modules meerdere opties voor het configureren van boekingen in het grootboek voor transacties die worden gegenereerd uit de subadministratie. In de module **Productiecontrole** kunt u bijvoorbeeld het boeken per productiegroep, resource of resourcegroep instellen.

Voor veel transactietypen is er een alternatief voor boekingsprofielen: boekingsdefinities. Voor ondersteunde documenten kunt u boekdefinities in plaats van boekingsprofielen gebruiken om hoofdrekeningen en financiële dimensies voor boekhoudvermeldingen te classificeren. Als u van plan bent om vorderingen of voorvorderingen gebruiken, is een boekingsdefinitie vereist om de rekeningen voor de boekhoudingsposten te definiëren.

Voordat u de boekingsprofielen, boekingsdefinities of de pagina **Rekeningen voor automatische transacties** kunt configureren, moet u het rekeningschema configureren op de **grootboekpagina** in de rechtspersoon die u wilt configureren.

## <a name="posting-types"></a>Boekingstypen

In apps voor financiën en bedrijfsactiviteiten wordt een boekingstype gebruikt om een algemene categorie voor debet of credit te definiëren. Deze categorie is onafhankelijk van de hoofdrekening in het grootboek. Er zijn boekingstypen voor elke debet- of creditpost in het grootboek.

Eén boekstuk kan een of meer boekingstypen hebben. Een transactie die bijvoorbeeld wordt geboekt via een algemeen journaal waarin de rekening en tegenrekening zijn ingesteld op **Grootboek**, heeft het boekingstype **Grootboekjournaal** voor zowel debet als credit. Een leveranciersfactuur heeft daarentegen meerdere boekingstypen. Die boekingstypen omvatten één regel voor het leveranciersaldo en extra regels voor de tegenboeking, zoals **Grootboekjournaal**.

U kunt het boekingstype het veld **Boekingstype** bekijken op het tabblad **Algemeen** van de pagina **Boekstuktransacties**.

> [!TIP]
> Met de werkbalk **Aanpassen** kunt u het veld **Boekingstype** toevoegen aan het raster op het tabblad **Overzicht** of verplaatsen. Op deze manier kunt u dit veld toegankelijk maken of weergeven wanneer u boekstukken bekijkt.

## <a name="detail-settings-for-a-posting-profile"></a>Gedetailleerde instellingen voor een boekingsprofiel 

Wanneer u boekingsprofielen configureert, definieert u met het veld **Rekeningcode** het niveau van de instelling. De volgende opties zijn beschikbaar: **Tabel**, **Groep** en **Alle**. De afstemming stopt na de eerste overeenkomst en de volgorde ligt tussen het meest specifieke niveau en het minst specifieke niveau. Hoewel het veld **Rekeningcode** in sommige gevallen een iets andere naam heeft, blijven het gedrag en de functie van het veld hetzelfde. Het voorraadboekingsprofiel bevat bijvoorbeeld een veld **Artikelcode** en een veld **Rekeningcode**. Beide velden hebben de waarden **Tabel**, **Groep** en **Alle**.

Als het veld **Hoofdrekening** leeg is voor een boekingsprofiel en u geen hoofdrekening hebt geconfigureerd op de pagina **Rekeningen voor automatische transactie** of op een modulespecifieke of functiespecifieke pagina, ontvangt u een foutbericht wanneer u een transactie boekt die het boekingstype gebruikt. Normaal is het bericht "De rekening voor \[het boekingstype\] kan niet worden gevonden".

### <a name="table-value"></a>Tabelwaarde

De **tabel** waarde verwijst naar de hoofdrecord die aan het boekingsprofiel is gekoppeld. Elke tabelrecord heeft één waarde. U geeft de waarde op in het veld dat na het veld **Rekeningcode** wordt weergegeven. Normaal gesproken heeft dit veld de naam **Rekening** of **Rekening/groepsnummer**. De exacte naam is afhankelijk van de pagina waarop deze wordt weergegeven.

Als u bijvoorbeeld werkt met een boekingsprofiel van een klant, vertegenwoordigt de waarde **Tabel** een bepaalde klant. Als u **Tabel** selecteert in het veld **Rekeningcode**, selecteert u daarom het klantnummer in het veld **Rekening/groepsnummer**.

De **tabel** waarde vertegenwoordigt het meest specifieke recordtype. Deze waarde wordt altijd gebruikt, zelfs als u een andere record hebt geconfigureerd waarin de waarde **Groep** of **Alle** is geselecteerd. Deze waarde heeft ook voorrang boven de waarden die u als standaardwaarden hebt ingesteld op de pagina **Rekeningen voor automatische transacties**.

Het is niet aan te raden de **tabelwaarde** als het primaire mechanisme voor het beheer van boekingsprofielen te gebruiken, omdat kwaliteitsproblemen met gegevens kunnen optreden als voor elke hoofdgegevensrecord een afzonderlijk boekingsprofiel wordt onderhouden. Het is ook lastig om een afzonderlijk boekingsprofiel voor elke hoofdgegevensrecord te onderhouden en af te stemmen. In plaats daarvan moet deze waarde worden gebruikt om uitzonderingen in uw boekingsprofielen te beheren.

### <a name="group-value"></a>Groepswaarde

De **groepswaarde** verwijst naar de groeperingsrecord die wordt ondersteund door de hoofdrecord die aan het boekingsprofiel is gekoppeld. Elke groepsrecord heeft één waarde. U geeft de waarde op in het veld dat na het veld **Rekeningcode** wordt weergegeven. Normaal gesproken heeft dit veld de naam **Rekening** of **Rekening/groepsnummer**. De exacte naam is afhankelijk van de pagina waarop deze wordt weergegeven.

Voor de **groepswaarde** moet u eerst een groep configureren en deze aan een of meer records voor de rekening koppelen. De waarde **Groep** is minder specifiek dan de waarde **Tabel**, maar specifieker dan de waarde **Alle**. Als er geen record voor een tabel is geconfigureerd, probeert het systeem een record te zoeken voor de groep waar de record bij hoort.

Als u bijvoorbeeld werkt met een klantboekingsprofiel en u **Groep** selecteert in het veld **Rekeningcode**, moet u een klantengroep selecteren in het veld **Rekening-/groepsnummer**. U moet de klantengroepen vooraf instellen op de pagina **Klantengroep** en u moet een klantengroep opgeven wanneer u een klant maakt.

Als u meerdere hoofdrekeningen moet bijhouden voor een bepaald boekingstype, raden we u aan de waarde **Groep** te gebruiken. U hebt bijvoorbeeld drie hoofdhandelsrekeningen voor Klanten: een voor normale klanten, een voor werknemers en een voor intercompany-verkoop. In dit geval is het raadzaam om drie klantengroepen te maken om de klanten te segmenteren. Wijs vervolgens elke klantengroep toe aan de juiste hoofdrekening in het boekingsprofiel van de klant. In de volgende tabel ziet u de drie klantengroepen voor dit voorbeeld.

| Klantgroep | Name | Description |
|----------------|------|-------------|
| EXT | Externe klant | Deze groep wordt gebruikt voor alle standaardklanten buiten het bedrijf. |
| EMP | Werknemers | Deze groep wordt gebruikt voor alle werknemers die inkopen doen vanuit uw organisatie. |
| INT | Intercompany-verkoop | Deze groep wordt gebruikt voor alle intercompany-klantrekeningen die worden gebruikt met integratieverkoop- en inkooporders. |

In het boekingsprofiel stelt u vervolgens drie regels in. Op elke regel selecteert u de waarde **Groep** en de bijbehorende hoofdrekening.

### <a name="all-value"></a>De waarde Alle

De waarde **Alle** geeft aan dat de instellingen van toepassing zijn op alle records. Als u de waarde **Alle** selecteert in het veld **Rekeningcode**, is het veld **Rekening/groepsnummer** niet beschikbaar en kunt u geen specifieke record selecteren om de configuratie op toe te passen.

De waarde **Alle** is de minst specifieke waarde. Deze wordt alleen gebruikt als er geen overeenkomst kan worden gevonden voor de waarde **Tabel** of **Groep**. U moet de waarde **Alle** selecteren als u slechts één hoofdrekening hebt voor een bepaald boekingstype.

Als u bijvoorbeeld met een klantboekingsprofiel werkt, zijn de opgegeven hoofdrekeningen van toepassing op alle andere klanten en klantengroepen die geen registratie hebben voor een specifieke tabel (klant) of groep (klantengroep).

### <a name="category"></a>Categorie

Voorraadboekingsprofielen hebben een extra waarde die specifiek is voor de verkoopcategorie of aanschaffingscategorie. Deze waarde lijkt op de waarde **Tabel**, omdat deze alleen van toepassing is op een bepaalde verkoop- of aanschaffingscategorie.

### <a name="default-value"></a>Standaardwaarde

Als u geen record maakt voor een boekingstype in een boekingsprofiel waarin het veld **Rekeningcode** is ingesteld op **Alle** en het systeem geen overeenkomende boekingsprofielrecord kan vinden voor de waarde **Groep** of **Tabel**, wordt de standaardwaarde teruggedraaid naar de standaardwaarde die kan worden opgegeven op de pagina **Rekeningen voor automatische transactie**. Zie [Rekeningen voor automatische transacties](accounts-for-auto-transactions.md) voor meer informatie.

## <a name="clearing-accounts"></a>Vereffeningsrekeningen

De term *vereffeningsrekening* wordt vaak gebruikt in de boekhouding. Sommige boekingstypen in Microsoft Dynamics 365-toepassingen zijn vereffeningsrekeningen. Met andere woorden, het saldo van de rekening wordt vereffend of omgekeerd wanneer er een andere transactie wordt geboekt. Wanneer u bijvoorbeeld een productontvangstbon van een inkooporder boekt, wordt de som van de geraamde kosten van de producten plus de btw en eventuele toeslagen op de inkooporderregels naar het boekingstype inkooptoerekening geboekt als een schuld. Wanneer u de inkooporder later factureert, wordt het saldo teruggeboekt van het boekingstype inkoopordertoerekening en verplaatst naar de handelsrekening Leveranciers.

## <a name="additional-resources"></a>Aanvullende bronnen

Veel modules in Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce en Dynamics 365 Project Operations hebben een boekingsprofiel of aanvullende configuraties die bepalen hoe boekingen naar grootboek werken. Gebruik de volgende onderwerpen voor meer informatie over de boekingsprofielen en boekingsinstellingen in elke module:

- [Rekeningen voor automatische transacties](accounts-for-auto-transactions.md)
- [Boeken voor Leveranciers](accts-payble-posting.md)
- [Boeken voor Klanten](accts-recvble-posting.md)
- [Activaleases boeken](../asset-leasing/set-up-lease-posting-accts.md)
- Activabeheer boeken (binnenkort beschikbaar)
- Contanten en bankbeheer (binnenkort beschikbaar)
- Boekingsrekeningen voor valutaherwaardering (binnenkort beschikbaar)
- Onkostenbeheer boeken (binnenkort beschikbaar)
- [Boekingsprofiel vaste activa](../fixed-assets/tasks/set-up-fixed-asset-posting-profiles.md)
- Boekingen voor Intercompany-boekhouding (binnenkort beschikbaar)
- [Voorraadboeking](inventory-posting.md)
- [Boeken van francoprijzen](../../supply-chain/landed-cost/costing-parameters-setup.md)
- [Overzicht van boekingsdefinities](posting-definitions.md)
- [Productieboeking](production-posting.md)
- Boeken voor Projectbeheer en boekhouding (binnenkort beschikbaar)
- Boeken voor Servicebeheer (binnenkort beschikbaar)
- Boeken voor belasting (binnenkort beschikbaar)
- Boeken voor Tijd en aanwezigheid (binnenkort beschikbaar)
- Boeken voor Transportbeheer (binnenkort beschikbaar)
- Boekingsprofielen voor kortingsbeheer (binnenkort beschikbaar)

