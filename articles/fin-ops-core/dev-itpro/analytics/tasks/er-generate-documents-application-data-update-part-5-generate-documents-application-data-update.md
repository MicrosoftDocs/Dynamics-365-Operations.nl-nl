---
title: Documenten genereren die toepassingsgegevens bevatten
description: "Als u de stappen in deze procedure wilt voltooien, moet u eerst de procedure 'ER Documenten genereren met update van toepassingsgegevens (deel 4: Indeling wijzigen)' voltooien."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6af7113031fd77a0a7e06ec23a149a3fa7ad0012
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026058"
---
# <a name="generate-documents-that-have-application-data"></a><span data-ttu-id="694d5-103">Documenten genereren die toepassingsgegevens bevatten</span><span class="sxs-lookup"><span data-stu-id="694d5-103">Generate documents that have application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="694d5-104">Als u de stappen in deze procedure wilt voltooien, moet u eerst de procedure 'ER Documenten genereren met update van toepassingsgegevens (deel 4: indeling wijzigen)' voltooien.</span><span class="sxs-lookup"><span data-stu-id="694d5-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 4: Modify format)”.</span></span>



<span data-ttu-id="694d5-105">De stappen in deze procedure leggen uit hoe u ER-configuraties ontwerpt om een elektronisch document te genereren en toepassingsgegevens bij te werken.</span><span class="sxs-lookup"><span data-stu-id="694d5-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="694d5-106">In deze procedure voert u de ER-indelingsconfiguratie uit om het Intrastat-rapport genereren en toepassingsgegevens bij te werken voor het archiveren van details van het rapportageproces.</span><span class="sxs-lookup"><span data-stu-id="694d5-106">In this procedure, you execute the ER format configuration to generate the Intrastat report and update application data for archiving details of the reporting process.</span></span>



<span data-ttu-id="694d5-107">Deze procedure is gemaakt voor gebruikers met de toegewezen rol van systeembeheerder of elektronische aangifteontwikkelaar.</span><span class="sxs-lookup"><span data-stu-id="694d5-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="694d5-108">Deze stappen kunnen worden voltooid met de DEMF-gegevensset.</span><span class="sxs-lookup"><span data-stu-id="694d5-108">These steps can be completed using the DEMF dataset.</span></span> <span data-ttu-id="694d5-109">Zorg voordat u begint dat de context van het land/de regio voor het DEMF-bedrijf BEL (België) is.</span><span class="sxs-lookup"><span data-stu-id="694d5-109">Before you begin, make sure that the country context for the DEMF company is BEL (Belgium).</span></span>


## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="694d5-110">Parameters voor buitenlandse handel instellen</span><span class="sxs-lookup"><span data-stu-id="694d5-110">Set up foreign trade parameters</span></span>
1. <span data-ttu-id="694d5-111">Ga naar Belasting > Instellen > Buitenlandse handel > Parameters buitenlandse handel.</span><span class="sxs-lookup"><span data-stu-id="694d5-111">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="694d5-112">Klik op het tabblad Nummerreeksen.</span><span class="sxs-lookup"><span data-stu-id="694d5-112">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="694d5-113">Bij het archiveren van details van het Intrastat-rapportageproces moeten we records identificeren van elk archief dat we hebben gemaakt.</span><span class="sxs-lookup"><span data-stu-id="694d5-113">Archiving details of Intrastat reporting process, we need to identify records of each archive we created.</span></span> <span data-ttu-id="694d5-114">Daarvoor moet een speciale nummerreeks worden geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="694d5-114">A special number sequence must be configured for that.</span></span>  
3. <span data-ttu-id="694d5-115">Selecteer de verwijzing 'Intrastat-archief-id'.</span><span class="sxs-lookup"><span data-stu-id="694d5-115">Select the ‘Intrastat archive ID’ reference.</span></span>
4. <span data-ttu-id="694d5-116">Typ een waarde in het veld Nummerreekscode.</span><span class="sxs-lookup"><span data-stu-id="694d5-116">In the Number sequence code field, type a value.</span></span>
    * <span data-ttu-id="694d5-117">Typ of selecteer de waarde 'Fore_2' in het veld 'Nummerreekscode'.</span><span class="sxs-lookup"><span data-stu-id="694d5-117">In the ‘Number sequence code’ field, enter or select the value ‘Fore_2’.</span></span>  
