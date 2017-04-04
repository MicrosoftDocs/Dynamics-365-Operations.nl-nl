---
title: Winkelvoorraad beheren
description: Dit artikel worden de typen documenten die u gebruiken kunt voor het beheren van voorraad.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fbe9945799f1e65ed6ad624a3df270fa4eb72b88
ms.lasthandoff: 03/31/2017


---

# <a name="manage-store-inventory"></a>Winkelvoorraad beheren

Dit artikel worden de typen documenten die u gebruiken kunt voor het beheren van voorraad.

Met de volgende typen documenten kunt u de voorraad van uw organisatie beheren.

## <a name="purchase-orders"></a>Inkooporders
Inkooporders worden gemaakt op het hoofdkantoor. Als een detailhandelmagazijn is opgenomen in de inkooporderkoptekst, kan de order in de winkel worden ontvangen met behulp van moderne POS (MPOS) of Cloud-POS in Microsoft Dynamics 365 voor bewerkingen: Retail. Nadat de hoeveelheden die in de winkel zijn ontvangen, worden ingevoerd, kunnen zij lokaal worden opgeslagen voor verdere wijzigingen. Ook kan de hoeveelheden kunnen worden vastgelegd en verzonden naar het hoofdkantoor. Op het hoofdkantoor de hoeveelheden die zijn ontvangen in de winkel worden weergegeven in Dynamics 365 voor bewerkingen in de **nu ontvangen** op de inkooporder.
Transferorders
---------------

Een transferorder kan opgeven dat een bepaalde winkel een locatie is waaruit artikelen kunnen worden verzonden. In dit geval wordt weergegeven de transferorder in de winkel als een aanvraag voor picken in MPOS of Cloud-POS. Nadat het picken van de aangevraagde hoeveelheden, worden ze toegezegd en verzonden naar het hoofdkantoor. Op het hoofdkantoor de hoeveelheden die zijn opgenomen in de winkel worden weergegeven in Dynamics 365 voor bewerkingen in de **nu verzenden** op de transferorder. Een transferorder kan opgeven dat een bepaalde winkel een locatie is waarnaar artikelen kunnen worden verzonden. In dit geval wordt weergegeven de transferorder in de winkel als een aanvraag voor ontvangen in MPOS of Cloud-POS. Nadat de hoeveelheden die in de winkel zijn ontvangen, worden ingevoerd, kunnen zij lokaal worden opgeslagen voor verdere wijzigingen. Ook kan de hoeveelheden kunnen worden vastgelegd en verzonden naar het hoofdkantoor. Op het hoofdkantoor de hoeveelheden die zijn ontvangen in de winkel worden weergegeven in Dynamics 365 voor bewerkingen in de **nu ontvangen** op de transferorder.

## <a name="stock-counts"></a>Voorraadtellingen
Voorraadtellingen kunnen gepland of ongepland worden uitgevoerd. Geplande voorraadtellingen worden in gang gezet op het hoofdkantoor, dat bepaalt welke artikelen moeten worden geteld. Het hoofdkantoor maakt een voorraadtellingsdocument dat kan worden ontvangen in de winkel waar de hoeveelheden van de werkelijke voorhanden voorraad in MPOS of Cloud-POS worden ingevoerd. Niet-geplande voorraadtellingen worden gestart in de winkel en de hoeveelheden van de werkelijke voorhanden voorraad in MPOS of Cloud-POS worden bijgewerkt. In tegenstelling tot de geplande voorraadtellingen werken ongeplande voorraadtellingen niet met een vooraf gedefinieerde lijst met artikelen. Wanneer een voorraadtelling van beide typen is voltooid, wordt deze toegezegd en verzonden naar het hoofdkantoor. De telling wordt op het hoofdkantoor gevalideerd en geboekt.




