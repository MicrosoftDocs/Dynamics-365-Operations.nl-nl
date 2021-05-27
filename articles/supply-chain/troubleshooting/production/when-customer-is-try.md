---
title: Het batchnummer wordt gewist wanneer een nieuwe partij-id is geselecteerd
description: Wanneer u een orderverzamellijstjournaalregel bekijkt, wordt de waarde in het veld Batchnummer gewist als u een nieuwe waarde selecteert in het veld Partij-id.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: datra
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 71977a04adb066a8b51c9bf7b8c5a4e752ca902e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026390"
---
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a><span data-ttu-id="8a489-103">Het batchnummer wordt gewist wanneer een nieuwe partij-id is geselecteerd</span><span class="sxs-lookup"><span data-stu-id="8a489-103">Batch number is cleared when a new lot ID is selected</span></span>

<span data-ttu-id="8a489-104">KB-nummer: 4613107</span><span class="sxs-lookup"><span data-stu-id="8a489-104">KB number: 4613107</span></span>

## <a name="symptoms"></a><span data-ttu-id="8a489-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="8a489-105">Symptoms</span></span>

<span data-ttu-id="8a489-106">Wanneer u een orderverzamellijstjournaalregel bekijkt, wordt de waarde in het veld **Batchnummer** gewist als u een nieuwe waarde selecteert in het veld **Partij-id**.</span><span class="sxs-lookup"><span data-stu-id="8a489-106">When you're reviewing a picking list journal line, the value in the **Batch number** field is cleared if you select a new value in the **Lot ID** field.</span></span>

## <a name="resolution"></a><span data-ttu-id="8a489-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="8a489-107">Resolution</span></span>

<span data-ttu-id="8a489-108">Dit gedrag van het systeem is inherent aan het ontwerp.</span><span class="sxs-lookup"><span data-stu-id="8a489-108">The system is behaving as designed.</span></span> <span data-ttu-id="8a489-109">Als u de partij-ID wijzigt, wijzigt u de artikelcontext.</span><span class="sxs-lookup"><span data-stu-id="8a489-109">If you change the lot ID, you change the item context.</span></span> <span data-ttu-id="8a489-110">Daarom wordt het batchnummer opnieuw ingesteld.</span><span class="sxs-lookup"><span data-stu-id="8a489-110">Therefore, the batch number is reset.</span></span>

<span data-ttu-id="8a489-111">Als u het batchnummer aan een partij-id wilt koppelen, moet u eerst de partij-id instellen.</span><span class="sxs-lookup"><span data-stu-id="8a489-111">To associate the batch number with a lot ID, you must set the lot ID first.</span></span>
