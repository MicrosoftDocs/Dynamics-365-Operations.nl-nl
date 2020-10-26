---
title: Integratie voor serviceovereenkomsten en projecten
description: Als u werkt met serviceovereenkomsten en serviceovereenkomstregels, maakt u gebruik van gegevens die in de gebieden in Projectbeheer en boekhouding zijn ingesteld.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 578e4b9fe5ef487e999fd0de28d7566bad21fd89
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985578"
---
# <a name="integration-for-service-agreements-and-projects"></a><span data-ttu-id="69de1-103">Integratie voor serviceovereenkomsten en projecten</span><span class="sxs-lookup"><span data-stu-id="69de1-103">Integration for service agreements and projects</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="69de1-104">Als u werkt met serviceovereenkomsten en serviceovereenkomstregels, maakt u gebruik van gegevens die in de volgende gebieden in **Projectbeheer en boekhouding** zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="69de1-104">When you work with service agreements and service agreement lines, you use data that is set up in the following areas in **Project management and accounting**.</span></span>

## <a name="project-prices"></a><span data-ttu-id="69de1-105">Projectprijzen</span><span class="sxs-lookup"><span data-stu-id="69de1-105">Project prices</span></span>

<span data-ttu-id="69de1-106">De kostprijs en verkoopprijs voor een serviceovereenkomsttransactie worden afgeleid uit de ingestelde kostprijzen die gelden voor het project dat aan de serviceovereenkomst is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="69de1-106">The cost and the sales price for a service agreement transaction are derived from the cost price setup that applies to the project that is attached to the service agreement.</span></span> <span data-ttu-id="69de1-107">Kost- en verkoopprijzen kunnen per project, werknemer en categorie worden ingesteld.</span><span class="sxs-lookup"><span data-stu-id="69de1-107">Cost and sales prices can be set up by project, employee, and category.</span></span> 

## <a name="project-validation"></a><span data-ttu-id="69de1-108">Projectvalidatie</span><span class="sxs-lookup"><span data-stu-id="69de1-108">Project validation</span></span>

<span data-ttu-id="69de1-109">Op basis van de validatie-instellingen in **Projectbeheer en boekhouding** wordt bepaald welke projecten, werknemers en categorieën in een serviceovereenkomstregel beschikbaar zijn voor selectie.</span><span class="sxs-lookup"><span data-stu-id="69de1-109">The projects, employees, and categories that are available for selection on a service agreement line can be limited by the validation setup in **Project management and accounting**.</span></span> <span data-ttu-id="69de1-110">Met de validatie-instellingen kunt u werknemers, projecten en categorieën combineren om de toegang te controleren.</span><span class="sxs-lookup"><span data-stu-id="69de1-110">By using the validation setup, you can combine employees, projects, and categories for control access.</span></span> 

## <a name="project-line-properties"></a><span data-ttu-id="69de1-111">Projectregeleigenschappen</span><span class="sxs-lookup"><span data-stu-id="69de1-111">Project line properties</span></span>

<span data-ttu-id="69de1-112">Voor een serviceovereenkomstregel wordt automatisch een regeleigenschap ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="69de1-112">A line property is entered automatically for a service agreement line.</span></span>

<span data-ttu-id="69de1-113">Regeleigenschappen worden gemaakt in het formulier **Regeleigenschappen** in **Projectbeheer en boekhouding**.</span><span class="sxs-lookup"><span data-stu-id="69de1-113">Line properties are created in the **Line properties** form in **Project management and accounting**.</span></span> <span data-ttu-id="69de1-114">De regeleigenschap die in een serviceovereenkomst wordt ingevoerd, is gekoppeld aan het project dat voor de serviceovereenkomst is geselecteerd, en wordt vervolgens overgenomen door de serviceovereenkomstregel.</span><span class="sxs-lookup"><span data-stu-id="69de1-114">The line property that is entered on a service agreement is attached to the project that is selected for the service agreement and inherited subsequently by the service agreement line.</span></span> 

## <a name="default-offset-accounts"></a><span data-ttu-id="69de1-115">Standaardtegenrekeningen</span><span class="sxs-lookup"><span data-stu-id="69de1-115">Default offset accounts</span></span>

<span data-ttu-id="69de1-116">Voor een onkostentransactie die u invoert, wordt automatisch een standaardonkostentegenrekening geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="69de1-116">If you enter an expense transaction, a default expense offset account is selected automatically for the transaction.</span></span> <span data-ttu-id="69de1-117">De standaardonkostenrekening is ingesteld voor het project dat aan de huidige serviceovereenkomst is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="69de1-117">The default expense account is set up for the project that is attached to the current service agreement.</span></span>

## <a name="project-categories"></a><span data-ttu-id="69de1-118">Projectcategorieën</span><span class="sxs-lookup"><span data-stu-id="69de1-118">Project categories</span></span>

