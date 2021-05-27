---
title: TDS-belastingcodes koppelen aan TDS-belastinggroepen en de formule voor het berekenen van TDS definiëren
description: In dit onderwerp wordt uitgelegd hoe u belastinggroepen voor TDS (belasting ingehouden op bron) kunt instellen en TDS-belastingcodes kunt koppelen aan TDS-belastinggroepen. Als u TDS voor een TDS-belastinggroep wilt berekenen, moet u de formule definiëren voor TDS-belastingcodes die eraan zijn gekoppeld.
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
ms.openlocfilehash: ec0d683153bd5ab731035159d32881fbdb352d70
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023157"
---
# <a name="attach-tds-tax-codes-to-tds-tax-groups-and-define-the-formula-for-calculating-tds"></a><span data-ttu-id="f5a10-104">TDS-belastingcodes koppelen aan TDS-belastinggroepen en de formule voor het berekenen van TDS definiëren</span><span class="sxs-lookup"><span data-stu-id="f5a10-104">Attach TDS tax codes to TDS tax groups and define the formula for calculating TDS</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f5a10-105">In dit onderwerp wordt uitgelegd hoe u belastinggroepen voor TDS (belasting ingehouden op bron) kunt instellen en TDS-belastingcodes kunt koppelen aan TDS-belastinggroepen.</span><span class="sxs-lookup"><span data-stu-id="f5a10-105">This topic explains how to set up Tax Deducted at Source (TDS) tax groups and attach TDS tax codes to TDS tax groups.</span></span> <span data-ttu-id="f5a10-106">Als u TDS voor een TDS-belastinggroep wilt berekenen, moet u de formule definiëren voor TDS-belastingcodes die eraan zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="f5a10-106">To calculate TDS for a TDS tax group, you must define the formula for TDS tax codes that are attached to it.</span></span>

<span data-ttu-id="f5a10-107">Volg deze stappen om een TDS-belastinggroep in te stellen, hier TDS-belastingcodes aan te koppelen en de formule voor het berekenen van TDS te definiëren.</span><span class="sxs-lookup"><span data-stu-id="f5a10-107">Follow these steps to set up a TDS tax group, attach TDS tax codes to it, and define the formula for calculating TDS.</span></span>

