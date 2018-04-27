---
title: HR-parameters instellen voor rechtspersonen
description: U moet gedeelde parameters instellen voor records die tussen bedrijven worden gedeeld, zoals Positierecords. In dit artikel wordt uitgelegd hoe u Human Resources-parameters instelt voor alle rechtspersonen.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmSharedParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2e73441a3f4190561d1d16db40ee1581267c8dfb
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---

# <a name="set-up-hr-parameters-across-legal-entities"></a><span data-ttu-id="b65dc-104">HR-parameters instellen voor rechtspersonen</span><span class="sxs-lookup"><span data-stu-id="b65dc-104">Set up HR parameters across legal entities</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="b65dc-105">U moet gedeelde parameters instellen voor records die tussen bedrijven worden gedeeld, zoals Positierecords.</span><span class="sxs-lookup"><span data-stu-id="b65dc-105">You must set up shared parameters for records that are shared across companies, such as Position records.</span></span> <span data-ttu-id="b65dc-106">In dit artikel wordt uitgelegd hoe u Human Resources-parameters instelt voor alle rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="b65dc-106">This article explains how to set up Human resources parameters across legal entities.</span></span>

<span data-ttu-id="b65dc-107">Bepaalde typen records, zoals positierecords worden gedeeld tussen bedrijven.</span><span class="sxs-lookup"><span data-stu-id="b65dc-107">Some types of records, such as Position records, are shared across companies.</span></span> <span data-ttu-id="b65dc-108">Voor deze records moet u gedeelde parameters instellen.</span><span class="sxs-lookup"><span data-stu-id="b65dc-108">For these records, you must set up shared parameters.</span></span> <span data-ttu-id="b65dc-109">U gebruikt bijvoorbeeld **Gedeelde Human resources-parameters** om human resources-parameters in te stellen voor rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="b65dc-109">For example, you use the **Human resources shared parameters** page to set up Human resources parameters across legal entities.</span></span> 

<span data-ttu-id="b65dc-110">Op de **Gedeelde Human resources-parameters** pagina worden de parameters gegroepeerd in gebieden, op basis van hun functionaliteit.</span><span class="sxs-lookup"><span data-stu-id="b65dc-110">On the **Human resources shared parameters** page, parameters are grouped into areas, based on their functionality.</span></span> 

### <a name="previously-released-functionality"></a><span data-ttu-id="b65dc-111">Eerder uitgebrachte functionaliteit</span><span class="sxs-lookup"><span data-stu-id="b65dc-111">Previously released functionality</span></span>
<span data-ttu-id="b65dc-112">Op het **Identificatie** tabblad, moet u de identificatietypen selecteren die de identificatienummers vertegenwoordigen die op de pagina worden weergeven.</span><span class="sxs-lookup"><span data-stu-id="b65dc-112">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="b65dc-113">U moet identificatietypen instellen voordat u identificatiegegevens voor werknemers kunt invoeren.</span><span class="sxs-lookup"><span data-stu-id="b65dc-113">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="b65dc-114">Informatie over het burgerservicenummer, het nationale id-nummer, het vreemdelingen-id-nummer en de persoonlijke id-code wordt onderhouden op de pagina **Identificatietype**.</span><span class="sxs-lookup"><span data-stu-id="b65dc-114">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="b65dc-115">Om een nieuw identificatietype te definiëren of de lijst met bestaande typen te controleren, klikt u op **Personeelsbeheer** &gt; tabblad **Koppelingen** &gt; **Instellingen** &gt; **Identificatietypen**.</span><span class="sxs-lookup"><span data-stu-id="b65dc-115">To define a new identification type or review the list of existing types, click **Personnel management** &gt; **Links tab** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="b65dc-116">U kunt eenvoudige code en omschrijving invoeren.</span><span class="sxs-lookup"><span data-stu-id="b65dc-116">You can enter a simple code and description.</span></span> 

