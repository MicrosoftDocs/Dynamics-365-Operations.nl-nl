---
title: Afschrijving vaste activa
description: Dit onderwerp bevat een overzicht van de afschrijving van vaste activa.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87317eedad06e93625212df3cc6e017b9475c932
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240989"
---
# <a name="fixed-asset-depreciation"></a><span data-ttu-id="675af-103">Afschrijving vaste activa</span><span class="sxs-lookup"><span data-stu-id="675af-103">Fixed asset depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="675af-104">Dit onderwerp bevat een overzicht van de afschrijving van vaste activa.</span><span class="sxs-lookup"><span data-stu-id="675af-104">This topic provides an overview of depreciation for fixed assets.</span></span>

<span data-ttu-id="675af-105">Afschrijving is een periodieke transactie die doorgaans de waarde van het vaste activum in de balans verlaagt en als uitgave in een winst-en-verliesrekening wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="675af-105">Depreciation is a periodic transaction that typically reduces the value of the fixed asset on the balance sheet, and is charged as an expenditure to a profit and loss account.</span></span> <span data-ttu-id="675af-106">Daarom wordt een hoofdrekening gewoonlijk gebruikt voor de creditering van de periodieke afschrijving op de balans.</span><span class="sxs-lookup"><span data-stu-id="675af-106">Therefore, a main account is typically used to credit the periodic depreciation on the balance sheet.</span></span> <span data-ttu-id="675af-107">Een tegenrekening is een rekening in het winst-en verliesgedeelte van het rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="675af-107">An offset account is an account in the profit and loss part of the chart of accounts.</span></span>

## <a name="depreciation-adjustment"></a><span data-ttu-id="675af-108">Afschrijvingscorrectie</span><span class="sxs-lookup"><span data-stu-id="675af-108">Depreciation adjustment</span></span>
<span data-ttu-id="675af-109">Doorgaans wordt alleen een correctie op een geboekte afschrijvingstransactie geboekt als een afschrijvingsaanpassing.</span><span class="sxs-lookup"><span data-stu-id="675af-109">Usually, only a correction to a posted depreciation transaction is posted as a depreciation adjustment.</span></span> <span data-ttu-id="675af-110">Daarom worden zowel de hoofdrekening als de tegenrekening ingesteld als de rekeningen voor de afschrijving.</span><span class="sxs-lookup"><span data-stu-id="675af-110">Therefore, both the main account and the offset account are set up just like the accounts for depreciation.</span></span> <span data-ttu-id="675af-111">Een afschrijvingscorrectie kan een positief of negatief bedrag zijn, maar de functies van de hoofdrekening (als balansrekening) en van de tegenrekening (meestal als een winst-en-verliesrekening) blijven hetzelfde.</span><span class="sxs-lookup"><span data-stu-id="675af-111">A depreciation adjustment can be either a positive amount or a negative amount, but the functionality of the main account (as a balance sheet account) and the functionality of the offset account (usually as a profit and loss account) remain the same.</span></span>

## <a name="extraordinary-depreciation"></a><span data-ttu-id="675af-112">Buitengewone afschrijving</span><span class="sxs-lookup"><span data-stu-id="675af-112">Extraordinary depreciation</span></span>
<span data-ttu-id="675af-113">Buitengewone afschrijving werkt hetzelfde als gewone afschrijving.</span><span class="sxs-lookup"><span data-stu-id="675af-113">Extraordinary depreciation works like basic depreciation.</span></span> <span data-ttu-id="675af-114">Daarom wordt een hoofdrekening gebruikt om het afschrijvingsbedrag naar de balans te crediteren en de waarde van het vaste activum te verminderen.</span><span class="sxs-lookup"><span data-stu-id="675af-114">Therefore, a main account is used to credit the depreciation amount to the balance sheet and reduce the value of the fixed asset.</span></span> <span data-ttu-id="675af-115">Een tegenrekening is een winst-en verliesrekening, waar de afschrijving die is berekend voor de fiscale periode, als een uitgave wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="675af-115">An offset account is a profit and loss account, where the depreciation that is calculated for the fiscal period is charged as an expenditure.</span></span> 

<span data-ttu-id="675af-116">Buitengewone afschrijving werkt onafhankelijk van de basisafschrijving.</span><span class="sxs-lookup"><span data-stu-id="675af-116">Extraordinary depreciation works independently of basic depreciation.</span></span> <span data-ttu-id="675af-117">Met buitengewone afschrijving als afzonderlijk transactietype kunt u de buitengewone afschrijving apart van de gewone basisafschrijving boeken en rapporteren.</span><span class="sxs-lookup"><span data-stu-id="675af-117">By having extraordinary depreciation as a separate transaction type, you can post and report the extraordinary depreciation separately from the basic depreciation.</span></span>

