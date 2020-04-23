---
title: Overzicht van Servicelevelovereenkomsten opstellen en tot stand brengen
description: Met serviceovereenkomsten kunt u de middelen opgeven die bij een standaardonderhoudsbezoek worden gebruikt en opgeven hoe die middelen aan de klant worden gefactureerd.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41081525fb9ff7bfa3adb87ba038d899f58e436a
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216155"
---
# <a name="develop-and-establish-service-agreements-overview"></a><span data-ttu-id="e9394-103">Overzicht van Servicelevelovereenkomsten opstellen en tot stand brengen</span><span class="sxs-lookup"><span data-stu-id="e9394-103">Develop and establish service agreements overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e9394-104">Met serviceovereenkomsten kunt u de middelen opgeven die bij een standaardonderhoudsbezoek worden gebruikt en opgeven hoe die middelen aan de klant worden gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="e9394-104">Service agreements let you define the resources that are used in a typical service visit and how those resources are invoiced to the customer.</span></span>

<span data-ttu-id="e9394-105">Elke serviceovereenkomst is gekoppeld aan een project en via dit project worden transacties geboekt en gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="e9394-105">Every service agreement is attached to a project through which transactions are posted and invoiced.</span></span> <span data-ttu-id="e9394-106">U kunt serviceordertransacties echter ook rechtstreeks via het project factureren, zonder dat u eerst de serviceorder aan een serviceovereenkomst hoeft te koppelen.</span><span class="sxs-lookup"><span data-stu-id="e9394-106">However, you can also invoice service order transactions directly through the project without first having to connect the service order to a service agreement.</span></span> <span data-ttu-id="e9394-107">U kunt dit doen als de serviceorder een serviceorder voor een eenmalig bezoek is en het verwerken van de servicetransacties belangrijker is dan de noodzaak om gedetailleerd de gegevens van de serviceovereenkomst voor de klant gedurende een bepaalde periode bij te houden.</span><span class="sxs-lookup"><span data-stu-id="e9394-107">You might decide to do this if the service order is for a one-time-only service visit and the need for processing the service transactions quickly outweighs the need for maintaining detailed service-agreement information about the customer over a period of time.</span></span>

## <a name="service-agreement"></a><span data-ttu-id="e9394-108">Serviceovereenkomst</span><span class="sxs-lookup"><span data-stu-id="e9394-108">Service agreement</span></span>

<span data-ttu-id="e9394-109">In elke serviceovereenkomst moet u een project, een serviceovereenkomst-ID en een serviceovereenkomstgroep opgeven.</span><span class="sxs-lookup"><span data-stu-id="e9394-109">In each service agreement, you must specify a project, a service-agreement ID, and a service-agreement group.</span></span> <span data-ttu-id="e9394-110">De serviceovereenkomstgroep kan worden gebruikt voor het sorteren en organiseren van serviceovereenkomsten.</span><span class="sxs-lookup"><span data-stu-id="e9394-110">The service-agreement group can be used to sort and organize service agreements.</span></span>

<span data-ttu-id="e9394-111">De koptekst van een serviceovereenkomst bevat de instellingen die voor alle bijgevoegde serviceovereenkomstregels gelden:</span><span class="sxs-lookup"><span data-stu-id="e9394-111">A service agreement header contains settings that apply to all attached agreement lines:</span></span>

-  <span data-ttu-id="e9394-112">Of de serviceovereenkomst is uitgesteld.</span><span class="sxs-lookup"><span data-stu-id="e9394-112">Whether the service agreement is suspended.</span></span> <span data-ttu-id="e9394-113">Als de serviceovereenkomst is uitgesteld, kunt u geen serviceorders van de serviceovereenkomst genereren.</span><span class="sxs-lookup"><span data-stu-id="e9394-113">If the service agreement is suspended, you cannot generate service orders from the service agreement.</span></span>
-  <span data-ttu-id="e9394-114">De duur van de serviceovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="e9394-114">The duration of the service agreement.</span></span>
-  <span data-ttu-id="e9394-115">De manier waarop serviceorderregels in serviceorders moeten worden gecombineerd.</span><span class="sxs-lookup"><span data-stu-id="e9394-115">How service-order lines are to be combined into service orders.</span></span>
-  <span data-ttu-id="e9394-116">Of de serviceovereenkomst een sjabloon is.</span><span class="sxs-lookup"><span data-stu-id="e9394-116">Whether the service agreement is a template.</span></span>

<span data-ttu-id="e9394-117">In de kop van een serviceovereenkomst stelt u ook alle serviceobjecten en -taken in die met de serviceovereenkomst kunnen worden gebruikt. Daarvoor voert u de specifieke servicetaken of -objecten in die aan de diverse regels van de overeenkomst moeten worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="e9394-117">In the service-agreement header, you also set up all the service objects and service tasks that can be used with the service agreement by entering the specific service tasks or service objects that are to be attached to the various lines of the agreement.</span></span>

<span data-ttu-id="e9394-118">Vanuit de koptekst van de serviceovereenkomst kunt u ook serviceovereenkomstregels of servicesjabloonregels naar de huidige serviceovereenkomst kopiëren.</span><span class="sxs-lookup"><span data-stu-id="e9394-118">From the service-agreement header, you can also copy service-agreement lines or service-template lines into the current service agreement.</span></span>