### <a name="if-youre-using-dynamics-365-for-talent"></a><span data-ttu-id="b65dc-117">Als u Dynamics 365 for Talent gebruikt</span><span class="sxs-lookup"><span data-stu-id="b65dc-117">If you're using Dynamics 365 for Talent</span></span>
<span data-ttu-id="b65dc-118">Op het **Identificatie** tabblad, moet u de identificatietypen selecteren die de identificatienummers vertegenwoordigen die op de pagina worden weergeven.</span><span class="sxs-lookup"><span data-stu-id="b65dc-118">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="b65dc-119">U moet identificatietypen instellen voordat u identificatiegegevens voor werknemers kunt invoeren.</span><span class="sxs-lookup"><span data-stu-id="b65dc-119">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="b65dc-120">Informatie over het burgerservicenummer, het nationale id-nummer, het vreemdelingen-id-nummer en de persoonlijke id-code wordt onderhouden op de pagina **Identificatietype**.</span><span class="sxs-lookup"><span data-stu-id="b65dc-120">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="b65dc-121">Om een nieuw identificatie type te definiëren of de lijst met bestaande typen te controleren, klikt u op **HRM** &gt; **Instellen** &gt; **Identificatietypen**.</span><span class="sxs-lookup"><span data-stu-id="b65dc-121">To define a new identification type or review the list of existing types, click **Human resources** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="b65dc-122">U kunt eenvoudige code en omschrijving invoeren.</span><span class="sxs-lookup"><span data-stu-id="b65dc-122">You can enter a simple code and description.</span></span> 

<span data-ttu-id="b65dc-123">Op het **Nummerreeksen** tabblad, kunt u nummerreeksen selecteren die voor de volgende records worden gebruikt: Het personeelsnummer, Positie, ID gebruikersaanvraag, I-9-document, Sollicitant, Discussie, Vergoeding-id en personeelsactie (als dit recordtype is ingeschakeld).</span><span class="sxs-lookup"><span data-stu-id="b65dc-123">On the **Number sequences** tab, you can select the number sequences that are used for the following records: Personnel number, Position, User request ID, I-9 document, Applicant, Discussion, Benefit ID, and Personnel action (if this record type is enabled).</span></span> <span data-ttu-id="b65dc-124">Voor het verzorgen van verwijzingen en codes, gebruikt u de lijstpagina **Nummerreeksen**.</span><span class="sxs-lookup"><span data-stu-id="b65dc-124">To maintain number sequence references and codes, use the **Number sequences** list page.</span></span> <span data-ttu-id="b65dc-125">U kunt deze pagina vinden via de paginazoekfunctie.</span><span class="sxs-lookup"><span data-stu-id="b65dc-125">To find this page, use the page search feature.</span></span> 

<span data-ttu-id="b65dc-126">Op het **Posities** tabblad, geeft u aan of de nieuwe posities beschikbaar zijn voor standaard toewijzing:</span><span class="sxs-lookup"><span data-stu-id="b65dc-126">On the **Positions** tab, indicate whether new positions are available for assignment by default:</span></span>

-   <span data-ttu-id="b65dc-127">**Altijd:** U kunt werknemers toewijzen aan nieuwe posities wanneer posities worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="b65dc-127">**Always** – You can assign workers to new positions when positions are created.</span></span> <span data-ttu-id="b65dc-128">Wanneer posities worden gemaakt, worden de datum en tijd van **Beschikbaar voor toewijzing** op het tabblad **Algemeen** van de pagina **Positie** automatisch ingesteld op de aanmaakdatum- en tijd.</span><span class="sxs-lookup"><span data-stu-id="b65dc-128">When positions are created, the **Available for assignment** date and time on the **General** tab of the **Position** page are automatically set to the creation date and time.</span></span>
-   <span data-ttu-id="b65dc-129">**Nooit** – U kunt geen werknemers toewijzen aan nieuwe posities wanneer posities worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="b65dc-129">**Never** – You can't assign workers to new positions when positions are created.</span></span> <span data-ttu-id="b65dc-130">Als u deze optie hebt geselecteerd, moet u de pagina **Positie** openen voor elke nieuwe positie zodra deze beschikbaar wordt en vervolgens op het tabblad **Algemeen** de datum **Beschikbaar voor toewijzing** invoeren om de werknemerstoewijzing in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="b65dc-130">If you select this option, you must open the **Position** page for each new position as it becomes available, and then, on the **General** tab, enter the **Available for assignment** date to enable worker assignment.</span></span>


<a name="see-also"></a><span data-ttu-id="b65dc-131">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b65dc-131">See also</span></span>
--------

[<span data-ttu-id="b65dc-132">Bedrijfsspecifieke HR-parameters instellen</span><span class="sxs-lookup"><span data-stu-id="b65dc-132">Set up company specific HR parameters</span></span>](set-up-company-specific-hr-parameters.md)




