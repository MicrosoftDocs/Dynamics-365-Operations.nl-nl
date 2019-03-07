---
title: Configureren en uitvoeren van taak om overzichten te berekenen
description: Deze procedure doorloopt de configuratie en uitvoering van terugkerende batchtaken om overzichten te maken en te berekenen voor een geselecteerde winkel of groep winkels.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f52603672e95d0ae4973844851c4ed260484e5f0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "365173"
---
# <a name="configure-and-run-job-to-calculate-statements"></a><span data-ttu-id="2c35e-103">Configureren en uitvoeren van taak om overzichten te berekenen</span><span class="sxs-lookup"><span data-stu-id="2c35e-103">Configure and run job to calculate statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="2c35e-104">Deze procedure doorloopt de configuratie en uitvoering van terugkerende batchtaken om overzichten te maken en te berekenen voor een geselecteerde winkel of groep winkels.</span><span class="sxs-lookup"><span data-stu-id="2c35e-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="2c35e-105">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="2c35e-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="2c35e-106">Ga naar Alle werkruimten > Financiën van detailhandelwinkel.</span><span class="sxs-lookup"><span data-stu-id="2c35e-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="2c35e-107">Klik op Overzichten berekenen.</span><span class="sxs-lookup"><span data-stu-id="2c35e-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="2c35e-108">Selecteer een specifieke winkel of een knooppunt als u de batchtaak wilt maken voor een groep winkels.</span><span class="sxs-lookup"><span data-stu-id="2c35e-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="2c35e-109">Klik op de pijl om uw selectie toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="2c35e-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="2c35e-110">Klik op het tabblad Op de achtergrond uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="2c35e-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="2c35e-111">Selecteer 'Ja' onder Batchverwerking.</span><span class="sxs-lookup"><span data-stu-id="2c35e-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="2c35e-112">Klik op Terugkeerpatroon.</span><span class="sxs-lookup"><span data-stu-id="2c35e-112">Click Recurrence.</span></span>
6. <span data-ttu-id="2c35e-113">Voer een datum in het veld Startdatum in.</span><span class="sxs-lookup"><span data-stu-id="2c35e-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="2c35e-114">Voer een tijd in het veld Begintijd in.</span><span class="sxs-lookup"><span data-stu-id="2c35e-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="2c35e-115">Selecteer de optie Geen einddatum.</span><span class="sxs-lookup"><span data-stu-id="2c35e-115">Select the No end date option.</span></span>
9. <span data-ttu-id="2c35e-116">Voer 'Dagen' in het veld Patrooneenheid in.</span><span class="sxs-lookup"><span data-stu-id="2c35e-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="2c35e-117">Voer een getal in het veld Per in.</span><span class="sxs-lookup"><span data-stu-id="2c35e-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="2c35e-118">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="2c35e-118">Click OK.</span></span>
12. <span data-ttu-id="2c35e-119">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="2c35e-119">Click OK.</span></span>

