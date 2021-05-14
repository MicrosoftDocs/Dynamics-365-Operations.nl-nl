---
title: Gewicht moet positief zijn
description: Gewicht moet positief zijn
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dcbcde3143cb509b68b277cb7c709263e2659b5b
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924298"
---
# <a name="weight-must-be-positive"></a><span data-ttu-id="8c784-103">Gewicht moet positief zijn</span><span class="sxs-lookup"><span data-stu-id="8c784-103">Weight must be positive</span></span>

<span data-ttu-id="8c784-104">Foutcode: WeightMustBePositive</span><span class="sxs-lookup"><span data-stu-id="8c784-104">Error code: WeightMustBePositive</span></span>

## <a name="symptoms"></a><span data-ttu-id="8c784-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="8c784-105">Symptoms</span></span>

<span data-ttu-id="8c784-106">Het systeem toont het volgende foutbericht:</span><span class="sxs-lookup"><span data-stu-id="8c784-106">The system shows the following error message:</span></span>

> <span data-ttu-id="8c784-107">Gewicht moet positief zijn.</span><span class="sxs-lookup"><span data-stu-id="8c784-107">Weight must be positive.</span></span>

## <a name="cause"></a><span data-ttu-id="8c784-108">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="8c784-108">Cause</span></span>

<span data-ttu-id="8c784-109">Het veld **Brutogewicht** is ingesteld op *0* (nul) of heeft een negatieve waarde.</span><span class="sxs-lookup"><span data-stu-id="8c784-109">The **Gross Weight** field is set to *0* (zero) or a negative value.</span></span>

## <a name="resolution"></a><span data-ttu-id="8c784-110">Oplossing</span><span class="sxs-lookup"><span data-stu-id="8c784-110">Resolution</span></span>

<span data-ttu-id="8c784-111">Als u een gewicht wilt opgeven, volgt u een van deze stappen.</span><span class="sxs-lookup"><span data-stu-id="8c784-111">To specify a weight, follow one of these steps.</span></span>

- <span data-ttu-id="8c784-112">Stel een waarde in het veld **Brutogewicht** in.</span><span class="sxs-lookup"><span data-stu-id="8c784-112">In the **Gross weight** field, set a value.</span></span> <span data-ttu-id="8c784-113">Selecteer vervolgens een eenheid in de vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="8c784-113">Then select a unit in the drop-down list.</span></span>
- <span data-ttu-id="8c784-114">Selecteer **Systeemgewicht** om de waarde van het **Brutogewicht** te berekenen.</span><span class="sxs-lookup"><span data-stu-id="8c784-114">Select **Get system weight** to calculate the **Gross weight** value.</span></span>