<span data-ttu-id="69de1-119">Welke categorieën voor serviceovereenkomstregels beschikbaar zijn, wordt ingesteld in het formulier **Projectcategorieën** in **Projectbeheer en boekhouding**.</span><span class="sxs-lookup"><span data-stu-id="69de1-119">The categories that are available for service agreement lines are set up in the **Project categories** form in **Project management and accounting**.</span></span> 

> [!NOTE]
> <P><span data-ttu-id="69de1-120">Categorieën waarvoor het selectievakje <STRONG>Actief in journalen</STRONG> op het tabblad <STRONG>Project</STRONG> in het formulier <STRONG>Projectcategorieën</STRONG> is ingeschakeld, zijn beschikbaar voor selectie.</span><span class="sxs-lookup"><span data-stu-id="69de1-120">Categories that have the <STRONG>Active in journals</STRONG> check box selected on the <STRONG>Project</STRONG> tab in the <STRONG>Project categories</STRONG> form are available for selection.</span></span> <span data-ttu-id="69de1-121">Als echter het selectievakje <STRONG>Inactieve categorieën</STRONG> op het tabblad <STRONG>Journalen</STRONG> in het formulier <STRONG>Projectbeheer- en boekhoudingsparameters</STRONG> is ingeschakeld, zijn alle categorieën beschikbaar voor selectie.</span><span class="sxs-lookup"><span data-stu-id="69de1-121">However, if the <STRONG>Inactive categories</STRONG> check box is selected on the <STRONG>Journals</STRONG> tab in the <STRONG>Project management and accounting parameters</STRONG> form, all categories are available for selection.</span></span></P>

## <a name="project-parameters"></a><span data-ttu-id="69de1-122">Projectparameters</span><span class="sxs-lookup"><span data-stu-id="69de1-122">Project parameters</span></span>

<span data-ttu-id="69de1-123">Als het veld **Ontslagen werknemers** op het tabblad **Journalen** in het formulier **Projectbeheer- en boekhoudingsparameters** is geselecteerd, kunt u inactieve werknemers en actieve werknemers in de formulieren **Serviceovereenkomsten** en **Serviceorders** selecteren.</span><span class="sxs-lookup"><span data-stu-id="69de1-123">If the **Terminated workers** field on the **Journals** tab in the **Project management and accounting parameters** form is selected, you can select inactive employees and active employees in the **Service agreements** and **Service orders** forms.</span></span>

<span data-ttu-id="69de1-124">Verder kunt u de velden **Begintijd** en **Eindtijd** op het tabblad **Project** in het formulier **Serviceorders** inschakelen om begin- en eindtijden op serviceorderregels in te voeren.</span><span class="sxs-lookup"><span data-stu-id="69de1-124">Also, you can enable the **Start time** and **End time** fields on the **Project** tab in the **Service orders** form to enter starting and ending times on service order lines.</span></span>

## <a name="enable-the-starting-and-ending-time-feature-for-service-orders"></a><span data-ttu-id="69de1-125">De functie voor begin- en eindtijd voor serviceorders inschakelen</span><span class="sxs-lookup"><span data-stu-id="69de1-125">Enable the starting and ending time feature for service orders</span></span>

1.  <span data-ttu-id="69de1-126">Klik op **Projectbeheer en boekhouding** \> **Instellen** \> **Projectbeheer- en boekhoudingsparameters**.</span><span class="sxs-lookup"><span data-stu-id="69de1-126">Click **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>

2.  <span data-ttu-id="69de1-127">Klik op het tabblad **Journalen** en schakel het selectievakje **Begin-/eindtijden weergeven** in.</span><span class="sxs-lookup"><span data-stu-id="69de1-127">Click the **Journals** tab, and then select the **Show start/end times** check box.</span></span>

3.  <span data-ttu-id="69de1-128">Klik op **Projectbeheer en boekhouding** \> **Instellen** \> **Journalen** \> **Journaalnamen**.</span><span class="sxs-lookup"><span data-stu-id="69de1-128">Click **Project management and accounting** \> **Setup** \> **Journals** \> **Journal names**.</span></span>

4.  <span data-ttu-id="69de1-129">Selecteer de journaalnaam die aan de serviceorder is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="69de1-129">Select the journal name that is attached to the service order.</span></span>

5.  <span data-ttu-id="69de1-130">Klik op het tabblad **Algemeen** en schakel het selectievakje **Begin-/eindtijden weergeven** in.</span><span class="sxs-lookup"><span data-stu-id="69de1-130">Click the **General** tab, and then select the **Show start/end times** check box.</span></span>


> [!NOTE]
> <P><span data-ttu-id="69de1-131">Selecteer de journaalnaam voor de serviceorder in het veld <STRONG>Uur</STRONG> op het tabblad <STRONG>Journalen</STRONG> in het formulier <STRONG>Parameters voor servicebeheer</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="69de1-131">Select the journal name for the service order in the <STRONG>Hour</STRONG> field on the <STRONG>Journals</STRONG> tab in the <STRONG>Service management parameters</STRONG> form.</span></span></P>





