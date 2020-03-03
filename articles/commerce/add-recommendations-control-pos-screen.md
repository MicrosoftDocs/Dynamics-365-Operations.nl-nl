---
title: Een besturingselement voor aanbevelingen toevoegen aan het transactiescherm op POS-apparaten
description: In dit onderwerp wordt beschreven hoe u een besturingselement voor aanbevelingen kunt toevoegen aan het transactiescherm op een POS-apparaat (Point of Sale) met behulp van de schermindelingsontwerper in Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
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
ms.openlocfilehash: 6d6f48197a36f633e3cd63cbad4518f53946fc7f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022083"
---
# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a><span data-ttu-id="250b4-103">Een besturingselement voor aanbevelingen toevoegen aan het transactiescherm op POS-apparaten</span><span class="sxs-lookup"><span data-stu-id="250b4-103">Add a recommendations control to the transaction screen on POS devices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="250b4-104">In dit onderwerp wordt beschreven hoe u een besturingselement voor aanbevelingen kunt toevoegen aan het transactiescherm op een POS-apparaat (Point of Sale) met behulp van de schermindelingsontwerper in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="250b4-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="250b4-105">Meer informatie over productaanbevelingen vindt u in de [documenten met productaanbevelingen voor POS](product.md).</span><span class="sxs-lookup"><span data-stu-id="250b4-105">For more information about product recommendations, read the  [product recommendations on POS documentation](product.md).</span></span>


<span data-ttu-id="250b4-106">U kunt productaanbevelingen op uw POS-apparaat weergeven wanneer u Commerce gebruikt.</span><span class="sxs-lookup"><span data-stu-id="250b4-106">You can display product recommendations on your POS device when you use Commerce.</span></span> <span data-ttu-id="250b4-107">Als u productaanbevelingen wilt weergeven, moet u een besturingselement toevoegen aan het transactiescherm met de schermindelingsontwerper.</span><span class="sxs-lookup"><span data-stu-id="250b4-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span> 

## <a name="open-layout-designer"></a><span data-ttu-id="250b4-108">Indelingsontwerper openen</span><span class="sxs-lookup"><span data-stu-id="250b4-108">Open Layout designer</span></span>

