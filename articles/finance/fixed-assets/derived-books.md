---
title: Afgeleide boeken
description: In dit artikel vindt u een overzicht van de functionaliteit van het afgeleide boek.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: kfend
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 81abb1b16069adb3cdcc73bdf6b963463cc88938
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/05/2022
ms.locfileid: "8714084"
---
# <a name="derived-books"></a>Afgeleide boeken

[!include [banner](../includes/banner.md)]

In dit artikel vindt u een overzicht van de functionaliteit van het afgeleide boek.

Het doel van afgeleide boeken is de vereenvoudiging van het boeken van transacties in het vaste-activaboek die op gezette tijden zijn gepland.  U kiest één boek als het primaire boek. Dit is gewoonlijk het boek dat wordt gebruikt voor boekhoudkundige afschrijving. Vervolgens koppelt u dit aan andere boeken die zijn ingesteld om transacties te boeken in dezelfde intervallen als het primaire boek. Belastingafschrijvingsboeken zijn vaak ingesteld als afgeleide boeken. 

De meest algemene transacties die u kunt instellen op het boeken naar afgeleide boeken zijn verwervingen, bijboekingscorrrecties en afboekingen. 

## <a name="example"></a>Voorbeeld

Boek B en boek C zijn ingesteld als afgeleide boeken voor boek A voor het transactietype verwerving. In boek A voert u een verwervingstransactie in voor activum 123 voor 1.500,00. 

Als de transactie geboekt is, wordt een verwervingstransactie gegenereerd en geboekt in activum 123 voor boek B en in activum 123 voor boek C voor 1.500,00. Wanneer u de transacties van het primaire boek voorbereidt voor het boeken in het vaste-activajournaal, kunt u ook de transacties van de afgeleide boeken weergeven en wijzigen. Als u de transacties van het primaire boek voorbereidt voor het boeken in een ander journaal, worden de transacties van de afgeleide waarde niet weergegeven. Deze worden echter geboekt naar de juiste rekeningen en boekingslagen wanneer u de transacties van het primaire boek boekt.

> [!NOTE]                                                                                                                               
> Boeken die zijn ingesteld op het boeken van transacties op andere tijden dan de tijden van het primaire boek moeten als afzonderlijke boeken aan de vaste activa worden gekoppeld en niet als afgeleide boeken.  

Zie voor meer informatie [Boeken met afgeleide boeken](post-derived-value-models.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
