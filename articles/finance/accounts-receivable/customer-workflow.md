---
title: Klantenworkflow
description: Dit onderwerp bevat informatie over de workflow voor klanten. U kunt specifieke velden voor een klant wijzigen en deze wijzigingen ter goedkeuring via de workflow verzenden voordat ze worden toegevoegd aan de klant.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 8ff91a1df82d6195da266b97c347ef27afec662d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175889"
---
# <a name="customer-workflow"></a><span data-ttu-id="c8bc7-104">Klantenworkflow</span><span class="sxs-lookup"><span data-stu-id="c8bc7-104">Customer workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c8bc7-105">De klantenworkflow is toegevoegd aan versie 8.0.4.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-105">The customer workflow has been added to version 8.0.4.</span></span> <span data-ttu-id="c8bc7-106">U kunt specifieke velden voor een klant wijzigen en deze wijzigingen ter goedkeuring via de workflow verzenden voordat ze worden toegevoegd aan de klant.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-106">You can change specific fields for a customer and then send those changes for approval by using the workflow before they are added to the customer.</span></span>

## <a name="set-up-the-customer-workflow"></a><span data-ttu-id="c8bc7-107">De klantenworkflow instellen</span><span class="sxs-lookup"><span data-stu-id="c8bc7-107">Set up the customer workflow</span></span>

<span data-ttu-id="c8bc7-108">Voordat u de functie voor klantenworkflow kunt gebruiken, moet u deze inschakelen.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-108">Before you can use the customer workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="c8bc7-109">Ga naar **Klanten \> Instellen \> Parameters van module Klanten**.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-109">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="c8bc7-110">Stel op het tabblad **Algemeen**, op de FastTab **Goedkeuring klant** de optie **Goedkeuringen van klanten inschakelen** in op **Ja** om de functie in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-110">On the **General** tab, on the **Customer approval** FastTab, set the **Enable customer approvals** option to **Yes** to enable the feature.</span></span>
3. <span data-ttu-id="c8bc7-111">In het veld **Gedrag van gegevensentiteit** selecteert u de werking die de gegevensentiteiten moeten gebruiken wanneer gegevens worden geïmporteerd:</span><span class="sxs-lookup"><span data-stu-id="c8bc7-111">In the **Data entity behavior** field, select the behavior that the data entities should use when data is imported:</span></span>

    - <span data-ttu-id="c8bc7-112">**Wijzigingen zonder goedkeuring toestaan**: een entiteit kan de klantrecord bijwerken zonder dit via de workflow te verwerken.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-112">**Allow changes without approval** – An entity can update the customer record without processing it through the workflow.</span></span>
    - <span data-ttu-id="c8bc7-113">**Wijzigingen negeren**: de klantrecord kan niet worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-113">**Reject changes** – Changes can't be made to the customer record.</span></span> <span data-ttu-id="c8bc7-114">Het importeren mislukt voor de velden die zijn ingeschakeld voor de workflow.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-114">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="c8bc7-115">**Wijzigingsvoorstellen maken**: alle velden worden gewijzigd behalve de velden die zijn ingeschakeld voor de workflow.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-115">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="c8bc7-116">De nieuwe waarden voor deze velden worden toegevoegd aan de klant als voorgestelde wijzigingen en de workflow wordt automatisch gestart.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-116">The new values for those fields will be added to the customer as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="c8bc7-117">Schakel vervolgens in de lijst met klantvelden het selectievakje **Inschakelen** in voor elk veld dat moet worden goedgekeurd voordat de wijzigingen kunnen worden aangebracht.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-117">In the list of customer fields, select then **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="c8bc7-118">Ga naar **Klanten \> Instellen \> Klantenworkflows**.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-118">Go to **Accounts receivable \> Setup \> Accounts receivable workflows**.</span></span>
