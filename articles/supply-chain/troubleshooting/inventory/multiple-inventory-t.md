---
title: Meerdere voorraadtransacties voor batchnummers als de optie Bij fysiek bijwerken is uitgeschakeld
description: Er worden meerdere voorraadtransacties gemaakt nadat u een inkooporderregel hebt aangepast voor artikelen waarbij de optie Bij fysiek bijwerken van de batchnummergroep is ingesteld op Nee.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventNumGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1fa54cdfdbc5608fb6c7114dced0f96bab47253e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026419"
---
# <a name="multiple-inventory-transactions-for-batch-numbers-when-on-physical-update-is-disabled"></a><span data-ttu-id="4d8f7-103">Meerdere voorraadtransacties voor batchnummers als de optie Bij fysiek bijwerken is uitgeschakeld</span><span class="sxs-lookup"><span data-stu-id="4d8f7-103">Multiple inventory transactions for batch numbers when On physical update is disabled</span></span>

<span data-ttu-id="4d8f7-104">KB-nummer: 4613390</span><span class="sxs-lookup"><span data-stu-id="4d8f7-104">KB number: 4613390</span></span>

## <a name="symptoms"></a><span data-ttu-id="4d8f7-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="4d8f7-105">Symptoms</span></span>

<span data-ttu-id="4d8f7-106">Er worden meerdere voorraadtransacties gemaakt nadat u een inkooporderregel hebt aangepast voor artikelen waarbij de optie **Bij fysiek bijwerken** van de batchnummergroep is ingesteld op *Nee*.</span><span class="sxs-lookup"><span data-stu-id="4d8f7-106">Multiple inventory transactions are created after you adjust a purchase order line for items where the **On physical update** option of the batch number group is set to *No*.</span></span>

<span data-ttu-id="4d8f7-107">Wanneer u een artikel maakt waarbij de optie **Bij fysiek bijwerken** van de batchnummergroep is ingesteld op *Nee*, wordt automatisch een nieuw batchnummer gemaakt als u de hoeveelheid op de inkoopregel wijzigt en de inkooporderpagina opslaat.</span><span class="sxs-lookup"><span data-stu-id="4d8f7-107">When you create an item where the **On physical update** option of the batch number group is set to *No*, the system automatically creates a new batch number if you modify a purchase line quantity and save the purchase order page.</span></span>

## <a name="resolution"></a><span data-ttu-id="4d8f7-108">Oplossing</span><span class="sxs-lookup"><span data-stu-id="4d8f7-108">Resolution</span></span>

<span data-ttu-id="4d8f7-109">De instelling **Bij fysiek bijwerken** voor batchnummergroepen werkt als volgt:</span><span class="sxs-lookup"><span data-stu-id="4d8f7-109">The **On physical update** setting for batch number groups works in the following way:</span></span>

- <span data-ttu-id="4d8f7-110">Wanneer de optie is ingesteld op *Ja*, worden er alleen nieuwe batchnummers gemaakt na fysiek bijwerken (bijvoorbeeld wanneer artikelen worden verzonden of ontvangen).</span><span class="sxs-lookup"><span data-stu-id="4d8f7-110">When the option is set to *Yes*, new batch numbers are created only after a physical update (for example, when items are shipped or received).</span></span>
- <span data-ttu-id="4d8f7-111">Wanneer de optie is ingesteld op *Nee*, wordt er telkens een nieuw batchnummer gemaakt wanneer een toepasselijke update wordt toegepast (bijvoorbeeld wanneer een nieuwe hoeveelheid aan een inkooporder wordt toegevoegd).</span><span class="sxs-lookup"><span data-stu-id="4d8f7-111">When the option is set to *No*, a new batch number is created every time that an applicable update occurs (for example, when a new quantity is added to a purchase order).</span></span>
