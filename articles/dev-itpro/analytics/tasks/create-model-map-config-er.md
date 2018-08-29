--- 
title: Configuraties voor toewijzing van model voor elektronische rapportage (ER) maken
description: "Gebruik deze procedure voor het ontwerpen van een nieuwe ER-modeltoewijzingsconfiguratie (elektronische aangifte) en pas de ingebouwde ER-functies toe voor efficiënte statistische berekeningen."
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 614ef06fcf5761f1cf2afb6e7655558d2858d763
ms.contentlocale: nl-nl
ms.lasthandoff: 08/08/2018

---
# <a name="create-electronic-reporting-er-model-mapping-configurations"></a><span data-ttu-id="26c1b-103">Configuraties voor toewijzing van model voor elektronische rapportage (ER) maken</span><span class="sxs-lookup"><span data-stu-id="26c1b-103">Create Electronic reporting (ER) model mapping configurations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="26c1b-104">Gebruik deze procedure voor het ontwerpen van een nieuwe ER-modeltoewijzingsconfiguratie (elektronische aangifte) en pas de ingebouwde ER-functies toe voor efficiënte statistische berekeningen.</span><span class="sxs-lookup"><span data-stu-id="26c1b-104">Use this procedure to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="26c1b-105">In deze procedure maakt u een configuratie voor voorbeeldbedrijf Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="26c1b-105">In this procedure, you will create a configuration for sample company, Litware, Inc.</span></span> 

<span data-ttu-id="26c1b-106">Deze procedure is gemaakt voor gebruikers met de toegewezen rol van Systeembeheerder of Elektronische aangifteontwikkelaar.</span><span class="sxs-lookup"><span data-stu-id="26c1b-106">This procedure is created for uses with the assigned role of System administrator or Electronic reporting developer.</span></span>

<span data-ttu-id="26c1b-107">Deze stappen kunnen worden voltooid met elke dataset.</span><span class="sxs-lookup"><span data-stu-id="26c1b-107">These steps can be completed using any dataset.</span></span> <span data-ttu-id="26c1b-108">Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.</span><span class="sxs-lookup"><span data-stu-id="26c1b-108">To complete these steps, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active.”</span></span>

1. <span data-ttu-id="26c1b-109">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="26c1b-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="26c1b-110">Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als Actief.</span><span class="sxs-lookup"><span data-stu-id="26c1b-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="26c1b-111">Als u deze configuratieprovider niet ziet, voert u eerst de stappen uit in de procedure 'Een configuratieprovider maken en deze als actief markeren'.</span><span class="sxs-lookup"><span data-stu-id="26c1b-111">If you don’t see this configuration provider, complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>  
2. <span data-ttu-id="26c1b-112">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="26c1b-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="26c1b-113">Klik op Filters weergeven.</span><span class="sxs-lookup"><span data-stu-id="26c1b-113">Click Show filters.</span></span>
4. <span data-ttu-id="26c1b-114">Typ de filterwaarde 'Intrastat' in het veld Naam en gebruik de filteroperator 'begint met'.</span><span class="sxs-lookup"><span data-stu-id="26c1b-114">In the "Name" field, enter the filter value, "Intrastat" and use the filter operator "begins with".</span></span>
    * <span data-ttu-id="26c1b-115">Pas dit filter toe om de configuratie van het 'Intrastat'-gegevensmodel te vinden.</span><span class="sxs-lookup"><span data-stu-id="26c1b-115">Apply this filter to find the ‘Intrastat’ data model configuration.</span></span> <span data-ttu-id="26c1b-116">Dit model bestaat mogelijk al in de configuratiestructuur.</span><span class="sxs-lookup"><span data-stu-id="26c1b-116">This model may already exist in the configurations tree.</span></span> <span data-ttu-id="26c1b-117">Als dit het geval is, gaat u naar de volgende subtaak.</span><span class="sxs-lookup"><span data-stu-id="26c1b-117">If it does, skip the next sub-task.</span></span>   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a><span data-ttu-id="26c1b-118">Intrastat-modelconfiguratie ophalen die door Microsoft wordt geleverd</span><span class="sxs-lookup"><span data-stu-id="26c1b-118">Get the Intrastat model configuration provided by Microsoft</span></span>