<span data-ttu-id="e9394-119">U kunt serviceovereenkomsten uitstellen en afzonderlijke serviceovereenkomstregels stoppen.</span><span class="sxs-lookup"><span data-stu-id="e9394-119">You can suspend service agreements and stop individual service agreement lines.</span></span>

<span data-ttu-id="e9394-120">Als u het selectievakje **Uitgesteld** voor een serviceovereenkomstregel inschakelt, bent u niet in staat om:</span><span class="sxs-lookup"><span data-stu-id="e9394-120">If you select the **Suspended** check box on a service agreement, you cannot:</span></span>

-    <span data-ttu-id="e9394-121">automatisch of handmatig serviceorders te maken op basis van de serviceovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="e9394-121">Create service orders automatically or manually from the service agreement.</span></span>

<span data-ttu-id="e9394-122">Als u het selectievakje **Gestopt** voor een serviceovereenkomstregel inschakelt, bent u niet in staat om:</span><span class="sxs-lookup"><span data-stu-id="e9394-122">If you select the **Stopped** check box on a service agreement line, you cannot:</span></span>

-    <span data-ttu-id="e9394-123">automatisch of handmatig serviceorders te maken op basis van de serviceovereenkomstregel.</span><span class="sxs-lookup"><span data-stu-id="e9394-123">Create service orders automatically or manually from the service agreement line.</span></span>
-    <span data-ttu-id="e9394-124">de serviceovereenkomstregel te kopiëren naar een andere serviceovereenkomst of serviceorder.</span><span class="sxs-lookup"><span data-stu-id="e9394-124">Copy the service agreement line into another service agreement or service order.</span></span>


> [!NOTE]
> <span data-ttu-id="e9394-125">Indien een serviceovereenkomst wordt uitgesteld, worden alle gekoppelde regels gestopt ongeacht de afzonderlijke status van deze regels.</span><span class="sxs-lookup"><span data-stu-id="e9394-125">If a service agreement is suspended, all the attached lines are stopped, regardless of their individual status.</span></span>

## <a name="service-agreement-lines"></a><span data-ttu-id="e9394-126">Serviceovereenkomstregels</span><span class="sxs-lookup"><span data-stu-id="e9394-126">Service-agreement lines</span></span>

<span data-ttu-id="e9394-127">Elke serviceovereenkomstregel beschrijft in detail de inhoud van het voorgestelde servicewerk.</span><span class="sxs-lookup"><span data-stu-id="e9394-127">Each service-agreement line describes in detail the content of the proposed service work.</span></span> <span data-ttu-id="e9394-128">Deze regels bevatten de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="e9394-128">The lines contain the following settings:</span></span>

-  <span data-ttu-id="e9394-129">Het transactietype en de omschrijving van het transactietype.</span><span class="sxs-lookup"><span data-stu-id="e9394-129">The transaction type and the description of the transaction type.</span></span>
-  <span data-ttu-id="e9394-130">De werknemer die het servicewerk uitvoert.</span><span class="sxs-lookup"><span data-stu-id="e9394-130">The employee who performs the service work.</span></span>
-  <span data-ttu-id="e9394-131">De objecten waarop de service conform de serviceovereenkomst moet worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="e9394-131">The objects on which service must be performed for the service agreement.</span></span>
-  <span data-ttu-id="e9394-132">De frequentie waarmee het werk wordt uitgevoerd, en bijhorende artikel-, onkosten- en bijzondere-kostentransacties worden geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="e9394-132">The frequency with which work is performed and associated item, expense, and fee transactions are registered.</span></span>
-  <span data-ttu-id="e9394-133">Het tijdvenster waarbinnen serviceorderregels in een serviceorder kunnen worden gegroepeerd.</span><span class="sxs-lookup"><span data-stu-id="e9394-133">The time window within which service-order lines can be grouped into a service order.</span></span>
-  <span data-ttu-id="e9394-134">De servicetaken waarmee sets overeenkomstregels worden gegroepeerd in werktaken en waarmee voor servicemonteurs en klanten wordt samengevat welke servicetaak er dient te worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="e9394-134">The service tasks that are used to group sets of agreement lines together into work tasks and to summarize for service technicians and customers what service task is to be provided.</span></span>
-  <span data-ttu-id="e9394-135">Of een regel is geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="e9394-135">Whether a line is stopped.</span></span> <span data-ttu-id="e9394-136">Als een regel is geblokkeerd, kunt u voor die regel geen serviceorders maken.</span><span class="sxs-lookup"><span data-stu-id="e9394-136">If a line is stopped, you cannot create service orders for that individual line.</span></span>
-  <span data-ttu-id="e9394-137">Projectinstellingen zoals de categorie en de regeleigenschap.</span><span class="sxs-lookup"><span data-stu-id="e9394-137">Project settings, such as the category and the line property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9394-138">Verwante onderwerpen</span><span class="sxs-lookup"><span data-stu-id="e9394-138">Related topics</span></span>

[<span data-ttu-id="e9394-139">Serviceovereenkomsten maken</span><span class="sxs-lookup"><span data-stu-id="e9394-139">Create service agreements</span></span>](create-service-agreements.md)
