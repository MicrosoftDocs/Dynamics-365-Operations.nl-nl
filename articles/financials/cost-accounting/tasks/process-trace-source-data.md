--- 
title: Brongegevens verwerken en traceren
description: Alle gegevensverwerking wordt uitgevoerd door taken.
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7093338fd306e90df79a787f9de9861b3fe49dd5
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="process-and-trace-source-data"></a><span data-ttu-id="4bf38-103">Brongegevens verwerken en traceren</span><span class="sxs-lookup"><span data-stu-id="4bf38-103">Process and trace source data</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4bf38-104">Alle gegevensverwerking wordt uitgevoerd door taken.</span><span class="sxs-lookup"><span data-stu-id="4bf38-104">All data processing is run by jobs.</span></span> <span data-ttu-id="4bf38-105">Voor elke taak en gegevensprovider wordt een journaal gemaakt om te documenteren dat het proces is uitgevoerd en dat de posten zijn verwerkt in de huidige taak.</span><span class="sxs-lookup"><span data-stu-id="4bf38-105">For each job and data provider, a journal is created to document that the process has been run, and that the entries were processed in the current job.</span></span> <span data-ttu-id="4bf38-106">Met deze procedure kunt u een gegevensbron instellen en vervolgens de oorsprong van een bepaalde kostenpost traceren.</span><span class="sxs-lookup"><span data-stu-id="4bf38-106">Use this procedure to set up a data source and then  trace the origin of a specific cost entry.</span></span> <span data-ttu-id="4bf38-107">Deze registratie gebruikt het USP2-demogegevensbedrijf USP2.</span><span class="sxs-lookup"><span data-stu-id="4bf38-107">This recording uses the USP2 demo data company USP2.</span></span> <span data-ttu-id="4bf38-108">Zorg voordat u deze taak voltooit dat u de volgende taakbegeleiders afspeelt: 'Een grootboek van kostprijsboekhouding maken', 'Kostenbeheereenheden definiëren' en 'Gegevensbron beheren voor het grootboek van kostprijsboekhouding'.</span><span class="sxs-lookup"><span data-stu-id="4bf38-108">Before you complete this task, make sure that you play the following task guides: "Create a cost accounting ledger," "Define cost control units," and "Manage data source for the cost accounting ledger."</span></span>

1. <span data-ttu-id="4bf38-109">Ga naar Kostprijsboekhouding  >Grootboek instellen > Grootboeken van kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="4bf38-109">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="4bf38-110">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="4bf38-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4bf38-111">Selecteer het grootboek van kostprijsboekhouding dat u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="4bf38-111">Select the cost accounting ledger that you created earlier.</span></span>  
3. <span data-ttu-id="4bf38-112">Klik op Actuele versies.</span><span class="sxs-lookup"><span data-stu-id="4bf38-112">Click Actual versions.</span></span>
4. <span data-ttu-id="4bf38-113">Klik in het actievenster op Verwerking van brongegevens.</span><span class="sxs-lookup"><span data-stu-id="4bf38-113">On the Action Pane, click Source data processing.</span></span>
5. <span data-ttu-id="4bf38-114">Klik op Overboekingsjournalen van grootboekposten.</span><span class="sxs-lookup"><span data-stu-id="4bf38-114">Click General ledger entry transfer journals.</span></span>
6. <span data-ttu-id="4bf38-115">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="4bf38-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="4bf38-116">Klik op Journaalboekingen.</span><span class="sxs-lookup"><span data-stu-id="4bf38-116">Click Journal entries.</span></span>
8. <span data-ttu-id="4bf38-117">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="4bf38-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="4bf38-118">Klik op Kosteninvoer.</span><span class="sxs-lookup"><span data-stu-id="4bf38-118">Click Cost entries.</span></span>
10. <span data-ttu-id="4bf38-119">Klik op Broninvoer.</span><span class="sxs-lookup"><span data-stu-id="4bf38-119">Click Source entry.</span></span>
11. <span data-ttu-id="4bf38-120">Klik in het actievenster op Verwerking van brongegevens.</span><span class="sxs-lookup"><span data-stu-id="4bf38-120">On the Action Pane, click Source data processing.</span></span>
12. <span data-ttu-id="4bf38-121">Klik op Grootboek.</span><span class="sxs-lookup"><span data-stu-id="4bf38-121">Click General ledger.</span></span>
13. <span data-ttu-id="4bf38-122">Typ of selecteer een waarde in het veld Fiscale kalenderperiode.</span><span class="sxs-lookup"><span data-stu-id="4bf38-122">In the Fiscal calendar period field, enter or select a value.</span></span>
    * <span data-ttu-id="4bf38-123">Selecteer voor dit voorbeeld Fiscaal 2017 periode 9.</span><span class="sxs-lookup"><span data-stu-id="4bf38-123">For this example, select Fiscal 2017 Period 9.</span></span>  
14. <span data-ttu-id="4bf38-124">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="4bf38-124">Click OK.</span></span>


