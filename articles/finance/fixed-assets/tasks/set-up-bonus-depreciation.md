---
title: Bonusafschrijving instellen
description: In deze procedure ziet u hoe u een speciale afschrijvingsaftrek maakt en deze koppelt aan een vaste-activaboek.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7fed9f09b4e37da00a5d78fa088e8814db48456b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968924"
---
# <a name="set-up-bonus-depreciation"></a><span data-ttu-id="06781-103">Bonusafschrijving instellen</span><span class="sxs-lookup"><span data-stu-id="06781-103">Set up bonus depreciation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="06781-104">In deze procedure ziet u hoe u een speciale afschrijvingsaftrek maakt en deze koppelt aan een vaste-activaboek.</span><span class="sxs-lookup"><span data-stu-id="06781-104">This procedure shows how to create a special depreciation allowance and associate it with a fixed asset book.</span></span> <span data-ttu-id="06781-105">Het gebruikt de rol Accountant en demogegevens voor de USMF-rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="06781-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-special-depreciation-allowance"></a><span data-ttu-id="06781-106">Een speciale afschrijvingsaftrek maken</span><span class="sxs-lookup"><span data-stu-id="06781-106">Create a special depreciation allowance</span></span>
1. <span data-ttu-id="06781-107">Ga naar Vaste activa > Instellingen > Speciale afschrijvingsaftrek.</span><span class="sxs-lookup"><span data-stu-id="06781-107">Go to Fixed assets > Setup > Special depreciation allowance.</span></span>
2. <span data-ttu-id="06781-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="06781-108">Click New.</span></span>
3. <span data-ttu-id="06781-109">Typ een waarde in het veld Speciale afschrijvingsaftrek.</span><span class="sxs-lookup"><span data-stu-id="06781-109">In the Special depreciation allowance field, type a value.</span></span>
4. <span data-ttu-id="06781-110">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="06781-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="06781-111">Voer een getal in het veld Percentage in.</span><span class="sxs-lookup"><span data-stu-id="06781-111">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="06781-112">Als geen percentage wordt vermeld, voert u een bedrag in.</span><span class="sxs-lookup"><span data-stu-id="06781-112">If a percentage was not indicated, set an amount.</span></span>  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a><span data-ttu-id="06781-113">Een speciale afschrijvingsaftrek koppelen aan een boek voor een groep vaste activa</span><span class="sxs-lookup"><span data-stu-id="06781-113">Associate a special depreciation allowance with a fixed asset group book</span></span>
1. <span data-ttu-id="06781-114">Ga naar Vaste activa > Instellingen > Vaste-activagroepen.</span><span class="sxs-lookup"><span data-stu-id="06781-114">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="06781-115">Selecteer in de lijst de vaste-activagroep die is gekoppeld aan de speciale afschrijvingsaftrek.</span><span class="sxs-lookup"><span data-stu-id="06781-115">In the list, select the fixed asset group associated with the special depreciation allowance.</span></span>
3. <span data-ttu-id="06781-116">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="06781-116">Click Books.</span></span>
4. <span data-ttu-id="06781-117">Selecteer in de lijst het boek dat aan de speciale afschrijvingsaftrek is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="06781-117">In the list, select the book that is associated with the special depreciation allowance.</span></span>
5. <span data-ttu-id="06781-118">Klik op Speciale afschrijvingsaftrek.</span><span class="sxs-lookup"><span data-stu-id="06781-118">Click Special depreciation allowance.</span></span>
6. <span data-ttu-id="06781-119">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="06781-119">Click New.</span></span>
7. <span data-ttu-id="06781-120">Typ of selecteer een waarde in het veld Speciale afschrijvingsaftrek.</span><span class="sxs-lookup"><span data-stu-id="06781-120">In the Special depreciation allowance field, enter or select a value.</span></span>
    * <span data-ttu-id="06781-121">De standaardwaarde voor Percentage of Bedrag komt uit de speciale afschrijvingsaftrekinstelling.</span><span class="sxs-lookup"><span data-stu-id="06781-121">The default for Percentage or Amount comes from the special depreciation allowance setup.</span></span>  
8. <span data-ttu-id="06781-122">Voer een getal in het veld Prioriteit in.</span><span class="sxs-lookup"><span data-stu-id="06781-122">In the Priority field, enter a number.</span></span>

