---
title: ER-configuraties uitvoeren in RCS en deze uploaden naar de algemene opslagplaats
description: In dit onderwerp wordt uitgelegd hoe u een configuratie voor elektronische rapportage (ER) kunt maken in Microsoft Regulatory Configuration Services (RCS) en deze kunt uploaden naar de algemene opslagplaats.
author: JaneA07
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: a138fd4b525077f12f6575f4b10f682728b71203
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838714"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a><span data-ttu-id="3e001-103">ER-configuraties uitvoeren in Regulatory Configuration Services (RCS) en deze uploaden naar de algemene opslagplaats</span><span class="sxs-lookup"><span data-stu-id="3e001-103">Create ER configurations in Regulatory Configuration Services (RCS) and upload them to the Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3e001-104">U kunt Microsoft Regulatory Configuration Services (RCS) gebruiken om configuraties voor elektronische rapportage (ER) te ontwerpen en deze zo te publiceren dat ze in uw organisatie kunnen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="3e001-104">You can use Microsoft Regulatory Configuration Services (RCS) to design Electronic reporting (ER) configurations and publish them so that they can be used in your organization.</span></span>

<span data-ttu-id="3e001-105">In de volgende procedures wordt uitgelegd hoe een gebruiker in de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een afgeleide versie van een ER-configuratie kan maken die is geconfigureerd in een RCS-exemplaar en vervolgens de afgeleide configuratie uploaden naar de algemene opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="3e001-105">The following procedures explain how a user in the System Administrator or Electronic Reporting Developer role can create a derived version of an ER configuration that has been configured in an RCS instance, and then upload the derived configuration to the Global repository.</span></span> 

