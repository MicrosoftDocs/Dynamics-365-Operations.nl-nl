---
title: Bewerken van persoonlijke gegevens beperken
description: Voorkomen dat werknemers contactgegevens bewerken in Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6e43b9127b247fa618558b725837d12bf290662f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052020"
---
# <a name="restrict-editing-of-personal-information"></a><span data-ttu-id="19d44-103">Bewerken van persoonlijke gegevens beperken</span><span class="sxs-lookup"><span data-stu-id="19d44-103">Restrict editing of personal information</span></span>

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

<span data-ttu-id="19d44-104">In dit onderwerp wordt beschreven hoe u voorkomt dat werknemers contactgegevens bewerken in Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="19d44-104">This topic describes how to restrict employees from editing contact details in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="19d44-105">U wilt mogelijk voorkomen dat werknemers bepaalde contactgegevens bewerken, zoals de locatie van hun bedrijf of e-mailadres.</span><span class="sxs-lookup"><span data-stu-id="19d44-105">You might want to prevent employees from editing certain contact details, such as their business location or email address.</span></span>

> [!NOTE]
> <span data-ttu-id="19d44-106">Als u deze functie wilt gebruiken, moet u eerst **(Preview) Voorkomen dat werknemers adres- en contactgegevens toevoegen of bewerken voor bepaalde doeleinden** in Functiebeheer.</span><span class="sxs-lookup"><span data-stu-id="19d44-106">To use this feature, you must first enable **(Preview) Restrict employees from adding or editing address and contact information for select purposes** in Feature management.</span></span> <span data-ttu-id="19d44-107">Meer informatie over het inschakelen van de previewfuncties vindt u in [Functies beheren](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="19d44-107">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span><br><br><span data-ttu-id="19d44-108">![Voorbeeldfunctie inschakelen](./media/hr-employee-self-service-restrict-enable.png)</span><span class="sxs-lookup"><span data-stu-id="19d44-108">![Enable preview feature](./media/hr-employee-self-service-restrict-enable.png)</span></span>

## <a name="choose-the-information-an-employee-can-add-or-edit"></a><span data-ttu-id="19d44-109">De informatie kiezen die een werknemer kan toevoegen of bewerken</span><span class="sxs-lookup"><span data-stu-id="19d44-109">Choose the information an employee can add or edit</span></span>

1. <span data-ttu-id="19d44-110">Selecteer **Personeelsbeheer** in Human Resources, en vervolgens **Koppelingen** en **Parameters Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="19d44-110">In Human Resources, select **Personnel management**, select **Links**, and then select **Human resources parameters**.</span></span>

   ![Ga naar Human Resources-parameters](./media/hr-employee-self-service-human-resources-parameters.png)

2. <span data-ttu-id="19d44-112">Selecteer op de pagina **Parameters voor Human Resources** het tabblad **Selfservice werknemers**.</span><span class="sxs-lookup"><span data-stu-id="19d44-112">On the **Human resources parameters** page, select the **Employee self service** tab.</span></span>

   ![Selfservice voor werknemers selecteren](./media/hr-employee-self-service-tab.png)

3. <span data-ttu-id="19d44-114">Schakel op het tabblad **Selfservice voor werknemers** alle informatie in de sectie **Adres- en contactgegevens** uit die u niet door werknemers wilt laten toevoegen of bewerken.</span><span class="sxs-lookup"><span data-stu-id="19d44-114">On the **Employee self service** tab, uncheck all information in the **Address and contact information** section that you don't want employees to add or edit.</span></span> <span data-ttu-id="19d44-115">In dit voorbeeld hebben we de **zakelijke** contactgegevens uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="19d44-115">In this example, we've unchecked **Business** contact information.</span></span>

   ![Bewerken van zakelijke contactgegevens beperken](./media/hr-employee-self-service-restrict-business.png)

4. <span data-ttu-id="19d44-117">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="19d44-117">Select **Save**.</span></span>

   ![Wijzigingen opslaan](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a><span data-ttu-id="19d44-119">Werknemerservaring</span><span class="sxs-lookup"><span data-stu-id="19d44-119">Employee experience</span></span>

<span data-ttu-id="19d44-120">Wanneer u hebt ingesteld dat werknemers beperkt contactgegevens kunnen toevoegen of bewerken, kunnen ze de informatie wel bekijken, maar ze kunnen deze niet wijzigen.</span><span class="sxs-lookup"><span data-stu-id="19d44-120">After you've restricted employees from adding or editing contact details, they can see the information, but can't change it.</span></span>

<span data-ttu-id="19d44-121">Hoewel werknemers in dit voorbeeld geen **zakelijke** contactgegevens mogen bewerken, kunnen ze de informatie nog wel zien in de Selfservice voor werknemers:</span><span class="sxs-lookup"><span data-stu-id="19d44-121">In this example, where employees are restricted from editing **Business** contact details, they can still see the information in Employee self service:</span></span>

![Zakelijke contactgegevens weergeven](./media/hr-employee-self-service-restrict-view.png)

<span data-ttu-id="19d44-123">Wanneer ze de zakelijke contactgegevens selecteren, wordt het deelvenster **Adres bewerken** echter weergegeven als alleen-lezen en kunnen ze de velden niet wijzigen.</span><span class="sxs-lookup"><span data-stu-id="19d44-123">However, when they select the business contact details, the **Edit address** pane appears as read-only, and they can't change any of the fields.</span></span>

![Zakelijke contactgegevens worden weergegeven als alleen-lezen](./media/hr-employee-self-service-restrict-read-only.png)

<span data-ttu-id="19d44-125">En als zijn **Toevoegen** selecteren om een nieuw adres toe te voegen, kunnen zij in het vervolgkeuzevak **Doel** de optie **Zakelijk** niet selecteren.</span><span class="sxs-lookup"><span data-stu-id="19d44-125">In addition, if they select **Add** to add a new address, they can't select **Business** from the **Purpose** dropdown box.</span></span>

![Werknemer kan geen zakelijk toevoegen](./media/hr-employee-self-service-restrict-add.png)

<span data-ttu-id="19d44-127">Werknemers krijgen dezelfde ervaring wanneer ze **Contactgegevens** selecteren op de pagina **Persoonlijke informatie** en een nieuw adres toevoegen.</span><span class="sxs-lookup"><span data-stu-id="19d44-127">Employees get the same experience when they select **Contact details** on the **Personal information** page and add a new address.</span></span> <span data-ttu-id="19d44-128">In het vervolgkeuzevak **Doel** worden alleen de typen gegevens weergegeven die ze kunnen toevoegen.</span><span class="sxs-lookup"><span data-stu-id="19d44-128">The **Purpose** dropdown box only displays the types of information they can add.</span></span> 

![Werknemer kan Zakelijk niet selecteren in de vervolgkeuzelijst Doel](./media/hr-employee-self-service-restrict-purpose.png)

<span data-ttu-id="19d44-130">**Contactgegevens** toont nu **Doel** in het raster.</span><span class="sxs-lookup"><span data-stu-id="19d44-130">**Contact details** now shows **Purpose** in the grid.</span></span>

![Doel wordt weergegeven in raster Contactgegevens](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a><span data-ttu-id="19d44-132">Zie ook</span><span class="sxs-lookup"><span data-stu-id="19d44-132">See also</span></span>

[<span data-ttu-id="19d44-133">Overzicht van Selfservice werknemer en Selfservice manager</span><span class="sxs-lookup"><span data-stu-id="19d44-133">Employee and Manager self service overview</span></span>](hr-employee-manager-self-service-overview.md)<br>
[<span data-ttu-id="19d44-134">Human Resources-parameters configureren</span><span class="sxs-lookup"><span data-stu-id="19d44-134">Configure Human resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="19d44-135">Persoonlijke gegevens bewerken</span><span class="sxs-lookup"><span data-stu-id="19d44-135">Edit personal information</span></span>](hr-employee-manager-self-service-edit-personal-information.md)