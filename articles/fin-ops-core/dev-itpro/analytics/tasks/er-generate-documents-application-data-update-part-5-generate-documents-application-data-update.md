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
ms.openlocfilehash: 759869577ef30cd3f81eb74103a93cc5d1a3d608
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042845"
---
# <a name="generate-documents-that-have-application-data"></a><span data-ttu-id="7988a-103">Documenten genereren die toepassingsgegevens bevatten</span><span class="sxs-lookup"><span data-stu-id="7988a-103">Generate documents that have application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7988a-104">Als u de stappen in deze procedure wilt voltooien, moet u eerst de procedure 'ER Documenten genereren met update van toepassingsgegevens (deel 4: indeling wijzigen)' voltooien.</span><span class="sxs-lookup"><span data-stu-id="7988a-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 4: Modify format)”.</span></span>



<span data-ttu-id="7988a-105">De stappen in deze procedure leggen uit hoe u ER-configuraties ontwerpt om een elektronisch document te genereren en toepassingsgegevens bij te werken.</span><span class="sxs-lookup"><span data-stu-id="7988a-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="7988a-106">In deze procedure voert u de ER-indelingsconfiguratie uit om het Intrastat-rapport genereren en toepassingsgegevens bij te werken voor het archiveren van details van het rapportageproces.</span><span class="sxs-lookup"><span data-stu-id="7988a-106">In this procedure, you execute the ER format configuration to generate the Intrastat report and update application data for archiving details of the reporting process.</span></span>



<span data-ttu-id="7988a-107">Deze procedure is gemaakt voor gebruikers met de toegewezen rol van systeembeheerder of elektronische aangifteontwikkelaar.</span><span class="sxs-lookup"><span data-stu-id="7988a-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="7988a-108">Deze stappen kunnen worden voltooid met de DEMF-gegevensset.</span><span class="sxs-lookup"><span data-stu-id="7988a-108">These steps can be completed using the DEMF dataset.</span></span> <span data-ttu-id="7988a-109">Zorg voordat u begint dat de context van het land/de regio voor het DEMF-bedrijf BEL (België) is.</span><span class="sxs-lookup"><span data-stu-id="7988a-109">Before you begin, make sure that the country context for the DEMF company is BEL (Belgium).</span></span>


## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="7988a-110">Parameters voor buitenlandse handel instellen</span><span class="sxs-lookup"><span data-stu-id="7988a-110">Set up foreign trade parameters</span></span>
1. <span data-ttu-id="7988a-111">Ga naar Belasting > Instellen > Buitenlandse handel > Parameters buitenlandse handel.</span><span class="sxs-lookup"><span data-stu-id="7988a-111">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="7988a-112">Klik op het tabblad Nummerreeksen.</span><span class="sxs-lookup"><span data-stu-id="7988a-112">Click the Number sequences tab.</span></span>

    <span data-ttu-id="7988a-113">Bij het archiveren van details van het Intrastat-rapportageproces moeten we records identificeren van elk archief dat we hebben gemaakt.</span><span class="sxs-lookup"><span data-stu-id="7988a-113">Archiving details of Intrastat reporting process, we need to identify records of each archive we created.</span></span> <span data-ttu-id="7988a-114">Daarvoor moet een speciale nummerreeks worden geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="7988a-114">A special number sequence must be configured for that.</span></span>  

3. <span data-ttu-id="7988a-115">Selecteer de verwijzing 'Intrastat-archief-id'.</span><span class="sxs-lookup"><span data-stu-id="7988a-115">Select the ‘Intrastat archive ID’ reference.</span></span>
4. <span data-ttu-id="7988a-116">Typ een waarde in het veld Nummerreekscode.</span><span class="sxs-lookup"><span data-stu-id="7988a-116">In the Number sequence code field, type a value.</span></span>

    <span data-ttu-id="7988a-117">Typ of selecteer de waarde 'Fore_2' in het veld 'Nummerreekscode'.</span><span class="sxs-lookup"><span data-stu-id="7988a-117">In the ‘Number sequence code’ field, enter or select the value ‘Fore_2’.</span></span>  

