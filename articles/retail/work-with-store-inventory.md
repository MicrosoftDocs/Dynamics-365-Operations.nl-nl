---
title: Voorraadbeheer winkel
description: In dit artikel worden de typen documenten beschreven waarmee u de voorraad van uw organisatie kunt beheren.
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 72f6f5e2645240ee3ddd31657176f27cb7db404f
ms.contentlocale: nl-nl
ms.lasthandoff: 08/08/2018

---

# <a name="store-inventory-management"></a>Voorraadbeheer winkel

[!include [banner](includes/banner.md)]

In dit artikel worden de typen documenten beschreven waarmee u de voorraad van uw organisatie kunt beheren.

Met de volgende typen documenten kunt u de voorraad van uw organisatie beheren.

## <a name="purchase-orders"></a>Inkooporders
Inkooporders worden gemaakt op het hoofdkantoor. Als een detailhandelsmagazijn in de koptekst van de inkooporder wordt opgenomen, kan de order worden ontvangen in de winkel door middel van Modern POS (MPOS) of Cloud POS in Microsoft Dynamics 365 for Retail. Nadat de hoeveelheden die in de winkel zijn ontvangen, worden ingevoerd, kunnen zij lokaal worden opgeslagen voor verdere wijzigingen. Ook kan de hoeveelheden kunnen worden vastgelegd en verzonden naar het hoofdkantoor. Op het hoofdkantoor worden de hoeveelheden die zijn ontvangen in de winkel weergegeven in Dynamics 365 for Retail in het veld **Nu ontvangen** op de inkooporder.

## <a name="transfer-orders"></a>Transferorders
Een transferorder kan opgeven dat een bepaalde winkel een locatie is waaruit artikelen kunnen worden verzonden. In dit geval wordt de transferorder weergegeven in de winkel als een aanvraag voor picken in MPOS of Cloud POS. Nadat het picken van de aangevraagde hoeveelheden, worden ze toegezegd en verzonden naar het hoofdkantoor. Op het hoofdkantoor worden de hoeveelheden die in de winkel zijn verzameld, weergegeven in Dynamics 365 for Retail in het veld **Nu verzenden** op de transferorder. Een transferorder kan opgeven dat een bepaalde winkel een locatie is waarnaar artikelen kunnen worden verzonden. In dit geval wordt de transferorder weergegeven in de winkel als een aanvraag voor ontvangen in MPOS of Cloud POS. Nadat de hoeveelheden die in de winkel zijn ontvangen, worden ingevoerd, kunnen zij lokaal worden opgeslagen voor verdere wijzigingen. Ook kan de hoeveelheden kunnen worden vastgelegd en verzonden naar het hoofdkantoor. Op het hoofdkantoor worden de hoeveelheden die zijn ontvangen in de winkel weergegeven in Dynamics 365 for Retail in het veld **Nu ontvangen** op de transferorder.

## <a name="stock-counts"></a>Voorraadtellingen
Voorraadtellingen kunnen gepland of ongepland worden uitgevoerd. Geplande voorraadtellingen worden in gang gezet op het hoofdkantoor, dat bepaalt welke artikelen moeten worden geteld. Het hoofdkantoor maakt een voorraadtellingsdocument dat in de winkel kan worden ontvangen waarop de hoeveelheden die daadwerkelijk in voorraad zijn, worden ingevoerd in MPOS of Cloud POS. Ongeplande voorraadtellingen worden gestart in de winkel en de hoeveelheden van de werkelijke voorhanden voorraad worden bijgewerkt in MPOS of Cloud POS. In tegenstelling tot de geplande voorraadtellingen werken ongeplande voorraadtellingen niet met een vooraf gedefinieerde lijst met artikelen. Wanneer een voorraadtelling van beide typen is voltooid, wordt deze toegezegd en verzonden naar het hoofdkantoor. De telling wordt op het hoofdkantoor gevalideerd en geboekt.

## <a name="inventory-lookup"></a>Zoeken in voorraad
De huidige voorhanden producthoeveelheid voor meerdere winkels en magazijnen kan worden weergegeven op de pagina Zoeken in voorraad. Naast de huidige voorhanden hoeveelheid kunnen de toekomstige ATP-hoeveelheden (Available To Promise) worden weergegeven voor elke afzonderlijke winkel. Als u dit wilt doen, selecteert u de winkel waarvoor u de ATP wilt weergeven en klikt u vervolgens op **Beschikbaarheid van winkel weergeven**.





