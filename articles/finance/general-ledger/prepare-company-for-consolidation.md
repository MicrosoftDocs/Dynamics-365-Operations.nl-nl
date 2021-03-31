---
title: Een rechtspersoon voorbereiden voor het consolidatieproces
description: Tijdens een consolidatie verzamelt u transacties uit meerdere reeksen rekeningen van rechtspersonen en neemt ze op in één reeks met rekeningen van rechtspersonen. In dit onderwerp wordt uitgelegd hoe u een rechtspersoon voorbereidt voor een consolidatie.
author: jinniew
manager: AnnBe
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 07988e71276c6439e392bce2087f3a8923f5f40b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230197"
---
# <a name="prepare-a-legal-entity-for-the-consolidation-process"></a><span data-ttu-id="ab26c-104">Een rechtspersoon voorbereiden voor het consolidatieproces</span><span class="sxs-lookup"><span data-stu-id="ab26c-104">Prepare a legal entity for the consolidation process</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ab26c-105">Tijdens een consolidatie verzamelt u transacties uit meerdere reeksen rekeningen van rechtspersonen en neemt ze op in één reeks met rekeningen van rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="ab26c-105">During a consolidation, you gather transactions from several sets of legal entity accounts into a single set of legal entity accounts.</span></span> <span data-ttu-id="ab26c-106">In dit onderwerp wordt uitgelegd hoe u een rechtspersoon voorbereidt voor een consolidatie.</span><span class="sxs-lookup"><span data-stu-id="ab26c-106">This topic explains how to prepare a legal entity for a consolidation.</span></span>

> [!NOTE]
> <span data-ttu-id="ab26c-107">Het is raadzaam om Management Reporter voor Microsoft Dynamics 365 Finance te gebruiken om de financiële resultaten voor meerdere rechtspersonen te combineren in een geconsolideerde indeling.</span><span class="sxs-lookup"><span data-stu-id="ab26c-107">We recommend that you use Management Reporter for Microsoft Dynamics 365 Finance to combine the financial results for multiple legal entities in a consolidated format.</span></span> <span data-ttu-id="ab26c-108">Met Management Reporter kunt u geconsolideerde financiële rapporten voor rechtspersonen maken, Excel gebruiken om consolidatiegegevens uit andere bronnen te importeren en bedragen om te zetten in het gewenste aantal aangiftevaluta's zonder dat het consolidatieproces in Dynamics 365 Finance te hoeven uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="ab26c-108">Management Reporter lets you create consolidated financial reports across legal entities, use Excel to import consolidation data from other sources, and translate amounts into any number of reporting currencies without having to run the consolidation process in Dynamics 365 Finance.</span></span>

<span data-ttu-id="ab26c-109">U kunt rapporten, zoals financiële overzichten, afdrukken vanuit de geconsolideerde rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="ab26c-109">You can print reports, such as financial statements, from the consolidated legal entity.</span></span> <span data-ttu-id="ab26c-110">U kunt de geconsolideerde rechtspersoon echter niet gebruiken voor dagelijkse transacties.</span><span class="sxs-lookup"><span data-stu-id="ab26c-110">However, you can't use the consolidated legal entity for daily transactions.</span></span>

<span data-ttu-id="ab26c-111">U kunt gegevens van rechtspersonen consolideren die andere databases gebruiken dan de geconsolideerde rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="ab26c-111">You can consolidate data from legal entities that use different databases than the consolidated legal entity.</span></span> <span data-ttu-id="ab26c-112">Dit consolidatieproces wordt een *importconsolidatie* genoemd.</span><span class="sxs-lookup"><span data-stu-id="ab26c-112">This consolidation process is referred to as an *import consolidation*.</span></span> <span data-ttu-id="ab26c-113">De rechtspersonen kunnen ook dezelfde database gebruiken als de geconsolideerde rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="ab26c-113">Alternatively, the legal entities can use the same database as the consolidated legal entity.</span></span> <span data-ttu-id="ab26c-114">Dit consolidatieproces wordt een *online consolidatie* genoemd.</span><span class="sxs-lookup"><span data-stu-id="ab26c-114">This consolidation process is referred to as an *online consolidation*.</span></span>

