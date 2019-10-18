---
title: PRODCOM instellen en onderhouden
description: In dit onderwerp wordt uitgelegd hoe u PRODCOM instelt en onderhoudt in Microsoft Dynamics 365 Finance.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: IntrastatToProdcom, InventProdComLineDetail, InventProdComLineWithCode, InventProdComParameters, InventProdComTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 264804
ms.search.region: Belgium
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fb471bef09e6fc9b12aaee4633a69be8953e96fe
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183825"
---
# <a name="set-up-and-maintain-prodcom"></a><span data-ttu-id="11385-103">PRODCOM instellen en onderhouden</span><span class="sxs-lookup"><span data-stu-id="11385-103">Set up and maintain PRODCOM</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11385-104">In dit onderwerp wordt uitgelegd hoe u PRODCOM instelt en onderhoudt.</span><span class="sxs-lookup"><span data-stu-id="11385-104">This topic explains how to set up and maintain PRODCOM.</span></span> <span data-ttu-id="11385-105">Fabrikanten van industriële producten zijn volgens de wet verplicht de hoeveelheden en waarden van de verkochte producten evenals bepaalde werknemersgegevens door te geven aan het Nationaal Instituut voor de Statistiek (NIS) in reactie op het jaarlijkse PRODCOM-onderzoek.</span><span class="sxs-lookup"><span data-stu-id="11385-105">Manufacturers of industrial products are required to report the quantities and values of products sold, as well as employment data, to the Nationaal Instituut voor de Statistiek (NIS) in response to the routine PRODCOM survey.</span></span> <span data-ttu-id="11385-106">De meeste producenten dienen maandelijks een gespecificeerd PRODCOM-rapport bij het NIS in middels een van de zes standaardrapportindelingen.</span><span class="sxs-lookup"><span data-stu-id="11385-106">Most producers submit an itemized PRODCOM report to the NIS monthly, using one of six standard report formats.</span></span> <span data-ttu-id="11385-107">Het NIS bepaalt de rapportindeling, afhankelijk van de aard van de geproduceerde materialen.</span><span class="sxs-lookup"><span data-stu-id="11385-107">The NIS determines the report layout, depending on the nature of the materials produced.</span></span> <span data-ttu-id="11385-108">Het PRODCOM-rapport bevat productiestatistieken voor industriële producten die worden vervaardigd door productiebedrijven die in België gevestigd zijn.</span><span class="sxs-lookup"><span data-stu-id="11385-108">The PRODCOM report displays production statistics for industrial products that are manufactured by production companies operating in Belgium.</span></span> <span data-ttu-id="11385-109">Dit rapport wordt meestal gebruikt door accountants en boekhoudmanagers.</span><span class="sxs-lookup"><span data-stu-id="11385-109">This report is typically used by accounting managers and accountants.</span></span>

## <a name="set-up-prodcom-reporting"></a><span data-ttu-id="11385-110">PRODCOM-rapportage instellen</span><span class="sxs-lookup"><span data-stu-id="11385-110">Set up PRODCOM reporting</span></span>
<span data-ttu-id="11385-111">Voordat u het PRODCOM-rapport kunt genereren, moet u het volgende instellen op de pagina **PRODCOM-parameters**.</span><span class="sxs-lookup"><span data-stu-id="11385-111">Before you can generate the PRODCOM report, you must set up the following on the **PRODCOM parameters** page.</span></span>

