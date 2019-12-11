---
title: Productaanbevelingen inschakelen
description: In dit onderwerp wordt uitgelegd hoe u productaanbevelingen kunt doen op basis van kunstmatige intelligentie-machine learning (AI-ML) die beschikbaar is voor klanten van Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ecda571a356c6968196d09cc19923105cf4544ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770134"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="99a26-103">Productaanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="99a26-103">Enable product recommendations</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="99a26-104">In dit onderwerp wordt uitgelegd hoe u productaanbevelingen kunt doen op basis van kunstmatige intelligentie-machine learning (AI-ML) die beschikbaar is voor klanten van Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="99a26-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="99a26-105">Meer informatie over lijsten met productaanbevelingen vindt u in [Overzicht van productaanbevelingen](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="99a26-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="99a26-106">Aanbevelingen voor controle vooraf</span><span class="sxs-lookup"><span data-stu-id="99a26-106">Recommendations pre-check</span></span>
<span data-ttu-id="99a26-107">Houd er rekening mee dat productaanbevelingen alleen worden ondersteund voor F&O-klanten die build 10.0.6 ondersteunen en hun opslag hebben gemigreerd naar BDL.</span><span class="sxs-lookup"><span data-stu-id="99a26-107">Before enabling, please note that product recommendations are only supported for F&O customers supporting build 10.0.6 and have migrated their storage to using BDL.</span></span> 

<span data-ttu-id="99a26-108">Zorg er bovendien voor dat RetailSale-metingen zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="99a26-108">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="99a26-109">[Hier](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures) vindt u meer informatie over dit instellingsproces.</span><span class="sxs-lookup"><span data-stu-id="99a26-109">To Learn more about this set up process, go [here.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="99a26-110">Aanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="99a26-110">Turn on recommendations</span></span>

<span data-ttu-id="99a26-111">Volg deze stappen om productaanbevelingen in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="99a26-111">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="99a26-112">Ga naar **Detailhandel** &gt; **Productaanbevelingen** &gt; **Aanbevelingsparameters**.</span><span class="sxs-lookup"><span data-stu-id="99a26-112">Go to **Retail** &gt; **Product recommendations** &gt; **Recommendation parameters**.</span></span>
1. <span data-ttu-id="99a26-113">Selecteer **Aanbevelingslijsten** in de lijst met gedeelde parameters voor detailhandel.</span><span class="sxs-lookup"><span data-stu-id="99a26-113">In the list of retail shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="99a26-114">Stel de optie **Aanbevelingen inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="99a26-114">Set the **Enable recommendations** option to **Yes**.</span></span>

![Productaanbevelingen inschakelen](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="99a26-116">Met deze procedure start u het genereren van lijsten voor productaanbevelingen.</span><span class="sxs-lookup"><span data-stu-id="99a26-116">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="99a26-117">Het kan enkele uren duren voordat de lijsten beschikbaar zijn en kunnen worden weergegeven op het verkooppunt (POS) of in Dynamics 365 for Commerce.</span><span class="sxs-lookup"><span data-stu-id="99a26-117">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 for Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="99a26-118">Parameters voor aanbevelingslijsten configureren</span><span class="sxs-lookup"><span data-stu-id="99a26-118">Configure recommendation list parameters</span></span>
<span data-ttu-id="99a26-119">Standaard bevat de lijst met productaanbevelingen op basis van AI-ML voorgestelde waarden.</span><span class="sxs-lookup"><span data-stu-id="99a26-119">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="99a26-120">U kunt de voorgestelde standaardwaarden aanpassen aan de stroom van uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="99a26-120">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="99a26-121">Als u meer wilt weten over het wijzigen van de standaardparameters, gaat u naar [Resultaten van productaanbevelingen op basis van AI-ML beheren](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="99a26-121">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="99a26-122">Aanbevelingen weergeven op POS-apparaten</span><span class="sxs-lookup"><span data-stu-id="99a26-122">Show recommendations on POS devices</span></span>
<span data-ttu-id="99a26-123">Nadat u aanbevelingen in de backoffice hebt ingeschakeld, moet het deelvenster met aanbevelingen worden toegevoegd aan het POS-scherm van het besturingselement via de indelingsfunctie.</span><span class="sxs-lookup"><span data-stu-id="99a26-123">After enabling recommendations in the back office, the recommendations pannel must be added to the control POS screen via the layout tool.</span></span> <span data-ttu-id="99a26-124">[Hier](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen) vindt u meer informatie over dit proces.</span><span class="sxs-lookup"><span data-stu-id="99a26-124">To learn about this process, go [here.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)</span></span>


## <a name="additional-resources"></a><span data-ttu-id="99a26-125">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="99a26-125">Additional resources</span></span>

[<span data-ttu-id="99a26-126">Overzicht productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="99a26-126">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="99a26-127">Lijsten met productaanbevelingen toevoegen aan pagina's</span><span class="sxs-lookup"><span data-stu-id="99a26-127">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="99a26-128">Het deelvenster met aanbevelingen toevoegen aan POS-apparaten</span><span class="sxs-lookup"><span data-stu-id="99a26-128">Add recommendations panel to POS devices</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


