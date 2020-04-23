---
title: Bijkomende opdrachten instellen
description: Deze procedure laat zien hoe u een bijkomende toewijzing instelt.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9c86461f980112e2d759dfd0c905ae2ef05e7041
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214982"
---
# <a name="set-up-accessorial-assignments"></a><span data-ttu-id="febba-103">Bijkomende opdrachten instellen</span><span class="sxs-lookup"><span data-stu-id="febba-103">Set up accessorial assignments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="febba-104">Deze procedure laat zien hoe u een bijkomende toewijzing instelt.</span><span class="sxs-lookup"><span data-stu-id="febba-104">This procedure shows how to set up an accessorial assignment.</span></span> <span data-ttu-id="febba-105">Dit wordt gewoonlijk gedaan door een transportcoördinator.</span><span class="sxs-lookup"><span data-stu-id="febba-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="febba-106">Voordat u deze handleiding gebruikt, moet u de handleiding "Bijkomende toeslagen van hub en modellen voor extra's instellen" uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="febba-106">Before you use this guide you need to run the "Set up hub accessorial charges and accessorial masters" guide.</span></span>


## <a name="set-up-accessorial-assignment"></a><span data-ttu-id="febba-107">Toewijzing van extra's instellen</span><span class="sxs-lookup"><span data-stu-id="febba-107">Set up Accessorial assignment</span></span>
1. <span data-ttu-id="febba-108">Ga naar Transportbeheer > Instellingen > Beoordeling > Bijkomende toewijzingen.</span><span class="sxs-lookup"><span data-stu-id="febba-108">Go to Transportation management > Setup > Rating > Accessorial assignments.</span></span>
2. <span data-ttu-id="febba-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="febba-109">Click New.</span></span>
3. <span data-ttu-id="febba-110">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="febba-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="febba-111">Schakel de uitbreiding van de sectie Details om.</span><span class="sxs-lookup"><span data-stu-id="febba-111">Toggle the expansion of the Details section.</span></span>
5. <span data-ttu-id="febba-112">Klik in het veld Hub op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="febba-112">In the Hub field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="febba-113">Selecteer in de lijst de hub waarvoor u een bijkomend model hebt gemaakt bij het uitvoeren van de handleiding "Bijkomende toeslagen van hub en modellen voor extra's instellen".</span><span class="sxs-lookup"><span data-stu-id="febba-113">In the list, select the Hub that you created an accessorial master for when you ran the "Set up hub accessorial charges and accessorial masters" guide.</span></span> 
7. <span data-ttu-id="febba-114">Klik in het veld Id extra's hub op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="febba-114">In the Hub accessorial ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="febba-115">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="febba-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="febba-116">Schakel de uitbreiding van de sectie Criteria om.</span><span class="sxs-lookup"><span data-stu-id="febba-116">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="febba-117">In de sectie Criteria kunt u de exacte criteria kiezen voor wanneer de toeslag moet gelden, op basis van de verschillende waarden die hier worden aangeboden.</span><span class="sxs-lookup"><span data-stu-id="febba-117">In the Criteria section you can choose the exact criteria for when the charge should apply, based on the different values offered here.</span></span>  
10. <span data-ttu-id="febba-118">Stel de optie Altijd toepassen in op Ja.</span><span class="sxs-lookup"><span data-stu-id="febba-118">Set the Always apply option to Yes.</span></span>
11. <span data-ttu-id="febba-119">Selecteer een optie in het veld Toewijzingsniveau van extra's.</span><span class="sxs-lookup"><span data-stu-id="febba-119">In the Accessorial assignment level field, select an option.</span></span>
12. <span data-ttu-id="febba-120">Schakel de uitbreiding van de sectie Berekening om.</span><span class="sxs-lookup"><span data-stu-id="febba-120">Toggle the expansion of the Calculation section.</span></span>
13. <span data-ttu-id="febba-121">Selecteer "Vast" in het veld type bijzondere kosten.</span><span class="sxs-lookup"><span data-stu-id="febba-121">In the Accessorial fee type field, select 'Flat'.</span></span>
    * <span data-ttu-id="febba-122">Het type bijzondere kosten s bepaalt hoe de feitelijke toeslag moet worden berekend.</span><span class="sxs-lookup"><span data-stu-id="febba-122">The Accessorial fee type determines how to calculate the actual charge.</span></span> <span data-ttu-id="febba-123">In dit voorbeeld is het een vaste toeslag.</span><span class="sxs-lookup"><span data-stu-id="febba-123">In this example it's a flat charge.</span></span>  
14. <span data-ttu-id="febba-124">Typ een getal in het veld Bijzondere kosten.</span><span class="sxs-lookup"><span data-stu-id="febba-124">In the Accessorial fee field, enter a number.</span></span>
15. <span data-ttu-id="febba-125">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="febba-125">Click Save.</span></span>

