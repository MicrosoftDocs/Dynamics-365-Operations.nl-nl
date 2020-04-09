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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: e7e67946930404ab7ba0c7fccf468722f723d675
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172964"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="71a66-103">Loyaliteitskaarten en beloningspunten van klanten</span><span class="sxs-lookup"><span data-stu-id="71a66-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="71a66-104">Bedrijven classificeren klanten en bieden geavanceerde services op basis van de koop- en uitgavenpatronen van klanten.</span><span class="sxs-lookup"><span data-stu-id="71a66-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="71a66-105">In de Microsoft Dynamics 365-suite van toepassingen biedt Dynamics 365 Commerce de infrastructuur en functies om loyaliteitskaarten, beloningspunten, loyaliteitsprijzen en winkelervaringen op basis van beloningen mogelijk te maken en te verwerken.</span><span class="sxs-lookup"><span data-stu-id="71a66-105">In the Microsoft Dynamics 365 suite of applications, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="71a66-106">Wanneer gegevens over klantloyaliteitskaarten en -beloningspunten in Commerce worden gesynchroniseerd met Common Data Service, kunnen deze gegevens worden gebruikt in modelgestuurde apps in Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="71a66-106">When data about customer loyalty cards and reward points in Commerce is synced to Common Data service, model-driven apps in Dynamics 365 can use that data.</span></span> <span data-ttu-id="71a66-107">Zo kunnen gebruikers van Dynamics 365 Customer Service de gegevens gebruiken om dezelfde geavanceerde services aan te bieden via de helpdesk.</span><span class="sxs-lookup"><span data-stu-id="71a66-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="71a66-108">Sjablonen</span><span class="sxs-lookup"><span data-stu-id="71a66-108">Templates</span></span>

| <span data-ttu-id="71a66-109">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="71a66-109">Finance and Operations apps</span></span> | <span data-ttu-id="71a66-110">Modelgestuurde apps in Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="71a66-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="71a66-111">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="71a66-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="71a66-112">Loyaliteitskaart</span><span class="sxs-lookup"><span data-stu-id="71a66-112">Loyalty card</span></span>                | <span data-ttu-id="71a66-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="71a66-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="71a66-114">Met deze sjabloon wordt informatie over klantloyaliteitskaarten gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="71a66-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="71a66-115">Beloningspunten voor loyaliteit</span><span class="sxs-lookup"><span data-stu-id="71a66-115">Loyalty reward points</span></span>       | <span data-ttu-id="71a66-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="71a66-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="71a66-117">Met deze sjabloon wordt informatie over klantbeloningspunten gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="71a66-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
