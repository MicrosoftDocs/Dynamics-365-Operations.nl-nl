---
title: ER-configuraties uitvoeren in RCS en deze uploaden naar de algemene opslagplaats
description: In dit onderwerp wordt uitgelegd hoe u een configuratie voor elektronische rapportage (ER) kunt maken in Microsoft Regulatory Configuration Services (RCS) en deze kunt uploaden naar de algemene opslagplaats.
author: JaneA07
manager: AnnBe
ms.date: 05/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 0e194a8b777f984412d81e315f92ab4bb8a3b0c9
ms.sourcegitcommit: 204cec8ca2a6c4474d21dbcd408e369131a47856
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/13/2020
ms.locfileid: "3371239"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a><span data-ttu-id="7a308-103">ER-configuraties uitvoeren in Regulatory Configuration Services (RCS) en deze uploaden naar de algemene opslagplaats</span><span class="sxs-lookup"><span data-stu-id="7a308-103">Create ER configurations in Regulatory Configuration Services (RCS) and upload them to the Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a308-104">U kunt Microsoft Regulatory Configuration Services (RCS) gebruiken om configuraties voor elektronische rapportage (ER) te ontwerpen en deze zo te publiceren dat ze in uw organisatie kunnen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="7a308-104">You can use Microsoft Regulatory Configuration Services (RCS) to design Electronic reporting (ER) configurations and publish them so that they can be used in your organization.</span></span>

<span data-ttu-id="7a308-105">In de volgende procedures wordt uitgelegd hoe een gebruiker in de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een afgeleide versie van een ER-configuratie kan maken die is geconfigureerd in een RCS-exemplaar en vervolgens de afgeleide configuratie uploaden naar de algemene opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="7a308-105">The following procedures explain how a user in the System Administrator or Electronic Reporting Developer role can create a derived version of an ER configuration that has been configured in an RCS instance, and then upload the derived configuration to the Global repository.</span></span> 

