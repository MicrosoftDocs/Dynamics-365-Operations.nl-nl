---
title: Artikelbehoeften bij serviceorders
description: Als u specifieke artikelen voor een serviceorder moet reserveren, kunt u er voorraadartikelbehoeften voor maken.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a0ce40c26e3d3028064b73a80a247180d6a9009
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226660"
---
# <a name="service-order-item-requirements"></a><span data-ttu-id="b03e3-103">Artikelbehoeften bij serviceorders</span><span class="sxs-lookup"><span data-stu-id="b03e3-103">Service order item requirements</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b03e3-104">U kunt een serviceorder maken om services, die u aan uw klanten levert, bij te houden en te beheren.</span><span class="sxs-lookup"><span data-stu-id="b03e3-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="b03e3-105">Als u specifieke artikelen voor een serviceorder moet reserveren, kunt u er voorraadartikelbehoeften voor maken.</span><span class="sxs-lookup"><span data-stu-id="b03e3-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="b03e3-106">Een artikelbehoefte kan direct worden verbruikt vanuit de voorraad, of er kan een productieorder of inkooporder voor het artikel mee worden geïnitialiseerd.</span><span class="sxs-lookup"><span data-stu-id="b03e3-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="b03e3-107">Door een artikelbehoefte te maken in plaats van een artikeltransactie kunt u de levering plannen vlak voordat het artikel werkelijk wordt gebruikt, een inkooporder maken, het artikel opnemen in het handelsovereenkomstframework en de artikelbehoefte opnemen in de productieplanning.</span><span class="sxs-lookup"><span data-stu-id="b03e3-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="b03e3-108">Artikelbehoeften voor serviceorders worden verwerkt via een project.</span><span class="sxs-lookup"><span data-stu-id="b03e3-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="b03e3-109">Als u een artikelbehoefte wilt maken voor een serviceorder, moet de serviceorder worden gekoppeld aan een project.</span><span class="sxs-lookup"><span data-stu-id="b03e3-109">To create an item requirement on a service order, the service order must be attached to a project.</span></span>

<span data-ttu-id="b03e3-110">Zodra een artikelbehoefte is gemaakt voor een serviceorder, kunt u deze weergeven via **Project** in de afzonderlijke serviceorder of via het formulier **Verkooporder**.</span><span class="sxs-lookup"><span data-stu-id="b03e3-110">As soon as an item requirement is created for a service order, it can be viewed from **Project** in the individual service order or through the **Sales order** form.</span></span>

## <a name="view-an-item-requirement-from-a-service-order"></a><span data-ttu-id="b03e3-111">Een artikelbehoefte voor een serviceorder weergeven</span><span class="sxs-lookup"><span data-stu-id="b03e3-111">View an item requirement from a service order</span></span>

1.  <span data-ttu-id="b03e3-112">Klik op **Servicebeheer** \> **Algemeen** \> **Serviceorders** \> **Serviceorders**.</span><span class="sxs-lookup"><span data-stu-id="b03e3-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="b03e3-113">Klik op **Verzending** en klik vervolgens op **Artikelbehoefte** om het formulier **Artikelbehoeften** te openen.</span><span class="sxs-lookup"><span data-stu-id="b03e3-113">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span>

3.  <span data-ttu-id="b03e3-114">Klik op het tabblad **Project** en selecteer vervolgens het veld **Serviceorder** in om de serviceorders van de artikelbehoefte te bekijken.</span><span class="sxs-lookup"><span data-stu-id="b03e3-114">Click the **Project** tab, and check the **Service order** field to see the service orders of the item requirement.</span></span>

## <a name="delete-service-orders-with-item-requirements"></a><span data-ttu-id="b03e3-115">Serviceorders met artikelbehoeften verwijderen</span><span class="sxs-lookup"><span data-stu-id="b03e3-115">Delete service orders with item requirements</span></span>

<span data-ttu-id="b03e3-116">Als u een artikelbehoefte hebt gemaakt voor een serviceorder, kunt u de serviceorder niet verwijderen.</span><span class="sxs-lookup"><span data-stu-id="b03e3-116">If an item requirement is created on a service order, you cannot delete the service order.</span></span> <span data-ttu-id="b03e3-117">U moet de artikelbehoefte verwijderen, voordat u de serviceorder kunt verwijderen.</span><span class="sxs-lookup"><span data-stu-id="b03e3-117">You must delete the item requirement before you can delete the service order.</span></span>

1.  <span data-ttu-id="b03e3-118">Klik op **Servicebeheer** \> **Algemeen** \> **Serviceorders** \> **Serviceorders**.</span><span class="sxs-lookup"><span data-stu-id="b03e3-118">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="b03e3-119">Klik op **Verzending** en klik vervolgens op **Artikelbehoefte** om het formulier **Artikelbehoeften** te openen.</span><span class="sxs-lookup"><span data-stu-id="b03e3-119">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span> <span data-ttu-id="b03e3-120">Dit formulier bevat een lijst met alle artikelbehoeften die voor de serviceorder zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="b03e3-120">This form lists the item requirements that are created on the service order.</span></span>

3.  <span data-ttu-id="b03e3-121">Selecteer de artikelbehoefte die u wilt verwijderen en klik vervolgens op **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="b03e3-121">Select the item requirement to delete, and then click **Delete**.</span></span>

<span data-ttu-id="b03e3-122">– of –</span><span class="sxs-lookup"><span data-stu-id="b03e3-122">–or–</span></span>

1.  <span data-ttu-id="b03e3-123">Klik op **Projectbeheer en boekhouding** \> **Algemeen** \> **Projecten** \> **Alle projecten**.</span><span class="sxs-lookup"><span data-stu-id="b03e3-123">Click **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="b03e3-124">Open het project met de serviceorder waarin een artikelbehoefte wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="b03e3-124">Open the project that has the service order in which an item requirement is created.</span></span>

3.  <span data-ttu-id="b03e3-125">In het formulier **Projecten** in het rechterdeelvenster klikt u op **Artikelbehoeften**.</span><span class="sxs-lookup"><span data-stu-id="b03e3-125">In the **Projects** form, in the right pane, click **Item requirements**.</span></span> <span data-ttu-id="b03e3-126">Het formulier **Artikelbehoeften** wordt geopend met de artikelbehoeften die aan het geselecteerde project zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="b03e3-126">The **Item requirements** form lists the item requirements that are associated with the selected project.</span></span>

4.  <span data-ttu-id="b03e3-127">Selecteer de artikelbehoefte die u wilt verwijderen en klik vervolgens op **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="b03e3-127">Select the item requirement to delete, and then click **Delete**.</span></span>

## <a name="see-also"></a><span data-ttu-id="b03e3-128">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b03e3-128">See also</span></span>

<span data-ttu-id="b03e3-129">[Artikelbehoeften (formulier)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="b03e3-129">[Item requirements (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]