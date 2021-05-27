---
title: Belastingcomponenten voor het belastingtype TDS instellen
description: In dit onderwerp wordt uitgelegd hoe u componenten voor bronbelasting, zoals Huur en Contractant, moet instellen voor het belastingtype TDS (belasting ingehouden op bron). Daarnaast wordt uitgelegd hoe u de drempellimiet definieert die wordt gebruikt om TDS te berekenen voor elke TDS-component.
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
ms.openlocfilehash: 6e0a6a05fcb4afb8c8965e25c3089bc1b3d98431
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023143"
---
# <a name="set-up-tax-components-for-the-tds-tax-type"></a><span data-ttu-id="2b25e-104">Belastingcomponenten voor het belastingtype TDS instellen</span><span class="sxs-lookup"><span data-stu-id="2b25e-104">Set up tax components for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2b25e-105">In dit onderwerp wordt uitgelegd hoe u componenten voor bronbelasting, zoals Huur en Contractant, moet instellen voor het belastingtype TDS (belasting ingehouden op bron).</span><span class="sxs-lookup"><span data-stu-id="2b25e-105">This topic explains how to set up withholding tax components for the Tax Deducted at Source (TDS) tax type.</span></span> <span data-ttu-id="2b25e-106">De TDS-compenten zijn TDS, toeslag, PE-Cess en SHE Cess.</span><span class="sxs-lookup"><span data-stu-id="2b25e-106">The TDS components are TDS, surcharge, PE-Cess, and SHE Cess.</span></span> <span data-ttu-id="2b25e-107">In dit onderwerp wordt daarnaast uitgelegd hoe u de drempellimiet definieert die wordt gebruikt om TDS te berekenen voor elke TDS-component.</span><span class="sxs-lookup"><span data-stu-id="2b25e-107">This topic also explains how to define the threshold that is used to calculate TDS for each TDS component.</span></span> <span data-ttu-id="2b25e-108">Daarnaast kunt u een uitzonderingsdrempel definiëren die wordt gebruikt om TDS te berekenen voor elke TDS-component.</span><span class="sxs-lookup"><span data-stu-id="2b25e-108">Additionally, you can define an exception threshold that is used to calculate TDS for each TDS component.</span></span>

<span data-ttu-id="2b25e-109">Voer de volgende stappen uit om TDS-componenten in te stellen.</span><span class="sxs-lookup"><span data-stu-id="2b25e-109">Follow these steps to set up TDS components.</span></span>

