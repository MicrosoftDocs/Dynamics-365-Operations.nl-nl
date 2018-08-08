---
title: Artikelbehoeften voor serviceorders maken
description: Als u specifieke artikelen voor een serviceorder moet reserveren, kunt u er voorraadartikelbehoeften voor maken.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: a5a730ae945af15c7bd4020c734bac971d8186e2
ms.contentlocale: nl-nl
ms.lasthandoff: 08/07/2018

---

# <a name="create-item-requirements-for-service-orders"></a><span data-ttu-id="34240-103">Artikelbehoeften voor serviceorders maken</span><span class="sxs-lookup"><span data-stu-id="34240-103">Create item requirements for service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="34240-104">U kunt een serviceorder maken om services, die u aan uw klanten levert, bij te houden en te beheren.</span><span class="sxs-lookup"><span data-stu-id="34240-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="34240-105">Als u specifieke artikelen voor een serviceorder moet reserveren, kunt u er voorraadartikelbehoeften voor maken.</span><span class="sxs-lookup"><span data-stu-id="34240-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="34240-106">Een artikelbehoefte kan direct worden verbruikt vanuit de voorraad, of er kan een productieorder of inkooporder voor het artikel mee worden geïnitialiseerd.</span><span class="sxs-lookup"><span data-stu-id="34240-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="34240-107">Door een artikelbehoefte te maken in plaats van een artikeltransactie kunt u de levering plannen vlak voordat het artikel werkelijk wordt gebruikt, een inkooporder maken, het artikel opnemen in het handelsovereenkomstframework en de artikelbehoefte opnemen in de productieplanning.</span><span class="sxs-lookup"><span data-stu-id="34240-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="34240-108">Artikelbehoeften voor serviceorders worden verwerkt via een project.</span><span class="sxs-lookup"><span data-stu-id="34240-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="34240-109">Als u een artikelbehoefte wilt maken voor een serviceorder, moet de serviceorder worden toegewezen aan een project.</span><span class="sxs-lookup"><span data-stu-id="34240-109">To create an item requirement on a service order, the service order must be assigned to a project.</span></span> <span data-ttu-id="34240-110">Nadat u een artikelbehoefte voor een serviceorder hebt gemaakt, kunt u de artikelbehoefte weergeven in het formulier**Projecten** voor het geselecteerde project.</span><span class="sxs-lookup"><span data-stu-id="34240-110">After you create an item requirement for a service order, you can view the item requirement in the **Projects** form for the selected project.</span></span>

## <a name="create-an-item-requirement-for-a-service-order"></a><span data-ttu-id="34240-111">Een artikelbehoefte maken voor een serviceorder</span><span class="sxs-lookup"><span data-stu-id="34240-111">Create an item requirement for a service order</span></span>

1.  <span data-ttu-id="34240-112">Klik op **Servicebeheer** \> **Algemeen** \> **Serviceorders** \> **Serviceorders**.</span><span class="sxs-lookup"><span data-stu-id="34240-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="34240-113">Selecteer de serviceorder waarvoor u een artikelbehoefte wilt maken.</span><span class="sxs-lookup"><span data-stu-id="34240-113">Select the service order that you want to create an item requirement for.</span></span>

3.  <span data-ttu-id="34240-114">Klik in het **Actievenster** op het tabblad **Verzenden** op **Artikelbehoefte**.</span><span class="sxs-lookup"><span data-stu-id="34240-114">On the **Action Pane**, on the **Dispatch** tab, click **Item requirement**.</span></span>

4.  <span data-ttu-id="34240-115">Voer in het formulier **Artikelbehoeften** de informatie voor het vereiste artikel in.</span><span class="sxs-lookup"><span data-stu-id="34240-115">In the **Item requirements** form, enter information for the required item.</span></span> <span data-ttu-id="34240-116">Zie voor meer informatie over de specifieke velden [Artikelbehoeften (formulier)](https://technet.microsoft.com/en-us/library/aa552021\(v=ax.60\)).</span><span class="sxs-lookup"><span data-stu-id="34240-116">For more information about the specific fields, see [Item requirements (form)](https://technet.microsoft.com/en-us/library/aa552021\(v=ax.60\)).</span></span>

## <a name="create-an-item-requirement-for-a-service-agreement"></a><span data-ttu-id="34240-117">Een artikelbehoefte maken voor een serviceovereenkomst</span><span class="sxs-lookup"><span data-stu-id="34240-117">Create an item requirement for a service agreement</span></span>

1.  <span data-ttu-id="34240-118">Klik op **Servicebeheer** \> **Algemeen** \> **Serviceovereenkomsten** \> **Serviceovereenkomsten**.</span><span class="sxs-lookup"><span data-stu-id="34240-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="34240-119">Open de serviceovereenkomst waarvoor u een artikelbehoefte wilt maken.</span><span class="sxs-lookup"><span data-stu-id="34240-119">Open the service agreement for which you want to create an item requirement.</span></span>

3.  <span data-ttu-id="34240-120">Klik op het sneltabblad **Regels** op **Toevoegen** om een nieuwe regel te maken.</span><span class="sxs-lookup"><span data-stu-id="34240-120">On the **Lines** FastTab, click **Add** to create a new line.</span></span>

4.  <span data-ttu-id="34240-121">Selecteer in het veld **Transactietype** **Artikel**.</span><span class="sxs-lookup"><span data-stu-id="34240-121">In the **Transaction type** field, select **Item**.</span></span>

5.  <span data-ttu-id="34240-122">Selecteer in het veld **Artikelinstellingen** **Artikelbehoefte**.</span><span class="sxs-lookup"><span data-stu-id="34240-122">In the **Item setup** field, select **Item requirement**.</span></span>

6.  <span data-ttu-id="34240-123">Selecteer in het veld **Artikelnummer** het artikel dat is vereist voor de serviceovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="34240-123">In the **Item number** field, select the item that is required for the service agreement.</span></span>

7.  <span data-ttu-id="34240-124">Selecteer op het sneltabblad **Regeldetails** op het tabblad **Productdimensies** in het veld **Site** de voorraadlocatie voor het artikel.</span><span class="sxs-lookup"><span data-stu-id="34240-124">On the **Line details** FastTab, on the **Product dimensions** tab, in the **Site** field, select the inventory site for the item.</span></span>

8.  <span data-ttu-id="34240-125">Als u een serviceorder op basis van de overeenkomstregel wilt maken, klikt u op het sneltabblad **Regels** op **Serviceorders maken** en voert u vervolgens de relevante informatie in het formulier **Serviceorders maken** in.</span><span class="sxs-lookup"><span data-stu-id="34240-125">To create a service order from the agreement line, on the **Lines** FastTab, click **Create service orders**, and then enter the relevant information in the **Create service orders** form.</span></span> 


## <a name="see-also"></a><span data-ttu-id="34240-126">Zie ook</span><span class="sxs-lookup"><span data-stu-id="34240-126">See also</span></span>

<span data-ttu-id="34240-127">[Automatisch serviceorders maken](create-service-orders-automatically.md).</span><span class="sxs-lookup"><span data-stu-id="34240-127">[Create service orders automatically](create-service-orders-automatically.md).</span></span>

  



