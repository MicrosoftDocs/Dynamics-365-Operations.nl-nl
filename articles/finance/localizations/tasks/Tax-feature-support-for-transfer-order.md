---
title: Ondersteuning voor belastingfunctie voor transferorders
description: In dit onderwerp wordt de ondersteuning voor de nieuwe belastingfunctie met behulp van de service voor belastingberekening uitgelegd.
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d1b99046b0e439c9dadbb240050e270a7b2a6914
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920950"
---
# <a name="tax-feature-support-for-transfer-orders"></a><span data-ttu-id="fcff1-103">Ondersteuning voor belastingfunctie voor transferorders</span><span class="sxs-lookup"><span data-stu-id="fcff1-103">Tax feature support for transfer orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fcff1-104">In dit onderwerp vindt u informatie over belastingberekening en boekingsintegratie in transferorders.</span><span class="sxs-lookup"><span data-stu-id="fcff1-104">This topic provides information about tax calculation and posting integration in transfer orders.</span></span> <span data-ttu-id="fcff1-105">Met deze functionaliteit kunt u belastingberekening en boekingen in transferorders instellen voor voorraadtransfers.</span><span class="sxs-lookup"><span data-stu-id="fcff1-105">This functionality lets you set up tax calculation and posting in transfer orders for stock transfers.</span></span> <span data-ttu-id="fcff1-106">Volgens de btw-regelgeving van de Europese Unie (EU) worden voorraadtransfers beschouwd als intracommunautaire leveringen en intracommunautaire verwervingen.</span><span class="sxs-lookup"><span data-stu-id="fcff1-106">Under European Union (EU) value-added tax (VAT) regulations, stock transfers are considered intra-community supply and intra-community acquisitions.</span></span>

<span data-ttu-id="fcff1-107">Als u deze functionaliteit wilt configureren en gebruiken, moet u drie hoofdstappen uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="fcff1-107">To configure and use this functionality, you must complete three main steps:</span></span>

1. <span data-ttu-id="fcff1-108">**RCS-instellingen**: stel in Regulatory Configuration Service de belastingfunctie, belastingcodes en toepasbaarheid van belastingcodes in die moeten worden gebruikt voor de bepaling van belastingcodes in transferorders.</span><span class="sxs-lookup"><span data-stu-id="fcff1-108">**RCS setup:** In Regulatory Configuration Service, set up the tax feature, tax codes, and tax codes applicability for tax code determination in transfer orders.</span></span>
2. <span data-ttu-id="fcff1-109">**Financiële instellingen**: schakel in Microsoft Dynamics 365 Finance de functie **Belasting in transferorder** in, stel de belastingserviceparameters voor voorraad in en stel kernbelastingparameters in.</span><span class="sxs-lookup"><span data-stu-id="fcff1-109">**Finance setup:** In Microsoft Dynamics 365 Finance, turn on the **Tax in transfer order** feature, set up the tax service parameters for inventory, and set up core tax parameters.</span></span>
3. <span data-ttu-id="fcff1-110">**Voorraadinstellingen**: stel de voorraadconfiguratie in voor transferordertransacties.</span><span class="sxs-lookup"><span data-stu-id="fcff1-110">**Inventory setup:** Set up the inventory configuration for transfer order transactions.</span></span>

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a><span data-ttu-id="fcff1-111">RCS instellen voor belasting- en transferordertransacties</span><span class="sxs-lookup"><span data-stu-id="fcff1-111">Set up RCS for tax and transfer order transactions</span></span>

<span data-ttu-id="fcff1-112">Volg deze stappen om de belasting voor een transferorder in te stellen.</span><span class="sxs-lookup"><span data-stu-id="fcff1-112">Follow these steps to set up the tax that is involved in a transfer order.</span></span> <span data-ttu-id="fcff1-113">In het voorbeeld dat hier wordt weergegeven, gaat het om een transferorder van Nederland naar België.</span><span class="sxs-lookup"><span data-stu-id="fcff1-113">In the example that is shown here, the transfer order is from the Netherlands to Belgium.</span></span>

1. <span data-ttu-id="fcff1-114">Selecteer op de pagina **Belastingfuncties** op het tabblad **Versies** de conceptfunctieversie en selecteer vervolgens **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-114">On the **Tax features** page, on the **Versions** tab, select the draft feature version, and then select **Edit**.</span></span>

    ![Bewerken selecteren](../media/image1.png)

