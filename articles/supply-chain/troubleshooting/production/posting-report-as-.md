---
title: Fout wanneer het Gereedmeldingsjournaal wordt geboekt
description: Wanneer u het Gereedmeldingsjournaal boekt, ontvangt u een foutbericht waarin wordt staat dat de bestelde hoeveelheid niet kan worden verminderd.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage, ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 55db7d0033dd66c1b973abf96671a20ab05d61d8
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026394"
---
# <a name="error-when-the-report-as-finished-journal-is-posted"></a><span data-ttu-id="1f788-103">Fout wanneer het Gereedmeldingsjournaal wordt geboekt</span><span class="sxs-lookup"><span data-stu-id="1f788-103">Error when the Report as finished journal is posted</span></span>

<span data-ttu-id="1f788-104">KB-nummer: 4612891</span><span class="sxs-lookup"><span data-stu-id="1f788-104">KB number: 4612891</span></span>

## <a name="symptoms"></a><span data-ttu-id="1f788-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="1f788-105">Symptoms</span></span>

<span data-ttu-id="1f788-106">Wanneer u het **Gereedmeldingsjournaal** boekt, treedt er een fout op en wordt het volgende foutbericht weergegeven:</span><span class="sxs-lookup"><span data-stu-id="1f788-106">When you post the **Report as finished** journal, an error occurs, and you receive the following error message:</span></span>

> <span data-ttu-id="1f788-107">Bestelde hoeveelheid kan niet worden verminderd omdat er onvoldoende openstaande voorraadtransacties met de status Besteld zijn.</span><span class="sxs-lookup"><span data-stu-id="1f788-107">Quantity ordered cannot be reduced because there are not enough open inventory transactions with the ordered status.</span></span> <span data-ttu-id="1f788-108">De artikelen zijn Ingekocht, Ontvangen of Geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="1f788-108">The items are Purchased, Received or Registered.</span></span>

<span data-ttu-id="1f788-109">Deze fout treedt alleen op als het veld **Slechte hoeveelheid** is ingesteld op de eerste regel van het **Gereedmeldingsjournaal** en het veld **Goede hoeveelheid** op de laatste regel is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="1f788-109">This error occurs only when the **Error quantity** field is set on the first line of the **Report as finished** journal, and the **Good quantity** field is set on the last line.</span></span> <span data-ttu-id="1f788-110">Als het veld **Slechte hoeveelheid** is ingesteld op de laatste regel, treedt er geen fout op.</span><span class="sxs-lookup"><span data-stu-id="1f788-110">If the **Error quantity** field is set on the last line, no error occurs.</span></span>

## <a name="resolution"></a><span data-ttu-id="1f788-111">Oplossing</span><span class="sxs-lookup"><span data-stu-id="1f788-111">Resolution</span></span>

<span data-ttu-id="1f788-112">Om deze fout te voorkomen opent u de pagina **Parameters van productiebeheer** en stelt u vervolgens op het tabblad **Algemeen** de optie **Resterende hoeveelheid verhogen met fouthoeveelheid** in op *Ja*.</span><span class="sxs-lookup"><span data-stu-id="1f788-112">To prevent this error, open the **Production control parameters** page, and then, on the **General** tab, set the **Increase remain qty with error qty** option to *Yes*.</span></span>
