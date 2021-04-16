---
title: Een werkklasse maken
description: Deze procedure laat zien hoe u een werkklasse instelt.
author: ShylaThompson
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be2c037ccc8f5cafc94d9fdee9647605889d0599
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830973"
---
# <a name="create-a-work-class"></a><span data-ttu-id="8abe4-103">Een werkklasse maken</span><span class="sxs-lookup"><span data-stu-id="8abe4-103">Create a work class</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8abe4-104">Deze procedure laat zien hoe u een werkklasse instelt.</span><span class="sxs-lookup"><span data-stu-id="8abe4-104">This procedure shows you how to set up a work class.</span></span> <span data-ttu-id="8abe4-105">Werkklassen worden gebruikt om het type werkorderregels te bepalen en/of beperken dat een magazijnwerknemer op een mobiel apparaat kan verwerken.</span><span class="sxs-lookup"><span data-stu-id="8abe4-105">Work classes are used to direct and/or limit the type of work order lines that a warehouse worker can process on a mobile device.</span></span> <span data-ttu-id="8abe4-106">De regels die een werknemer kan verwerken, worden bepaald op basis van de werkklassen in menuopdrachten van mobiele apparaten waartoe de magazijnwerknemer toegang heeft, en de werkklasse die op de werkregels is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="8abe4-106">The lines that a worker can process are determined from the work classes on the mobile device menu items that the warehouse worker has access to and the work class that's specified on the work lines.</span></span> <span data-ttu-id="8abe4-107">Werkklassen kunnen ook worden gebruikt om de neerzetlocatie van een werkorderregel te valideren.</span><span class="sxs-lookup"><span data-stu-id="8abe4-107">Work classes can also be used to validate the put location for a work order line.</span></span> <span data-ttu-id="8abe4-108">U kunt deze procedure uitvoeren in het demogegevensbedrijf USMF of met uw eigen gegevens.</span><span class="sxs-lookup"><span data-stu-id="8abe4-108">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="8abe4-109">Deze procedure is bedoeld voor de magazijnbeheerder.</span><span class="sxs-lookup"><span data-stu-id="8abe4-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="8abe4-110">Ga naar Magazijnbeheer > Instellingen > Werk > Werkklassen.</span><span class="sxs-lookup"><span data-stu-id="8abe4-110">Go to Warehouse management > Setup > Work > Work classes.</span></span>
2. <span data-ttu-id="8abe4-111">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="8abe4-111">Click New.</span></span>
3. <span data-ttu-id="8abe4-112">Typ een waarde in het veld Werkklasse-id.</span><span class="sxs-lookup"><span data-stu-id="8abe4-112">In the Work class ID field, type a value.</span></span>
4. <span data-ttu-id="8abe4-113">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="8abe4-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8abe4-114">Selecteer een optie in het veld Werkordertype.</span><span class="sxs-lookup"><span data-stu-id="8abe4-114">In the Work order type field, select an option.</span></span>
6. <span data-ttu-id="8abe4-115">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="8abe4-115">Click New.</span></span>
7. <span data-ttu-id="8abe4-116">Typ een waarde in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="8abe4-116">In the Location type field, type a value.</span></span>
    * <span data-ttu-id="8abe4-117">Als u een locatietype selecteert, stelt dit een beperking in op waar artikelen kunnen worden geplaatst nadat ze zijn verzameld.</span><span class="sxs-lookup"><span data-stu-id="8abe4-117">If you select a location type, this sets a restriction on where items can be put after they've been picked.</span></span> <span data-ttu-id="8abe4-118">Deze instelling wordt gebruikt wanneer een locatierichtlijn probeert de locatie op te lossen of als een magazijnwerknemer handmatig de locatie voor menuopdrachten van mobiele apparaten verschaft.</span><span class="sxs-lookup"><span data-stu-id="8abe4-118">This setting is used when a location directive tries to resolve the location, or if a warehouse worker manually provides the location for the mobile device menu item.</span></span>  
8. <span data-ttu-id="8abe4-119">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="8abe4-119">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]