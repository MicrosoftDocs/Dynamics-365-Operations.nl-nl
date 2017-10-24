--- 
title: Een indeling uitvoeren die gebruikmaakt van horizontaal uitvouwbare bereiken voor het dynamisch toevoegen van kolommen in Excel-rapporten voor elektronische aangifte (ER)
description: In de volgende stappen wordt uitgelegd hoe een gebruiker die aan de rol van systeembeheerder of ontwikkelaar elektronische rapportage is toegewezen, een elektronische rapportindeling (ER) kan configureren om rapporten als OPENXML-werkbladen (Excel-bestanden) te genereren waarin de vereiste kolommen dynamisch kunnen worden gemaakt als horizontaal uitvouwbare bereiken.
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 8e5c53905b903bc5242625283f3b093144243cf9
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="run-a-format-that-uses-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-for-electronic-reporting-er"></a><span data-ttu-id="02915-103">Een indeling uitvoeren die gebruikmaakt van horizontaal uitvouwbare bereiken voor het dynamisch toevoegen van kolommen in Excel-rapporten voor elektronische aangifte (ER)</span><span class="sxs-lookup"><span data-stu-id="02915-103">Run a format that uses horizontally-expandable ranges to dynamically add columns in Excel reports for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="02915-104">In de volgende stappen wordt uitgelegd hoe een gebruiker die aan de rol van systeembeheerder of ontwikkelaar elektronische rapportage is toegewezen, een elektronische rapportindeling (ER) kan configureren om rapporten als OPENXML-werkbladen (Excel-bestanden) te genereren waarin de vereiste kolommen dynamisch kunnen worden gemaakt als horizontaal uitvouwbare bereiken.</span><span class="sxs-lookup"><span data-stu-id="02915-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="02915-105">Deze stappen kunnen in het DEMF-bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="02915-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="02915-106">Als u deze stappen wilt uitvoeren, voert u eerst de stappen uit in de procedure "ER Gebruik horizontaal uitvouwbare bereiken om kolommen in Excel-rapporten dynamisch toe te voegen (Deel 1: Ontwerpindeling)".</span><span class="sxs-lookup"><span data-stu-id="02915-106">To complete these steps, you must first complete the steps in the “ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)” procedure.</span></span>

<span data-ttu-id="02915-107">Deze procedure is voor een functie die in versie 1611 van Dynamics 365 for Operations is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="02915-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="02915-108">Gemaakte indeling zoeken</span><span class="sxs-lookup"><span data-stu-id="02915-108">Find created format</span></span>
1. <span data-ttu-id="02915-109">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="02915-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="02915-110">Vouw in de structuur 'Voorbeeldmodel Financiële dimensies' uit.</span><span class="sxs-lookup"><span data-stu-id="02915-110">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="02915-111">In de structuur selecteert u 'Voorbeeldmodel Financiële dimensies\Voorbeeldrapport met horizontaal uitvouwbare bereiken'.</span><span class="sxs-lookup"><span data-stu-id="02915-111">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="02915-112">Indeling uitvoeren om Excel-uitvoer te maken</span><span class="sxs-lookup"><span data-stu-id="02915-112">Execute format to create Excel output</span></span>
1. <span data-ttu-id="02915-113">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="02915-113">Click Run.</span></span>
2. <span data-ttu-id="02915-114">Typ in het veld Dimensienaam 'BusinessUnit;CostCenter;Department'.</span><span class="sxs-lookup"><span data-stu-id="02915-114">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="02915-115">Typ of selecteer een waarde in het veld Dimensienaam.</span><span class="sxs-lookup"><span data-stu-id="02915-115">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="02915-116">Om alle dimensies voor het huidige bedrijf te selecteren, voert u het volgende in: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="02915-116">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="02915-117">Breid de sectie Op te nemen records uit.</span><span class="sxs-lookup"><span data-stu-id="02915-117">Expand the Records to include section.</span></span>
4. <span data-ttu-id="02915-118">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="02915-118">Click Filter.</span></span>
5. <span data-ttu-id="02915-119">Selecteer de rij voor de tabel Grootboekjournaal en het veld Batchnummer journaal.</span><span class="sxs-lookup"><span data-stu-id="02915-119">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="02915-120">Typ in het veld Criteria '00057..00058'.</span><span class="sxs-lookup"><span data-stu-id="02915-120">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="02915-121">00057..00058</span><span class="sxs-lookup"><span data-stu-id="02915-121">00057..00058</span></span>  
7. <span data-ttu-id="02915-122">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="02915-122">Click OK.</span></span>
8. <span data-ttu-id="02915-123">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="02915-123">Click OK.</span></span>
    * <span data-ttu-id="02915-124">Controleer de gegenereerde uitvoer.</span><span class="sxs-lookup"><span data-stu-id="02915-124">Review the generated output.</span></span> <span data-ttu-id="02915-125">Houd er rekening mee dat het nieuwe Excel-bestand hetzelfde aantal kolommen bevat als voor financiële dimensies zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="02915-125">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="02915-126">De rapportkoptekst in deze kolommen geeft de namen van de financiële dimensies weer.</span><span class="sxs-lookup"><span data-stu-id="02915-126">The report header in those columns represents financial dimensions’ names.</span></span> <span data-ttu-id="02915-127">De transactieregels in deze kolommen geven de financiële dimensies weer.</span><span class="sxs-lookup"><span data-stu-id="02915-127">The transactions’ lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="02915-128">Voer dit rapport uit en selecteer verschillende dimensies om te zien of het rapport niet afhankelijk is van het geselecteerde aantal dimensies of het aantal dimensies dat voor dit exemplaar van Dynamics 365 for Finance and Operations, Enterprise edition, is geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="02915-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations, Enterprise edition instance.</span></span>  


