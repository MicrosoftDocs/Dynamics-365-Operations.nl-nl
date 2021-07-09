---
title: Verlof inkopen en verkopen
description: In Dynamics 365 Human Resources kunt u aanvragen voor het kopen en verkopen van verlof indienen op basis van het beleid voor kopen en verkopen dat is ingesteld door uw bedrijf.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d32abacc1539cb930ad6f1ebcfe6fa9af4befcf
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271475"
---
# <a name="buy-and-sell-leave"></a><span data-ttu-id="5d347-103">Verlof inkopen en verkopen</span><span class="sxs-lookup"><span data-stu-id="5d347-103">Buy and sell leave</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="5d347-104">In Dynamics 365 Human Resources kunt u aanvragen voor het kopen en verkopen van verlof indienen op basis van het beleid voor kopen en verkopen dat is ingesteld door uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="5d347-104">In Dynamics 365 Human Resources, you can submit requests to buy and sell leave based on the buy and sell leave policies set up by your company.</span></span>  

## <a name="request-to-buy-leave"></a><span data-ttu-id="5d347-105">Aanvraag om verlof te kopen</span><span class="sxs-lookup"><span data-stu-id="5d347-105">Request to buy leave</span></span>

1. <span data-ttu-id="5d347-106">Selecteer in het werkgebied **Selfservice werknemer** de optie **Aanvraag om verlof te kopen** op de tegel **Verlofsaldi**.</span><span class="sxs-lookup"><span data-stu-id="5d347-106">In the **Employee self service** workspace, select **Buy leave request** in the **Time Off Balances** tile.</span></span> 

2. <span data-ttu-id="5d347-107">Voeg een **verloftype** toe en voer in **hoeveel** verlof u wilt kopen.</span><span class="sxs-lookup"><span data-stu-id="5d347-107">Add a **Leave type** and enter an **Amount** for the amount of leave you'd like to buy.</span></span> 

3. <span data-ttu-id="5d347-108">Selecteer **Indienen** wanneer u gereed bent om uw aanvraag in te dienen.</span><span class="sxs-lookup"><span data-stu-id="5d347-108">Select **Submit** when you're ready to submit your request.</span></span> 

<span data-ttu-id="5d347-109">Uw saldi worden vóór het bijwerken automatisch bijgewerkt of doorlopen een goedkeuringsproces.</span><span class="sxs-lookup"><span data-stu-id="5d347-109">Your balances will either automatically update or go through an approval process before updating.</span></span> <span data-ttu-id="5d347-110">Dit is afhankelijk van hoe het koopbeleid is geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="5d347-110">This depends on how the buy policy has been configured.</span></span>

## <a name="request-to-sell-leave"></a><span data-ttu-id="5d347-111">Aanvraag om verlof te verkopen</span><span class="sxs-lookup"><span data-stu-id="5d347-111">Request to sell leave</span></span>

1. <span data-ttu-id="5d347-112">Selecteer in de werkruimte **Selfservice werknemer** de optie **Aanvraag om verlof te verkopen** op de tegel **Verlofsaldi**.</span><span class="sxs-lookup"><span data-stu-id="5d347-112">In the **Employee self service** workspace, select **Sell leave request** in the **Time Off Balances** tile.</span></span> 

2. <span data-ttu-id="5d347-113">Voeg een **Verloftype** toe en voer een **Hoeveelheid** in voor de hoeveelheid verlof die u wilt verkopen.</span><span class="sxs-lookup"><span data-stu-id="5d347-113">Add a **Leave type** and enter an **Amount** for the amount of leave you'd like to sell.</span></span> 

3. <span data-ttu-id="5d347-114">Selecteer **Indienen** wanneer u gereed bent om uw aanvraag in te dienen.</span><span class="sxs-lookup"><span data-stu-id="5d347-114">Select **Submit** when you're ready to submit your request.</span></span>

<span data-ttu-id="5d347-115">Uw saldi worden vóór het bijwerken automatisch bijgewerkt of doorlopen een goedkeuringsproces.</span><span class="sxs-lookup"><span data-stu-id="5d347-115">Your balances will either automatically update or go through an approval process before updating.</span></span> <span data-ttu-id="5d347-116">Dit is afhankelijk van hoe het koopbeleid is geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="5d347-116">This depends on how the buy policy has been configured.</span></span>


## <a name="troubleshooting"></a><span data-ttu-id="5d347-117">Problemen oplossen</span><span class="sxs-lookup"><span data-stu-id="5d347-117">Troubleshooting</span></span> 

<span data-ttu-id="5d347-118">Als een workflow voor verlofaanvragen voor kopen of verkopen mislukt, kunnen gebruikers met de bevoegdheid **EssLebugBuyBugRequestApprover** het berichtenlogboek controleren voor alle verlofaanvragen voor kopen en verkopen.</span><span class="sxs-lookup"><span data-stu-id="5d347-118">If a buy or sell leave request workflow fails, users with the **EssLeaveBuySellRequestApprover** privilege can review the message log for all leave buy and sell requests.</span></span> <span data-ttu-id="5d347-119">Hiervoor gaat u naar **Verlof en verzuim > Koppeling > Verlofaanvragen kopen en verkopen > Bericht** (linksboven).</span><span class="sxs-lookup"><span data-stu-id="5d347-119">To do this, go to **Leave and absence > Link > Buy and sell leave requests > Message log** (on the upper left).</span></span> <span data-ttu-id="5d347-120">Gebruikers kunnen in **Berichtenlogboek** zien hoe de transacties werden verwerkt en de bijbehorende workflowhistorie wordt getoond.</span><span class="sxs-lookup"><span data-stu-id="5d347-120">The **Message log** shows users how the transactions were processed and the associated workflow history.</span></span>


## <a name="see-also"></a><span data-ttu-id="5d347-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5d347-121">See also</span></span>

[<span data-ttu-id="5d347-122">Overzicht van verlof en verzuim</span><span class="sxs-lookup"><span data-stu-id="5d347-122">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="5d347-123">Beleid voor verlof inkopen/verkopen beheren</span><span class="sxs-lookup"><span data-stu-id="5d347-123">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
