---
title: Vaste activa afstoten als uitval
description: In dit onderwerp wordt het proces beschreven voor het elimineren van transacties voor een vast activum dat als uitval is afgestoten.
author: moaamer
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 371cc2efa64916698da8e4230825c3c949920698
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975239"
---
# <a name="dispose-of-a-fixed-asset-as-scrap"></a><span data-ttu-id="22a43-103">Vaste activa afstoten als uitval</span><span class="sxs-lookup"><span data-stu-id="22a43-103">Dispose of a fixed asset as scrap</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="22a43-104">In dit onderwerp wordt het proces beschreven voor het elimineren van transacties voor een vast activum dat als uitval is afgestoten.</span><span class="sxs-lookup"><span data-stu-id="22a43-104">The topic describes the process of eliminating transactions for a fixed asset that was disposed of as scrap.</span></span> <span data-ttu-id="22a43-105">De transactietypen die kunnen worden geëlimineerd, zijn onder andere de aanschaf- en geaccumuleerde afschrijvingstransacties van een activum en andere vaste-activatransacties.</span><span class="sxs-lookup"><span data-stu-id="22a43-105">The transaction types that can be eliminated include an asset's acquisition and accumulated depreciation transactions and other fixed asset transactions.</span></span> <span data-ttu-id="22a43-106">Het verwijderen van deze transacties heeft invloed op balansrekeningen, zoals aanschafcorrectie, afschrijvingscorrectie, herwaardering, waardevermeerderings- en waardeverminderingsrekeningen.</span><span class="sxs-lookup"><span data-stu-id="22a43-106">Elimination of these transactions affects balance sheet accounts, such as acquisition adjustment, depreciation adjustment, revaluation, write-up, and write-down accounts.</span></span>

| <span data-ttu-id="22a43-107">Transactie</span><span class="sxs-lookup"><span data-stu-id="22a43-107">Transaction</span></span>                                         | <span data-ttu-id="22a43-108">Debet (Dr.)</span><span class="sxs-lookup"><span data-stu-id="22a43-108">Debit (Dr.)</span></span> | <span data-ttu-id="22a43-109">Credit (Cr.)</span><span class="sxs-lookup"><span data-stu-id="22a43-109">Credit (Cr.)</span></span> |
|-----------------------------------------------------|-------------|--------------|
| <span data-ttu-id="22a43-110">Samengevoegde afschrijving Dr.</span><span class="sxs-lookup"><span data-stu-id="22a43-110">Dr. Accumulated depreciation</span></span>                        | <span data-ttu-id="22a43-111">X</span><span class="sxs-lookup"><span data-stu-id="22a43-111">X</span></span>           |              |
| <span data-ttu-id="22a43-112">Winst/verlies vaste activa Cr.</span><span class="sxs-lookup"><span data-stu-id="22a43-112">Cr. Fixed assets gain/loss</span></span>                          |             | <span data-ttu-id="22a43-113">X</span><span class="sxs-lookup"><span data-stu-id="22a43-113">X</span></span>            |
| <span data-ttu-id="22a43-114">Winst/verlies vaste activa Dr.</span><span class="sxs-lookup"><span data-stu-id="22a43-114">Dr. Fixed assets gain/loss</span></span>                          | <span data-ttu-id="22a43-115">X</span><span class="sxs-lookup"><span data-stu-id="22a43-115">X</span></span>           |              |
| <span data-ttu-id="22a43-116">Aanschafrekening voor vaste activa Cr.</span><span class="sxs-lookup"><span data-stu-id="22a43-116">Cr. Fixed asset acquisition account</span></span>                 |             | <span data-ttu-id="22a43-117">X</span><span class="sxs-lookup"><span data-stu-id="22a43-117">X</span></span>            |
| <span data-ttu-id="22a43-118">Winst/verlies vaste activa Dr. (nettoboekwaarde \[NBV\])</span><span class="sxs-lookup"><span data-stu-id="22a43-118">Dr. Fixed assets gain/loss (net book value \[NBV\])</span></span> | <span data-ttu-id="22a43-119">X</span><span class="sxs-lookup"><span data-stu-id="22a43-119">X</span></span>           |              |
| <span data-ttu-id="22a43-120">Winst/verlies vaste activa Cr. (NBW)</span><span class="sxs-lookup"><span data-stu-id="22a43-120">Cr. Fixed assets gain/loss (NBV)</span></span>                    |             | <span data-ttu-id="22a43-121">X</span><span class="sxs-lookup"><span data-stu-id="22a43-121">X</span></span>            |

