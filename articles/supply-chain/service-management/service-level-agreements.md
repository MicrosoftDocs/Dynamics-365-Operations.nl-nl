---
title: Overzicht van Servicelevelovereenkomsten
description: In een serviceovereenkomst stemt de klant in met een minimale responstijd gebaseerd op het moment waarop het servicebedrijf een probleem registreert en het moment waarop het probleem is opgelost.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f2cfa8b72e515b6237914499af626ff8262429d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974355"
---
# <a name="service-level-agreements-overview"></a>Overzicht van Servicelevelovereenkomsten       

[!include [banner](../includes/banner.md)]


Een serviceniveauovereenkomst (SLA) is een overeenkomst tussen een servicebedrijf en een serviceklant. In een SLA stemt de klant in met een minimale responstijd gebaseerd op het moment waarop het servicebedrijf een probleem registreert en het moment waarop het probleem is opgelost.

Via een SLA wordt een standaardserviceniveau bepaald dat klanten ontvangen en kan een servicebedrijf ook inschatten wanneer een servicetaak moet zijn voltooid.

U kunt het gewenste aantal serviceovereenkomsten maken voor de verschillende serviceniveaus voor serviceklanten.

## <a name="create-a-service-level-agreement"></a>Een serviceovereenkomst maken

1.  Klik op **Servicebeheer** \> **Instellen** \> **Serviceovereenkomsten** \> **Serviceovereenkomsten**.

2.  Selecteer in het veld **Serviceovereenkomst** een naam voor de serviceovereenkomst.

3.  Typ de tijd in die u wilt toestaan voor de voltooiing van serviceoproepen die zijn gekoppeld aan de serviceniveauovereenkomst. Selecteer vervolgens een agenda als u de serviceniveauovereenkomst op een specifieke kalender wilt baseren.

## <a name="apply-a-service-level-agreement"></a>Een serviceovereenkomst toepassen

De serviceovereenkomst wordt rechtstreeks toegepast.

Serviceorders die u handmatig maakt en aan een serviceovereenkomst met een SLA koppelt, worden gemeten op basis van deze SLA.

Serviceorders die automatisch worden gemaakt, worden niet aan een serviceovereenkomst gekoppeld.

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a>Het serviceniveau toepassen op de serviceovereenkomst

1.  Klik op **Servicebeheer** \> **Algemeen** \> **Serviceovereenkomsten** \> **Serviceovereenkomsten**. Selecteer de serviceovereenkomst waarop u de SLA wilt toepassen en klik vervolgens op **Bewerken** in het **Actievenster**.

2.  Selecteer in het veld **Serviceovereenkomst** de serviceovereenkomst die u wilt toewijzen.

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a>De serviceovereenkomst toepassen op de serviceovereenkomstgroep

1.  Klik op **Servicebeheer** \> **Instellen** \> **Serviceovereenkomsten** \> **Serviceovereenkomstgroepen**.

2.  Selecteer in het veld **Serviceovereenkomst** de serviceovereenkomst die u wilt toewijzen.

## <a name="track-time-on-a-service-order-against-an-sla"></a>De tijd bijhouden voor een serviceorder op basis van een serviceovereenkomst

Wanneer u een nieuwe serviceorder maakt voor een serviceovereenkomst waaraan een SLA is toegewezen, wordt het tijdsinterval voor de levering van de service gestart en begint het systeem met het bijhouden van de levertijd. Daarnaast kunt u de volgende opties instellen:

  - U kunt de tijdregistratie voor de serviceorder starten en stoppen om de totale tijd die aan serviceorders is besteed te registreren.

  - U kunt controleren of het tijdsinterval overeenkomt met de instelling in de serviceniveauovereenkomst.

  - U kunt redencodes definiëren die moeten worden ingesteld als het tijdsinterval van de serviceniveauovereenkomst wordt overschreden.

## <a name="see-also"></a>Zie ook

[Compatibiliteit met serviceovereenkomsten weergeven](view-compliance-with-service-level-agreements.md)

  


