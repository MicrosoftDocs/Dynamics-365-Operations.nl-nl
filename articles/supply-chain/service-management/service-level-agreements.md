---
title: Servicelevelovereenkomsten
description: In een serviceovereenkomst stemt de klant in met een minimale responstijd gebaseerd op het moment waarop het servicebedrijf een probleem registreert en het moment waarop het probleem is opgelost.
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 63389ed348e9b1bebe00d9aaa9f78b97ac39317b
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="service-level-agreements"></a><span data-ttu-id="fa488-103">Servicelevelovereenkomsten</span><span class="sxs-lookup"><span data-stu-id="fa488-103">Service level agreements</span></span>        

[!include [banner](../includes/banner.md)]


<span data-ttu-id="fa488-104">Een serviceniveauovereenkomst (SLA) is een overeenkomst tussen een servicebedrijf en een serviceklant.</span><span class="sxs-lookup"><span data-stu-id="fa488-104">A service level agreement (SLA) is an agreement between a service company and a service customer.</span></span> <span data-ttu-id="fa488-105">In een SLA stemt de klant in met een minimale responstijd gebaseerd op het moment waarop het servicebedrijf een probleem registreert en het moment waarop het probleem is opgelost.</span><span class="sxs-lookup"><span data-stu-id="fa488-105">In a SLA, the customer agrees to a minimum response time based on when the service company records the issue and when the issue is resolved.</span></span>

<span data-ttu-id="fa488-106">Via een SLA wordt een standaardserviceniveau bepaald dat klanten ontvangen en kan een servicebedrijf ook inschatten wanneer een servicetaak moet zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="fa488-106">A SLA enforces a standard level of service that is offered to customers, and also makes it transparent to a service company when a service job should be completed.</span></span>

<span data-ttu-id="fa488-107">U kunt het gewenste aantal serviceovereenkomsten maken voor de verschillende serviceniveaus voor serviceklanten.</span><span class="sxs-lookup"><span data-stu-id="fa488-107">Any number of SLAs can be created to offer service customers different levels of service.</span></span>

## <a name="create-a-service-level-agreement"></a><span data-ttu-id="fa488-108">Een serviceovereenkomst maken</span><span class="sxs-lookup"><span data-stu-id="fa488-108">Create a service level agreement</span></span>

1.  <span data-ttu-id="fa488-109">Klik op **Servicebeheer** \> **Instellen** \> **Serviceovereenkomsten** \> **Serviceovereenkomsten**.</span><span class="sxs-lookup"><span data-stu-id="fa488-109">Click **Service management** \> **Setup** \> **Service agreements** \> **Service level agreements**.</span></span>

2.  <span data-ttu-id="fa488-110">Selecteer in het veld **Serviceovereenkomst** een naam voor de serviceovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="fa488-110">Type a name for the service level agreement in the **Service level agreement** field.</span></span>

3.  <span data-ttu-id="fa488-111">Typ de tijd in die u wilt toestaan voor de voltooiing van serviceoproepen die zijn gekoppeld aan de serviceniveauovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="fa488-111">Type the time that you want to allow for completion of service calls that are attached to the service level agreement.</span></span> <span data-ttu-id="fa488-112">Selecteer vervolgens een agenda als u de serviceniveauovereenkomst op een specifieke kalender wilt baseren.</span><span class="sxs-lookup"><span data-stu-id="fa488-112">Then select a calendar if you want to base the service level agreement on a specific calendar.</span></span>

## <a name="apply-a-service-level-agreement"></a><span data-ttu-id="fa488-113">Een serviceovereenkomst toepassen</span><span class="sxs-lookup"><span data-stu-id="fa488-113">Apply a service level agreement</span></span>

<span data-ttu-id="fa488-114">De serviceovereenkomst wordt rechtstreeks toegepast.</span><span class="sxs-lookup"><span data-stu-id="fa488-114">The SLA is applied directly to a service agreement.</span></span>

<span data-ttu-id="fa488-115">Serviceorders die u handmatig maakt en aan een serviceovereenkomst met een SLA koppelt, worden gemeten op basis van deze SLA.</span><span class="sxs-lookup"><span data-stu-id="fa488-115">Service orders that you create manually and attach to a service agreement that has an SLA are measured against that SLA.</span></span>