1. <span data-ttu-id="f5a10-108">Ga naar **Belasting \> Indirecte belastingen \> Bronbelasting \> Bronbelastinggroepen**.</span><span class="sxs-lookup"><span data-stu-id="f5a10-108">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax groups**.</span></span>

    <span data-ttu-id="f5a10-109">[![Pagina Bronbelastinggroepen](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span><span class="sxs-lookup"><span data-stu-id="f5a10-109">[![Withholding tax groups page](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span></span>

2. <span data-ttu-id="f5a10-110">Selecteer in het actievenster **Nieuw** om een bronbelastinggroep voor TDS te maken en voer de vereiste gegevens in.</span><span class="sxs-lookup"><span data-stu-id="f5a10-110">On the Action Pane, select **New** to create a withholding tax group for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="f5a10-111">Selecteer in het veld **Belastingtype** de optie **TDS**.</span><span class="sxs-lookup"><span data-stu-id="f5a10-111">In the **Tax type** field, select **TDS**.</span></span>
4. <span data-ttu-id="f5a10-112">Selecteer op het sneltabblad **Instellingen** de optie **Toevoegen** om een regel te maken.</span><span class="sxs-lookup"><span data-stu-id="f5a10-112">On the **Setup** FastTab, select **Add** to create a line.</span></span>
5. <span data-ttu-id="f5a10-113">Selecteer in het veld **Bronbelastingcode** de TDS-belastingcode voor de TDS-belastinggroep.</span><span class="sxs-lookup"><span data-stu-id="f5a10-113">In the **Withholding tax code** field, select the TDS tax code for the TDS tax group.</span></span> <span data-ttu-id="f5a10-114">In het veld **Bronbelastingnaam** wordt de naam van de TDS-belastingcode en de waarde in het veld **Waarde** weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f5a10-114">The **Withholding tax name** field shows the name of the TDS tax code, and the **Value** field shows the value.</span></span>
6. <span data-ttu-id="f5a10-115">Schakel het selectievakje **Drempel overslaan** in als u de drempellimiet en uitzonderingsdrempellimiet wilt negeren die zijn gedefinieerd voor de TDS-belastingcomponent die is gekoppeld aan de TDS-belastingcode in TDS-transacties.</span><span class="sxs-lookup"><span data-stu-id="f5a10-115">To ignore the threshold limit and exception threshold limit that are defined for the TDS tax component that is attached to the TDS tax code in TDS transactions, select the **Overlook threshold** check box.</span></span>
7. <span data-ttu-id="f5a10-116">Schakel het selectievakje **Vrijstelling** in om te voorkomen dat de belastinggroep wordt berekend in transacties.</span><span class="sxs-lookup"><span data-stu-id="f5a10-116">To prevent the tax group from being calculated in transactions, select the **Exempt** check box.</span></span>
8. <span data-ttu-id="f5a10-117">Selecteer in het actievenster **Ontwerper** om de formuleontwerper te openen, zodat u de formule kunt definiëren voor het berekenen van TDS voor de TDS-belastinggroep.</span><span class="sxs-lookup"><span data-stu-id="f5a10-117">On the Action Pane, select **Designer** to open the formula designer, so that you can define the formula for calculating TDS for the TDS tax group.</span></span> <span data-ttu-id="f5a10-118">Op de pagina **Ontwerper** worden op het tabblad **Belastingen** de TDS-belastingcodes weergegeven die zijn geselecteerd voor de TDS-belastinggroep.</span><span class="sxs-lookup"><span data-stu-id="f5a10-118">On the **Designer** page, the **Taxes** tab shows the TDS tax codes that have been selected for the TDS tax group.</span></span>

    <span data-ttu-id="f5a10-119">[![Pagina Ontwerper](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span><span class="sxs-lookup"><span data-stu-id="f5a10-119">[![Designer page](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span></span>

9. <span data-ttu-id="f5a10-120">Selecteer **Alt+N** op het tabblad **Berekening** om een regel te maken.</span><span class="sxs-lookup"><span data-stu-id="f5a10-120">On the **Calculation** tab, select **Alt+N** to create a line.</span></span> <span data-ttu-id="f5a10-121">Het veld **Id** geeft de automatisch gegenereerde prioriteits-id weer voor de TDS-berekening.</span><span class="sxs-lookup"><span data-stu-id="f5a10-121">The **ID** field shows the automatically generated priority ID for TDS calculation.</span></span>
10. <span data-ttu-id="f5a10-122">Selecteer in het veld **Belastingcode** de TDS-belastingcode waarvoor u de formule wilt definiëren.</span><span class="sxs-lookup"><span data-stu-id="f5a10-122">In the **Tax code** field, select the TDS tax code to define the formula for.</span></span> <span data-ttu-id="f5a10-123">Alle TDS-belastingcodes die zijn geselecteerd voor de TDS-belastinggroep kunnen in dit veld worden geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="f5a10-123">All the TDS tax codes that have been selected for the TDS tax group are available for selection in this field.</span></span>
11. <span data-ttu-id="f5a10-124">Selecteer in het veld **Belastbare basis** de basis voor het berekenen van de TDS:</span><span class="sxs-lookup"><span data-stu-id="f5a10-124">In the **Taxable basis** field, select the basis for calculating TDS:</span></span>

    - <span data-ttu-id="f5a10-125">**Brutobedrag**: TDS berekenen op basis van het brutotransactiebedrag (dat wil zeggen het factuurbedrag) met behulp van de berekeningsexpressie die voor de belastingcode is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="f5a10-125">**Gross amount** – Calculate TDS based on the gross transaction amount (that is, the invoice amount) by using the calculation expression that is defined for the tax code.</span></span>
    - <span data-ttu-id="f5a10-126">**Excl. brutobedrag**: TDS berekenen op basis van de berekeningsexpressie die voor de belastingcode is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="f5a10-126">**Excl Gross amount** – Calculate TDS based on the calculation expression that is defined for the tax code.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f5a10-127">Het veld **Belastbare basis** kan niet worden ingesteld op **Excl. brutobedrag** voor de TDS-belastingcode met prioriteits-id **1**.</span><span class="sxs-lookup"><span data-stu-id="f5a10-127">The **Taxable basis** field can't be set to **Excl Gross amount** for the TDS tax code that has a priority ID of **1**.</span></span>

12. <span data-ttu-id="f5a10-128">De TDS-berekening is gebaseerd op de formule die is gedefinieerd in het veld **Berekeningsexpressie** voor elke belastingcode die is gekoppeld aan de TDS-belastinggroep.</span><span class="sxs-lookup"><span data-stu-id="f5a10-128">The TDS calculation is based on the formula that is defined in the **Calculation expression** field for each tax code that is attached to the TDS tax group.</span></span> <span data-ttu-id="f5a10-129">Selecteer de knop met het plusteken (**+**), minteken (**-**), vermenigvuldigingsteken (**\**_) of deelteken (_*/**) om de berekeningsexpressie in te voeren voor de geselecteerde belastingcode in het veld **Berekeningsexpressie**.</span><span class="sxs-lookup"><span data-stu-id="f5a10-129">Select the plus sign (**+**), minus sign (**-**), multiplication sign (**\**_), or division sign (_*/**) button to enter the calculation expression for the selected TDS tax code in the **Calculation expression** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f5a10-130">Er kan geen berekeningsexpressie worden gedefinieerd voor de TDS-belastingcode met prioriteits-id **1**.</span><span class="sxs-lookup"><span data-stu-id="f5a10-130">No calculation expression can be defined for the TDS tax code that has a priority ID of **1**.</span></span>

13. <span data-ttu-id="f5a10-131">Als u de berekeningsexpressie voor de TDS-belastingcode wilt definiëren in het veld **Berekeningsexpressie**, voegt u TDS-belastingcodes toe die beschikbaar zijn op het tabblad **Belastingen**. Als u TDS-belastingcodes wilt toevoegen aan het veld **Berekeningsexpressie**, kunt u een van de volgende methoden gebruiken:</span><span class="sxs-lookup"><span data-stu-id="f5a10-131">To define the calculation expression for the TDS tax code in the **Calculation expression** field, add TDS tax codes that are available on the **Taxes** tab. To add TDS tax codes in the **Calculation expression** field, you can use any of the following methods:</span></span>

    - <span data-ttu-id="f5a10-132">Sleep de vereiste belastingcode van het tabblad **Belastingen** naar het veld **Berekeningsexpressie**.</span><span class="sxs-lookup"><span data-stu-id="f5a10-132">Drag the required tax code from the **Taxes** tab to the **Calculation expression** field.</span></span>
    - <span data-ttu-id="f5a10-133">Dubbelklik op de vereiste belastingcode op het tabblad **Belastingen** of dubbelklik erop.</span><span class="sxs-lookup"><span data-stu-id="f5a10-133">Double-tap (or double-click) the required tax code on the **Taxes** tab.</span></span>
    - <span data-ttu-id="f5a10-134">Selecteer de vereiste belastingcode op het tabblad **Belastingen** en houd deze vast (of klik met de rechtermuisknop) en selecteer **Belastingcode toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="f5a10-134">Select and hold (or right-click) the required tax code on the **Taxes** tab, and then select **Add tax code**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f5a10-135">Een berekeningsexpressie invoegen vóór elke TDS-belastingcode.</span><span class="sxs-lookup"><span data-stu-id="f5a10-135">Insert a calculation expression before each TDS tax code.</span></span> <span data-ttu-id="f5a10-136">De TDS-belastingcodes die aan de berekeningsexpressie zijn toegevoegd, worden tussen haakjes weergegeven (\[...\]).</span><span class="sxs-lookup"><span data-stu-id="f5a10-136">The TDS tax codes that have been added to the calculation expression appear in brackets (\[...\]).</span></span>

14. <span data-ttu-id="f5a10-137">Als u de berekeningsexpressie wilt verwijderen die is gedefinieerd voor een belastingcode in het veld **Berekeningsexpressie**, selecteert u de knop **C**.</span><span class="sxs-lookup"><span data-stu-id="f5a10-137">To clear the calculation expression that is defined for a tax code in the **Calculation expression** field, select the **C** button.</span></span>
15. <span data-ttu-id="f5a10-138">Als u een record op het tabblad **Berekening** wilt verwijderen, selecteert u **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="f5a10-138">To delete a record on the **Calculation** tab, select **Delete**.</span></span>
16. <span data-ttu-id="f5a10-139">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f5a10-139">Close the page.</span></span>
