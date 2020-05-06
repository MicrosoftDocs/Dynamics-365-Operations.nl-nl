---
title: Statussen van levenscyclus voor onderhoudsverzoeken
description: In dit onderwerp wordt beschreven hoe u levenscyclusstatussen van onderhoudsverzoeken instelt in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 08c45742b064f3a13a0ea2704f8873b9c53aad4e
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275621"
---
# <a name="maintenance-request-lifecycle-states"></a><span data-ttu-id="d1608-103">Statussen van levenscyclus voor onderhoudsverzoeken</span><span class="sxs-lookup"><span data-stu-id="d1608-103">Maintenance request lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="d1608-104">Levenscyclusstatussen van onderhoudsverzoeken bepalen de fasen die een verzoek kan doorlopen.</span><span class="sxs-lookup"><span data-stu-id="d1608-104">Maintenance request lifecycle states define the stages that a request can go through.</span></span> <span data-ttu-id="d1608-105">Voorbeelden zijn **Gemaakt**, **Actief** en **Beëindigd**.</span><span class="sxs-lookup"><span data-stu-id="d1608-105">Examples include **Created**, **Active**, and **Ended**.</span></span> <span data-ttu-id="d1608-106">Wanneer een onderhoudsverzoek wordt geconverteerd naar een werkorder, moet de levenscyclusstatus van het onderhoudsverzoek worden bijgewerkt naar **Beëindigd** of **Gesloten** om aan te geven dat het onderhoudsverzoek niet langer actief is.</span><span class="sxs-lookup"><span data-stu-id="d1608-106">When a maintenance request is converted to a work order, the maintenance request lifecycle state should be updated to **Ended** or **Closed** to indicate that the maintenance request is no longer active.</span></span> <span data-ttu-id="d1608-107">Op de pagina **Alle onderhoudsverzoeken** worden alle onderhoudsverzoeken weergegeven, ongeacht de levenscyclusstatus.</span><span class="sxs-lookup"><span data-stu-id="d1608-107">On the **All maintenance requests** list page, you can view all maintenance requests, regardless of their lifecycle state.</span></span>

## <a name="set-up-maintenance-request-lifecycle-states"></a><span data-ttu-id="d1608-108">Levenscyclusstatussen van onderhoudsverzoek instellen</span><span class="sxs-lookup"><span data-stu-id="d1608-108">Set up maintenance request lifecycle states</span></span>

1. <span data-ttu-id="d1608-109">Selecteer **Activabeheer** \> **Instellen** \> **Onderhoudsverzoeken** \> **Levenscyclusstatussen**.</span><span class="sxs-lookup"><span data-stu-id="d1608-109">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="d1608-110">Selecteer **Nieuw** om een levenscyclusstatus van een onderhoudsverzoek te maken.</span><span class="sxs-lookup"><span data-stu-id="d1608-110">Select **New** to create a maintenance request lifecycle state.</span></span>
3. <span data-ttu-id="d1608-111">Voer in het veld **Levenscyclusstatus** een id voor de levenscyclusstatus in.</span><span class="sxs-lookup"><span data-stu-id="d1608-111">In the **Lifecycle state** field, enter an ID for the lifecycle state.</span></span>
4. <span data-ttu-id="d1608-112">Voer in het veld **Naam** een naam in.</span><span class="sxs-lookup"><span data-stu-id="d1608-112">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="d1608-113">Op het sneltabblad **Details** wordt in het veld **Levenscyclusmodellen** het aantal levencyclusmodellen van onderhoudsverzoeken weergegeven die deze levenscyclusstatus gebruiken.</span><span class="sxs-lookup"><span data-stu-id="d1608-113">On the **Details** FastTab, the **Lifecycle models** field shows the number of maintenance request lifecycle models that use this lifecycle state.</span></span>

