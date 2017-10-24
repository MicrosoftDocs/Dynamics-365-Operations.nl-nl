--- 
title: " Door machine learning aangestuurde productaanbevelingen configureren"
description: Deze procedure vernieuwt de gegevens in de Entiteitopslag die wordt gebruikt door het leersysteem van de machine dat productaanbevelingen genereert, en schakelt productaanbevelingen op POS-clients in.
author: ashishmsft
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e32c7cf1283487cb7a52f7d8e261b6b587b76364
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="configure-machine-learning-powered-product-recommendations"></a><span data-ttu-id="08b8f-103"> Door machine learning aangestuurde productaanbevelingen configureren</span><span class="sxs-lookup"><span data-stu-id="08b8f-103">Configure machine learning-powered product recommendations</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="08b8f-104">Deze procedure vernieuwt de gegevens in de Entiteitopslag die wordt gebruikt door het leersysteem van de machine dat productaanbevelingen genereert, en schakelt productaanbevelingen op POS-clients in.</span><span class="sxs-lookup"><span data-stu-id="08b8f-104">This procedure refreshes the data in the Entity store that is used by the machine learning system that powers product recommendations, and then enables product recommendations on POS clients.</span></span> <span data-ttu-id="08b8f-105">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="08b8f-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="08b8f-106">Ga naar Systeembeheer > Instellingen > Entiteitopslag.</span><span class="sxs-lookup"><span data-stu-id="08b8f-106">Go to System administration > Setup > Entity Store.</span></span>
2. <span data-ttu-id="08b8f-107">Zoek en selecteer de gewenste record RetailSales in de lijst.</span><span class="sxs-lookup"><span data-stu-id="08b8f-107">In the list, find and select the record 'RetailSales'.</span></span>
3. <span data-ttu-id="08b8f-108">Klik op Vernieuwen.</span><span class="sxs-lookup"><span data-stu-id="08b8f-108">Click Refresh.</span></span>
4. <span data-ttu-id="08b8f-109">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="08b8f-109">Click OK.</span></span>
5. <span data-ttu-id="08b8f-110">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="08b8f-110">Close the page.</span></span>
6. <span data-ttu-id="08b8f-111">Ga naar Detailhandel en commerce > Instelling van hoofdkantoor > Parameters > Detailhandelparameters.</span><span class="sxs-lookup"><span data-stu-id="08b8f-111">Go to Retail and commerce > Headquarters setup > Parameters > Retail parameters.</span></span>
7. <span data-ttu-id="08b8f-112">Klik op het tabblad Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="08b8f-112">Click the Machine learning tab.</span></span>
8. <span data-ttu-id="08b8f-113">Selecteer Ja in het veld Productaanbevelingen inschakelen.</span><span class="sxs-lookup"><span data-stu-id="08b8f-113">Select 'Yes' in the Enable product recommendations field.</span></span>
    * <span data-ttu-id="08b8f-114">Als u het bericht "Kan de aanbevelingsmodellen niet ophalen" ziet, komt dat doordat u de entiteitopslag zeer onlangs hebt vernieuwd en het systeem mogelijk niet gereed is met het assimileren van de nieuwe gegevens.</span><span class="sxs-lookup"><span data-stu-id="08b8f-114">If you receive the message "The recommendation models couldn't be retrieved", it’s because you refreshed the Entity Store very recently and the system may not have finished assimilating the new data.</span></span> <span data-ttu-id="08b8f-115">Wacht 2-3 uur en probeer het opnieuw.</span><span class="sxs-lookup"><span data-stu-id="08b8f-115">Wait 2-3 hours and try again.</span></span>  
9. <span data-ttu-id="08b8f-116">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="08b8f-116">Click Save.</span></span>
10. <span data-ttu-id="08b8f-117">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="08b8f-117">Close the page.</span></span>


