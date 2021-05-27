---
title: Bronbelastingcodes voor het TDS-belastingtype instellen
description: In dit onderwerp wordt uitgelegd hoe u belastingcodes moet instellen voor TDS (belasting ingehouden op bron).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: d56a23f7af7633e1761a8a7c48f71381d6f14df2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023160"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a><span data-ttu-id="5a46a-103">Bronbelastingcodes voor het TDS-belastingtype instellen</span><span class="sxs-lookup"><span data-stu-id="5a46a-103">Set up withholding tax codes for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a46a-104">In dit onderwerp wordt uitgelegd hoe u belastingcodes moet instellen voor TDS (belasting ingehouden op bron).</span><span class="sxs-lookup"><span data-stu-id="5a46a-104">This topic explains how to set up tax codes for Tax Deducted at Source (TDS).</span></span>

1. <span data-ttu-id="5a46a-105">Ga naar **Belasting \> Indirecte belastingen \> Bronbelasting \> Bronbelastingcodes**.</span><span class="sxs-lookup"><span data-stu-id="5a46a-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax codes**.</span></span>

    <span data-ttu-id="5a46a-106">[![Pagina Bronbelastingcodes](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span><span class="sxs-lookup"><span data-stu-id="5a46a-106">[![Withholding tax codes page](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span></span>

2. <span data-ttu-id="5a46a-107">Selecteer in het actievenster **Nieuw** om een bronbelastingcode voor TDS te maken en voer de vereiste gegevens in.</span><span class="sxs-lookup"><span data-stu-id="5a46a-107">On the Action Pane, select **New** to create a withholding tax code for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="5a46a-108">Selecteer op het sneltabblad **Algemeen** in het veld **Belastingtype** de optie **TDS** om de belastingcode als een TDS-belastingcode te categoriseren.</span><span class="sxs-lookup"><span data-stu-id="5a46a-108">On the **General** FastTab, in the **Tax type** field, select **TDS** to categorize the tax code as a TDS tax code.</span></span>
4. <span data-ttu-id="5a46a-109">Selecteer in het veld **Vereffeningsperiode** de TDS-vereffeningsperiode voor de TDS-belastingcode.</span><span class="sxs-lookup"><span data-stu-id="5a46a-109">In the **Settlement period** field, select the TDS settlement period for the TDS tax code.</span></span>
5. <span data-ttu-id="5a46a-110">Selecteer in het veld **Hoofdrekening** de grootboekrekening waar het TDS-bedrag naar moet worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="5a46a-110">In the **Main account** field, select the ledger account that the TDS amount should be posted to.</span></span>
6. <span data-ttu-id="5a46a-111">Selecteer in het veld **Debiteurenrekening** de debiteurenrekening waar het TDS-bedrag, dat wordt afgetrokken in verkooptransacties, naar moet worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="5a46a-111">In the **Receivable account** field, select the receivable account that the TDS amount that is deducted in sales transactions should be posted to.</span></span>

    <span data-ttu-id="5a46a-112">Het veld **Oorsprong** wordt automatisch ingesteld op **Percentage van brutobedrag** en de waarde kan niet worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="5a46a-112">The **Origin** field is automatically set to **Percentage of gross amount**, and the value can't be changed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5a46a-113">U kunt de oorsprong niet instellen op **Percentage van nettobedrag** voor belastingcodes van het TDS-belastingtype.</span><span class="sxs-lookup"><span data-stu-id="5a46a-113">You can't set the origin to **Percentage of net amount** for tax codes of the TDS tax type.</span></span>

7. <span data-ttu-id="5a46a-114">Selecteer in het veld **Bronbelastingcomponent** de TDS-belastingcomponent voor de TDS-belastingcode.</span><span class="sxs-lookup"><span data-stu-id="5a46a-114">In the **Withholding tax component** field, select the TDS tax component for the TDS tax code.</span></span>
8. <span data-ttu-id="5a46a-115">Selecteer **Waarden** in het actievenster om de pagina **Bronbelastingwaarden** te openen.</span><span class="sxs-lookup"><span data-stu-id="5a46a-115">On the Action Pane, select **Values** to open the **Withholding tax values** page.</span></span>
9. <span data-ttu-id="5a46a-116">Voer in het veld **Begindatum** de begindatum in voor de TDS-waarde.</span><span class="sxs-lookup"><span data-stu-id="5a46a-116">In the **From date** field, enter the start date for the TDS value.</span></span> <span data-ttu-id="5a46a-117">Voer in het veld **Einddatum** de einddatum in.</span><span class="sxs-lookup"><span data-stu-id="5a46a-117">In the **To date** field, enter the end date.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5a46a-118">De velden **Ondergrens**, **Bovengrens** en **% uitsluiten** zijn niet beschikbaar voor belastingcodes van het TDS-belastingtype.</span><span class="sxs-lookup"><span data-stu-id="5a46a-118">The **Minimum limit**, **Upper limit**, and **Exclude %** fields aren't available for tax codes of the TDS tax type.</span></span>

10. <span data-ttu-id="5a46a-119">Voer in het veld **Waarde** het TDS-percentage in voor de TDS-belastingcode.</span><span class="sxs-lookup"><span data-stu-id="5a46a-119">In the **Value** field, enter the percentage of TDS for the TDS tax code.</span></span>
11. <span data-ttu-id="5a46a-120">Sluit de pagina **Bronbelastingwaarden** om terug te keren naar de pagina **Bronbelastingcodes**.</span><span class="sxs-lookup"><span data-stu-id="5a46a-120">Close the **Withholding tax values** page to return to the **Withholding tax codes** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5a46a-121">De knop **Limieten** op de pagina **Bronbelastingcodes** is niet beschikbaar voor belastingcodes van het TDS-belastingtype.</span><span class="sxs-lookup"><span data-stu-id="5a46a-121">The **Limits** button on the **Withholding tax codes** page isn't available for tax codes of the TDS tax type.</span></span>

12. <span data-ttu-id="5a46a-122">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5a46a-122">Close the page.</span></span>
