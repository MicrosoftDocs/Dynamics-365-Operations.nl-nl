---
title: Winkelvoorraad beheren
description: In dit artikel worden de typen documenten beschreven waarmee u de voorraad van uw organisatie kunt beheren.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: 37f9cb7d8118c3aa4cf287a8b7ed2dc9270acb52
ms.contentlocale: nl-nl
ms.lasthandoff: 04/26/2017


---

# <a name="manage-store-inventory"></a>Winkelvoorraad beheren

[!include[banner](includes/banner.md)]


In dit artikel worden de typen documenten beschreven waarmee u de voorraad van uw organisatie kunt beheren.

Met de volgende typen documenten kunt u de voorraad van uw organisatie beheren.

## <a name="purchase-orders"></a>Inkooporders
Inkooporders worden gemaakt op het hoofdkantoor. Als een detailhandelsmagazijn in de koptekst van de inkooporder is opgenomen, kan de order worden ontvangen in de winkel door middel van Modern POS (MPOS) of Cloud POS in Microsoft Dynamics 365 for Operations - Retail. Nadat de hoeveelheden die in de winkel zijn ontvangen, worden ingevoerd, kunnen zij lokaal worden opgeslagen voor verdere wijzigingen. Ook kan de hoeveelheden kunnen worden vastgelegd en verzonden naar het hoofdkantoor. Op het hoofdkantoor worden de hoeveelheden die zijn ontvangen in de winkel weergegeven in Microsoft Dynamics 365 for Operations in het veld **Nu ontvangen** op de inkooporder.

## <a name="transfer-orders"></a>Transferorders
Een transferorder kan opgeven dat een bepaalde winkel een locatie is waaruit artikelen kunnen worden verzonden. In dit geval wordt de transferorder weergegeven in de winkel als een aanvraag voor picken in MPOS of Cloud POS. Nadat het picken van de aangevraagde hoeveelheden, worden ze toegezegd en verzonden naar het hoofdkantoor. Op het hoofdkantoor worden de hoeveelheden die in de winkel zijn verzameld, weergegeven in Microsoft Dynamics 365 for Operations in het veld **Nu verzenden** op de transferorder. Een transferorder kan opgeven dat een bepaalde winkel een locatie is waarnaar artikelen kunnen worden verzonden. In dit geval wordt de transferorder weergegeven in de winkel als een aanvraag voor ontvangen in MPOS of Cloud POS. Nadat de hoeveelheden die in de winkel zijn ontvangen, worden ingevoerd, kunnen zij lokaal worden opgeslagen voor verdere wijzigingen. Ook kan de hoeveelheden kunnen worden vastgelegd en verzonden naar het hoofdkantoor. Op het hoofdkantoor worden de hoeveelheden die zijn ontvangen in de winkel weergegeven in Microsoft Dynamics 365 for Operations in het veld **Nu ontvangen** op de transferorder.

## <a name="stock-counts"></a>Voorraadtellingen
Voorraadtellingen kunnen gepland of ongepland worden uitgevoerd. Geplande voorraadtellingen worden in gang gezet op het hoofdkantoor, dat bepaalt welke artikelen moeten worden geteld. Het hoofdkantoor maakt een voorraadtellingsdocument dat in de winkel kan worden ontvangen waarop de hoeveelheden die daadwerkelijk in voorraad zijn, worden ingevoerd in MPOS of Cloud POS. Ongeplande voorraadtellingen worden gestart in de winkel en de hoeveelheden van de werkelijke voorhanden voorraad worden bijgewerkt in MPOS of Cloud POS. In tegenstelling tot de geplande voorraadtellingen werken ongeplande voorraadtellingen niet met een vooraf gedefinieerde lijst met artikelen. Wanneer een voorraadtelling van beide typen is voltooid, wordt deze toegezegd en verzonden naar het hoofdkantoor. De telling wordt op het hoofdkantoor gevalideerd en geboekt.






