---
title: 'ER Horizontaal uitvouwbare bereiken gebruiken om kolommen in Excel-rapporten dynamisch toe te voegen (deel 2: Indeling uitvoeren)'
description: In de volgende stappen wordt uitgelegd hoe een gebruiker die aan de rol van systeembeheerder of ontwikkelaar elektronische rapportage is toegewezen, een elektronische rapportindeling (ER) kan configureren om rapporten als OPENXML-werkbladen (Excel-bestanden) te genereren waarin de vereiste kolommen dynamisch kunnen worden gemaakt als horizontaal uitvouwbare bereiken.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 66c2a97a068ed83f93699f14e827bdc2fb580d93
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141828"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a><span data-ttu-id="b8f37-103">ER Horizontaal uitvouwbare bereiken gebruiken om kolommen in Excel-rapporten dynamisch toe te voegen (deel 2: Indeling uitvoeren)</span><span class="sxs-lookup"><span data-stu-id="b8f37-103">ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 2 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b8f37-104">In de volgende stappen wordt uitgelegd hoe een gebruiker die aan de rol van systeembeheerder of ontwikkelaar elektronische rapportage is toegewezen, een elektronische rapportindeling (ER) kan configureren om rapporten als OPENXML-werkbladen (Excel-bestanden) te genereren waarin de vereiste kolommen dynamisch kunnen worden gemaakt als horizontaal uitvouwbare bereiken.</span><span class="sxs-lookup"><span data-stu-id="b8f37-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="b8f37-105">Deze stappen kunnen in het DEMF-bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="b8f37-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="b8f37-106">Als u deze stappen wilt uitvoeren, voert u eerst de stappen uit in de procedure "ER Gebruik horizontaal uitvouwbare bereiken om kolommen in Excel-rapporten dynamisch toe te voegen (Deel 1: Ontwerpindeling)".</span><span class="sxs-lookup"><span data-stu-id="b8f37-106">To complete these steps, you must first complete the steps in the "ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)" procedure.</span></span>

<span data-ttu-id="b8f37-107">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="b8f37-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="b8f37-108">Gemaakte indeling zoeken</span><span class="sxs-lookup"><span data-stu-id="b8f37-108">Find created format</span></span>
1. <span data-ttu-id="b8f37-109">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="b8f37-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="b8f37-110">Vouw in de structuur 'Voorbeeldmodel Financiële dimensies' uit.</span><span class="sxs-lookup"><span data-stu-id="b8f37-110">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="b8f37-111">In de structuur selecteert u 'Voorbeeldmodel Financiële dimensies\Voorbeeldrapport met horizontaal uitvouwbare bereiken'.</span><span class="sxs-lookup"><span data-stu-id="b8f37-111">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="b8f37-112">Indeling uitvoeren om Excel-uitvoer te maken</span><span class="sxs-lookup"><span data-stu-id="b8f37-112">Execute format to create Excel output</span></span>
1. <span data-ttu-id="b8f37-113">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="b8f37-113">Click Run.</span></span>
2. <span data-ttu-id="b8f37-114">Typ in het veld Dimensienaam 'BusinessUnit;CostCenter;Department'.</span><span class="sxs-lookup"><span data-stu-id="b8f37-114">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="b8f37-115">Typ of selecteer een waarde in het veld Dimensienaam.</span><span class="sxs-lookup"><span data-stu-id="b8f37-115">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="b8f37-116">Om alle dimensies voor het huidige bedrijf te selecteren, voert u het volgende in: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="b8f37-116">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="b8f37-117">Breid de sectie Op te nemen records uit.</span><span class="sxs-lookup"><span data-stu-id="b8f37-117">Expand the Records to include section.</span></span>
4. <span data-ttu-id="b8f37-118">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="b8f37-118">Click Filter.</span></span>
5. <span data-ttu-id="b8f37-119">Selecteer de rij voor de tabel Grootboekjournaal en het veld Batchnummer journaal.</span><span class="sxs-lookup"><span data-stu-id="b8f37-119">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="b8f37-120">Typ in het veld Criteria '00057..00058'.</span><span class="sxs-lookup"><span data-stu-id="b8f37-120">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="b8f37-121">00057..00058</span><span class="sxs-lookup"><span data-stu-id="b8f37-121">00057..00058</span></span>  
7. <span data-ttu-id="b8f37-122">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b8f37-122">Click OK.</span></span>
8. <span data-ttu-id="b8f37-123">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b8f37-123">Click OK.</span></span>
    * <span data-ttu-id="b8f37-124">Controleer de gegenereerde uitvoer.</span><span class="sxs-lookup"><span data-stu-id="b8f37-124">Review the generated output.</span></span> <span data-ttu-id="b8f37-125">Houd er rekening mee dat het nieuwe Excel-bestand hetzelfde aantal kolommen bevat als voor financiële dimensies zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="b8f37-125">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="b8f37-126">De rapportkoptekst in deze kolommen geeft de namen van de financiële dimensies weer.</span><span class="sxs-lookup"><span data-stu-id="b8f37-126">The report header in those columns represents financial dimensions' names.</span></span> <span data-ttu-id="b8f37-127">De transactieregels in deze kolommen geven de financiële dimensies weer.</span><span class="sxs-lookup"><span data-stu-id="b8f37-127">The transactions' lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="b8f37-128">Voer dit rapport uit en selecteer verschillende dimensies om te zien of het rapport niet afhankelijk is van het geselecteerde aantal dimensies of het aantal dimensies dat voor dit exemplaar is geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="b8f37-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  

