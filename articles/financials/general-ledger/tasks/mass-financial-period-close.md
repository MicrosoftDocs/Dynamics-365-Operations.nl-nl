---
title: Massale sluiting van financiële periode
description: In deze procedure ziet u hoe u een periode in de wachtstand plaatst of definitief afsluit voor meer dan één rechtspersoon tegelijk.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2988b7ab0837cc9a3e4f1c4eaf3fe6e219fa721
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564476"
---
# <a name="mass-financial-period-close"></a><span data-ttu-id="c13d3-103">Massale sluiting van financiële periode</span><span class="sxs-lookup"><span data-stu-id="c13d3-103">Mass financial period close</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c13d3-104">In deze procedure ziet u hoe u een periode in de wachtstand plaatst of definitief afsluit voor meer dan één rechtspersoon tegelijk.</span><span class="sxs-lookup"><span data-stu-id="c13d3-104">This procedure shows how to place a period on hold or permanently close a period or more than one legal entity at a time.</span></span> <span data-ttu-id="c13d3-105">Daarnaast ziet u hoe u een gebruikersgroep kunt blokkeren voor het boeken naar specifieke modules.</span><span class="sxs-lookup"><span data-stu-id="c13d3-105">In addition, the task will show how to restrict user group posting to specific modules.</span></span>

1. <span data-ttu-id="c13d3-106">Ga naar Grootboek > Afgesloten periode > Grootboekkalenders.</span><span class="sxs-lookup"><span data-stu-id="c13d3-106">Go to General ledger > Period close > Ledger calendars.</span></span>
    * <span data-ttu-id="c13d3-107">Merk op dat de getoonde lijst van rechtspersonen afhankelijk is van de fiscale kalender die is geselecteerd op de pagina.</span><span class="sxs-lookup"><span data-stu-id="c13d3-107">Note that the list of legal entities displayed is dependent on the fiscal calendar selected on the page.</span></span> <span data-ttu-id="c13d3-108">Alleen rechtspersonen die de geselecteerde fiscale kalender gebruiken, worden weergeven.</span><span class="sxs-lookup"><span data-stu-id="c13d3-108">Only legal entities using the selected fiscal calendar will display.</span></span>  
2. <span data-ttu-id="c13d3-109">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="c13d3-109">Click Edit.</span></span>
3. <span data-ttu-id="c13d3-110">Selecteer de periode waarvan u de status wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="c13d3-110">Select the period for which you want to modify the status.</span></span>
4. <span data-ttu-id="c13d3-111">Selecteer de rechtspersonen waarvan u de status wilt bijwerken.</span><span class="sxs-lookup"><span data-stu-id="c13d3-111">Select the legal entities for which you want to update the status.</span></span>
    * <span data-ttu-id="c13d3-112">U kunt alle entiteiten snel selecteren door het selectievakje linksbovenin het raster in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="c13d3-112">You can quickly select all legal entities  by selecting the check mark on the upper left side of the grid.</span></span>  
5. <span data-ttu-id="c13d3-113">Selecteer Moduletoegang bijwerken om de toegang voor boeken naar een geselecteerde module te definiëren.</span><span class="sxs-lookup"><span data-stu-id="c13d3-113">Select Update module access to define the posting access to a selected module.</span></span>
    * <span data-ttu-id="c13d3-114">U kunt de modulestatus ook één voor één bijwerken, door de records in het raster te bewerken.</span><span class="sxs-lookup"><span data-stu-id="c13d3-114">The module status can also be updated one-by-one by editing the records in the grid.</span></span> <span data-ttu-id="c13d3-115">De knop is handig wanneer u snel meerdere rechtspersoonrecords wilt bijwerken.</span><span class="sxs-lookup"><span data-stu-id="c13d3-115">The button is useful when you want to quickly update multiple legal entity records.</span></span>  