5. <span data-ttu-id="d1608-114">Stel op het sneltabblad **Algemeen** de optie **Actief** in op **Ja** als een onderhoudsverzoek actief moet zijn terwijl deze zich in deze levenscyclusstatus bevindt.</span><span class="sxs-lookup"><span data-stu-id="d1608-114">On the **General** FastTab, set the **Active** option to **Yes** if a maintenance request should be active while it's in this lifecycle state.</span></span>
6. <span data-ttu-id="d1608-115">Stel de optie **Werkelijk einde instellen** in op **Ja** als een werkelijke einddatum en -tijd automatisch moeten worden ingevoerd op een onderhoudsverzoek dat zich in deze levenscyclusstatus bevindt.</span><span class="sxs-lookup"><span data-stu-id="d1608-115">Set the **Set actual end** option to **Yes** if an actual end date and time should automatically be entered on a maintenance request that is in this lifecycle state.</span></span>
7. <span data-ttu-id="d1608-116">Stel de optie **Werkorder maken** in op **Ja** als een werkorder kan worden gemaakt op basis van een onderhoudsverzoek dat zich in deze levenscyclusstatus bevindt.</span><span class="sxs-lookup"><span data-stu-id="d1608-116">Set the **Create work order** option to **Yes** if a work order can be created from a maintenance request that is in this lifecycle state.</span></span>
8. <span data-ttu-id="d1608-117">Stel de optie **Verwijderen** in op **Ja** als een onderhoudsverzoek kan worden verwijderd terwijl deze zich in deze levenscyclusstatus bevindt.</span><span class="sxs-lookup"><span data-stu-id="d1608-117">Set the **Delete** option to **Yes** if a maintenance request can be deleted while it's in this lifecycle state.</span></span>
9. <span data-ttu-id="d1608-118">Op het sneltabblad **Bijwerken** zijn de opties **Inkomend** en **Uitgaand** in de sectie **Activa** relevant als u depotreparatie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d1608-118">On the **Update** FastTab, the **Inbound** and **Outbound** options in the **Asset** section are relevant if you use depot repair.</span></span> <span data-ttu-id="d1608-119">Stel de optie in op **Ja** als de levenscyclusstatus van de activa in een onderhoudsverzoek automatisch wordt bijgewerkt naar **Inkomend** of **Uitgaand** wanneer de status van de levenscyclus van onderhoudsaanvraag is ingesteld op **Inkomend** of **Uitgaand**.</span><span class="sxs-lookup"><span data-stu-id="d1608-119">Set the appropriate option to **Yes** if the asset lifecycle state of assets that are selected on a maintenance request should automatically be updated to **Inbound** or **Outbound** when the maintenance request lifecycle state of that maintenance request is set to **Inbound** or **Outbound**.</span></span>

<span data-ttu-id="d1608-120">In de volgende afbeelding ziet u een voorbeeld van de pagina **Levenscyclusstatussen van onderhoudsverzoeken**.</span><span class="sxs-lookup"><span data-stu-id="d1608-120">The follow illustration shows an example of the **Maintenance request lifecycle states** page.</span></span>

![Pagina Statussen van levenscyclus voor onderhoudsverzoeken](media/02-setup-for-requests.png)

> [!NOTE]
> <span data-ttu-id="d1608-122">Levenscyclusstatussen, levenscyclusstatusgroepen en -typen van onderhoudsverzoeken zijn gerelateerd aan en worden op dezelfde manier gebruikt als levenscyclusstatussen, levenscyclusstatusgroepen en -typen van werkorders.</span><span class="sxs-lookup"><span data-stu-id="d1608-122">Maintenance request lifecycle states, lifecycle state groups, and types are related to, and used in the same way as, work order lifecycle states, lifecycle state groups, and types.</span></span> 

## <a name="set-up-maintenance-request-lifecycle-models"></a><span data-ttu-id="d1608-123">Levenscyclusmodellen van onderhoudsverzoeken instellen</span><span class="sxs-lookup"><span data-stu-id="d1608-123">Set up maintenance request lifecycle models</span></span>

<span data-ttu-id="d1608-124">Nadat u de levenscyclusstatussen hebt gemaakt die vereist zijn voor uw onderhoudsverzoeken, kunnen deze worden onderverdeeld in levenscyclusstatusgroepen of levenscyclusmodellen.</span><span class="sxs-lookup"><span data-stu-id="d1608-124">After you've created the lifecycle states that are required for your maintenance requests, they can be divided into lifecycle state groups, or lifecycle models.</span></span> <span data-ttu-id="d1608-125">Levenscyclusmodellen van onderhoudsverzoeken worden gebruikt voor het maken van de stroom die kan worden gebruikt voor verschillende typen onderhoudsverzoeken.</span><span class="sxs-lookup"><span data-stu-id="d1608-125">Maintenance request lifecycle models are used to create the flow that can be used for different types of maintenance requests.</span></span> <span data-ttu-id="d1608-126">Er moet minimaal één standaardlevenscyclusmodel voor onderhoudsverzoeken worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d1608-126">At a minimum, one standard maintenance request lifecycle model should be created.</span></span>

