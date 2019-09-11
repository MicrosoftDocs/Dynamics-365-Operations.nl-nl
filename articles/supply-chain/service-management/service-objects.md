---
title: Overzicht van Serviceobjecten
description: De serviceobjecten zijn de activum en de producten van een klant waarvoor u een service kunt uitvoeren.
author: ShylaThompson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a25c4d71d617a0b7cacd31f708421fd9dd960ea
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865868"
---
# <a name="service-objects-overview"></a><span data-ttu-id="e6a58-103">Overzicht van Serviceobjecten</span><span class="sxs-lookup"><span data-stu-id="e6a58-103">Service objects overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e6a58-104">De serviceobjecten zijn de activum en de producten van een klant waarvoor u een service kunt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="e6a58-104">Service objects are a customer’s assets and products for which you can perform a service.</span></span> <span data-ttu-id="e6a58-105">Afhankelijk van het type service dat u levert, kunnen objecten tastbaar of ontastbaar zijn:</span><span class="sxs-lookup"><span data-stu-id="e6a58-105">Depending on the type of service you provide, objects can be tangible or intangible:</span></span>

-  <span data-ttu-id="e6a58-106">Tastbare objecten zijn bijvoorbeeld machines of gebouwen waarop u een fysieke servicetaak kunt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="e6a58-106">Tangible objects are things, such as a machine or a building, on which you can perform a physical service task.</span></span>

    <span data-ttu-id="e6a58-107">Een tastbaar serviceobject kan ook een voorraadartikel zijn dat u maakt in het formulier Vrijgegeven productdetails.</span><span class="sxs-lookup"><span data-stu-id="e6a58-107">A tangible service object can also be an inventory item that you create in the Released product details form.</span></span> <span data-ttu-id="e6a58-108">Afhankelijk van de voorraaddimensiegroep die u aan het artikel koppelt, kunt u het serviceobject maken tot het detailniveau van het serienummer van het artikel bevat.</span><span class="sxs-lookup"><span data-stu-id="e6a58-108">Depending on the inventory dimension group that you attach to the item, you can create a service object to a level of detail that includes the item serial number.</span></span> <span data-ttu-id="e6a58-109">Dit is handig wanneer u het artikel dat wordt aangeduid door het serviceobject precies moet bijhouden.</span><span class="sxs-lookup"><span data-stu-id="e6a58-109">This is useful when you must keep track of the exact item that the service object represents.</span></span>

    <span data-ttu-id="e6a58-110">Een tastbaar serviceobject kan een artikel zijn dat niet rechtstreeks is gerelateerd aan de directe productie of de keten van toeleveranciers.</span><span class="sxs-lookup"><span data-stu-id="e6a58-110">A tangible service object can also be an item that is not directly related to a company's direct production or supply chain.</span></span> <span data-ttu-id="e6a58-111">Bijvoorbeeld, een toolkit reparaties in die voor een serviceorder is gebruikt kan een serviceobject dat niet in voorraad is.</span><span class="sxs-lookup"><span data-stu-id="e6a58-111">For example, a tool kit that is used for repairs in a service order can be a service object that is not included in inventory.</span></span> <span data-ttu-id="e6a58-112">In dit geval, registreert u het niet als voorraadartikel.</span><span class="sxs-lookup"><span data-stu-id="e6a58-112">In this case, you don’t register it as an inventory item.</span></span>

-  <span data-ttu-id="e6a58-113">Ontastbare objecten zijn niet-fysieke entiteiten, zoals een set rekeningen of een juridisch document, waarop servicetaken kunnen worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="e6a58-113">Intangible objects are nonphysical things, such as a set of accounts or a legal document, on which you can perform a service task.</span></span>

## <a name="example-of-an-intangible-service-object"></a><span data-ttu-id="e6a58-114">Voorbeeld van een serviceobject ontastbaar</span><span class="sxs-lookup"><span data-stu-id="e6a58-114">Example of an intangible service object</span></span>

<span data-ttu-id="e6a58-115">Bedrijf A onderhouden de financiële records voor kleine verschillende bedrijven.</span><span class="sxs-lookup"><span data-stu-id="e6a58-115">Company A maintains the financial records for several small companies.</span></span> <span data-ttu-id="e6a58-116">Een van de klanten van bedrijf A is de plaatselijke voetbalvereniging, waarvoor bedrijf A de wekelijkse boekhouding en de jaarlijkse controle van de rekeningen van de vereniging uitvoert.</span><span class="sxs-lookup"><span data-stu-id="e6a58-116">One of Company A's clients is the local football team, for which Company A does the weekly bookkeeping and annual audit of the club's accounts.</span></span> <span data-ttu-id="e6a58-117">De rekeningen van de vereniging zijn ingesteld in het formulier Serviceobjecten en worden in de serviceovereenkomst aangegeven als het object.</span><span class="sxs-lookup"><span data-stu-id="e6a58-117">The club's accounts are set up in the Service objects form and specified as the object in the service agreement.</span></span> <span data-ttu-id="e6a58-118">Er zijn twee serviceovereenkomstregels voor het object.</span><span class="sxs-lookup"><span data-stu-id="e6a58-118">There are two service agreement lines for the object.</span></span> <span data-ttu-id="e6a58-119">Regel 1 is wekelijkse boekhouding met een wekelijks interval die aan de regel is toegewezen, en regel 2 is de jaarlijkse controle met een jaarlijks interval die eraan is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="e6a58-119">Line 1 is weekly bookkeeping with a weekly interval assigned to the line, and line 2 is the annual audit with a yearly interval assigned to it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6a58-120">Verwante onderwerpen</span><span class="sxs-lookup"><span data-stu-id="e6a58-120">Related topics</span></span>

[<span data-ttu-id="e6a58-121">Serviceobjecten maken</span><span class="sxs-lookup"><span data-stu-id="e6a58-121">Create service objects</span></span>](create-service-objects.md)