6. <span data-ttu-id="c13d3-116">Selecteer in de module Toepassing de module waarvan u de status wilt bijwerken.</span><span class="sxs-lookup"><span data-stu-id="c13d3-116">In the Application module, select the module that you want to update the status.</span></span> <span data-ttu-id="c13d3-117">Klik op Selecteren.</span><span class="sxs-lookup"><span data-stu-id="c13d3-117">Click Select.</span></span>
7. <span data-ttu-id="c13d3-118">Selecteer in Toegangsniveau een waarde: Alle, Geen of een specifieke gebruikersgroep.</span><span class="sxs-lookup"><span data-stu-id="c13d3-118">In the Access level, select All, None, or a specific user group.</span></span> <span data-ttu-id="c13d3-119">Klik op Selecteren.</span><span class="sxs-lookup"><span data-stu-id="c13d3-119">Click Select.</span></span>
    * <span data-ttu-id="c13d3-120">Alle geeft aan dat alle gebruikers met bewerkingsmachtiging naar de module kunnen boeken als de periode is geopend.</span><span class="sxs-lookup"><span data-stu-id="c13d3-120">All indicates all users with edit access to the module can post if the period is open.</span></span> <span data-ttu-id="c13d3-121">Geen geeft aan dat gebruikers niet naar de module kunnen boeken als de periode open is.</span><span class="sxs-lookup"><span data-stu-id="c13d3-121">None indicates that users cannot post to the module if the period is open.</span></span> <span data-ttu-id="c13d3-122">Een specifieke gebruikersgroep geeft aan dat alleen gebruikers in de groep naar de module mogen boeken als de periode is geopend.</span><span class="sxs-lookup"><span data-stu-id="c13d3-122">A specific user group indicates only users in the group are able to post to the module if the period is open.</span></span>  
8. <span data-ttu-id="c13d3-123">Klik op Bijwerken.</span><span class="sxs-lookup"><span data-stu-id="c13d3-123">Click Update.</span></span>
9. <span data-ttu-id="c13d3-124">Selecteer een andere periode waarvan u de status wilt bijwerken.</span><span class="sxs-lookup"><span data-stu-id="c13d3-124">Select another period to update the status.</span></span>
10. <span data-ttu-id="c13d3-125">Selecteer de rechtspersonen waarvan u de periodestatus wilt bijwerken.</span><span class="sxs-lookup"><span data-stu-id="c13d3-125">Select the legal entites for which you want to update the period status.</span></span>
11. <span data-ttu-id="c13d3-126">Selecteer Periodestatus bijwerken en stel de status in op In wachtstand, Open of Definitief gesloten.</span><span class="sxs-lookup"><span data-stu-id="c13d3-126">Select Update period status and set the status of On hold, Open, or Permanently closed.</span></span>
    * <span data-ttu-id="c13d3-127">Open geeft aan dat er naar de periode kan worden geboekt, mits de gebruiker toegang heeft.</span><span class="sxs-lookup"><span data-stu-id="c13d3-127">Open indicates the period can be posted to, provided the user has access.</span></span> <span data-ttu-id="c13d3-128">Bij In wachtstand kan er niet worden geboekt naar de periode, maar kan de periode wel worden heropend.</span><span class="sxs-lookup"><span data-stu-id="c13d3-128">On hold means the period cannot be posted to, but the period can be reopened.</span></span> <span data-ttu-id="c13d3-129">Bij Definitief afgesloten is de periode afgesloten en kan hij niet meer worden geopend.</span><span class="sxs-lookup"><span data-stu-id="c13d3-129">Permanently closed means the period is closed and can never be opened.</span></span> <span data-ttu-id="c13d3-130">Aanpassingen kunnen niet worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="c13d3-130">Adjustments cannot be posted.</span></span> <span data-ttu-id="c13d3-131">Het is raadzaam om een periode pas op Definitie afgesloten in te stellen wanneer alle correcties en audits zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="c13d3-131">We do not recommend setting a period to Permanently closed until all adjustments and audits are complete.</span></span>  
12. <span data-ttu-id="c13d3-132">Klik op Bijwerken.</span><span class="sxs-lookup"><span data-stu-id="c13d3-132">Click Update.</span></span>

