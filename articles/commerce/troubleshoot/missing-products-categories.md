---
title: Producten en categorieën ontbreken na het kopiëren van een omgeving
description: Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen als producten en categorieën ontbreken nadat een site is gekopieerd tussen omgevingen of binnen dezelfde omgeving.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 35f2cbd98a91149395f40bf821c1d5d7e58eaf77
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585275"
---
# <a name="products-and-categories-missing-after-environment-copy"></a><span data-ttu-id="8f1b2-103">Producten en categorieën ontbreken na het kopiëren van een omgeving</span><span class="sxs-lookup"><span data-stu-id="8f1b2-103">Products and categories missing after environment copy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8f1b2-104">Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen als producten en categorieën ontbreken nadat een site is gekopieerd tussen omgevingen of binnen dezelfde omgeving.</span><span class="sxs-lookup"><span data-stu-id="8f1b2-104">This topic provides troubleshooting guidance that can help when products and categories are missing after a site is copied between environments or within the same environment.</span></span>

## <a name="description"></a><span data-ttu-id="8f1b2-105">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="8f1b2-105">Description</span></span>

<span data-ttu-id="8f1b2-106">Nadat een site van de ene omgeving naar de andere of in dezelfde omgeving is gekopieerd, ontbreken de producten en categorieën van de site.</span><span class="sxs-lookup"><span data-stu-id="8f1b2-106">After a site is copied from one environment to another, or within the same environment, the products and categories are missing from the site.</span></span> <span data-ttu-id="8f1b2-107">De producten en categorieën ontbreken in de e-commerce-winkel en op het tabblad **Producten** in Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="8f1b2-107">The products and categories will be missing from the e-commerce storefront and from the **Products** tab in Commerce site builder.</span></span>

## <a name="resolution"></a><span data-ttu-id="8f1b2-108">Oplossing</span><span class="sxs-lookup"><span data-stu-id="8f1b2-108">Resolution</span></span>

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a><span data-ttu-id="8f1b2-109">Het operationeel eenheidsnummer van een kanaal toewijzen aan een zojuist gekopieerde site in Commerce Site Builder</span><span class="sxs-lookup"><span data-stu-id="8f1b2-109">Map the channel operating unit number to a newly copied site in Commerce site builder</span></span>

<span data-ttu-id="8f1b2-110">Voer deze stappen uit als u het operationeel eenheidsnummer (OUN) van een kanaal wilt toewijzen aan een zojuist gekopieerde site in Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="8f1b2-110">To map the channel operating unit number (OUN) to a newly copied site in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="8f1b2-111">Selecteer de zojuist gekopieerde site.</span><span class="sxs-lookup"><span data-stu-id="8f1b2-111">Select the newly copied site.</span></span>
1. <span data-ttu-id="8f1b2-112">Selecteer **Kanalen** onder **Site-instellingen**.</span><span class="sxs-lookup"><span data-stu-id="8f1b2-112">Under **Site settings**, select **Channels**.</span></span>
1. <span data-ttu-id="8f1b2-113">Selecteer het weglatingsteken (**...**) naast de kanaalnaam en selecteer vervolgens **Online winkelkanaal wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="8f1b2-113">Next to the channel name, select the ellipsis (**...**), and then select **Change online store channel**.</span></span>
1. <span data-ttu-id="8f1b2-114">Selecteer in het dialoogvenster **Online winkelkanaal wijzigen** het kanaal dat u wilt toewijzen aan de zojuist gekopieerde site en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="8f1b2-114">In the **Change online store channel** dialog box, select the channel to map to the newly copied site, and then select **OK**.</span></span>
1. <span data-ttu-id="8f1b2-115">Selecteer **Opslaan en publiceren**.</span><span class="sxs-lookup"><span data-stu-id="8f1b2-115">Select **Save and publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8f1b2-116">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="8f1b2-116">Additional resources</span></span>

[<span data-ttu-id="8f1b2-117">Een Dynamics 365 Commerce-site koppelen aan een online kanaal</span><span class="sxs-lookup"><span data-stu-id="8f1b2-117">Associate a Dynamics 365 Commerce site with an online channel</span></span>](../associate-site-online-store.md)
