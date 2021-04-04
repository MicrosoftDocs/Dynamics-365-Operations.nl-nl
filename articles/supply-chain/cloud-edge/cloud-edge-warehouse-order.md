---
title: Magazijnorders voor cloud- en randschaaleenheden
description: Dit onderwerp biedt informatie over de mogelijkheid voor magazijnorders die wordt gebruikt als onderdeel van de werkbelasting van de magazijnschaaleenheid.
author: perlynne
manager: tfeyr
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 9102f53ab1b63d08b8bba7b0ae505416ec5a83fd
ms.sourcegitcommit: 70b1567d316f19c15a4b032b4897f15c8dcdca09
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/08/2021
ms.locfileid: "5556357"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a>Magazijnorders voor cloud- en randschaaleenheden

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> Niet alle bedrijfsfuncties worden volledig ondersteund in de openbare preview wanneer werkbelastingen voor schaaleenheden worden gebruikt. Als u schaaleenheden gebruikt, zorg ervoor dat u alleen de processen gebruikt die in dit onderwerp expliciet worden ondersteund.

## <a name="what-are-warehouse-orders"></a>Wat zijn magazijnorders?

*Magazijnorders* zijn een type order dat is gemaakt ter ondersteuning van magazijnimplementaties voor hub en schaaleenheden. Hiermee kunt u voorraad ontvangen wanneer u een magazijnwerkbelasting voor een schaaleenheid uitvoert. Deze worden momenteel alleen bij inkooporders gebruikt.

Magazijnorders worden gebruikt als onderdeel van magazijnbeheerverwerking, bijvoorbeeld wanneer de magazijn-app wordt gebruikt om de fysieke beschikbare voorraad te registreren tijdens de verwerking van een binnenkomende inkooporder. Magazijnorders worden gemaakt als onderdeel van het proces *Vrijgeven aan magazijn* dat beschikbaar is voor inkooporders met een schaaleenheidmagazijn en artikelen die zijn ingeschakeld om magazijnbeheerprocessen te gebruiken.

> [!IMPORTANT]
> Magazijnorders zijn alleen beschikbaar in implementaties waarin gebruik wordt gemaakt van de [werkbelastingen van magazijnbeheer voor cloud- en randschaaleenheden](cloud-edge-workload-warehousing.md).

## <a name="create-a-warehouse-order"></a>Magazijnorder maken

Volg de onderstaande stappen om een magazijnorder te maken.

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

In de weergave **Magazijnorderregels** kunt u de voortgang van de inkomende ontvangst controleren door de waarden in de kolom **Hoeveelheid resterend voor ontvangst** te controleren. Volg een van deze stappen om details weer te geven met betrekking tot het werk dat via de magazijn-app wordt uitgevoerd.

- Ga naar **Magazijnbeheer \> Query's en rapporten \> Magazijnorderregels** en gebruik het filter om te zoeken naar regels.
- Ga naar **Inkoopbeheer \> Inkooporders \> Alle inkooporders** en open de relevante inkooporder. Selecteer in de sectie **Inkooporderregels** een of meer regels en selecteer op de werkbalk **Magazijn \> Magazijnontvangstbonnen**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]