5. <span data-ttu-id="7988a-118">ResolveChanges de nummerreekscode.</span><span class="sxs-lookup"><span data-stu-id="7988a-118">ResolveChanges the Number sequence code.</span></span>
6. <span data-ttu-id="7988a-119">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="7988a-119">Click Save.</span></span>
7. <span data-ttu-id="7988a-120">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="7988a-120">Close the page.</span></span>

## <a name="run-modified-er-format"></a><span data-ttu-id="7988a-121">Gewijzigde ER-indeling uitvoeren</span><span class="sxs-lookup"><span data-stu-id="7988a-121">Run modified ER format</span></span>
1. <span data-ttu-id="7988a-122">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="7988a-122">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="7988a-123">Vouw in de structuur 'Intrastat (model)' uit.</span><span class="sxs-lookup"><span data-stu-id="7988a-123">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="7988a-124">Selecteer in de structuur 'Intrastat (model)\Intrastat (indeling)'.</span><span class="sxs-lookup"><span data-stu-id="7988a-124">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="7988a-125">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="7988a-125">Click Run.</span></span>
5. <span data-ttu-id="7988a-126">Typ in het veld Invoeren 'intrastat2.xml'.</span><span class="sxs-lookup"><span data-stu-id="7988a-126">In the Enter file name field, type 'intrastat2.xml'.</span></span>
6. <span data-ttu-id="7988a-127">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="7988a-127">Click OK.</span></span>

## <a name="review-er-format-executions-results"></a><span data-ttu-id="7988a-128">Resultaten van uitvoering van ER-indeling</span><span class="sxs-lookup"><span data-stu-id="7988a-128">Review ER format execution’s results</span></span>
<span data-ttu-id="7988a-129">Bekijk het gegenereerde XML-bestand.</span><span class="sxs-lookup"><span data-stu-id="7988a-129">Review the generated XML file.</span></span>  
1. <span data-ttu-id="7988a-130">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="7988a-130">Close the page.</span></span>
2. <span data-ttu-id="7988a-131">Ga naar Belasting > Aangiften > Buitenlandse handel > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="7988a-131">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>

    <span data-ttu-id="7988a-132">Open dit formulier met Intrastat-transacties die zijn opgenomen in het gegenereerde elektronische document.</span><span class="sxs-lookup"><span data-stu-id="7988a-132">Open this form containing Intrastat transactions that have been included to the generated electronic document.</span></span>  

3. <span data-ttu-id="7988a-133">Klik op Intrastat-archief.</span><span class="sxs-lookup"><span data-stu-id="7988a-133">Click Intrastat archive.</span></span>

    <span data-ttu-id="7988a-134">Omdat de uitgevoerde ER-indeling nu instellingen bevat voor het bijwerken van toepassingsgegevens, zijn de details van de voltooide Intrastat-rapportage gearchiveerd.</span><span class="sxs-lookup"><span data-stu-id="7988a-134">Since the executed ER format contains now settings for application data update, the details of the completed Intrastat reporting have been archived.</span></span> <span data-ttu-id="7988a-135">In dit formulier ziet u de koptekstrecord van het gemaakte archief.</span><span class="sxs-lookup"><span data-stu-id="7988a-135">In this form, you can see the header record of the created archive.</span></span>  

4. <span data-ttu-id="7988a-136">Klik op Details.</span><span class="sxs-lookup"><span data-stu-id="7988a-136">Click Details.</span></span>

    <span data-ttu-id="7988a-137">In dit formulier ziet u de details van het gemaakte archief.</span><span class="sxs-lookup"><span data-stu-id="7988a-137">In this form, you can see the details for the created archive.</span></span>  

5. <span data-ttu-id="7988a-138">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="7988a-138">Close the page.</span></span>
6. <span data-ttu-id="7988a-139">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="7988a-139">Close the page.</span></span>
7. <span data-ttu-id="7988a-140">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="7988a-140">Close the page.</span></span>

