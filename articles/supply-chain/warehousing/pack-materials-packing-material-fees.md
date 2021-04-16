---
title: Verpakkingsmaterialen en -kosten
description: Dit onderwerp bevat informatie over de kosten voor verpakkingsmateriaal die met specifieke intervallen worden betaald aan recyclingbedrijven.
author: MarkusFogelberg
ms.date: 02/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventPackagingGroup, InventPackagingMaterialCode, InventPackagingMaterialFee, InventPackagingMaterialTrans, InventPackagingMaterialTransPurch, InventPackagingUnit
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2194
ms.assetid: 040b65dc-43c9-4256-b69f-b2d6e736fbe9
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2020-02-19
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b37e61a3c48d646dce9007229fcb7fa4ecde45a8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816335"
---
# <a name="packing-materials-and-fees"></a>Verpakkingsmaterialen en -kosten

[!include [banner](../includes/banner.md)]

De kosten voor verpakkingsmateriaal worden met specifieke intervallen aan een recyclingbedrijf betaald. Een bedrag per gewichtseenheid moet worden betaald voor het materiaal waarvan de verpakking is gemaakt. Hoewel de kosten voor verpakkingsmateriaal worden berekend en gerapporteerd, worden er geen grootboektransacties geboekt, omdat de kosten niet als een belastingheffing worden beschouwd die aan de overheid moet worden afgedragen.

Het gewicht en de kosten van het verpakkingsmateriaal worden voor zowel verkoop- als inkooporderregels berekend.

U kunt een of meer verpakkingseenheden definiëren voor een enkel artikel, voor een groep van artikelen (verpakkingsgroep) of voor alle artikelen. Een verpakking bestaat uit de verschillende verpakkingsmaterialen en het gewicht daarvan plus het aantal artikelen in de verpakking. Een verpakkingsmateriaalcode wordt toegewezen aan elk type verpakkingsmateriaal dat is gedefinieerd. Op basis van de verpakkingsmateriaalcode kunt u een prijs opgeven voor een bepaalde periode. De kosten van het verpakkingsmateriaal worden berekend op basis van deze informatie.

> [!NOTE]
> Ook als er door uw bedrijf geen kosten voor verpakkingsmateriaal worden betaald, kunt u toch met deze functie statistieken voor het gewicht van het verpakkingsmateriaal berekenen.

## <a name="set-up-packing-material-allocation"></a><a name="allocations"></a>Toewijzing van verpakkingsmateriaal instellen

Voordat u het gewicht van het verpakkingsmateriaal, kosten voor verpakkingsmateriaal of beide kunt berekenen, moet u de berekening inschakelen en definiëren welke materialen en kosten gelden voor welke artikelen.

1. Ga naar **Voorraadbeheer \> Instellen \> Parameters voor voorraad- en magazijnbeheer**.
1. Stel op het tabblad **Algemeen** in de sectie **Verpakkingsmateriaal** de optie **Verpakkingsmateriaalkosten berekenen** in op **Ja**.
1. Ga naar **Voorraadbeheer \> Instellen \> Verpakkingsmateriaal \> Verpakkingsgroepen** en maak alle verpakkingsgroepen die u gebruikt. Voor alle artikelen in een verpakkingsgroep wordt dezelfde verpakkingsmateriaaltoewijzing gebruikt. Als u geen verpakkingsgroepen gebruikt, kunt u deze stap overslaan.

    > [!TIP]
    > Nadat u de verpakkingsgroepen hebt gemaakt, kunt u een groep toewijzen aan elk product dat u nodig hebt. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**, selecteer een product en selecteer vervolgens op het sneltabblad **Voorraad beheren** in het veld **Verpakkingsgroep** de toepasselijke verpakkingsgroep.

