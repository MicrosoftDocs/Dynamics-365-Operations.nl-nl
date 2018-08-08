---
title: Redencodes voor de gebruiksfase
description: U gebruikt een redencode om aan te geven waarom een SLA (Service Level Agreement) is geannuleerd of waarom een serviceorder de tijdslimiet die u in de SLA hebt gedefinieerd, heeft overschreden.
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAParameters
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
ms.openlocfilehash: 33fa7e5f08f09fe109d0507d686315d01e043928
ms.contentlocale: nl-nl
ms.lasthandoff: 08/07/2018

---


# <a name="use-stage-reason-codes"></a><span data-ttu-id="9c078-103">Redencodes voor de gebruiksfase</span><span class="sxs-lookup"><span data-stu-id="9c078-103">Use stage reason codes</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="9c078-104">U gebruikt een redencode om aan te geven waarom een SLA (Service Level Agreement) is geannuleerd of waarom een serviceorder de tijdslimiet die u in de SLA hebt gedefinieerd, heeft overschreden.</span><span class="sxs-lookup"><span data-stu-id="9c078-104">You use a reason code to indicate why a service level agreement (SLA) has been canceled, or why a service order has exceeded the time limit that is you define in the SLA.</span></span>

<span data-ttu-id="9c078-105">U kunt ook opgeven dat een redencode vereist is wanneer een SLA wordt geannuleerd, of wanneer de tijdslimiet de tijd overschrijdt die is opgegeven in de SLA voor de serviceorder.</span><span class="sxs-lookup"><span data-stu-id="9c078-105">You can also specify that a reason code is required when an SLA is canceled, or when the time limit exceeds the time that is specified in the SLA for the service order.</span></span>

<span data-ttu-id="9c078-106">Als u hebt opgegeven dat een redencode vereist is, moet u een redencode invoeren in de volgende situaties:</span><span class="sxs-lookup"><span data-stu-id="9c078-106">If you have specified that a reason code is required, you must enter a reason code in the following situations:</span></span>

  - <span data-ttu-id="9c078-107">Wanneer de serviceorder wordt verplaatst naar een fase waarin de tijdregistratie van de SLA wordt gestopt voor de serviceorder.</span><span class="sxs-lookup"><span data-stu-id="9c078-107">When a service order is moved to a stage that stops time recording against the SLA for the service order.</span></span>

  - <span data-ttu-id="9c078-108">Wanneer de serviceorder wordt afgemeld.</span><span class="sxs-lookup"><span data-stu-id="9c078-108">When the service order is signed off.</span></span>

  - <span data-ttu-id="9c078-109">Wanneer de tijdregistratie handmatig wordt gestopt.</span><span class="sxs-lookup"><span data-stu-id="9c078-109">When time recording is manually stopped.</span></span>

## <a name="set-up-reason-codes"></a><span data-ttu-id="9c078-110">Redencodes instellen</span><span class="sxs-lookup"><span data-stu-id="9c078-110">Set up reason codes</span></span>

1.  <span data-ttu-id="9c078-111">Klik op **Servicebeheer** \> **Instellen** \> **Serviceorders** \> **Redencodes voor fase**.</span><span class="sxs-lookup"><span data-stu-id="9c078-111">Click **Service management** \> **Setup** \> **Service orders** \> **Stage reason codes**.</span></span>

2.  <span data-ttu-id="9c078-112">Klik in het formulier **Redencode voor de fase** op **Nieuw** om een nieuwe redencode te maken.</span><span class="sxs-lookup"><span data-stu-id="9c078-112">In the **Stage reason codes** form, click **New** to create a new reason code.</span></span>

3.  <span data-ttu-id="9c078-113">Voer in het veld **Redencode voor de fase** een unieke redencode voor de fase in.</span><span class="sxs-lookup"><span data-stu-id="9c078-113">In the **Stage reason code** field, enter a unique stage reason code.</span></span>

4.  <span data-ttu-id="9c078-114">Voer in het veld **Beschrijving** een omschrijving van de redencode voor de fase in.</span><span class="sxs-lookup"><span data-stu-id="9c078-114">In the **Description** field, enter a description of the stage reason code.</span></span>

5.  <span data-ttu-id="9c078-115">Sluit het formulier om de wijzigingen op te slaan.</span><span class="sxs-lookup"><span data-stu-id="9c078-115">Close the form to save your changes.</span></span>

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a><span data-ttu-id="9c078-116">Redencodes vereisen wanneer een SLA wordt geannuleerd</span><span class="sxs-lookup"><span data-stu-id="9c078-116">Require reason codes when a service level agreement is canceled</span></span>

1.  <span data-ttu-id="9c078-117">Klik op **Servicebeheer** \> **Instellen** \> **Parameters voor servicebeheer**.</span><span class="sxs-lookup"><span data-stu-id="9c078-117">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="9c078-118">Klik in het formulier **Parameters voor servicebeheer** op de koppeling **Algemeen** en schakel vervolgens het selectievakje **Redencode bij annuleren** in.</span><span class="sxs-lookup"><span data-stu-id="9c078-118">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on canceling** check box.</span></span>

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a><span data-ttu-id="9c078-119">Redencodes vereisen wanneer een serviceorder de ingestelde tijdslimiet voor de SLA overschrijdt</span><span class="sxs-lookup"><span data-stu-id="9c078-119">Require reason codes when the a service order exceeds the time limit that is set by the service level agreement</span></span>

1.  <span data-ttu-id="9c078-120">Klik op **Servicebeheer** \> **Instellen** \> **Parameters voor servicebeheer**.</span><span class="sxs-lookup"><span data-stu-id="9c078-120">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="9c078-121">Klik in het formulier **Parameters voor servicebeheer** op de koppeling **Algemeen** en schakel vervolgens het selectievakje **Redencode bij overschrijden van tijd** in.</span><span class="sxs-lookup"><span data-stu-id="9c078-121">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on exceeding time** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="9c078-122">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9c078-122">See also</span></span>

[<span data-ttu-id="9c078-123">Tijdregistratie voor een serviceorder starten en stoppen</span><span class="sxs-lookup"><span data-stu-id="9c078-123">Start and stop time recording on a service order</span></span>](start-and-stop-time-recording-on-a-service-order.md)

  



