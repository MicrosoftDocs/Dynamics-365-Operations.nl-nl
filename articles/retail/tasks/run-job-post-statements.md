--- 
title: Configureren en uitvoeren van taak om overzichten te boeken
description: Deze procedure doorloopt de configuratie en uitvoering van een terugkerende batchtaak om overzichten te boeken voor een geselecteerde winkel of groep winkels.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 676216d90c50c0d3fa1a839cab7a734e624708ba
ms.contentlocale: nl-nl
ms.lasthandoff: 09/14/2018

---
# <a name="configure-and-run-job-to-post-statements"></a><span data-ttu-id="b1d75-103">Configureren en uitvoeren van taak om overzichten te boeken</span><span class="sxs-lookup"><span data-stu-id="b1d75-103">Configure and run job to post statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="b1d75-104">Deze procedure doorloopt de configuratie en uitvoering van een terugkerende batchtaak om overzichten te boeken voor een geselecteerde winkel of groep winkels.</span><span class="sxs-lookup"><span data-stu-id="b1d75-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="b1d75-105">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="b1d75-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="b1d75-106">Ga naar Alle werkgebieden > ..</span><span class="sxs-lookup"><span data-stu-id="b1d75-106">Go to All workspaces > ..</span></span> <span data-ttu-id="b1d75-107">> Financiën van detailhandelwinkel.</span><span class="sxs-lookup"><span data-stu-id="b1d75-107">> Retail store financials.</span></span>
2. <span data-ttu-id="b1d75-108">Klik op Overzichten boeken.</span><span class="sxs-lookup"><span data-stu-id="b1d75-108">Click Post statements.</span></span>
    * <span data-ttu-id="b1d75-109">Selecteer een organisatiehiërarchie en selecteer vervolgens in de structuur van organisatieknooppunten een individuele winkel of een knooppunt.</span><span class="sxs-lookup"><span data-stu-id="b1d75-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="b1d75-110">Selecteer een knooppunt als u de batchtaak wilt maken voor een groep winkels.</span><span class="sxs-lookup"><span data-stu-id="b1d75-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="b1d75-111">Klik op de pijl om uw selectie toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="b1d75-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="b1d75-112">Klik op het tabblad Op de achtergrond uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="b1d75-112">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="b1d75-113">Schakel het selectievakje Batchverwerking in of uit.</span><span class="sxs-lookup"><span data-stu-id="b1d75-113">Check or uncheck the Batch processing checkbox.</span></span>
5. <span data-ttu-id="b1d75-114">Klik op Terugkeerpatroon.</span><span class="sxs-lookup"><span data-stu-id="b1d75-114">Click Recurrence.</span></span>
6. <span data-ttu-id="b1d75-115">Voer een datum in het veld Startdatum in.</span><span class="sxs-lookup"><span data-stu-id="b1d75-115">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="b1d75-116">Voer een tijd in het veld Begintijd in.</span><span class="sxs-lookup"><span data-stu-id="b1d75-116">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="b1d75-117">Kies of u de herhaling wilt beëindigen na een bepaald aantal uitvoeringen, op een specifieke datum of nooit.</span><span class="sxs-lookup"><span data-stu-id="b1d75-117">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="b1d75-118">Kies vervolgens de verschillende opties om te bepalen hoe vaak u de taak wilt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="b1d75-118">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="b1d75-119">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b1d75-119">Click OK.</span></span>
9. <span data-ttu-id="b1d75-120">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b1d75-120">Click OK.</span></span>


