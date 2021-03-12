---
title: Gecombineerde nummerplaat ontvangen
description: In dit onderwerp wordt beschreven hoe u met ontvangst van gecombineerde nummerplaten werk kunt registreren en maken voor meerdere artikelen met een mobiel apparaat.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c4dcafa5d997bce21d37d02f87fbf604568c24e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965628"
---
# <a name="mixed-license-plate-receiving"></a><span data-ttu-id="8ad9c-103">Gecombineerde nummerplaat ontvangen</span><span class="sxs-lookup"><span data-stu-id="8ad9c-103">Mixed license plate receiving</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ad9c-104">Met gecombineerde nummerplaatontvangst kunt u een nummerplaat maken die meerdere artikelen omvat, voordat u wegzetwerk registreert en maakt.</span><span class="sxs-lookup"><span data-stu-id="8ad9c-104">Mixed license plate receiving allows you to build a license plate consisting of multiple items before you register and create put-away work.</span></span> 

<span data-ttu-id="8ad9c-105">Een nummerplaat die meerdere artikelen omvat, hoeft niet te worden opgesplitst in de ontvangende dock om elk artikel te kunnen registreren.</span><span class="sxs-lookup"><span data-stu-id="8ad9c-105">A license plate that consists of multiple items does not have to be split at the receiving dock for you to register each item.</span></span> 

<span data-ttu-id="8ad9c-106">Als u een artikelgerelateerde stroom gebruikt om de brondocumentregels te identificeren, kunt u streepjescodes op het besturingselement van het artikel scannen.</span><span class="sxs-lookup"><span data-stu-id="8ad9c-106">When using an item-related flow to identify the source document lines, you can scan bar codes on the item control.</span></span> <span data-ttu-id="8ad9c-107">Als in de streepjescode een hoeveelheid en een maateenheid zijn geconfigureerd, worden het artikel en de hoeveelheid automatisch toegevoegd aan de gecombineerde nummerplaat en keert u terug naar het scherm om een ander artikel te scannen.</span><span class="sxs-lookup"><span data-stu-id="8ad9c-107">If the bar code has a quantity and a unit of measure (UOM) configured on it, the item and quantity will automatically be added to the mixed license plate, and you will be returned to the screen to scan another item.</span></span> <span data-ttu-id="8ad9c-108">Hiermee kunt u snel alle items scannen, zonder elke stap te hoeven bevestigen.</span><span class="sxs-lookup"><span data-stu-id="8ad9c-108">This allows you to quickly scan all the items without having to make a confirmation at each step.</span></span> 

<span data-ttu-id="8ad9c-109">In de stroom voor gecombineerde nummerplaatontvangst kunt u de lijst weergeven met artikelen die al zijn gescand naar de nummerplaat en van hieruit kunt u de hoeveelheid van een artikel aanpassen of corrigeren.</span><span class="sxs-lookup"><span data-stu-id="8ad9c-109">In the flow for mixed license plate receiving, you can display the list of items that are already scanned to the license plate and from here you can modify or correct the quantity of an item.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="8ad9c-110">Waar van toepassing</span><span class="sxs-lookup"><span data-stu-id="8ad9c-110">Where it applies</span></span>

<span data-ttu-id="8ad9c-111">Ontvangst van gecombineerde nummerplaten is een ontvangststroom voor mobiele apparaten, waarmee u werk voor meerdere regels/artikelen tegelijkertijd kunt registreren en maken.</span><span class="sxs-lookup"><span data-stu-id="8ad9c-111">Mixed license plate receiving is a mobile device receiving flow to register and create work for multiple lines/items at the same time.</span></span> <span data-ttu-id="8ad9c-112">Dit is handig als u binnenkomende nummerplaten met meerdere artikelen ontvangt.</span><span class="sxs-lookup"><span data-stu-id="8ad9c-112">This is useful if you receive inbound license plates with multiple items.</span></span> 

## <a name="how-to-set-up-mixed-license-plate-receiving"></a><span data-ttu-id="8ad9c-113">Gecombineerde nummerplaatontvangst instellen</span><span class="sxs-lookup"><span data-stu-id="8ad9c-113">How to set up mixed license plate receiving</span></span>
<span data-ttu-id="8ad9c-114">Gecombineerde nummerplaatontvangst wordt ingesteld als een menu-item voor mobiel apparaten.</span><span class="sxs-lookup"><span data-stu-id="8ad9c-114">Mixed license plate receiving is set up as a mobile device menu item.</span></span>

<span data-ttu-id="8ad9c-115">U moet een nieuwe menuoptie maken met de modus werk, die geen bestaand werk gebruikt en een van de volgende methoden gebruikt:</span><span class="sxs-lookup"><span data-stu-id="8ad9c-115">You need to create a new menu item with mode work that does not use existing work and use one of the following methods:</span></span>

- <span data-ttu-id="8ad9c-116">Gecombineerde nummerplaat ontvangen</span><span class="sxs-lookup"><span data-stu-id="8ad9c-116">Mixed license plate receiving</span></span>
- <span data-ttu-id="8ad9c-117">Nummerplaat ontvangen en wegzetten</span><span class="sxs-lookup"><span data-stu-id="8ad9c-117">Mixed license plate receiving and put away</span></span>

<span data-ttu-id="8ad9c-118">De opties om de brondocumentregels te identificeren zijn inkooporderartikel, inkooporderregel, retourorder, transferorderartikel en transferorderregel.</span><span class="sxs-lookup"><span data-stu-id="8ad9c-118">The options to identify the source document lines are purchase order item, purchase order line, return order, transfer order item, and transfer order line.</span></span> <span data-ttu-id="8ad9c-119">Deze opties kunnen de ontvangstvolgorde op een enkele nummerplaat wijzigen.</span><span class="sxs-lookup"><span data-stu-id="8ad9c-119">These options can change the receiving order on a single license plate.</span></span> <span data-ttu-id="8ad9c-120">De laatste optie is op ladingsartikel.</span><span class="sxs-lookup"><span data-stu-id="8ad9c-120">The last option is by load item.</span></span> <span data-ttu-id="8ad9c-121">U kunt meerdere artikelen toevoegen aan een nummerplaat, maar u kunt niet schakelen tussen meerdere ladingen.</span><span class="sxs-lookup"><span data-stu-id="8ad9c-121">You can add multiple items to a license plate, but you cannot switch between multiple loads.</span></span>