2. <span data-ttu-id="fcff1-116">Selecteer **Toevoegen** op het tabblad **Belastingcodes** op de pagina **Belastingfuncties instellen** om nieuwe belastingcodes te maken.</span><span class="sxs-lookup"><span data-stu-id="fcff1-116">On the **Tax features setup** page, on the **Tax codes** tab, select **Add** to create new tax codes.</span></span> <span data-ttu-id="fcff1-117">Voor dit voorbeeld worden drie belastingcodes gemaakt: **NL-Vrijgesteld**, **BE-RC-21** en **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-117">For this example, three tax codes are created: **NL-Exempt**, **BE-RC-21**, and **BE-RC+21**.</span></span>

    - <span data-ttu-id="fcff1-118">Wanneer een transferorder vanuit een magazijn in Nederland wordt verzonden, wordt de Nederlandse code voor vrijgestelde btw (**NL-Vrijgesteld**) toegepast.</span><span class="sxs-lookup"><span data-stu-id="fcff1-118">When a transfer order is shipped from a warehouse in the Netherlands, the Netherlands VAT exempted tax code (**NL-Exempt**) is applied.</span></span>
      
        <span data-ttu-id="fcff1-119">Maak de belastingcode **NL-Vrijgesteld**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-119">Create the tax code **NL-Exempt**.</span></span>
        1. <span data-ttu-id="fcff1-120">Selecteer **Toevoegen** en voer **NL-Vrijgesteld** in het veld **Belastingcode** in.</span><span class="sxs-lookup"><span data-stu-id="fcff1-120">Select **Add**, enter **NL-Exempt** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="fcff1-121">Selecteer **Op nettobedrag** in het veld **Belastingcomponent**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-121">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="fcff1-122">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-122">Select **Save**.</span></span>
        4. <span data-ttu-id="fcff1-123">Selecteer **Toevoegen** in de tabel **Tarief**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-123">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="fcff1-124">Stel **Is Vrijgesteld** in op **Ja** in de sectie **Algemeen**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-124">Swtich **Is Exempt** to **Yes** in the **General** section.</span></span>

        ![Belastingcode NL-Vrijgesteld](../media/image2.png)

    - <span data-ttu-id="fcff1-126">Wanneer een transferorder wordt ontvangen in een Belgisch magazijn, wordt het terugboekingsmechanisme toegepast op basis van de belastingcodes **BE-RC-21** en **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-126">When a transfer order is received at a Belgium warehouse, the reverse charge mechanism is applied by using the **BE-RC-21** and **BE-RC+21** tax codes.</span></span>
        
        <span data-ttu-id="fcff1-127">Maak de belastingcode **BE-RC-21**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-127">Create the tax code **BE-RC-21**.</span></span>      
        1. <span data-ttu-id="fcff1-128">Selecteer **Toevoegen** en voer **BE-RC-21** in het veld **Belastingcode** in.</span><span class="sxs-lookup"><span data-stu-id="fcff1-128">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="fcff1-129">Selecteer **Op nettobedrag** in het veld **Belastingcomponent**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-129">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="fcff1-130">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-130">Select **Save**.</span></span>
        4. <span data-ttu-id="fcff1-131">Selecteer **Toevoegen** in de tabel **Tarief**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-131">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="fcff1-132">Voer **-21** in het veld **Belastingtarief** in.</span><span class="sxs-lookup"><span data-stu-id="fcff1-132">Enter **-21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="fcff1-133">Stel **Is Terugboeking** in op **Ja** in de sectie **Algemeen**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-133">Swtich **Is Reverse Charge** to **Yes** in the **General** section.</span></span>
        7. <span data-ttu-id="fcff1-134">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-134">Select **Save**.</span></span>

        ![BE-RC-21-belastingcode voor terugboekingen](../media/image3.png)
        
        <span data-ttu-id="fcff1-136">Maak de belastingcode **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-136">Create the tax code **BE-RC+21**.</span></span>
        1. <span data-ttu-id="fcff1-137">Selecteer **Toevoegen** en voer **BE-RC-21** in het veld **Belastingcode** in.</span><span class="sxs-lookup"><span data-stu-id="fcff1-137">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="fcff1-138">Selecteer **Op nettobedrag** in het veld **Belastingcomponent**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-138">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="fcff1-139">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-139">Select **Save**.</span></span>
        4. <span data-ttu-id="fcff1-140">Selecteer **Toevoegen** in de tabel **Tarief**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-140">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="fcff1-141">Voer **21** in het veld **Belastingtarief** in.</span><span class="sxs-lookup"><span data-stu-id="fcff1-141">Enter **21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="fcff1-142">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-142">Select **Save**.</span></span>

        ![BE-RC+21-belastingcode voor terugboekingen](../media/image4.png)

