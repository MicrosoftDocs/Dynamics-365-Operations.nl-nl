---
title: Klantrecords worden niet weergegeven in Commerce Headquarters
description: Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen wanneer klantrecords niet direct in Commerce Headquarters worden weergegeven.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 790468ac244f1647c07024604886c65d22feca24
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585266"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a>Klantrecords worden niet weergegeven in Commerce Headquarters

[!include [banner](../../includes/banner.md)]

Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen wanneer klantrecords niet direct in Commerce Headquarters worden weergegeven.

## <a name="description"></a>Beschrijving

Wanneer u een nieuwe klantrecord maakt met de aanmeldingsstroom in de e-commerce-winkel, wordt de bijbehorende klantrecord niet direct weergegeven in Commerce Headquarters.

## <a name="resolution"></a>Oplossing

### <a name="disable-customer-creation-in-async-mode"></a>Maken van klant in asynchrone modus uitschakelen

> [!IMPORTANT]
> Als u het asynchroon maken van klanten uitschakelt, kan dit gevolgen hebben voor de systeemprestaties, omdat er door het maken van elke record een realtime aanvraag voor Commerce Headquarters wordt gemaakt. Bovendien resulteren eventuele nieuwe stromen voor het maken van klanten in fouten als Commerce Headquarters inactief is (bijvoorbeeld tijdens het onderhoud).

Voer deze stappen uit om het maken van klanten in de asynchrone modus in Commerce Headquarters uit te schakelen.

1. Ga naar **Retail en Commerce \> Afzetkanaalinstellingen \> Onlinewinkel instellen \> Functionaliteitsprofielen**.
1. Maak een functionaliteitsprofiel voor uw online afzetkanaal als u nog geen functionaliteitsprofiel gebruikt.
1. Zorg ervoor dat de optie **Klant maken in asynchrone modus** is ingesteld op **Nee**.
1. Ga naar **Retail en Commerce \> Afzetkanalen \> Online winkels**.
1. Selecteer de online winkel om het maken van klanten in de asynchrone modus uit te schakelen.
1. Ga naar het tabblad **Algemeen** en zorg ervoor dat het veld **Functionaliteitsprofiel** is ingesteld op het functionaliteitsprofiel dat u voor uw online kanaal gebruikt.

## <a name="additional-resources"></a>Aanvullende bronnen

[Een B2C-tenant instellen in Commerce](../set-up-b2c-tenant.md)