1. <span data-ttu-id="26c1b-119">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="26c1b-119">Close the page.</span></span>
2. <span data-ttu-id="26c1b-120">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="26c1b-120">Close the page.</span></span>
3. <span data-ttu-id="26c1b-121">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="26c1b-121">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
4. <span data-ttu-id="26c1b-122">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="26c1b-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="26c1b-123">Selecteer de Microsoft-providertegel.</span><span class="sxs-lookup"><span data-stu-id="26c1b-123">Select the Microsoft provider tile.</span></span>  
5. <span data-ttu-id="26c1b-124">Klik op Opslagplaatsen.</span><span class="sxs-lookup"><span data-stu-id="26c1b-124">Click Repositories.</span></span>
    * <span data-ttu-id="26c1b-125">Klik op de Microsoft-providertegel op Opslagplaatsen.</span><span class="sxs-lookup"><span data-stu-id="26c1b-125">Click Repositories in the Microsoft provider tile.</span></span>  
6. <span data-ttu-id="26c1b-126">Klik op Filters weergeven.</span><span class="sxs-lookup"><span data-stu-id="26c1b-126">Click Show filters.</span></span>
7. <span data-ttu-id="26c1b-127">Typ de filterwaarde 'resources' in het veld Naam en gebruik de filteroperator 'bevat'.</span><span class="sxs-lookup"><span data-stu-id="26c1b-127">In the "Type name" field, enter the filter value, “resources” and use the filter operator "contains".</span></span> 
8. <span data-ttu-id="26c1b-128">Klik op Openen.</span><span class="sxs-lookup"><span data-stu-id="26c1b-128">Click Open.</span></span>
9. <span data-ttu-id="26c1b-129">Selecteer in de structuur 'Intrastatmodel'.</span><span class="sxs-lookup"><span data-stu-id="26c1b-129">In the tree, select 'Intrastat model'.</span></span>
10. <span data-ttu-id="26c1b-130">Klik op Importeren.</span><span class="sxs-lookup"><span data-stu-id="26c1b-130">Click Import.</span></span>
11. <span data-ttu-id="26c1b-131">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="26c1b-131">Click Yes.</span></span>
    * <span data-ttu-id="26c1b-132">U hebt de ER-modelconfiguratie geïmporteerd die het gegevensmodel bevat die u wilt gebruiken om te onderzoeken hoe de nieuwe ER-functionaliteit kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="26c1b-132">You imported the ER model configuration that contains the data model that you will use to explore how the new ER functionality can be used.</span></span>  
12. <span data-ttu-id="26c1b-133">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="26c1b-133">Close the page.</span></span>
13. <span data-ttu-id="26c1b-134">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="26c1b-134">Close the page.</span></span>
14. <span data-ttu-id="26c1b-135">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="26c1b-135">Click Reporting configurations.</span></span>

## <a name="add-a-new-model-mapping-configuration"></a><span data-ttu-id="26c1b-136">Een nieuwe modeltoewijzingsconfiguratie toevoegen</span><span class="sxs-lookup"><span data-stu-id="26c1b-136">Add a new model mapping configuration</span></span>
1. <span data-ttu-id="26c1b-137">Selecteer in de structuur 'Intrastatmodel'.</span><span class="sxs-lookup"><span data-stu-id="26c1b-137">In the tree, select 'Intrastat model'.</span></span>
2. <span data-ttu-id="26c1b-138">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="26c1b-138">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="26c1b-139">Typ in het veld Nieuw 'Modeltoewijzing gebaseerd op het Intrastatmodel'.</span><span class="sxs-lookup"><span data-stu-id="26c1b-139">In the New field, enter 'Model Mapping based on data model Intrastat'.</span></span>
4. <span data-ttu-id="26c1b-140">Typ 'Voorbeeldtoewijzing Intrastat' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="26c1b-140">In the Name field, type 'Intrastat sample mapping'.</span></span>
    * <span data-ttu-id="26c1b-141">Voorbeeldtoewijzing van Intrastat</span><span class="sxs-lookup"><span data-stu-id="26c1b-141">Intrastat sample mapping</span></span>  
5. <span data-ttu-id="26c1b-142">Klik op Configuratie maken.</span><span class="sxs-lookup"><span data-stu-id="26c1b-142">Click Create configuration.</span></span>


