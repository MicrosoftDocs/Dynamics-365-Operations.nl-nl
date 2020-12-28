---
title: Bijkomende toeslagen van hub en modellen voor extra's instellen
description: Deze procedure laat zien hoe u een model van extra's voor een hub kunt maken en dat model kunt gebruiken om een bijkomende toeslag van hub te maken.
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSCarrierAccessorial,TMSAccessorialMaster, TMSHubAccessorial
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad89afe0a21261c57311c439153b969d837748e4
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/29/2020
ms.locfileid: "4425904"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a><span data-ttu-id="9efd7-103">Bijkomende toeslagen van hub en modellen voor extra's instellen</span><span class="sxs-lookup"><span data-stu-id="9efd7-103">Set up hub accessorial charges and accessorial masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9efd7-104">Deze procedure laat zien hoe u een model van extra's voor een hub kunt maken en dat model kunt gebruiken om een bijkomende toeslag van hub te maken.</span><span class="sxs-lookup"><span data-stu-id="9efd7-104">This procedure shows how to create an accessorial master for a hub and use that master to create a hub accessorial charge.</span></span> <span data-ttu-id="9efd7-105">De procedure gebruikt de USMF-dataset.</span><span class="sxs-lookup"><span data-stu-id="9efd7-105">The procedure uses the USMF dataset.</span></span> <span data-ttu-id="9efd7-106">Deze instellingen worden gewoonlijk uitgevoerd door een transportcoördinator.</span><span class="sxs-lookup"><span data-stu-id="9efd7-106">This set up will typically be done by a transportation coordinator.</span></span>


## <a name="set-up-a-hub-master"></a><span data-ttu-id="9efd7-107">Een model voor een hub instellen</span><span class="sxs-lookup"><span data-stu-id="9efd7-107">Set up a hub master</span></span>
1. <span data-ttu-id="9efd7-108">Ga naar Transportbeheer > Instellingen > Beoordeling > Modellen van extra's.</span><span class="sxs-lookup"><span data-stu-id="9efd7-108">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="9efd7-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="9efd7-109">Click New.</span></span>
3. <span data-ttu-id="9efd7-110">Typ een waarde in het veld Model van extra's.</span><span class="sxs-lookup"><span data-stu-id="9efd7-110">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="9efd7-111">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9efd7-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="9efd7-112">Selecteer "Hub" in het veld Type van extra's.</span><span class="sxs-lookup"><span data-stu-id="9efd7-112">In the Accessorial type field, select 'Hub'.</span></span>
6. <span data-ttu-id="9efd7-113">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="9efd7-113">Click Save.</span></span>
7. <span data-ttu-id="9efd7-114">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="9efd7-114">Close the page.</span></span>

## <a name="set-up-a-hub-accessorial-charge"></a><span data-ttu-id="9efd7-115">Een extra toeslag van hub instellen</span><span class="sxs-lookup"><span data-stu-id="9efd7-115">Set up a hub accessorial charge</span></span>
1. <span data-ttu-id="9efd7-116">Ga naar Transportbeheer > Instellingen > Beoordeling > Toeslag extra's hub.</span><span class="sxs-lookup"><span data-stu-id="9efd7-116">Go to Transportation management > Setup > Rating > Hub accessorial charges.</span></span>
2. <span data-ttu-id="9efd7-117">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="9efd7-117">Click New.</span></span>
3. <span data-ttu-id="9efd7-118">Typ een waarde in het veld Id extra's hub.</span><span class="sxs-lookup"><span data-stu-id="9efd7-118">In the Hub accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="9efd7-119">Klik in het veld Hub op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="9efd7-119">In the Hub field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="9efd7-120">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="9efd7-120">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="9efd7-121">Selecteer een optie in het veld Hubpositie.</span><span class="sxs-lookup"><span data-stu-id="9efd7-121">In the Hub position field, select an option.</span></span>
    * <span data-ttu-id="9efd7-122">U kunt de toeslag maken voor ophalen of afleveren.</span><span class="sxs-lookup"><span data-stu-id="9efd7-122">You can either create the charge as a pickup or drop-off.</span></span> <span data-ttu-id="9efd7-123">Afhankelijk van uw selectie wordt de toeslag toegepast op het bijbehorende transportsegment op uw route.</span><span class="sxs-lookup"><span data-stu-id="9efd7-123">Depending on your selection the charge will be applied to the corresponding transportation segment on your route.</span></span>  
7. <span data-ttu-id="9efd7-124">Klik in het veld Model van extra's op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="9efd7-124">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="9efd7-125">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="9efd7-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9efd7-126">Selecteer het model dat u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="9efd7-126">Select the master you just created.</span></span>  
9. <span data-ttu-id="9efd7-127">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="9efd7-127">Click Save.</span></span>
10. <span data-ttu-id="9efd7-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="9efd7-128">Close the page.</span></span>