1. <span data-ttu-id="d1608-127">Selecteer **Activabeheer** \> **Instellen** \> **Onderhoudsverzoeken** \> **Levenscyclusmodellen**.</span><span class="sxs-lookup"><span data-stu-id="d1608-127">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle models**.</span></span>
2. <span data-ttu-id="d1608-128">Selecteer **Nieuw** om een levenscyclusmodel voor onderhoudsverzoeken te maken.</span><span class="sxs-lookup"><span data-stu-id="d1608-128">Select **New** to create a maintenance request lifecycle model.</span></span>
3. <span data-ttu-id="d1608-129">Voer in het veld **Levenscyclusmodel** de id van het levenscyclusmodel in.</span><span class="sxs-lookup"><span data-stu-id="d1608-129">In the **Lifecycle model** field, enter an ID for the lifecycle model.</span></span>
4. <span data-ttu-id="d1608-130">Voer in het veld **Naam** een naam in.</span><span class="sxs-lookup"><span data-stu-id="d1608-130">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="d1608-131">Het veld **Levenscyclusstatussen** op het sneltabblad **Details** bevat het aantal levencyclusstatussen die in dit levenscyclusmodel zijn geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="d1608-131">On the **Details** FastTab, the **Lifecycle states** shows the number of lifecycle states that are selected in this lifecycle model.</span></span> <span data-ttu-id="d1608-132">Het veld **Typen onderhoudsverzoeken** bevat het aantal typen onderhoudsverzoeken dat gebruikmaakt van dit levenscyclusmodel.</span><span class="sxs-lookup"><span data-stu-id="d1608-132">The **Maintenance request types** field shows the number of maintenance request types that use this lifecycle model.</span></span>

5. <span data-ttu-id="d1608-133">Ga naar het sneltabblad **Levenscyclusstatussen** en selecteer de levencyclusstatussen die moet worden opgenomen in het levenscyclusmodel:</span><span class="sxs-lookup"><span data-stu-id="d1608-133">On the **Lifecycle states** FastTab, select the lifecycle states that should be included in the lifecycle model:</span></span>

    - <span data-ttu-id="d1608-134">Als u een levenscyclusstatus wilt opnemen in het levenscyclusmodel, selecteert u deze in de sectie **Resterende levenscyclusstatussen** en selecteert u vervolgens de knop Pijl-rechts ![Pijl-rechts](media/03-setup-for-requests.png) om deze te verplaatsen naar de sectie **Geselecteerde levenscyclusstatussen**.</span><span class="sxs-lookup"><span data-stu-id="d1608-134">To include a lifecycle state in the lifecycle model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/03-setup-for-requests.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="d1608-135">Als u alle beschikbare levenscyclusstatussen in het levenscyclusmodel wilt opnemen, selecteert u de knop **Alle beschikbare statussen selecteren** ![Alle beschikbare statussen selecteren](media/04-setup-for-requests.png).</span><span class="sxs-lookup"><span data-stu-id="d1608-135">To include all the available lifecycle states in the lifecycle model, select the **Select all available states** button ![Select all available states](media/04-setup-for-requests.png).</span></span> <span data-ttu-id="d1608-136">Alle levenscyclusstatussen worden verplaatst naar de sectie **Geselecteerde levenscyclusstatussen**.</span><span class="sxs-lookup"><span data-stu-id="d1608-136">All lifecycle states are moved to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="d1608-137">Als u een levenscyclusstatus uit het levenscyclusmodel wilt verwijderen, selecteert u deze in de sectie **Geselecteerde levenscyclusstatussen** en selecteert u vervolgens de knop Pijl-links ![Pijl-links](media/05-setup-for-requests.png) om deze te verplaatsen naar de sectie **Resterende levenscyclusstatussen**.</span><span class="sxs-lookup"><span data-stu-id="d1608-137">To remove a lifecycle state from the lifecycle model, select it in the **Lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/05-setup-for-requests.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="d1608-138">Op het sneltabblad **Algemeen** zijn de velden in de sectie **Updates** relevant als u depotreparatie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d1608-138">On the **General** FastTab, the fields in the **Updates** section are relevant if you use depot repair.</span></span>

    - <span data-ttu-id="d1608-139">Selecteer in het veld **Levenscyclusstatus voor ontvangen activum** de levenscyclusstatus waarnaar activa die zijn geselecteerd op een onderhoudsverzoek automatisch moeten worden bijgewerkt wanneer ze worden ontvangen voor depotreparatie.</span><span class="sxs-lookup"><span data-stu-id="d1608-139">In the **Lifecycle state for asset received** field, select the asset lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are received for depot repair.</span></span>
    - <span data-ttu-id="d1608-140">Selecteer in het veld **Levenscyclusstatus voor geleverd activum** de levenscyclusstatus waarnaar activa die zijn geselecteerd op een onderhoudsverzoek automatisch moeten worden bijgewerkt wanneer ze worden geretourneerd na reparatie.</span><span class="sxs-lookup"><span data-stu-id="d1608-140">In the **Lifecycle state for asset delivered** field, select the lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are returned after repair.</span></span>

<span data-ttu-id="d1608-141">In de volgende afbeelding ziet u een voorbeeld van de pagina **Levenscyclusmodellen van onderhoudsverzoeken**.</span><span class="sxs-lookup"><span data-stu-id="d1608-141">The following illustration shows an example of the **Maintenance request lifecycle models** page.</span></span>

![Pagina Levenscyclusmodellen van onderhoudsverzoeken](media/06-setup-for-requests.png)
