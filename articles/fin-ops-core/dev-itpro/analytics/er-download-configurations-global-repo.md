---
title: ER-configuraties downloaden uit de algemene opslagplaats van de configuratieservice
description: In dit onderwerp wordt uitgelegd hoe u ER-configuraties kunt downloaden uit de algemene opslagplaats van de configuratieservice.
author: NickSelin
manager: AnnBe
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: a96e78a64fe0559ae5f3bfddabf3fe1cad8a3dcb
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679553"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a><span data-ttu-id="a10e3-103">ER-configuraties downloaden uit de algemene opslagplaats van de configuratieservice</span><span class="sxs-lookup"><span data-stu-id="a10e3-103">Download ER configurations from the Global repository of Configuration service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a10e3-104">In dit onderwerp wordt uitgelegd hoe u [ER-configuraties](general-electronic-reporting.md#Configuration) kunt downloaden uit de algemene opslagplaats van de configuratieservice.</span><span class="sxs-lookup"><span data-stu-id="a10e3-104">This topic explains how to download [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the Global repository of configuration service.</span></span> <span data-ttu-id="a10e3-105">Zie [Microsoft Dynamics 365 for Finance and Operations - Regulatory services, configuratieservice](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="a10e3-105">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="open-configurations-repository"></a><span data-ttu-id="a10e3-106">Opslagplaats met configuraties openen</span><span class="sxs-lookup"><span data-stu-id="a10e3-106">Open configurations repository</span></span>

1. <span data-ttu-id="a10e3-107">Meld u aan bij de Dynamics 365 Finance-toepassing met een van de volgende rollen:</span><span class="sxs-lookup"><span data-stu-id="a10e3-107">Sign in to the Dynamics 365 Finance application using one of the following roles:</span></span>

    - <span data-ttu-id="a10e3-108">Ontwikkelaar elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="a10e3-108">Electronic reporting developer</span></span>
    - <span data-ttu-id="a10e3-109">Functioneel consultant elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="a10e3-109">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="a10e3-110">Systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="a10e3-110">System administrator</span></span>

2. <span data-ttu-id="a10e3-111">Ga naar **Organisatiebeheer > Werkruimten > Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="a10e3-111">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="a10e3-112">Selecteer in de sectie **Configuratieproviders** de tegel **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="a10e3-112">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
3. <span data-ttu-id="a10e3-113">Klik op de tegel **Microsoft** op **Opslagplaatsen**.</span><span class="sxs-lookup"><span data-stu-id="a10e3-113">On the **Microsoft** tile, select **Repositories**.</span></span>

    ![Werkgebied voor elektronische rapportage](./media/er-download-configurations-global-repo-er-workspace.png)

4. <span data-ttu-id="a10e3-115">Selecteer in het raster op de pagina **Opslagplaatsen van configuraties** pagina de bestaande opslagplaats van het type **Algemeen**.</span><span class="sxs-lookup"><span data-stu-id="a10e3-115">On the **Configuration repositories** page, in the grid, select the existing repository of the **Global** type.</span></span> <span data-ttu-id="a10e3-116">Als deze opslagplaats niet wordt weergegeven in het raster, volgt u deze stappen:</span><span class="sxs-lookup"><span data-stu-id="a10e3-116">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="a10e3-117">Selecteer **Toevoegen** om een nieuwe opslagplaats toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="a10e3-117">Select **Add** to add a new repository.</span></span>
    2. <span data-ttu-id="a10e3-118">Selecteer **Algemeen** als type opslagplaats en selecteer vervolgens **Opslagplaats maken**.</span><span class="sxs-lookup"><span data-stu-id="a10e3-118">Select **Global** as the repository type, and then select **Create repository**.</span></span>
    3. <span data-ttu-id="a10e3-119">Volg de instructies van de autorisatie als hierom wordt gevraagd.</span><span class="sxs-lookup"><span data-stu-id="a10e3-119">If prompted, follow the authorization instructions.</span></span>
    4. <span data-ttu-id="a10e3-120">Voer een naam en beschrijving in voor de opslagplaats en selecteer **OK** om de nieuwe opslagplaats te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="a10e3-120">Enter a name and description for the repository and then select **OK** to confirm the new repository entry.</span></span>
    5. <span data-ttu-id="a10e3-121">Selecteer in het raster de nieuwe opslagplaats van het type **Algemeen**.</span><span class="sxs-lookup"><span data-stu-id="a10e3-121">In the grid, select the new repository of the **Global** type.</span></span>

5. <span data-ttu-id="a10e3-122">Selecteer **Openen** om de lijst met ER-configuraties voor de geselecteerde opslagplaats weer te geven.</span><span class="sxs-lookup"><span data-stu-id="a10e3-122">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    ![De pagina Opslagplaatsen van configuraties](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a><span data-ttu-id="a10e3-124">Eén configuratie importeren</span><span class="sxs-lookup"><span data-stu-id="a10e3-124">Import a single configuration</span></span>

1. <span data-ttu-id="a10e3-125">Selecteer op de pagina **Opslagplaatsen van configuraties** in de configuratiestructuur de gewenste ER-configuratie.</span><span class="sxs-lookup"><span data-stu-id="a10e3-125">On the **Configuration repositories** page, in the configurations tree, select the ER configuration that you want.</span></span>
2. <span data-ttu-id="a10e3-126">Selecteer op het sneltabblad **Versies** de vereiste versie van de geselecteerde ER-configuratie.</span><span class="sxs-lookup"><span data-stu-id="a10e3-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
3. <span data-ttu-id="a10e3-127">Selecteer **Importeren** om de geselecteerde versie vanuit de algemene opslagplaats te downloaden naar het huidige exemplaar van Finance.</span><span class="sxs-lookup"><span data-stu-id="a10e3-127">Select **Import** to download the selected version from Global repository to the current Finance instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a10e3-128">De knop **Importeren** is niet beschikbaar voor ER-configuratieversies die al aanwezig zijn in het huidige Finance-exemplaar.</span><span class="sxs-lookup"><span data-stu-id="a10e3-128">The **Import** button is unavailable for ER configuration versions that are already present in the current Finance instance.</span></span>

    ![Configuratie archiefpagina](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a><span data-ttu-id="a10e3-130">Gefilterde configuraties importeren</span><span class="sxs-lookup"><span data-stu-id="a10e3-130">Import filtered configurations</span></span>

1. <span data-ttu-id="a10e3-131">Vouw op de pagina **Opslagplaatsen van configuraties** in de configuratiestructuur het sneltabblad **Filter** uit.</span><span class="sxs-lookup"><span data-stu-id="a10e3-131">On the **Configuration repositories** page, in the configurations tree, expand the **Filter** FastTab.</span></span>
2. <span data-ttu-id="a10e3-132">Voeg in raster **Labels** de benodigde labels toe.</span><span class="sxs-lookup"><span data-stu-id="a10e3-132">In the **Tags** grid, add any tags that are needed.</span></span>
3. <span data-ttu-id="a10e3-133">Selecteer de betreffende land-/regiocodes in het veld **Toepasbaarheid land/regio** en selecteer vervolgens **Filter toepassen**.</span><span class="sxs-lookup"><span data-stu-id="a10e3-133">In the **Country/region applicability** field, select the appropriate country/region codes, and then select  **Apply filter**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a10e3-134">Op het sneltabblad **Configuraties** worden alle configuraties weergegeven die voldoen aan de opgegeven selectievoorwaarden.</span><span class="sxs-lookup"><span data-stu-id="a10e3-134">The **Configurations** FastTab shows all the configurations that satisfy the specified selection conditions.</span></span>

4. <span data-ttu-id="a10e3-135">Selecteer op het sneltabblad **Configuraties** de optie **Importeren** om de gefilterde configuraties uit de algemene opslagplaats naar het huidige exemplaar te downloaden.</span><span class="sxs-lookup"><span data-stu-id="a10e3-135">On the **Configurations** FastTab, select **Import** to download the filtered configurations from the Global repository to the current instance.</span></span>
5. <span data-ttu-id="a10e3-136">Selecteer op het sneltabblad **Configuraties** de optie **Filter opnieuw instellen** om de opgegeven selectievoorwaarden op te schonen.</span><span class="sxs-lookup"><span data-stu-id="a10e3-136">On the **Configurations** FastTab, select **Reset filter** to clean up the specified selection conditions.</span></span>

    ![Configuratie archiefpagina](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> <span data-ttu-id="a10e3-138">Afhankelijk van de ER-instellingen worden configuraties gevalideerd nadat ze zijn geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="a10e3-138">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="a10e3-139">U krijgt mogelijk meldingen over inconsistentieproblemen die worden vastgesteld.</span><span class="sxs-lookup"><span data-stu-id="a10e3-139">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="a10e3-140">U moet de problemen oplossen voordat u de geïmporteerde configuratieversie kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="a10e3-140">Before you can use the imported configuration version, you must resolve the issues.</span></span> <span data-ttu-id="a10e3-141">Zie voor meer informatie de lijst met gerelateerde bronnen voor dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="a10e3-141">For more information, see the list of related resources for this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="a10e3-142">ER-configuraties worden geconfigureerd als afhankelijk van andere configuraties.</span><span class="sxs-lookup"><span data-stu-id="a10e3-142">ER configurations can be configured as being dependent on other configurations.</span></span> <span data-ttu-id="a10e3-143">In combinatie met een geselecteerde configuratie kunnen andere configuraties dus automatisch worden geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="a10e3-143">Therefore, along with a selected configuration, other configurations might be automatically imported.</span></span> <span data-ttu-id="a10e3-144">Zie [De afhankelijkheid van ER-configuraties voor andere onderdelen definiëren](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md) voor meer informatie over configuratieafhankelijkheden.</span><span class="sxs-lookup"><span data-stu-id="a10e3-144">For more about configuration dependencies, see [Define the dependency of ER configurations on other components](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a10e3-145">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="a10e3-145">Additional resources</span></span>

[<span data-ttu-id="a10e3-146">Overzicht van elektronische rapportage (ER)</span><span class="sxs-lookup"><span data-stu-id="a10e3-146">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
