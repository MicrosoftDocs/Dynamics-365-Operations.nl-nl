---
title: Wanneer moet een datamart opnieuw worden ingesteld
description: In dit onderwerp worden de omstandigheden vermeld die kunnen worden verbeterd door het opnieuw instellen van een datamart en omstandigheden waarin het resetten van uw datamart waarschijnlijk niet helpt.
author: jinniew
manager: AnnBe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1c1524c7a1a3fbe71c51b23571996d87641cdf7e
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093207"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="9739a-103">Wanneer moet een datamart opnieuw worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="9739a-103">When to reset a data mart</span></span>

<span data-ttu-id="9739a-104">Het opnieuw instellen van een datamart kan tijdrovend zijn.</span><span class="sxs-lookup"><span data-stu-id="9739a-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="9739a-105">Afhankelijk van de omstandigheden is deze reset-actie mogelijk niet de oplossing die nodig is.</span><span class="sxs-lookup"><span data-stu-id="9739a-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="9739a-106">In dit onderwerp worden de omstandigheden vermeld die kunnen worden verbeterd door het opnieuw instellen van een datamart en omstandigheden waarin het resetten van uw datamart waarschijnlijk niet helpt.</span><span class="sxs-lookup"><span data-stu-id="9739a-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-you-need-to-do-a-data-mart-reset"></a><span data-ttu-id="9739a-107">Wanneer moet een datamart opnieuw worden ingesteld?</span><span class="sxs-lookup"><span data-stu-id="9739a-107">When do you need to do a data mart reset?</span></span>
<span data-ttu-id="9739a-108">Houd rekening met de volgende vragen voordat u een datamart opnieuw instelt.</span><span class="sxs-lookup"><span data-stu-id="9739a-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="9739a-109">Als u een of meer vragen met ja beantwoordt, kan dat erop wijzen dat uw organisatie baat kan hebben van het opnieuw instellen van de datamart.</span><span class="sxs-lookup"><span data-stu-id="9739a-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="9739a-110">De toepassingsdatabase is opnieuw ingesteld, maar de database van de datamart niet.</span><span class="sxs-lookup"><span data-stu-id="9739a-110">The application database was restored, but the data mart database was not restored.</span></span>
- <span data-ttu-id="9739a-111">U ziet onjuiste gegevens voor een boekhoudperiode. Dit is dus niet het resultaat van een probleem met het rapportontwerp.</span><span class="sxs-lookup"><span data-stu-id="9739a-111">You see incorrect data for an accounting period, which isn't the result of an issue with the report design.</span></span>
- <span data-ttu-id="9739a-112">U ziet onjuiste gegevens voor een boekhoudperiode en records worden weergegeven onder Integratiepogingen op de pagina **Integratiestatus** in Report Designer (start Report Designer en selecteer **Extra > Integratiestatus**).</span><span class="sxs-lookup"><span data-stu-id="9739a-112">You see incorrect data for an accounting period, and records are listed under Integration attempts on the **Integration status** page in Report Designer (start the Report Designer and select **Tools > Integration status**).</span></span>
- <span data-ttu-id="9739a-113">U hebt een ondersteuningsincident geopend en een ondersteuningstechnicus heeft u opdracht gegeven om de datamart opnieuw in te stellen als onderdeel van een probleemoplossingsstap.</span><span class="sxs-lookup"><span data-stu-id="9739a-113">You've opened a support incident and a support engineer has instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-its-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="9739a-114">Wanneer kunt u een datamart beter niet opnieuw instellen?</span><span class="sxs-lookup"><span data-stu-id="9739a-114">When it's not appropriate to reset a data mart?</span></span>
<span data-ttu-id="9739a-115">Er zijn omstandigheden waarin het niet wordt aangeraden een datamart opnieuw in te stellen.</span><span class="sxs-lookup"><span data-stu-id="9739a-115">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="9739a-116">Deze omstandigheden zijn:</span><span class="sxs-lookup"><span data-stu-id="9739a-116">These include the following.</span></span> 

