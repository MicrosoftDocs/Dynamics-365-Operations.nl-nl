---
title: Door het omkeren van de gereedmelding wordt een onverwachte openstaande transactie gemaakt
description: Door het omkeren van gereedmelding met markering wordt een openstaande transactie gemaakt waarin de omgekeerde hoeveelheid dezelfde voorraaddimenssies heeft als de omgekeerde transactie.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ea9044a9008e766c7fc92f98e27cfb91076f5b44
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026417"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a><span data-ttu-id="adf41-103">Door het omkeren van de gereedmelding wordt een onverwachte openstaande transactie gemaakt</span><span class="sxs-lookup"><span data-stu-id="adf41-103">Reversal of reporting as finished creates an unexpected open transaction</span></span>

<span data-ttu-id="adf41-104">KB-nummer: 4612469</span><span class="sxs-lookup"><span data-stu-id="adf41-104">KB number: 4612469</span></span>

## <a name="symptoms"></a><span data-ttu-id="adf41-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="adf41-105">Symptoms</span></span>

<span data-ttu-id="adf41-106">Door het omkeren van gereedmelding met markering wordt een openstaande transactie gemaakt waarin de omgekeerde hoeveelheid dezelfde voorraaddimenssies heeft als de omgekeerde transactie.</span><span class="sxs-lookup"><span data-stu-id="adf41-106">If you reverse reporting as finished that has marking, the system creates an open transaction where the reversed quantity has the same inventory dimensions as the transaction that was reversed.</span></span>

## <a name="resolution"></a><span data-ttu-id="adf41-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="adf41-107">Resolution</span></span>

<span data-ttu-id="adf41-108">Wanneer u een gereedmeldingsbewerking omkeert, wordt de voorraaddimensie vanuit het productiejournaal geïnitialiseerd.</span><span class="sxs-lookup"><span data-stu-id="adf41-108">When you reverse a report-as-finished operation, the inventory dimension is initialized from the production journal.</span></span> <span data-ttu-id="adf41-109">Daarom krijgt deze het batchnummer.</span><span class="sxs-lookup"><span data-stu-id="adf41-109">Therefore, it gets the batch number.</span></span> <span data-ttu-id="adf41-110">Vanwege de markering nemen de verkoopordertransacties het batchnummer over.</span><span class="sxs-lookup"><span data-stu-id="adf41-110">Because of marking, the sales order transactions will inherit the batch number.</span></span>

<span data-ttu-id="adf41-111">De dimensie kan opnieuw worden ingesteld wanneer de gereedgemelding wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="adf41-111">The dimension can be reset when the reporting as finished is posted.</span></span>
