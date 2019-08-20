---
title: Leverancierswerkstroom
description: Wijzig leveranciergegevens en gebruik de werkstroom om deze goed te keuren.
author: mikefalkner
manager: annbe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Vendor
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 112f9d6adeee583a63da8ab700d7adc179de2c1d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835305"
---
# <a name="vendor-workflow"></a><span data-ttu-id="eed89-103">Leverancierswerkstroom</span><span class="sxs-lookup"><span data-stu-id="eed89-103">Vendor workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eed89-104">Wanneer de leverancierswerkstroom wordt gebruikt, worden wijzigingen die zijn aangebracht in specifieke velden verzonden naar de werkstroom voordat ze worden toegevoegd aan de leverancier.</span><span class="sxs-lookup"><span data-stu-id="eed89-104">When the vendor workflow is used, changes that are made to specific fields are sent to the workflow for approval before they are added to the vendor.</span></span>

## <a name="set-up-the-vendor-workflow"></a><span data-ttu-id="eed89-105">De leverancierswerkstroom instellen</span><span class="sxs-lookup"><span data-stu-id="eed89-105">Set up the vendor workflow</span></span>

<span data-ttu-id="eed89-106">Voordat u de werkstroomfunctie kunt gebruiken, moet u deze inschakelen.</span><span class="sxs-lookup"><span data-stu-id="eed89-106">Before you can use the workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="eed89-107">Ga naar **Leveranciers \> Instellen \> Parameters van Leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="eed89-107">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
2. <span data-ttu-id="eed89-108">Stel op het tabblad **Algemeen** op het sneltabblad **Goedkeuring van leverancier** de optie **Goedkeuringen van leveranciers inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="eed89-108">On the **General** tab, on the **Vendor approval** FastTab, set the **Enable vendor approvals** option to **Yes**.</span></span>
3. <span data-ttu-id="eed89-109">Geef in het veld **Gedrag van gegevensentiteit** aan hoe gegevens moeten worden geïmporteerd:</span><span class="sxs-lookup"><span data-stu-id="eed89-109">In the **Data entity behavior** field, select the behavior that should be used when data is imported:</span></span>

    - <span data-ttu-id="eed89-110">**Wijzigingen zonder goedkeuring toestaan**: de gegevensentiteit kan de leveranciersrecord bijwerken zonder deze via de werkstroom te verwerken.</span><span class="sxs-lookup"><span data-stu-id="eed89-110">**Allow changes without approval** – The data entity can update the vendor record without processing it through the workflow.</span></span>
    - <span data-ttu-id="eed89-111">**Wijzigingen afwijzen**: de leveranciersrecord kan niet worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="eed89-111">**Reject changes** – Changes can't be made to the vendor record.</span></span> <span data-ttu-id="eed89-112">Het importeren mislukt voor de velden die zijn ingeschakeld voor de werkstroom.</span><span class="sxs-lookup"><span data-stu-id="eed89-112">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="eed89-113">**Wijzigingsvoorstellen maken**: alle velden worden gewijzigd behalve de velden die zijn ingeschakeld voor de werkstroom.</span><span class="sxs-lookup"><span data-stu-id="eed89-113">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="eed89-114">De nieuwe waarden voor deze velden worden toegevoegd aan de leverancier als voorgestelde wijzigingen en de werkstroom wordt automatisch gestart.</span><span class="sxs-lookup"><span data-stu-id="eed89-114">The new values for those fields will be added to the vendor as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="eed89-115">Schakel vervolgens in de lijst met leveranciersvelden het selectievakje **Inschakelen** in voor elk veld dat moet worden goedgekeurd voordat de wijzigingen kunnen worden aangebracht.</span><span class="sxs-lookup"><span data-stu-id="eed89-115">In the list of vendor fields, select the **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="eed89-116">Ga naar **Leveranciers \> Instellen \> Leverancierswerkstromen**.</span><span class="sxs-lookup"><span data-stu-id="eed89-116">Go to **Accounts payable \> Setup \> Accounts payable workflows**.</span></span>
6. <span data-ttu-id="eed89-117">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="eed89-117">Select **New**.</span></span>
7. <span data-ttu-id="eed89-118">Selecteer **Werkstroom van voorgestelde leverancierswijzigingen**.</span><span class="sxs-lookup"><span data-stu-id="eed89-118">Select **Proposed vendor changes workflow**.</span></span> 
8. <span data-ttu-id="eed89-119">Stel de werkstroom in zodat deze overeenkomt met uw goedkeuringsproces.</span><span class="sxs-lookup"><span data-stu-id="eed89-119">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="eed89-120">Door het goedkeuringselement **Werkstroomgoedkeuring voor voorgestelde leverancierswijziging** van de werkstroom worden de wijzigingen toegepast op de leverancier.</span><span class="sxs-lookup"><span data-stu-id="eed89-120">The **Workflow approval for proposed vendor change** workflow approval element will apply the changes to the vendor.</span></span>

