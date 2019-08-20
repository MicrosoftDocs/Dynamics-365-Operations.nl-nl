---
title: Levenscyclusstatussen van activa
description: In dit onderwerp worden levenscyclusstatussen van activa en levenscyclusmodellen in Activabeheer uitgelegd.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2dc72c61ed4dbb04122c6859123307dc79f2b233
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783171"
---
# <a name="asset-lifecycle-states"></a><span data-ttu-id="709ce-103">Levenscyclusstatussen van activa</span><span class="sxs-lookup"><span data-stu-id="709ce-103">Asset lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="709ce-104">In dit onderwerp worden levenscyclusstatussen van activa en levenscyclusmodellen in Activabeheer uitgelegd.</span><span class="sxs-lookup"><span data-stu-id="709ce-104">This topic explains asset lifecycle states and lifecycle models in Asset Management.</span></span> <span data-ttu-id="709ce-105">Levenscyclusstatussen van activa worden gebruikt om te definiëren of een activum actief of inactief is.</span><span class="sxs-lookup"><span data-stu-id="709ce-105">Asset lifecycle states are used to define whether an asset is active or inactive.</span></span> <span data-ttu-id="709ce-106">U kunt bijvoorbeeld de levenscyclusstatussen van activa instellen op **Gemaakt**, **Actief** en **Beëindigd**.</span><span class="sxs-lookup"><span data-stu-id="709ce-106">For example, you can set up asset lifecycle states such as **Created**, **Active**, and **Terminated**.</span></span>

> [!NOTE]
> - <span data-ttu-id="709ce-107">Aanvragen voor levenscyclusstatussen zijn gekoppeld aan levenscyclusstatussen van activa.</span><span class="sxs-lookup"><span data-stu-id="709ce-107">Request lifecycle states are linked to asset lifecycle states.</span></span> <span data-ttu-id="709ce-108">Daarom krijgt, wanneer een aanvraag wordt gewijzigd in een nieuwe aanvraag voor levenscyclusstatus, het activum dat is gekoppeld aan de aanvraag een nieuwe van de levenscyclusstatus van activa.</span><span class="sxs-lookup"><span data-stu-id="709ce-108">Therefore, when a request is changed to a new request lifecycle state, the asset that is attached to the request is changed to a new asset lifecycle state.</span></span> <span data-ttu-id="709ce-109">Als bijvoorbeeld de levenscyclusstatus van een aanvraag wordt gewijzigd in **Inkomend**, wordt de levenscyclusstatus van het gekoppelde activum gewijzigd in de levenscyclusstatus die is geselecteerd in het veld **Inkomende levenscyclusstatus** op het sneltabblad **Levenscyclusstatus van activa** van de pagina **Modellen voor levenscyclusstatussen van activa**.</span><span class="sxs-lookup"><span data-stu-id="709ce-109">For example, if the lifecycle state of a request is changed to **Inbound**, the lifecycle state of the attached asset is changed to the lifecycle state that is selected in the **Inbound lifecycle state** field on the **Asset lifecycle state** FastTab of the **Asset lifecycle state models** page.</span></span> 


<span data-ttu-id="709ce-110">Levenscyclusstatussen van activa kunnen worden ingesteld in levenscyclusmodellen van activa, waar u de vereiste levenscyclusstatussen voor verschillende typen activa kunt definiëren.</span><span class="sxs-lookup"><span data-stu-id="709ce-110">Asset lifecycle states can be set up in asset lifecycle models, where you can define the required lifecycle states for various types of assets.</span></span> <span data-ttu-id="709ce-111">U stelt eerst levenscyclusstatussen in.</span><span class="sxs-lookup"><span data-stu-id="709ce-111">You first set up lifecycle states.</span></span> <span data-ttu-id="709ce-112">Vervolgens maakt u een levenscyclusmodel en selecteert u levenscyclusstatussen hiervoor.</span><span class="sxs-lookup"><span data-stu-id="709ce-112">You then create a lifecycle model and select lifecycle states for it.</span></span>

