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
ms.openlocfilehash: 2d3f1bc2526eeacb4bd6338a0679eadd95a75989
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024951"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="ff262-103">Productaanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="ff262-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ff262-104">In dit onderwerp wordt uitgelegd hoe u productaanbevelingen kunt doen op basis van kunstmatige intelligentie-machine learning (AI-ML) die beschikbaar is voor klanten van Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ff262-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="ff262-105">Meer informatie over lijsten met productaanbevelingen vindt u in [Overzicht van productaanbevelingen](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="ff262-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="ff262-106">Aanbevelingen voor controle vooraf</span><span class="sxs-lookup"><span data-stu-id="ff262-106">Recommendations pre-check</span></span>

<span data-ttu-id="ff262-107">Houd er rekening mee dat productaanbevelingen alleen worden ondersteund voor Commerce-klanten die hun opslag hebben gemigreerd met behulp van Azure Data Lake Storage (ADLS).</span><span class="sxs-lookup"><span data-stu-id="ff262-107">Before enabling, please note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="ff262-108">Zie [ADLS in een Dynamics 365-omgeving inschakelen](enable-ADLS-environment.md) voor stapsgewijze instructies voor het inschakelen van ADLS.</span><span class="sxs-lookup"><span data-stu-id="ff262-108">For steps on enabling ADLS, see [How to enable ADLS in a Dynamics 365 environment](enable-ADLS-environment.md).</span></span>

<span data-ttu-id="ff262-109">Zorg er bovendien voor dat RetailSale-metingen zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="ff262-109">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="ff262-110">[Hier](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures) vindt u meer informatie over dit instellingsproces.</span><span class="sxs-lookup"><span data-stu-id="ff262-110">To learn more about this set up process, go [here.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="ff262-111">Aanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="ff262-111">Turn on recommendations</span></span>

<span data-ttu-id="ff262-112">Volg deze stappen om productaanbevelingen in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="ff262-112">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="ff262-113">Ga naar **Retail en Commerce &gt; Productaanbevelingen &gt; Aanbevelingsparameters**.</span><span class="sxs-lookup"><span data-stu-id="ff262-113">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="ff262-114">Selecteer **Aanbevelingslijsten** in de lijst met gedeelde parameters.</span><span class="sxs-lookup"><span data-stu-id="ff262-114">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="ff262-115">Stel de optie **Aanbevelingen inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ff262-115">Set the **Enable recommendations** option to **Yes**.</span></span>

![Productaanbevelingen inschakelen](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="ff262-117">Met deze procedure start u het genereren van lijsten voor productaanbevelingen.</span><span class="sxs-lookup"><span data-stu-id="ff262-117">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="ff262-118">Het kan enkele uren duren voordat de lijsten beschikbaar zijn en kunnen worden weergegeven op het verkooppunt (POS) of in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ff262-118">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="ff262-119">Parameters voor aanbevelingslijsten configureren</span><span class="sxs-lookup"><span data-stu-id="ff262-119">Configure recommendation list parameters</span></span>

<span data-ttu-id="ff262-120">Standaard bevat de lijst met productaanbevelingen op basis van AI-ML voorgestelde waarden.</span><span class="sxs-lookup"><span data-stu-id="ff262-120">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="ff262-121">U kunt de voorgestelde standaardwaarden aanpassen aan de stroom van uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="ff262-121">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="ff262-122">Als u meer wilt weten over het wijzigen van de standaardparameters, gaat u naar [Resultaten van productaanbevelingen op basis van AI-ML beheren](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="ff262-122">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="ff262-123">Aanbevelingen weergeven op POS-apparaten</span><span class="sxs-lookup"><span data-stu-id="ff262-123">Show recommendations on POS devices</span></span>

<span data-ttu-id="ff262-124">Nadat u aanbevelingen in de Commerce-backoffice hebt ingeschakeld, moet het deelvenster met aanbevelingen worden toegevoegd aan het POS-scherm van het besturingselement via de indelingsfunctie.</span><span class="sxs-lookup"><span data-stu-id="ff262-124">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="ff262-125">Zie [Een besturingselement voor aanbevelingen toevoegen aan het transactiescherm op POS-apparaten](add-recommendations-control-pos-screen.md) voor meer informatie over dit proces.</span><span class="sxs-lookup"><span data-stu-id="ff262-125">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="ff262-126">Gepersonaliseerde aanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="ff262-126">Enable personalized recommendations</span></span>

<span data-ttu-id="ff262-127">Zie [Persoonlijke aanbevelingen inschakelen](personalized-recommendations.md) voor meer informatie over het ontvangen van persoonlijke productaanbevelingen.</span><span class="sxs-lookup"><span data-stu-id="ff262-127">To learn more about how to receive personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ff262-128">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="ff262-128">Additional resources</span></span>

[<span data-ttu-id="ff262-129">Overzicht productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="ff262-129">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="ff262-130">Gepersonaliseerde aanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="ff262-130">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="ff262-131">Lijsten met productaanbevelingen toevoegen aan pagina's</span><span class="sxs-lookup"><span data-stu-id="ff262-131">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="ff262-132">Het deelvenster met aanbevelingen toevoegen aan POS-apparaten</span><span class="sxs-lookup"><span data-stu-id="ff262-132">Add recommendations panel to POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="ff262-133">Overzicht productverzamelingsmodule</span><span class="sxs-lookup"><span data-stu-id="ff262-133">Product collection module overview</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="ff262-134">ADLS inschakelen in een Dynamics 365-omgeving</span><span class="sxs-lookup"><span data-stu-id="ff262-134">Enable ADLS in Dynamics 365 environment</span></span>](enable-ADLS-environment.md)

