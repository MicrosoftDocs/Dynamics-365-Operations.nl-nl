---
title: Product staat in wachtstand voor transacties
description: Wanneer u planningsorders hebt gefiatteerd, ontvangt u een foutbericht dat een artikel in de wachtstand staat voor transacties.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6654e6437a088218db116b955631be4c7e62de5f
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301274"
---
# <a name="product-is-on-hold-for-transactions"></a><span data-ttu-id="5fc91-103">Product staat in wachtstand voor transacties</span><span class="sxs-lookup"><span data-stu-id="5fc91-103">Product is on hold for transactions</span></span>

<span data-ttu-id="5fc91-104">Foutcode: SYS13295</span><span class="sxs-lookup"><span data-stu-id="5fc91-104">Error code: SYS13295</span></span>

## <a name="symptoms"></a><span data-ttu-id="5fc91-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="5fc91-105">Symptoms</span></span>

<span data-ttu-id="5fc91-106">Wanneer u geplande orders hebt gefiateerd, wordt het volgende foutbericht weergegeven:</span><span class="sxs-lookup"><span data-stu-id="5fc91-106">After you firm planned orders, you receive the following error message:</span></span>

> <span data-ttu-id="5fc91-107">Artikel %1 is geblokkeerd voor transacties in %2.</span><span class="sxs-lookup"><span data-stu-id="5fc91-107">Item %1 is on hold for transactions in %2.</span></span>

## <a name="cause"></a><span data-ttu-id="5fc91-108">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="5fc91-108">Cause</span></span>

<span data-ttu-id="5fc91-109">Wanneer geblokkeerde artikelen worden beschreven, worden de termen *geblokkeerd*, *gestopt* en *in wachtstand* door elkaar gebruikt.</span><span class="sxs-lookup"><span data-stu-id="5fc91-109">When describing blocked items, system uses the terms *blocked*, *stopped*, and *on hold* interchangeably.</span></span> <span data-ttu-id="5fc91-110">Dit betekent dat het artikel is ingesteld op **Gestopt** in de standaardorderinstellingen.</span><span class="sxs-lookup"><span data-stu-id="5fc91-110">This error means that the item is set as **Stopped** in its default order settings.</span></span>

<span data-ttu-id="5fc91-111">Als een artikel is geblokkeerd en u voegt het toe aan een inkoop- of verkooporderregel, ontvangt u een waarschuwingsbericht.</span><span class="sxs-lookup"><span data-stu-id="5fc91-111">If an item is blocked, and you add it to a purchase order or sales order line, you receive a warning message.</span></span> <span data-ttu-id="5fc91-112">Als een artikel is geblokkeerd, kunnen voorraadtransacties die zijn gerelateerd aan de inkooporder- of verkooporderregel niet worden gewijzigd, bijvoorbeeld als u een pakbon of factuur boekt.</span><span class="sxs-lookup"><span data-stu-id="5fc91-112">When an item is blocked, inventory transactions that are related to the purchase order or sales order line can't be modified (for example, when you post a packing slip or an invoice).</span></span> <span data-ttu-id="5fc91-113">U kunt een ingekocht artikel blokkeren en het artikel tegelijkertijd verkopen.</span><span class="sxs-lookup"><span data-stu-id="5fc91-113">You can block a purchased item, and, at the same time, sell the item.</span></span> <span data-ttu-id="5fc91-114">In dit geval is het selectievakje **Gestopt** ingeschakeld op een inkooporder. Het artikel is echter niet geblokkeerd in voorraad of op een verkooporder.</span><span class="sxs-lookup"><span data-stu-id="5fc91-114">In this case, the **Stopped** check box is selected on a purchase order, but the item isn't blocked in inventory or on a sales order.</span></span>

<span data-ttu-id="5fc91-115">Hieronder staan enkele voorwaarden die ertoe leiden dat een artikelnummer kan worden geblokkeerd voor verkoop:</span><span class="sxs-lookup"><span data-stu-id="5fc91-115">Here are some of the conditions that can cause an item number to be blocked from being sold:</span></span>

- <span data-ttu-id="5fc91-116">Het artikel wordt nog ontwikkeld of gemaakt.</span><span class="sxs-lookup"><span data-stu-id="5fc91-116">The item is still under development or manufacture.</span></span> <span data-ttu-id="5fc91-117">Daarom wilt u niet dat het wordt verkocht of gereserveerd.</span><span class="sxs-lookup"><span data-stu-id="5fc91-117">Therefore, you don't want it to be sold or reserved.</span></span>
- <span data-ttu-id="5fc91-118">U hebt een groot aantal defecte artikelen ontvangen en de defecten moeten worden gecorrigeerd voordat het artikel kan worden verkocht.</span><span class="sxs-lookup"><span data-stu-id="5fc91-118">You've received many defective items, and the defects must be corrected before the item can be sold.</span></span>

<span data-ttu-id="5fc91-119">U kunt in dit soort gevallen het artikel blokkeren totdat het probleem is opgelost.</span><span class="sxs-lookup"><span data-stu-id="5fc91-119">In cases of this type, you can block the item until the issue is resolved.</span></span>

<span data-ttu-id="5fc91-120">Als een artikel is geblokkeerd en u een retourorderregel maakt, ontvangt u een bericht.</span><span class="sxs-lookup"><span data-stu-id="5fc91-120">If an item is blocked, and you create a return order line, you receive a message.</span></span> <span data-ttu-id="5fc91-121">U kunt niet een reeks of partij van een artikel blokkeren.</span><span class="sxs-lookup"><span data-stu-id="5fc91-121">You can't block a series or a lot of an item.</span></span> <span data-ttu-id="5fc91-122">Als onderdelen van een artikel moeten worden geblokkeerd, kunt u dit doen door voorraad te verplaatsen of de volledige voorraad van het artikel voor de desbetreffende periode te blokkeren.</span><span class="sxs-lookup"><span data-stu-id="5fc91-122">If parts of an item must be blocked, you can block them by moving inventory or by blocking the full stock of the item for that period.</span></span>

## <a name="resolution"></a><span data-ttu-id="5fc91-123">Oplossing</span><span class="sxs-lookup"><span data-stu-id="5fc91-123">Resolution</span></span>

- <span data-ttu-id="5fc91-124">Open de pagina **Standaardorderinstellingen** voor het artikel en schakel het selectievakje **Gestopt** uit.</span><span class="sxs-lookup"><span data-stu-id="5fc91-124">Open the **Default order settings** page for the item, and clear the **Stopped** checkbox.</span></span>
