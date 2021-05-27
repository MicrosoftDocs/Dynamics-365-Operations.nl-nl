---
title: Wanneer moet een datamart opnieuw worden ingesteld
description: In dit onderwerp worden de omstandigheden vermeld die kunnen worden verbeterd door het opnieuw instellen van een datamart en omstandigheden waarin het resetten van uw datamart waarschijnlijk niet helpt.
author: jinniew
ms.date: 05/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: bc2c4ee490f3bebd6e7c91609a06f8dfedfcb628
ms.sourcegitcommit: 5916ea2a94ab9af7aac21f0fc44e194d5ce82917
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2021
ms.locfileid: "5988987"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="3c886-103">Wanneer moet een datamart opnieuw worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="3c886-103">When to reset a data mart</span></span>

<span data-ttu-id="3c886-104">Het opnieuw instellen van een datamart kan tijdrovend zijn.</span><span class="sxs-lookup"><span data-stu-id="3c886-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="3c886-105">Afhankelijk van de omstandigheden is deze reset-actie mogelijk niet de oplossing die nodig is.</span><span class="sxs-lookup"><span data-stu-id="3c886-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="3c886-106">In dit onderwerp worden de omstandigheden vermeld die kunnen worden verbeterd door het opnieuw instellen van een datamart en omstandigheden waarin het resetten van uw datamart waarschijnlijk niet helpt.</span><span class="sxs-lookup"><span data-stu-id="3c886-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-i-need-to-do-a-data-mart-reset"></a><span data-ttu-id="3c886-107">Wanneer moet ik een datamart opnieuw instellen?</span><span class="sxs-lookup"><span data-stu-id="3c886-107">When do I need to do a data mart reset?</span></span>
<span data-ttu-id="3c886-108">Houd rekening met de volgende vragen voordat u een datamart opnieuw instelt.</span><span class="sxs-lookup"><span data-stu-id="3c886-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="3c886-109">Als u een of meer vragen met ja beantwoordt, kan dat erop wijzen dat uw organisatie baat kan hebben van het opnieuw instellen van de datamart.</span><span class="sxs-lookup"><span data-stu-id="3c886-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="3c886-110">Is de toepassingsdatabase teruggezet?</span><span class="sxs-lookup"><span data-stu-id="3c886-110">Was the application database restored?</span></span>
- <span data-ttu-id="3c886-111">Als u een ondersteuningsincident hebt geopend en een ondersteuningstechnicus heeft u opdracht gegeven om de datamart opnieuw in te stellen als onderdeel van een probleemoplossingsstap?</span><span class="sxs-lookup"><span data-stu-id="3c886-111">If you've opened a support incident that and a support engineer has instructed you to reset the data mart as part of a troubleshooting step?</span></span>
 
## <a name="when-is-it-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="3c886-112">Wanneer kunt u een datamart beter niet opnieuw instellen?</span><span class="sxs-lookup"><span data-stu-id="3c886-112">When is it not appropriate to reset a data mart?</span></span>
<span data-ttu-id="3c886-113">Er zijn omstandigheden waarin het niet wordt aangeraden een datamart opnieuw in te stellen.</span><span class="sxs-lookup"><span data-stu-id="3c886-113">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="3c886-114">Deze omstandigheden zijn:</span><span class="sxs-lookup"><span data-stu-id="3c886-114">These include the following.</span></span> 