3. <span data-ttu-id="fcff1-144">Definieer de toepasbaarheid van de belastingcodes.</span><span class="sxs-lookup"><span data-stu-id="fcff1-144">Define the applicability of the tax codes.</span></span>

    1. <span data-ttu-id="fcff1-145">Selecteer **Kolommen beheren** en selecteer vervolgens kolommen die moeten worden gebruikt om de toepasbaarheidstabel te maken.</span><span class="sxs-lookup"><span data-stu-id="fcff1-145">Select **Manage columns**, and then select columns that should be used to build the applicability table.</span></span>

        > [!NOTE]
        > <span data-ttu-id="fcff1-146">Zorg ervoor dat u de kolommen **Bedrijfsproces** en **Belastingrichtingen** aan de tabel toevoegt.</span><span class="sxs-lookup"><span data-stu-id="fcff1-146">Be sure to add the **Business process** and **Tax directions** columns to the table.</span></span> <span data-ttu-id="fcff1-147">Beide kolommen zijn essentieel voor de belastingfunctionaliteit in transferorders.</span><span class="sxs-lookup"><span data-stu-id="fcff1-147">Both columns are essential to the functionality for tax in transfer orders.</span></span>

    2. <span data-ttu-id="fcff1-148">Voeg toepasbaarheidsregels toe.</span><span class="sxs-lookup"><span data-stu-id="fcff1-148">Add applicability rules.</span></span> <span data-ttu-id="fcff1-149">Laat de velden **Belastingcodes**, **Belastinggroep** en **Artikelbelastinggroep** niet leeg.</span><span class="sxs-lookup"><span data-stu-id="fcff1-149">Don't leave the **Tax codes**, **Tax group**, and **Item tax group** fields blank.</span></span>
        
        <span data-ttu-id="fcff1-150">Voeg een nieuwe regel toe voor de transferorderzending.</span><span class="sxs-lookup"><span data-stu-id="fcff1-150">Add a new rule for transfer order shipment.</span></span>
        1. <span data-ttu-id="fcff1-151">Selecteer **Toevoegen** in de tabel **Toepasbaarheidsregels**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-151">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="fcff1-152">Selecteer **Voorraad** in het veld **Bedrijfsproces** om de regel van toepassing te maken voor een transferorder.</span><span class="sxs-lookup"><span data-stu-id="fcff1-152">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="fcff1-153">Voer **NLD** in het veld **Land/regio van oorsprong** in.</span><span class="sxs-lookup"><span data-stu-id="fcff1-153">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="fcff1-154">Voer **BEL** in het veld **Land/regio van verzending** in.</span><span class="sxs-lookup"><span data-stu-id="fcff1-154">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="fcff1-155">Selecteer **Uitvoer** in het veld **Belastingrichting** om de regel van toepassing te maken op de verzending van transferorders.</span><span class="sxs-lookup"><span data-stu-id="fcff1-155">In the **Tax direction** field, select **Output** to make the rule applicable to transfer order shipment.</span></span>
        6. <span data-ttu-id="fcff1-156">Selecteer **NL-Vrijgesteld** in het veld **Belastingcodes**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-156">In the **Tax codes** field, select **NL-Exempt**.</span></span>
        7. <span data-ttu-id="fcff1-157">Voer in het velden **Belastinggroep** en **Artikelbelastinggroep** de bijbehorende belastinggroep en artikelbelastinggroep in die zijn gedefinieerd in uw Finance-systeem.</span><span class="sxs-lookup"><span data-stu-id="fcff1-157">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>
        
        <span data-ttu-id="fcff1-158">Voeg nog een regel toe voor de transferorderontvangst.</span><span class="sxs-lookup"><span data-stu-id="fcff1-158">Add another rule for transfer order receipt.</span></span>
        1. <span data-ttu-id="fcff1-159">Selecteer **Toevoegen** in de tabel **Toepasbaarheidsregels**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-159">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="fcff1-160">Selecteer **Voorraad** in het veld **Bedrijfsproces** om de regel van toepassing te maken voor een transferorder.</span><span class="sxs-lookup"><span data-stu-id="fcff1-160">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="fcff1-161">Voer **NLD** in het veld **Land/regio van oorsprong** in.</span><span class="sxs-lookup"><span data-stu-id="fcff1-161">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="fcff1-162">Voer **BEL** in het veld **Land/regio van verzending** in.</span><span class="sxs-lookup"><span data-stu-id="fcff1-162">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="fcff1-163">Selecteer **Invoer** in het veld **Belastingrichting** om de regel van toepassing te maken op de ontvangst van transferorders.</span><span class="sxs-lookup"><span data-stu-id="fcff1-163">In the **Tax direction** field, select **Input** to make the rule applicable to transfer order receipt.</span></span>
        6. <span data-ttu-id="fcff1-164">Selecteer in het veld **Belastingcodes** de opties **BE-RC+21** en **BE-RC-21**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-164">In the **Tax codes** field, select **BE-RC+21** and **BE-RC-21**.</span></span>
        7. <span data-ttu-id="fcff1-165">Voer in het velden **Belastinggroep** en **Artikelbelastinggroep** de bijbehorende belastinggroep en artikelbelastinggroep in die zijn gedefinieerd in uw Finance-systeem.</span><span class="sxs-lookup"><span data-stu-id="fcff1-165">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>

        ![Toepasbaarheidsregels](../media/image5.png)

