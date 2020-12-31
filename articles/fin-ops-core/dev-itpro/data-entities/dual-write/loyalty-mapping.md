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
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="03bec-103">Loyaliteitskaarten en beloningspunten voor klanten</span><span class="sxs-lookup"><span data-stu-id="03bec-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="03bec-104">Bedrijven classificeren klanten en bieden geavanceerde services op basis van de koop- en uitgavenpatronen van klanten.</span><span class="sxs-lookup"><span data-stu-id="03bec-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="03bec-105">Zo biedt Dynamics 365 Commerce bijvoorbeeld de infrastructuur en functies om loyaliteitskaarten, beloningspunten, loyaliteitsprijzen en winkelervaringen op basis van beloningen mogelijk te maken en te verwerken.</span><span class="sxs-lookup"><span data-stu-id="03bec-105">For example, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="03bec-106">Wanneer gegevens over klantloyaliteitskaarten en -beloningspunten in Commerce worden gesynchroniseerd met Dataverse, kunnen deze gegevens worden gebruikt in Customer Engagement-apps.</span><span class="sxs-lookup"><span data-stu-id="03bec-106">When data about customer loyalty cards and reward points in Commerce is synced to Dataverse, customer engagement apps can use that data.</span></span> <span data-ttu-id="03bec-107">Zo kunnen gebruikers van Dynamics 365 Customer Service de gegevens gebruiken om dezelfde geavanceerde services aan te bieden via de helpdesk.</span><span class="sxs-lookup"><span data-stu-id="03bec-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="03bec-108">Sjablonen</span><span class="sxs-lookup"><span data-stu-id="03bec-108">Templates</span></span>

| <span data-ttu-id="03bec-109">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="03bec-109">Finance and Operations apps</span></span> | <span data-ttu-id="03bec-110">Modelgestuurde apps in Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="03bec-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="03bec-111">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="03bec-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="03bec-112">Loyaliteitskaart</span><span class="sxs-lookup"><span data-stu-id="03bec-112">Loyalty card</span></span>                | <span data-ttu-id="03bec-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="03bec-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="03bec-114">Met deze sjabloon wordt informatie over klantloyaliteitskaarten gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="03bec-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="03bec-115">Beloningspunten voor loyaliteit</span><span class="sxs-lookup"><span data-stu-id="03bec-115">Loyalty reward points</span></span>       | <span data-ttu-id="03bec-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="03bec-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="03bec-117">Met deze sjabloon wordt informatie over klantbeloningspunten gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="03bec-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