1.  <span data-ttu-id="11385-112">Voer een primaire contactpersoon-id in.</span><span class="sxs-lookup"><span data-stu-id="11385-112">Enter a primary contact ID.</span></span> <span data-ttu-id="11385-113">Dit is de identificatie die wordt afgedrukt onder het gedeelte met informatie over de primaire contactpersoon van de PRODCOM-aangifte.</span><span class="sxs-lookup"><span data-stu-id="11385-113">This is the identification that is printed under the primary contact information section of the PRODCOM declaration.</span></span>
2.  <span data-ttu-id="11385-114">Voer een contactpersoon-id in. Dit is de identificatie die wordt afgedrukt onder het gedeelte met informatie over de externe contactpersoon van de PRODCOM-aangifte.</span><span class="sxs-lookup"><span data-stu-id="11385-114">Enter an external contact ID - This is the identification that is printed under the external contact information section of the PRODCOM declaration.</span></span>
3.  <span data-ttu-id="11385-115">Selecteer een bedrijf of magazijn.</span><span class="sxs-lookup"><span data-stu-id="11385-115">Select a company or warehouse.</span></span>
    -   <span data-ttu-id="11385-116">Als de lokale vestiging **Bedrijf** is, wordt het vestigingsnummer van het bedrijf naar de PRODCOM-regels overgeboekt.</span><span class="sxs-lookup"><span data-stu-id="11385-116">If the local branch is **Company**, the branch number of the company is transferred to the PRODCOM lines.</span></span>
    -   <span data-ttu-id="11385-117">Als de lokale vestiging **Magazijn** is, wordt het vestigingsnummer van het magazijn waar de verkoop heeft plaatsgevonden, naar de PRODCOM-regels overgeboekt.</span><span class="sxs-lookup"><span data-stu-id="11385-117">If the local branch is **Warehouse**, the branch number of the warehouse where the sale took place is transferred to the PRODCOM lines.</span></span>
    -   <span data-ttu-id="11385-118">Als het magazijn geen vestigingsnummer heeft, wordt het vestigingsnummer van het bedrijf gebruikt.</span><span class="sxs-lookup"><span data-stu-id="11385-118">If the warehouse does not have a branch number, the branch number of the company is used.</span></span>

