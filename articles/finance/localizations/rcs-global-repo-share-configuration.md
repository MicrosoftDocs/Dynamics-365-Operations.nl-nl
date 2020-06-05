---
title: ER-configuraties in RCS/de algemene opslagplaats delen met externe organisaties
description: In dit onderwerp wordt uitgelegd hoe u ER-configuraties (elektronische rapportage) in Microsoft Regulatory Configuration Services (RCS)/de algemene opslagplaats rechtstreeks met externe organisaties kunt delen.
author: JaneA07
manager: AnnBe
ms.date: 05/04/2020
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
ms.openlocfilehash: 04c46824123906eccbfff18a03974c8043729e0a
ms.sourcegitcommit: 204cec8ca2a6c4474d21dbcd408e369131a47856
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/13/2020
ms.locfileid: "3371238"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a><span data-ttu-id="3d65d-103">ER-configuraties (elektronische rapportage) in Microsoft Regulatory Configuration Services (RCS) algemene opslagplaats met externe organisaties delen</span><span class="sxs-lookup"><span data-stu-id="3d65d-103">Share Electronic reporting (ER) configurations in Regulatory Configuration Services (RCS) Global repository with external organizations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d65d-104">U kunt Microsoft Regulatory Configuration Services (RCS) gebruiken om configuraties voor elektronische rapportage (ER) te delen en deze vervolgens te publiceren naar externe organisaties.</span><span class="sxs-lookup"><span data-stu-id="3d65d-104">You can use Microsoft Regulatory Configuration Services (RCS) to share Electronic reporting (ER) configurations and then publish them to external organizations.</span></span>

