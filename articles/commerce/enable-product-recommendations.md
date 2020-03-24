---
title: Productaanbevelingen inschakelen
description: In dit onderwerp wordt uitgelegd hoe u productaanbevelingen kunt doen op basis van kunstmatige intelligentie-machine learning (AI-ML) die beschikbaar is voor klanten van Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
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
ms.openlocfilehash: 879fccb063ca0b74e0f022a9edf6a15f7d1311ae
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127877"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="1700f-103">Productaanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="1700f-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1700f-104">In dit onderwerp wordt uitgelegd hoe u productaanbevelingen kunt doen op basis van kunstmatige intelligentie-machine learning (AI-ML) die beschikbaar is voor klanten van Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1700f-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="1700f-105">Meer informatie over lijsten met productaanbevelingen vindt u in [Overzicht van productaanbevelingen](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="1700f-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="1700f-106">Aanbevelingen voor controle vooraf</span><span class="sxs-lookup"><span data-stu-id="1700f-106">Recommendations pre-check</span></span>

<span data-ttu-id="1700f-107">Houd er rekening mee dat productaanbevelingen alleen worden ondersteund voor Commerce-klanten die hun opslag hebben gemigreerd met behulp van Azure Data Lake Storage (ADLS).</span><span class="sxs-lookup"><span data-stu-id="1700f-107">Before enabling, please note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="1700f-108">Zie [ADLS in een Dynamics 365-omgeving inschakelen](enable-ADLS-environment.md) voor stapsgewijze instructies voor het inschakelen van ADLS.</span><span class="sxs-lookup"><span data-stu-id="1700f-108">For steps on enabling ADLS, see [How to enable ADLS in a Dynamics 365 environment](enable-ADLS-environment.md).</span></span>

<span data-ttu-id="1700f-109">Zorg er bovendien voor dat RetailSale-metingen zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="1700f-109">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="1700f-110">[Hier](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures) vindt u meer informatie over dit instellingsproces.</span><span class="sxs-lookup"><span data-stu-id="1700f-110">To learn more about this set up process, go [here.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="1700f-111">Aanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="1700f-111">Turn on recommendations</span></span>

<span data-ttu-id="1700f-112">Volg deze stappen om productaanbevelingen in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="1700f-112">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="1700f-113">Ga naar **Retail en Commerce &gt; Productaanbevelingen &gt; Aanbevelingsparameters**.</span><span class="sxs-lookup"><span data-stu-id="1700f-113">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="1700f-114">Selecteer **Aanbevelingslijsten** in de lijst met gedeelde parameters.</span><span class="sxs-lookup"><span data-stu-id="1700f-114">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="1700f-115">Stel de optie **Aanbevelingen inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="1700f-115">Set the **Enable recommendations** option to **Yes**.</span></span>

![Productaanbevelingen inschakelen](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="1700f-117">Met deze procedure start u het genereren van lijsten voor productaanbevelingen.</span><span class="sxs-lookup"><span data-stu-id="1700f-117">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="1700f-118">Het kan enkele uren duren voordat de lijsten beschikbaar zijn en kunnen worden weergegeven op het verkooppunt (POS) of in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1700f-118">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="1700f-119">Parameters voor aanbevelingslijsten configureren</span><span class="sxs-lookup"><span data-stu-id="1700f-119">Configure recommendation list parameters</span></span>

<span data-ttu-id="1700f-120">Standaard bevat de lijst met productaanbevelingen op basis van AI-ML voorgestelde waarden.</span><span class="sxs-lookup"><span data-stu-id="1700f-120">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="1700f-121">U kunt de voorgestelde standaardwaarden aanpassen aan de stroom van uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="1700f-121">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="1700f-122">Als u meer wilt weten over het wijzigen van de standaardparameters, gaat u naar [Resultaten van productaanbevelingen op basis van AI-ML beheren](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="1700f-122">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="1700f-123">Aanbevelingen weergeven op POS-apparaten</span><span class="sxs-lookup"><span data-stu-id="1700f-123">Show recommendations on POS devices</span></span>

<span data-ttu-id="1700f-124">Nadat u aanbevelingen in de Commerce-backoffice hebt ingeschakeld, moet het deelvenster met aanbevelingen worden toegevoegd aan het POS-scherm van het besturingselement via de indelingsfunctie.</span><span class="sxs-lookup"><span data-stu-id="1700f-124">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="1700f-125">Zie [Een besturingselement voor aanbevelingen toevoegen aan het transactiescherm op POS-apparaten](add-recommendations-control-pos-screen.md) voor meer informatie over dit proces.</span><span class="sxs-lookup"><span data-stu-id="1700f-125">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="1700f-126">Gepersonaliseerde aanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="1700f-126">Enable personalized recommendations</span></span>

<span data-ttu-id="1700f-127">Zie [Persoonlijke aanbevelingen inschakelen](personalized-recommendations.md) voor meer informatie over het ontvangen van persoonlijke productaanbevelingen.</span><span class="sxs-lookup"><span data-stu-id="1700f-127">To learn more about how to receive personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1700f-128">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="1700f-128">Additional resources</span></span>

[<span data-ttu-id="1700f-129">Overzicht productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="1700f-129">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="1700f-130">ADLS inschakelen in een Dynamics 365 Commerce-omgeving</span><span class="sxs-lookup"><span data-stu-id="1700f-130">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="1700f-131">Gepersonaliseerde aanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="1700f-131">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="1700f-132">Afmelden voor gepersonaliseerde aanbevelingen</span><span class="sxs-lookup"><span data-stu-id="1700f-132">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="1700f-133">Lijsten met aanbevelingen toevoegen aan e-commerce-site</span><span class="sxs-lookup"><span data-stu-id="1700f-133">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="1700f-134">Productaanbevelingen toevoegen op POS</span><span class="sxs-lookup"><span data-stu-id="1700f-134">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="1700f-135">Aanbevelingen toevoegen aan het transactiescherm</span><span class="sxs-lookup"><span data-stu-id="1700f-135">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="1700f-136">Resultaten van AI-ML-aanbevelingen aanpassen</span><span class="sxs-lookup"><span data-stu-id="1700f-136">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="1700f-137">Handmatig gecureerde aanbevelingen maken</span><span class="sxs-lookup"><span data-stu-id="1700f-137">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="1700f-138">Aanbevelingen maken met voorbeeldgegevens</span><span class="sxs-lookup"><span data-stu-id="1700f-138">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="1700f-139">Veelgestelde vragen over productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="1700f-139">Product recommendations FAQ</span></span>](faq-recommendations.md)