## <a name="special-depreciation-allowance"></a><span data-ttu-id="675af-118">Speciale afschrijvingsaftrek</span><span class="sxs-lookup"><span data-stu-id="675af-118">Special depreciation allowance</span></span>
<span data-ttu-id="675af-119">U kunt speciale afschrijvingsaftrekposten gebruiken om extra afschrijvingsbedragen af te schrijven gedurende het eerste jaar dat een activum in gebruik wordt genomen en wordt afgeschreven.</span><span class="sxs-lookup"><span data-stu-id="675af-119">You can use special depreciation allowances to take extra depreciation amounts during the first year that an asset is put in service and depreciated.</span></span> <span data-ttu-id="675af-120">Speciale afschrijvingsaftrekposten moeten vóór andere afschrijvingsberekeningen worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="675af-120">Special depreciation allowances must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="675af-121">Omdat de speciale afschrijvingsaftrekposten pas later in de gebruiksduur van het activum bekend worden, kunt u voor dit type afschrijving beter een boek gebruiken dat niet naar het grootboek boekt.</span><span class="sxs-lookup"><span data-stu-id="675af-121">Because special depreciation allowances are often unknown until later in the service life of the fixed asset, it's best to use this type of depreciation with a book that doesn't post to the general ledger.</span></span> <span data-ttu-id="675af-122">U kunt de periodieke functie Transacties verwijderen die niet zijn geboekt naar grootboek gebruiken om de transactiehistorie te verwijderen voor deze boeken.</span><span class="sxs-lookup"><span data-stu-id="675af-122">You can use the Delete transactions not posted to general ledger periodic function to delete the transaction history for these books.</span></span> <span data-ttu-id="675af-123">U kunt de afschrijvingshistorie voor het vaste-activaboek vervolgens verwijderen, de speciale afschrijvingsaftrekposten boeken wanneer ze bekend zijn en dan de resterende afschrijvingstransacties voor het jaar boeken.</span><span class="sxs-lookup"><span data-stu-id="675af-123">You can then delete the depreciation history for the fixed asset book, post the special depreciation allowance when it's known, and then post the remaining depreciation transactions for the year.</span></span> 

<span data-ttu-id="675af-124">U kunt net zoveel speciale afschrijvingsaftrekrecords maken als u wilt.</span><span class="sxs-lookup"><span data-stu-id="675af-124">You can create an unlimited number of special depreciation allowance records.</span></span> <span data-ttu-id="675af-125">Als u deze records toewijst aan een activagroepsboek, worden deze records op het activumboek toegepast.</span><span class="sxs-lookup"><span data-stu-id="675af-125">After you assign those records to an asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="675af-126">Een speciale afschrijvingsaftrek wordt als een percentage of een vast bedrag ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="675af-126">A special depreciation allowance is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="675af-127">Wanneer u afschrijvingsvoorstellen boekt, worden transacties voor speciale afschrijvingsaftrekposten naar het boek geboekt als transacties die los staan van de afschrijvingstransacties.</span><span class="sxs-lookup"><span data-stu-id="675af-127">When you post depreciation proposals, special depreciation allowance transactions are posted to the book as transactions that are separate from the depreciation transactions.</span></span>

## <a name="depreciation-calendars"></a><span data-ttu-id="675af-128">Afschrijvingskalenders</span><span class="sxs-lookup"><span data-stu-id="675af-128">Depreciation calendars</span></span>
<span data-ttu-id="675af-129">Elk boek heeft een kalender die wordt gebruikt wanneer u vaste activa afschrijft.</span><span class="sxs-lookup"><span data-stu-id="675af-129">Each book has a calendar that is used when you depreciate fixed assets.</span></span> <span data-ttu-id="675af-130">Het boek gebruikt standaard de fiscale kalender van het grootboek, als u geen kalender voor het boek opgeeft.</span><span class="sxs-lookup"><span data-stu-id="675af-130">By default, if you don't indicate a calendar on the book, the book uses the ledger fiscal calendar.</span></span> <span data-ttu-id="675af-131">U moet een fiscale kalender voor een boek selecteren, wanneer het afschrijvingsprofiel dat aan het boek is gekoppeld een afschrijvingsboekjaar gebruikt.</span><span class="sxs-lookup"><span data-stu-id="675af-131">You must select a fiscal calendar for a book when the depreciation profile that is associated with the book uses a fiscal depreciation year.</span></span> 

<span data-ttu-id="675af-132">U kunt gedeelde kalenders maken op de pagina **Fiscale kalenders** in Grootboek.</span><span class="sxs-lookup"><span data-stu-id="675af-132">You can create shared calendars by using the **Fiscal calendars** page in General ledger.</span></span>

<span data-ttu-id="675af-133">Zie voor meer informatie [Afschrijvingsmethoden en conventies](depreciation-methods-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="675af-133">For more information, see [Depreciation methods and conventions](depreciation-methods-conventions.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]