---
title: Er wordt slechts één label afgedrukt voor meerdere werkkopteksten op één ontvangstbewijs
description: Er wordt slechts één label afgedrukt voor meerdere werkkopteksten op één ontvangstbewijs.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8e11dc918eb3c9085018d15b43819522cc8bebe3
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026404"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a><span data-ttu-id="02d72-103">Er wordt slechts één label afgedrukt voor meerdere werkkopteksten op één ontvangstbewijs</span><span class="sxs-lookup"><span data-stu-id="02d72-103">Only one label is printed for multiple work headers on a single receipt</span></span>

<span data-ttu-id="02d72-104">KB-nummer: 4614667</span><span class="sxs-lookup"><span data-stu-id="02d72-104">KB number: 4614667</span></span>

## <a name="symptoms"></a><span data-ttu-id="02d72-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="02d72-105">Symptoms</span></span>

<span data-ttu-id="02d72-106">Er worden meerdere werkkopteksten gemaakt voor dezelfde doelnummerplaat als onderdeel van één ontvangstgebeurtenis voor de magazijn-app.</span><span class="sxs-lookup"><span data-stu-id="02d72-106">Multiple work headers are created for the same target license plate as part of a single warehouse app receiving event.</span></span> <span data-ttu-id="02d72-107">Wanneer het product binnen is, wordt echter slechts één nummerplaatlabel afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="02d72-107">However, only one license plate label is printed when the product is received.</span></span>

## <a name="resolution"></a><span data-ttu-id="02d72-108">Oplossing</span><span class="sxs-lookup"><span data-stu-id="02d72-108">Resolution</span></span>

<span data-ttu-id="02d72-109">Dit gedrag van het systeem is inherent aan het ontwerp.</span><span class="sxs-lookup"><span data-stu-id="02d72-109">The system is behaving as designed.</span></span>

<span data-ttu-id="02d72-110">In het huidige ontwerp wordt altijd één nummerplaatlabel gegenereerd, ongeacht het aantal bestaande combinaties van werkkoptekst en werkregel.</span><span class="sxs-lookup"><span data-stu-id="02d72-110">In the current design, a single license plate label is always generated, regardless of the number of work header and work line combinations that exist.</span></span> <span data-ttu-id="02d72-111">Het gegenereerde label bevat de informatie voor slechts één combinatie.</span><span class="sxs-lookup"><span data-stu-id="02d72-111">The generated label includes the information for only one combination.</span></span>

<span data-ttu-id="02d72-112">Als u dit probleem wilt oplossen, moet u ervoor zorgen dat het maken van werkkopteksten altijd is toegewezen aan slechts één doelnummerplaat.</span><span class="sxs-lookup"><span data-stu-id="02d72-112">To work around this issue, make sure that work header creation is always mapped to just one target license plate.</span></span>
