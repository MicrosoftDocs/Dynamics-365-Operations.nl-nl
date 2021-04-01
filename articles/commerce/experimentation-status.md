---
title: De status van een experiment controleren
description: In dit onderwerp wordt uitgelegd welke status een experiment heeft in de levenscyclus van het experiment in Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: ae459ddaf947db6c3de2602a706390edab49efa1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250853"
---
# <a name="review-the-status-of-an-experiment"></a><span data-ttu-id="a46a2-103">De status van een experiment controleren</span><span class="sxs-lookup"><span data-stu-id="a46a2-103">Review the status of an experiment</span></span>
<span data-ttu-id="a46a2-104">Er zijn diverse stappen betrokken bij het instellen en uitvoeren van een experiment in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a46a2-104">There are many steps involved in setting up and running an experiment in Dynamics 365 Commerce.</span></span> <span data-ttu-id="a46a2-105">Zie [Experimenten in Dynamics 365 Commerce](experimentation-overview.md) voor informatie over de levenscyclus van experimenten.</span><span class="sxs-lookup"><span data-stu-id="a46a2-105">For information about the experimentation lifecycle, see [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="a46a2-106">Selecteer **Experimenten** in het linkernavigatievenster in Commerce Site Builder als u wilt weten waar een experiment zich in de levenscyclus bevindt.</span><span class="sxs-lookup"><span data-stu-id="a46a2-106">To learn where an experiment is in the lifecycle, in Commerce site builder select **Experiments** in the left navigation pane.</span></span> <span data-ttu-id="a46a2-107">Er wordt een lijst met experimenten weergegeven met de status van elk experiment in zowel Commerce als de service van derden die wordt gebruikt om experimenten te maken, variaties toe te wijzen en gegevens te analyseren.</span><span class="sxs-lookup"><span data-stu-id="a46a2-107">A list of experiments is displayed with the status of each experiment in both Commerce and the third-party service that is being used to enable the creation of experiments, assign variations, and analyze data.</span></span>

<span data-ttu-id="a46a2-108">In de kolom **Commerce-status** kunnen de volgende waarden worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="a46a2-108">In the **Commerce status** column, the following values may be displayed.</span></span> 
- <span data-ttu-id="a46a2-109">**Concept**: het experiment is verbonden met een pagina of fragment in Commerce en wordt bewerkt.</span><span class="sxs-lookup"><span data-stu-id="a46a2-109">**Draft** - The experiment is connected to a page or fragment in Commerce and is being edited.</span></span>
- <span data-ttu-id="a46a2-110">**Gepubliceerd**: de experimentvariaties zijn klaar om op uw website te worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="a46a2-110">**Published** - The experiment variations are ready to be displayed on your website.</span></span> <span data-ttu-id="a46a2-111">Als het experiment wordt uitgevoerd in de service van derden, zien de gebruikers van de website een variatie op de pagina of het fragment zoals deze is geselecteerd door de service van derden.</span><span class="sxs-lookup"><span data-stu-id="a46a2-111">If the experiment is running in the third-party service, website users will see a variation of the page or fragment as selected by the third-party service.</span></span>
- <span data-ttu-id="a46a2-112">**Niet-gepubliceerd**: het experiment is niet meer beschikbaar op uw website.</span><span class="sxs-lookup"><span data-stu-id="a46a2-112">**Unpublished** - The experiment is no longer available on your website.</span></span> <span data-ttu-id="a46a2-113">Zelfs als het experiment wordt uitgevoerd in de service van derden, zien de gebruikers van de website alleen de standaardversie van de pagina of het fragment.</span><span class="sxs-lookup"><span data-stu-id="a46a2-113">Website users will only see the default version of the page or fragment even if the experiment is running in the third-party service.</span></span>
- <span data-ttu-id="a46a2-114">**Voltooid**: het experiment is uitgevoerd en er is een variatie gepromoveerd voor gebruik op de live site voor alle websitegebruikers.</span><span class="sxs-lookup"><span data-stu-id="a46a2-114">**Completed** - The experiment has run its course and a variation was promoted to live for all website users.</span></span>

<span data-ttu-id="a46a2-115">Zo ook kunnen in de kolom **Status van derden** de volgende waarden worden weergegeven om aan te geven welke status de experimenten hebben in de service van derden.</span><span class="sxs-lookup"><span data-stu-id="a46a2-115">Similarly, in the **third-party status** column, the following values may be displayed to indicate what status the experiments are in the third-party service.</span></span>
- <span data-ttu-id="a46a2-116">**Concept**: het experiment is ingesteld in de service van derden, maar is niet gestart.</span><span class="sxs-lookup"><span data-stu-id="a46a2-116">**Draft** - The experiment is set up in the third-party service but hasn't been started.</span></span>
- <span data-ttu-id="a46a2-117">**Actief**: het experiment is gestart in de service van derden en er worden gegevens verzameld.</span><span class="sxs-lookup"><span data-stu-id="a46a2-117">**Running** - The experiment was started in the third-party service and is collecting data.</span></span>
- <span data-ttu-id="a46a2-118">**Onderbroken**: het experiment is onderbroken en er worden geen gegevens verzameld.</span><span class="sxs-lookup"><span data-stu-id="a46a2-118">**Paused** - The experiment is paused and not collecting data.</span></span> <span data-ttu-id="a46a2-119">U moet het experiment hervatten om gegevens opnieuw te verzamelen.</span><span class="sxs-lookup"><span data-stu-id="a46a2-119">You must resume the experiment for it to collect data again.</span></span>
- <span data-ttu-id="a46a2-120">**Gearchiveerd**: het experiment is uitgevoerd en is gecatalogiseerd in de service van derden voor toekomstige naslag.</span><span class="sxs-lookup"><span data-stu-id="a46a2-120">**Archived** - The experiment has run its course and has been cataloged in the third-party service for future reference.</span></span>

<span data-ttu-id="a46a2-121">In het onderstaande diagram ziet u beide sets statuswaarden en de relatie tussen deze twee sets.</span><span class="sxs-lookup"><span data-stu-id="a46a2-121">The diagram below shows both sets of statuses and how they relate to each other.</span></span>

<span data-ttu-id="a46a2-122">[ ![Statuswaarden van experimenten](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="a46a2-122">[ ![Experimentation statuses](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]