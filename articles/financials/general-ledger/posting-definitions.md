---
title: Boekdefinities
description: "Dit artikel bevat informatie over boekdefinities en hoe u deze definieert en koppelt. Voor ondersteunde boekingstypen en documenten kunt u boekdefinities in plaats van boekingsprofielen gebruiken om hoofdrekeningen en financiële dimensies voor boekhoudvermeldingen te classificeren."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 513d3e20e0c89eb0064e3c1bc11a3a8dea43cfe4
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="posting-definitions"></a><span data-ttu-id="4f9a1-104">Boekdefinities</span><span class="sxs-lookup"><span data-stu-id="4f9a1-104">Posting definitions</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="4f9a1-105">Dit artikel bevat informatie over boekdefinities en hoe u deze definieert en koppelt.</span><span class="sxs-lookup"><span data-stu-id="4f9a1-105">This article provides information about posting definitions, and how to define and link them.</span></span> <span data-ttu-id="4f9a1-106">Voor ondersteunde boekingstypen en documenten kunt u boekdefinities in plaats van boekingsprofielen gebruiken om hoofdrekeningen en financiële dimensies voor boekhoudvermeldingen te classificeren.</span><span class="sxs-lookup"><span data-stu-id="4f9a1-106">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span>

<span data-ttu-id="4f9a1-107">Voor ondersteunde boekingstypen en documenten kunt u boekdefinities in plaats van boekingsprofielen gebruiken om hoofdrekeningen en financiële dimensies voor boekhoudvermeldingen te classificeren.</span><span class="sxs-lookup"><span data-stu-id="4f9a1-107">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span> <span data-ttu-id="4f9a1-108">U kunt de ondersteunde documenten en boekingstypen op de pagina **Boekdefinities voor transacties** weergeven.</span><span class="sxs-lookup"><span data-stu-id="4f9a1-108">You can view the supported documents and posting types on the **Transaction posting definitions** page.</span></span> 

<span data-ttu-id="4f9a1-109">Als u boekdefinities wilt gaan gebruiken, selecteert u de optie **Boekdefinities gebruiken** op de pagina **Grootboekparameters**.</span><span class="sxs-lookup"><span data-stu-id="4f9a1-109">To start using posting definitions, select the **Use posting definitions** option on the **General ledger parameters** page.</span></span> <span data-ttu-id="4f9a1-110">Zelfs wanneer u boekdefinities gebruikt, moet u nog steeds boekingsprofielen definiëren voor de oorspronkelijke vermeldingen en niet-ondersteunde boekingstypen en documenten.</span><span class="sxs-lookup"><span data-stu-id="4f9a1-110">Even when you use posting definitions, you must still define posting profiles for the originating entries and non-supported posting types and documents.</span></span> 

<span data-ttu-id="4f9a1-111">U moet boekdefinities gebruiken om vorderingsboekhouding in te schakelen voor inkooporders en voorvorderingsboekhouding voor opdrachten tot inkoop.</span><span class="sxs-lookup"><span data-stu-id="4f9a1-111">You must use posting definitions in order to enable encumbrance accounting for purchase orders and pre-encumbrance accounting for purchase requisitions.</span></span>

## <a name="defining-posting-definitions"></a><span data-ttu-id="4f9a1-112">Boekdefinities definiëren</span><span class="sxs-lookup"><span data-stu-id="4f9a1-112">Defining posting definitions</span></span>
<span data-ttu-id="4f9a1-113">Gebruik de pagina **Boekdefinities** om de matchcriteria en de gegevens op te geven die moeten worden gegenereerd wanneer een overeenkomst optreedt.</span><span class="sxs-lookup"><span data-stu-id="4f9a1-113">Use the **Posting definitions** page to specify the match criteria and define the entries that should be generated when a match occurs.</span></span> <span data-ttu-id="4f9a1-114">De matchcriteria worden geëvalueerd voor de oorspronkelijke invoer als boekhoudingsverdelingen.</span><span class="sxs-lookup"><span data-stu-id="4f9a1-114">The match criteria are evaluated for the originating entries as accounting distributions.</span></span> 

<span data-ttu-id="4f9a1-115">Op de pagina **Boekdefinities** kunt u ook prioriteitsnummers toewijzen aan invoerregels om de volgorde te bepalen waarin de regels worden geëvalueerd.</span><span class="sxs-lookup"><span data-stu-id="4f9a1-115">On the **Posting definitions** page, you can also assign priority numbers to entry lines to control the order in which the lines are evaluated.</span></span> <span data-ttu-id="4f9a1-116">De regels met het laagste prioriteitsnummer worden eerst geëvalueerd.</span><span class="sxs-lookup"><span data-stu-id="4f9a1-116">The lines that have the lowest priority number are evaluated first.</span></span> <span data-ttu-id="4f9a1-117">Alle regels met prioriteit 1 worden bijvoorbeeld geëvalueerd, vervolgens regels met prioriteit 2, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="4f9a1-117">For example, all lines that have a priority of 1 are evaluated, and then lines that have a priority of 2, and so on.</span></span> <span data-ttu-id="4f9a1-118">Wanneer een match wordt gevonden, worden de andere matchcriteria genegeerd.</span><span class="sxs-lookup"><span data-stu-id="4f9a1-118">When a match is found, the other match criteria are ignored.</span></span> <span data-ttu-id="4f9a1-119">Bovendien maken alleen de criteria in de groep die overeenkomt met de oorspronkelijke transactie gegenereerde vermeldingen.</span><span class="sxs-lookup"><span data-stu-id="4f9a1-119">Additionally, only the criteria in the group that match the originating transaction create generated entries.</span></span> 