- <span data-ttu-id="3c886-115">U ondervindt prestatieproblemen die betrekking hebben op gegevenssynchronisatie.</span><span class="sxs-lookup"><span data-stu-id="3c886-115">You're experiencing performance issues that are associated with a data sync.</span></span> 
- <span data-ttu-id="3c886-116">Als er sprake is van een terugkerend resetpatroon vanwege een van de volgende redenen:</span><span class="sxs-lookup"><span data-stu-id="3c886-116">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="3c886-117">**Ontbrekende gegevens**</span><span class="sxs-lookup"><span data-stu-id="3c886-117">**Missing data**</span></span> 
  - <span data-ttu-id="3c886-118">**Vastgelopen integratie**</span><span class="sxs-lookup"><span data-stu-id="3c886-118">**Stuck integration state**</span></span> 
  - <span data-ttu-id="3c886-119">**Verouderde records**: verouderde records zijn op zichzelf geen reden om de datamart opnieuw in te stellen.</span><span class="sxs-lookup"><span data-stu-id="3c886-119">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="3c886-120">Als u een grote gegevensset hebt, zal het even duren deze opnieuw in te stellen, maar is het niet waarschijnlijk dat dit iets oplevert.</span><span class="sxs-lookup"><span data-stu-id="3c886-120">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="3c886-121">Wat houdt opnieuw instellen van een datamart in?</span><span class="sxs-lookup"><span data-stu-id="3c886-121">What is a data mart reset?</span></span>
- <span data-ttu-id="3c886-122">Een reset wordt alleen gestart wanneer bestaande taken zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="3c886-122">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="3c886-123">Op deze manier zorgt u ervoor dat er geen oude gegevens worden ingevoegd.</span><span class="sxs-lookup"><span data-stu-id="3c886-123">This ensures that old data is not inserted.</span></span> <span data-ttu-id="3c886-124">Op dit punt wordt er mogelijk een bericht weergegeven met de tekst "De datamart-reset kan niet worden verwerkt vanwege een actieve taak.</span><span class="sxs-lookup"><span data-stu-id="3c886-124">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="3c886-125">Probeer het later opnieuw.”</span><span class="sxs-lookup"><span data-stu-id="3c886-125">Please try again later.”</span></span>
- <span data-ttu-id="3c886-126">Met de reset worden de integratietaken uitgeschakeld en worden alle datamartgegevens verwijderd.</span><span class="sxs-lookup"><span data-stu-id="3c886-126">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="3c886-127">De integratie wordt opnieuw ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="3c886-127">The integration is re-enabled.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="3c886-128">Als ik de datamart opnieuw instel, raak ik dan rapporten kwijt die ik al heb ontworpen?</span><span class="sxs-lookup"><span data-stu-id="3c886-128">If I reset the data mart, will I lose reports that I've already designed?</span></span> 
<span data-ttu-id="3c886-129">Nee, uw rapporten worden opgeslagen in SQL-tabellen die niet worden beïnvloed door opnieuw instellen van de datamart.</span><span class="sxs-lookup"><span data-stu-id="3c886-129">No, your reports are stored in SQL tables that are not impacted by a reset of the data mart.</span></span> <span data-ttu-id="3c886-130">Als u zich zorgen maakt over het kwijtraken van rapporten die u hebt ontworpen, kunt u een back-up maken van de ontwerpen die u niet kwijt wilt raken.</span><span class="sxs-lookup"><span data-stu-id="3c886-130">If you are concerned about losing any reports you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="3c886-131">Als u een back-up wilt maken, opent u Report Designer en gaat u naar **Bedrijf > Bedrijven > Bouwstenen > Exporteren**.</span><span class="sxs-lookup"><span data-stu-id="3c886-131">To back them up, open Report Designer and go to **Company > Companies > Building Blocks > Export**.</span></span>
 
## <a name="is-it-necessary-for-all-users-to-exit-the-system-to-reset-the-data-mart"></a><span data-ttu-id="3c886-132">Moeten alle gebruikers het systeem afsluiten om de datamart opnieuw in te stellen?</span><span class="sxs-lookup"><span data-stu-id="3c886-132">Is it necessary for all users to exit the system to reset the data mart?</span></span>
<span data-ttu-id="3c886-133">Nee, gebruikers kunnen in het systeem blijven werken tijdens het opnieuw instellen van de datamart.</span><span class="sxs-lookup"><span data-stu-id="3c886-133">No, users can continue working in the system during the data mart reset.</span></span> <span data-ttu-id="3c886-134">Ze hebben echter geen toegang tot rapporten die met Financial Reporter zijn gemaakt totdat de datamart opnieuw is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="3c886-134">However, they won’t be able to access any reports that were created with Financial Reporter until the reset is finished.</span></span> 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
