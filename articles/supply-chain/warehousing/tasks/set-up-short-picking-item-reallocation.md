---
title: Artikelhertoewijzing voor kort orderverzamelen instellen
description: Deze procedure laat zien hoe magazijnmedewerkers snel andere locaties kunnen vinden als er onvoldoende voorraad is voor de locatie waaraan ze zijn toegewezen.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 964302cb7e7835b6e619602ac7165c9e7adbcefb
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916749"
---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="89621-103">Artikelhertoewijzing voor kort orderverzamelen instellen</span><span class="sxs-lookup"><span data-stu-id="89621-103">Set up short picking item reallocation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="89621-104">Deze procedure laat zien hoe magazijnmedewerkers snel andere locaties kunnen vinden als er onvoldoende voorraad is voor de locatie waaraan ze zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="89621-104">This procedure shows you how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> <span data-ttu-id="89621-105">Het is mogelijk om een automatisch hertoewijzingsproces te gebruiken, dat locatierichtlijnen gebruikt voor het ophalen van de goederen als ze op een andere locatie beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="89621-105">It’s possible to use an automatic re-allocation process, which uses location directives to retrieve the goods if they’re available at another location.</span></span> <span data-ttu-id="89621-106">Ook kan wanneer handmatige hertoewijzing wordt gebruikt, op het mobiele apparaat een lijst met locaties worden weergegeven met de beschikbare hoeveelheid, zodat de magazijnwerknemer de locatie kan kiezen waaruit de voorraad wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="89621-106">Alternatively, when manual re-allocation is used, a list of the locations with the available quantity is shown on the mobile device, allowing the warehouse worker to choose which location to use inventory from.</span></span> <span data-ttu-id="89621-107">U kunt deze procedure gebruiken in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="89621-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="89621-108">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="89621-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-work-exceptions"></a><span data-ttu-id="89621-109">Werkuitzonderingen instellen</span><span class="sxs-lookup"><span data-stu-id="89621-109">Set up work exceptions</span></span>
1. <span data-ttu-id="89621-110">Ga in het **navigatievenster** naar **Magazijnbeheer > Instellingen > Werk >Werkuitzonderingen**.</span><span class="sxs-lookup"><span data-stu-id="89621-110">In the **Navigation pane**, go to **Warehouse management > Setup > Work > Work exceptions**.</span></span>
2. <span data-ttu-id="89621-111">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="89621-111">Click **New**.</span></span> <span data-ttu-id="89621-112">Het is mogelijk om meerdere werkuitzonderingen te definiëren met verschillende beleidsregels voor artikelhertoewijzing zodat de magazijnwerknemer één regel kan kiezen op basis van de vereisten van de zending die wordt verwerkt.</span><span class="sxs-lookup"><span data-stu-id="89621-112">It’s possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>  
3. <span data-ttu-id="89621-113">Typ een waarde in het veld **Werkuitzonderingscode**.</span><span class="sxs-lookup"><span data-stu-id="89621-113">In the **Work exception code** field, type a value.</span></span> <span data-ttu-id="89621-114">Geef de werkuitzondering een titel om aan te geven waarvoor deze wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="89621-114">Give the work exception a title to indicate what it’s used for.</span></span> <span data-ttu-id="89621-115">Bijvoorbeeld Handmatige orderverzameling.</span><span class="sxs-lookup"><span data-stu-id="89621-115">For example, Short picking manual.</span></span>  
4. <span data-ttu-id="89621-116">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="89621-116">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="89621-117">Selecteer Korte verzameling in het veld **Type uitzondering**.</span><span class="sxs-lookup"><span data-stu-id="89621-117">In the **Exception** type field, select 'Short pick'.</span></span>
6. <span data-ttu-id="89621-118">Schakel het selectievakje **Voorraad aanpassen** in.</span><span class="sxs-lookup"><span data-stu-id="89621-118">Select the **Adjust inventory** check box.</span></span> <span data-ttu-id="89621-119">Deze optie betekent dat de voorraad automatisch tot 0 wordt aangepast op de locatie voor orderverzameling.</span><span class="sxs-lookup"><span data-stu-id="89621-119">This option means that inventory will automatically be adjusted to 0 at the short picked location.</span></span>  
7. <span data-ttu-id="89621-120">Typ of selecteer een waarde in het veld **Standaard correctietypecode**.</span><span class="sxs-lookup"><span data-stu-id="89621-120">In the **Default adjustment type code** field, enter or select a value.</span></span> <span data-ttu-id="89621-121">Selecteer in USMF bijvoorbeeld Res Adj Out verwijderen.</span><span class="sxs-lookup"><span data-stu-id="89621-121">For example, in USMF you can select 'Remove Res Adj Out'.</span></span>  
8. <span data-ttu-id="89621-122">Selecteer Handmatig in het veld **Artikelhertoewijzing**.</span><span class="sxs-lookup"><span data-stu-id="89621-122">In the **Item reallocation** field, select 'Manual'.</span></span> <span data-ttu-id="89621-123">Als u Handmatig of Automatisch en handmatig selecteert, moet de magazijnwerknemer in staat zijn om handmatige hertoewijzing te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="89621-123">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="89621-124">Een werknemer instellen om handmatige artikelhertoewijzing te gebruiken</span><span class="sxs-lookup"><span data-stu-id="89621-124">Set up a worker to use manual item reallocation</span></span>
1. <span data-ttu-id="89621-125">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="89621-125">Close the page.</span></span>
2. <span data-ttu-id="89621-126">Ga in het **navigatievenster** naar **Magazijnbeheer > Instellingen > Medewerker**.</span><span class="sxs-lookup"><span data-stu-id="89621-126">In the **Navigation pane**, go to **Warehouse management > Setup > Worker**.</span></span>
3. <span data-ttu-id="89621-127">Klik op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="89621-127">Click **Edit**.</span></span>
4. <span data-ttu-id="89621-128">Selecteer medewerker 24 in de lijst.</span><span class="sxs-lookup"><span data-stu-id="89621-128">In the list, select worker 24.</span></span>
5. <span data-ttu-id="89621-129">Vouw het sneltabblad **Werk** uit.</span><span class="sxs-lookup"><span data-stu-id="89621-129">Expand the **Work** fastTab.</span></span>
6. <span data-ttu-id="89621-130">Selecteer Ja in het veld **Handmatige artikelhertoewijzing toestaan**.</span><span class="sxs-lookup"><span data-stu-id="89621-130">Select 'Yes' in the **Allow manual item reallocation** field.</span></span>