- <span data-ttu-id="9739a-117">Omstandigheden waarvoor de reden niet in dit onderwerp wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="9739a-117">Anytime the reason isn’t listed in this topic.</span></span>
- <span data-ttu-id="9739a-118">U ondervindt prestatieproblemen die zijn gekoppeld aan gegevenssynchronisatie. Hierbij helpt het opnieuw instellen van de datamart waarschijnlijk niet.</span><span class="sxs-lookup"><span data-stu-id="9739a-118">You're experiencing performance issues that are associated with a data sync. In this circumstance, resetting the data mart probably won't help.</span></span>
- <span data-ttu-id="9739a-119">Als er sprake is van een terugkerend resetpatroon vanwege een van de volgende redenen:</span><span class="sxs-lookup"><span data-stu-id="9739a-119">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="9739a-120">**Ontbrekende gegevens**: elimineer eerst problemen met rapportontwerp en timing van gegevenssynchronisatie. U ziet bijvoorbeeld dat het feitenoverzicht niet is uitgevoerd omdat er ontbrekende gegevens zijn geboekt.</span><span class="sxs-lookup"><span data-stu-id="9739a-120">**Missing data** - First, eliminate report design issues and data sync timing issues, for example, you observe that the fact map hasn’t run since missing data was posted.</span></span>
  - <span data-ttu-id="9739a-121">**Vastgelopen integratie**: als de integratie langzaam is of lijkt te zijn vastgelopen, wordt het probleem waarschijnlijk niet opgelost door de datamart opnieuw in te stellen.</span><span class="sxs-lookup"><span data-stu-id="9739a-121">**Stuck integration state** - If the integration is slow or seems stuck, resetting the data mart is unlikely to resolve the issue.</span></span>
  - <span data-ttu-id="9739a-122">**Pogingen om opnieuw in te stellen zijn mislukt**: als een aantal pogingen is gedaan om een reset te voltooien en deze niet zijn gelukt vanwege ontbrekende gegevens, is het raadzaam een ondersteuningsincident te openen en samen met een ondersteuningstechnicus de situatie te analyseren voordat u de datamart opnieuw probeert in te stellen.</span><span class="sxs-lookup"><span data-stu-id="9739a-122">**Attempts to reset have been unsuccessful** - If a number of attempts to complete a reset have been made, and have been unsuccessful because of missing data, we recommend opening a support incident and working with a support engineer to analyze your situation before attempting to reset the data mart again.</span></span>
  - <span data-ttu-id="9739a-123">**Verouderde records**: verouderde records zijn op zichzelf geen reden om de datamart opnieuw in te stellen.</span><span class="sxs-lookup"><span data-stu-id="9739a-123">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="9739a-124">Als u een grote gegevensset hebt, zal het even duren deze opnieuw in te stellen, maar is het niet waarschijnlijk dat dit iets oplevert.</span><span class="sxs-lookup"><span data-stu-id="9739a-124">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-a-data-mart-reset-does-not-do"></a><span data-ttu-id="9739a-125">Wat een datamart-reset niet doet</span><span class="sxs-lookup"><span data-stu-id="9739a-125">What a data mart reset does not do</span></span>  
- <span data-ttu-id="9739a-126">Een reset wordt alleen gestart wanneer bestaande taken zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="9739a-126">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="9739a-127">Op deze manier zorgt u ervoor dat er geen oude gegevens worden ingevoegd.</span><span class="sxs-lookup"><span data-stu-id="9739a-127">This ensures that old data is not inserted.</span></span> <span data-ttu-id="9739a-128">Op dit punt wordt er mogelijk een bericht weergegeven met de tekst "De datamart-reset kan niet worden verwerkt vanwege een actieve taak.</span><span class="sxs-lookup"><span data-stu-id="9739a-128">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="9739a-129">Probeer het later opnieuw.”</span><span class="sxs-lookup"><span data-stu-id="9739a-129">Please try again later.”</span></span>
- <span data-ttu-id="9739a-130">Met de reset worden de integratietaken uitgeschakeld en worden alle datamartgegevens verwijderd.</span><span class="sxs-lookup"><span data-stu-id="9739a-130">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="9739a-131">De integratie wordt opnieuw ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="9739a-131">The integration is re-enabled.</span></span>

> [!NOTE]
> <span data-ttu-id="9739a-132">De volgende punten geven twee zaken aan die met een datamart-reset *niet* gebeuren.</span><span class="sxs-lookup"><span data-stu-id="9739a-132">The following points specify two things that resetting a data mart will *not* do.</span></span> <br>
> - <span data-ttu-id="9739a-133">Met resets worden rapportontwerpen niet gewist.</span><span class="sxs-lookup"><span data-stu-id="9739a-133">Resets do not clear report designs.</span></span> <br>
> - <span data-ttu-id="9739a-134">Met resets worden bedrijfs- of gebruikersgegevens niet gewist, tenzij u dat hebt aangegeven.</span><span class="sxs-lookup"><span data-stu-id="9739a-134">Resets do not clear company data or user data unless selected.</span></span>
