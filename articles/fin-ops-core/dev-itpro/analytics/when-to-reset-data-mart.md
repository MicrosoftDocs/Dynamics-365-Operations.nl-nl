---
title: Veelgestelde vragen over opnieuw instellen van een datamart
description: Dit onderwerp biedt antwoorden op een aantal veelgestelde vragen over het opnieuw instellen (reset) van een datamart.
author: jinniew
ms.date: 06/09/2021
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
ms.openlocfilehash: 7cd96c7bc698986ef1ef07ca88479a3d49f22924
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266604"
---
# <a name="data-mart-resets-faq"></a><span data-ttu-id="8a386-103">Veelgestelde vragen over opnieuw instellen van een datamart</span><span class="sxs-lookup"><span data-stu-id="8a386-103">Data mart resets FAQ</span></span>

<span data-ttu-id="8a386-104">Dit onderwerp biedt antwoorden op een aantal veelgestelde vragen over het opnieuw instellen (reset) van een datamart.</span><span class="sxs-lookup"><span data-stu-id="8a386-104">This topic provides answers to some frequently asked questions about data mart resets.</span></span> <span data-ttu-id="8a386-105">Het opnieuw instellen van de datamart kan een tijdrovend proces zijn en is, afhankelijk van de omstandigheden, mogelijk niet de oplossing die nodig is.</span><span class="sxs-lookup"><span data-stu-id="8a386-105">A reset of the data mart can be a time-consuming process and, depending on the circumstances, might not be the solution that is required.</span></span> <span data-ttu-id="8a386-106">Daarom bevat dit onderwerp informatie over omstandigheden waarin opnieuw instellen van een datamart kan helpen en omstandigheden waarin het opnieuw instellen van de datamart waarschijnlijk niet helpt.</span><span class="sxs-lookup"><span data-stu-id="8a386-106">Therefore, this topic includes information about circumstances where a data mart reset might help and also circumstances where it's unlikely to help.</span></span>

## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="8a386-107">Wat houdt opnieuw instellen van een datamart in?</span><span class="sxs-lookup"><span data-stu-id="8a386-107">What is a data mart reset?</span></span>

<span data-ttu-id="8a386-108">Met opnieuw instellen van een datamart worden de integratietaken uitgeschakeld, alle datamart-gegevens verwijderd en de integratie opnieuw ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="8a386-108">A data mart reset will disable the integration tasks, delete all the data mart data, and then re-enable integration.</span></span>

<span data-ttu-id="8a386-109">Om te zorgen dat oude gegevens niet zijn ingevoegd, kan opnieuw instellen van een datamart alleen worden gestart nadat bestaande taken zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="8a386-109">To ensure that old data isn't inserted, a data mart reset can be started only after existing tasks are completed.</span></span> <span data-ttu-id="8a386-110">Als u probeert een datamart opnieuw in te stellen voordat alle taken zijn voltooid, ontvangt u mogelijk een bericht, bijvoorbeeld: 'De datamart-reset kan niet worden verwerkt vanwege een actieve taak.</span><span class="sxs-lookup"><span data-stu-id="8a386-110">If you try to reset the data mart before all tasks are completed, you might receive a message such as, "The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="8a386-111">Probeer het later opnieuw.'</span><span class="sxs-lookup"><span data-stu-id="8a386-111">Please try again later."</span></span>

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a><span data-ttu-id="8a386-112">Wanneer moet ik een datamart opnieuw instellen?</span><span class="sxs-lookup"><span data-stu-id="8a386-112">When do I have to do a data mart reset?</span></span>

<span data-ttu-id="8a386-113">Als er een of meer van de volgende uitspraken van toepassing zijn op uw situatie, kan opnieuw instellen van een datamart voor uw organisatie zin hebben:</span><span class="sxs-lookup"><span data-stu-id="8a386-113">If one or more of the following statements apply to your situation, your organization can benefit from a data mart reset:</span></span>

- <span data-ttu-id="8a386-114">De toepassingsdatabase is teruggezet.</span><span class="sxs-lookup"><span data-stu-id="8a386-114">The application database was restored.</span></span>
- <span data-ttu-id="8a386-115">U hebt een ondersteuningsticket geopend en een ondersteuningstechnicus heeft u opdracht gegeven om de datamart opnieuw in te stellen als onderdeel van een probleemoplossingsstap.</span><span class="sxs-lookup"><span data-stu-id="8a386-115">You opened a support ticket, and a Support engineer instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a><span data-ttu-id="8a386-116">Wanneer kunt u een datamart beter niet opnieuw instellen?</span><span class="sxs-lookup"><span data-stu-id="8a386-116">When is a data mart reset inappropriate?</span></span>