1. Ga naar **Voorraadbeheer \> Instellen \> Verpakkingsmateriaal \> Verpakkingsmateriaalcodes**, definieer elk type verpakkingsmateriaal dat u gebruikt en geef de eenheid op waarin het verpakkingsmateriaal wordt verbruikt wanneer u zendingen voorbereidt.
1. Ga naar **Voorraadbeheere \> Instellen \> Verpakkingsmateriaal \> Verpakkingsmateriaalkosten** en stel kosten in voor elk type verpakkingsmateriaal dat u zojuist hebt gedefinieerd. Kosten worden berekend op basis van de prijs per eenheid die is verbruikt.
1. Als u verpakkingsmaterialen aan artikelen wilt toewijzen, gaat u naar **Voorraadbeheer \> Instellen \> Verpakkingsmateriaal \> Toewijzing verpakkingsmateriaal** en maakt u toewijzingen. U kunt zoveel toewijzingen maken als nodig zijn. U kunt verpakkingsmaterialen toewijzen voor afzonderlijke artikelen, groepen artikelen (verpakkingsgroepen) of alle artikelen, afhankelijk van hoe gedetailleerd uw toewijzingen moeten zijn.

    Volg deze stappen voor elke toewijzing die u maakt.

    1. Stel op het sneltabblad **Algemeen** de volgende velden in:

        - **Artikelcode**: selecteer het bereik van de toewijzing:

            - **Tabel**: maak een toewijzing voor een enkel specifiek artikel.
            - **Groep**: maak een toewijzing voor alle artikelen die behoren tot een verpakkingsgroep die is gedefinieerd op de pagina **Verpakkingsgroepen**.
            - **Alle**: maak een toewijzing voor alle artikelen.

            > [!NOTE]
            > Normaal gesproken moet u al uw toewijzingen op hetzelfde niveau (**Tabel**, **Groep** of **Alle**) maken. Als u meer dan één niveau gebruikt, wordt de meest specifieke toewijzing voor elk artikel gebruikt. (Het niveau **Tabel** heeft voorrang op het niveau **Groep** en beide niveaus hebben voorrang op het niveau **Alle**.)

        - **Artikelrelatie**: selecteer het artikel als u toewijst voor een enkel artikel. Als u toewijst voor een groep artikelen, selecteert u de verpakkingsgroep. Als u toewijst voor alle artikelen, laat u dit veld leeg.
        - **Configuratie**, **Grootte**, **Kleur** en **Stijl**: voer naar behoefte waarden in voor deze dimensies om het artikel dat u toewijst verder te definiëren.
        - **Verpakkingseenheid**: selecteer de eenheid waarin het artikel wordt verpakt wanneer het verpakkingsmateriaal wordt gebruikt. Deze eenheid kan verschillen van de eenheid waarin het artikel is ingekocht en opgeslagen.
        - **Factor voor verpakkingseenheid**: voer de omrekeningsfactor in die wordt gebruikt om van de voorraadeenheid naar de verpakkingseenheid te converteren. (Bij de conversie wordt de formule *Verpakkingseenheden* = *Artikeleenheden* × *Factor voor verpakkingseenheid* gebruikt.)

    1. Voeg op het sneltabblad **Verpakkingsmateriaal** een regel toe voor elk verpakkingsmateriaal dat voor de huidige toewijzing is vereist. Geef op elke regel het type materiaal op (zoals gedefinieerd op de pagina **Verpakkingsmateriaalcodes**) en de hoeveelheid die wordt verbruikt voor elke verzonden eenheid van het huidige artikel.

## <a name="packing-units-on-sales-order-lines"></a>Verpakkingseenheden op verkooporderregels