<span data-ttu-id="4f9a1-120">U kunt uw boekdefinities valideren met behulp van de wizard **Boekdefinitie testen**.</span><span class="sxs-lookup"><span data-stu-id="4f9a1-120">You can validate your posting definitions by using the **Test posting definition** wizard.</span></span> <span data-ttu-id="4f9a1-121">Nadat u een oorspronkelijke vermelding voor een boekdefinitie hebt gedefinieerd, ziet u de gegenereerde vermeldingen.</span><span class="sxs-lookup"><span data-stu-id="4f9a1-121">After you define a sample originating entry for a posting definition, you'll see the generated entries.</span></span> 

<span data-ttu-id="4f9a1-122">U kunt boekdefinitieversies samen met ingangsdatums gebruiken.</span><span class="sxs-lookup"><span data-stu-id="4f9a1-122">You can use posting definition versions together with effective dates.</span></span> <span data-ttu-id="4f9a1-123">U kunt bijvoorbeeld een toekomstige versie maken van een boekingsdefinitie die in een nieuw boekjaar naar een andere grootboekrekening moet worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="4f9a1-123">For example, you can create a future version of a posting definition to post to a different ledger account in a new fiscal year.</span></span> 

<span data-ttu-id="4f9a1-124">Gebruik de pagina **Boekdefinities voor transacties** om boekdefinities toe te wijzen aan transactietypen.</span><span class="sxs-lookup"><span data-stu-id="4f9a1-124">Use the **Transaction posting definitions** page to assign posting definitions to transaction types.</span></span>

## <a name="linking-posting-definitions"></a><span data-ttu-id="4f9a1-125">Boekdefinities koppelen</span><span class="sxs-lookup"><span data-stu-id="4f9a1-125">Linking posting definitions</span></span>
<span data-ttu-id="4f9a1-126">U kunt van een boekingsdefinities naar een andere koppelen wanneer u boekingsdefinities maakt.</span><span class="sxs-lookup"><span data-stu-id="4f9a1-126">You can link from one posting definition to another when you create posting definitions.</span></span> <span data-ttu-id="4f9a1-127">Met de criteria voor de definitie waarmee u hebt gekoppeld, wordt vervolgens rekening gehouden naast de criteria voor de huidige boekdefinitie.</span><span class="sxs-lookup"><span data-stu-id="4f9a1-127">The criteria for the definition that you linked to are then considered in addition to the criteria for the current posting definition.</span></span> <span data-ttu-id="4f9a1-128">Deze functie bespaart u tijd, omdat u criteria niet opnieuw hoeft in te voeren op het sneltabblad **Vermeldingen** op de pagina **Boekdefinities** voor de huidige boekdefinitie als u deze regels al voor een andere definitie hebt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="4f9a1-128">This feature helps save you time, because you don't have to reenter criteria on the **Entries** FastTab on the **Posting definitions** page for the current posting definition if you already entered those lines for another definition.</span></span> 

<span data-ttu-id="4f9a1-129">Vermeld alle koppelingen die u wellicht gebruikt in de diagrammen of tabellen.</span><span class="sxs-lookup"><span data-stu-id="4f9a1-129">In the diagrams or tables, include any links that you might use.</span></span> <span data-ttu-id="4f9a1-130">Zorg ervoor dat de regels in alle boekdefinities waarnaar u koppelt, uniek zijn om conflicten met de huidige boekdefinitie te voorkomen.</span><span class="sxs-lookup"><span data-stu-id="4f9a1-130">To avoid conflicts with the current posting definition, make sure that the lines in any posting definitions that you link to are unique.</span></span> 

<span data-ttu-id="4f9a1-131">De volgende beperkingen gelden wanneer u koppelingen maakt in boekingsdefinities.</span><span class="sxs-lookup"><span data-stu-id="4f9a1-131">The following restrictions apply when you create links in posting definitions:</span></span>

-   <span data-ttu-id="4f9a1-132">Een bepaalde boekdefinitie kan een koppeling zijn naar een andere boekdefinitie of er kan naar worden gekoppeld via een andere boekdefinitie, maar niet beide.</span><span class="sxs-lookup"><span data-stu-id="4f9a1-132">A given posting definition can either link to another posting definition or be linked to from another posting definition, but not both.</span></span> <span data-ttu-id="4f9a1-133">Een boekdefinitie kan echter met meerdere boekdefinities worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="4f9a1-133">However, a posting definition can link to multiple posting definitions.</span></span>
-   <span data-ttu-id="4f9a1-134">U kunt uitsluitend koppelingen instellen tussen boekingsdefinities in dezelfde module.</span><span class="sxs-lookup"><span data-stu-id="4f9a1-134">You can set up links only among posting definitions that are in the same module.</span></span>
-   <span data-ttu-id="4f9a1-135">U kunt een boekingsdefinitie toewijzen aan ieder transactietype, maar het transactietype moet zich in dezelfde module bevinden als de boekingsdefinitie.</span><span class="sxs-lookup"><span data-stu-id="4f9a1-135">You can assign a posting definition to any transaction type, but the transaction type must be in the same module as the posting definition.</span></span> <span data-ttu-id="4f9a1-136">Gebruik de pagina **Boekdefinities voor transacties** om te zien in welke module een transactietype zich bevindt.</span><span class="sxs-lookup"><span data-stu-id="4f9a1-136">Use the **Transaction posting definitions** page to see what module a transaction type is in.</span></span>


<span data-ttu-id="4f9a1-137">Zie voor meer informatie [Voorbeelden van boekingsdefinities](example-posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="4f9a1-137">For more information, see [Posting definitions examples](example-posting-definitions.md).</span></span> 