<span data-ttu-id="7a308-106">Voordat u deze procedures kunt uitvoeren, moet u eerst aan de volgende vereisten voldoen:</span><span class="sxs-lookup"><span data-stu-id="7a308-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="7a308-107">Open een RCS-exemplaar.</span><span class="sxs-lookup"><span data-stu-id="7a308-107">Access an RCS instance.</span></span>
- <span data-ttu-id="7a308-108">Maak een actieve configuratieprovider.</span><span class="sxs-lookup"><span data-stu-id="7a308-108">Create an active configuration provider.</span></span> <span data-ttu-id="7a308-109">Zie [Configuratieproviders maken en deze als actief markeren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="7a308-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="7a308-110">U moet er ook voor zorgen dat een RCS-omgeving wordt ingericht voor uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="7a308-110">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="7a308-111">Ga in een Finance and Operations-app naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="7a308-111">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7a308-112">Als er geen RCS-omgeving is ingericht voor uw bedrijf, selecteert u **Regulatory services ‑ Configuratie extern** en volgt u vervolgens de instructies om een RCS-omgeving in te richten.</span><span class="sxs-lookup"><span data-stu-id="7a308-112">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="7a308-113">Als er al een RCS-omgeving is ingericht voor uw bedrijf, gebruikt u de pagina-URL om deze te openen door de aanmeldingsoptie te selecteren.</span><span class="sxs-lookup"><span data-stu-id="7a308-113">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a><span data-ttu-id="7a308-114">Een afgeleide versie van een configuratie maken in RCS</span><span class="sxs-lookup"><span data-stu-id="7a308-114">Create a derived version of a configuration in RCS</span></span>

1. <span data-ttu-id="7a308-115">Controleer in het werkgebied **Elektronische rapportage** of u een actieve configuratieprovider hebt voor uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="7a308-115">In the **Electronic reporting** workspace, verify that you have an active configuration provider for your organization.</span></span> 
2. <span data-ttu-id="7a308-116">Selecteer **Rapportageconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="7a308-116">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="7a308-117">Selecteer de configuratie waarvan u een nieuwe versie wilt afleiden.</span><span class="sxs-lookup"><span data-stu-id="7a308-117">Select the configuration that you want to derive a new version from.</span></span> <span data-ttu-id="7a308-118">U kunt het filterveld boven de structuur gebruiken om de zoekopdracht te verfijnen.</span><span class="sxs-lookup"><span data-stu-id="7a308-118">You can use the filter field above the tree to narrow your search.</span></span>
4. <span data-ttu-id="7a308-119">Selecteer **Configuratie make** \> **Afleiden van naam**.</span><span class="sxs-lookup"><span data-stu-id="7a308-119">Select **Create configuration** \> **Derive from Name**.</span></span>
5. <span data-ttu-id="7a308-120">Voer een naam en omschrijving in en selecteer vervolgens **Configuratie maken** om een nieuwe afgeleide versie te maken.</span><span class="sxs-lookup"><span data-stu-id="7a308-120">Enter a name and description, and then select **Create configuration** to create a new derived version.</span></span>
6. <span data-ttu-id="7a308-121">Selecteer de nieuw afgeleide configuratie, voeg een beschrijving van de versie toe en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="7a308-121">Select the newly derived configuration, add a description of the version, and then select **OK**.</span></span> <span data-ttu-id="7a308-122">De status van de configuratie wordt gewijzigd in **Voltooid**.</span><span class="sxs-lookup"><span data-stu-id="7a308-122">The status of the configuration to is changed to **Completed**.</span></span>

![Nieuwe configuratieversie in RCS](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_CompleteConfig.JPG)

> [!NOTE]
> <span data-ttu-id="7a308-124">Wanneer de configuratiestatus wordt gewijzigd, kan er een validatiefoutbericht worden weergegeven met betrekking tot de verbonden toepassingen.</span><span class="sxs-lookup"><span data-stu-id="7a308-124">When the configuration status is changed, you might receive a validation error message that is related to the connected applications.</span></span> <span data-ttu-id="7a308-125">Als u de validatie wilt uitschakelen, selecteert u in het actievenster op het tablad **Configuraties** de optie **Gebruikersparameters** en stelt u vervolgens de optie **Validatie overslaan bij statuswijziging en rebase van configuratie** in op **Ja**</span><span class="sxs-lookup"><span data-stu-id="7a308-125">To turn off the validation, on the Action Pane on the **Configurations** tab, select **User parameters**, and then set the **Skip validation at configuration's status change and rebase** option to **Yes**</span></span> 

## <a name="upload-a-configuration-to-the-global-repository"></a><span data-ttu-id="7a308-126">Een configuratie uploaden naar de algemene opslagplaats</span><span class="sxs-lookup"><span data-stu-id="7a308-126">Upload a configuration to the Global repository</span></span>

<span data-ttu-id="7a308-127">Als u een nieuwe of afgeleide configuratie wilt delen met uw organisatie, kunt u deze uploaden naar de algemene opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="7a308-127">To share a new or derived configuration with your organization, you can upload it to the Global repository.</span></span>

1. <span data-ttu-id="7a308-128">Selecteer de voltooide versie van de configuratie en selecteer vervolgens **Uploaden naar opslagplaats**.</span><span class="sxs-lookup"><span data-stu-id="7a308-128">Select the completed version of the configuration, and then select **Upload into repository**.</span></span>
2. <span data-ttu-id="7a308-129">Selecteer de optie **Algemeen (Microsoft)** en selecteer vervolgens **Uploaden**.</span><span class="sxs-lookup"><span data-stu-id="7a308-129">Select the **Global (Microsoft)** option, and then select **Upload**.</span></span>

    ![Opties voor uploaden naar opslagplaats](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_Upload_to_GlobalRepo_options.JPG)

3. <span data-ttu-id="7a308-131">Selecteer **Ja** in het venster met het bevestigingsbericht.</span><span class="sxs-lookup"><span data-stu-id="7a308-131">In the confirmation message box, select **Yes**.</span></span> 
4. <span data-ttu-id="7a308-132">Werk de beschrijving van de versie zo nodig bij en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="7a308-132">Update the description of the version as required, and then select **OK**.</span></span> 

<span data-ttu-id="7a308-133">De status van de configuratie wordt bijgewerkt naar **Delen** en de configuratie wordt geüpload naar de algemene opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="7a308-133">The status of the configuration is updated to **Share**, and the configuration is uploaded to the Global repository.</span></span> <span data-ttu-id="7a308-134">Vervolgens kunt u er het volgende mee doen:</span><span class="sxs-lookup"><span data-stu-id="7a308-134">From there, you can work with it in the following ways:</span></span>

- <span data-ttu-id="7a308-135">Importeren in uw Dynamics 365-exemplaar.</span><span class="sxs-lookup"><span data-stu-id="7a308-135">Import it into your Dynamics 365 instance.</span></span> <span data-ttu-id="7a308-136">Zie [(ER) Configuraties importeren vanuit RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="7a308-136">For more information, see [(ER) Import configurations from RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span></span>
- <span data-ttu-id="7a308-137">Delen met een derde of een externe organisatie. Zie [RCS-configuraties voor elektronisch rapportage (ER) delen met externe organisaties](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/rcs-global-share-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="7a308-137">Share it with a third party or an external organization, see [RCS Share Electronic reporting (ER) configurations with external organizations](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/rcs-global-share-configuration.md)</span></span>

![Afgeleide Intrastat-configuratieversie voor Contoso in de algemene opslagplaats](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_Config_upload_GlobalRepo.JPG)
