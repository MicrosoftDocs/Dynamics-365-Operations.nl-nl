---
title: Productaanbevelingen op POS
description: Dit onderwerp beschrijft het gebruik van productaanbevelingen op een POS-apparaat (Point of Sale).
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: bfb13904b774558907b29e74158b1e0a193e17cd
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057436"
---
# <a name="product-recommendations-on-pos"></a><span data-ttu-id="4a2a9-103">Productaanbevelingen op POS</span><span class="sxs-lookup"><span data-stu-id="4a2a9-103">Product recommendations on POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4a2a9-104">In feite zijn productaanbevelingen een transformatieve zakelijke toepassing voor alle gebieden van commerce, voor het creëren van uitgebreide, prettige en op maat gemaakte productkennismakingservaringen.</span><span class="sxs-lookup"><span data-stu-id="4a2a9-104">At its core, product recommendations are a transformative business application that span across all commerce spaces to create rich, engaging, and tailored product discovery experiences.</span></span> <span data-ttu-id="4a2a9-105">Als u deze functie op POS wilt implementeren, volgt u de stappen voor het [toevoegen van aanbevelingen aan uw POS-apparaten.](add-recommendations-control-pos-screen.md)</span><span class="sxs-lookup"><span data-stu-id="4a2a9-105">To implement this feature on POS, follow the steps on [how to add recommendations to your POS devices.](add-recommendations-control-pos-screen.md)</span></span> 

