--- 
title: "ER Financiële dimensies gebruiken als gegevensbron (deel 4: het rapport uitvoeren)"
description: "In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan configureren om financiële dimensies te gebruiken als bron voor ER-rapporten."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 917eae141bbb8792f02d3323054e2a4096dae551
ms.contentlocale: nl-nl
ms.lasthandoff: 09/14/2018

---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4-run-the-report"></a><span data-ttu-id="38a50-103">ER Financiële dimensies gebruiken als gegevensbron (Deel 4: het rapport uitvoeren)</span><span class="sxs-lookup"><span data-stu-id="38a50-103">ER Use financial dimensions as a data source (Part 4: Run the report)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="38a50-104">In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan configureren om financiële dimensies te gebruiken als bron voor ER-rapporten.</span><span class="sxs-lookup"><span data-stu-id="38a50-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="38a50-105">Deze stappen kunnen in het DEMF-bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="38a50-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="38a50-106">Als u deze stappen wilt uitvoeren, moet u eerst de stappen uitvoeren in de procedure “ER Financiële dimensies gebruiken als gegevensbron (Deel 3: Het rapport ontwerpen)”.</span><span class="sxs-lookup"><span data-stu-id="38a50-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 3: Design the report)” procedure.</span></span> <span data-ttu-id="38a50-107">U moet ook standaarddocumenttypen op pagina Parameters van elektronische rapportage configureren.</span><span class="sxs-lookup"><span data-stu-id="38a50-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="38a50-108">De standaarddocumenttypen worden ook ingesteld als u een ER-configuratie downloadt en importeert.</span><span class="sxs-lookup"><span data-stu-id="38a50-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="38a50-109">Rapport uitvoeren</span><span class="sxs-lookup"><span data-stu-id="38a50-109">Run report</span></span>
1. <span data-ttu-id="38a50-110">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="38a50-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="38a50-111">Vouw in de structuur 'Voorbeeldmodel Financiële dimensies' uit.</span><span class="sxs-lookup"><span data-stu-id="38a50-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="38a50-112">Selecteer in de structuur 'Voorbeeldmodel Financiële dimensies\Grootboekjournaalrapport'.</span><span class="sxs-lookup"><span data-stu-id="38a50-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="38a50-113">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="38a50-113">Click Run.</span></span>
5. <span data-ttu-id="38a50-114">Typ of selecteer een waarde in het veld Dimensienaam.</span><span class="sxs-lookup"><span data-stu-id="38a50-114">In the Dimension name field, In the Dimension name field, enter or select a value..</span></span>
    * <span data-ttu-id="38a50-115">Om alle dimensies in het huidige bedrijf te selecteren, typt u het volgende: BusinessUnit;CostCenter;Afdeling; ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="38a50-115">To select all dimensions in the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
6. <span data-ttu-id="38a50-116">Breid de sectie Op te nemen records uit.</span><span class="sxs-lookup"><span data-stu-id="38a50-116">Expand the Records to include section.</span></span>
7. <span data-ttu-id="38a50-117">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="38a50-117">Click Filter.</span></span>
8. <span data-ttu-id="38a50-118">Selecteer de rij voor de tabel Grootboekjournaal en het veld Batchnummer journaal.</span><span class="sxs-lookup"><span data-stu-id="38a50-118">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="38a50-119">Typ 00057 in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="38a50-119">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="38a50-120">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="38a50-120">Click OK.</span></span>
11. <span data-ttu-id="38a50-121">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="38a50-121">Click OK.</span></span>
    * <span data-ttu-id="38a50-122">Controleer de gegenereerde uitvoer.</span><span class="sxs-lookup"><span data-stu-id="38a50-122">Review the generated output.</span></span> <span data-ttu-id="38a50-123">Merk op dat voor elke transactie van de geselecteerde batch, de financiële dimensies uit de bijbehorende ingestelde dimensies worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="38a50-123">Note that for each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="38a50-124">Voer dit rapport uit en selecteer verschillende dimensies om te zien of het rapport niet afhankelijk is van het geselecteerde aantal dimensies of het aantal dimensies dat voor dit exemplaar van Dynamics 365 for Finance and Operations, Enterprise edition, is geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="38a50-124">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations, Enterprise edition instance.</span></span>  