1. <span data-ttu-id="709ce-113">Selecteer **Activabeheer** \> **Instellingen** \> **Activa** \> **Levenscyclusstatussen**.</span><span class="sxs-lookup"><span data-stu-id="709ce-113">Select **Asset management** \> **Setup** \> **Assets** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="709ce-114">Selecteer **Nieuw** om een nieuwe levenscyclusstatus van activa te maken.</span><span class="sxs-lookup"><span data-stu-id="709ce-114">Select **New** to create a new asset lifecycle state.</span></span>
3. <span data-ttu-id="709ce-115">Voer in het veld **Levenscyclusstatus** de id van de levenscyclusstatus in.</span><span class="sxs-lookup"><span data-stu-id="709ce-115">In the **Lifecycle state** field, enter the lifecycle state ID.</span></span>
4. <span data-ttu-id="709ce-116">Voer in het veld **Naam** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="709ce-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="709ce-117">Het veld **Levenscyclusmodellen** bevat het aantal levencyclusmodellen van activa dat gebruikmaakt van de levenscyclusstatus van activa.</span><span class="sxs-lookup"><span data-stu-id="709ce-117">The **Lifecycle models** field shows the number of asset lifecycle models that use the asset lifecycle state.</span></span>

5. <span data-ttu-id="709ce-118">Stel de optie **Actief** in op **Ja** als deze levenscyclusstatus een actieve levenscyclusstatus moet zijn (met andere woorden, als werkorders kunnen worden gemaakt voor activa die zich in deze levenscyclusstatus bevinden).</span><span class="sxs-lookup"><span data-stu-id="709ce-118">Set the **Active** option to **Yes** if this lifecycle state should be an active lifecycle state (in other words, if work orders can be created for assets that are in this lifecycle state).</span></span>
6. <span data-ttu-id="709ce-119">Stel de optie **Openstaande kalenderregels verwijderen** in op **Ja** als openstaande activakalenderregels die de levenscyclusstatus **Gemaakt** van activa hebben, moeten worden verwijderd wanneer ze zich in deze levenscyclusstatus bevinden.</span><span class="sxs-lookup"><span data-stu-id="709ce-119">Set the **Delete open calendar lines** option to **Yes** if open asset calendar lines that have an asset lifecycle state of **Created** should be deleted when they are in this lifecycle state.</span></span> <span data-ttu-id="709ce-120">Deze instelling is handig als u alle open onderhoudsschema's wilt opschonen die niet langer relevant zijn voor het activum (bijvoorbeeld als het activum niet meer actief is).</span><span class="sxs-lookup"><span data-stu-id="709ce-120">This setting is useful if you want to clean up any open maintenance schedules that are no longer relevant for the asset (for example, if the asset is no longer active).</span></span>

> [!NOTE]
> <span data-ttu-id="709ce-121">Levencyclusstatussen van activa, levenscyclusmodellen van activa en activatypen zijn gerelateerd.</span><span class="sxs-lookup"><span data-stu-id="709ce-121">Asset lifecycle states, asset lifecycle models, and asset types are related.</span></span> <span data-ttu-id="709ce-122">Ze worden op dezelfde manier gebruikt als levenscyclusstatussen van werkorders, levenscyclusmodellen van werkorders en typen werkorders.</span><span class="sxs-lookup"><span data-stu-id="709ce-122">They are used in the same way as work order lifecycle states, work order lifecycle models, and work order types.</span></span> 


<span data-ttu-id="709ce-123">Nadat u de vereiste levenscyclusstatussen van activa hebt gemaakt, kunt u levenscyclusstatussen instellen in levenscyclusmodellen van activa.</span><span class="sxs-lookup"><span data-stu-id="709ce-123">After you've created the required asset lifecycle states, you can set up lifecycle states in asset lifecycle models.</span></span>

1. <span data-ttu-id="709ce-124">Selecteer **Activabeheer** \> **Instellingen** \> **Activa** \> **Levenscyclusmodellen**.</span><span class="sxs-lookup"><span data-stu-id="709ce-124">Select **Asset management** \> **Setup** \> **assets** \> **lifecycle models**.</span></span>
2. <span data-ttu-id="709ce-125">Selecteer **Nieuw** om een nieuw levenscyclusmodel van activa te maken.</span><span class="sxs-lookup"><span data-stu-id="709ce-125">Select **New** to create a new asset lifecycle model.</span></span>
3. <span data-ttu-id="709ce-126">Voer in het veld **Levenscyclusmodel** de id van het levenscyclusmodel in.</span><span class="sxs-lookup"><span data-stu-id="709ce-126">In the **Lifecycle model** field, enter the lifecycle model ID.</span></span>
4. <span data-ttu-id="709ce-127">Voer in het veld **Naam** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="709ce-127">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="709ce-128">Het veld **Levenscyclusstatussen** bevat het aantal levencyclusstatussen activa die zijn geselecteerd in het levenscyclusmodel van activa.</span><span class="sxs-lookup"><span data-stu-id="709ce-128">The **Lifecycle states** field shows the number of asset lifecycle states that are selected in the asset lifecycle model.</span></span> <span data-ttu-id="709ce-129">Het veld **Activatypen** bevat het aantal activatypen dat gebruikmaakt van het levenscyclusmodel.</span><span class="sxs-lookup"><span data-stu-id="709ce-129">The **Asset types** field shows the number of asset types that use the lifecycle model.</span></span>

