---
title: Een productieorder gereedmelden
description: Deze procedure toont aan hoe u een productieorder gereedmeldt.
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: e6f5e7316f89ba7c2b7091eb9df02aa07ea44dbd
ms.contentlocale: nl-nl
ms.lasthandoff: 02/06/2018

---
# <a name="report-a-production-order-as-finished"></a><span data-ttu-id="0a838-103">Een productieorder gereedmelden</span><span class="sxs-lookup"><span data-stu-id="0a838-103">Report a production order as finished</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0a838-104">Deze procedure toont aan hoe u een productieorder gereedmeldt.</span><span class="sxs-lookup"><span data-stu-id="0a838-104">This procedure shows how to report a production order as finished.</span></span> <span data-ttu-id="0a838-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="0a838-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="0a838-106">Dit is de zesde procedure van zeven die de productieorderlevenscyclus beschrijven.</span><span class="sxs-lookup"><span data-stu-id="0a838-106">This is the sixth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="report-a-production-order-as-finished"></a><span data-ttu-id="0a838-107">Een productieorder gereedmelden</span><span class="sxs-lookup"><span data-stu-id="0a838-107">Report a production order as finished</span></span>
1. <span data-ttu-id="0a838-108">Ga naar Productiebeheer > Productieorders > Alle productieorders.</span><span class="sxs-lookup"><span data-stu-id="0a838-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="0a838-109">Selecteer een productieorder met de status Gestart.</span><span class="sxs-lookup"><span data-stu-id="0a838-109">Select a production order that has the Started status.</span></span>  
2. <span data-ttu-id="0a838-110">Klik in het actievenster op Productieorder.</span><span class="sxs-lookup"><span data-stu-id="0a838-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="0a838-111">Klik op Gereedmelden.</span><span class="sxs-lookup"><span data-stu-id="0a838-111">Click Report as finished.</span></span>
    * <span data-ttu-id="0a838-112">Op deze pagina kunt u de hoeveelheid bevestigen van het eindproduct die moet worden gereedgemeld.</span><span class="sxs-lookup"><span data-stu-id="0a838-112">On this page, you can confirm the quantity of the finished product to be reported as finished.</span></span>  
4. <span data-ttu-id="0a838-113">Klik op het tabblad Algemeen.</span><span class="sxs-lookup"><span data-stu-id="0a838-113">Click the General tab.</span></span>
5. <span data-ttu-id="0a838-114">Stel Goede hoeveelheid in op '18'.</span><span class="sxs-lookup"><span data-stu-id="0a838-114">Set Good quantity to '18'.</span></span>
6. <span data-ttu-id="0a838-115">Stel Slechte hoeveelheid in op '2'.</span><span class="sxs-lookup"><span data-stu-id="0a838-115">Set Error quantity to '2'.</span></span>
7. <span data-ttu-id="0a838-116">Selecteer 'Materiaal' in het veld Foutoorzaak.</span><span class="sxs-lookup"><span data-stu-id="0a838-116">In the Error cause field, select 'Material'.</span></span>
8. <span data-ttu-id="0a838-117">Schakel selectievakje Taak beëindigen in of uit.</span><span class="sxs-lookup"><span data-stu-id="0a838-117">Select or clear the End job check box.</span></span>
9. <span data-ttu-id="0a838-118">Schakel het selectievakje Fout accepteren in of uit.</span><span class="sxs-lookup"><span data-stu-id="0a838-118">Select or clear the Accept error check box.</span></span>
10. <span data-ttu-id="0a838-119">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="0a838-119">Click OK.</span></span>

## <a name="verify-the-report-as-finished-journal"></a><span data-ttu-id="0a838-120">Het gereedmeldingsjournaal verifiëren</span><span class="sxs-lookup"><span data-stu-id="0a838-120">Verify the Report as finished journal</span></span>
1. <span data-ttu-id="0a838-121">Klik in het actievenster op Weergeven.</span><span class="sxs-lookup"><span data-stu-id="0a838-121">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="0a838-122">Klik op Gereedgemeld.</span><span class="sxs-lookup"><span data-stu-id="0a838-122">Click Reported as finished.</span></span>
3. <span data-ttu-id="0a838-123">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="0a838-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="0a838-124">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="0a838-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0a838-125">Het gereedmeldingsjournaal is geboekt.</span><span class="sxs-lookup"><span data-stu-id="0a838-125">The Report as finished journal is posted.</span></span> <span data-ttu-id="0a838-126">Als u aan het journaal correcties wilt aanbrengen, kunt u handmatig een nieuw journaal maken waarin u wijzigingen kunt aanbrengen.</span><span class="sxs-lookup"><span data-stu-id="0a838-126">If you want to make adjustments to the journal, you can manually create  a new journal where you can make changes.</span></span>  

