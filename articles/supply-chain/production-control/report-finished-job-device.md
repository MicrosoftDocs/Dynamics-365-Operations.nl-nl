---
title: Melden als voltooid aan een nummerplaatgestuurde locatie vanaf het taakkaartapparaat
description: Dit onderwerp beschrijft het proces voor het voltooien van eindproducten voor een productieorder tot aan de voorraad wanneer een nummerplaat de locatie beheert.
author: johanhoffmann
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: 35ad27a6b8a52bfd086fbe4fc57b1681ff88fd5b
ms.sourcegitcommit: 58db26b7edf02e7c33aaaf1c934e3263aa74b01f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/11/2019
ms.locfileid: "1995137"
---
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="c5b10-103">Melden als voltooid aan een nummerplaatgestuurde locatie vanaf het taakkaartapparaat</span><span class="sxs-lookup"><span data-stu-id="c5b10-103">Report as finished to a license plate controlled location from the Job card device</span></span> 

<span data-ttu-id="c5b10-104">Het proces met de naam Gereedmelding voltooit eindproducten op een productieorder in de voorraad.</span><span class="sxs-lookup"><span data-stu-id="c5b10-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="c5b10-105">Als het voltooide product is ingeschakeld voor de geavanceerde magazijnprocessen, wordt het product gereedgemeld aan een locatie die de productie-uitvoerlocatie wordt genoemd.</span><span class="sxs-lookup"><span data-stu-id="c5b10-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="c5b10-106">Zie [productie-uitvoerlocatie](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location)voor informatie over het instellen van de productie-uitvoerlocatie.</span><span class="sxs-lookup"><span data-stu-id="c5b10-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="c5b10-107">U moet een bestaand nummerplaatnummer selecteren om deze taak te voltooien.</span><span class="sxs-lookup"><span data-stu-id="c5b10-107">You must select an existing license plate number to complete this task.</span></span> <span data-ttu-id="c5b10-108">Als de productie-uitvoerlocatie is ingesteld voor tracering met een nummerplaat, moet er een nummerplaatnummer worden opgenomen wanneer de productie-uitvoerlocatie wordt gereedgemeld.</span><span class="sxs-lookup"><span data-stu-id="c5b10-108">If the production output location is set up to be tracked by license plate, then a license plate number must be included when reporting the production output location as finished.</span></span> <span data-ttu-id="c5b10-109">Het veld **Nummerplaat** wordt weer gegeven op de prompt **Voortgang rapporteren** van de pagina **Taakkaartapparaat**.</span><span class="sxs-lookup"><span data-stu-id="c5b10-109">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="c5b10-110">Het veld wordt alleen weer gegeven op de prompt **Voortgang rapporteren** bij het rapporteren van de laatste bewerking van de productieorder.</span><span class="sxs-lookup"><span data-stu-id="c5b10-110">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order.</span></span> <span data-ttu-id="c5b10-111">Het veld wordt alleen weergegeven als het artikel voor de productieorder is ingeschakeld voor magazijnbeheerprocessen.</span><span class="sxs-lookup"><span data-stu-id="c5b10-111">The field is only shown if the item for the production order is enabled for the warehouse management processes.</span></span> 
