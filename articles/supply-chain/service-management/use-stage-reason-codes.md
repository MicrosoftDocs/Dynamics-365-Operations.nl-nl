---
title: Redencodes voor de gebruiksfase
description: U gebruikt een redencode om aan te geven waarom een SLA (Service Level Agreement) is geannuleerd of waarom een serviceorder de tijdslimiet die u in de SLA hebt gedefinieerd, heeft overschreden.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 220012011e6fb1818cffa3992a3c39f46e5c071a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259621"
---
# <a name="use-stage-reason-codes"></a><span data-ttu-id="97f75-103">Redencodes voor de gebruiksfase</span><span class="sxs-lookup"><span data-stu-id="97f75-103">Use stage reason codes</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="97f75-104">U gebruikt een redencode om aan te geven waarom een SLA (Service Level Agreement) is geannuleerd of waarom een serviceorder de tijdslimiet die u in de SLA hebt gedefinieerd, heeft overschreden.</span><span class="sxs-lookup"><span data-stu-id="97f75-104">You use a reason code to indicate why a service level agreement (SLA) has been canceled, or why a service order has exceeded the time limit that is you define in the SLA.</span></span>

<span data-ttu-id="97f75-105">U kunt ook opgeven dat een redencode vereist is wanneer een SLA wordt geannuleerd, of wanneer de tijdslimiet de tijd overschrijdt die is opgegeven in de SLA voor de serviceorder.</span><span class="sxs-lookup"><span data-stu-id="97f75-105">You can also specify that a reason code is required when an SLA is canceled, or when the time limit exceeds the time that is specified in the SLA for the service order.</span></span>

<span data-ttu-id="97f75-106">Als u hebt opgegeven dat een redencode vereist is, moet u een redencode invoeren in de volgende situaties:</span><span class="sxs-lookup"><span data-stu-id="97f75-106">If you have specified that a reason code is required, you must enter a reason code in the following situations:</span></span>

  - <span data-ttu-id="97f75-107">Wanneer de serviceorder wordt verplaatst naar een fase waarin de tijdregistratie van de SLA wordt gestopt voor de serviceorder.</span><span class="sxs-lookup"><span data-stu-id="97f75-107">When a service order is moved to a stage that stops time recording against the SLA for the service order.</span></span>

  - <span data-ttu-id="97f75-108">Wanneer de serviceorder wordt afgemeld.</span><span class="sxs-lookup"><span data-stu-id="97f75-108">When the service order is signed off.</span></span>

  - <span data-ttu-id="97f75-109">Wanneer de tijdregistratie handmatig wordt gestopt.</span><span class="sxs-lookup"><span data-stu-id="97f75-109">When time recording is manually stopped.</span></span>

## <a name="set-up-reason-codes"></a><span data-ttu-id="97f75-110">Redencodes instellen</span><span class="sxs-lookup"><span data-stu-id="97f75-110">Set up reason codes</span></span>

1.  <span data-ttu-id="97f75-111">Klik op **Servicebeheer** \> **Instellen** \> **Serviceorders** \> **Redencodes voor fase**.</span><span class="sxs-lookup"><span data-stu-id="97f75-111">Click **Service management** \> **Setup** \> **Service orders** \> **Stage reason codes**.</span></span>

2.  <span data-ttu-id="97f75-112">Klik in het formulier **Redencode voor de fase** op **Nieuw** om een nieuwe redencode te maken.</span><span class="sxs-lookup"><span data-stu-id="97f75-112">In the **Stage reason codes** form, click **New** to create a new reason code.</span></span>

3.  <span data-ttu-id="97f75-113">Voer in het veld **Redencode voor de fase** een unieke redencode voor de fase in.</span><span class="sxs-lookup"><span data-stu-id="97f75-113">In the **Stage reason code** field, enter a unique stage reason code.</span></span>

4.  <span data-ttu-id="97f75-114">Voer in het veld **Beschrijving** een omschrijving van de redencode voor de fase in.</span><span class="sxs-lookup"><span data-stu-id="97f75-114">In the **Description** field, enter a description of the stage reason code.</span></span>

5.  <span data-ttu-id="97f75-115">Sluit het formulier om de wijzigingen op te slaan.</span><span class="sxs-lookup"><span data-stu-id="97f75-115">Close the form to save your changes.</span></span>

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a><span data-ttu-id="97f75-116">Redencodes vereisen wanneer een SLA wordt geannuleerd</span><span class="sxs-lookup"><span data-stu-id="97f75-116">Require reason codes when a service level agreement is canceled</span></span>

1.  <span data-ttu-id="97f75-117">Klik op **Servicebeheer** \> **Instellen** \> **Parameters voor servicebeheer**.</span><span class="sxs-lookup"><span data-stu-id="97f75-117">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="97f75-118">Klik in het formulier **Parameters voor servicebeheer** op de koppeling **Algemeen** en schakel vervolgens het selectievakje **Redencode bij annuleren** in.</span><span class="sxs-lookup"><span data-stu-id="97f75-118">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on canceling** check box.</span></span>

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a><span data-ttu-id="97f75-119">Redencodes vereisen wanneer een serviceorder de ingestelde tijdslimiet voor de SLA overschrijdt</span><span class="sxs-lookup"><span data-stu-id="97f75-119">Require reason codes when the a service order exceeds the time limit that is set by the service level agreement</span></span>

1.  <span data-ttu-id="97f75-120">Klik op **Servicebeheer** \> **Instellen** \> **Parameters voor servicebeheer**.</span><span class="sxs-lookup"><span data-stu-id="97f75-120">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="97f75-121">Klik in het formulier **Parameters voor servicebeheer** op de koppeling **Algemeen** en schakel vervolgens het selectievakje **Redencode bij overschrijden van tijd** in.</span><span class="sxs-lookup"><span data-stu-id="97f75-121">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on exceeding time** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="97f75-122">Zie ook</span><span class="sxs-lookup"><span data-stu-id="97f75-122">See also</span></span>

[<span data-ttu-id="97f75-123">Tijdregistratie voor een serviceorder starten en stoppen</span><span class="sxs-lookup"><span data-stu-id="97f75-123">Start and stop time recording on a service order</span></span>](start-and-stop-time-recording-on-a-service-order.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]