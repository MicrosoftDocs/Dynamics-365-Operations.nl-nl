---
title: " Correcties van beloningspunten voor loyaliteit verwerken"
description: Deze procedure toont hoe u de loyaliteitskaartgegevens opzoekt en de beloningspunten voor loyaliteit aanpast.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailLoyaltyCards, RetailLoyaltyCardRewardPointTrans, RetailLoyaltyCardRewardPointAdjustment, RetailAffiliationLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bdbd9fa60fe4d000359e4695a9fb034fae3ca1b0
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140719"
---
# <a name="process-loyalty-reward-point-adjustments"></a><span data-ttu-id="61d25-103"> Correcties van beloningspunten voor loyaliteit verwerken</span><span class="sxs-lookup"><span data-stu-id="61d25-103">Process loyalty reward point adjustments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="61d25-104">Deze procedure toont hoe u de loyaliteitskaartgegevens opzoekt en de beloningspunten voor loyaliteit aanpast.</span><span class="sxs-lookup"><span data-stu-id="61d25-104">This procedure demonstrates how to look up loyalty card information and adjust loyalty reward points.</span></span> <span data-ttu-id="61d25-105">Het demobedrijf dat wordt gebruikt om deze taak te maken is USRT.</span><span class="sxs-lookup"><span data-stu-id="61d25-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="61d25-106">Deze taak is bedoeld voor de rol Bedrijfsbeheerder Commerce of Klantenservicemanager.</span><span class="sxs-lookup"><span data-stu-id="61d25-106">This task is intended for the Commerce operations manager role or a Customer service manager role.</span></span>

1. <span data-ttu-id="61d25-107">Ga naar Loyaliteitskaarten.</span><span class="sxs-lookup"><span data-stu-id="61d25-107">Go to Loyalty cards.</span></span>
2. <span data-ttu-id="61d25-108">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="61d25-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="61d25-109">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="61d25-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="61d25-110">Klik op Kaarttransacties.</span><span class="sxs-lookup"><span data-stu-id="61d25-110">Click Card transactions.</span></span>
    * <span data-ttu-id="61d25-111">Op deze pagina kunt u alle loyaliteitstransacties voor de geselecteerde loyaliteitskaart weergeven.</span><span class="sxs-lookup"><span data-stu-id="61d25-111">On this page you can view all loyalty transactions for the selected loyalty card.</span></span>  
5. <span data-ttu-id="61d25-112">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="61d25-112">Close the page.</span></span>
6. <span data-ttu-id="61d25-113">Klik op Kaartcorrecties.</span><span class="sxs-lookup"><span data-stu-id="61d25-113">Click Card adjustments.</span></span>
7. <span data-ttu-id="61d25-114">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="61d25-114">Click New.</span></span>
8. <span data-ttu-id="61d25-115">Typ of selecteer een waarde in het veld Beloningspunt.</span><span class="sxs-lookup"><span data-stu-id="61d25-115">In the Reward point field, enter or select a value.</span></span>
9. <span data-ttu-id="61d25-116">Typ een getal in het veld Bedrag of hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="61d25-116">In the Amount or quantity field, enter a number.</span></span>
    * <span data-ttu-id="61d25-117">U kunt punten toevoegen aan of verwijderen van de loyaliteitskaart door positiever of negatieve bedragen te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="61d25-117">You can add or remove points from the loyalty card by using positive or negative amounts.</span></span>  
10. <span data-ttu-id="61d25-118">Typ of selecteer een waarde in het veld Loyaliteitsprogramma.</span><span class="sxs-lookup"><span data-stu-id="61d25-118">In the Loyalty program field, enter or select a value.</span></span>
11. <span data-ttu-id="61d25-119">Typ een waarde in het veld Opmerking.</span><span class="sxs-lookup"><span data-stu-id="61d25-119">In the Comment field, type a value.</span></span>
12. <span data-ttu-id="61d25-120">Klik op Correctie boeken.</span><span class="sxs-lookup"><span data-stu-id="61d25-120">Click Post adjustment.</span></span>
13. <span data-ttu-id="61d25-121">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="61d25-121">Click Yes.</span></span>
14. <span data-ttu-id="61d25-122">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="61d25-122">Close the page.</span></span>
    * <span data-ttu-id="61d25-123">Normaal gesproken moet u de pagina op dit moment vernieuwen om het resultaat van de correctie van beloningspunten op het tabblad Samenvatting beloningspunten te bekijken. Maar als u dit als een taakbegeleiding uitvoert, mag u nu niet vernieuwen want als u dat wel doet, stopt de taakbegeleiding.</span><span class="sxs-lookup"><span data-stu-id="61d25-123">Normally at this point you'd refresh the page to see the result of the reward points adjustment in the Reward point summary tab. But if you are running this as a task guide, don't refresh now because if you do, the task guide will stop.</span></span>  
15. <span data-ttu-id="61d25-124">Klik op Kaarttransacties.</span><span class="sxs-lookup"><span data-stu-id="61d25-124">Click Card transactions.</span></span>
16. <span data-ttu-id="61d25-125">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="61d25-125">Close the page.</span></span>

