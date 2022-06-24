---
title: Magazijnorders voor cloud- en randschaaleenheden
description: Dit artikel biedt informatie over de mogelijkheid voor magazijnorders die wordt gebruikt als onderdeel van de werkbelasting van de magazijnschaaleenheid.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: db254216e6c34b81f83c87a8fda454d0aeb1cece
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893521"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a>Magazijnorders voor cloud- en randschaaleenheden

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Niet alle bedrijfsfuncties worden volledig ondersteund in de openbare preview wanneer werkbelastingen voor schaaleenheden worden gebruikt. Als u schaaleenheden gebruikt, zorg ervoor dat u alleen de processen gebruikt die in dit artikel expliciet worden ondersteund.

## <a name="what-are-warehouse-orders"></a>Wat zijn magazijnorders?

*Magazijnorders* zijn een type order dat wordt gebruikt ter ondersteuning van magazijnimplementaties voor centrale punten en schaaleenheden. Hiermee kunt u voorraad ontvangen en verzenden wanneer u een magazijn-workload voor een schaaleenheid uitvoert.

Magazijnorders worden gebruikt als onderdeel van de verwerking van zowel inkomend als uitgaand magazijnbeheer. Ze worden aangemaakt als onderdeel van het proces *Vrijgave naar magazijn*, dat op het centrale punt wordt geïnitialiseerd.
Voor de inkomende verwerking wordt de Warehouse Mobile App gebruikt om fysiek voorhanden voorraad te registreren tijdens de verwerking van inkomende orders. Dit is beschikbaar voor inkoop- en productieorders die een magazijn met een schaaleenheid aangeven en artikelen waarvoor het gebruik van magazijnbeheerprocessen is ingeschakeld.
De uitgaande magazijnorders worden gebruikt als onderdeel van het verzendingswave-proces voor transfer- en verkooporders.

> [!IMPORTANT]
> Magazijnorders zijn alleen beschikbaar in implementaties waarin gebruik wordt gemaakt van de [werkbelastingen van magazijnbeheer voor cloud- en randschaaleenheden](cloud-edge-workload-warehousing.md).

## <a name="create-an-inbound-warehouse-order"></a>Een inkomende magazijnorder aanmaken

Volg deze stappen om een inkomende magazijnorder voor een inkooporderproces aan te maken.

1. Meld u aan bij het exemplaar van Microsoft Dynamics 365 Supply Chain Management dat op de hub wordt uitgevoerd. (U moet het proces *Vrijgeven aan magazijn* initiëren terwijl u bent aangemeld bij de hub.)
1. Ga naar **Inkoop en sourcing \> Inkooporders \> Alle inkooporders**.
1. Selecteer in het actievenster op het tabblad **Magazijn** in de groep **Acties** de optie **Vrijgeven aan magazijn**.
1. Als u de gerelateerde magazijnorderregels wilt weergeven, opent u de desbetreffende inkooporder, selecteert u een regel in de sectie **Inkooporderregels** en selecteert u op de werkbalk **Magazijn \> Magazijnorderregels**. Als u alle regels wilt weergeven, gaat u naar **Magazijnbeheer \> Query's en rapporten \> Magazijnorderregels**.

U kunt het proces *Vrijgeven naar magazijn* ook starten vanuit een batchtaak door naar **Magazijnbeheer > Vrijgave naar magazijn > Automatische vrijgave van inkooporders** te gaan. Wanneer u de batchtaak instelt, kunt u specifieke inkooporderregels selecteren op basis van een query. Een standaardscenario is het instellen van een terugkerende batchtaak waarbij alle bevestigde inkooporderregels worden vrijgegeven die naar verwachting de volgende dag zullen binnenkomen.

## <a name="cancel-a-warehouse-order"></a>Een magazijnorder annuleren

Als onderdeel van het proces *Vrijgave naar magazijn* worden voorraadtransacties van inkooporders gekoppeld aan magazijnorders en vergrendeld voor bijwerking door de hub. Als u per ongeluk naar een magazijn hebt vrijgegeven of als u een andere reden hebt om het maken van magazijnorderregels om te keren, kunt u aanvragen om magazijnorderregels te annuleren.

Volg de onderstaande stappen om magazijnorderregels te annuleren.

1. Meld u aan bij het exemplaar van Supply Chain Management dat op de hub wordt uitgevoerd.
1. Ga naar **Magazijnbeheer \> Query's en rapporten \> Magazijnorderregels**.
1. Selecteer de betreffende regel.
1. Selecteer **Magazijnorderregels annuleren** in het actievenster.

> [!NOTE]
> De aanvraag om regels te annuleren wordt geweigerd voor regels die al in afwachting zijn van annulering of die worden verwerkt in een magazijn waar de werkbelasting voor een schaaleenheid wordt uitgevoerd.

## <a name="monitor-a-warehouse-order"></a>Een magazijnorder bewaken

In de weergave **Magazijnorderregels** kunt u de voortgang van de inkomende ontvangst controleren door de waarden in de kolom **Hoeveelheid resterend voor ontvangst** te controleren. Volg een van deze stappen om details weer te geven met betrekking tot het werk dat via de mobiele app Magazijnbeheer wordt uitgevoerd.

- Ga naar **Magazijnbeheer \> Query's en rapporten \> Magazijnorderregels** en gebruik het filter om te zoeken naar regels.
- Ga naar **Inkoopbeheer \> Inkooporders \> Alle inkooporders** en open de relevante inkooporder. Selecteer in de sectie **Inkooporderregels** een of meer regels en selecteer op de werkbalk **Magazijn \> Magazijnontvangstbonnen**.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