<span data-ttu-id="ab26c-115">De geconsolideerde rechtspersoon verzamelt de resultaten en de saldi van de dochterondernemingen.</span><span class="sxs-lookup"><span data-stu-id="ab26c-115">The consolidated legal entity collects the results and balances of the subsidiaries.</span></span> <span data-ttu-id="ab26c-116">Om een geconsolideerde rechtspersoon voor te bereiden op een consolidatie, neemt u de volgende stappen.</span><span class="sxs-lookup"><span data-stu-id="ab26c-116">To prepare a consolidated legal entity for a consolidation, follow these steps.</span></span>

1. <span data-ttu-id="ab26c-117">Ga naar **Grootboek \> Instellen \> Organisatie \> Rechtspersonen**.</span><span class="sxs-lookup"><span data-stu-id="ab26c-117">Go to **General ledger \> Setup \> Organization \> Legal entities**.</span></span>
2. <span data-ttu-id="ab26c-118">Selecteer **Nieuw** om de rechtspersoon te maken die de geconsolideerde rechtspersoon zal zijn.</span><span class="sxs-lookup"><span data-stu-id="ab26c-118">Select **New** to create the legal entity that will be the consolidated legal entity.</span></span>
3. <span data-ttu-id="ab26c-119">Schakel het selectievakje **Gebruiken voor financieel consolidatieproces** in en voer vervolgens informatie in over de geconsolideerde rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="ab26c-119">Select the **Use for financial consolidation process** check box, and then enter information about the consolidated legal entity.</span></span> <span data-ttu-id="ab26c-120">Voer deze informatie precies in zoals u deze wilt weergeven op financiële overzichten voor de geconsolideerde rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="ab26c-120">Be sure to enter this information exactly as you want it to appear on financial statements for the consolidated legal entity.</span></span>
4. <span data-ttu-id="ab26c-121">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ab26c-121">Close the page.</span></span>
5. <span data-ttu-id="ab26c-122">Selecteer de geconsolideerde rechtspersoon in het veld in de rechterbovenhoek van de pagina en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="ab26c-122">Select the consolidated legal entity in the field in the upper-right corner of the page, and then select **OK**.</span></span>
6. <span data-ttu-id="ab26c-123">Ga naar **Grootboek \> Instellen \> Grootboek**.</span><span class="sxs-lookup"><span data-stu-id="ab26c-123">Go to **General ledger \> Setup \> Ledger**.</span></span>
7. <span data-ttu-id="ab26c-124">Selecteer het rekeningschema, de fiscale kalender, de valuta voor de boekhouding, een optionele aangiftevaluta en het standaardtype wisselkoers voor de geconsolideerde rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="ab26c-124">Select the chart of accounts, the fiscal calendar, the accounting currency, an optional reporting currency, and the default type of exchange rate for the consolidated legal entity.</span></span> 
8. <span data-ttu-id="ab26c-125">Ga naar **Grootboek \> Instellen \> Valuta \> Valutawisselkoersen**.</span><span class="sxs-lookup"><span data-stu-id="ab26c-125">Go to **General ledger \> Setup \> Currency \> Currency exchange rates**.</span></span>
9. <span data-ttu-id="ab26c-126">Stel valutawisselkoersen in relevante perioden in voor de valuta's van de dochterondernemingen.</span><span class="sxs-lookup"><span data-stu-id="ab26c-126">Set up currency exchange rates in relevant periods for the currencies of the subsidiary legal entities.</span></span>
10. <span data-ttu-id="ab26c-127">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ab26c-127">Close the page.</span></span>
11. <span data-ttu-id="ab26c-128">Als de geconsolideerde rechtspersoon dochterondernemingen heeft die vreemde valuta's gebruiken, neemt u de volgende stappen:</span><span class="sxs-lookup"><span data-stu-id="ab26c-128">If the consolidated legal entity has subsidiaries that use foreign currencies, follow these steps:</span></span>

    1. <span data-ttu-id="ab26c-129">Ga naar **Grootboek \> Instellen \> Boeken \> Rekeningen voor automatische transacties**.</span><span class="sxs-lookup"><span data-stu-id="ab26c-129">Go to **General ledger \> Setup \> Posting \> Accounts for automatic transactions**.</span></span>
    2. <span data-ttu-id="ab26c-130">Selecteer in het veld **Boekingstype** een geschikte rekening.</span><span class="sxs-lookup"><span data-stu-id="ab26c-130">In the **Posting type** field, select an appropriate account:</span></span>

        - <span data-ttu-id="ab26c-131">Als de rechtspersoon buitenlandse dochtermaatschappijen heeft die financieel of operationeel afhankelijk zijn van de bovenliggende rechtspersoon, selecteert u een geschikte rekening voor het boekingstype **Verlies-en-winstrekening voor consolidatieverschillen**.</span><span class="sxs-lookup"><span data-stu-id="ab26c-131">If the legal entity has foreign subsidiaries that are financially or operationally interdependent with the parent legal entity, select an appropriate account for the **Profit and loss account for consolidation differences** posting type.</span></span>
        - <span data-ttu-id="ab26c-132">Als u een dochteronderneming consolideert die financieel en operationeel onafhankelijk is van de bovenliggende rechtspersoon, of een rechtspersoon met de resultaten van verschillende dochterondernemingen die financieel en operationeel onafhankelijk zijn van de bovenliggende rechtspersoon en als u vertaalmethoden gebruikt om de gegevens te consolideren, selecteert u een geschikte rekening voor het boekingstype **Saldorekening voor consolidatieverschillen**.</span><span class="sxs-lookup"><span data-stu-id="ab26c-132">If you're consolidating a subsidiary that is financially and operationally independent of the parent legal entity, or a legal entity that contains the results of several subsidiaries that are financially and operationally independent of the parent legal entity, and if you're using translation methods to consolidate the data, select an appropriate account for the **Balance account for consolidation differences** posting type.</span></span>

    3. <span data-ttu-id="ab26c-133">Selecteer in het veld **Hoofdrekening** de hoofdrekeningen die moeten worden gebruikt voor aanpassingen van de herwaardering van vreemde valuta.</span><span class="sxs-lookup"><span data-stu-id="ab26c-133">In the **Main account** field, select the main accounts that should be used for foreign currency revaluation adjustments.</span></span>
    4. <span data-ttu-id="ab26c-134">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ab26c-134">Close the page.</span></span>

    <span data-ttu-id="ab26c-135">Als u vroeg in een periode de geconsolideerde rechtspersoon maakt, kunt u vreemde valutabedragen herwaarderen als gewijzigde wisselkoersen tijdens de consolidatieperiode.</span><span class="sxs-lookup"><span data-stu-id="ab26c-135">If you create the consolidated legal entity early in a period, you can revalue foreign currency amounts as exchange rates change during the consolidation period.</span></span>

