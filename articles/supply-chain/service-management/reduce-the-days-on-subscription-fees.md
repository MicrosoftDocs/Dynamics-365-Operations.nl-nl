---
title: De dagen van abonnementskosten verminderen
description: Als u het aantal dagen van bestaande abonnementskosten wilt beperken, kunt u een nieuwe transactie maken waarin u de periode verwijdert die geen deel meer moet uitmaken van het abonnementskosteninterval.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 04b183d8fc8083c630bcb4e0e69fb755f8a50f95
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "361999"
---
# <a name="reduce-the-days-on-subscription-fees"></a><span data-ttu-id="1831c-103">De dagen van abonnementskosten verminderen</span><span class="sxs-lookup"><span data-stu-id="1831c-103">Reduce the days on subscription fees</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="1831c-104">Als u het aantal dagen van bestaande abonnementskosten wilt beperken, kunt u een nieuwe transactie maken waarin u de periode verwijdert die geen deel meer moet uitmaken van het abonnementskosteninterval.</span><span class="sxs-lookup"><span data-stu-id="1831c-104">To reduce the number of days of an existing subscription fee, you can create a new transaction in which you remove the period of time that should no longer be part of the subscription fee interval.</span></span>

## <a name="reduce-the-days-on-a-subscription-fee"></a><span data-ttu-id="1831c-105">Het aantal dagen van abonnementskosten beperken</span><span class="sxs-lookup"><span data-stu-id="1831c-105">Reduce the days on a subscription fee</span></span>

1.  <span data-ttu-id="1831c-106">Klik op **Servicebeheer** \> **Algemeen** \> **Serviceabonnementen** \> **Alle serviceabonnementen**.</span><span class="sxs-lookup"><span data-stu-id="1831c-106">Click **Service management** \> **Common** \> **Service subscriptions** \> **All service subscriptions**.</span></span> <span data-ttu-id="1831c-107">Selecteer het serviceabonnement en klik in het actievenster op **Abonnementskosten**</span><span class="sxs-lookup"><span data-stu-id="1831c-107">Select the service subscription, and on the Action Pane, click **Subscription fees**</span></span>

2.  <span data-ttu-id="1831c-108">Selecteer in het veld **Abonnementstype** **Reductiedagen**.</span><span class="sxs-lookup"><span data-stu-id="1831c-108">In the **Subscription type** field, select **Reduction days**.</span></span>

3.  <span data-ttu-id="1831c-109">Gebruik de velden **Datum vanaf** en **Datum t/m** om het datuminterval op te geven van de abonnementskosten die u wilt verwijderen uit de periode van de abonnementskosten en klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="1831c-109">Use the **From date** field and the **To date** fields to define the date interval of the subscription fee that you want to remove from the subscription fee period, and then click **OK**.</span></span>

<span data-ttu-id="1831c-110">Als u de gemaakte transactie wilt weergeven, klikt u in het formulier **Abonnement** op **Tarieftransacties**.</span><span class="sxs-lookup"><span data-stu-id="1831c-110">To view the transaction that was created, in the **Subscription** form, click **Fee transactions**.</span></span>

## <a name="example"></a><span data-ttu-id="1831c-111">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="1831c-111">Example</span></span>

<span data-ttu-id="1831c-112">Als de periode van een abonnementstransactie loopt van 1 januari tot 31 januari en u de periode wilt verkorten met tien dagen, maakt u een nieuwe transactie waarin de reductieperiode 1 januari tot 10 januari is.</span><span class="sxs-lookup"><span data-stu-id="1831c-112">If a subscription transaction period runs from January 1 to January 31, and you want to reduce the period by 10 days, create a new transaction in which the reduction period is January 1 to January 10.</span></span> <span data-ttu-id="1831c-113">(De reductieperiode kan ook 5 januari tot 15 januari zijn of een andere periode van 10 dagen.)</span><span class="sxs-lookup"><span data-stu-id="1831c-113">(The reduction period could also be January 5 to January 15, or any other ten day period).</span></span>

<span data-ttu-id="1831c-114">Als **Datum vanaf** in de reductieperiode 21 januari is (31 min 10), kunt u bovendien de **Datum t/m** instellen op elke gewenste datum na 31 januari, waarna nog steeds tien dagen worden verwijderd uit de periode van de bijzondere-kostentransactie.</span><span class="sxs-lookup"><span data-stu-id="1831c-114">Also, if the **From date** on the reduction period is January 21 (31 minus 10), you could set the **To date** to any date after January 31, and 10 days will still be removed from the fee transaction period.</span></span>

## <a name="see-also"></a><span data-ttu-id="1831c-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1831c-115">See also</span></span>

[<span data-ttu-id="1831c-116">Voorbeeld van reductiedagen</span><span class="sxs-lookup"><span data-stu-id="1831c-116">Reduction days example</span></span>](reduction-days-example.md)

  


