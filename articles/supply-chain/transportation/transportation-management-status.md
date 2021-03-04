---
title: Statussen voor Transportbeheer
description: In dit onderwerp wordt uitgelegd hoe u een transportstatus maakt en die status toewijst aan een de status van een vervoerder.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 3f7d471771ec2b4703d878fbf395cd90902b6669
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/29/2020
ms.locfileid: "4425906"
---
# <a name="transportation-management-statuses"></a>Statussen voor Transportbeheer

[!include [banner](../includes/banner.md)]

Stel modelcodes voor transportstatussen in om codes te interpreteren die door uw vervoerders worden verstrekt. Hiermee kunt u integreren met vervoerders om een status te geven. De transportstatus die u voor een transportstatusmodelcode opgeeft, kan u helpen de status van een lading, zending of container te volgen. De specifieke transportstatus voor een lading, zending of container kan alleen worden bijgewerkt via gegevensintegratie en niet handmatig via de gebruikersinterface.

## <a name="create-a-transportation-status"></a>Een transportstatus maken

Volg deze stappen om een transportstatus te maken:

1. Ga naar **Transportbeheer \> Instellingen \> Transportstatusmodellen**.
1. Selecteer **Nieuw** om een nieuw transportstatusmodel te maken.
1. Voer in het veld **Transportstatusmodel** een unieke code voor de transportstatus in.
1. Selecteer in het veld **Transporttype** als type transport *Vervoerder* of *Hub*.
1. Voer een naam en een transportstatus in.
1. Sluit de pagina.

## <a name="map-a-transportation-status-to-a-carrier-status"></a>Een transportstatus toewijzen aan de status van een vervoerder

Ga als volgt te werk om een transportstatus toe te wijzen aan de status van een vervoerder:

1. Ga naar **Transportbeheer \> Instellingen \> Vervoerders \> Transportstatus vervoerder**.
1. Selecteer **Nieuw** om een code van een vervoerder te koppelen aan een transportstatusmodelcode.
1. Selecteer de unieke id voor de vervoerder en de vervoerdersservice.
1. Selecteer de transportstatuscode die u wilt koppelen aan de code van de geselecteerde vervoerder.
1. Voer de externe code in die door de vervoerder wordt gebruikt.
1. Sluit de pagina.