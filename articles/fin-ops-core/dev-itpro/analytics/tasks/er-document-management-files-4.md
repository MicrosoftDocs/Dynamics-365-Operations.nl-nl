---
title: ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (deel 4 - Indeling uitvoeren)
description: In dit onderwerp wordt beschreven hoe u een indeling voor elektronische rapportage configureert om documentbeheerbestanden te gebruiken in ER-uitvoer. (Deel 4)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f7a7c9705d8b53ef13cd3faf13290f3f1b1d1c43
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749112"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4---run-format"></a><span data-ttu-id="ae51e-104">ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (deel 4 - Indeling uitvoeren)</span><span class="sxs-lookup"><span data-stu-id="ae51e-104">ER Use Document Management files in format outputs (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ae51e-105">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken met de Documentbeheerbestanden (bijlagen) in ER-uitvoer.</span><span class="sxs-lookup"><span data-stu-id="ae51e-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="ae51e-106">Deze stappen kunnen in het DEMF-bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="ae51e-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="ae51e-107">Als u deze stappen wilt uitvoeren, voert u eerst de stappen uit in de procedure "ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (Deel 3: Indeling maken)".</span><span class="sxs-lookup"><span data-stu-id="ae51e-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 3: Create format)" procedure.</span></span>

<span data-ttu-id="ae51e-108">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="ae51e-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="ae51e-109">Vereiste bijlagen toevoegen voor een verkooporder van één factuur</span><span class="sxs-lookup"><span data-stu-id="ae51e-109">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="ae51e-110">Ga naar Klanten > Facturen > Openstaande klantfacturen.</span><span class="sxs-lookup"><span data-stu-id="ae51e-110">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="ae51e-111">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="ae51e-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ae51e-112">Filter bijvoorbeeld op het veld Factuur met de waarde 'CIV-000148'.</span><span class="sxs-lookup"><span data-stu-id="ae51e-112">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="ae51e-113">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="ae51e-113">CIV-000148</span></span>  
3. <span data-ttu-id="ae51e-114">Klik om de koppeling van de geselecteerde factuur te volgen.</span><span class="sxs-lookup"><span data-stu-id="ae51e-114">Click to follow the selected invoice's link.</span></span>
    * <span data-ttu-id="ae51e-115">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="ae51e-115">CIV-000148</span></span>  
4. <span data-ttu-id="ae51e-116">Klik om de koppeling in het veld Verkooporder te volgen.</span><span class="sxs-lookup"><span data-stu-id="ae51e-116">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="ae51e-117">000148</span><span class="sxs-lookup"><span data-stu-id="ae51e-117">000148</span></span>  
5. <span data-ttu-id="ae51e-118">Selecteer in het veld Regels of koptekst de optie Koptekst.</span><span class="sxs-lookup"><span data-stu-id="ae51e-118">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="ae51e-119">Koptekst selecteren om aan te geven dat dit het doel voor het toevoegen van bijlagen is.</span><span class="sxs-lookup"><span data-stu-id="ae51e-119">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="ae51e-120">Klik op Koppelen.</span><span class="sxs-lookup"><span data-stu-id="ae51e-120">Click Attach.</span></span>
    * <span data-ttu-id="ae51e-121">Voeg een paar bestanden als bijlagen voor deze verkooporder toe.</span><span class="sxs-lookup"><span data-stu-id="ae51e-121">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="ae51e-122">Gebruik de bestanden van de documenttypen die worden ondersteund door Documentbeheer (met bestandextensies DOCX, DPF, XML, JPG, enzovoort.).</span><span class="sxs-lookup"><span data-stu-id="ae51e-122">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="ae51e-123">Blader en selecteer bestanden die met de bijbehorende factuur in het ER elektronische bericht moeten worden gekoppeld en verwerkt.</span><span class="sxs-lookup"><span data-stu-id="ae51e-123">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="ae51e-124">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="ae51e-124">Click New.</span></span>
8. <span data-ttu-id="ae51e-125">Klik op Bestand.</span><span class="sxs-lookup"><span data-stu-id="ae51e-125">Click File.</span></span>
9. <span data-ttu-id="ae51e-126">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="ae51e-126">Click New.</span></span>
10. <span data-ttu-id="ae51e-127">Klik op Bestand.</span><span class="sxs-lookup"><span data-stu-id="ae51e-127">Click File.</span></span>
11. <span data-ttu-id="ae51e-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ae51e-128">Close the page.</span></span>
12. <span data-ttu-id="ae51e-129">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ae51e-129">Close the page.</span></span>
13. <span data-ttu-id="ae51e-130">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ae51e-130">Close the page.</span></span>
14. <span data-ttu-id="ae51e-131">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ae51e-131">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="ae51e-132">Het ontworpen rapport uitvoeren voor de geselecteerde factuur</span><span class="sxs-lookup"><span data-stu-id="ae51e-132">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="ae51e-133">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="ae51e-133">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="ae51e-134">Vouw in de structuur Klantfactuurmodel uit.</span><span class="sxs-lookup"><span data-stu-id="ae51e-134">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="ae51e-135">Vouw in de structuur 'Customer invoice model\Customer invoice model (custom)' uit.</span><span class="sxs-lookup"><span data-stu-id="ae51e-135">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="ae51e-136">Selecteer in de structuur 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span><span class="sxs-lookup"><span data-stu-id="ae51e-136">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="ae51e-137">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="ae51e-137">Click Run.</span></span>
6. <span data-ttu-id="ae51e-138">Vouw de records uit zodat de sectie () is opgenomen.</span><span class="sxs-lookup"><span data-stu-id="ae51e-138">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="ae51e-139">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="ae51e-139">Click Filter.</span></span>
8. <span data-ttu-id="ae51e-140">Selecteer de rij van het Klantfacturenjournaal en het veld Verkooporder.</span><span class="sxs-lookup"><span data-stu-id="ae51e-140">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="ae51e-141">Typ 000148 in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="ae51e-141">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="ae51e-142">Typ in het criteriaveld "Verkooporder" het ordernummer 000148.</span><span class="sxs-lookup"><span data-stu-id="ae51e-142">In the criteria "Sales order" field, type the order number 000148.</span></span>  
10. <span data-ttu-id="ae51e-143">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="ae51e-143">Click OK.</span></span>
11. <span data-ttu-id="ae51e-144">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="ae51e-144">Click OK.</span></span>
    * <span data-ttu-id="ae51e-145">Controleer de gegenereerde uitvoer.</span><span class="sxs-lookup"><span data-stu-id="ae51e-145">Review the generated output.</span></span> <span data-ttu-id="ae51e-146">Merk op dat voor elke bijlage één XML-knooppunt is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="ae51e-146">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="ae51e-147">De inhoud van de bijlage is gevuld met de XML-uitvoer in de tekstindeling MIME (base64).</span><span class="sxs-lookup"><span data-stu-id="ae51e-147">The attachment's content is populated to the XML output in MIME (base64) text format.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]