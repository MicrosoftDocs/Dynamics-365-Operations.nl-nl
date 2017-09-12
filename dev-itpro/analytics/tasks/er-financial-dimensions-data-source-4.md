--- 
title: "Een rapport uitvoeren dat gebruikmaakt van financiële dimensies als gegevensbron voor elektronische aangifte (ER)"
description: "In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan configureren om financiële dimensies te gebruiken als bron voor ER-rapporten."
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e319c9d11ccc4311437ce1e74d4f6c8be0e0de35
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="run-a-report-that-uses-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="44126-103">Een rapport uitvoeren dat gebruikmaakt van financiële dimensies als gegevensbron voor elektronische aangifte (ER)</span><span class="sxs-lookup"><span data-stu-id="44126-103">Run a report that uses financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="44126-104">In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan configureren om financiële dimensies te gebruiken als bron voor ER-rapporten.</span><span class="sxs-lookup"><span data-stu-id="44126-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="44126-105">Deze stappen kunnen in het DEMF-bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="44126-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="44126-106">Als u deze stappen wilt uitvoeren, moet u eerst de stappen uitvoeren in de procedure “ER Financiële dimensies gebruiken als gegevensbron (Deel 3: Het rapport ontwerpen)”.</span><span class="sxs-lookup"><span data-stu-id="44126-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 3: Design the report)” procedure.</span></span> <span data-ttu-id="44126-107">U moet ook standaarddocumenttypen op pagina Parameters van elektronische rapportage configureren.</span><span class="sxs-lookup"><span data-stu-id="44126-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="44126-108">De standaarddocumenttypen worden ook ingesteld als u een ER-configuratie downloadt en importeert.</span><span class="sxs-lookup"><span data-stu-id="44126-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="44126-109">Rapport uitvoeren</span><span class="sxs-lookup"><span data-stu-id="44126-109">Run report</span></span>
1. <span data-ttu-id="44126-110">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="44126-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="44126-111">Vouw in de structuur 'Voorbeeldmodel Financiële dimensies' uit.</span><span class="sxs-lookup"><span data-stu-id="44126-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="44126-112">Selecteer in de structuur 'Voorbeeldmodel Financiële dimensies\Grootboekjournaalrapport'.</span><span class="sxs-lookup"><span data-stu-id="44126-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="44126-113">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="44126-113">Click Run.</span></span>
5. <span data-ttu-id="44126-114">Typ of selecteer een waarde in het veld Dimensienaam.</span><span class="sxs-lookup"><span data-stu-id="44126-114">In the Dimension name field, In the Dimension name field, enter or select a value..</span></span>
    * <span data-ttu-id="44126-115">Om alle dimensies in het huidige bedrijf te selecteren, typt u het volgende:
BusinessUnit;CostCenter;Afdeling; ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="44126-115">To select all dimensions in the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
6. <span data-ttu-id="44126-116">Breid de sectie Op te nemen records uit.</span><span class="sxs-lookup"><span data-stu-id="44126-116">Expand the Records to include section.</span></span>
7. <span data-ttu-id="44126-117">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="44126-117">Click Filter.</span></span>
8. <span data-ttu-id="44126-118">Selecteer de rij voor de tabel Grootboekjournaal en het veld Batchnummer journaal.</span><span class="sxs-lookup"><span data-stu-id="44126-118">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="44126-119">Typ 00057 in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="44126-119">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="44126-120">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="44126-120">Click OK.</span></span>
11. <span data-ttu-id="44126-121">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="44126-121">Click OK.</span></span>
    * <span data-ttu-id="44126-122">Controleer de gegenereerde uitvoer.</span><span class="sxs-lookup"><span data-stu-id="44126-122">Review the generated output.</span></span> <span data-ttu-id="44126-123">Merk op dat voor elke transactie van de geselecteerde batch, de financiële dimensies uit de bijbehorende ingestelde dimensies worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="44126-123">Note that for each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="44126-124">Voer dit rapport uit en selecteer verschillende dimensies om te zien of het rapport niet afhankelijk is van het geselecteerde aantal dimensies of het aantal dimensies dat voor dit exemplaar van Dynamics 365 for Finance and Operations, Enterprise edition, is geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="44126-124">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations, Enterprise edition instance.</span></span>  