<span data-ttu-id="3d65d-105">In de volgende procedures wordt uitgelegd hoe een RCS-gebruiker een versie van een ER-configuratie die is geconfigureerd in een RCS-exemplaar kan delen met een externe organisatie.</span><span class="sxs-lookup"><span data-stu-id="3d65d-105">The following procedures explain how an RCS user can share a version of an ER configuration that has been configured in an RCS instance with an external organization.</span></span> <span data-ttu-id="3d65d-106">Voordat u deze procedures kunt uitvoeren, moet u eerst aan de volgende vereisten voldoen:</span><span class="sxs-lookup"><span data-stu-id="3d65d-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="3d65d-107">Open een RCS-exemplaar.</span><span class="sxs-lookup"><span data-stu-id="3d65d-107">Access an RCS instance.</span></span>
- <span data-ttu-id="3d65d-108">Maak een actieve configuratieprovider.</span><span class="sxs-lookup"><span data-stu-id="3d65d-108">Create an active configuration provider.</span></span> <span data-ttu-id="3d65d-109">Zie [Configuratieproviders maken en deze als actief markeren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="3d65d-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
- <span data-ttu-id="3d65d-110">Maak en upload een nieuwe versie van een ER-configuratie.</span><span class="sxs-lookup"><span data-stu-id="3d65d-110">Create and upload a new version of an ER configuration.</span></span> <span data-ttu-id="3d65d-111">Zie [Een nieuwe versie van een ER-configuratie (elektronische rapportage) maken en uploaden](rcs-global-repo-upload.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="3d65d-111">For more information, see [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

<span data-ttu-id="3d65d-112">U moet er ook voor zorgen dat een RCS-omgeving wordt ingericht voor uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="3d65d-112">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="3d65d-113">Ga in een Finance and Operations-app naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="3d65d-113">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="3d65d-114">Als er geen RCS-omgeving is ingericht voor uw bedrijf, selecteert u **Regulatory services ‑ Configuratie extern** en volgt u vervolgens de instructies om een RCS-omgeving in te richten.</span><span class="sxs-lookup"><span data-stu-id="3d65d-114">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="3d65d-115">Als er al een RCS-omgeving is ingericht voor uw bedrijf, gebruikt u de pagina-URL om deze te openen door de aanmeldingsoptie te selecteren.</span><span class="sxs-lookup"><span data-stu-id="3d65d-115">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="verify-the-configuration-that-you-want-to-share"></a><span data-ttu-id="3d65d-116">De configuratie controleren die u wilt delen</span><span class="sxs-lookup"><span data-stu-id="3d65d-116">Verify the configuration that you want to share</span></span>

<span data-ttu-id="3d65d-117">Voer de volgende stappen uit om te controleren of de configuratie die u wilt delen al is geüpload naar de algemene opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="3d65d-117">Follow these steps to verify that the configuration that you want to share has already been uploaded to the Global repository.</span></span>

1. <span data-ttu-id="3d65d-118">Selecteer in het werkgebied **Elektronische rapportage** de optie **Opslagplaatsen** voor uw configuratieprovider.</span><span class="sxs-lookup"><span data-stu-id="3d65d-118">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>

    ![Configuratieproviders](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_config_provider.JPG)

2. <span data-ttu-id="3d65d-120">Selecteer **Algemene opslagplaats** \> **Openen**.</span><span class="sxs-lookup"><span data-stu-id="3d65d-120">Select **Global repository** \> **Open**.</span></span>
3. <span data-ttu-id="3d65d-121">Zoek naar de configuratie die u wilt delen.</span><span class="sxs-lookup"><span data-stu-id="3d65d-121">Search for the configuration that you want to share.</span></span> <span data-ttu-id="3d65d-122">U kunt het filterveld gebruiken om de zoekopdracht te verfijnen.</span><span class="sxs-lookup"><span data-stu-id="3d65d-122">You can use the filter field to narrow your search.</span></span> <span data-ttu-id="3d65d-123">Als u de configuratie niet kunt vinden in de algemene opslagplaats, volgt u de stappen in [Een nieuwe versie van een ER-configuratie (elektronische rapportage) maken en uploaden](rcs-global-repo-upload.md).</span><span class="sxs-lookup"><span data-stu-id="3d65d-123">If you can't find the configuration in the Global repository, follow the steps in [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

## <a name="share-er-configurations-with-external-organizations"></a><span data-ttu-id="3d65d-124">ER-configuraties delen met externe organisaties</span><span class="sxs-lookup"><span data-stu-id="3d65d-124">Share ER configurations with external organizations</span></span>

<span data-ttu-id="3d65d-125">Nadat u een configuratie hebt gemaakt onder uw configuratieprovider, kunt u deze rechtstreeks delen met externe organisaties via het sneltabblad **Gedeeld met** op de pagina **Algemene opslagplaats voor configuratie**.</span><span class="sxs-lookup"><span data-stu-id="3d65d-125">After a configuration has been created under your configuration provider, you can share it directly with external organizations by using the **Shared with** FastTab on the **Global configuration repository** page.</span></span>

1. <span data-ttu-id="3d65d-126">Selecteer in het werkgebied **Elektronische rapportage** de optie **Opslagplaatsen** voor uw configuratieprovider.</span><span class="sxs-lookup"><span data-stu-id="3d65d-126">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>
2. <span data-ttu-id="3d65d-127">Selecteer **Algemene opslagplaats** \> **Openen**.</span><span class="sxs-lookup"><span data-stu-id="3d65d-127">Select **Global repository** \> **Open**.</span></span> 
3. <span data-ttu-id="3d65d-128">Selecteer de configuratie die u wilt delen.</span><span class="sxs-lookup"><span data-stu-id="3d65d-128">Select the configuration that you want to share.</span></span>
4. <span data-ttu-id="3d65d-129">Selecteer op het sneltabblad **Gedeeld met** de optie **Organisatie**.</span><span class="sxs-lookup"><span data-stu-id="3d65d-129">On the **Shared with** FastTab, select **Organization**.</span></span>

    ![Sneltabblad Gedeeld met](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_Share_with_org.JPG)

5. <span data-ttu-id="3d65d-131">Voer in het dialoogvenster de domeinnaam in voor de externe organisatie en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="3d65d-131">In the dialog box, enter the domain name for the external organization, and then select **OK**.</span></span>

    ![Dialoogvenster Configuratieversie delen met externe organisatie](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_Share_with_form.JPG)

<span data-ttu-id="3d65d-133">De configuratie wordt gedeeld met de externe organisatie en is beschikbaar voor die organisatie in de algemene opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="3d65d-133">The configuration is shared with the external organization and is available to that organization in the Global repository.</span></span> <span data-ttu-id="3d65d-134">Hier vandaan kan het worden geïmporteerd in het exemplaar van RCS of in de exemplaren van Finance and Operations-apps van de organisatie.</span><span class="sxs-lookup"><span data-stu-id="3d65d-134">From there, it can be imported into the organization's instance of RCS or into its instances of Finance and Operations apps.</span></span>

![Configuratie gedeeld met een externe organisatie](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_Share_with_test.com)

6. <span data-ttu-id="3d65d-136">Als u het delen van een configuratie die eerder met een externe organisatie is gedeeld ongedaan wilt maken, selecteert u de configuratie en klikt u op **Delen ongedaan maken**. Selecteer vervolgens **OK**</span><span class="sxs-lookup"><span data-stu-id="3d65d-136">To unshare a configuration that has been previously shared with an external organization, select the configuration and click **Unshare**, and then select **OK**</span></span>
