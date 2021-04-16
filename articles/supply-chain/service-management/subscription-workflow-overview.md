---
title: Overzicht van abonnementsworkflow
description: Dit onderwerp bevat een overzicht van de abonnementswerkstroom.
author: ShylaThompson
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dbc87dc9c6327550020270468346800a7b80f4c3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817384"
---
# <a name="subscription-workflow-overview"></a>Overzicht van abonnementsworkflow 

[!include [banner](../includes/banner.md)]


U bent de abonnementenbeheerder voor een verlichtingsbedrijf dat abonnementen aanbiedt voor het onderhoud van verlichtingsinstallaties. Een klant wil een jaarlijks abonnement voor het onderhoud van de verlichtingsinstallatie aanschaffen bij uw bedrijf.

## <a name="setting-up-subscriptions"></a>Abonnementen instellen

Als u een abonnement wilt instellen, moet u eerst een abonnementsgroep maken voor de nieuwe serviceovereenkomst of controleren of er een abonnementsgroep bestaat. Als er al een abonnementsgroep bestaat, moet u deze zo instellen dat de klant jaarlijks wordt gefactureerd en dat de verkoopopbrengst elke maand van het jaar wordt toegerekend. Zie [Abonnementsgroepen instellen](set-up-subscription-groups.md) voor meer informatie over het instellen van abonnementen.

Wanneer u de abonnementsgroep hebt gemaakt, kunt u het abonnement maken. Zie voor meer informatie over het maken van serviceabonnementen [Serviceabonnementen maken op basis van een abonnementsgroep](create-service-subscriptions-from-subscription-group.md).

## <a name="create-and-modify-subscription-transactions"></a>Abonnementstransacties maken en wijzigen

Nadat u het abonnement hebt ingesteld, maakt u de abonnementskostentransactie voor de eerste factuurperiode van één jaar. De transacties hebben het type **Normaal**. Daarom kunt u alleen abonnementstransacties maken waarvan de begindatum en de einddatum overeenstemmen met de perioden die eerder zijn gemaakt in het formulier **Periodetypen**. Zie voor meer informatie over tarieftransacties [Tarieftransacties abonnement maken](create-subscription-fee-transactions.md).

Nadat u het abonnement hebt ingesteld voor deze klant, herinnert u zich dat er een korting van 10% is overeengekomen voor alle lijstprijzen van serviceaanbiedingen. Daarom moet u de prijs verlagen van de bijzondere transactiekosten die u hebt gemaakt.

Later op de dag neemt uw contactpersoon bij de klant met u contact op om door te geven dat ze nog wel gebruik willen maken van de serviceovereenkomst voor de verlichtingsinstallatie, maar dat ze later in het jaar een nieuwe verlichtingsinstallatie willen plaatsen. Ze hebben daarom de onderhoudsovereenkomst slechts nodig tot oktober 2013. U maakt nu een nieuwe transactie voor abonnementskosten met het type **Reductiedagen** om het aantal maanden van het abonnement van de klant te beperken. Zie voor meer informatie over het beperken van dagen [De dagen van abonnementskosten verminderen](reduce-the-days-on-subscription-fees.md).

## <a name="invoice-and-accrue-subscription-transactions"></a>Abonnementstransacties factureren en toerekenen

U bent nu klaar met het instellen van het abonnement en u kunt de klant factureren voor het abonnement. Zie [Abonnementstransacties factureren](invoice-subscription-transactions.md) voor meer informatie over het factureren van abonnementen.

Twee dagen later belt uw klant om te zeggen dat het abonnement moet worden gefactureerd in Amerikaanse dollars in plaats van in euro's. U maakt daarvoor een creditnota en u maakt ook een nieuwe abonnementstransactie in de juiste valuta. Zie voor meer informatie over het crediteren van abonnementstransacties [Abonnementstransacties crediteren](credit-subscription-transactions.md).

Aan het eind van elke maand rekent u de opbrengst van één maand van de abonnementen van de klant toe aan de winst- en verliesrekening en OHW-rekeningen. Zie voor meer informatie over het toerekenen van opbrengst voor abonnementen [Abonnementsopbrengsten samenvoegen](accrue-subscription-revenue.md).

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]