5. <span data-ttu-id="709ce-130">Selecteer op het sneltabblad **Levenscyclusstatussen** het aantal levencyclusstatussen van activa dat moet worden opgenomen in het levenscyclusmodel van activa.</span><span class="sxs-lookup"><span data-stu-id="709ce-130">On the **Lifecycle states** FastTab, select the asset lifecycle states that should be included in the asset lifecycle model:</span></span>

    - <span data-ttu-id="709ce-131">Als u een levenscyclusstatus voor het model wilt gebruiken, selecteert u deze in de sectie **Resterende levenscyclusstatussen** en selecteert u vervolgens de knop Pijl-rechts ![Pijl-rechts](media/15-setup-for-objects.png) om deze te verplaatsen naar de sectie **Geselecteerde levenscyclusstatussen**.</span><span class="sxs-lookup"><span data-stu-id="709ce-131">To use a lifecycle state for the model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/15-setup-for-objects.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="709ce-132">Als u alle beschikbare levenscyclusstatussen voor het model wilt gebruiken, selecteert u de knop **Alle beschikbare levenscyclusstatussen** ![Alle beschikbare levenscyclusstatussen](media/20-setup-for-objects.png).</span><span class="sxs-lookup"><span data-stu-id="709ce-132">To use all the available lifecycle states for the model, select the **All available lifecycle states** button ![All available lifecycle states](media/20-setup-for-objects.png).</span></span> <span data-ttu-id="709ce-133">Alle levenscyclusstatussen worden overgebracht naar de sectie **Geselecteerde levenscyclusstatussen**.</span><span class="sxs-lookup"><span data-stu-id="709ce-133">All lifecycle states are transferred to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="709ce-134">Als u een levenscyclusstatus uit het model wilt verwijderen, selecteert u deze in de sectie **Geselecteerde levenscyclusstatussen** en selecteert u vervolgens de knop Pijl-links ![Pijl-links](media/16-setup-for-objects.png) om deze te verplaatsen naar de sectie **Resterende levenscyclusstatussen**.</span><span class="sxs-lookup"><span data-stu-id="709ce-134">To remove a lifecycle state from the model, select it in the **lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/16-setup-for-objects.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="709ce-135">Selecteer **Updates van levenscyclusstatussen** om de levenscyclusstatussen van activa te definiëren die een geselecteerde levenscyclusstatus kunnen volgen.</span><span class="sxs-lookup"><span data-stu-id="709ce-135">Select **Lifecycle state updates** to define the asset lifecycle states that can follow a selected lifecycle state.</span></span>
7. <span data-ttu-id="709ce-136">U gebruikt het sneltabblad **Activastatus** als u activa verwerkt die u voor reparatie ontvangt.</span><span class="sxs-lookup"><span data-stu-id="709ce-136">You use the **Asset state** FastTab if you handle assets that you receive for repair.</span></span> <span data-ttu-id="709ce-137">In de sectie **Inkomend/uitgaand** kunt u levenscyclusstatussen van activa selecteren om de werkstroom aan te geven van een activum dat u voor reparatie ontvangt.</span><span class="sxs-lookup"><span data-stu-id="709ce-137">In the **Inbound/outbound** section, you can select asset lifecycle states to indicate the workflow of an asset that you receive for repair.</span></span> <span data-ttu-id="709ce-138">Als u leenactiva aanbiedt aan klanten of afdelingen, kunt u in de sectie **Loan** levenscyclusstatussen selecteren voor leenactiva.</span><span class="sxs-lookup"><span data-stu-id="709ce-138">If you offer loan assets to customers or departments, in the **Loan** section, you can select lifecycle states for loan assets.</span></span>