4.  <span data-ttu-id="11385-119">Geef de voorkeur op voor een automatische herberekening.</span><span class="sxs-lookup"><span data-stu-id="11385-119">Specify an automatic recalculation preference.</span></span>
5.  <span data-ttu-id="11385-120">Nummerreeksen instellen.</span><span class="sxs-lookup"><span data-stu-id="11385-120">Set up number sequences.</span></span>
6.  <span data-ttu-id="11385-121">Geef de vestigings-id voor de rechtspersoon of magazijnen op.</span><span class="sxs-lookup"><span data-stu-id="11385-121">Specify the branch ID for Legal entity or Warehouses.</span></span> <span data-ttu-id="11385-122">Zie voor meer informatie over de vestigings-id voor verwerking van rechtspersonen, waaronder de vereisten [Registratie-id's](emea-registration-ids.md).</span><span class="sxs-lookup"><span data-stu-id="11385-122">For more information about the branch ID of Legal entity processing, including required prerequisites, see [Registration IDs](emea-registration-ids.md).</span></span>

## <a name="assign-prodcom-properties-to-an-item"></a><span data-ttu-id="11385-123">PRODCOM-eigenschappen toewijzen aan een artikel</span><span class="sxs-lookup"><span data-stu-id="11385-123">Assign PRODCOM properties to an item</span></span>
<span data-ttu-id="11385-124">PRODCOM-eigenschappen toewijzen aan een artikel (**Productgegevensbeheer** &gt; **Producten** &gt; **Vrijgegeven producten**).</span><span class="sxs-lookup"><span data-stu-id="11385-124">Assign PRODCOM properties to an item (**Product information management** &gt; **Products** &gt; **Released products**).</span></span> <span data-ttu-id="11385-125">Open de pagina **Vrijgegeven productdetails** in de sectie **Buitenlandse handel**, open het dialoogvenster PRODCOM en geef de volgende gegevens op.</span><span class="sxs-lookup"><span data-stu-id="11385-125">Open the **Released product details** page, in the **Foreign trade** section, open the PRODCOM dialog box and provide the following details.</span></span>

-   <span data-ttu-id="11385-126">**Eigen product**: schakel dit selectievakje in als u hoeveelheden en waarden van producten moet rapporteren die zijn geleverd door bedrijven.</span><span class="sxs-lookup"><span data-stu-id="11385-126">**Product made in company** - Select this check box to report quantities and values of products that were delivered by companies.</span></span>
-   <span data-ttu-id="11385-127">**Levering aan derden**: schakel dit selectievakje in als u hoeveelheden en waarden van producten wilt rapporteren die zijn geleverd door derden.</span><span class="sxs-lookup"><span data-stu-id="11385-127">**Delivery to a third party** - Select this check box to report quantities and values of products that were delivered by third parties.</span></span>
-   <span data-ttu-id="11385-128">**Werk voor** **ondernemingen**: schakel dit selectievakje in als u hoeveelheden en waarden van producten wilt rapporteren die zijn geleverd door ondernemingen.</span><span class="sxs-lookup"><span data-stu-id="11385-128">**Work done for** **enterprises** - Select this check box to report quantities and values of products that were delivered by enterprises.</span></span>

<span data-ttu-id="11385-129">Nadat u PRODCOM hebt ingesteld, kunt u de pagina **PRODCOM** gebruiken om PRODCOM-perioden te maken en verkoopregels naar het PRODCOM-rapport over te boeken.</span><span class="sxs-lookup"><span data-stu-id="11385-129">After you've set up PRODCOM, you can use the **PRODCOM** page to create PRODCOM periods and transfer sales lines to the PRODCOM report.</span></span>

## <a name="convert-intrastat-to-prodcom"></a><span data-ttu-id="11385-130">Conversie van Intrastat naar PRODCOM</span><span class="sxs-lookup"><span data-stu-id="11385-130">Convert Intrastat to PRODCOM</span></span>
<span data-ttu-id="11385-131">Gebruik de pagina **Conversie van Intrastat naar PRODCOM** om PRODCOM-codes toe te wijzen aan Intrastat-basisproductcodes.</span><span class="sxs-lookup"><span data-stu-id="11385-131">Use the **Intrastat to PRODCOM conversion** page to assign PRODCOM codes to Intrastat commodity codes.</span></span> <span data-ttu-id="11385-132">Deze codes kunnen elk jaar wijzigen.</span><span class="sxs-lookup"><span data-stu-id="11385-132">These codes can change every year.</span></span> <span data-ttu-id="11385-133">Klik op de pagina **Conversie van Intrastat naar PRODCOM** op **PRODCOM-gegevens importeren** om de gegevens te importeren.</span><span class="sxs-lookup"><span data-stu-id="11385-133">On the **Intrastat to PRODCOM conversion** page, click **Import PRODCOM data** to import the information.</span></span>

## <a name="use-prodcom"></a><span data-ttu-id="11385-134">PRODCOM gebruiken</span><span class="sxs-lookup"><span data-stu-id="11385-134">Use PRODCOM</span></span>
<span data-ttu-id="11385-135">Gebruik de pagina **PRODCOM** om PRODCOM-perioden te maken en verkoopregels naar het PRODCOM-rapport over te boeken.</span><span class="sxs-lookup"><span data-stu-id="11385-135">Use the **PRODCOM** page to create PRODCOM periods and transfer sales lines to the PRODCOM report.</span></span> <span data-ttu-id="11385-136">Nadat u de datums voor de aangifteperiode hebt ingevoerd en vervolgens de sectiecodes invoert, kunt u de verkoopregels overboeken naar het PRODCOM-rapport.</span><span class="sxs-lookup"><span data-stu-id="11385-136">After you enter the dates for the declaration period and then enter the section codes, you can transfer the sales lines to the PRODCOM report.</span></span> <span data-ttu-id="11385-137">Nadat u de verkoopregels naar het rapport hebt overgeboekt, kunt u de producten op de PRODCOM-lijst bekijken en bewerken en vervolgens het rapport afdrukken.</span><span class="sxs-lookup"><span data-stu-id="11385-137">After you transfer the sales lines to the report, you can review and edit the products on the PRODCOM list, and then you can print the report.</span></span>