1. <span data-ttu-id="250b4-109">Ga naar **Retail en Commerce** &gt; **Afzetkanaalinstellingen** &gt; **POS-instellingen** &gt; **POS** &gt; **Schermindelingen**.</span><span class="sxs-lookup"><span data-stu-id="250b4-109">Go to **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="250b4-110">Met het snelfilter kunt u zoeken naar het scherm waaraan u het besturingselement wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="250b4-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="250b4-111">Filter bijvoorbeeld op het veld **Schermindelings-id** met de waarde **F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="250b4-111">For example, filter on the **Screen layout ID** field using a value of **F2CP16:9M**.</span></span>
3. <span data-ttu-id="250b4-112">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="250b4-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="250b4-113">Selecteer bijvoorbeeld **Naam: F2CP16:9M Schermindelings-ID: F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="250b4-113">For example, select **Name: F2CP16:9M Screen Layout ID: F2CP16:9M**.</span></span>
4. <span data-ttu-id="250b4-114">Klik op **Ontwerper van indeling**.</span><span class="sxs-lookup"><span data-stu-id="250b4-114">Click **Layout designer**.</span></span>
5. <span data-ttu-id="250b4-115">Volg de aanwijzingen voor het starten van de indelingsontwerper.</span><span class="sxs-lookup"><span data-stu-id="250b4-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="250b4-116">Wanneer naar referenties wordt gevraagd, voert u de referenties in die zijn gebruikt bij het starten van de indelingsontwerper op de pagina **Schermindelingen**.</span><span class="sxs-lookup"><span data-stu-id="250b4-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="250b4-117">Wanneer u zich aanmeldt, wordt er een pagina weergegeven die vergelijkbaar is met de onderstaande pagina.</span><span class="sxs-lookup"><span data-stu-id="250b4-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="250b4-118">De indeling zal afwijken, afhankelijk van de aanpassingen die voor uw winkel zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="250b4-118">The layout will be different depending on the customizations that were made for your store.</span></span>


    <span data-ttu-id="250b4-119">[![Ontwerper van indeling](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="250b4-119">[![Layout designer](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="250b4-120">Een weergaveoptie kiezen</span><span class="sxs-lookup"><span data-stu-id="250b4-120">Choose a display option</span></span>

<span data-ttu-id="250b4-121">Er zijn twee configuratieopties beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="250b4-121">There are two configurations options available.</span></span> <span data-ttu-id="250b4-122">Kies de optie die het meest geschikt is voor uw winkel en volg de rest van de instructies om de instelling van het besturingselement te voltooien.</span><span class="sxs-lookup"><span data-stu-id="250b4-122">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="250b4-123">De twee opties zijn:</span><span class="sxs-lookup"><span data-stu-id="250b4-123">The two options are:</span></span>

- <span data-ttu-id="250b4-124">Aanbevelingen zijn altijd zichtbaar.</span><span class="sxs-lookup"><span data-stu-id="250b4-124">Recommendations are always visible.</span></span>
- <span data-ttu-id="250b4-125">Het tabblad **Aanbevelingen** wordt weergegeven in het raster aan de rechterkant van het scherm.</span><span class="sxs-lookup"><span data-stu-id="250b4-125">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="250b4-126">Aanbevelingen altijd zichtbaar maken</span><span class="sxs-lookup"><span data-stu-id="250b4-126">Make recommendations always visible</span></span>


1. <span data-ttu-id="250b4-127">Verklein de hoogte van het detailgebied van de transactieregels zodat het even hoog is als het deelvenster van de klant aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="250b4-127">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>


    <span data-ttu-id="250b4-128">[![Hoogte van het detailgebied van de transactieregels verlaagd](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="250b4-128">[![Height of the transaction lines details area reduced](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="250b4-129">Sleep in het menu aan de linkerkant het besturingselement voor aanbevelingen en zet het neer tussen het detailgebied van de transactieregels en het knoppenraster onderaan in het midden van het transactiescherm.</span><span class="sxs-lookup"><span data-stu-id="250b4-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="250b4-130">Pas de grootte van het besturingselement aan zodat het in die ruimte past.</span><span class="sxs-lookup"><span data-stu-id="250b4-130">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="250b4-131">[![Het besturings Aanbevelingen is toegevoegd aan de indeling](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="250b4-131">[![Recommendations control added to the layout](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>


3. <span data-ttu-id="250b4-132">Klik op **OK** om de indelingsontwerper op te slaan en af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="250b4-132">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="250b4-133">Ga in Commerce naar **Retail en Commerce** &gt; **Retail en Commerce IT** &gt; **Distributieplanningen**.</span><span class="sxs-lookup"><span data-stu-id="250b4-133">In Commerce, go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="250b4-134">Selecteer **1090, kassa´s** in de lijst.</span><span class="sxs-lookup"><span data-stu-id="250b4-134">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="250b4-135">Klik op **Nu uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="250b4-135">Click **Run now**.</span></span>


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="250b4-136">Het tabblad Aanbevelingen toevoegen aan het knoppenraster aan de rechterkant van het scherm</span><span class="sxs-lookup"><span data-stu-id="250b4-136">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="250b4-137">Klik met de rechtermuisknop op de lege ruimte onder het laatste tabblad van het knoppenraster dat zich aan de rechterkant van de pagina bevindt.</span><span class="sxs-lookup"><span data-stu-id="250b4-137">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>

2. <span data-ttu-id="250b4-138">Klik op **Aanpassen**.</span><span class="sxs-lookup"><span data-stu-id="250b4-138">Click **Customize**.</span></span>

    <span data-ttu-id="250b4-139">[![Het dialoogvenster Aanpassing - Tabblad](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="250b4-139">[![Customization - Tab control dialog box](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="250b4-140">Klik op **Nieuw tabblad**.</span><span class="sxs-lookup"><span data-stu-id="250b4-140">Click **New tab**.</span></span>
4. <span data-ttu-id="250b4-141">Zoek naar het nieuwe tabblad dat u zojuist hebt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="250b4-141">Find the new tab that you just added.</span></span> <span data-ttu-id="250b4-142">Wellicht moet u omlaag bladeren.</span><span class="sxs-lookup"><span data-stu-id="250b4-142">You may need to scroll down.</span></span>
5. <span data-ttu-id="250b4-143">Selecteer in de vervolgkeuzelijst **Inhoud** **Aanbevolen producten**.</span><span class="sxs-lookup"><span data-stu-id="250b4-143">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="250b4-144">[![Aanbevolen producten in het veld Inhoud](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="250b4-144">[![Selecting Recommended products in the Contents field](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="250b4-145">Typ in het veld **Label** een naam voor het tabblad Aanbevelingen. Typ bijvoorbeeld Aanbevolen producten.</span><span class="sxs-lookup"><span data-stu-id="250b4-145">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="250b4-146">Selecteer in het veld **Afbeelding** de afbeelding die op het tabblad moet worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="250b4-146">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="250b4-147">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="250b4-147">Click **OK**.</span></span> <span data-ttu-id="250b4-148">Het nieuwe tabblad wordt weergegeven in het knoppenraster.</span><span class="sxs-lookup"><span data-stu-id="250b4-148">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="250b4-149">Klik op **OK** om de indelingsontwerper op te slaan en af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="250b4-149">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="250b4-150">Ga in Commerce naar **Retail en Commerce** &gt; **Retail en Commerce IT** &gt; **Distributieplanningen**.</span><span class="sxs-lookup"><span data-stu-id="250b4-150">In Commerce, go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="250b4-151">Selecteer **1090, kassa´s** in de lijst.</span><span class="sxs-lookup"><span data-stu-id="250b4-151">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="250b4-152">Klik op **Nu uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="250b4-152">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="250b4-153">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="250b4-153">Additional resources</span></span>

[<span data-ttu-id="250b4-154">Productaanbevelingen op POS</span><span class="sxs-lookup"><span data-stu-id="250b4-154">Product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="250b4-155">Overzicht productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="250b4-155">Product recommendations overview</span></span>](../commerce/product-recommendations.md)