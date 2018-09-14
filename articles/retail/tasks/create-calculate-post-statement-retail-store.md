--- 
title: " Een overzicht maken, berekenen en boeken voor een detailhandelwinkel"
description: Deze procedure doorloopt de handmatige stappen voor het maken, berekenen en boeken van een overzicht voor een winkel.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 9ea30e7e008bfcce77a7ee2f4d7d01a6cf1ababc
ms.contentlocale: nl-nl
ms.lasthandoff: 09/14/2018

---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a><span data-ttu-id="cd6e6-103"> Een overzicht maken, berekenen en boeken voor een detailhandelwinkel</span><span class="sxs-lookup"><span data-stu-id="cd6e6-103">Create, calculate, and post a statement for a retail store</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="cd6e6-104">Deze procedure doorloopt de handmatige stappen voor het maken, berekenen en boeken van een overzicht voor een winkel.</span><span class="sxs-lookup"><span data-stu-id="cd6e6-104">This procedure walks through the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="cd6e6-105">Er zijn ook batchtaken die voor dezelfde taken kunnen worden geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="cd6e6-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="cd6e6-106">De stappen voor het configureren en uitvoeren van de batchtaken kunnen in andere onderwerpen worden gevonden.</span><span class="sxs-lookup"><span data-stu-id="cd6e6-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="cd6e6-107">Als u deze procedure wilt voltooien, moet u transacties hebben die in POS zijn voltooid en vervolgens in Dynamics AX zijn opgehaald.</span><span class="sxs-lookup"><span data-stu-id="cd6e6-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics AX.</span></span> <span data-ttu-id="cd6e6-108">Deze registratie gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="cd6e6-108">This recording uses the USRT company in demo data.</span></span> <span data-ttu-id="cd6e6-109">In deze procedure kan worden verwezen naar Microsoft Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="cd6e6-109">This procedure may refer to Microsoft Dynamics AX.</span></span> <span data-ttu-id="cd6e6-110">Houd er rekening mee dat Dynamics AX nu Microsoft Dynamics 365 for Operations wordt genoemd.</span><span class="sxs-lookup"><span data-stu-id="cd6e6-110">Please note that Dynamics AX is now called Microsoft Dynamics 365 for Operations.</span></span>

1. <span data-ttu-id="cd6e6-111">Ga naar Alle werkgebieden > ..</span><span class="sxs-lookup"><span data-stu-id="cd6e6-111">Go to All workspaces > ..</span></span> <span data-ttu-id="cd6e6-112">> Financiën van detailhandelwinkel.</span><span class="sxs-lookup"><span data-stu-id="cd6e6-112">> Retail store financials.</span></span>
2. <span data-ttu-id="cd6e6-113">Klik op Nieuw overzicht.</span><span class="sxs-lookup"><span data-stu-id="cd6e6-113">Click New statement.</span></span>
3. <span data-ttu-id="cd6e6-114">Klik in het veld Winkelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="cd6e6-114">In the Store number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="cd6e6-115">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="cd6e6-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="cd6e6-116">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="cd6e6-116">Click OK.</span></span>
    * <span data-ttu-id="cd6e6-117">De instellingengroep bevat de instellingen die bepalen welke transacties in het overzicht worden opgenomen en hoe ze in overzichtsregels worden gegroepeerd.</span><span class="sxs-lookup"><span data-stu-id="cd6e6-117">The Setup group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="cd6e6-118">U kunt de instellingengroep openen en deze instellingen wijzigen of u kunt de standaardwaarden gebruiken.</span><span class="sxs-lookup"><span data-stu-id="cd6e6-118">You can open the Setup group and change these settings, or you can use the defaults.</span></span>  
    * <span data-ttu-id="cd6e6-119">Het veld Overzichtsmethode bepaalt hoe de overzichtsregels worden gegroepeerd.</span><span class="sxs-lookup"><span data-stu-id="cd6e6-119">The Statement method field defines how the statement lines will be grouped.</span></span>  
    * <span data-ttu-id="cd6e6-120">Selecteer een personeelslid of een register als u alleen een overzicht wilt berekenen voor dat specifieke personeelslid of register.</span><span class="sxs-lookup"><span data-stu-id="cd6e6-120">Select a staff member or a register if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="cd6e6-121">Selecteer een optie in het veld Afsluitingsmethode.</span><span class="sxs-lookup"><span data-stu-id="cd6e6-121">In the Closing method field, select an option.</span></span>
7. <span data-ttu-id="cd6e6-122">Klik op Overzicht berekenen.</span><span class="sxs-lookup"><span data-stu-id="cd6e6-122">Click Calculate statement.</span></span>
8. <span data-ttu-id="cd6e6-123">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="cd6e6-123">Click Yes.</span></span>
    * <span data-ttu-id="cd6e6-124">Na het berekenen van het overzicht moeten er regels zijn gemaakt met totale bedragen voor elke betalingsmethode en de overzichtsmethode die is gebruikt.</span><span class="sxs-lookup"><span data-stu-id="cd6e6-124">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    * <span data-ttu-id="cd6e6-125">Voer een geteld bedrag op elke regel in als het moet worden ingevoerd of bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="cd6e6-125">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="cd6e6-126">Het getelde veld wordt gevuld met bedragen van kascontroles die in POS zijn uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="cd6e6-126">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="cd6e6-127">Klik op Overzicht boeken.</span><span class="sxs-lookup"><span data-stu-id="cd6e6-127">Click Post statement.</span></span>
10. <span data-ttu-id="cd6e6-128">Klik op Sluiten.</span><span class="sxs-lookup"><span data-stu-id="cd6e6-128">Click Close.</span></span>
11. <span data-ttu-id="cd6e6-129">Ga naar Detailhandel en commerce > Kanalen > Financiën van detailhandelwinkel.</span><span class="sxs-lookup"><span data-stu-id="cd6e6-129">Go to Retail and commerce > Channels > Retail store financials.</span></span>
12. <span data-ttu-id="cd6e6-130">Klik op het tabblad Geboekte overzichten.</span><span class="sxs-lookup"><span data-stu-id="cd6e6-130">Click the Posted statements tab.</span></span>