4. <span data-ttu-id="fcff1-167">Voltooi en publiceer de nieuwe versie van de belastingfunctie.</span><span class="sxs-lookup"><span data-stu-id="fcff1-167">Complete and publish the new tax feature version.</span></span>

    <span data-ttu-id="fcff1-168">[![De status van de nieuwe versie wijzigen](../media/image6.png)](../media/image6.png)</span><span class="sxs-lookup"><span data-stu-id="fcff1-168">[![Changing the status of the new version](../media/image6.png)](../media/image6.png)</span></span>

## <a name="set-up-finance-for-transfer-order-transactions"></a><span data-ttu-id="fcff1-169">Finance instellen voor belasting- en transferordertransacties</span><span class="sxs-lookup"><span data-stu-id="fcff1-169">Set up Finance for transfer order transactions</span></span>

<span data-ttu-id="fcff1-170">Voer de volgende stappen uit om belastingen voor transferorders in te stellen.</span><span class="sxs-lookup"><span data-stu-id="fcff1-170">Follow these steps to enable and set up taxes for transfer orders.</span></span>

1. <span data-ttu-id="fcff1-171">Ga in Finance naar **Werkruimten** \> **Functiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-171">In Finance, go to **Workspaces** \> **Feature management**.</span></span>
2. <span data-ttu-id="fcff1-172">Selecteer de functie **Belasting in transferorder** in de lijst en selecteer **Nu inschakelen** om deze in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="fcff1-172">In the list, find and select the **Tax in transfer order** feature, and then select **Enable now** to turn it on.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="fcff1-173">De functie **Belasting in transferorder** is volledig afhankelijk van de belastingservice.</span><span class="sxs-lookup"><span data-stu-id="fcff1-173">The **Tax in transfer order** feature is fully dependent on the tax service.</span></span> <span data-ttu-id="fcff1-174">Daarom kan deze alleen worden ingeschakeld als u de belastingservice hebt geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="fcff1-174">Therefore, it can be turned on only after you've installed the tax service.</span></span>

    ![De functie Belasting in transferorder](../media/image7.png)

3. <span data-ttu-id="fcff1-176">Schakel de belastingservice in en selecteer het bedrijfsproces **Voorraad**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-176">Enable the tax service, and select the **Inventory** business process.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="fcff1-177">U moet deze stap voltooien voor elke rechtspersoon in Finance waarvoor de belastingservice en de functionaliteit voor belasting in transferorders beschikbaar moeten zijn.</span><span class="sxs-lookup"><span data-stu-id="fcff1-177">You must complete this step for each legal entity in Finance where you want the tax service and the functionality for tax in transfer orders to be available.</span></span>

    1. <span data-ttu-id="fcff1-178">Ga naar **Belasting** \> **Instellingen** \> **Belastingconfiguratie** \> **Instellingen van belastingservice**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-178">Go to **Tax** \> **Setup** \> **Tax configuration** \> **Tax service setup**.</span></span>
    2. <span data-ttu-id="fcff1-179">Selecteer **Voorraad** in het veld **Bedrijfsproces**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-179">In the **Business process** field, select **Inventory**.</span></span>

    ![Het veld Bedrijfsproces instellen](../media/image8.png)

