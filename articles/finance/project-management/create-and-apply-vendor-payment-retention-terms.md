---
title: Inhoudingstermijnen voor leveranciersbetalingen maken en toepassen
description: Dit onderwerp bevat informatie over het instellen en beheren van inhoudingstermijnen leveranciersbetalingen.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 0e14050a79220b5d02763a025040edb934489d00
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410209"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="bd7a6-103">Inhoudingstermijnen voor leveranciersbetalingen maken en toepassen</span><span class="sxs-lookup"><span data-stu-id="bd7a6-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="bd7a6-104">Het instellen van inhoudingstermijnen voor leveranciersbetalingen voor een project is handig wanneer uw organisatie een deel van de betalingen die aan een leverancier zijn gedaan wil inhouden.</span><span class="sxs-lookup"><span data-stu-id="bd7a6-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="bd7a6-105">Bijvoorbeeld wanneer u de betaling aan een leverancier wilt inhouden totdat de geleverde producten aan uw verwachtingen voldoen.</span><span class="sxs-lookup"><span data-stu-id="bd7a6-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="bd7a6-106">Wanneer u over een leverancierscontract onderhandelt, kunt u de voorwaarden voor betalingsinhouding aan de leverancier opgeven.</span><span class="sxs-lookup"><span data-stu-id="bd7a6-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="bd7a6-107">Inhoudingstermijnen voor leveranciersbetaling maken</span><span class="sxs-lookup"><span data-stu-id="bd7a6-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="bd7a6-108">U kunt het percentage van een leveranciersbetaling voor inhouding invoeren dat u wilt inhouden en het percentage van de eerder ingehouden bedragen dat u wilt vrijgeven.</span><span class="sxs-lookup"><span data-stu-id="bd7a6-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="bd7a6-109">Bedragen worden automatisch op leveranciersfacturen ingehouden, totdat het desbetreffende voltooiingsniveau is bereikt.</span><span class="sxs-lookup"><span data-stu-id="bd7a6-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="bd7a6-110">Nadat u de inhoudingstermijnen voor een leverancier hebt ingesteld, kunt u deze toepassen op elk project voor die leverancier.</span><span class="sxs-lookup"><span data-stu-id="bd7a6-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="bd7a6-111">Gebruik de volgende stappen om inhoudingstermijnen voor leveranciersbetalingen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="bd7a6-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="bd7a6-112">Ga naar **Projectbeheer en boekhouding** > **Inhouding** > **Inhoudingstermijnen voor leveranciersbetaling**.</span><span class="sxs-lookup"><span data-stu-id="bd7a6-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="bd7a6-113">Selecteer **Nieuw** om een nieuwe inhoudingstermijn voor een leverancier toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="bd7a6-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="bd7a6-114">De waarde van **Regel-ID** voor de nieuwe voorwaarde wordt automatisch ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="bd7a6-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="bd7a6-115">Voer een korte omschrijving in het veld **Omschrijving** in en selecteer op het sneltabblad **Voorwaarden** de optie **Regel toevoegen** om waarden voor de volgende instellingen op te geven:</span><span class="sxs-lookup"><span data-stu-id="bd7a6-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="bd7a6-116">**Percentage geleverde eenheden**: voer een voltooiingspercentage voor de termijn in.</span><span class="sxs-lookup"><span data-stu-id="bd7a6-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="bd7a6-117">Bedragen worden automatisch op leveranciersfacturen ingehouden totdat de voltooiingsfase van het project gelijk is aan het opgegeven percentage.</span><span class="sxs-lookup"><span data-stu-id="bd7a6-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="bd7a6-118">Als u bijvoorbeeld 50,00 invoert, worden bedragen ingehouden totdat 50% van het project is voltooid.</span><span class="sxs-lookup"><span data-stu-id="bd7a6-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="bd7a6-119">**In te houden percentage**: voer een percentage van het bedrag van de leveranciersfactuur in dat ingehouden moet worden.</span><span class="sxs-lookup"><span data-stu-id="bd7a6-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="bd7a6-120">Als u in dit veld bijvoorbeeld 10,00 invoert, wordt 10 procent van het bedrag op een leveranciersfactuur ingehouden totdat het project het voltooiingspercentage bereikt dat u instelt in het veld **Percentage geleverde eenheden**.</span><span class="sxs-lookup"><span data-stu-id="bd7a6-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="bd7a6-121">**Vrij te geven percentage**: selecteer **Regel toevoegen** om een percentage van eventuele eerder ingehouden bedragen in te voeren die moeten worden vrijgegeven bij het aangewezen voltooiingsniveau van het project.</span><span class="sxs-lookup"><span data-stu-id="bd7a6-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="bd7a6-122">Als er meer dan één mijlpaal is ingesteld voor verschillende voltooiingsniveaus van een project, voert u een afzonderlijke inhoudingstermijn voor leverancier in voor elke inhoudingsregel.</span><span class="sxs-lookup"><span data-stu-id="bd7a6-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="bd7a6-123">Elke regel kan een ander inhoudingspercentage betekenen en een ander vrij te geven percentage voor elk aangewezen voltooiingsniveau van een project.</span><span class="sxs-lookup"><span data-stu-id="bd7a6-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="bd7a6-124">Nadat u inhoudingstermijnen voor een leverancier hebt ingesteld, kunt u deze toepassen op de termijnen voor een project.</span><span class="sxs-lookup"><span data-stu-id="bd7a6-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="bd7a6-125">Inhoudingstermijnen voor leveranciers toepassen op een project</span><span class="sxs-lookup"><span data-stu-id="bd7a6-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="bd7a6-126">Ga naar **Projectbeheer en boekhouding** > **Projecten** > **Alle projecten** en open een project vanuit de projectlijstpagina.</span><span class="sxs-lookup"><span data-stu-id="bd7a6-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="bd7a6-127">Selecteer op het sneltabblad **Leveranciersovereenkomsten** de optie **Regel toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="bd7a6-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="bd7a6-128">Selecteer in het veld **Rekeningcode** een van de volgende opties:</span><span class="sxs-lookup"><span data-stu-id="bd7a6-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="bd7a6-129">**Tabel**: de inhoudingstermijnen voor leveranciers gelden voor één leverancier.</span><span class="sxs-lookup"><span data-stu-id="bd7a6-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="bd7a6-130">**Groep**: de inhoudingstermijnen voor een leverancier gelden voor alle leveranciers in een leveranciersgroep.</span><span class="sxs-lookup"><span data-stu-id="bd7a6-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="bd7a6-131">**Alle**: de inhoudingstermijnen voor een leverancier gelden voor alle leveranciers.</span><span class="sxs-lookup"><span data-stu-id="bd7a6-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="bd7a6-132">Selecteer in het veld **Leverancier/Leveranciersgroep** de leverancier of leveranciersgroep waarop de inhoudingstermijnen van toepassing zijn.</span><span class="sxs-lookup"><span data-stu-id="bd7a6-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="bd7a6-133">Als u **Alle** hebt geselecteerd in de vorige stap is dit veld niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="bd7a6-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="bd7a6-134">Selecteer in het veld **Inhoudingstermijnen voor leverancier** de inhoudingstermijnen die u in de vorige procedure hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="bd7a6-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="bd7a6-135">Indien ook betalen bij betaling (PWP) is ingesteld bij het project voor die leverancier, voert u het drempelpercentage voor het project in het veld **PWP drempelpercentage** in.</span><span class="sxs-lookup"><span data-stu-id="bd7a6-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="bd7a6-136">De inhoudingsvoorwaarden voor leveranciers worden ook weergegeven op inkooporders die u voor de leverancier maakt.</span><span class="sxs-lookup"><span data-stu-id="bd7a6-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>
