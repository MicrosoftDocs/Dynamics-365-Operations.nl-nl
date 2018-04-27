---
title: Verpakkingsmateriaal en kosten
description: De kosten van het verpakkingsmateriaal worden op regelmatige basis aan een recyclingbedrijf betaald. Een bedrag per gewichtseenheid moet worden betaald voor het materiaal waarvan de verpakking is gemaakt. Deze kosten voor verpakkingsmateriaal worden berekend en gerapporteerd, maar er worden geen grootboektransacties geboekt, omdat de kosten niet als een belastingheffing worden beschouwd die aan de overheid moet worden afgedragen.
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventPackagingGroup, InventPackagingMaterialCode, InventPackagingMaterialFee, InventPackagingMaterialTrans, InventPackagingMaterialTransPurch, InventPackagingUnit
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 2194
ms.assetid: 040b65dc-43c9-4256-b69f-b2d6e736fbe9
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b131cdfa2f0e3b6a8f116464323d49eaa4584634
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="packing-materials-and-fees"></a>Verpakkingsmateriaal en kosten

[!INCLUDE [banner](../includes/banner.md)]

De kosten van het verpakkingsmateriaal worden op regelmatige basis aan een recyclingbedrijf betaald. Een bedrag per gewichtseenheid moet worden betaald voor het materiaal waarvan de verpakking is gemaakt. Deze kosten voor verpakkingsmateriaal worden berekend en gerapporteerd, maar er worden geen grootboektransacties geboekt, omdat de kosten niet als een belastingheffing worden beschouwd die aan de overheid moet worden afgedragen.

Het gewicht en de kosten van het verpakkingsmateriaal worden voor zowel verkoop- als inkooporderregels berekend.

U definieert een of meer verpakkingseenheden voor een artikel, voor een verpakkingsgroep van artikelen of voor alle artikelen. Een verpakking bestaat uit de verschillende verpakkingsmaterialen en het gewicht daarvan plus het aantal artikelen in de verpakking. Een verpakkingsmateriaalcode wordt toegewezen aan elk type verpakkingsmateriaal dat is gedefinieerd. Op basis van de verpakkingsmateriaalcode kunt u een prijs opgeven voor een bepaalde periode. De kosten van het verpakkingsmateriaal worden berekend op basis van deze informatie.

| **Opmerking**                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ook als er door uw bedrijf geen kosten voor verpakkingsmateriaal worden betaald, kunt u toch met deze functie statistieken voor het gewicht van het verpakkingsmateriaal berekenen. |

## <a name="setup-requirements-for-packing-material-fees"></a>Vereisten voor het instellen verpakkingsmateriaalkosten
Voordat u het gewicht en/of de kosten van het verpakkingsmateriaal gaat berekenen, geeft u eerst de volgende basisgegevens op:

-   Verpakkingsgroepen: Maak verpakkingsgroepen en wijs die aan artikelen toe.
-   Verpakkingsmateriaalcodes: Maak verpakkingsmateriaalcodes voor elk type verpakkingsmateriaal dat is gedefinieerd.
-   Verpakkingseenheden: Geef een verpakkingseenheid op voor een artikel, voor een verpakkingsgroep of voor alle artikelen. Definieer voor elke verpakkingseenheid welk verpakkingsmateriaal moeten worden opgenomen, wijs gewichten toe en voer in het veld Factor voor verpakkingseenheid de omrekeningsfactor op van de voorraadeenheid.
-   Bijzondere verpakkingsmateriaalkosten: Geef de kosten van het verpakkingsmateriaal op per verpakkingsmateriaalcode. Voor elk type materiaal definieert u de geldigheidsperiode, de prijs per materiaal, de valuta en de eenheid.

## <a name="packing-units-on-sales-order-lines"></a>Verpakkingseenheden op verkooporderregels
Wanneer u een verkooporderregel maakt, controleert het systeem of er verpakkingseenheden voor het artikel zijn opgegeven. Als er verpakkingseenheden worden opgegeven, werkt het systeem de verkooporderregel bij met de opgegeven verpakkingseenheid en de hoeveelheid van de verpakkingseenheid. De hoeveelheid van de verpakkingseenheid is gebaseerd op de bestelde hoeveelheid gedeeld door het aantal artikelen in de geselecteerde verpakkingseenheid. Als er geen verpakkingseenheid is opgegeven, voert u zelf een verpakkingseenheid en de hoeveelheid van de verpakkingseenheid op de verkooporderregel in. U kunt de verpakkingseenheid en de hoeveelheid van de verpakkingseenheid bij het boeken van de verkooporderregel wijzigen. Dit is van belang als de verkooporderregel alleen gedeeltelijk is geleverd of gefactureerd. Wanneer u de verkooporder factureert, worden de verpakkingsmateriaaltransacties gemaakt. Verpakkingsmateriaaltransacties bevatten de gewichten van de verpakkingsmaterialen voor de verkoopregel. U kunt ook de transacties wijzigen nadat u deze factureert en nieuwe transacties maakt.

## <a name="packing-units-on-purchase-order-lines"></a>Verpakkingseenheden op inkooporderregels
Verpakkingsmateriaaltransacties voor een inkooporderregel zijn niet door het systeem gemaakt. U kunt handmatig transacties aanmaken voor gefactureerde inkooporderregels op de pagina **Verpakkingsmateriaaltransacties**.

## <a name="set-up-customer-packaging-material-fee-license-numbers"></a>Licentienummers van de klant voor de kosten van het verpakkingsmateriaal instellen
Als de klanten de kosten van het verpakkingsmateriaal betalen, geeft u op de pagina **Klanten** de licentienummers van de klanten voor de kosten van het verpakkingsmateriaal op. Wanneer er aan een klant een licentienummer is toegewezen, worden de kosten van het verpakkingsmateriaal automatisch berekend wanneer de verkooporders worden gefactureerd. Daarna wordt het selectievakje **Kosten berekenen** op de pagina **Verpakkingsmateriaaltransacties** uitgeschakeld, omdat u niet meer een rapport hoeft te berekenen en af te drukken. U kunt het gewicht van het verpakkingsmateriaal op de factuur afdrukken en de klanten laten weten dat zij de kosten dragen. 

Als uw bedrijf de kosten voor het verpakkingsmateriaal betaalt, geeft u de licentienummers van de klant niet op. Na facturering wordt het selectievakje **Kosten berekenen** ingeschakeld op de pagina **Verpakkingsmateriaaltransacties**. Hierdoor wordt aangegeven dat de kosten worden berekend wanneer een rapport wordt gemaakt. U kunt het gewicht van het verpakkingsmateriaal op de factuur afdrukken en aangeven dat de kosten door uw bedrijf worden betaald.

## <a name="print-packaging-material-weights-on-invoices"></a>Gewicht van verpakkingsmateriaal op facturen afdrukken
U kunt het gewicht van het verpakkingsmateriaal op de factuur afdrukken en aangeven wie de kosten voor het verpakkingsmateriaal moet betalen. De gewichten worden per verpakkingscode samengevat.






