---
title: Parameters voor HR-resources instellen voor rechtspersonen
description: U moet gedeelde parameters instellen voor records die tussen bedrijven worden gedeeld, zoals Positierecords. In dit artikel wordt uitgelegd hoe u Human Resources-parameters instelt voor alle rechtspersonen.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
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
ms.openlocfilehash: cc5acf7ba1b350ee2c91923c7de3b4780385f3ef
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "303821"
---
# <a name="set-up-human-resources-hr-parameters-across-legal-entities"></a><span data-ttu-id="18ef0-104">Parameters voor HR-resources instellen voor rechtspersonen</span><span class="sxs-lookup"><span data-stu-id="18ef0-104">Set up Human resources (HR) parameters across legal entities</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="18ef0-105">U moet gedeelde parameters instellen voor records die tussen bedrijven worden gedeeld, zoals Positierecords.</span><span class="sxs-lookup"><span data-stu-id="18ef0-105">You must set up shared parameters for records that are shared across companies, such as Position records.</span></span> <span data-ttu-id="18ef0-106">In dit artikel wordt uitgelegd hoe u Human Resources-parameters instelt voor alle rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="18ef0-106">This article explains how to set up Human resources parameters across legal entities.</span></span>

<span data-ttu-id="18ef0-107">Bepaalde typen records, zoals positierecords worden gedeeld tussen bedrijven.</span><span class="sxs-lookup"><span data-stu-id="18ef0-107">Some types of records, such as Position records, are shared across companies.</span></span> <span data-ttu-id="18ef0-108">Voor deze records moet u gedeelde parameters instellen.</span><span class="sxs-lookup"><span data-stu-id="18ef0-108">For these records, you must set up shared parameters.</span></span> <span data-ttu-id="18ef0-109">U gebruikt bijvoorbeeld **Gedeelde Human resources-parameters** om human resources-parameters in te stellen voor rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="18ef0-109">For example, you use the **Human resources shared parameters** page to set up Human resources parameters across legal entities.</span></span> 

<span data-ttu-id="18ef0-110">Op de **Gedeelde Human resources-parameters** pagina worden de parameters gegroepeerd in gebieden, op basis van hun functionaliteit.</span><span class="sxs-lookup"><span data-stu-id="18ef0-110">On the **Human resources shared parameters** page, parameters are grouped into areas, based on their functionality.</span></span> 

### <a name="previously-released-functionality"></a><span data-ttu-id="18ef0-111">Eerder uitgebrachte functionaliteit</span><span class="sxs-lookup"><span data-stu-id="18ef0-111">Previously released functionality</span></span>
<span data-ttu-id="18ef0-112">Op het **Identificatie** tabblad, moet u de identificatietypen selecteren die de identificatienummers vertegenwoordigen die op de pagina worden weergeven.</span><span class="sxs-lookup"><span data-stu-id="18ef0-112">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="18ef0-113">U moet identificatietypen instellen voordat u identificatiegegevens voor werknemers kunt invoeren.</span><span class="sxs-lookup"><span data-stu-id="18ef0-113">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="18ef0-114">Informatie over het burgerservicenummer, het nationale id-nummer, het vreemdelingen-id-nummer en de persoonlijke id-code wordt onderhouden op de pagina **Identificatietype**.</span><span class="sxs-lookup"><span data-stu-id="18ef0-114">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="18ef0-115">Om een nieuw identificatietype te definiëren of de lijst met bestaande typen te controleren, klikt u op **Personeelsbeheer** &gt; tabblad **Koppelingen** &gt; **Instellingen** &gt; **Identificatietypen**.</span><span class="sxs-lookup"><span data-stu-id="18ef0-115">To define a new identification type or review the list of existing types, click **Personnel management** &gt; **Links tab** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="18ef0-116">U kunt eenvoudige code en omschrijving invoeren.</span><span class="sxs-lookup"><span data-stu-id="18ef0-116">You can enter a simple code and description.</span></span> 