<span data-ttu-id="4a2a9-106">Meer informatie over de functies voor productaanbevelingen vindt u in het [overzicht van productaanbevelingen.](../commerce/product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="4a2a9-106">For more information about product recommendations features, read the [product recommendations overview.](../commerce/product-recommendations.md)</span></span> 

## <a name="scenarios"></a><span data-ttu-id="4a2a9-107">Scenario's</span><span class="sxs-lookup"><span data-stu-id="4a2a9-107">Scenarios</span></span>

<span data-ttu-id="4a2a9-108">Productaanbevelingen zijn ingeschakeld voor de volgende POS-scenario's.</span><span class="sxs-lookup"><span data-stu-id="4a2a9-108">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="4a2a9-109">Ze zijn beschikbaar in de cloud-POS of Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="4a2a9-109">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="4a2a9-110">Op de pagina **Productdetails**:</span><span class="sxs-lookup"><span data-stu-id="4a2a9-110">On the **Product details** page:</span></span>

    - <span data-ttu-id="4a2a9-111">Als een winkelmedewerker een pagina met **productdetails** bezoekt wanneer hij eerdere transacties via verschillende kanalen bekijkt, worden door de aanbevelingsservice extra artikelen voorgesteld die veelal samen worden gekocht.</span><span class="sxs-lookup"><span data-stu-id="4a2a9-111">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendations service suggests additional items that are likely to be purchased together.</span></span>

    <span data-ttu-id="4a2a9-112">[![Aanbevelingen op de pagina Productgegevens](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="4a2a9-112">[![Recommendations on the Product details page](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="4a2a9-113">Op de pagina **Transactie**:</span><span class="sxs-lookup"><span data-stu-id="4a2a9-113">On the **Transaction** page:</span></span>

    - <span data-ttu-id="4a2a9-114">De aanbevelingsengine stelt artikelen voor op basis van de volledige lijst met artikelen in de mand die vaak samen worden gekocht.</span><span class="sxs-lookup"><span data-stu-id="4a2a9-114">The recommendation engine suggests items based on the entire list of items in the basket that are frequently bought together.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4a2a9-115">Om aanbevelingen weer te geven op de pagina **Transactie**, moet de detailhandelaar de schermindeling in Dynamics 365 Commerce bijwerken.</span><span class="sxs-lookup"><span data-stu-id="4a2a9-115">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 Commerce.</span></span> <span data-ttu-id="4a2a9-116">Het besturingselement **Aanbevelingen** moet aan de pagina **Transactie** worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="4a2a9-116">The **Recommendations** control must be dropped onto the **Transaction** page.</span></span>

    <span data-ttu-id="4a2a9-117">[![Aanbevelingen op de pagina Transactie](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="4a2a9-117">[![Recommendations on the Transaction page](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

## <a name="configure-commerce-to-enable-pos-recommendations"></a><span data-ttu-id="4a2a9-118">Commerce configureren om aanbevelingen voor POS in te schakelen</span><span class="sxs-lookup"><span data-stu-id="4a2a9-118">Configure Commerce to enable POS recommendations</span></span>

<span data-ttu-id="4a2a9-119">Volg deze stappen om productaanbevelingen in te stellen:</span><span class="sxs-lookup"><span data-stu-id="4a2a9-119">To set up product recommendations, follow these steps:</span></span>

1. <span data-ttu-id="4a2a9-120">Controleer of de service is bijgewerkt naar **build 10.0.6**.</span><span class="sxs-lookup"><span data-stu-id="4a2a9-120">Ensure your service has been updated to the **10.0.6 build.**</span></span>
2. <span data-ttu-id="4a2a9-121">Volg de instructies voor het [inschakelen van productaanbevelingen](../commerce/enable-product-recommendations.md) voor uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="4a2a9-121">Follow the instructions on how to [enable product recommendations](../commerce/enable-product-recommendations.md) for your business.</span></span>
3. <span data-ttu-id="4a2a9-122">Optioneel: als u aanbevelingen in het transactiescherm wilt weergeven, gaat u naar **Schermindeling**, kiest u de schermindeling, start u **Ontwerper van schermindeling** en plaats u het besturingselement **aanbevelingen** op de gewenste locatie.</span><span class="sxs-lookup"><span data-stu-id="4a2a9-122">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="4a2a9-123">Ga naar **Commerce-parameters**, selecteer **Machine Learning** en selecteer **Ja** onder **POS-aanbevelingen inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="4a2a9-123">Go to **Commerce parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="4a2a9-124">Als u aanbevelingen op POS wilt zien, voert u algemene-configuratietaak **1110** uit.</span><span class="sxs-lookup"><span data-stu-id="4a2a9-124">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="4a2a9-125">Om wijzigingen in de ontwerper van de POS-schermindeling door te voeren, voert u afzetkanaalconfiguratietaak **1070** uit.</span><span class="sxs-lookup"><span data-stu-id="4a2a9-125">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="4a2a9-126">Problemen oplossen waar u al ingeschakelde productaanbevelingen hebt</span><span class="sxs-lookup"><span data-stu-id="4a2a9-126">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="4a2a9-127">Ga naar **Commerce-parameters** \> **Lijsten met aanbevelingen** \> **Productaanbevelingen uitschakelen** en start **Algemene configuratietaak \[9999\]**.</span><span class="sxs-lookup"><span data-stu-id="4a2a9-127">Navigate to **Commerce Parameters** \> **Recommendation lists** \> **Disable product recommendations** and run **Global configuration job \[9999\]**.</span></span> 
- <span data-ttu-id="4a2a9-128">Als u het besturingselement **Aanbevelingen** hebt toegevoegd aan uw transactiescherm met **Ontwerper van schermindeling**, verwijdert u dat ook.</span><span class="sxs-lookup"><span data-stu-id="4a2a9-128">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>
- <span data-ttu-id="4a2a9-129">Als u nog meer vragen hebt, raadpleegt u [Veelgestelde vragen over aanbevelingen](../commerce/faq-recommendations.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="4a2a9-129">If you have additional questions, check out the [Product recommendations FAQ](../commerce/faq-recommendations.md) for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4a2a9-130">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="4a2a9-130">Additional resources</span></span>

[<span data-ttu-id="4a2a9-131">Een besturingselement voor aanbevelingen toevoegen aan het transactiescherm op POS-apparaten</span><span class="sxs-lookup"><span data-stu-id="4a2a9-131">Add a recommendations control to the transaction screen on POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="4a2a9-132">Overzicht productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="4a2a9-132">Product recommendations overview</span></span>](../commerce/product-recommendations.md)

[<span data-ttu-id="4a2a9-133">Productaanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="4a2a9-133">Enable product recommendations</span></span>](../commerce/enable-product-recommendations.md) 
