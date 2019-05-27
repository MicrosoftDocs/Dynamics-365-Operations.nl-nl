---
title: Kostenwaarden voor voorhanden voorraad corrigeren
description: Gebruik de pagina Correctie van voorhanden voorraad om de kostprijs van de voorhanden voorraadhoeveelheden aan te passen nadat het voorraadafsluitingsproces is uitgevoerd.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2417a278e58f4309873ab4d33b0d1f1686081951
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556110"
---
# <a name="adjust-on-hand-inventory-cost-values"></a><span data-ttu-id="079e8-103">Kostenwaarden voor voorhanden voorraad corrigeren</span><span class="sxs-lookup"><span data-stu-id="079e8-103">Adjust on-hand inventory cost values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="079e8-104">Gebruik de pagina Correctie van voorhanden voorraad om de kostprijs van de voorhanden voorraadhoeveelheden aan te passen nadat het voorraadafsluitingsproces is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="079e8-104">Use the Adjustment of on-hand inventory page to adjust the cost value of the on-hand inventory quantities after an inventory close process is run.</span></span>

<span data-ttu-id="079e8-105">U kunt de pagina **Correctie van voorhanden voorraad** gebruiken om de kostprijs van de voorhanden voorraadhoeveelheden aan te passen nadat het voorraadafsluitingsproces is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="079e8-105">You can use the **Adjustment of on-hand inventory** page to adjust the cost value of on-hand inventory quantities after an inventory close process is run.</span></span> <span data-ttu-id="079e8-106">**Opmerking:** als u de pagina **Correctie van voorhanden voorraad** wilt openen, selecteert u op de pagina **Afsluiten en corrigeren** de record van een voltooid voorraadafsluitingsproces en klikt u vervolgens op **Correctie** &gt; **Voorhanden**.</span><span class="sxs-lookup"><span data-stu-id="079e8-106">**Note:** To open the **Adjustment of on-hand inventory** page, on the **Closing and adjustment** page, select the record of a completed inventory close process, and then click **Adjustment** &gt; **On-hand**.</span></span> <span data-ttu-id="079e8-107">**Voorbeeld:** u hebt de volgende transacties in februari:</span><span class="sxs-lookup"><span data-stu-id="079e8-107">**Example:** You have the following transactions in February:</span></span>

-   <span data-ttu-id="079e8-108">1 februari: financiële ontvangst in voorraad voor een hoeveelheid van 2 tegen USD 10,00 aan kosten</span><span class="sxs-lookup"><span data-stu-id="079e8-108">February 1: An inventory financial receipt for a quantity of 2 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="079e8-109">5 februari: financiële ontvangst in voorraad voor een hoeveelheid van 1 tegen USD 13,00 aan kosten</span><span class="sxs-lookup"><span data-stu-id="079e8-109">February 5: An inventory financial receipt for a quantity of 1 at a cost of USD 13.00</span></span>
-   <span data-ttu-id="079e8-110">19 februari: financiële voorraaduitgifte voor een hoeveelheid van 1 tegen een gemiddelde kostprijs van 11,00 EUR</span><span class="sxs-lookup"><span data-stu-id="079e8-110">February 19: An inventory financial issue for a quantity of 1 at a running average cost of USD 11.00</span></span>

<span data-ttu-id="079e8-111">Dit artikel is ingesteld met het FIFO-voorraadmodel (first in, first out) en de voorraadafsluiting is uitgevoerd vanaf 28 februari.</span><span class="sxs-lookup"><span data-stu-id="079e8-111">This item was set up with the first in, first out (FIFO) inventory model, and inventory close was performed as of February 28.</span></span> <span data-ttu-id="079e8-112">De financiële uitgiftetransactie van USD 11,00 wordt vereffend met de financiële ontvangst van 1 februari en er wordt een correctie van USD 1,00 doorgevoerd.</span><span class="sxs-lookup"><span data-stu-id="079e8-112">The financial issue transaction of USD 11.00 will be settled against the financial receipt that is dated February 1, and an adjustment of USD 1.00 will be made.</span></span> <span data-ttu-id="079e8-113">De volgende voorraadontvangsten bevatten vervolgens openstaande voorraadhoeveelheden:</span><span class="sxs-lookup"><span data-stu-id="079e8-113">The following inventory receipts will then contain open inventory quantities:</span></span>

-   <span data-ttu-id="079e8-114">1 februari: een hoeveelheid van 1 tegen 10,00 EUR aan kosten</span><span class="sxs-lookup"><span data-stu-id="079e8-114">February 1: A quantity of 1 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="079e8-115">5 februari: een hoeveelheid van 1 tegen 13,00 EUR aan kosten</span><span class="sxs-lookup"><span data-stu-id="079e8-115">February 5: A quantity of 1 at a cost of USD 13.00</span></span>

<span data-ttu-id="079e8-116">Als u de kosten van deze twee artikelen wilt instellen op USD 15,00, gebruikt u de optie voor het corrigeren van de voorhanden voorraad om de openstaande voorhanden hoeveelheden te corrigeren vanaf de laatste voorraadafsluitingsperiode.</span><span class="sxs-lookup"><span data-stu-id="079e8-116">To set the cost of these two items to USD 15.00, use the on-hand adjustment option to adjust the open on-hand quantities as of the last inventory close period.</span></span> <span data-ttu-id="079e8-117">**Opmerking:** de boekingsdatum van de correctietransactie voor de voorhanden voorraad is de datum van de laatste voorraadafsluiting.</span><span class="sxs-lookup"><span data-stu-id="079e8-117">**Note:** The posting date of the on-hand adjustment transaction will be the date of the last inventory close.</span></span> <span data-ttu-id="079e8-118">Deze datum kan niet worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="079e8-118">This date can't be modified.</span></span>