5. <span data-ttu-id="694d5-118">ResolveChanges de nummerreekscode.</span><span class="sxs-lookup"><span data-stu-id="694d5-118">ResolveChanges the Number sequence code.</span></span>
6. <span data-ttu-id="694d5-119">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="694d5-119">Click Save.</span></span>
7. <span data-ttu-id="694d5-120">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="694d5-120">Close the page.</span></span>

## <a name="run-modified-er-format"></a><span data-ttu-id="694d5-121">Gewijzigde ER-indeling uitvoeren</span><span class="sxs-lookup"><span data-stu-id="694d5-121">Run modified ER format</span></span>
1. <span data-ttu-id="694d5-122">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="694d5-122">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="694d5-123">Vouw in de structuur 'Intrastat (model)' uit.</span><span class="sxs-lookup"><span data-stu-id="694d5-123">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="694d5-124">Selecteer in de structuur 'Intrastat (model)\Intrastat (indeling)'.</span><span class="sxs-lookup"><span data-stu-id="694d5-124">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="694d5-125">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="694d5-125">Click Run.</span></span>
5. <span data-ttu-id="694d5-126">Typ in het veld Invoeren 'intrastat2.xml'.</span><span class="sxs-lookup"><span data-stu-id="694d5-126">In the Enter file name field, type 'intrastat2.xml'.</span></span>
    * <span data-ttu-id="694d5-127">intrastat2.xml</span><span class="sxs-lookup"><span data-stu-id="694d5-127">intrastat2.xml</span></span>  
6. <span data-ttu-id="694d5-128">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="694d5-128">Click OK.</span></span>

## <a name="review-er-format-executions-results"></a><span data-ttu-id="694d5-129">Resultaten van uitvoering van ER-indeling</span><span class="sxs-lookup"><span data-stu-id="694d5-129">Review ER format execution’s results</span></span>
<span data-ttu-id="694d5-130">Bekijk het gegenereerde XML-bestand.</span><span class="sxs-lookup"><span data-stu-id="694d5-130">Review the generated XML file.</span></span>  
1. <span data-ttu-id="694d5-131">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="694d5-131">Close the page.</span></span>
2. <span data-ttu-id="694d5-132">Ga naar Belasting > Aangiften > Buitenlandse handel > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="694d5-132">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="694d5-133">Open dit formulier met Intrastat-transacties die zijn opgenomen in het gegenereerde elektronische document.</span><span class="sxs-lookup"><span data-stu-id="694d5-133">Open this form containing Intrastat transactions that have been included to the generated electronic document.</span></span>  
3. <span data-ttu-id="694d5-134">Klik op Intrastat-archief.</span><span class="sxs-lookup"><span data-stu-id="694d5-134">Click Intrastat archive.</span></span>
    * <span data-ttu-id="694d5-135">Omdat de uitgevoerde ER-indeling nu instellingen bevat voor het bijwerken van toepassingsgegevens, zijn de details van de voltooide Intrastat-rapportage gearchiveerd.</span><span class="sxs-lookup"><span data-stu-id="694d5-135">Since the executed ER format contains now settings for application data update, the details of the completed Intrastat reporting have been archived.</span></span> <span data-ttu-id="694d5-136">In dit formulier ziet u de koptekstrecord van het gemaakte archief.</span><span class="sxs-lookup"><span data-stu-id="694d5-136">In this form, you can see the header record of the created archive.</span></span>  
4. <span data-ttu-id="694d5-137">Klik op Details.</span><span class="sxs-lookup"><span data-stu-id="694d5-137">Click Details.</span></span>
    * <span data-ttu-id="694d5-138">In dit formulier ziet u de details van het gemaakte archief.</span><span class="sxs-lookup"><span data-stu-id="694d5-138">In this form, you can see the details for the created archive.</span></span>  
5. <span data-ttu-id="694d5-139">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="694d5-139">Close the page.</span></span>
6. <span data-ttu-id="694d5-140">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="694d5-140">Close the page.</span></span>
7. <span data-ttu-id="694d5-141">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="694d5-141">Close the page.</span></span>

