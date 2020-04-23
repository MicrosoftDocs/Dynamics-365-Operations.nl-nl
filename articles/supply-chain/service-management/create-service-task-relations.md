---
title: Servicetaakrelaties maken
description: U kunt servicetaken koppelen aan serviceovereenkomsten of serviceorders om de servicetaak te omschrijven die moet worden uitgevoerd voor de overeenkomst of order.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b167714dc81cf0e4ee70d7092f2ec030043abe71
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202601"
---
# <a name="create-service-task-relations"></a><span data-ttu-id="43b91-103">Servicetaakrelaties maken</span><span class="sxs-lookup"><span data-stu-id="43b91-103">Create service task relations</span></span>    

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43b91-104">U kunt servicetaken koppelen aan serviceovereenkomsten of serviceorders om de servicetaak te omschrijven die moet worden uitgevoerd voor de overeenkomst of order.</span><span class="sxs-lookup"><span data-stu-id="43b91-104">You can associate service tasks with service agreements or service orders in order to describe the service task to be completed for the agreement or order.</span></span> <span data-ttu-id="43b91-105">Deze informatie is beschikbaar voor servicemonteurs en klanten.</span><span class="sxs-lookup"><span data-stu-id="43b91-105">This information is available to service technicians and customers.</span></span>

## <a name="create-a-relation-with-a-service-agreement"></a><span data-ttu-id="43b91-106">Een relatie maken met een serviceovereenkomst</span><span class="sxs-lookup"><span data-stu-id="43b91-106">Create a relation with a service agreement</span></span>

1.  <span data-ttu-id="43b91-107">Klik op **Servicebeheer** \> **Algemeen** \> **Serviceovereenkomsten** \> **Serviceovereenkomsten**.</span><span class="sxs-lookup"><span data-stu-id="43b91-107">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="43b91-108">Selecteer een bestaande serviceovereenkomst of maak een nieuwe serviceovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="43b91-108">Select an existing service agreement, or create a new service agreement.</span></span>

3.  <span data-ttu-id="43b91-109">Klik in het actievenster op de knop **Servicetaken**.</span><span class="sxs-lookup"><span data-stu-id="43b91-109">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="43b91-110">Druk in het formulier **Servicetaken** op CTRL+N om een nieuwe regel te maken en selecteer vervolgens een servicetaak in de lijst **Servicetaak** om de servicetaak te koppelen aan de serviceovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="43b91-110">On the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service task to the service agreement.</span></span>

5.  <span data-ttu-id="43b91-111">Voer op het tabblad **Beschrijving** interne of externe notitieomschrijvingen in de vrije-tekstvelden in.</span><span class="sxs-lookup"><span data-stu-id="43b91-111">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="43b91-112">Sluit het formulier om de record op te slaan.</span><span class="sxs-lookup"><span data-stu-id="43b91-112">Close the form to save the record.</span></span>

<span data-ttu-id="43b91-113">Herhaal deze procedure totdat u alle benodigde servicetaakrelaties hebt gemaakt voor de serviceovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="43b91-113">Repeat this procedure until you have created all the necessary service task relations for the service agreement.</span></span> <span data-ttu-id="43b91-114">U kunt deze servicetaken nu opgeven voor gekoppelde overeenkomstregels.</span><span class="sxs-lookup"><span data-stu-id="43b91-114">You can now specify these service tasks for any attached agreement lines.</span></span>

<span data-ttu-id="43b91-115">Een servicetaakrelatie die is gemaakt voor een serviceovereenkomst, is beschikbaar vanuit alle serviceorders die aan de serviceovereenkomst zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="43b91-115">A service tasks relation that is created on a service agreement is available from all service orders that are attached to the service agreement.</span></span>

## <a name="create-a-relation-with-a-service-order"></a><span data-ttu-id="43b91-116">Een relatie maken met een serviceorder</span><span class="sxs-lookup"><span data-stu-id="43b91-116">Create a relation with a service order</span></span>

1.  <span data-ttu-id="43b91-117">Klik op **Servicebeheer** \> **Algemeen** \> **Serviceorders** \> **Serviceorders**.</span><span class="sxs-lookup"><span data-stu-id="43b91-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="43b91-118">Selecteer een bestaande serviceorder of maak een nieuwe serviceorder.</span><span class="sxs-lookup"><span data-stu-id="43b91-118">Select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="43b91-119">Klik in het actievenster op de knop **Servicetaken**.</span><span class="sxs-lookup"><span data-stu-id="43b91-119">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="43b91-120">Druk in het formulier **Servicetaken** op CTRL+N om een nieuwe regel te maken en selecteer vervolgens een servicetaak in de lijst **Servicetaak** om de servicetaken te koppelen aan de serviceorder.</span><span class="sxs-lookup"><span data-stu-id="43b91-120">From the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service tasks to the service order.</span></span>

5.  <span data-ttu-id="43b91-121">Voer op het tabblad **Beschrijving** interne of externe notitieomschrijvingen in de vrije-tekstvelden in.</span><span class="sxs-lookup"><span data-stu-id="43b91-121">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="43b91-122">Sluit het formulier om de record op te slaan.</span><span class="sxs-lookup"><span data-stu-id="43b91-122">Close the form to save the record.</span></span>

<span data-ttu-id="43b91-123">Herhaal deze procedure totdat u alle benodigde servicetaakrelaties hebt gemaakt voor de serviceorder.</span><span class="sxs-lookup"><span data-stu-id="43b91-123">Repeat this procedure until you have created all the necessary service task relations for the service order.</span></span> <span data-ttu-id="43b91-124">U kunt nu de servicetaak waarvoor u de relatie hebt gemaakt, selecteren wanneer u serviceorderregels maakt.</span><span class="sxs-lookup"><span data-stu-id="43b91-124">You can now select the service task for which you have created the relation when you create service order lines.</span></span>

<span data-ttu-id="43b91-125">De servicetaakrelaties die zijn gemaakt voor een serviceorder, zijn beschikbaar op de desbetreffende serviceorder.</span><span class="sxs-lookup"><span data-stu-id="43b91-125">Service task relations that are created on a service order are available on the specific service order.</span></span>

## <a name="see-also"></a><span data-ttu-id="43b91-126">Zie ook</span><span class="sxs-lookup"><span data-stu-id="43b91-126">See also</span></span>

[<span data-ttu-id="43b91-127">Overzicht van Servicetaken</span><span class="sxs-lookup"><span data-stu-id="43b91-127">Service tasks overview</span></span>](service-tasks.md)


  


