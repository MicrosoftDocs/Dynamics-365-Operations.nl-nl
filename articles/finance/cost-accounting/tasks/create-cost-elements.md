---
title: Kostenelementen maken
description: Er zijn verschillende manieren om kostenelementen in Kostprijsboekhouding te maken.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11107993fe91e39409ccf06615a21574ad51d079
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236813"
---
# <a name="create-cost-elements"></a><span data-ttu-id="b7d36-103">Kostenelementen maken</span><span class="sxs-lookup"><span data-stu-id="b7d36-103">Create cost elements</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b7d36-104">Er zijn verschillende manieren om kostenelementen in Kostprijsboekhouding te maken.</span><span class="sxs-lookup"><span data-stu-id="b7d36-104">There are several ways to create cost elements in Cost accounting.</span></span> <span data-ttu-id="b7d36-105">Deze procedure laat zien hoe u kostenelementen maakt door hoofdrekeningen te importeren via een gegevensconnector.</span><span class="sxs-lookup"><span data-stu-id="b7d36-105">This procedure shows how to create cost elements by importing main accounts via a data connector.</span></span> <span data-ttu-id="b7d36-106">Het demobedrijf USMF wordt gebruikt om deze procedure te maken.</span><span class="sxs-lookup"><span data-stu-id="b7d36-106">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="b7d36-107">Deze procedure is voor een functie van Kostprijsboekhouding die in Dynamics 365 for Operations, versie 1611 is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="b7d36-107">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-elements"></a><span data-ttu-id="b7d36-108">Nieuwe kostenelementen maken</span><span class="sxs-lookup"><span data-stu-id="b7d36-108">Create new cost elements</span></span>
1. <span data-ttu-id="b7d36-109">Ga naar Kostprijsboekhouding > Dimensies > Dimensies van kostenelement.</span><span class="sxs-lookup"><span data-stu-id="b7d36-109">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="b7d36-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="b7d36-110">Click New.</span></span>
3. <span data-ttu-id="b7d36-111">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="b7d36-111">In the Name field, type a value.</span></span>
4. <span data-ttu-id="b7d36-112">Typ of selecteer een waarde in het veld Gegevensconnector voor dimensieleden.</span><span class="sxs-lookup"><span data-stu-id="b7d36-112">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="b7d36-113">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="b7d36-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="b7d36-114">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b7d36-114">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="b7d36-115">De gegevensconnector configureren</span><span class="sxs-lookup"><span data-stu-id="b7d36-115">Configure the data connector</span></span>
1. <span data-ttu-id="b7d36-116">Klik op Dimensielidprovider configureren.</span><span class="sxs-lookup"><span data-stu-id="b7d36-116">Click Configure dimension member provider.</span></span>
2. <span data-ttu-id="b7d36-117">Typ of selecteer een waarde in het veld Rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="b7d36-117">In the Chart of accounts field, enter or select a value.</span></span>
    * <span data-ttu-id="b7d36-118">Selecteer Gedeeld om het gedeelde rekeningschema te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="b7d36-118">Select Shared to use the shared chart of accounts.</span></span>  
3. <span data-ttu-id="b7d36-119">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="b7d36-119">Click New.</span></span>
4. <span data-ttu-id="b7d36-120">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b7d36-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b7d36-121">U kunt filters op rekeningen toepassen om aan de criteria te voldoen.</span><span class="sxs-lookup"><span data-stu-id="b7d36-121">You can apply filters to accounts to meet your criteria.</span></span>  
5. <span data-ttu-id="b7d36-122">Typ of selecteer een waarde in het veld Van hoofdrekening.</span><span class="sxs-lookup"><span data-stu-id="b7d36-122">In the From main account field, enter or select a value.</span></span>
6. <span data-ttu-id="b7d36-123">Typ of selecteer een waarde in het veld Naar hoofdrekening.</span><span class="sxs-lookup"><span data-stu-id="b7d36-123">In the To main account field, enter or select a value.</span></span>
7. <span data-ttu-id="b7d36-124">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b7d36-124">Click OK.</span></span>

## <a name="import-main-accounts"></a><span data-ttu-id="b7d36-125">Hoofdrekeningen importeren</span><span class="sxs-lookup"><span data-stu-id="b7d36-125">Import main accounts</span></span>
1. <span data-ttu-id="b7d36-126">Klik op Dimensieleden importeren.</span><span class="sxs-lookup"><span data-stu-id="b7d36-126">Click Import dimension members.</span></span>
    * <span data-ttu-id="b7d36-127">Hoofdrekeningen worden in Kostprijsboekhouding geïmporteerd en gebruikt als kostenelementen.</span><span class="sxs-lookup"><span data-stu-id="b7d36-127">Main accounts will be imported into Cost accounting and used as cost elements.</span></span>  
2. <span data-ttu-id="b7d36-128">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b7d36-128">Click OK.</span></span>

## <a name="view-the-imported-accounts-as-cost-elements"></a><span data-ttu-id="b7d36-129">De geïmporteerde rekeningen als kostenelementen weergeven</span><span class="sxs-lookup"><span data-stu-id="b7d36-129">View the imported accounts as cost elements</span></span>
1. <span data-ttu-id="b7d36-130">Klik op Dimensieleden weergeven.</span><span class="sxs-lookup"><span data-stu-id="b7d36-130">Click View dimension members.</span></span>
    * <span data-ttu-id="b7d36-131">Geef in uw bedrijf de geïmporteerde grootboekrekeningen als kostenelementen weer om de kosten daarnaartoe te laten stromen.</span><span class="sxs-lookup"><span data-stu-id="b7d36-131">View the imported ledger accounts as cost elements in your business that costs can flow to.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]