Nadat u de [berekening voor verpakkingsmateriaalkosten hebt ingeschakeld en uw toewijzingen hebt ingesteld](#allocations), controleert het systeem of de verpakkingseenheden zijn opgegeven voor elk artikel dat aan een verkooporder wordt toegevoegd. Vervolgens worden alle vereiste kosten berekend. Wanneer een artikel aan een verkooporder wordt toegevoegd, vindt een van de volgende stappen plaats:

- **Als een toewijzing van een verpakkingmateriaal geldt voor het artikel:** het systeem werkt de verkooporderregel bij met de opgegeven verpakkingseenheid en de hoeveelheid van de verpakkingseenheid. (De hoeveelheid van de verpakkingseenheid wordt berekend via de formule *Hoeveelheid voor verpakkingseenheden* = *Bestelde hoeveelheid* ÷ *Aantal artikelen in de geselecteerde verpakkingseenheid*.)
- **Als er geen toewijzing van een verpakkingmateriaal geldt voor het artikel:** u kunt handmatig een verpakkingseenheid en de hoeveelheid van de verpakkingseenheid op de verkooporderregel invoeren.

U kunt de verpakkingseenheid en de hoeveelheid van de verpakkingseenheid bij het boeken van de verkooporderregel wijzigen. Deze mogelijkheid is van belang als de verkooporderregel alleen gedeeltelijk is geleverd of gefactureerd.

Wanneer u de verkooporder factureert, worden de verpakkingsmateriaaltransacties gemaakt in het systeem. Verpakkingsmateriaaltransacties bevatten de gewichten van de verpakkingsmaterialen voor de verkoopregel. U kunt de transacties wijzigen nadat u ze hebt gefactureerd. U kunt vervolgens nieuwe transacties maken.

## <a name="packing-units-on-purchase-order-lines"></a>Verpakkingseenheden op inkooporderregels

Het systeem maakt geen verpakkingsmateriaaltransacties voor inkooporderregels. In plaats daarvan kunt u handmatig transacties maken voor gefactureerde inkooporderregels op de pagina **Verpakkingsmateriaaltransacties**.

## <a name="set-up-license-numbers-for-customers-that-are-charged-packing-material-fees"></a>Licentienummers instellen voor klanten aan wie verpakkingsmateriaalkosten in rekening worden gebracht

Als de verkooporders voor een bepaalde klant kosten moeten bevatten voor de verpakkingsmaterialen die voor elke order worden gebruikt, voert u de volgende stappen uit.

1. Ga naar **Klanten \> Klanten \> Alle klanten**.
1. Selecteer de klant aan wie verpakkingsmaterialen in rekening moeten worden gebracht.
1. Stel op het sneltabblad **Factuur en levering** de volgende velden in:

    - Voer in de sectie **Btw** in het veld **Licentienummer van verpakkingsheffing** het licentienummer van het bedrijf in.
    - Voer in de sectie **Bijzondere verpakkingsmateriaalkosten** in het veld **Licentienummer** het licentienummer van het bedrijf in.

Wanneer u nu een verkooporder maakt en factureert die een of meer artikelen bevat waarvoor verpakkingsmaterialen worden gebruikt, worden in de factuur de verpakkingsmateriaalkosten weergegeven.

Voor klanten die geen verpakkingsmateriaalkosten hoeven te betalen, voert u dezelfde stappen uit, maar wist u de licentienummers in de velden **Licentienummer van verpakkingsheffing** en **Licentienummer**. Op facturen voor klanten die geen verpakkingsmateriaalkosten betalen, worden de gewichten van de verpakkingsmaterialen weergegeven, maar ontbreken de kosten.

Als u een rapport wilt genereren waarin alle verpakkingsmateriaalkosten worden weergegeven die uw bedrijf voor een bepaalde periode moet betalen, gaat u naar **Voorraadbeheer \> Query's en rapporten \> Verpakkingsmateriaalrapporten \> Berekening van verpakkingsmateriaalkosten**, geeft u een datumbereik op en selecteert u vervolgens **OK**.

## <a name="print-packing-material-weights-on-invoices"></a>Gewicht van verpakkingsmateriaal op facturen afdrukken

U kunt het gewicht van verpakkingsmaterialen op een factuur afdrukken en aangeven wie de bijbehorende kosten betaalt. De gewichten worden per verpakkingscode samengevat.

1. Ga naar **Klanten \> Instellen \> Parameters van module Klanten**.
1. Stel op het tabblad **Updates** op het sneltabblad **Factuur** de optie **Verpakkingsmateriaalgewicht afdrukken** in op **Ja**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]