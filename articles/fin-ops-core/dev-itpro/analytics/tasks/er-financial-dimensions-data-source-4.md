---
title: 'ER Financiële dimensies gebruiken als gegevensbron (deel 4: het rapport uitvoeren)'
description: In dit onderwerp wordt beschreven hoe u een ER-model (Electronic Reporting) configureert om financiële dimensies te gebruiken als gegevensbron voor ER-rapporten. (Deel 4)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1fe332de84339d3369ba495ca13f50c4901f366
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092270"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="ea524-104">ER Financiële dimensies gebruiken als gegevensbron (deel 4: het rapport uitvoeren)</span><span class="sxs-lookup"><span data-stu-id="ea524-104">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ea524-105">In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan configureren om financiële dimensies te gebruiken als bron voor ER-rapporten.</span><span class="sxs-lookup"><span data-stu-id="ea524-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="ea524-106">Deze stappen kunnen in het DEMF-bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="ea524-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="ea524-107">Als u deze stappen wilt uitvoeren, moet u eerst de stappen uitvoeren in de procedure "ER Financiële dimensies gebruiken als gegevensbron (Deel 3: Het rapport ontwerpen)".</span><span class="sxs-lookup"><span data-stu-id="ea524-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="ea524-108">U moet ook standaarddocumenttypen op pagina Parameters van elektronische rapportage configureren.</span><span class="sxs-lookup"><span data-stu-id="ea524-108">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="ea524-109">De standaarddocumenttypen worden ook ingesteld als u een ER-configuratie downloadt en importeert.</span><span class="sxs-lookup"><span data-stu-id="ea524-109">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="ea524-110">Rapport uitvoeren</span><span class="sxs-lookup"><span data-stu-id="ea524-110">Run report</span></span>
1. <span data-ttu-id="ea524-111">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="ea524-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="ea524-112">Vouw in de structuur 'Voorbeeldmodel Financiële dimensies' uit.</span><span class="sxs-lookup"><span data-stu-id="ea524-112">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="ea524-113">Selecteer in de structuur 'Voorbeeldmodel Financiële dimensies\Grootboekjournaalrapport'.</span><span class="sxs-lookup"><span data-stu-id="ea524-113">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="ea524-114">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="ea524-114">Click Run.</span></span>
<span data-ttu-id="ea524-115">![Pagina ER-configuraties](../media/er-financial-dimensions-guides-run1.png)</span><span class="sxs-lookup"><span data-stu-id="ea524-115">![ER configurations page](../media/er-financial-dimensions-guides-run1.png)</span></span>
5. <span data-ttu-id="ea524-116">Typ of selecteer een waarde in het veld Dimensienaam.</span><span class="sxs-lookup"><span data-stu-id="ea524-116">In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="ea524-117">Om alle dimensies in het huidige bedrijf te selecteren, typt u het volgende: BusinessUnit;CostCenter;Afdeling; ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="ea524-117">To select all dimensions in the current company, enter the following information:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
![Pagina ER-configuraties](../media/er-financial-dimensions-guides-run2.png)
6. <span data-ttu-id="ea524-119">Breid de sectie Op te nemen records uit.</span><span class="sxs-lookup"><span data-stu-id="ea524-119">Expand the Records to include section.</span></span>
7. <span data-ttu-id="ea524-120">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="ea524-120">Click Filter.</span></span>
8. <span data-ttu-id="ea524-121">Selecteer de rij voor de tabel Grootboekjournaal en het veld Batchnummer journaal.</span><span class="sxs-lookup"><span data-stu-id="ea524-121">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="ea524-122">Typ 00057 in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="ea524-122">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="ea524-123">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="ea524-123">Click OK.</span></span>
11. <span data-ttu-id="ea524-124">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="ea524-124">Click OK.</span></span>
<span data-ttu-id="ea524-125">![Pagina ER-configuraties](../media/er-financial-dimensions-guides-run3.png)</span><span class="sxs-lookup"><span data-stu-id="ea524-125">![ER configurations page](../media/er-financial-dimensions-guides-run3.png)</span></span>
    * <span data-ttu-id="ea524-126">Controleer de gegenereerde uitvoer.</span><span class="sxs-lookup"><span data-stu-id="ea524-126">Review the generated output.</span></span> <span data-ttu-id="ea524-127">Voor elke transactie van de geselecteerde batch worden de financiële dimensies uit de bijbehorende ingestelde dimensies weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ea524-127">For each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="ea524-128">Voer dit rapport uit en selecteer verschillende dimensies om te zien of het rapport niet afhankelijk is van het geselecteerde aantal dimensies of het aantal dimensies dat voor dit exemplaar is geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="ea524-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  
![Pagina ER-configuraties](../media/er-financial-dimensions-guides-run4.png)
