---
title: Een besturingselement voor aanbevelingen toevoegen aan de transactiepagina op een POS-apparaat
description: In dit onderwerp wordt beschreven hoe u een besturingselement voor aanbevelingen kunt toevoegen aan het transactiescherm op een POS-apparaat (Point of Sale) met behulp van de schermindelingsontwerper in Microsoft Dynamics 365 for Retail.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: 86dce19011b98dace5c5df72280180e0b1c8bbaa
ms.contentlocale: nl-nl
ms.lasthandoff: 01/17/2018

---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a><span data-ttu-id="eda53-103">Een besturingselement voor aanbevelingen toevoegen aan de transactiepagina op een POS-apparaat</span><span class="sxs-lookup"><span data-stu-id="eda53-103">Add a recommendations control to the transaction page on a POS device</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="eda53-104">In dit onderwerp wordt beschreven hoe u een besturingselement voor aanbevelingen kunt toevoegen aan het transactiescherm op een POS-apparaat (Point of Sale) met behulp van de schermindelingsontwerper in Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="eda53-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="eda53-105">Wanneer u Microsoft Dynamics 365 for Retail gebruikt, kunt u productaanbevelingen weergeven op uw POS-apparaat.</span><span class="sxs-lookup"><span data-stu-id="eda53-105">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="eda53-106">*Aanbevelingen* zijn items waarin uw klanten mogelijk geïnteresseerd zijn op basis van hun inkoophistorie, items in hun verlanglijst en items die andere klanten online en in fysieke winkels hebben gekocht.</span><span class="sxs-lookup"><span data-stu-id="eda53-106">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="eda53-107">Als u productaanbevelingen wilt weergeven, moet u een besturingselement toevoegen aan het transactiescherm met de schermindelingsontwerper.</span><span class="sxs-lookup"><span data-stu-id="eda53-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="eda53-108">Indelingsontwerper openen</span><span class="sxs-lookup"><span data-stu-id="eda53-108">Open Layout designer</span></span>
1.  <span data-ttu-id="eda53-109">Ga naar **Detailhandel** &gt; **Kanaalinstellingen** &gt; **POS-instellingen** &gt; **POS** &gt; **Schermindelingen**.</span><span class="sxs-lookup"><span data-stu-id="eda53-109">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2.  <span data-ttu-id="eda53-110">Met het snelfilter kunt u zoeken naar het scherm waaraan u het besturingselement wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="eda53-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="eda53-111">Filter bijvoorbeeld op het veld **Schermindelings-ID** met de waarde 'F2CP16:9M'.</span><span class="sxs-lookup"><span data-stu-id="eda53-111">For example, filter on the **Screen layout ID** field using a value of ‘F2CP16:9M’.</span></span>
3.  <span data-ttu-id="eda53-112">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="eda53-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="eda53-113">Selecteer bijvoorbeeld 'Naam: F2CP16:9M Schermindelings-ID: F2CP16:9M'.</span><span class="sxs-lookup"><span data-stu-id="eda53-113">For example, select ‘Name: F2CP16:9M Screen Layout ID: F2CP16:9M’.</span></span>
4.  <span data-ttu-id="eda53-114">Klik op **Ontwerper van indeling**.</span><span class="sxs-lookup"><span data-stu-id="eda53-114">Click **Layout designer**.</span></span>
5.  <span data-ttu-id="eda53-115">Volg de aanwijzingen voor het starten van de indelingsontwerper.</span><span class="sxs-lookup"><span data-stu-id="eda53-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="eda53-116">Wanneer naar referenties wordt gevraagd, voert u de referenties in die zijn gebruikt bij het starten van de indelingsontwerper op de pagina **Schermindelingen**.</span><span class="sxs-lookup"><span data-stu-id="eda53-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6.  <span data-ttu-id="eda53-117">Wanneer u zich aanmeldt, wordt er een pagina weergegeven die vergelijkbaar is met de onderstaande pagina.</span><span class="sxs-lookup"><span data-stu-id="eda53-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="eda53-118">De indeling zal afwijken, afhankelijk van de aanpassingen die voor uw winkel zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="eda53-118">The layout will be different depending on the customizations that were made for your store.</span></span>

