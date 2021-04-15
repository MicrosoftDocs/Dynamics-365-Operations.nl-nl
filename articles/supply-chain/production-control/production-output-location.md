---
title: Productie-uitvoerlocatie
description: In dit onderwerp wordt de hiërarchie beschreven die wordt gebruikt ter identificatie van de uitvoerlocatie van de productie.
author: johanhoffmann
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 48b68c36718fa42b7f80e3ffe1f54b7efbbee8bd
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814627"
---
# <a name="production-output-location"></a><span data-ttu-id="6058c-103">Productie-uitvoerlocatie</span><span class="sxs-lookup"><span data-stu-id="6058c-103">Production output location</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6058c-104">In dit onderwerp wordt de hiërarchie beschreven die wordt gebruikt ter identificatie van de uitvoerlocatie van de productie.</span><span class="sxs-lookup"><span data-stu-id="6058c-104">This topic describes the hierarchy that is used to identify the production output location.</span></span>

<span data-ttu-id="6058c-105">De productie-uitvoerlocatie is de locatie waar een eindproduct eerst wordt opgeslagen nadat het is geproduceerd.</span><span class="sxs-lookup"><span data-stu-id="6058c-105">The production output location is the location where a finished good is first stored after it's produced.</span></span> <span data-ttu-id="6058c-106">Deze locatie bevindt zich meestal in de buurt van het productieproces dat het gerede product produceert.</span><span class="sxs-lookup"><span data-stu-id="6058c-106">Usually, this location is close to the production process that produces the finished good.</span></span> <span data-ttu-id="6058c-107">De productie-uitvoerlocatie wordt gebruikt als tussentijdse opslag voor het materiaal voordat het wordt verplaatst naar het verzendgebied, een opslaglocatie, een productie-invoerlocatie voor een stroomafwaartse productieproces, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="6058c-107">The production output location is used as intermediate storage for the material before it's moved on to the shipment area, a storage location, a production input location for a downstream production process, and so on.</span></span> 

<span data-ttu-id="6058c-108">Een standaardlocatie voor de productie-uitvoer wordt ingesteld wanneer eindproducten worden gemeld op een productieorder of batchorder.</span><span class="sxs-lookup"><span data-stu-id="6058c-108">A default production output location is set when finished goods are reported on a production order or batch order.</span></span> <span data-ttu-id="6058c-109">De volgende hiërarchie wordt gebruikt voor deze uitvoerlocatie:</span><span class="sxs-lookup"><span data-stu-id="6058c-109">The following hierarchy is used to identify this output location:</span></span>

1. <span data-ttu-id="6058c-110">Gebruik de uitvoerlocatie die wordt gedefinieerd in de koptekst van de productieorder of batchorder.</span><span class="sxs-lookup"><span data-stu-id="6058c-110">Use the output location that is defined on the production order or batch order header.</span></span>
2. <span data-ttu-id="6058c-111">Als er geen locatie wordt gevonden, gebruikt u de uitvoerlocatie die wordt gedefinieerd voor de bron die is gebruikt door de laatste bewerking die is gedefinieerd in de productieroute.</span><span class="sxs-lookup"><span data-stu-id="6058c-111">If no location is found there, use the output location that is defined on the resource that is used by the last operation that is defined in the production route.</span></span>
3. <span data-ttu-id="6058c-112">Als er geen locatie wordt gevonden, gebruikt u de uitvoerlocatie die wordt gedefinieerd voor de brongroep die is gebruikt door de bron voor de laatste bewerking die is gedefinieerd in de productieroute.</span><span class="sxs-lookup"><span data-stu-id="6058c-112">If no location is found there, use the output location that is defined on the resource group that is used by the resource for the last operation that is defined in the production route.</span></span>
4. <span data-ttu-id="6058c-113">Als er geen locatie wordt gevonden, gebruikt u de uitvoerlocatie die is gedefinieerd in het magazijn dat is gedefinieerd voor de productieorder.</span><span class="sxs-lookup"><span data-stu-id="6058c-113">If no location is found there, use the output location that is defined on the warehouse that is defined for the production order.</span></span>

<span data-ttu-id="6058c-114">Een standaardlocatie voor de productie-uitvoer wordt alleen ingesteld voor producten die zijn ingesteld met geavanceerde magazijnprocessen.</span><span class="sxs-lookup"><span data-stu-id="6058c-114">A default production output location is set only for products that are set up by using advanced warehouse processes.</span></span> <span data-ttu-id="6058c-115">Wanneer dit type artikel is gereedgemeld, wordt een magazijntaak van het type **Eindproducten wegzetten** of **Coproducten en bijproducten wegzetten** gemaakt.</span><span class="sxs-lookup"><span data-stu-id="6058c-115">When this type of item is reported as finished, warehouse work of the **Finished goods put away** or **Co-product and by-product put away** type is created.</span></span> <span data-ttu-id="6058c-116">Dit type tak gebruikt de productie-uitvoerlocatie als orderverzamellocatie.</span><span class="sxs-lookup"><span data-stu-id="6058c-116">This type of work uses the production output location as the pick location.</span></span> <span data-ttu-id="6058c-117">De opslaglocatie wordt bepaald door de richtlijnen van de locatie.</span><span class="sxs-lookup"><span data-stu-id="6058c-117">The put-away location is determined by the location directives.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]