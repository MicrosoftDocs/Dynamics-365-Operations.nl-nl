---
title: Afschrijvingsconventies voor meerdere vaste activa wijzigen
description: Deze taak werkt de afschrijvingsconventie voor een opgegeven vaste-activagroep bij.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21baf3692cbcb87f6ed37459848376a1fa87a438
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177138"
---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a><span data-ttu-id="be53c-103">Afschrijvingsconventies voor meerdere vaste activa wijzigen</span><span class="sxs-lookup"><span data-stu-id="be53c-103">Change depreciation conventions for multiple fixed assets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="be53c-104">Deze taak werkt de afschrijvingsconventie voor een opgegeven vaste-activagroep bij.</span><span class="sxs-lookup"><span data-stu-id="be53c-104">This task updates the depreciation convention for a specified fixed asset group.</span></span> <span data-ttu-id="be53c-105">Bij deze taakbegeleiding wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="be53c-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="be53c-106">Ga naar Vaste activa > Periodieke taken > Groepsgewijs bijwerken</span><span class="sxs-lookup"><span data-stu-id="be53c-106">Go to Fixed assets > Periodic tasks > Mass update</span></span>
2. <span data-ttu-id="be53c-107">Klik in het veld Afschrijvingsboek op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="be53c-107">In the Depreciation book field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="be53c-108">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="be53c-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="be53c-109">Voer in het veld Begindatum in gebruik genomen een datum in.</span><span class="sxs-lookup"><span data-stu-id="be53c-109">In the Placed in service start field, enter a date.</span></span>
5. <span data-ttu-id="be53c-110">Voer in het veld Einddatum in gebruik genomen een datum in.</span><span class="sxs-lookup"><span data-stu-id="be53c-110">In the Placed in service end field, enter a date.</span></span>
    * <span data-ttu-id="be53c-111">Alleen activa die onderdeel zijn van het geselecteerde afschrijvingsboek en die u tussen die datums in gebruik hebt genomen, worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="be53c-111">Only assets that are a part of the select depreciation book and that have been placed in service between these dates will be updated.</span></span>  
6. <span data-ttu-id="be53c-112">Selecteer in het veld Huidige afschrijvingsconventie een optie.</span><span class="sxs-lookup"><span data-stu-id="be53c-112">In the Current depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="be53c-113">Alleen de activa die de huidige afschrijvingsconventie hebben worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="be53c-113">Only assets that have the current depreciation convention will be updated.</span></span>  
7. <span data-ttu-id="be53c-114">Selecteer in het veld Nieuwe afschrijvingsconventie een optie.</span><span class="sxs-lookup"><span data-stu-id="be53c-114">In the New depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="be53c-115">Controleer of het rapport naar de gewenste bestemming wordt afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="be53c-115">Verify the report will print to the desired destination.</span></span>  
8. <span data-ttu-id="be53c-116">Breid de sectie Op te nemen records uit.</span><span class="sxs-lookup"><span data-stu-id="be53c-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="be53c-117">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="be53c-117">Click Filter.</span></span>
10. <span data-ttu-id="be53c-118">Selecteer de vaste-activagroep in de lijst.</span><span class="sxs-lookup"><span data-stu-id="be53c-118">In the list, select the Fixed asset group.</span></span>
11. <span data-ttu-id="be53c-119">Klik in het veld Criteria op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="be53c-119">In the Criteria field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="be53c-120">Selecteer de gewenste vaste-activagroep.</span><span class="sxs-lookup"><span data-stu-id="be53c-120">Select the desired Fixed asset group.</span></span>
13. <span data-ttu-id="be53c-121">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="be53c-121">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="be53c-122">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="be53c-122">Click OK.</span></span>
15. <span data-ttu-id="be53c-123">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="be53c-123">Click OK.</span></span>
    *  <span data-ttu-id="be53c-124">De resultaten van het proces worden weergegeven in het rapport Groepsgewijs bijwerken.</span><span class="sxs-lookup"><span data-stu-id="be53c-124">Results of the process are shown on the Mass update report.</span></span>     

