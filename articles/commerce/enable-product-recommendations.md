---
title: Productaanbevelingen inschakelen
description: In dit onderwerp wordt uitgelegd hoe u productaanbevelingen kunt doen op basis van kunstmatige intelligentie-machine learning (AI-ML) die beschikbaar is voor klanten van Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 03/19/2020
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
ms.openlocfilehash: d8a579be5df3c5e7718a6fb4720341f3bd01a64c
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154408"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="1bd24-103">Productaanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="1bd24-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1bd24-104">In dit onderwerp wordt uitgelegd hoe u productaanbevelingen kunt doen op basis van kunstmatige intelligentie-machine learning (AI-ML) die beschikbaar is voor klanten van Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1bd24-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="1bd24-105">Meer informatie over lijsten met productaanbevelingen vindt u in [Overzicht van productaanbevelingen](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="1bd24-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="1bd24-106">Aanbevelingen voor controle vooraf</span><span class="sxs-lookup"><span data-stu-id="1bd24-106">Recommendations pre-check</span></span>

<span data-ttu-id="1bd24-107">Houd er rekening mee dat productaanbevelingen alleen worden ondersteund voor Commerce-klanten die hun opslag hebben gemigreerd met behulp van Azure Data Lake Storage (ADLS).</span><span class="sxs-lookup"><span data-stu-id="1bd24-107">Before enabling, please note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="1bd24-108">Zie [ADLS in een Dynamics 365-omgeving inschakelen](enable-ADLS-environment.md) voor stapsgewijze instructies voor het inschakelen van ADLS.</span><span class="sxs-lookup"><span data-stu-id="1bd24-108">For steps on enabling ADLS, see [How to enable ADLS in a Dynamics 365 environment](enable-ADLS-environment.md).</span></span>

<span data-ttu-id="1bd24-109">Zorg er bovendien voor dat RetailSale-metingen zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="1bd24-109">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="1bd24-110">[Hier](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures) vindt u meer informatie over dit instellingsproces.</span><span class="sxs-lookup"><span data-stu-id="1bd24-110">To learn more about this set up process, go [here.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="1bd24-111">Aanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="1bd24-111">Turn on recommendations</span></span>

<span data-ttu-id="1bd24-112">Volg deze stappen om productaanbevelingen in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="1bd24-112">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="1bd24-113">Ga naar **Retail en Commerce &gt; Productaanbevelingen &gt; Aanbevelingsparameters**.</span><span class="sxs-lookup"><span data-stu-id="1bd24-113">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="1bd24-114">Selecteer **Aanbevelingslijsten** in de lijst met gedeelde parameters.</span><span class="sxs-lookup"><span data-stu-id="1bd24-114">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="1bd24-115">Stel de optie **Aanbevelingen inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="1bd24-115">Set the **Enable recommendations** option to **Yes**.</span></span>

![Productaanbevelingen inschakelen](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="1bd24-117">Met deze procedure start u het genereren van lijsten voor productaanbevelingen.</span><span class="sxs-lookup"><span data-stu-id="1bd24-117">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="1bd24-118">Het kan enkele uren duren voordat de lijsten beschikbaar zijn en kunnen worden weergegeven op het verkooppunt (POS) of in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1bd24-118">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="1bd24-119">Parameters voor aanbevelingslijsten configureren</span><span class="sxs-lookup"><span data-stu-id="1bd24-119">Configure recommendation list parameters</span></span>

<span data-ttu-id="1bd24-120">Standaard bevat de lijst met productaanbevelingen op basis van AI-ML voorgestelde waarden.</span><span class="sxs-lookup"><span data-stu-id="1bd24-120">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="1bd24-121">U kunt de voorgestelde standaardwaarden aanpassen aan de stroom van uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="1bd24-121">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="1bd24-122">Als u meer wilt weten over het wijzigen van de standaardparameters, gaat u naar [Resultaten van productaanbevelingen op basis van AI-ML beheren](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="1bd24-122">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="1bd24-123">Aanbevelingen weergeven op POS-apparaten</span><span class="sxs-lookup"><span data-stu-id="1bd24-123">Show recommendations on POS devices</span></span>

<span data-ttu-id="1bd24-124">Nadat u aanbevelingen in de Commerce-backoffice hebt ingeschakeld, moet het deelvenster met aanbevelingen worden toegevoegd aan het POS-scherm van het besturingselement via de indelingsfunctie.</span><span class="sxs-lookup"><span data-stu-id="1bd24-124">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="1bd24-125">Zie [Een besturingselement voor aanbevelingen toevoegen aan het transactiescherm op POS-apparaten](add-recommendations-control-pos-screen.md) voor meer informatie over dit proces.</span><span class="sxs-lookup"><span data-stu-id="1bd24-125">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="1bd24-126">Gepersonaliseerde aanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="1bd24-126">Enable personalized recommendations</span></span>

<span data-ttu-id="1bd24-127">Zie [Persoonlijke aanbevelingen inschakelen](personalized-recommendations.md) voor meer informatie over het ontvangen van persoonlijke productaanbevelingen.</span><span class="sxs-lookup"><span data-stu-id="1bd24-127">To learn more about how to receive personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1bd24-128">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="1bd24-128">Additional resources</span></span>

[<span data-ttu-id="1bd24-129">Overzicht productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="1bd24-129">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="1bd24-130">ADLS inschakelen in een Dynamics 365 Commerce-omgeving</span><span class="sxs-lookup"><span data-stu-id="1bd24-130">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="1bd24-131">Gepersonaliseerde aanbevelingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="1bd24-131">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="1bd24-132">Afmelden voor gepersonaliseerde aanbevelingen</span><span class="sxs-lookup"><span data-stu-id="1bd24-132">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="1bd24-133">Productaanbevelingen toevoegen op POS</span><span class="sxs-lookup"><span data-stu-id="1bd24-133">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="1bd24-134">Aanbevelingen toevoegen aan het transactiescherm</span><span class="sxs-lookup"><span data-stu-id="1bd24-134">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="1bd24-135">Resultaten van AI-ML-aanbevelingen aanpassen</span><span class="sxs-lookup"><span data-stu-id="1bd24-135">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="1bd24-136">Handmatig gecureerde aanbevelingen maken</span><span class="sxs-lookup"><span data-stu-id="1bd24-136">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="1bd24-137">Aanbevelingen maken met voorbeeldgegevens</span><span class="sxs-lookup"><span data-stu-id="1bd24-137">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="1bd24-138">Veelgestelde vragen over productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="1bd24-138">Product recommendations FAQ</span></span>](faq-recommendations.md)

