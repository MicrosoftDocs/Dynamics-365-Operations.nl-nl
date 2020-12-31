---
title: Loyaliteitskaarten en beloningspunten van klanten
description: Dit onderwerp beschrijft de integratie van gegevens over loyaliteitskaarten en beloningspunten van klanten in twee keer wegschrijven.
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
ms.openlocfilehash: 28872e9510394cf3d5cee151798d4130b8b6fe27
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683493"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>Loyaliteitskaarten en beloningspunten voor klanten

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bedrijven classificeren klanten en bieden geavanceerde services op basis van de koop- en uitgavenpatronen van klanten. Zo biedt Dynamics 365 Commerce bijvoorbeeld de infrastructuur en functies om loyaliteitskaarten, beloningspunten, loyaliteitsprijzen en winkelervaringen op basis van beloningen mogelijk te maken en te verwerken. Wanneer gegevens over klantloyaliteitskaarten en -beloningspunten in Commerce worden gesynchroniseerd met Dataverse, kunnen deze gegevens worden gebruikt in Customer Engagement-apps. Zo kunnen gebruikers van Dynamics 365 Customer Service de gegevens gebruiken om dezelfde geavanceerde services aan te bieden via de helpdesk.

## <a name="templates"></a>Sjablonen

| Finance and Operations-apps | Modelgestuurde apps in Dynamics 365 | Omschrijving |
|-----------------------------|-----------------------------------|-------------|
| Loyaliteitskaart                | msdyn\_loyaltycards               | Met deze sjabloon wordt informatie over klantloyaliteitskaarten gesynchroniseerd. |
| Beloningspunten voor loyaliteit       | msdyn\_loyaltyrewardpoints        | Met deze sjabloon wordt informatie over klantbeloningspunten gesynchroniseerd. |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