<span data-ttu-id="3e001-106">Voordat u deze procedures kunt uitvoeren, moet u eerst aan de volgende vereisten voldoen:</span><span class="sxs-lookup"><span data-stu-id="3e001-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="3e001-107">Open een RCS-exemplaar.</span><span class="sxs-lookup"><span data-stu-id="3e001-107">Access an RCS instance.</span></span>
- <span data-ttu-id="3e001-108">Maak een actieve configuratieprovider.</span><span class="sxs-lookup"><span data-stu-id="3e001-108">Create an active configuration provider.</span></span> <span data-ttu-id="3e001-109">Zie [Configuratieproviders maken en deze als actief markeren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="3e001-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="3e001-110">U moet er ook voor zorgen dat een RCS-omgeving wordt ingericht voor uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="3e001-110">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="3e001-111">Ga in een Finance and Operations-app naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="3e001-111">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="3e001-112">Als er geen RCS-omgeving is ingericht voor uw bedrijf, selecteert u **Regulatory services ‑ Configuratie extern** en volgt u vervolgens de instructies om een RCS-omgeving in te richten.</span><span class="sxs-lookup"><span data-stu-id="3e001-112">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="3e001-113">Als er al een RCS-omgeving is ingericht voor uw bedrijf, gebruikt u de pagina-URL om deze te openen door de aanmeldingsoptie te selecteren.</span><span class="sxs-lookup"><span data-stu-id="3e001-113">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a><span data-ttu-id="3e001-114">Een afgeleide versie van een configuratie maken in RCS</span><span class="sxs-lookup"><span data-stu-id="3e001-114">Create a derived version of a configuration in RCS</span></span>

1. <span data-ttu-id="3e001-115">Controleer in het werkgebied **Elektronische rapportage** of u een actieve configuratieprovider hebt voor uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="3e001-115">In the **Electronic reporting** workspace, verify that you have an active configuration provider for your organization.</span></span> 
2. <span data-ttu-id="3e001-116">Selecteer **Rapportageconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="3e001-116">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="3e001-117">Selecteer de configuratie waarvan u een nieuwe versie wilt afleiden.</span><span class="sxs-lookup"><span data-stu-id="3e001-117">Select the configuration that you want to derive a new version from.</span></span> <span data-ttu-id="3e001-118">U kunt het filterveld boven de structuur gebruiken om de zoekopdracht te verfijnen.</span><span class="sxs-lookup"><span data-stu-id="3e001-118">You can use the filter field above the tree to narrow your search.</span></span>
4. <span data-ttu-id="3e001-119">Selecteer **Configuratie make** \> **Afleiden van naam**.</span><span class="sxs-lookup"><span data-stu-id="3e001-119">Select **Create configuration** \> **Derive from Name**.</span></span>
5. <span data-ttu-id="3e001-120">Voer een naam en omschrijving in en selecteer vervolgens **Configuratie maken** om een nieuwe afgeleide versie te maken.</span><span class="sxs-lookup"><span data-stu-id="3e001-120">Enter a name and description, and then select **Create configuration** to create a new derived version.</span></span>
6. <span data-ttu-id="3e001-121">Selecteer de nieuw afgeleide configuratie, voeg een beschrijving van de versie toe en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="3e001-121">Select the newly derived configuration, add a description of the version, and then select **OK**.</span></span> <span data-ttu-id="3e001-122">De status van de configuratie wordt gewijzigd in **Voltooid**.</span><span class="sxs-lookup"><span data-stu-id="3e001-122">The status of the configuration to is changed to **Completed**.</span></span>

![Nieuwe configuratieversie in RCS](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> <span data-ttu-id="3e001-124">Wanneer de configuratiestatus wordt gewijzigd, kan er een validatiefoutbericht worden weergegeven met betrekking tot de verbonden toepassingen.</span><span class="sxs-lookup"><span data-stu-id="3e001-124">When the configuration status is changed, you might receive a validation error message that is related to the connected applications.</span></span> <span data-ttu-id="3e001-125">Als u de validatie wilt uitschakelen, selecteert u in het actievenster op het tablad **Configuraties** de optie **Gebruikersparameters** en stelt u vervolgens de optie **Validatie overslaan bij statuswijziging en rebase van configuratie** in op **Ja**</span><span class="sxs-lookup"><span data-stu-id="3e001-125">To turn off the validation, on the Action Pane on the **Configurations** tab, select **User parameters**, and then set the **Skip validation at configuration's status change and rebase** option to **Yes**</span></span> 

## <a name="upload-a-configuration-to-the-global-repository"></a><span data-ttu-id="3e001-126">Een configuratie uploaden naar de algemene opslagplaats</span><span class="sxs-lookup"><span data-stu-id="3e001-126">Upload a configuration to the Global repository</span></span>

<span data-ttu-id="3e001-127">Als u een nieuwe of afgeleide configuratie wilt delen met uw organisatie, kunt u deze uploaden naar de algemene opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="3e001-127">To share a new or derived configuration with your organization, you can upload it to the Global repository.</span></span>

1. <span data-ttu-id="3e001-128">Selecteer de voltooide versie van de configuratie en selecteer vervolgens **Uploaden naar opslagplaats**.</span><span class="sxs-lookup"><span data-stu-id="3e001-128">Select the completed version of the configuration, and then select **Upload into repository**.</span></span>
2. <span data-ttu-id="3e001-129">Selecteer de optie **Algemeen (Microsoft)** en selecteer vervolgens **Uploaden**.</span><span class="sxs-lookup"><span data-stu-id="3e001-129">Select the **Global (Microsoft)** option, and then select **Upload**.</span></span>

    ![Opties voor uploaden naar opslagplaats](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. <span data-ttu-id="3e001-131">Selecteer **Ja** in het venster met het bevestigingsbericht.</span><span class="sxs-lookup"><span data-stu-id="3e001-131">In the confirmation message box, select **Yes**.</span></span> 
4. <span data-ttu-id="3e001-132">Werk de beschrijving van de versie zo nodig bij en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="3e001-132">Update the description of the version as required, and then select **OK**.</span></span> 

<span data-ttu-id="3e001-133">De status van de configuratie wordt bijgewerkt naar **Delen** en de configuratie wordt geüpload naar de algemene opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="3e001-133">The status of the configuration is updated to **Share**, and the configuration is uploaded to the Global repository.</span></span> <span data-ttu-id="3e001-134">Vervolgens kunt u er het volgende mee doen:</span><span class="sxs-lookup"><span data-stu-id="3e001-134">From there, you can work with it in the following ways:</span></span>

- <span data-ttu-id="3e001-135">Importeren in uw Dynamics 365-exemplaar.</span><span class="sxs-lookup"><span data-stu-id="3e001-135">Import it into your Dynamics 365 instance.</span></span> <span data-ttu-id="3e001-136">Zie [(ER) Configuraties importeren vanuit RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="3e001-136">For more information, see [(ER) Import configurations from RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span></span>
- <span data-ttu-id="3e001-137">Delen met een derde of een externe organisatie. Zie [RCS-configuraties voor elektronisch rapportage (ER) delen met externe organisaties](rcs-global-repo-share-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="3e001-137">Share it with a third party or an external organization, see [RCS Share Electronic reporting (ER) configurations with external organizations](rcs-global-repo-share-configuration.md)</span></span>

    ![Afgeleide Intrastat-configuratieversie voor Contoso in de algemene opslagplaats](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a><span data-ttu-id="3e001-139">Een configuratie verwijderen uit de algemene opslagplaats</span><span class="sxs-lookup"><span data-stu-id="3e001-139">Delete a configuration from the Global repository</span></span>
<span data-ttu-id="3e001-140">Voer de volgende stappen uit om een configuratie te verwijderen die uw organisatie heeft gemaakt.</span><span class="sxs-lookup"><span data-stu-id="3e001-140">Complete the following steps to delete a configuration that your organization has created.</span></span>

1. <span data-ttu-id="3e001-141">Controleer in het werkgebied **Elektronische rapportage** of uw configuratieprovider **Actief** is.</span><span class="sxs-lookup"><span data-stu-id="3e001-141">In the **Electronic reporting** workspace, verify that your configuration provider is **Active**.</span></span> <span data-ttu-id="3e001-142">Zie [Configuratieproviders maken en deze als actief markeren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="3e001-142">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
2. <span data-ttu-id="3e001-143">Selecteer voor uw actieve configuratieprovider de optie **Opslagplaats**.</span><span class="sxs-lookup"><span data-stu-id="3e001-143">On your active configuration provider, select **repository**.</span></span>
3. <span data-ttu-id="3e001-144">Selecteer het type opslagplaats **Algemeen** en selecteer **Openen**.</span><span class="sxs-lookup"><span data-stu-id="3e001-144">Select the repository type **Global**, and select **Open**.</span></span>
4. <span data-ttu-id="3e001-145">Zoek op het sneltabblad **Filter** de configuratie die u wilt verwijderen met behulp van de functionaliteit **Filter**.</span><span class="sxs-lookup"><span data-stu-id="3e001-145">On the **Filter** FastTab, find the configuration that you want to delete by using the **Filter** functionality.</span></span>
5. <span data-ttu-id="3e001-146">Selecteer op het sneltabblad **Versie** de versie van de configuratie die u wilt verwijderen en selecteer **Verwijderen**:</span><span class="sxs-lookup"><span data-stu-id="3e001-146">On the **Version** FastTab, select the version of the configuration that you want to delete, and then select **Delete**:</span></span>

    ![Configuratie verwijderen uit algemene opslagplaats](media/RCS_Delete_from_GlobalRepo.JPG)

6. <span data-ttu-id="3e001-148">Selecteer **Ja** in het venster met het bevestigingsbericht.</span><span class="sxs-lookup"><span data-stu-id="3e001-148">In the confirmation message box, select **Yes**.</span></span>

    ![Bevestigingsbericht van configuratieversie verwijderen](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
<span data-ttu-id="3e001-150">De configuratieversie wordt verwijderd en er wordt een bevestigingsbericht weergegeven.</span><span class="sxs-lookup"><span data-stu-id="3e001-150">The configuration version is deleted, and confirmation message is shown.</span></span> 

> [!NOTE]
> <span data-ttu-id="3e001-151">Configuraties kunnen alleen worden verwijderd door de configuratieprovider die deze heeft gemaakt.</span><span class="sxs-lookup"><span data-stu-id="3e001-151">Configurations can only be deleted by the Configuration provider that created them.</span></span> <span data-ttu-id="3e001-152">Als de configuratie is gedeeld met een andere organisatie, moet het delen van de configuratie ongedaan worden maken voordat u deze kunt verwijderen.</span><span class="sxs-lookup"><span data-stu-id="3e001-152">If the configuration has been shared with another organization, the configuration will need to be unshared before you delete it.</span></span>
 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]