<span data-ttu-id="eda53-119">[![schermindelingsafbeelding-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Een weergaveoptie kiezen</span><span class="sxs-lookup"><span data-stu-id="eda53-119">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Choose a display option</span></span>
-----------------------

<span data-ttu-id="eda53-120">Er zijn twee configuratieopties beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="eda53-120">There are two configurations options available.</span></span> <span data-ttu-id="eda53-121">Kies de optie die het meest geschikt is voor uw winkel en volg de rest van de instructies om de instelling van het besturingselement te voltooien.</span><span class="sxs-lookup"><span data-stu-id="eda53-121">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="eda53-122">De twee opties zijn:</span><span class="sxs-lookup"><span data-stu-id="eda53-122">The two options are:</span></span>
-   <span data-ttu-id="eda53-123">Aanbevelingen zijn altijd zichtbaar.</span><span class="sxs-lookup"><span data-stu-id="eda53-123">Recommendations are always visible.</span></span>
-   <span data-ttu-id="eda53-124">Het tabblad **Aanbevelingen** wordt weergegeven in het raster aan de rechterkant van het scherm.</span><span class="sxs-lookup"><span data-stu-id="eda53-124">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

#### <a name="to-make-recommendations-always-visible"></a><span data-ttu-id="eda53-125">Aanbevelingen altijd zichtbaar maken</span><span class="sxs-lookup"><span data-stu-id="eda53-125">To make recommendations always visible</span></span>

1.  <span data-ttu-id="eda53-126">Verklein de hoogte van het detailgebied van de transactieregels zodat het even hoog is als het deelvenster van de klant aan de linkerkant.[](./media/pic-2.png)[![schermindelingsafbeelding-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="eda53-126">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>
2.  <span data-ttu-id="eda53-127">Sleep in het menu aan de linkerkant het besturingselement voor aanbevelingen en zet het neer tussen het detailgebied van de transactieregels en het knoppenraster onderaan in het midden van het transactiescherm.</span><span class="sxs-lookup"><span data-stu-id="eda53-127">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="eda53-128">Pas de grootte van het besturingselement aan zodat het in die ruimte past.[](./media/pic-3.png)[![schermindelingsafbeelding-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="eda53-128">Resize the control so it fits in that space.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>
3.  <span data-ttu-id="eda53-129">Klik op **OK** om de indelingsontwerper op te slaan en af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="eda53-129">Click the **X** to save and exit Layout designer.</span></span>
4.  <span data-ttu-id="eda53-130">Ga in Dynamics 365 for Retail naar **Detailhandel** &gt; **IT detailhandel** &gt; **Distributieplanningen**.</span><span class="sxs-lookup"><span data-stu-id="eda53-130">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5.  <span data-ttu-id="eda53-131">Selecteer **1090, kassa´s** in de lijst.</span><span class="sxs-lookup"><span data-stu-id="eda53-131">In the list, select **1090 Registers**.</span></span>
6.  <span data-ttu-id="eda53-132">Klik op **Nu uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="eda53-132">Click **Run now**.</span></span>

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="eda53-133">Het tabblad Aanbevelingen toevoegen aan het knoppenraster aan de rechterkant van het scherm</span><span class="sxs-lookup"><span data-stu-id="eda53-133">To add a Recommendations tab to the button grid on the right side of the screen</span></span>

1.  <span data-ttu-id="eda53-134">Klik met de rechtermuisknop op de lege ruimte onder het laatste tabblad van het knoppenraster dat zich aan de rechterkant van de pagina bevindt.</span><span class="sxs-lookup"><span data-stu-id="eda53-134">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2.  <span data-ttu-id="eda53-135">Klik op **Aanpassen**.[![afbeelding-5](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="eda53-135">Click **Customize**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span></span>
3.  <span data-ttu-id="eda53-136">Klik op **Nieuw tabblad**.</span><span class="sxs-lookup"><span data-stu-id="eda53-136">Click **New tab**.</span></span>
4.  <span data-ttu-id="eda53-137">Zoek naar het nieuwe tabblad dat u zojuist hebt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="eda53-137">Find the new tab that you just added.</span></span> <span data-ttu-id="eda53-138">Wellicht moet u omlaag bladeren.</span><span class="sxs-lookup"><span data-stu-id="eda53-138">You may need to scroll down.</span></span>
5.  <span data-ttu-id="eda53-139">Selecteer in de vervolgkeuzelijst **Inhoud** **Aanbevolen producten**.</span><span class="sxs-lookup"><span data-stu-id="eda53-139">In the **Contents** drop-down, select **Recommended products**.</span></span> <span data-ttu-id="eda53-140">[![afbeelding-6](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="eda53-140">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span></span>
6.  <span data-ttu-id="eda53-141">Typ in het veld **Label** een naam voor het tabblad Aanbevelingen. Typ bijvoorbeeld ´Aanbevolen producten´.</span><span class="sxs-lookup"><span data-stu-id="eda53-141">In the **Label** field, type a name for the recommendations tab. For example, type ‘Recommended products’.</span></span>
7.  <span data-ttu-id="eda53-142">Selecteer in het veld **Afbeelding** de afbeelding die op het tabblad moet worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="eda53-142">In the **Image** field, select the image to appear on the tab.</span></span>
8.  <span data-ttu-id="eda53-143">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="eda53-143">Click **OK**.</span></span> <span data-ttu-id="eda53-144">Het nieuwe tabblad wordt weergegeven in het knoppenraster.</span><span class="sxs-lookup"><span data-stu-id="eda53-144">The new tab appears in the button grid.</span></span>
9.  <span data-ttu-id="eda53-145">Klik op **OK** om de indelingsontwerper op te slaan en af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="eda53-145">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="eda53-146">Ga in Dynamics 365 for Retail naar **Detailhandel** &gt; **IT detailhandel** &gt; **Distributieplanningen**.</span><span class="sxs-lookup"><span data-stu-id="eda53-146">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="eda53-147">Selecteer **1090, kassa´s** in de lijst.</span><span class="sxs-lookup"><span data-stu-id="eda53-147">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="eda53-148">Klik op **Nu uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="eda53-148">Click **Run now**.</span></span>


<a name="see-also"></a><span data-ttu-id="eda53-149">Zie ook</span><span class="sxs-lookup"><span data-stu-id="eda53-149">See also</span></span>
--------

[<span data-ttu-id="eda53-150">Overzicht persoonlijke productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="eda53-150">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)




