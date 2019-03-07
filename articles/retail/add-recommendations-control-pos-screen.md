---
title: Een besturingselement voor aanbevelingen toevoegen aan het transactiescherm op POS-apparaten
description: In dit onderwerp wordt beschreven hoe u een besturingselement voor aanbevelingen kunt toevoegen aan het transactiescherm op een POS-apparaat (Point of Sale) met behulp van de schermindelingsontwerper in Microsoft Dynamics 365 for Retail.
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 213b47422a5e31c2cfc2d173b8c7d9efdecc7568
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "320438"
---
# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a><span data-ttu-id="fa483-103">Een besturingselement voor aanbevelingen toevoegen aan het transactiescherm op POS-apparaten</span><span class="sxs-lookup"><span data-stu-id="fa483-103">Add a recommendations control to the transaction screen on POS devices</span></span>

[!include [banner](includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="fa483-104">We verwijderen de huidige versie van de productaanbevelingsservice aangezien we deze opnieuw willen ontwerpen met een beter algoritme en nieuwe mogelijkheden voor detailhandelaren.</span><span class="sxs-lookup"><span data-stu-id="fa483-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="fa483-105">Zie voor meer informatie [Verwijderde of verouderde functies](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span><span class="sxs-lookup"><span data-stu-id="fa483-105">For more information see [Removed or deprecated features](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span></span>

<span data-ttu-id="fa483-106">In dit onderwerp wordt beschreven hoe u een besturingselement voor aanbevelingen kunt toevoegen aan het transactiescherm op een POS-apparaat (Point of Sale) met behulp van de schermindelingsontwerper in Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="fa483-106">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="fa483-107">Wanneer u Microsoft Dynamics 365 for Retail gebruikt, kunt u productaanbevelingen weergeven op uw POS-apparaat.</span><span class="sxs-lookup"><span data-stu-id="fa483-107">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="fa483-108">*Aanbevelingen* zijn items waarin uw klanten mogelijk geïnteresseerd zijn op basis van hun inkoophistorie, items in hun verlanglijst en items die andere klanten online en in fysieke winkels hebben gekocht.</span><span class="sxs-lookup"><span data-stu-id="fa483-108">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="fa483-109">Als u productaanbevelingen wilt weergeven, moet u een besturingselement toevoegen aan het transactiescherm met de schermindelingsontwerper.</span><span class="sxs-lookup"><span data-stu-id="fa483-109">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="fa483-110">Indelingsontwerper openen</span><span class="sxs-lookup"><span data-stu-id="fa483-110">Open Layout designer</span></span>

1. <span data-ttu-id="fa483-111">Ga naar **Detailhandel** &gt; **Kanaalinstellingen** &gt; **POS-instellingen** &gt; **POS** &gt; **Schermindelingen**.</span><span class="sxs-lookup"><span data-stu-id="fa483-111">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="fa483-112">Met het snelfilter kunt u zoeken naar het scherm waaraan u het besturingselement wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="fa483-112">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="fa483-113">Filter bijvoorbeeld op het veld **Schermindelings-id** met de waarde 'F2CP16:9M'.</span><span class="sxs-lookup"><span data-stu-id="fa483-113">For example, filter on the **Screen layout ID** field using a value of 'F2CP16:9M'.</span></span>
3. <span data-ttu-id="fa483-114">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="fa483-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="fa483-115">Selecteer bijvoorbeeld 'Naam: F2CP16:9M Schermindelings-ID: F2CP16:9M'.</span><span class="sxs-lookup"><span data-stu-id="fa483-115">For example, select 'Name: F2CP16:9M Screen Layout ID: F2CP16:9M'.</span></span>
4. <span data-ttu-id="fa483-116">Klik op **Ontwerper van indeling**.</span><span class="sxs-lookup"><span data-stu-id="fa483-116">Click **Layout designer**.</span></span>
5. <span data-ttu-id="fa483-117">Volg de aanwijzingen voor het starten van de indelingsontwerper.</span><span class="sxs-lookup"><span data-stu-id="fa483-117">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="fa483-118">Wanneer naar referenties wordt gevraagd, voert u de referenties in die zijn gebruikt bij het starten van de indelingsontwerper op de pagina **Schermindelingen**.</span><span class="sxs-lookup"><span data-stu-id="fa483-118">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="fa483-119">Wanneer u zich aanmeldt, wordt er een pagina weergegeven die vergelijkbaar is met de onderstaande pagina.</span><span class="sxs-lookup"><span data-stu-id="fa483-119">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="fa483-120">De indeling zal afwijken, afhankelijk van de aanpassingen die voor uw winkel zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="fa483-120">The layout will be different depending on the customizations that were made for your store.</span></span>

    <span data-ttu-id="fa483-121">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="fa483-121">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="fa483-122">Een weergaveoptie kiezen</span><span class="sxs-lookup"><span data-stu-id="fa483-122">Choose a display option</span></span>

<span data-ttu-id="fa483-123">Er zijn twee configuratieopties beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="fa483-123">There are two configurations options available.</span></span> <span data-ttu-id="fa483-124">Kies de optie die het meest geschikt is voor uw winkel en volg de rest van de instructies om de instelling van het besturingselement te voltooien.</span><span class="sxs-lookup"><span data-stu-id="fa483-124">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="fa483-125">De twee opties zijn:</span><span class="sxs-lookup"><span data-stu-id="fa483-125">The two options are:</span></span>

- <span data-ttu-id="fa483-126">Aanbevelingen zijn altijd zichtbaar.</span><span class="sxs-lookup"><span data-stu-id="fa483-126">Recommendations are always visible.</span></span>
- <span data-ttu-id="fa483-127">Het tabblad **Aanbevelingen** wordt weergegeven in het raster aan de rechterkant van het scherm.</span><span class="sxs-lookup"><span data-stu-id="fa483-127">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="fa483-128">Aanbevelingen altijd zichtbaar maken</span><span class="sxs-lookup"><span data-stu-id="fa483-128">Make recommendations always visible</span></span>

1. <span data-ttu-id="fa483-129">Verklein de hoogte van het detailgebied van de transactieregels zodat het even hoog is als het deelvenster van de klant aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="fa483-129">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>

    <span data-ttu-id="fa483-130">[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="fa483-130">[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="fa483-131">Sleep in het menu aan de linkerkant het besturingselement voor aanbevelingen en zet het neer tussen het detailgebied van de transactieregels en het knoppenraster onderaan in het midden van het transactiescherm.</span><span class="sxs-lookup"><span data-stu-id="fa483-131">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="fa483-132">Pas de grootte van het besturingselement aan zodat het in die ruimte past.</span><span class="sxs-lookup"><span data-stu-id="fa483-132">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="fa483-133">[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="fa483-133">[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>

3. <span data-ttu-id="fa483-134">Klik op **OK** om de indelingsontwerper op te slaan en af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="fa483-134">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="fa483-135">Klik in Dynamics 365 for Retail op **Retail** &gt; **IT detailhandel** &gt; **Distributieplanningen**.</span><span class="sxs-lookup"><span data-stu-id="fa483-135">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="fa483-136">Selecteer  **1090, kassa´s** in de lijst.</span><span class="sxs-lookup"><span data-stu-id="fa483-136">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="fa483-137">Klik op **Nu uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="fa483-137">Click **Run now**.</span></span>

### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="fa483-138">Het tabblad Aanbevelingen toevoegen aan het knoppenraster aan de rechterkant van het scherm</span><span class="sxs-lookup"><span data-stu-id="fa483-138">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="fa483-139">Klik met de rechtermuisknop op de lege ruimte onder het laatste tabblad van het knoppenraster dat zich aan de rechterkant van de pagina bevindt.</span><span class="sxs-lookup"><span data-stu-id="fa483-139">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2. <span data-ttu-id="fa483-140">Klik op **Aanpassen**.</span><span class="sxs-lookup"><span data-stu-id="fa483-140">Click **Customize**.</span></span>

    <span data-ttu-id="fa483-141">[![afbeelding-5](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="fa483-141">[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="fa483-142">Klik op **Nieuw tabblad**.</span><span class="sxs-lookup"><span data-stu-id="fa483-142">Click **New tab**.</span></span>
4. <span data-ttu-id="fa483-143">Zoek naar het nieuwe tabblad dat u zojuist hebt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="fa483-143">Find the new tab that you just added.</span></span> <span data-ttu-id="fa483-144">Wellicht moet u omlaag bladeren.</span><span class="sxs-lookup"><span data-stu-id="fa483-144">You may need to scroll down.</span></span>
5. <span data-ttu-id="fa483-145">Selecteer in de vervolgkeuzelijst **Inhoud** **Aanbevolen producten**.</span><span class="sxs-lookup"><span data-stu-id="fa483-145">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="fa483-146">[![afbeelding-6](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="fa483-146">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="fa483-147">Typ in het veld **Label** een naam voor het tabblad Aanbevelingen. Typ bijvoorbeeld Aanbevolen producten.</span><span class="sxs-lookup"><span data-stu-id="fa483-147">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="fa483-148">Selecteer in het veld **Afbeelding** de afbeelding die op het tabblad moet worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="fa483-148">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="fa483-149">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="fa483-149">Click **OK**.</span></span> <span data-ttu-id="fa483-150">Het nieuwe tabblad wordt weergegeven in het knoppenraster.</span><span class="sxs-lookup"><span data-stu-id="fa483-150">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="fa483-151">Klik op **OK** om de indelingsontwerper op te slaan en af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="fa483-151">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="fa483-152">Klik in Dynamics 365 for Retail op **Retail** &gt; **IT detailhandel** &gt; **Distributieplanningen**.</span><span class="sxs-lookup"><span data-stu-id="fa483-152">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="fa483-153">Selecteer **1090, kassa's** in de lijst.</span><span class="sxs-lookup"><span data-stu-id="fa483-153">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="fa483-154">Klik op **Nu uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="fa483-154">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fa483-155">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="fa483-155">Additional resources</span></span>

[<span data-ttu-id="fa483-156">Overzicht van gepersonaliseerde productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="fa483-156">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)