1. <span data-ttu-id="2b25e-110">Ga naar **Belasting \> Instellen \> Bronbelasting \> Bronbelastingcomponenten**.</span><span class="sxs-lookup"><span data-stu-id="2b25e-110">Go to **Tax \> Setup \> Withholding tax \> Withholding tax components**.</span></span>

    <span data-ttu-id="2b25e-111">[![Pagina Bronbelastingcomponenten](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span><span class="sxs-lookup"><span data-stu-id="2b25e-111">[![Withholding tax components page](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span></span>

2. <span data-ttu-id="2b25e-112">Selecteer in het veld **Belastingtype** de optie **TDS** om bronbelastingcomponenten in te stellen voor het belastingtype TDS.</span><span class="sxs-lookup"><span data-stu-id="2b25e-112">In the **Tax type** field, select **TDS** to set up withholding tax components for the TDS tax type.</span></span>
3. <span data-ttu-id="2b25e-113">Selecteer in het actievenster **Nieuw** om een regel te maken.</span><span class="sxs-lookup"><span data-stu-id="2b25e-113">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="2b25e-114">Voer in het veld **Bronbelastingcomponent** een naam in voor de TDS-component.</span><span class="sxs-lookup"><span data-stu-id="2b25e-114">In the **Withholding tax component** field, enter a name for the TDS component.</span></span>
5. <span data-ttu-id="2b25e-115">Selecteer in het veld **Componentgroep voor bronbelasting** de TDS-bronbelastingcomponentgroep waar u de TDS-component aan wilt koppelen.</span><span class="sxs-lookup"><span data-stu-id="2b25e-115">In the **Withholding tax component group** field, select the TDS withholding tax component group to attach the TDS component to.</span></span>
6. <span data-ttu-id="2b25e-116">Typ op het sneltabblad **Algemeen** in het veld **Omschrijving** een beschrijving van de TDS-component.</span><span class="sxs-lookup"><span data-stu-id="2b25e-116">On the **General** FastTab, in the **Description** field, enter a description of  the TDS component.</span></span>
7. <span data-ttu-id="2b25e-117">Selecteer in het actievenster **Drempel** om de pagina **Drempel** te openen zodat u de drempel kunt definiëren die wordt gebruikt om TDS te berekenen voor de TDS-component.</span><span class="sxs-lookup"><span data-stu-id="2b25e-117">On the Action Pane, select **Threshold** to open **Threshold** page, so that you can define the threshold that is used to calculate TDS for the TDS component.</span></span>
8. <span data-ttu-id="2b25e-118">Met de velden **Begindatum** en **Einddatum** kunt u de periode definiëren waarop de drempel van toepassing is.</span><span class="sxs-lookup"><span data-stu-id="2b25e-118">Use the **From date** and **To date** fields to define the period that the threshold is applicable to.</span></span>
9. <span data-ttu-id="2b25e-119">Voer op het sneltabblad **Algemeen** in het veld **Drempel** het drempelbedrag in dat wordt gebruikt om TDS te berekenen voor de TDS-component.</span><span class="sxs-lookup"><span data-stu-id="2b25e-119">On the **General** FastTab, in the **Threshold** field, enter the threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="2b25e-120">De btw wordt alleen bij de bron ingehouden als het cumulatieve factuurbedrag de drempel overschrijdt.</span><span class="sxs-lookup"><span data-stu-id="2b25e-120">The tax will be deducted at the source only when the cumulative invoice amount crosses the threshold.</span></span>

    <span data-ttu-id="2b25e-121">Als het drempelbedrag bijvoorbeeld 10.000 is, wordt TDS berekend nadat het cumulatieve factuurbedrag hoger is dan 10.000 (met andere woorden wanneer het 10.001 of meer is).</span><span class="sxs-lookup"><span data-stu-id="2b25e-121">For example, if the threshold amount is 10,000, TDS is calculated after the cumulative invoice amount exceeds 10,000 (in other words, when it's 10,001 or more).</span></span>

10. <span data-ttu-id="2b25e-122">Voer in het veld **Uitzonderingsdrempel** het uitzonderingsdrempelbedrag in dat wordt gebruikt om TDS te berekenen voor de TDS-component.</span><span class="sxs-lookup"><span data-stu-id="2b25e-122">In the **Exception threshold** field, enter the exception threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="2b25e-123">De belasting op een factuurregel wordt alleen bij de bron ingehouden als het cumulatieve factuurbedrag de uitzonderingsdrempel overschrijdt.</span><span class="sxs-lookup"><span data-stu-id="2b25e-123">The tax on an invoice line will be deducted at the source only when the amount crosses the exception threshold.</span></span>

    <span data-ttu-id="2b25e-124">Als het uitzonderingsdrempelbedrag bijvoorbeeld 5.000 is, wordt TDS berekend op een specifieke factuurregel als het bedrag van de factuurregel hoger is dan 5.000 (met andere woorden, als het 5.001 of meer is).</span><span class="sxs-lookup"><span data-stu-id="2b25e-124">For example, if the exception threshold amount is 5,000, TDS is calculated on a specific invoice line if the invoice line amount exceeds 5,000 (in other words, if it's 5,001 or more).</span></span>

    <span data-ttu-id="2b25e-125">[![Pagina Drempel](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span><span class="sxs-lookup"><span data-stu-id="2b25e-125">[![Threshold page](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="2b25e-126">Het uitzonderingsdrempelbedrag moet lager zijn dan of gelijk zijn aan het drempelbedrag.</span><span class="sxs-lookup"><span data-stu-id="2b25e-126">The exception threshold amount must be less than or equal to the threshold amount.</span></span>
    >
    > <span data-ttu-id="2b25e-127">De belasting wordt voor een transactie ingehouden als het transactiebedrag de uitzonderingsdrempel overschrijdt, zelfs als het cumulatieve factuurbedrag de drempel die is opgegeven in het veld **Drempel** niet overschrijdt.</span><span class="sxs-lookup"><span data-stu-id="2b25e-127">The tax is deducted for a transaction if the transaction amount crosses the exception threshold, even if the cumulative invoice amount doesn't cross the threshold that is specified in the **Threshold** field.</span></span>

11. <span data-ttu-id="2b25e-128">Sluit de pagina **Drempel** om terug te keren naar de pagina **Bronbelastingcomponenten**.</span><span class="sxs-lookup"><span data-stu-id="2b25e-128">Close the **Threshold** page to return to the **Withholding tax components** page.</span></span>
12. <span data-ttu-id="2b25e-129">Selecteer in het actievenster **Kopiëren** om het dialoogvenster **Bronbelastingcomponenten kopiëren** te openen, zodat u de TDS-componenten die voor een TDS-componentgroep zijn ingesteld, naar een andere TDS-componentgroep kunt kopiëren.</span><span class="sxs-lookup"><span data-stu-id="2b25e-129">On the Action Pane, select **Copy** to open the **Copy withholding tax components** dialog box, so that you can copy the TDS components that were set up for one TDS component group to another TDS component group.</span></span>
13. <span data-ttu-id="2b25e-130">Selecteer in het veld **Van** de TDS-componentgroep waar vandaan u de TDS-componenten wilt kopiëren.</span><span class="sxs-lookup"><span data-stu-id="2b25e-130">In the **From** field, select the TDS component group to copy the TDS components from.</span></span> <span data-ttu-id="2b25e-131">Selecteer in het veld **Naar** de componentgroep voor bronbelasting waar u de TDS-componenten naar wilt kopiëren.</span><span class="sxs-lookup"><span data-stu-id="2b25e-131">In the **To** field, select the withholding tax component group to copy the TDS components to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2b25e-132">Veelgebruikte TDS-componenten die aan beide TDS-componentgroepen zijn gekoppeld, worden niet gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="2b25e-132">Common TDS components that are attached to both TDS component groups aren't copied.</span></span>

14. <span data-ttu-id="2b25e-133">Selecteer **OK** om TDS-componenten te kopiëren en te maken voor de andere TDS-componentgroep op de pagina **Bronbelastingcomponenten**.</span><span class="sxs-lookup"><span data-stu-id="2b25e-133">Select **OK** to copy and create TDS components for the other TDS component group on the **Withholding tax components** page.</span></span>

    <span data-ttu-id="2b25e-134">[![Dialoogvenster Bronbelastingcomponenten kopiëren](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span><span class="sxs-lookup"><span data-stu-id="2b25e-134">[![Copy withholding tax components dialog box](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span></span>

15. <span data-ttu-id="2b25e-135">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="2b25e-135">Close the page.</span></span>
