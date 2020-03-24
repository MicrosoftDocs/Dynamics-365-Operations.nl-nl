---
title: Melden als voltooid aan een nummerplaatgestuurde locatie vanaf het taakkaartapparaat
description: Dit onderwerp beschrijft het proces voor het voltooien van eindproducten voor een productieorder tot aan de voorraad wanneer een nummerplaat de locatie beheert.
author: johanhoffmann
manager: AnnBe
ms.date: 01/06/2020
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
ms.openlocfilehash: 5f61c1abfb115f02e6ff314f6a3e42bb1d3b543f
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092563"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="3f446-103">Melden als voltooid aan een nummerplaatgestuurde locatie vanaf het taakkaartapparaat</span><span class="sxs-lookup"><span data-stu-id="3f446-103">Report as finished to a license plate controlled location from the Job card device</span></span> 

<span data-ttu-id="3f446-104">Het proces met de naam Gereedmelding voltooit eindproducten op een productieorder in de voorraad.</span><span class="sxs-lookup"><span data-stu-id="3f446-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="3f446-105">Als het voltooide product is ingeschakeld voor de geavanceerde magazijnprocessen, wordt het product gereedgemeld aan een locatie die de productie-uitvoerlocatie wordt genoemd.</span><span class="sxs-lookup"><span data-stu-id="3f446-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="3f446-106">Zie [productie-uitvoerlocatie](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location)voor informatie over het instellen van de productie-uitvoerlocatie.</span><span class="sxs-lookup"><span data-stu-id="3f446-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="3f446-107">Als de productie-uitvoerlocatie wordt gecontroleerd op nummerplaat, moet een nummerplaat worden opgegeven bij het gereedmelden.</span><span class="sxs-lookup"><span data-stu-id="3f446-107">If the production output location is license plate controlled, then a license plate must be provided when reporting as finished.</span></span> <span data-ttu-id="3f446-108">Het veld **Nummerplaat** wordt weer gegeven op de prompt **Voortgang rapporteren** van de pagina **Taakkaartapparaat**.</span><span class="sxs-lookup"><span data-stu-id="3f446-108">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="3f446-109">Het veld is alleen zichtbaar bij **Voortgang melden** bij het rapporteren over de laatste bewerking van de productieorder en als het artikel voor de productieorder is ingeschakeld voor de magazijnbeheerprocessen.</span><span class="sxs-lookup"><span data-stu-id="3f446-109">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order and the item for the production order is enabled for the warehouse management processes.</span></span> 

<span data-ttu-id="3f446-110">Er zijn twee opties voor het opgeven van de nummerplaat</span><span class="sxs-lookup"><span data-stu-id="3f446-110">There are two options for providing the license plate</span></span>
- <span data-ttu-id="3f446-111">De gebruiker selecteert een bestaande nummerplaat in het veld Nummerplaat.</span><span class="sxs-lookup"><span data-stu-id="3f446-111">The user is selecting an existing license plate in the license plate field.</span></span>
- <span data-ttu-id="3f446-112">De nummerplaat wordt automatisch gegenereerd op basis van een nummerreeks en wordt standaard opgenomen in het veld Nummerplaat.</span><span class="sxs-lookup"><span data-stu-id="3f446-112">The license plate is automatically generated from a number sequence and defaulted to the license plate field.</span></span>

<span data-ttu-id="3f446-113">U configureert de optie om de nummerplaat automatisch te laten genereren door de optie **Nummerplaat genereren** op de pagina **Taakkaart configureren voor apparaten** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="3f446-113">The option to have the license plate generated automatically is configured by selecting the option **Generate license plate** on the **Configure job card for devices** page.</span></span>