> [!NOTE]
> <span data-ttu-id="22a43-122">We raden u aan nauw samen te werken met de Chief Financial Officer (CFO) of de controller van uw bedrijf om de juiste rekeningen te identificeren die voor elk transactietype moeten worden gebruikt, en ook om te controleren of deze rekeningen op de juiste manier worden bijgewerkt door het buitengebruikstellingsproces en de transacties die erdoor worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="22a43-122">We recommend that you work closely with your company's chief financial officer (CFO) or controller to identify the correct accounts that should be used for each transaction type, and also to verify that the disposal process and the transactions that it generates update those accounts correctly.</span></span>

<span data-ttu-id="22a43-123">Voordat u een vast activum afstoot als uitval, moet u grootboekrekeningen maken die zijn gekoppeld aan de aanschafwaarde van het activum, afschrijving voor het huidige jaar, afschrijving voor voorgaande jaren en de NBW van het activum.</span><span class="sxs-lookup"><span data-stu-id="22a43-123">Before you dispose of a fixed asset as scrap, you must create ledger accounts that are associated with the asset's acquisition value, depreciation for the current year, depreciation for previous years, and the asset's NBV.</span></span> <span data-ttu-id="22a43-124">De transactietypen van de vaste activa worden vermeld op de pagina **Boekingsprofielen van vaste activa**.</span><span class="sxs-lookup"><span data-stu-id="22a43-124">The fixed asset transaction types are listed on the **Fixed assets posting profile** page.</span></span> <span data-ttu-id="22a43-125">Ga naar **Vaste activa \> Instellen \> Boekingsprofielen voor vaste activa** en selecteer op het sneltabblad **Afstoting** de optie **Uitval** in het veld boven het raster.</span><span class="sxs-lookup"><span data-stu-id="22a43-125">Go to **Fixed assets \> Setup \> Fixed asset posting profiles**, and then, on the **Disposal** FastTab, select **Scrap** in the field above the grid.</span></span> <span data-ttu-id="22a43-126">In de volgende afbeelding ziet u de lijst met transactietypen voor vaste activa op de pagina **Boekingsprofielen vaste activa**.</span><span class="sxs-lookup"><span data-stu-id="22a43-126">The following illustration shows the list of fixed asset transaction types on the **Fixed asset posting profiles** page.</span></span>


