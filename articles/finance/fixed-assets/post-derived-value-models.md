---
title: Boeken met afgeleide boeken
description: In dit artikel wordt beschreven hoe u afgeleide boeken gebruikt.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2b58b2da949211f7eef804af98c866bf5074d47f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187125"
---
# <a name="post-with-derived-books"></a><span data-ttu-id="4d394-103">Boeken met afgeleide boeken</span><span class="sxs-lookup"><span data-stu-id="4d394-103">Post with derived books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d394-104">In dit artikel wordt beschreven hoe u afgeleide boeken gebruikt.</span><span class="sxs-lookup"><span data-stu-id="4d394-104">This article describes how to use derived books.</span></span>

<span data-ttu-id="4d394-105">Wanneer u transacties boekt voor een boek dat afgeleide afschrijvingsboeken bevat, worden transacties met afgeleide boeken automatisch in journalen, inkooporders of vrije-tekstfacturen geboekt.</span><span class="sxs-lookup"><span data-stu-id="4d394-105">When you post transactions for a book that contains derived books, the derived book transactions are posted automatically in journals, purchase orders, or free text invoices.</span></span> <span data-ttu-id="4d394-106">Als u echter de transacties voor het primaire boek in het journaal Vaste activa gereedmaakt, kunt u de bedragen van de afgeleide transacties bekijken en wijzigen voordat u ze boekt.</span><span class="sxs-lookup"><span data-stu-id="4d394-106">However, if you prepare the primary book transactions in the Fixed assets journal, you can view and modify the amounts of the derived transactions before you post them.</span></span>
-   <span data-ttu-id="4d394-107">Bepaalde bedragen, zoals btw en de klant- en leveranciersrekeningen, worden slechts één keer bijgewerkt door boekingen van het primaire boek.</span><span class="sxs-lookup"><span data-stu-id="4d394-107">Certain accounts, such as sales tax and customer or vendor accounts, are updated only once by postings of the primary book.</span></span> <span data-ttu-id="4d394-108">De transacties met afgeleide boeken worden naar de rekeningen geboekt die voor het afgeleide boek in de pagina Boekingsprofielen voor vaste activa zijn opgegeven.</span><span class="sxs-lookup"><span data-stu-id="4d394-108">The derived book transactions are posted to the accounts that have been defined for the derived book in the Fixed asset posting profiles page.</span></span>
-   <span data-ttu-id="4d394-109">Verwerving wordt vaak gebruikt als het transactietype voor de afgeleide boeken.</span><span class="sxs-lookup"><span data-stu-id="4d394-109">Acquisition is often used as the transaction type for the derived books.</span></span> <span data-ttu-id="4d394-110">U gebruikt dit transactietype wanneer het boek en het afgeleide boek vanaf de tijd van de verwerving van de vaste activa op de vaste activa moeten worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="4d394-110">You use this when the book and the derived book should be applied to the fixed asset from the time of the acquisition of the fixed asset.</span></span>
-   <span data-ttu-id="4d394-111">Andere waarden voor het transactietype kunnen ook worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="4d394-111">Other values for the transaction type can also apply.</span></span> <span data-ttu-id="4d394-112">Als bijvoorbeeld het primaire boek en de afgeleide boeken dezelfde intervallen voor verkoop of afboeking hebben, kunnen alle typen vaste-activatransacties worden gebruikt bij het instellen van een afgeleid boek.</span><span class="sxs-lookup"><span data-stu-id="4d394-112">For example, if the primary book and the derived books have the same intervals regarding sale or disposal, all fixed asset transaction types are available for the setup of a derived book.</span></span>

> [!WARNING]
> <span data-ttu-id="4d394-113">De afschrijving die in het afgeleide boek is geboekt, wordt hetzelfde bedrag als het bedrag dat voor het primaire boek is geboekt.</span><span class="sxs-lookup"><span data-stu-id="4d394-113">Depreciation posted in the derived book will be the same amount as was posted for the primary book.</span></span> <span data-ttu-id="4d394-114">Als de afschrijvingsmethoden bij de boeken verschillen, moet u geen afschrijvingstransacties met behulp van het afgeleide proces genereren.</span><span class="sxs-lookup"><span data-stu-id="4d394-114">If the depreciation methods are different between the books, you should not generate depreciation transactions using the derived process.</span></span> |

## <a name="example"></a><span data-ttu-id="4d394-115">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="4d394-115">Example</span></span> 
<span data-ttu-id="4d394-116">Hieronder wordt beschreven hoe u verwervingsmethoden instelt met de functionaliteit van het afgeleide boek.</span><span class="sxs-lookup"><span data-stu-id="4d394-116">The following information describes how to set up acquisition transactions with the derived book functionality.</span></span>

1.  <span data-ttu-id="4d394-117">Maak de boeken op de pagina Boeken.</span><span class="sxs-lookup"><span data-stu-id="4d394-117">Create the books on the Books page.</span></span>
    -   <span data-ttu-id="4d394-118">Het boek voor boekhouding: VM 1, huidige boekingslaag</span><span class="sxs-lookup"><span data-stu-id="4d394-118">The book for accounting: VM 1, Current posting layer</span></span>
    -   <span data-ttu-id="4d394-119">Het boek voor belasting: VM 2, boekingslaag belasting</span><span class="sxs-lookup"><span data-stu-id="4d394-119">The book for tax purposes: VM 2, Tax posting layer</span></span>

2.  <span data-ttu-id="4d394-120">Klik voor VM 1 op het tabblad Afgeleide boeken. Selecteer VM 2 in het veld Boek en Verwerving in het veld Transactietype.</span><span class="sxs-lookup"><span data-stu-id="4d394-120">On VM 1, click the Derived books tab. Select VM 2 in the Book field, and Acquisition in the Transaction type field.</span></span>

<span data-ttu-id="4d394-121">De boeken kunnen aan een specifieke vaste activa worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="4d394-121">The books then can be attached to specific fixed assets.</span></span> 

<span data-ttu-id="4d394-122">Wanneer een verwerving wordt geboekt voor een vast activum met boek VM 1, wordt de verwerking niet alleen op VM 1, maar ook op het afgeleide afgeleide boek VM 2 geboekt.</span><span class="sxs-lookup"><span data-stu-id="4d394-122">When an acquisition is posted for a fixed asset with book VM 1, the acquisition is posted not only on VM 1, but also on the derived book VM 2.</span></span> <span data-ttu-id="4d394-123">De status van beide vaste-activaboeken wordt gewijzigd in Open.</span><span class="sxs-lookup"><span data-stu-id="4d394-123">The status of both fixed asset books is updated to Open.</span></span>

> [!NOTE]                                                                                                         
> <span data-ttu-id="4d394-124">Als u geen afgeleide boeken gebruikt, moet u de verwerving van de vaste activa voor zowel boek VM 1 als voor boek VM 2 afschrijven.</span><span class="sxs-lookup"><span data-stu-id="4d394-124">If you do not use derived books, you must post the acquisition of the fixed asset both for book VM 1 and book VM 2.</span></span>

<span data-ttu-id="4d394-125">Zie voor meer informatie [Afgeleide boeken](derived-books.md).</span><span class="sxs-lookup"><span data-stu-id="4d394-125">For more information, see [Derived books](derived-books.md)</span></span>