## <a name="change-vendor-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="eed89-121">Leveranciersgegevens wijzigen en de wijzigingen in de werkstroom indienen</span><span class="sxs-lookup"><span data-stu-id="eed89-121">Change vendor information and submit the changes to the workflow</span></span>

<span data-ttu-id="eed89-122">Wanneer u een veld wijzigt dat is ingeschakeld voor de werkstroom, wordt de pagina **Voorgestelde wijzigingen** weergegeven.</span><span class="sxs-lookup"><span data-stu-id="eed89-122">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="eed89-123">Deze pagina geeft de oorspronkelijke waarde weer van het veld en de nieuwe waarde die u hebt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="eed89-123">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="eed89-124">Het veld dat u hebt gewijzigd, wordt teruggezet op de oorspronkelijke waarde.</span><span class="sxs-lookup"><span data-stu-id="eed89-124">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="eed89-125">Ook een statusbericht op de pagina meldt dat uw wijzigingen niet zijn ingediend.</span><span class="sxs-lookup"><span data-stu-id="eed89-125">A status message also informs you that your changes haven't been submitted.</span></span> 

<span data-ttu-id="eed89-126">Elke keer dat u een veld wijzigt dat is ingeschakeld voor de werkstroom, wordt dat veld toegevoegd aan de lijst op de pagina **Voorgestelde wijzigingen**.</span><span class="sxs-lookup"><span data-stu-id="eed89-126">Every time that you change a field that is enabled for the workflow, that field is added to the list on the **Proposed changes** page.</span></span> <span data-ttu-id="eed89-127">Als u de voorgestelde waarde voor een veld wilt verwijderen, gebruikt u de knop **Verwijderen** naast het veld in de lijst.</span><span class="sxs-lookup"><span data-stu-id="eed89-127">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="eed89-128">Als u alle wijzigingen wilt verwijderen, gebruikt u de knop **Alle wijzigingen verwijderen** onder aan de pagina.</span><span class="sxs-lookup"><span data-stu-id="eed89-128">To discard all changes, use the **Discard all changes** button at the bottom of the page.</span></span> <span data-ttu-id="eed89-129">Selecteer **OK** om de pagina te sluiten.</span><span class="sxs-lookup"><span data-stu-id="eed89-129">Select **OK** to close the page.</span></span>

<span data-ttu-id="eed89-130">Als u ten minste één voorgestelde wijziging hebt, worden twee extra tabbladen weergegeven in het Actievenster: **Voorgestelde wijzigingen** en **Werkstroom**.</span><span class="sxs-lookup"><span data-stu-id="eed89-130">After you have at least one proposed change, two additional tabs appear on the action pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="eed89-131">Selecteer **Voorgestelde wijzigingen** om de pagina **Voorgestelde wijzigingen** te openen en uw wijzigingen te bekijken.</span><span class="sxs-lookup"><span data-stu-id="eed89-131">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="eed89-132">Selecteer **Werkstroom \> Indienen** om de wijzigingen in te dienen bij de werkstroom.</span><span class="sxs-lookup"><span data-stu-id="eed89-132">Select **Workflow \> Submit to submit the changes to workflow**.</span></span>

    <span data-ttu-id="eed89-133">De status op de pagina wordt gewijzigd in **Wijzigingen in afwachting van goedkeuring**.</span><span class="sxs-lookup"><span data-stu-id="eed89-133">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="eed89-134">De werkstroom volgt het standaard werkstroomproces in Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="eed89-134">The workflow follows the standard workflow process in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="eed89-135">De fiatteur wordt doorgestuurd naar de pagina **Leverancier**, waar hij/zij de wijzigingen op de pagina **Voorgestelde wijzigingen** kan bekijken en **Werkstroom \> Goedkeuren** om de werkstroom goed te keuren.</span><span class="sxs-lookup"><span data-stu-id="eed89-135">The approver is directed to the **Vendor** page, where he or she can review the changes on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="eed89-136">Nadat alle goedkeuringen zijn voltooid, worden de velden bijgewerkt met de voorgestelde waarden.</span><span class="sxs-lookup"><span data-stu-id="eed89-136">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>