4. <span data-ttu-id="fcff1-181">Controleer of het teruboekingsmechanisme is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="fcff1-181">Verify that the reverse charge mechanism is set up.</span></span> <span data-ttu-id="fcff1-182">Ga naar **Grootboek** \> **Instellingen** \> **Parameters** en controleer vervolgens op het tabblad **Terugboeking** of de optie **Terugboeking inschakelen** is ingesteld op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-182">Go to **General ledger** \> **Setup** \> **Parameters**, and then, on the **Reverse charge** tab, verify that the **Enable reverse charge** option is set to **Yes**.</span></span>

    ![De optie Terugboeking inschakelen](../media/image9.png)

5. <span data-ttu-id="fcff1-184">Controleer of de gerelateerde belastingcodes, belastinggroepen, artikelbelastinggroepen en btw-registratienummers in Finance zijn ingesteld volgens de richtlijnen van de belastingservice.</span><span class="sxs-lookup"><span data-stu-id="fcff1-184">Verify that the related tax codes, tax groups, item tax groups, and VAT registration numbers have been set up in Finance according to the tax service guidance.</span></span>
6. <span data-ttu-id="fcff1-185">Stel een tussentijdse transitrekening in.</span><span class="sxs-lookup"><span data-stu-id="fcff1-185">Set up an interim transit account.</span></span> <span data-ttu-id="fcff1-186">Deze stap is alleen vereist wanneer de belasting die wordt toegepast op een overdrachtsorder niet van toepassing is op een mechanisme voor vrijgestelde belastingen of terugboeking.</span><span class="sxs-lookup"><span data-stu-id="fcff1-186">This step is required only when the tax that is applied to a transfer order isn't applicable to a tax exempted or reverse charge mechanism.</span></span>

    1. <span data-ttu-id="fcff1-187">Ga naar **Belasting** \> **Instellingen** \> **Btw** \> **Grootboekboekingsgroepen**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-187">Go to **Tax** \> **Setup** \> **Sales tax** \> **Ledger posting groups**.</span></span>
    2. <span data-ttu-id="fcff1-188">Selecteer een grootboekrekening in het veld **Tussentijds transit**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-188">In the **Interim transit** field, select a ledger account.</span></span>

    ![Een tussentijdse transitrekening selecteren](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a><span data-ttu-id="fcff1-190">Basisvoorraad instellen voor belasting- en transferordertransacties</span><span class="sxs-lookup"><span data-stu-id="fcff1-190">Set up basic inventory for transfer order transactions</span></span>

<span data-ttu-id="fcff1-191">Volg deze stappen om basisvoorraad in te stellen om transferordertransacties mogelijk te maken.</span><span class="sxs-lookup"><span data-stu-id="fcff1-191">Follow these steps to set up basic inventory to enable transfer order transactions.</span></span>

1. <span data-ttu-id="fcff1-192">Maak verzend- en doellocaties in verschillende landen of regio's voor uw magazijnen en voeg het primaire adres voor elke locatie toe.</span><span class="sxs-lookup"><span data-stu-id="fcff1-192">Create ship-from and ship-to sites for your warehouses in different countries or regions, and add the primary address for each site.</span></span>

    1. <span data-ttu-id="fcff1-193">Ga naar **Magazijnbeheer** \> **Instellingen** \> **Magazijn** \> **Vestigingen**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-193">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Sites**.</span></span>
    2. <span data-ttu-id="fcff1-194">Selecteer **Nieuw** om de vestiging te maken die u later aan een magazijn toewijst.</span><span class="sxs-lookup"><span data-stu-id="fcff1-194">Select **New** to create the site that you will assign to a warehouse later.</span></span>
    3. <span data-ttu-id="fcff1-195">Herhaal stap 2 voor alle andere vestigingen die u moet maken.</span><span class="sxs-lookup"><span data-stu-id="fcff1-195">Repeat step 2 for all the other sites that you must create.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fcff1-196">Een van de vestigingen die u maakt, moet **Transit** heten.</span><span class="sxs-lookup"><span data-stu-id="fcff1-196">One of the sites that you create should be named **Transit**.</span></span> <span data-ttu-id="fcff1-197">In latere stappen van deze procedure wijst u deze vestiging toe aan het transitmagazijn, zodat btw-gerelateerde voorraadboekstukken kunnen worden geboekt in verzend- en ontvangsttransacties voor transferorders.</span><span class="sxs-lookup"><span data-stu-id="fcff1-197">In later steps of this procedure, you will assign this site to the transit warehouse, so that tax-related inventory vouchers can be posted in "ship" and "receive" transactions for transfer orders.</span></span> <span data-ttu-id="fcff1-198">Het adres van de transitvestiging is niet relevant voor belastingberekening.</span><span class="sxs-lookup"><span data-stu-id="fcff1-198">The address of the transit site is irrelevant to tax calculation.</span></span> <span data-ttu-id="fcff1-199">U kunt dit veld daarom leeg laten.</span><span class="sxs-lookup"><span data-stu-id="fcff1-199">Therefore, you can leave it blank.</span></span>

    ![Vestigingen instellen](../media/image11.png)

2. <span data-ttu-id="fcff1-201">Maak verzend-, transit- en doelmagazijnen.</span><span class="sxs-lookup"><span data-stu-id="fcff1-201">Create ship-from, transit, and ship-to warehouses.</span></span> <span data-ttu-id="fcff1-202">Alle adresgegevens die in een magazijn worden bijgehouden, overschrijven het vestigingsadres tijdens de belastingberekening.</span><span class="sxs-lookup"><span data-stu-id="fcff1-202">Any address information that is maintained in a warehouse will override the site address during tax calculation.</span></span>

    1. <span data-ttu-id="fcff1-203">Ga naar **Magazijnbeheer** \> **Instellen** \> **Magazijn** \> **Magazijnen**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-203">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Warehouses**.</span></span>
    2. <span data-ttu-id="fcff1-204">Selecteer **Nieuw** om een magazijn te maken en deze aan de bijbehorende vestiging toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="fcff1-204">Select **New** to create a warehouse, and assign it to the corresponding site.</span></span>
    3. <span data-ttu-id="fcff1-205">Herhaal stap 2 om naar behoefte een magazijn voor elke vestiging te maken.</span><span class="sxs-lookup"><span data-stu-id="fcff1-205">Repeat step 2 to create a warehouse for each site as required.</span></span>

    ![Magazijnen instellen](../media/image12.png)

    > [!NOTE]
    > <span data-ttu-id="fcff1-207">Voor een verzendmagazijn moet een transitmagazijn worden geselecteerd in het veld **Transitmagazijn** voor transferordertransacties.</span><span class="sxs-lookup"><span data-stu-id="fcff1-207">For a ship-from warehouse, a transit warehouse must be selected in the **Transit warehouse** field for transfer order transactions.</span></span>
    >
    > ![Een transitmagazijn selecteren](../media/image13.png)

3. <span data-ttu-id="fcff1-209">Verifieer of de voorraadboekingsconfiguratie is ingesteld voor transferordertransacties.</span><span class="sxs-lookup"><span data-stu-id="fcff1-209">Verify that the inventory posting configuration is set up for transfer order transactions.</span></span>

    1. <span data-ttu-id="fcff1-210">Ga naar **Voorraadbeheer** \> **Instellen** \> **Boeken** \> **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-210">Go to **Inventory management** \> **Setup** \> **Posting** \> **Posting**.</span></span>
    2. <span data-ttu-id="fcff1-211">Controleer op het tabblad **Voorraad** of er een grootboekrekening is ingesteld voor de boekingen **Voorraaduitgifte** en **Voorraadontvangst**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-211">On the **Inventory** tab, verify that a ledger account is set up for both **Inventory issue** and **Inventory receipt** posting.</span></span>

        ![De boeking van voorraaduitgifte en voorraadontvangst instellen](../media/image14.png)

    3. <span data-ttu-id="fcff1-213">Controleer of er een grootboekrekening is ingesteld voor de boeking **Inter-unit te betalen**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-213">Verify that a ledger account is set up for **Inter-unit payable** posting.</span></span>

        ![De boeking Inter-unit te betalen instellen](../media/image15.png)

    4. <span data-ttu-id="fcff1-215">Controleer of er een grootboekrekening is ingesteld voor de boeking **Inter-unit te ontvangen**.</span><span class="sxs-lookup"><span data-stu-id="fcff1-215">Verify that a ledger account is set up for **Inter-unit receivable** posting.</span></span>

        ![De boeking Inter-unit te ontvangen instellen](../media/image16.png)
