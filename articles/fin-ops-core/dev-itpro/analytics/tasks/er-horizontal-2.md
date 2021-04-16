---
title: 'ER Horizontaal uitvouwbare bereiken gebruiken om kolommen in Excel-rapporten dynamisch toe te voegen (deel 2: Indeling uitvoeren)'
description: In dit onderwerp wordt beschreven hoe u een ER-indeling (Electronic Reporting) configureert om rapporten te genereren als OPENXML-werkbladbestanden (Excel). (Deel 2)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a62bad6ca241a2372a72e312ec5a707008a5fc09
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744982"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a><span data-ttu-id="77c4f-104">ER Horizontaal uitvouwbare bereiken gebruiken om kolommen in Excel-rapporten dynamisch toe te voegen (deel 2: Indeling uitvoeren)</span><span class="sxs-lookup"><span data-stu-id="77c4f-104">ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 2 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="77c4f-105">In de volgende stappen wordt uitgelegd hoe een gebruiker die aan de rol van systeembeheerder of ontwikkelaar elektronische rapportage is toegewezen, een elektronische rapportindeling (ER) kan configureren om rapporten als OPENXML-werkbladen (Excel-bestanden) te genereren waarin de vereiste kolommen dynamisch kunnen worden gemaakt als horizontaal uitvouwbare bereiken.</span><span class="sxs-lookup"><span data-stu-id="77c4f-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="77c4f-106">Deze stappen kunnen in het DEMF-bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="77c4f-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="77c4f-107">Als u deze stappen wilt uitvoeren, voert u eerst de stappen uit in de procedure "ER Gebruik horizontaal uitvouwbare bereiken om kolommen in Excel-rapporten dynamisch toe te voegen (Deel 1: Ontwerpindeling)".</span><span class="sxs-lookup"><span data-stu-id="77c4f-107">To complete these steps, you must first complete the steps in the "ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)" procedure.</span></span>

<span data-ttu-id="77c4f-108">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="77c4f-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="77c4f-109">Gemaakte indeling zoeken</span><span class="sxs-lookup"><span data-stu-id="77c4f-109">Find created format</span></span>
1. <span data-ttu-id="77c4f-110">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="77c4f-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="77c4f-111">Vouw in de structuur 'Voorbeeldmodel Financiële dimensies' uit.</span><span class="sxs-lookup"><span data-stu-id="77c4f-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="77c4f-112">In de structuur selecteert u 'Voorbeeldmodel Financiële dimensies\Voorbeeldrapport met horizontaal uitvouwbare bereiken'.</span><span class="sxs-lookup"><span data-stu-id="77c4f-112">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="77c4f-113">Indeling uitvoeren om Excel-uitvoer te maken</span><span class="sxs-lookup"><span data-stu-id="77c4f-113">Execute format to create Excel output</span></span>
1. <span data-ttu-id="77c4f-114">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="77c4f-114">Click Run.</span></span>
2. <span data-ttu-id="77c4f-115">Typ in het veld Dimensienaam 'BusinessUnit;CostCenter;Department'.</span><span class="sxs-lookup"><span data-stu-id="77c4f-115">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="77c4f-116">Typ of selecteer een waarde in het veld Dimensienaam.</span><span class="sxs-lookup"><span data-stu-id="77c4f-116">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="77c4f-117">Om alle dimensies voor het huidige bedrijf te selecteren, voert u het volgende in: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="77c4f-117">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="77c4f-118">Breid de sectie Op te nemen records uit.</span><span class="sxs-lookup"><span data-stu-id="77c4f-118">Expand the Records to include section.</span></span>
4. <span data-ttu-id="77c4f-119">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="77c4f-119">Click Filter.</span></span>
5. <span data-ttu-id="77c4f-120">Selecteer de rij voor de tabel Grootboekjournaal en het veld Batchnummer journaal.</span><span class="sxs-lookup"><span data-stu-id="77c4f-120">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="77c4f-121">Typ in het veld Criteria '00057..00058'.</span><span class="sxs-lookup"><span data-stu-id="77c4f-121">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="77c4f-122">00057..00058</span><span class="sxs-lookup"><span data-stu-id="77c4f-122">00057..00058</span></span>  
7. <span data-ttu-id="77c4f-123">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="77c4f-123">Click OK.</span></span>
8. <span data-ttu-id="77c4f-124">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="77c4f-124">Click OK.</span></span>
    * <span data-ttu-id="77c4f-125">Controleer de gegenereerde uitvoer.</span><span class="sxs-lookup"><span data-stu-id="77c4f-125">Review the generated output.</span></span> <span data-ttu-id="77c4f-126">Houd er rekening mee dat het nieuwe Excel-bestand hetzelfde aantal kolommen bevat als voor financiële dimensies zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="77c4f-126">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="77c4f-127">De rapportkoptekst in deze kolommen geeft de namen van de financiële dimensies weer.</span><span class="sxs-lookup"><span data-stu-id="77c4f-127">The report header in those columns represents financial dimensions' names.</span></span> <span data-ttu-id="77c4f-128">De transactieregels in deze kolommen geven de financiële dimensies weer.</span><span class="sxs-lookup"><span data-stu-id="77c4f-128">The transactions' lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="77c4f-129">Voer dit rapport uit en selecteer verschillende dimensies om te zien of het rapport niet afhankelijk is van het geselecteerde aantal dimensies of het aantal dimensies dat voor dit exemplaar is geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="77c4f-129">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]