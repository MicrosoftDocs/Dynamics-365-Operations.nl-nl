---
title: Overzichten maken, berekenen en boeken voor een detailhandelwinkel
description: In dit onderwerp worden de handmatige stappen beschreven voor het maken, berekenen en boeken van een overzicht voor een winkel.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4517b9ddeb648b3d789773fc0dcb1ecd3c8be85c
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024793"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a><span data-ttu-id="8cf0e-103">Overzichten maken, berekenen en boeken voor een detailhandelwinkel</span><span class="sxs-lookup"><span data-stu-id="8cf0e-103">Create, calculate, and post statements for a retail store</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="8cf0e-104">In dit onderwerp worden de handmatige stappen beschreven voor het maken, berekenen en boeken van een overzicht voor een winkel.</span><span class="sxs-lookup"><span data-stu-id="8cf0e-104">This topic describes the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="8cf0e-105">Er zijn ook batchtaken die voor dezelfde taken kunnen worden geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="8cf0e-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="8cf0e-106">De stappen voor het configureren en uitvoeren van de batchtaken kunnen in andere onderwerpen worden gevonden.</span><span class="sxs-lookup"><span data-stu-id="8cf0e-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="8cf0e-107">Als u deze procedure wilt voltooien, moet u transacties hebben die in POS zijn voltooid en vervolgens in Dynamics 365 Retail zijn opgehaald.</span><span class="sxs-lookup"><span data-stu-id="8cf0e-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics 365 Retail.</span></span> <span data-ttu-id="8cf0e-108">Deze registratie gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="8cf0e-108">This recording uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="8cf0e-109">Selecteer **Financiën van detailhandelwinkel** op de startpagina.</span><span class="sxs-lookup"><span data-stu-id="8cf0e-109">Select **Retail store financials** from the home page.</span></span>
2. <span data-ttu-id="8cf0e-110">Selecteer **Nieuw overzicht**.</span><span class="sxs-lookup"><span data-stu-id="8cf0e-110">Select **New statement**.</span></span>
3. <span data-ttu-id="8cf0e-111">Selecteer in het veld **Winkelnummer** een optie in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="8cf0e-111">In the **Store number** field, select a option from the drop-down.</span></span>
4. <span data-ttu-id="8cf0e-112">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="8cf0e-112">Select **OK**.</span></span>
5. <span data-ttu-id="8cf0e-113">De groep **Instellingen** bevat de instellingen die bepalen welke transacties in het overzicht worden opgenomen en hoe ze in overzichtsregels worden gegroepeerd.</span><span class="sxs-lookup"><span data-stu-id="8cf0e-113">The **Setup** group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="8cf0e-114">U kunt de groep **Instellingen** openen en deze instellingen wijzigen of u kunt de standaardwaarden gebruiken.</span><span class="sxs-lookup"><span data-stu-id="8cf0e-114">You can open the **Setup** group and change these settings, or you can use the defaults.</span></span>  
    - <span data-ttu-id="8cf0e-115">Het veld **Overzichtsmethode** bepaalt hoe de overzichtsregels worden gegroepeerd.</span><span class="sxs-lookup"><span data-stu-id="8cf0e-115">The **Statement method** field defines how the statement lines will be grouped.</span></span>  
    - <span data-ttu-id="8cf0e-116">Selecteer een personeelslid of een register in het veld **Personeel/kassa** als u alleen een overzicht wilt berekenen voor dat specifieke personeelslid of die specifieke kassa.</span><span class="sxs-lookup"><span data-stu-id="8cf0e-116">Select a staff member or a register in the **staff/register** field if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="8cf0e-117">Selecteer een optie in het veld **Afsluitingsmethode**.</span><span class="sxs-lookup"><span data-stu-id="8cf0e-117">In the **Closing method** field, select an option.</span></span>
7. <span data-ttu-id="8cf0e-118">Selecteer **Overzicht berekenen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="8cf0e-118">Select **Calculate statement** from the Action Pane.</span></span>
8. <span data-ttu-id="8cf0e-119">Selecteer **Ja**.</span><span class="sxs-lookup"><span data-stu-id="8cf0e-119">Select **Yes**.</span></span>
    - <span data-ttu-id="8cf0e-120">Na het berekenen van het overzicht moeten er regels zijn gemaakt met totale bedragen voor elke betalingsmethode en de overzichtsmethode die is gebruikt.</span><span class="sxs-lookup"><span data-stu-id="8cf0e-120">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    - <span data-ttu-id="8cf0e-121">Voer een geteld bedrag op elke regel in als het moet worden ingevoerd of bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="8cf0e-121">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="8cf0e-122">Het getelde veld wordt gevuld met bedragen van kascontroles die in POS zijn uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="8cf0e-122">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="8cf0e-123">Selecteer **Overzicht boeken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="8cf0e-123">Select **Post statement** from the Action Pane.</span></span>
10. <span data-ttu-id="8cf0e-124">Selecteer **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="8cf0e-124">Select **Close**.</span></span>
11. <span data-ttu-id="8cf0e-125">Sluit het deelvenster.</span><span class="sxs-lookup"><span data-stu-id="8cf0e-125">Close the pane.</span></span>
12. <span data-ttu-id="8cf0e-126">Selecteer **Financiën van detailhandelwinkel** op de startpagina.</span><span class="sxs-lookup"><span data-stu-id="8cf0e-126">At the home page, select **Retail store financials**.</span></span>
13. <span data-ttu-id="8cf0e-127">Selecteer het tabblad **Geboekte overzichten**.</span><span class="sxs-lookup"><span data-stu-id="8cf0e-127">Select the **Posted statements** tab.</span></span>

