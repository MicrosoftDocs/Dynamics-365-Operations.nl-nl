---
title: Transactieopties voor vaste activa
description: In dit onderwerp worden de beschikbare methoden voor het maken van vaste-activatransacties beschreven.
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6362a63bca43b5ac8da14becf6b966e459365ce1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552736"
---
# <a name="fixed-asset-transaction-options"></a>Transactieopties voor vaste activa

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de beschikbare methoden voor het maken van vaste-activatransacties beschreven.

U kunt vaste activa instellen voor integratie met crediteuren, debiteuren, inkoop en sourcing en grootboek. Ook kunt u artikelen in voorraadbeheer overbrengen naar vaste activa als u deze items intern gebruikt.

## <a name="accounts-payable"></a>Leveranciers    
U kunt transacties voor vaste activa invoeren op de pagina Journaalboekstuk. Deze pagina kan worden geopend vanuit de pagina Factuurjournaal. U kunt de pagina Journaalboekstuk ook openen via de pagina Factuurgoedkeuringsjournaal. Selecteer Vaste activa in het veld Tegenrekeningtype. Selecteer vervolgens een nummer voor vaste activa in het veld Tegenrekening. Voer op het tabblad Vaste activa waarden in het veld Transactietype en Boek in.

## <a name="accounts-receivable"></a>Klanten  
U kunt transacties voor vaste activa invoeren op de pagina Vrije-tekstfactuur.  Selecteer een regelartikel op de pagina Vrije-tekstfactuur in het raster met factuurregels. Klik op het sneltabblad Regeldetails. Geef het VA-nummer en boek op voor de afboekingstransactie. Voor facturen met vrije tekst is het vaste-activatransactietype altijd Verkoop/afstoting.

## <a name="procurement-and-sourcing"></a>Inkoopbeheer
U kunt transacties voor vaste activa invoeren op de pagina Inkooporder. Voer de vereiste informatie in om een inkooporder te maken en klik op OK. Klik op de pagina Inkooporder op het sneltabblad Regeldetails. Geef vervolgens op het tabblad Vaste activa informatie op over het vaste activum. 

Om een verwervingstransactie voor een bestaand vast activum te boeken, geeft u het VA-nummer, het boek en het transactietype op. Het vaste activum kan niet worden geboekt als deze informatie ontbreekt. U boekt een verwervingstransactie voor een nieuw vast activum door het selectievakje Nieuw vast activum? in te schakelen en de vaste-activagroep te selecteren waaraan het nieuwe activum moet worden toegewezen. Geen van de vaste-activavelden voor een regel zijn echter beschikbaar als het artikel zich in een voorraadmodelgroep bevindt die een standaardkostenvoorraadmodel gebruikt. Bovendien bepalen de opties die zijn gedefinieerd op de pagina Parameters vaste activa of u verwervingstransacties kunt boeken vanuit de inkoopmodules. 

Wanneer een inkooporder of het Voorraad naar vaste-activajournaal wordt gebruikt voor de verwerking van vaste activa, heeft dit gevolgen voor de voorraadwaarde.

## <a name="general-ledger"></a>Grootboek
Elk type vaste-activatransactie kan worden geboekt op de Algemeen journaal. Ook kunt u dagboeken gebruiken in vaste activa om VA-transacties te boeken.

## <a name="options-for-entering-fixed-asset-transaction-types"></a>Opties voor het invoeren van vaste-activatransactietypen


| Transactietype                    | Module                   | Opties                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| Verwerving, Correctie van verwerving | Vaste activa             | Vaste activa, Voorraad naar vaste activa   |
|                                     | Grootboek           | Algemeen journaal                           |
|                                     | Leveranciers             | Factuurjournaal, Factuurgoedkeuringsjournaal |
|                                     | Inkoopbeheer | Inkooporder                            |
| Afschrijving                        | Vaste activa             | Vaste activa                              |
|                                     | Grootboek           | Algemeen journaal                           |
| Afstoting                            | Vaste activa             | Vaste activa                              |
| ** **                               | Grootboek           | Algemeen journaal                           |
| ** **                               | Klanten        | Vrije-tekstfactuur                         |


De resterende waarde van de afschrijvingsperioden van het vaste activum wordt niet bijgewerkt wanneer een regel van een journaal van het type afschrijvingstransactie handmatig wordt gemaakt of wordt geïmporteerd door middel van een gegevensentiteit. Deze waarde wordt bijgewerkt wanneer het afschrijvingsvoorstelproces wordt gebruikt om de journaalregel te maken.

Zie [Integratie vaste activa](fixed-asset-integration.md) voor meer informatie.