<span data-ttu-id="fa488-116">Serviceorders die automatisch worden gemaakt, worden niet aan een serviceovereenkomst gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="fa488-116">Service orders that you create automatically are not attached to an SLA.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a><span data-ttu-id="fa488-117">Het serviceniveau toepassen op de serviceovereenkomst</span><span class="sxs-lookup"><span data-stu-id="fa488-117">Apply the service level agreement to the service agreement</span></span>

1.  <span data-ttu-id="fa488-118">Klik op **Servicebeheer** \> **Algemeen** \> **Serviceovereenkomsten** \> **Serviceovereenkomsten**.</span><span class="sxs-lookup"><span data-stu-id="fa488-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="fa488-119">Selecteer de serviceovereenkomst waarop u de SLA wilt toepassen en klik vervolgens op **Bewerken** in het **Actievenster**.</span><span class="sxs-lookup"><span data-stu-id="fa488-119">Select the service agreement that you want to apply the SLA to, and then click **Edit** on the **Action Pane**.</span></span>

2.  <span data-ttu-id="fa488-120">Selecteer in het veld **Serviceovereenkomst** de serviceovereenkomst die u wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="fa488-120">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a><span data-ttu-id="fa488-121">De serviceovereenkomst toepassen op de serviceovereenkomstgroep</span><span class="sxs-lookup"><span data-stu-id="fa488-121">Apply the service level agreement to the service agreement group</span></span>

1.  <span data-ttu-id="fa488-122">Klik op **Servicebeheer** \> **Instellen** \> **Serviceovereenkomsten** \> **Serviceovereenkomstgroepen**.</span><span class="sxs-lookup"><span data-stu-id="fa488-122">Click **Service management** \> **Setup** \> **Service agreements** \> **Service agreement groups**.</span></span>

2.  <span data-ttu-id="fa488-123">Selecteer in het veld **Serviceovereenkomst** de serviceovereenkomst die u wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="fa488-123">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="track-time-on-a-service-order-against-an-sla"></a><span data-ttu-id="fa488-124">De tijd bijhouden voor een serviceorder op basis van een serviceovereenkomst</span><span class="sxs-lookup"><span data-stu-id="fa488-124">Track time on a service order against an SLA</span></span>

<span data-ttu-id="fa488-125">Wanneer u een nieuwe serviceorder maakt voor een serviceovereenkomst waaraan een SLA is toegewezen, wordt het tijdsinterval voor de levering van de service gestart en begint het systeem met het bijhouden van de levertijd.</span><span class="sxs-lookup"><span data-stu-id="fa488-125">When you create a new service order for a service agreement that an SLA is assigned to, the time interval for the delivery of the service is initiated, and the system starts to track the delivery time.</span></span> <span data-ttu-id="fa488-126">Daarnaast kunt u de volgende opties instellen:</span><span class="sxs-lookup"><span data-stu-id="fa488-126">Additionally, you can set the following options:</span></span>

  - <span data-ttu-id="fa488-127">U kunt de tijdregistratie voor de serviceorder starten en stoppen om de totale tijd die aan serviceorders is besteed te registreren.</span><span class="sxs-lookup"><span data-stu-id="fa488-127">You can start and stop time recording on the service order to register the total amount of time that is spent on service orders.</span></span>

  - <span data-ttu-id="fa488-128">U kunt controleren of het tijdsinterval overeenkomt met de instelling in de serviceniveauovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="fa488-128">You can monitor compliance with the time interval that is set in the service level agreement.</span></span>

  - <span data-ttu-id="fa488-129">U kunt redencodes definiëren die moeten worden ingesteld als het tijdsinterval van de serviceniveauovereenkomst wordt overschreden.</span><span class="sxs-lookup"><span data-stu-id="fa488-129">You can define reason codes that must be set if the time interval of the service level agreement is exceeded.</span></span>

## <a name="see-also"></a><span data-ttu-id="fa488-130">Zie ook</span><span class="sxs-lookup"><span data-stu-id="fa488-130">See also</span></span>

[<span data-ttu-id="fa488-131">Compatibiliteit met serviceovereenkomsten weergeven</span><span class="sxs-lookup"><span data-stu-id="fa488-131">View compliance with service level agreements</span></span>](view-compliance-with-service-level-agreements.md)

  