<span data-ttu-id="22a43-127">[![Een activum afstoten als uitval, figuur 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span><span class="sxs-lookup"><span data-stu-id="22a43-127">[![Disposing of an asset as scap, Fig. 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span></span>

<span data-ttu-id="22a43-128">Voor het volgende voorbeeld is een vast activum aangeschaft op 1 januari 2018 en afgestoten op 31 maart 2019.</span><span class="sxs-lookup"><span data-stu-id="22a43-128">For the following example, a fixed asset was acquired on January 1, 2018, and it will be scrapped on March 31, 2019.</span></span>

- <span data-ttu-id="22a43-129">**Aanschafprijs:** 24.000,00 euro Amerikaanse dollars (USD)</span><span class="sxs-lookup"><span data-stu-id="22a43-129">**Acquisition price:** 24,000.00 US dollars (USD)</span></span>
- <span data-ttu-id="22a43-130">**Levensduur:** twee kaar</span><span class="sxs-lookup"><span data-stu-id="22a43-130">**Service life:** Two years</span></span>
- <span data-ttu-id="22a43-131">**Afschrijvingsmethode:** lineaire levensduur</span><span class="sxs-lookup"><span data-stu-id="22a43-131">**Depreciation method:** Straight line service life</span></span>
- <span data-ttu-id="22a43-132">**Afschrijvingsbedrag** : 1.000,00 USD per maand</span><span class="sxs-lookup"><span data-stu-id="22a43-132">**Depreciation amount:** 1,000.00 USD per month</span></span>

<span data-ttu-id="22a43-133">De NBW van een vast activum wordt met de volgende formule berekend:</span><span class="sxs-lookup"><span data-stu-id="22a43-133">The NBV of a fixed asset is calculated by using the following formula:</span></span>

<span data-ttu-id="22a43-134">Nettoboekwaarde = aanschafprijs – afschrijving</span><span class="sxs-lookup"><span data-stu-id="22a43-134">Net book value = Acquisition price – Depreciation</span></span>

<span data-ttu-id="22a43-135">In dit voorbeeld is de vaste activa verworven en 15 maanden lang afgeschreven, van januari 2018 tot en met maart 2019.</span><span class="sxs-lookup"><span data-stu-id="22a43-135">In this example, the fixed asset was acquired and was depreciated for 15 months, from January 2018 through March 2019.</span></span> <span data-ttu-id="22a43-136">Daarom is de NBW van het activum 9.000,00 USD (24.000,00 USD - 15.000,00 USD).</span><span class="sxs-lookup"><span data-stu-id="22a43-136">Therefore, the asset's NBV is 9,000.00 USD (24,000.00 USD – 15,000.00 USD).</span></span>

<span data-ttu-id="22a43-137">[![Voorbeeld van afschrijving voor vaste activa](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span><span class="sxs-lookup"><span data-stu-id="22a43-137">[![Fixed asset depreciation example](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span></span>


<span data-ttu-id="22a43-138">Als u een buitengebruikstellingsjournaal wilt maken, gaat u naar **Vaste activa \> Journaalboekingen \> Vaste-activajournaal** en selecteert u **Regels** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="22a43-138">To create a disposal journal, go to **Fixed assets \> Journal entries \> Fixed assets journal**, and then, on the Action Pane, select **Lines**.</span></span> <span data-ttu-id="22a43-139">Selecteer **Afstoting - uitval** en vervolgens een vaste-activa-id.</span><span class="sxs-lookup"><span data-stu-id="22a43-139">Select **Disposal – scrap**, and then select a fixed asset ID.</span></span> <span data-ttu-id="22a43-140">Als u het activum volledig wilt afstoten, voert u geen waarde in het veld **Debet** of het veld **Credit** in.</span><span class="sxs-lookup"><span data-stu-id="22a43-140">To fully dispose of the asset, don't enter a value in either the **Debit** field or the **Credit** field.</span></span>

<span data-ttu-id="22a43-141">[![Vaste-activajournaal](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span><span class="sxs-lookup"><span data-stu-id="22a43-141">[![Fixed assets journal](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span></span>

<span data-ttu-id="22a43-142">Met de uitvaltransactie voor vaste activa worden de veldwaarden op de volgende manieren gewijzigd in het vaste-activaboek:</span><span class="sxs-lookup"><span data-stu-id="22a43-142">The fixed asset disposal scrap transaction changes the field values for the fixed asset book in the following ways:</span></span>

- <span data-ttu-id="22a43-143">In de sectie **Saldo** wordt het veld **Status** bijgewerkt naar **Buiten gebruik gesteld**.</span><span class="sxs-lookup"><span data-stu-id="22a43-143">In the **Balance** section, the **Status** field is updated to **Scrapped**.</span></span>
- <span data-ttu-id="22a43-144">In de sectie **Uitgifte** wordt het veld **Afstotingsdatum** ingesteld op de datum waarop het activum buiten gebruik is gesteld.</span><span class="sxs-lookup"><span data-stu-id="22a43-144">In the **Issue** section, the **Disposal date** field is set to the date when the asset was scrapped.</span></span>

<span data-ttu-id="22a43-145">[![Details vaste-activajournaal](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span><span class="sxs-lookup"><span data-stu-id="22a43-145">[![Fixed assets journal detail](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span></span>

<span data-ttu-id="22a43-146">In de volgende afbeelding wordt het vaste-activasaldo weergegeven.</span><span class="sxs-lookup"><span data-stu-id="22a43-146">The following illustration shows the fixed asset balance.</span></span>

<span data-ttu-id="22a43-147">[![Vaste-activasaldo](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span><span class="sxs-lookup"><span data-stu-id="22a43-147">[![Fixed asset balance](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span></span>

<span data-ttu-id="22a43-148">In de volgende afbeelding wordt het boekstuk weergegeven dat is geboekt.</span><span class="sxs-lookup"><span data-stu-id="22a43-148">The following illustration shows the voucher that is posted.</span></span>

<span data-ttu-id="22a43-149">[![Nettoboekwaarde](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span><span class="sxs-lookup"><span data-stu-id="22a43-149">[![Net book value](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span></span>