<span data-ttu-id="8a386-117">Hierna volgen enkele omstandigheden waarin het niet raadzaam is om een datamart opnieuw in te stellen:</span><span class="sxs-lookup"><span data-stu-id="8a386-117">Here are some of the circumstances where we don't recommend that you reset the data mart:</span></span>

- <span data-ttu-id="8a386-118">U ondervindt prestatieproblemen die betrekking hebben op gegevenssynchronisatie.</span><span class="sxs-lookup"><span data-stu-id="8a386-118">You're experiencing performance issues that are associated with data synchronization.</span></span>
- <span data-ttu-id="8a386-119">Er is sprake van een terugkerend resetpatroon om een van de volgende redenen:</span><span class="sxs-lookup"><span data-stu-id="8a386-119">You have a recurring reset pattern for any of the following reasons:</span></span>

    - <span data-ttu-id="8a386-120">**Ontbrekende gegevens**: als u ziet dat er gegevens ontbreken, opent u een ondersteuningticket bij Microsoft om de rapportindeling en mogelijke problemen met gegevenssynchronisatie te bekijken.</span><span class="sxs-lookup"><span data-stu-id="8a386-120">**Missing data** – If you notice that data is missing, open a support ticket with Microsoft to review your report format and possible data synchronization issues.</span></span>
    - <span data-ttu-id="8a386-121">**Vastgelopen integratie**</span><span class="sxs-lookup"><span data-stu-id="8a386-121">**Stuck integration state**</span></span>
    - <span data-ttu-id="8a386-122">**Verouderde records**: verouderde records zijn op zichzelf geen reden om de datamart opnieuw in te stellen.</span><span class="sxs-lookup"><span data-stu-id="8a386-122">**Stale records** – Stale records by themselves don't necessarily justify a data mart reset.</span></span> <span data-ttu-id="8a386-123">Als u een grote gegevensset hebt, zal het even duren deze opnieuw in te stellen, maar is het niet waarschijnlijk dat dit iets oplevert.</span><span class="sxs-lookup"><span data-stu-id="8a386-123">If you have a large data set, the reset process will take some time to run but is unlikely to lead to any improvement.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="8a386-124">Als ik de datamart opnieuw instel, raak ik dan rapporten kwijt die ik al heb ontworpen?</span><span class="sxs-lookup"><span data-stu-id="8a386-124">If I reset the data mart, will I lose reports that I've already designed?</span></span>

<span data-ttu-id="8a386-125">Nee.</span><span class="sxs-lookup"><span data-stu-id="8a386-125">No.</span></span> <span data-ttu-id="8a386-126">Uw rapporten worden opgeslagen in SQL-tabellen die niet worden beïnvloed door opnieuw instellen van de datamart.</span><span class="sxs-lookup"><span data-stu-id="8a386-126">Your reports are stored in SQL tables that aren't affected by a data mart reset.</span></span> <span data-ttu-id="8a386-127">Als u zich zorgen maakt over het kwijtraken van rapporten die u hebt ontworpen, kunt u een back-up maken van de ontwerpen die u niet kwijt wilt raken.</span><span class="sxs-lookup"><span data-stu-id="8a386-127">If you're concerned about losing reports that you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="8a386-128">Als u een back-up van de ontwerpen wilt maken, opent u Report Designer en gaat u naar **Bedrijf \> Bedrijven \> Bouwstenen \> Exporteren**.</span><span class="sxs-lookup"><span data-stu-id="8a386-128">To back up designs, open Report Designer, and go to **Company \> Companies \> Building Blocks \> Export**.</span></span>
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a><span data-ttu-id="8a386-129">Moeten alle gebruikers het systeem afsluiten voordat ik de datamart opnieuw kan instellen?</span><span class="sxs-lookup"><span data-stu-id="8a386-129">Do all users have to exit the system before I can reset the data mart?</span></span>

<span data-ttu-id="8a386-130">Nee.</span><span class="sxs-lookup"><span data-stu-id="8a386-130">No.</span></span> <span data-ttu-id="8a386-131">Gebruikers kunnen in het systeem blijven werken tijdens het opnieuw instellen van een datamart.</span><span class="sxs-lookup"><span data-stu-id="8a386-131">Users can continue to work in the system during a data mart reset.</span></span> <span data-ttu-id="8a386-132">Ze hebben echter geen toegang tot rapporten die met Financial Reporter zijn gemaakt totdat het instellen van de datamart is voltooid.</span><span class="sxs-lookup"><span data-stu-id="8a386-132">However, until the reset is completed, users won't be able to access any reports that were created by using Financial Reporter.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
