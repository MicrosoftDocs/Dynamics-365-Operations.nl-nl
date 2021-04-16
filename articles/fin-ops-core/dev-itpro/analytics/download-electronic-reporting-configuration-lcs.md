---
title: Elektronische rapportageconfiguraties downloaden van Lifecycle Services
description: In dit onderwerp wordt uitgelegd hoe u configuraties voor Elektronische rapportage (ER) kunt downloaden vanuit Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 418586113c038c3227f0704495a561eac319bdc9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745082"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="b8060-103">Elektronische rapportageconfiguraties downloaden van Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="b8060-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b8060-104">In dit onderwerp wordt uitgelegd hoe u de nieuwste versie van [ER-configuraties](general-electronic-reporting.md#Configuration) kunt downloaden uit de [bibliotheek met gedeelde activa](../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="b8060-104">This topic explains how to download the newest version of [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the [Shared asset library](../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="b8060-105">Meld u aan bij de toepassing met een van de volgende rollen:</span><span class="sxs-lookup"><span data-stu-id="b8060-105">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="b8060-106">Ontwikkelaar elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="b8060-106">Electronic reporting developer</span></span>
    - <span data-ttu-id="b8060-107">Functioneel consultant elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="b8060-107">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="b8060-108">Systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="b8060-108">System administrator</span></span>

2. <span data-ttu-id="b8060-109">Ga naar **Organisatiebeheer** &gt; **Werkgebieden** &gt; **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="b8060-109">Go to **Organization administration** &gt; **Workspaces** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="b8060-110">Selecteer in de sectie **Configuratieproviders** de tegel **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="b8060-110">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="b8060-111">Klik op de tegel **Microsoft** op **Opslagplaatsen**.</span><span class="sxs-lookup"><span data-stu-id="b8060-111">On the **Microsoft** tile, select **Repositories**.</span></span>

    <span data-ttu-id="b8060-112">[![Microsoft-tegel op de pagina Lokalisatieconfiguraties](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="b8060-112">[![Microsoft tile on the Localization configurations page](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="b8060-113">Selecteer in het raster op de pagina **Opslagplaatsen van configuraties** pagina de bestaande opslagplaats van het type **LCS**.</span><span class="sxs-lookup"><span data-stu-id="b8060-113">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="b8060-114">Als deze opslagplaats niet wordt weergegeven in het raster, volgt u deze stappen:</span><span class="sxs-lookup"><span data-stu-id="b8060-114">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="b8060-115">Selecteer **Toevoegen** om een opslagplaats toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="b8060-115">Select **Add** to add a repository.</span></span>
    2. <span data-ttu-id="b8060-116">Selecteer **LCS** als opslagplaatstype.</span><span class="sxs-lookup"><span data-stu-id="b8060-116">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="b8060-117">Selecteer **Opslagplaats maken**.</span><span class="sxs-lookup"><span data-stu-id="b8060-117">Select **Create repository**.</span></span>
    4. <span data-ttu-id="b8060-118">Volg de instructies op het scherm als u wordt gevraagd om autorisatie.</span><span class="sxs-lookup"><span data-stu-id="b8060-118">If you're prompted about authorization, follow the on-screen instructions.</span></span>
    5. <span data-ttu-id="b8060-119">Voer een naam en een beschrijving in voor de opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="b8060-119">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="b8060-120">Selecteer **OK** om de nieuwe opslagplaats te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="b8060-120">Select **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="b8060-121">Selecteer in het raster de nieuwe opslagplaats van het type **LCS**.</span><span class="sxs-lookup"><span data-stu-id="b8060-121">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="b8060-122">Selecteer **Openen** om de lijst met ER-configuraties voor de geselecteerde opslagplaats weer te geven.</span><span class="sxs-lookup"><span data-stu-id="b8060-122">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="b8060-123">[![De pagina Opslagplaatsen van configuraties](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="b8060-123">[![Configuration repositories page](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

    > [!TIP]
    > <span data-ttu-id="b8060-124">Als u problemen ondervindt bij het openen van de LCS-opslagplaats voor het downloaden van configuraties uit de bibliotheek met gedeelde activa in LCS, kunt u configuraties vanuit de [globale opslagplaats](er-download-configurations-global-repo.md) downloaden.</span><span class="sxs-lookup"><span data-stu-id="b8060-124">If you have trouble accessing the LCS repository to download configurations from the Shared asset library in LCS, you can download configurations from the [Global repository](er-download-configurations-global-repo.md) instead.</span></span>

7. <span data-ttu-id="b8060-125">Selecteer in de configuratiestructuur in het linkerdeelvenster de vereiste ER-configuratie.</span><span class="sxs-lookup"><span data-stu-id="b8060-125">In the configurations tree in the left pane, select the required ER configuration.</span></span>
8. <span data-ttu-id="b8060-126">Selecteer op het sneltabblad **Versies** de vereiste versie van de geselecteerde ER-configuratie.</span><span class="sxs-lookup"><span data-stu-id="b8060-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="b8060-127">Selecteer **Importeren** om de geselecteerde versie vanuit LCS te downloaden naar het huidige exemplaar.</span><span class="sxs-lookup"><span data-stu-id="b8060-127">Select **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b8060-128">De knop **Importeren** is niet beschikbaar voor ER-configuratieversies die al aanwezig zijn in het huidige exemplaar.</span><span class="sxs-lookup"><span data-stu-id="b8060-128">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="b8060-129">[![Configuratie archiefpagina](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="b8060-129">[![Configuration repository page](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="b8060-130">Afhankelijk van de ER-instellingen worden configuraties gevalideerd nadat ze zijn geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="b8060-130">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="b8060-131">U krijgt mogelijk meldingen over inconsistentieproblemen die worden vastgesteld.</span><span class="sxs-lookup"><span data-stu-id="b8060-131">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="b8060-132">U moet deze problemen oplossen voordat u de geïmporteerde configuratieversie kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="b8060-132">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="b8060-133">Zie voor meer informatie de lijst met gerelateerde onderwerpen voor dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="b8060-133">For more information, see the list of related topics for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b8060-134">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="b8060-134">Additional resources</span></span>

[<span data-ttu-id="b8060-135">Overzicht van elektronische rapportage (ER)</span><span class="sxs-lookup"><span data-stu-id="b8060-135">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="b8060-136">ER-configuraties downloaden uit de algemene opslagplaats van de configuratieservice</span><span class="sxs-lookup"><span data-stu-id="b8060-136">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]