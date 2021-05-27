---
title: Het veld Datum laatst getest wordt niet bijgewerkt wanneer er meerdere kwaliteitsorders worden gemaakt
description: Het veld Datum laatst getest wordt niet bijgewerkt wanneer er meerdere kwaliteitsorders worden gemaakt.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f796bdaa88d32b1c58dd8a4bca19f0ce4f3943d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026416"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a><span data-ttu-id="f672f-103">Het veld Datum laatst getest wordt niet bijgewerkt wanneer er meerdere kwaliteitsorders worden gemaakt</span><span class="sxs-lookup"><span data-stu-id="f672f-103">The Last tested date field isn't updated when multiple quality orders are created</span></span>

<span data-ttu-id="f672f-104">KB-nummer: 4612803</span><span class="sxs-lookup"><span data-stu-id="f672f-104">KB number: 4612803</span></span>

## <a name="symptoms"></a><span data-ttu-id="f672f-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="f672f-105">Symptoms</span></span>

<span data-ttu-id="f672f-106">Het veld **Datum laatst getest** wordt niet bijgewerkt wanneer er meerdere kwaliteitsorders worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f672f-106">The **Last tested date** field isn't updated when multiple quality orders are created.</span></span>

## <a name="resolution"></a><span data-ttu-id="f672f-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="f672f-107">Resolution</span></span>

<span data-ttu-id="f672f-108">Dit gedrag van het systeem is inherent aan het ontwerp.</span><span class="sxs-lookup"><span data-stu-id="f672f-108">The system is behaving as designed.</span></span> <span data-ttu-id="f672f-109">De datum van de laatste test is niet gerelateerd aan kwaliteitsorders.</span><span class="sxs-lookup"><span data-stu-id="f672f-109">The last tested date isn't related to quality orders.</span></span> <span data-ttu-id="f672f-110">Dit is de datum waarop de eindproducten voor het eerst zijn ingekocht of gefabriceerd.</span><span class="sxs-lookup"><span data-stu-id="f672f-110">It stores the date when the finished goods were first purchased or manufactured.</span></span> <span data-ttu-id="f672f-111">Met deze datum wordt de adviesdatum voor de houdbaarheid berekend.</span><span class="sxs-lookup"><span data-stu-id="f672f-111">This date is used to calculate the shelf life advice date.</span></span>