6. <span data-ttu-id="c8bc7-119">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-119">Select **New**.</span></span>
7. <span data-ttu-id="c8bc7-120">Selecteer **Voorgestelde workflow voor klantwijziging**.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-120">Select **Proposed customer change workflow**.</span></span> 
8. <span data-ttu-id="c8bc7-121">Stel de workflow in zodat deze overeenkomt met uw goedkeuringsproces.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-121">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="c8bc7-122">Door het goedkeuringselement **Workflowgoedkeuring voor voorgestelde klantwijziging** van de workflow worden de wijzigingen toegepast op de klant.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-122">The **Workflow approval for proposed customer change** workflow approval element will apply the changes to the customer.</span></span>

## <a name="change-customer-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="c8bc7-123">Klantgegevens wijzigen en de wijzigingen in de workflow indienen</span><span class="sxs-lookup"><span data-stu-id="c8bc7-123">Change customer information and submit the changes to the workflow</span></span>

<span data-ttu-id="c8bc7-124">Wanneer u een veld wijzigt dat is ingeschakeld voor de workflow, wordt de pagina **Voorgestelde wijzigingen** weergegeven.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-124">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="c8bc7-125">Deze pagina geeft de oorspronkelijke waarde weer van het veld en de nieuwe waarde die u hebt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-125">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="c8bc7-126">Het veld dat u hebt gewijzigd, wordt teruggezet op de oorspronkelijke waarde.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-126">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="c8bc7-127">Een statusbericht op de pagina meldt dat uw wijzigingen niet zijn ingediend.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-127">A status message on the page informs you that your changes haven't been submitted.</span></span>

<span data-ttu-id="c8bc7-128">Elke keer dat u een veld wijzigt dat is ingeschakeld voor de workflow, wordt dat veld toegevoegd aan de lijst met voorgestelde wijzigingen.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-128">Every time that you change a field that is enabled for the workflow, that field is added to the list of proposed changes.</span></span> <span data-ttu-id="c8bc7-129">Als u de voorgestelde waarde voor een veld wilt verwijderen, gebruikt u de knop **Verwijderen** naast het veld in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-129">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="c8bc7-130">Als u alle wijzigingen wilt verwijderen, gebruikt u de knop **Alle wijzigingen verwijderen** onder aan de pagina.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-130">To discard all changes, use the **Discard all change** button at the bottom of the page.</span></span> <span data-ttu-id="c8bc7-131">Selecteer **OK** om de pagina te sluiten.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-131">Select **OK** to close the page.</span></span>

<span data-ttu-id="c8bc7-132">Als u ten minste één voorgestelde wijziging hebt, worden twee extra menu's weergegeven in het Actievenster: **Voorgestelde wijzigingen** en **Workflow**.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-132">After you have at least one proposed change, two additional menus appear on the Action Pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="c8bc7-133">Selecteer **Voorgestelde wijzigingen** om de pagina **Voorgestelde wijzigingen** te openen en uw wijzigingen te bekijken.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-133">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="c8bc7-134">Selecteer **Workflow \> Indienen** om de wijzigingen in te dienen bij de workflow.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-134">Select **Workflow \> Submit** to submit the changes to the workflow.</span></span>

    <span data-ttu-id="c8bc7-135">De status op de pagina wordt gewijzigd in **Wijzigingen in afwachting van goedkeuring**.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-135">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="c8bc7-136">De workflow volgt het standaard workflowproces in de toepassing.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-136">The workflow follows the standard workflow process in the application.</span></span> <span data-ttu-id="c8bc7-137">De fiatteur wordt doorgestuurd naar de pagina **Klant**, waar de wijzigingen op de pagina **Voorgestelde wijzigingen** kunnen worden bekeken en **Workflow \> Goedkeuren** kan worden geselecteerd om de werkstroom goed te keuren.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-137">The approver is directed to the **Customer** page, where he or she can review the changes on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="c8bc7-138">Nadat alle goedkeuringen zijn voltooid, worden de velden bijgewerkt met de voorgestelde waarden.</span><span class="sxs-lookup"><span data-stu-id="c8bc7-138">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>