<span data-ttu-id="ab26c-136">De geconsolideerde rechtspersoon is nu ingesteld voor de periodieke taak **Consolideren**.</span><span class="sxs-lookup"><span data-stu-id="ab26c-136">The consolidated legal entity is now set up for the **Consolidate** periodic job.</span></span> <span data-ttu-id="ab26c-137">U kunt zowel een importconsolidatie als een online consolidatie uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="ab26c-137">You can do either an import consolidation or an online consolidation.</span></span>

- <span data-ttu-id="ab26c-138">Als u een importconsolidatie wilt uitvoeren, gaat u naar **Grootboek \> Periodiek \> Consolideren \> Consolideren \[Importeren uit\]**.</span><span class="sxs-lookup"><span data-stu-id="ab26c-138">To do an import consolidation, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Import from\]**.</span></span>
- <span data-ttu-id="ab26c-139">Als u een onlineconsolidatie wilt uitvoeren, gaat u naar **Grootboek \> Periodiek \> Consolideren \> Consolideren \[Online\]**.</span><span class="sxs-lookup"><span data-stu-id="ab26c-139">To do an online consolidation, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Online\]**.</span></span>

> [!NOTE]
> <span data-ttu-id="ab26c-140">U kunt de consolidatie pas uitvoeren nadat u de dochtermaatschappijen hebt voorbereid voor consolidatie.</span><span class="sxs-lookup"><span data-stu-id="ab26c-140">Before you can process the consolidation, you must prepare the subsidiary legal entities for consolidation.</span></span> <span data-ttu-id="ab26c-141">Zie [Een dochtermaatschappij voor consolidatie instellen](set-up-subsidiary-company-for-consolidation.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="ab26c-141">For more information, see [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]