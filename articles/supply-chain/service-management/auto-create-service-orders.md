---
title: Automatisch serviceorders maken
description: U kunt serviceorders genereren op basis van een serviceovereenkomst voor de periode waarin de serviceovereenkomst van kracht is.
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2d942d4448e0f792945603d3f5960fb82095be30
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="automatically-create-service-orders"></a><span data-ttu-id="9fa67-103">Automatisch serviceorders maken</span><span class="sxs-lookup"><span data-stu-id="9fa67-103">Automatically create service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="9fa67-104">U kunt serviceorders genereren op basis van een serviceovereenkomst voor de periode waarin de serviceovereenkomst van kracht is.</span><span class="sxs-lookup"><span data-stu-id="9fa67-104">You can generate service orders that are based on a service agreement for the valid period of the service agreement.</span></span>

<span data-ttu-id="9fa67-105">De serviceorders die u van een serviceovereenkomst genereert, worden aan de serviceovereenkomst gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="9fa67-105">The service orders that you generate from a service agreement are all attached to the service agreement.</span></span>

<span data-ttu-id="9fa67-106">Serviceorders worden automatisch van de volgende instellingen gegenereerd:</span><span class="sxs-lookup"><span data-stu-id="9fa67-106">Service orders are generated automatically from the following settings:</span></span>

  - <span data-ttu-id="9fa67-107">Het interval dat voor de serviceovereenkomst op de serviceovereenkomstregels is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="9fa67-107">The service agreement interval that is set up in the service agreement lines.</span></span> <span data-ttu-id="9fa67-108">Dat serviceovereenkomstinterval geeft de frequentie aan waarmee serviceorderregels worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="9fa67-108">The service agreement interval indicates the frequency that service-order lines are created.</span></span> <span data-ttu-id="9fa67-109">Zie voor meer informatie [Service-intervallen](service-intervals.md).</span><span class="sxs-lookup"><span data-stu-id="9fa67-109">For more information, see [Service intervals](service-intervals.md).</span></span>

  - <span data-ttu-id="9fa67-110">De periode die u in de velden **Datum vanaf** en **Datum t/m** in het formulier **Serviceorders maken** opgeeft voor het specificeren van de serviceperiode.</span><span class="sxs-lookup"><span data-stu-id="9fa67-110">The period that you specify to define the service period in the **From date** and **To date** fields in the **Create service orders** form.</span></span> <span data-ttu-id="9fa67-111">Zie voor meer informatie [Serviceorders automatisch maken](create-service-orders-automatically.md).</span><span class="sxs-lookup"><span data-stu-id="9fa67-111">For more information, see [Create service orders automatically](create-service-orders-automatically.md).</span></span>

  - <span data-ttu-id="9fa67-112">De optie **Serviceorders combineren** in de koptekst van de serviceovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="9fa67-112">The **Combine service orders** option on the service agreement header.</span></span> <span data-ttu-id="9fa67-113">Met deze optie wordt aangegeven of serviceorderregels die worden gegenereerd vanuit een serviceovereenkomst, worden gecombineerd op werknemer, diensttaak, serviceobject of serviceovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="9fa67-113">This option defines whether service order lines generated from a service agreement, combines service orders according to employee, service task, service object, or service agreement.</span></span> <span data-ttu-id="9fa67-114">Zie voor meer informatie [Serviceorders combineren](combine-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="9fa67-114">For more information, see [Combine service orders](combine-service-orders.md).</span></span>

  - <span data-ttu-id="9fa67-115">De optie **Tijdvenster** op de serviceovereenkomstregel.</span><span class="sxs-lookup"><span data-stu-id="9fa67-115">The **Time window** option on the service agreement line.</span></span> <span data-ttu-id="9fa67-116">Door het tijdvenster wordt bepaald in hoeverre een serviceorderregel ten opzichte van de berekende datum kan worden verplaatst.</span><span class="sxs-lookup"><span data-stu-id="9fa67-116">The time window defines how far a service order line can move with regard to its calculated date.</span></span> <span data-ttu-id="9fa67-117">Zie voor meer informatie [Tijdvensters](time-windows.md).</span><span class="sxs-lookup"><span data-stu-id="9fa67-117">For more information, see [Time windows](time-windows.md).</span></span>


> [!NOTE]
> <P><span data-ttu-id="9fa67-118">Als de dag die voor een serviceorder is opgegeven, niet is geopend in de kalender die u in het formulier <STRONG>Parameters voor servicebeheer</STRONG> hebt geselecteerd, wordt er melding van een kalenderconflict gemaakt.</span><span class="sxs-lookup"><span data-stu-id="9fa67-118">If the day that is specified for a service order is not open in the calendar that you have selected in the <STRONG>Service management parameters</STRONG> form, a message will indicate that there is a calendar conflict.</span></span> <span data-ttu-id="9fa67-119">U kunt dit bericht gewoon negeren. De serviceorder wordt gemaakt, ondanks dat de dag in het kalender is gesloten.</span><span class="sxs-lookup"><span data-stu-id="9fa67-119">You can safely ignore the message; the service order will be created, even though the day is closed on the calendar.</span></span></P>

## <a name="example-1"></a><span data-ttu-id="9fa67-120">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="9fa67-120">Example 1</span></span>

<span data-ttu-id="9fa67-121">De serviceovereenkomst loopt van 1 januari 2012 tot en met 31 december 2012.</span><span class="sxs-lookup"><span data-stu-id="9fa67-121">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="9fa67-122">Als de serviceperiode die u hebt opgegeven in het formulier **Serviceorders maken** van 1 november 2012 tot en met 1 februari 2013 loopt, worden er toch alleen serviceorders gemaakt van 1 november 2012 tot en met 31 december 2012.</span><span class="sxs-lookup"><span data-stu-id="9fa67-122">If the service period that you specify in the **Create service orders** form is from November 1, 2012 until February 1, 2013, service orders are created from November 1, 2012 until December 31, 2012.</span></span>

## <a name="example-2"></a><span data-ttu-id="9fa67-123">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="9fa67-123">Example 2</span></span>

<span data-ttu-id="9fa67-124">De serviceovereenkomst loopt van 1 januari 2012 tot en met 31 december 2012.</span><span class="sxs-lookup"><span data-stu-id="9fa67-124">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="9fa67-125">Aan die serviceovereenkomst zijn twee serviceovereenkomstregels gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="9fa67-125">Two service agreement lines are attached to the service agreement.</span></span> <span data-ttu-id="9fa67-126">De eerste serviceovereenkomstregel heeft een begindatum van 2 januari 2012 en een einddatum van 1 maart 2012.</span><span class="sxs-lookup"><span data-stu-id="9fa67-126">The first service agreement line has a starting date on January 2, 2012 and an ending date on March 1, 2012.</span></span> <span data-ttu-id="9fa67-127">De tweede serviceovereenkomstregel heeft een begindatum van 1 april 2012 en een einddatum van 31 december 2012.</span><span class="sxs-lookup"><span data-stu-id="9fa67-127">The second service agreement line has a starting date on April 1, 2012 and an ending date on December 31, 2012.</span></span> <span data-ttu-id="9fa67-128">U geeft in het formulier **Serviceorders maken** een periode op die loopt van 1 oktober 2012 tot en met 31 december 2012.</span><span class="sxs-lookup"><span data-stu-id="9fa67-128">You specify a period in the **Create service orders** form that is from October 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="9fa67-129">Er worden alleen serviceorders gegenereerd voor de tweede overeenkomstregel, omdat de begin- en einddatum van de eerste overeenkomstregel vóór de periode liggen die u voor de serviceperiode hebt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="9fa67-129">Therefore, service orders are generated only for the second agreement line, because the starting date and ending date of the first agreement line are before the period that you specified for the service order.</span></span>

  



