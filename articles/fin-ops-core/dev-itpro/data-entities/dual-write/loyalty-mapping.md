---
title: Loyaliteitskaarten en beloningspunten van klanten
description: Dit onderwerp beschrijft de integratie van gegevens over loyaliteitskaarten en beloningspunten van klanten tussen Finance and Operations-apps en Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 24ce08bb6cba9c74075151bafe0b07509fbdf73d
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "3998009"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>Loyaliteitskaarten en beloningspunten van klanten

[!include [banner](../../includes/banner.md)]



Bedrijven classificeren klanten en bieden geavanceerde services op basis van de koop- en uitgavenpatronen van klanten. In de Microsoft Dynamics 365-suite van toepassingen biedt Dynamics 365 Commerce de infrastructuur en functies om loyaliteitskaarten, beloningspunten, loyaliteitsprijzen en winkelervaringen op basis van beloningen mogelijk te maken en te verwerken. Wanneer gegevens over klantloyaliteitskaarten en -beloningspunten in Commerce worden gesynchroniseerd met Common Data Service, kunnen deze gegevens worden gebruikt in modelgestuurde apps in Dynamics 365. Zo kunnen gebruikers van Dynamics 365 Customer Service de gegevens gebruiken om dezelfde geavanceerde services aan te bieden via de helpdesk.

## <a name="templates"></a>Sjablonen

| Finance and Operations-apps | Modelgestuurde apps in Dynamics 365 | Omschrijving |
|-----------------------------|-----------------------------------|-------------|
| Loyaliteitskaart                | msdyn\_loyaltycards               | Met deze sjabloon wordt informatie over klantloyaliteitskaarten gesynchroniseerd. |
| Beloningspunten voor loyaliteit       | msdyn\_loyaltyrewardpoints        | Met deze sjabloon wordt informatie over klantbeloningspunten gesynchroniseerd. |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
