---
title: ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (deel 4 - Indeling uitvoeren)
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken met de documentbeheerbestanden in ER-uitvoer.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f5639a46c105e735d028e903513b4fcfb1f0d968
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142611"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4---run-format"></a><span data-ttu-id="ffa7d-103">ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (deel 4 - Indeling uitvoeren)</span><span class="sxs-lookup"><span data-stu-id="ffa7d-103">ER Use Document Management files in format outputs (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ffa7d-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken met de Documentbeheerbestanden (bijlagen) in ER-uitvoer.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="ffa7d-105">Deze stappen kunnen in het DEMF-bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="ffa7d-106">Als u deze stappen wilt uitvoeren, voert u eerst de stappen uit in de procedure "ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (Deel 3: Indeling maken)".</span><span class="sxs-lookup"><span data-stu-id="ffa7d-106">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 3: Create format)" procedure.</span></span>

<span data-ttu-id="ffa7d-107">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="ffa7d-108">Vereiste bijlagen toevoegen voor een verkooporder van één factuur</span><span class="sxs-lookup"><span data-stu-id="ffa7d-108">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="ffa7d-109">Ga naar Klanten > Facturen > Openstaande klantfacturen.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-109">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="ffa7d-110">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ffa7d-111">Filter bijvoorbeeld op het veld Factuur met de waarde 'CIV-000148'.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-111">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="ffa7d-112">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="ffa7d-112">CIV-000148</span></span>  
3. <span data-ttu-id="ffa7d-113">Klik om de koppeling van de geselecteerde factuur te volgen.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-113">Click to follow the selected invoice's link.</span></span>
    * <span data-ttu-id="ffa7d-114">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="ffa7d-114">CIV-000148</span></span>  
4. <span data-ttu-id="ffa7d-115">Klik om de koppeling in het veld Verkooporder te volgen.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-115">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="ffa7d-116">000148</span><span class="sxs-lookup"><span data-stu-id="ffa7d-116">000148</span></span>  
5. <span data-ttu-id="ffa7d-117">Selecteer in het veld Regels of koptekst de optie Koptekst.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-117">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="ffa7d-118">Koptekst selecteren om aan te geven dat dit het doel voor het toevoegen van bijlagen is.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-118">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="ffa7d-119">Klik op Koppelen.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-119">Click Attach.</span></span>
    * <span data-ttu-id="ffa7d-120">Voeg een paar bestanden als bijlagen voor deze verkooporder toe.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-120">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="ffa7d-121">Gebruik de bestanden van de documenttypen die worden ondersteund door Documentbeheer (met bestandextensies DOCX, DPF, XML, JPG, enzovoort.).</span><span class="sxs-lookup"><span data-stu-id="ffa7d-121">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="ffa7d-122">Blader en selecteer bestanden die met de bijbehorende factuur in het ER elektronische bericht moeten worden gekoppeld en verwerkt.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-122">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="ffa7d-123">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-123">Click New.</span></span>
8. <span data-ttu-id="ffa7d-124">Klik op Bestand.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-124">Click File.</span></span>
9. <span data-ttu-id="ffa7d-125">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-125">Click New.</span></span>
10. <span data-ttu-id="ffa7d-126">Klik op Bestand.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-126">Click File.</span></span>
11. <span data-ttu-id="ffa7d-127">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-127">Close the page.</span></span>
12. <span data-ttu-id="ffa7d-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-128">Close the page.</span></span>
13. <span data-ttu-id="ffa7d-129">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-129">Close the page.</span></span>
14. <span data-ttu-id="ffa7d-130">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-130">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="ffa7d-131">Het ontworpen rapport uitvoeren voor de geselecteerde factuur</span><span class="sxs-lookup"><span data-stu-id="ffa7d-131">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="ffa7d-132">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-132">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="ffa7d-133">Vouw in de structuur Klantfactuurmodel uit.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-133">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="ffa7d-134">Vouw in de structuur 'Customer invoice model\Customer invoice model (custom)' uit.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-134">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="ffa7d-135">Selecteer in de structuur 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-135">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="ffa7d-136">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-136">Click Run.</span></span>
6. <span data-ttu-id="ffa7d-137">Vouw de records uit zodat de sectie () is opgenomen.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-137">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="ffa7d-138">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-138">Click Filter.</span></span>
8. <span data-ttu-id="ffa7d-139">Selecteer de rij van het Klantfacturenjournaal en het veld Verkooporder.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-139">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="ffa7d-140">Typ 000148 in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-140">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="ffa7d-141">Typ in het criteriaveld "Verkooporder" het ordernummer 000148.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-141">In the criteria "Sales order" field, type the order number 000148.</span></span>  
10. <span data-ttu-id="ffa7d-142">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-142">Click OK.</span></span>
11. <span data-ttu-id="ffa7d-143">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-143">Click OK.</span></span>
    * <span data-ttu-id="ffa7d-144">Controleer de gegenereerde uitvoer.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-144">Review the generated output.</span></span> <span data-ttu-id="ffa7d-145">Merk op dat voor elke bijlage één XML-knooppunt is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-145">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="ffa7d-146">De inhoud van de bijlage is gevuld met de XML-uitvoer in de tekstindeling MIME (base64).</span><span class="sxs-lookup"><span data-stu-id="ffa7d-146">The attachment's content is populated to the XML output in MIME (base64) text format.</span></span>  