### <a name="if-youre-using-dynamics-365-for-talent"></a><span data-ttu-id="18ef0-117">Als u Dynamics 365 for Talent gebruikt</span><span class="sxs-lookup"><span data-stu-id="18ef0-117">If you're using Dynamics 365 for Talent</span></span>
<span data-ttu-id="18ef0-118">Op het **Identificatie** tabblad, moet u de identificatietypen selecteren die de identificatienummers vertegenwoordigen die op de pagina worden weergeven.</span><span class="sxs-lookup"><span data-stu-id="18ef0-118">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="18ef0-119">U moet identificatietypen instellen voordat u identificatiegegevens voor werknemers kunt invoeren.</span><span class="sxs-lookup"><span data-stu-id="18ef0-119">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="18ef0-120">Informatie over het burgerservicenummer, het nationale id-nummer, het vreemdelingen-id-nummer en de persoonlijke id-code wordt onderhouden op de pagina **Identificatietype**.</span><span class="sxs-lookup"><span data-stu-id="18ef0-120">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="18ef0-121">Om een nieuw identificatie type te definiëren of de lijst met bestaande typen te controleren, klikt u op **HRM** &gt; **Instellen** &gt; **Identificatietypen**.</span><span class="sxs-lookup"><span data-stu-id="18ef0-121">To define a new identification type or review the list of existing types, click **Human resources** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="18ef0-122">U kunt eenvoudige code en omschrijving invoeren.</span><span class="sxs-lookup"><span data-stu-id="18ef0-122">You can enter a simple code and description.</span></span> 

<span data-ttu-id="18ef0-123">Op het **Nummerreeksen** tabblad, kunt u nummerreeksen selecteren die voor de volgende records worden gebruikt: Het personeelsnummer, Positie, ID gebruikersaanvraag, I-9-document, Sollicitant, Discussie, Vergoeding-id en personeelsactie (als dit recordtype is ingeschakeld).</span><span class="sxs-lookup"><span data-stu-id="18ef0-123">On the **Number sequences** tab, you can select the number sequences that are used for the following records: Personnel number, Position, User request ID, I-9 document, Applicant, Discussion, Benefit ID, and Personnel action (if this record type is enabled).</span></span> <span data-ttu-id="18ef0-124">Voor het verzorgen van verwijzingen en codes, gebruikt u de lijstpagina **Nummerreeksen**.</span><span class="sxs-lookup"><span data-stu-id="18ef0-124">To maintain number sequence references and codes, use the **Number sequences** list page.</span></span> <span data-ttu-id="18ef0-125">U kunt deze pagina vinden via de paginazoekfunctie.</span><span class="sxs-lookup"><span data-stu-id="18ef0-125">To find this page, use the page search feature.</span></span> 

<span data-ttu-id="18ef0-126">Op het **Posities** tabblad, geeft u aan of de nieuwe posities beschikbaar zijn voor standaard toewijzing:</span><span class="sxs-lookup"><span data-stu-id="18ef0-126">On the **Positions** tab, indicate whether new positions are available for assignment by default:</span></span>

-   <span data-ttu-id="18ef0-127">**Altijd:** U kunt werknemers toewijzen aan nieuwe posities wanneer posities worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="18ef0-127">**Always** – You can assign workers to new positions when positions are created.</span></span> <span data-ttu-id="18ef0-128">Wanneer posities worden gemaakt, worden de datum en tijd van **Beschikbaar voor toewijzing** op het tabblad **Algemeen** van de pagina **Positie** automatisch ingesteld op de aanmaakdatum- en tijd.</span><span class="sxs-lookup"><span data-stu-id="18ef0-128">When positions are created, the **Available for assignment** date and time on the **General** tab of the **Position** page are automatically set to the creation date and time.</span></span>
-   <span data-ttu-id="18ef0-129">**Nooit** – U kunt geen werknemers toewijzen aan nieuwe posities wanneer posities worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="18ef0-129">**Never** – You can't assign workers to new positions when positions are created.</span></span> <span data-ttu-id="18ef0-130">Als u deze optie hebt geselecteerd, moet u de pagina **Positie** openen voor elke nieuwe positie zodra deze beschikbaar wordt en vervolgens op het tabblad **Algemeen** de datum **Beschikbaar voor toewijzing** invoeren om de werknemerstoewijzing in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="18ef0-130">If you select this option, you must open the **Position** page for each new position as it becomes available, and then, on the **General** tab, enter the **Available for assignment** date to enable worker assignment.</span></span>


<a name="additional-resources"></a><span data-ttu-id="18ef0-131">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="18ef0-131">Additional resources</span></span>
--------

[<span data-ttu-id="18ef0-132">Bedrijfsspecifieke HR-parameters instellen</span><span class="sxs-lookup"><span data-stu-id="18ef0-132">Set up company specific HR parameters</span></span>](set-up-company-specific-hr-parameters.md)



