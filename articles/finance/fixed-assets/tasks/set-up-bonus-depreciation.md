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
ms.openlocfilehash: 6627e7fa9a1eb1a9131ec7e2c3cc823b49b286cc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257556"
---
# <a name="set-up-bonus-depreciation"></a><span data-ttu-id="13042-103">Bonusafschrijving instellen</span><span class="sxs-lookup"><span data-stu-id="13042-103">Set up bonus depreciation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="13042-104">In deze procedure ziet u hoe u een speciale afschrijvingsaftrek maakt en deze koppelt aan een vaste-activaboek.</span><span class="sxs-lookup"><span data-stu-id="13042-104">This procedure shows how to create a special depreciation allowance and associate it with a fixed asset book.</span></span> <span data-ttu-id="13042-105">Het gebruikt de rol Accountant en demogegevens voor de USMF-rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="13042-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-special-depreciation-allowance"></a><span data-ttu-id="13042-106">Een speciale afschrijvingsaftrek maken</span><span class="sxs-lookup"><span data-stu-id="13042-106">Create a special depreciation allowance</span></span>
1. <span data-ttu-id="13042-107">Ga naar Vaste activa > Instellingen > Speciale afschrijvingsaftrek.</span><span class="sxs-lookup"><span data-stu-id="13042-107">Go to Fixed assets > Setup > Special depreciation allowance.</span></span>
2. <span data-ttu-id="13042-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="13042-108">Click New.</span></span>
3. <span data-ttu-id="13042-109">Typ een waarde in het veld Speciale afschrijvingsaftrek.</span><span class="sxs-lookup"><span data-stu-id="13042-109">In the Special depreciation allowance field, type a value.</span></span>
4. <span data-ttu-id="13042-110">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="13042-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="13042-111">Voer een getal in het veld Percentage in.</span><span class="sxs-lookup"><span data-stu-id="13042-111">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="13042-112">Als geen percentage wordt vermeld, voert u een bedrag in.</span><span class="sxs-lookup"><span data-stu-id="13042-112">If a percentage was not indicated, set an amount.</span></span>  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a><span data-ttu-id="13042-113">Een speciale afschrijvingsaftrek koppelen aan een boek voor een groep vaste activa</span><span class="sxs-lookup"><span data-stu-id="13042-113">Associate a special depreciation allowance with a fixed asset group book</span></span>
1. <span data-ttu-id="13042-114">Ga naar Vaste activa > Instellingen > Vaste-activagroepen.</span><span class="sxs-lookup"><span data-stu-id="13042-114">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="13042-115">Selecteer in de lijst de vaste-activagroep die is gekoppeld aan de speciale afschrijvingsaftrek.</span><span class="sxs-lookup"><span data-stu-id="13042-115">In the list, select the fixed asset group associated with the special depreciation allowance.</span></span>
3. <span data-ttu-id="13042-116">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="13042-116">Click Books.</span></span>
4. <span data-ttu-id="13042-117">Selecteer in de lijst het boek dat aan de speciale afschrijvingsaftrek is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="13042-117">In the list, select the book that is associated with the special depreciation allowance.</span></span>
5. <span data-ttu-id="13042-118">Klik op Speciale afschrijvingsaftrek.</span><span class="sxs-lookup"><span data-stu-id="13042-118">Click Special depreciation allowance.</span></span>
6. <span data-ttu-id="13042-119">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="13042-119">Click New.</span></span>
7. <span data-ttu-id="13042-120">Typ of selecteer een waarde in het veld Speciale afschrijvingsaftrek.</span><span class="sxs-lookup"><span data-stu-id="13042-120">In the Special depreciation allowance field, enter or select a value.</span></span>
    * <span data-ttu-id="13042-121">De standaardwaarde voor Percentage of Bedrag komt uit de speciale afschrijvingsaftrekinstelling.</span><span class="sxs-lookup"><span data-stu-id="13042-121">The default for Percentage or Amount comes from the special depreciation allowance setup.</span></span>  
8. <span data-ttu-id="13042-122">Voer een getal in het veld Prioriteit in.</span><span class="sxs-lookup"><span data-stu-id="13042-122">In the Priority field, enter a number.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]