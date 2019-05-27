---
title: Boeking van online verkopen en betalingen
description: Deze procedure doorloopt de configuratie en uitvoering van een terugkerende batchtaak om verkooporders en betalingen voor online winkeltransacties te maken.
author: jashanno
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
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13839bbe6ca03f3cfc7036fce87477bf7d5af2a7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550203"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="049f8-103">Boeking van online verkopen en betalingen</span><span class="sxs-lookup"><span data-stu-id="049f8-103">Posting of online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="049f8-104">Deze procedure doorloopt de configuratie en uitvoering van een terugkerende batchtaak om verkooporders en betalingen voor online winkeltransacties te maken.</span><span class="sxs-lookup"><span data-stu-id="049f8-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="049f8-105">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="049f8-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="049f8-106">Ga naar Alle werkruimten > Financiën van detailhandelwinkel.</span><span class="sxs-lookup"><span data-stu-id="049f8-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="049f8-107">Klik op Orders synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="049f8-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="049f8-108">Selecteer in het veld Organisatiehiërarchie 'Detailhandelwinkels per regio'.</span><span class="sxs-lookup"><span data-stu-id="049f8-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="049f8-109">Selecteer een specifieke online winkel of een knooppunt als u de batchtaak wilt maken voor een groep winkels.</span><span class="sxs-lookup"><span data-stu-id="049f8-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="049f8-110">Klik op de pijl om uw selectie toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="049f8-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="049f8-111">Klik op het tabblad Op de achtergrond uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="049f8-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="049f8-112">Schakel het selectievakje Batchverwerking in of uit.</span><span class="sxs-lookup"><span data-stu-id="049f8-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="049f8-113">Klik op Terugkeerpatroon.</span><span class="sxs-lookup"><span data-stu-id="049f8-113">Click Recurrence.</span></span>
7. <span data-ttu-id="049f8-114">Selecteer de optie Geen einddatum.</span><span class="sxs-lookup"><span data-stu-id="049f8-114">Select the No end date option.</span></span>
8. <span data-ttu-id="049f8-115">Voer een getal in het veld Aantal in.</span><span class="sxs-lookup"><span data-stu-id="049f8-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="049f8-116">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="049f8-116">Click OK.</span></span>
10. <span data-ttu-id="049f8-117">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="049f8-117">Click OK.</span></span>

