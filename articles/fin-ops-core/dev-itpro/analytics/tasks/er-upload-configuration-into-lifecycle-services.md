---
title: Een configuratie in Lifecycle Services uploaden
description: In dit onderwerp wordt uitgelegd hoe u een nieuwe configuratie voor Elektronische rapportage (ER) maakt en uploadt in Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 41a8fcf2592bde4901aba703e0cd124b1155dac6
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270554"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="f4854-103">Een configuratie in Lifecycle Services uploaden</span><span class="sxs-lookup"><span data-stu-id="f4854-103">Upload a configuration into Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f4854-104">In dit onderwerp wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe [configuratie voor elektronische rapportage (ER)](../general-electronic-reporting.md#Configuration) kan maken en uploaden in de [activabibliotheek op projectniveau](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="f4854-104">This topic explains how a user in the System administrator or Electronic reporting developer role can create a new [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) and upload it into the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f4854-105">Het gebruik van LCS als opslagplaats voor ER-configuraties wordt [afgeschaft](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span><span class="sxs-lookup"><span data-stu-id="f4854-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="f4854-106">Zie [Afschaffing Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) Storage](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f4854-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

<span data-ttu-id="f4854-107">In dit voorbeeld maakt u een configuratie en uploadt u deze in LCS voor het voorbeeldbedrijf, Litware, Inc. Deze stappen kunnen in elk bedrijf worden uitgevoerd aangezien ER-configuraties tussen bedrijven worden gedeeld.</span><span class="sxs-lookup"><span data-stu-id="f4854-107">In this example, you will create a configuration and upload it into LCS for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="f4854-108">Als u deze stappen wilt uitvoeren, moet u eerst de stappen voltooien in [Configuratieproviders maken en deze als actief markeren](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="f4854-108">To complete these steps, you must first complete the steps in [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="f4854-109">Ook is toegang tot LCS vereist.</span><span class="sxs-lookup"><span data-stu-id="f4854-109">Access to LCS is also required.</span></span>

1. <span data-ttu-id="f4854-110">Meld u aan bij de toepassing met een van de volgende rollen:</span><span class="sxs-lookup"><span data-stu-id="f4854-110">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="f4854-111">Ontwikkelaar elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="f4854-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="f4854-112">Systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="f4854-112">System administrator</span></span>

2. <span data-ttu-id="f4854-113">Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="f4854-113">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="f4854-114">Selecteer **Litware, Inc.** en markeer dit als **Actief**.</span><span class="sxs-lookup"><span data-stu-id="f4854-114">Select **Litware, Inc.**, and mark it as **Active**.</span></span>
4. <span data-ttu-id="f4854-115">Selecteer **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="f4854-115">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="f4854-116">Zorg ervoor dat de huidige Dynamics 365 Finance-gebruiker lid is van het LCS-project dat de [activabibliotheek](../../lifecycle-services/asset-library.md#asset-library-support) bevat die wordt gebruikt voor het importeren van ER-configuraties.</span><span class="sxs-lookup"><span data-stu-id="f4854-116">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the [Asset library](../../lifecycle-services/asset-library.md#asset-library-support) that is used to import ER configurations.</span></span>
>
> <span data-ttu-id="f4854-117">U hebt geen toegang tot een LCS-project vanuit een ER-opslagplaats voor een ander domein dan het domein dat in Finance wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="f4854-117">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="f4854-118">Als u het probeert, wordt een lege lijst met LCS-projecten weergegeven en kunt u geen ER-configuraties importeren uit de activabibliotheek op projectniveau in LCS.</span><span class="sxs-lookup"><span data-stu-id="f4854-118">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="f4854-119">Als u activabibliotheken op projectniveau wilt openen vanuit een ER-opslagplaats die wordt gebruikt voor het importeren van ER-configuraties, meldt u zich aan bij Finance met de referenties van een gebruiker die hoort bij de tenant (domein) waarvoor het huidige Finance-exemplaar is ingericht.</span><span class="sxs-lookup"><span data-stu-id="f4854-119">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="f4854-120">Een nieuwe gegevensmodelconfiguratie maken</span><span class="sxs-lookup"><span data-stu-id="f4854-120">Create a new data model configuration</span></span>

1. <span data-ttu-id="f4854-121">Ga naar **Organisatiebeheer \> Elektronische rapportage \> Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="f4854-121">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="f4854-122">Selecteer op de pagina **Configuraties** de optie **Configuratie maken** om het dialoogvenster met de vervolgkeuzelijst te openen.</span><span class="sxs-lookup"><span data-stu-id="f4854-122">On the **Configurations** page, select **Create configuration** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="f4854-123">In dit voorbeeld maakt u een configuratie die een voorbeeldgegevensmodel voor elektronische documenten bevat.</span><span class="sxs-lookup"><span data-stu-id="f4854-123">In this example, you will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="f4854-124">Deze gegevensmodelconfiguratie wordt later in LCS geüpload.</span><span class="sxs-lookup"><span data-stu-id="f4854-124">This data model configuration will be uploaded into LCS later.</span></span>

3. <span data-ttu-id="f4854-125">Typ **Voorbeeldmodelconfiguratie** in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="f4854-125">In the **Name** field, enter **Sample model configuration**.</span></span>
4. <span data-ttu-id="f4854-126">Typ **Voorbeeldmodelconfiguratie** in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="f4854-126">In the **Description** field, enter **Sample model configuration**.</span></span>
5. <span data-ttu-id="f4854-127">Selecteer **Configuratie maken**.</span><span class="sxs-lookup"><span data-stu-id="f4854-127">Select **Create configuration**.</span></span>
6. <span data-ttu-id="f4854-128">Selecteer **Modelontwerper**.</span><span class="sxs-lookup"><span data-stu-id="f4854-128">Select **Model designer**.</span></span>
7. <span data-ttu-id="f4854-129">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="f4854-129">Select **New**.</span></span>
8. <span data-ttu-id="f4854-130">Voer in het veld **Naam** de waarde **Invoerpunt** in.</span><span class="sxs-lookup"><span data-stu-id="f4854-130">In the **Name** field, enter **Entry point**.</span></span>
9. <span data-ttu-id="f4854-131">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="f4854-131">Select **Add**.</span></span>
10. <span data-ttu-id="f4854-132">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="f4854-132">Select **Save**.</span></span>
11. <span data-ttu-id="f4854-133">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f4854-133">Close the page.</span></span>
12. <span data-ttu-id="f4854-134">Selecteer **Status wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="f4854-134">Select **Change status**.</span></span>
13. <span data-ttu-id="f4854-135">Selecteer **Voltooien**.</span><span class="sxs-lookup"><span data-stu-id="f4854-135">Select **Complete**.</span></span>
14. <span data-ttu-id="f4854-136">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="f4854-136">Select **OK**.</span></span>
15. <span data-ttu-id="f4854-137">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f4854-137">Close the page.</span></span>

## <a name="register-a-new-repository"></a><span data-ttu-id="f4854-138">Een nieuwe opslagplaats registreren</span><span class="sxs-lookup"><span data-stu-id="f4854-138">Register a new repository</span></span>

1. <span data-ttu-id="f4854-139">Ga naar **Organisatiebeheer \> Werkgebieden \> Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="f4854-139">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="f4854-140">Selecteer in de sectie **Configuratieproviders** de tegel **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="f4854-140">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="f4854-141">Klik op de tegel **Litware, Inc.** op **Opslagplaatsen**.</span><span class="sxs-lookup"><span data-stu-id="f4854-141">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="f4854-142">U kunt nu de lijst met opslagplaatsen voor de configuratieprovider Litware, Inc. openen.</span><span class="sxs-lookup"><span data-stu-id="f4854-142">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="f4854-143">Selecteer **Toevoegen** om het dialoogvenster met vervolgkeuzemenu te openen.</span><span class="sxs-lookup"><span data-stu-id="f4854-143">Select **Add** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="f4854-144">U kunt nu een nieuwe opslagplaats toevoegen.</span><span class="sxs-lookup"><span data-stu-id="f4854-144">You can now add a new repository.</span></span>

5. <span data-ttu-id="f4854-145">Selecteer **LCS** in het veld **Opslagplaats van configuratie**.</span><span class="sxs-lookup"><span data-stu-id="f4854-145">In the **Configuration repository enter** field, select **LCS**.</span></span>
6. <span data-ttu-id="f4854-146">Selecteer **Opslagplaats maken**.</span><span class="sxs-lookup"><span data-stu-id="f4854-146">Select **Create repository**.</span></span>
7. <span data-ttu-id="f4854-147">Typ of selecteer een waarde in het veld **Project**.</span><span class="sxs-lookup"><span data-stu-id="f4854-147">In the **Project** field, enter or select a value.</span></span>

    <span data-ttu-id="f4854-148">Selecteer voor dit voorbeeld het gewenste LCS-project.</span><span class="sxs-lookup"><span data-stu-id="f4854-148">For this example, select the desired LCS project.</span></span> <span data-ttu-id="f4854-149">U moet [toegang](#accessconditions) tot het project hebben.</span><span class="sxs-lookup"><span data-stu-id="f4854-149">You must have [access](#accessconditions) to the project.</span></span>

8. <span data-ttu-id="f4854-150">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="f4854-150">Select **OK**.</span></span>

    <span data-ttu-id="f4854-151">Voer een nieuwe opslagplaats in.</span><span class="sxs-lookup"><span data-stu-id="f4854-151">Complete a new repository entry.</span></span>

9. <span data-ttu-id="f4854-152">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f4854-152">In the list, mark the selected row.</span></span>

    <span data-ttu-id="f4854-153">Selecteer voor dit voorbeeld de opslaglocatierecord **LCS**.</span><span class="sxs-lookup"><span data-stu-id="f4854-153">For this example, select the **LCS** repository record.</span></span>

    <span data-ttu-id="f4854-154">Een geregistreerde opslagplaats wordt gemarkeerd door de huidige provider.</span><span class="sxs-lookup"><span data-stu-id="f4854-154">Note that a registered repository is marked by the current provider.</span></span> <span data-ttu-id="f4854-155">Met andere woorden, alleen configuraties die eigendom van die provider zijn, kunnen in deze opslagplaats worden geplaatst en dus naar het geselecteerde LCS-project worden geüpload.</span><span class="sxs-lookup"><span data-stu-id="f4854-155">In other words, only configurations that are owned by that provider can be put in this repository and therefore uploaded into the selected LCS project.</span></span>

10. <span data-ttu-id="f4854-156">Selecteer **Openen**.</span><span class="sxs-lookup"><span data-stu-id="f4854-156">Select **Open**.</span></span>

    <span data-ttu-id="f4854-157">U opent de opslagplaats om de lijst met ER-configuraties weer te geven.</span><span class="sxs-lookup"><span data-stu-id="f4854-157">You open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="f4854-158">Als het geselecteerde project nog niet voor delen van ER-configuraties is gebruikt, is de lijst leeg.</span><span class="sxs-lookup"><span data-stu-id="f4854-158">If the selected project hasn't yet been used for ER configurations sharing, the list will be empty.</span></span>

11. <span data-ttu-id="f4854-159">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f4854-159">Close the page.</span></span>
12. <span data-ttu-id="f4854-160">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f4854-160">Close the page.</span></span>

## <a name="upload-a-configuration-into-lcs"></a><span data-ttu-id="f4854-161">Een configuratie uploaden naar LCS</span><span class="sxs-lookup"><span data-stu-id="f4854-161">Upload a configuration into LCS</span></span>

1. <span data-ttu-id="f4854-162">Ga naar **Organisatiebeheer \> Elektronische rapportage \> Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="f4854-162">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="f4854-163">Selecteer op de pagina **Configuraties** in de configuratiestructuur het item **Voorbeeldmodelconfiguratie**.</span><span class="sxs-lookup"><span data-stu-id="f4854-163">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="f4854-164">U moet een gemaakte configuratie selecteren die al is voltooid.</span><span class="sxs-lookup"><span data-stu-id="f4854-164">You must select a created configuration that has been already completed.</span></span>

3. <span data-ttu-id="f4854-165">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f4854-165">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="f4854-166">Selecteer voor dit voorbeeld de versie van de geselecteerde configuratie met de status **Voltooid**.</span><span class="sxs-lookup"><span data-stu-id="f4854-166">For this example, select the version of the selected configuration that has a status of **Completed**.</span></span>

4. <span data-ttu-id="f4854-167">Selecteer **Status wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="f4854-167">Select **Change status**.</span></span>
5. <span data-ttu-id="f4854-168">Selecteer **Delen**.</span><span class="sxs-lookup"><span data-stu-id="f4854-168">Select **Share**.</span></span>

    <span data-ttu-id="f4854-169">De status van de configuratie wordt gewijzigd van **Voltooid** in **Gedeeld** wanneer de configuratie wordt gepubliceerd in LCS.</span><span class="sxs-lookup"><span data-stu-id="f4854-169">The status of the configuration is changed from **Completed** to **Shared** when the configuration is published in LCS.</span></span>

6. <span data-ttu-id="f4854-170">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="f4854-170">Select **OK**.</span></span>
7. <span data-ttu-id="f4854-171">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f4854-171">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="f4854-172">Selecteer voor dit voorbeeld de versie van de configuratie die de status **Gedeeld** heeft.</span><span class="sxs-lookup"><span data-stu-id="f4854-172">For this example, select the configuration version that has a status of **Shared**.</span></span>

    <span data-ttu-id="f4854-173">De status van de geselecteerde versie is gewijzigd van **Voltooid** in **Gedeeld**.</span><span class="sxs-lookup"><span data-stu-id="f4854-173">Note that the status of the selected version was changed from **Completed** to **Shared**.</span></span>

8. <span data-ttu-id="f4854-174">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f4854-174">Close the page.</span></span>
9. <span data-ttu-id="f4854-175">Selecteer **Opslagplaatsen**.</span><span class="sxs-lookup"><span data-stu-id="f4854-175">Select **Repositories**.</span></span>

    <span data-ttu-id="f4854-176">U kunt nu de lijst met opslagplaatsen voor de configuratieprovider Litware, Inc. openen.</span><span class="sxs-lookup"><span data-stu-id="f4854-176">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

10. <span data-ttu-id="f4854-177">Selecteer **Openen**.</span><span class="sxs-lookup"><span data-stu-id="f4854-177">Select **Open**.</span></span>

    <span data-ttu-id="f4854-178">Selecteer voor dit voorbeeld de opslaglocatierecord **LCS** en open deze.</span><span class="sxs-lookup"><span data-stu-id="f4854-178">For this example, select the **LCS** repository, and open it.</span></span>

    <span data-ttu-id="f4854-179">De geselecteerde configuratie wordt getoond als een activum van het geselecteerde LCS-project.</span><span class="sxs-lookup"><span data-stu-id="f4854-179">Notice that the selected configuration is shown as an asset of the selected LCS project.</span></span>

11. <span data-ttu-id="f4854-180">Open LCS door naar <https://lcs.dynamics.com> te gaan.</span><span class="sxs-lookup"><span data-stu-id="f4854-180">Open LCS by going to <https://lcs.dynamics.com>.</span></span>
12. <span data-ttu-id="f4854-181">Open een project dat eerder is gebruikt voor de registratie van de opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="f4854-181">Open a project that was used earlier for repository registration.</span></span>
13. <span data-ttu-id="f4854-182">Open de activabibliotheek van het project.</span><span class="sxs-lookup"><span data-stu-id="f4854-182">Open the Asset library of the project.</span></span>
14. <span data-ttu-id="f4854-183">Selecteer het activumtype **GER-configuratie**.</span><span class="sxs-lookup"><span data-stu-id="f4854-183">Select the **GER configuration** asset type.</span></span>

    <span data-ttu-id="f4854-184">De ER-configuratie die u hebt geüpload, moet worden vermeld.</span><span class="sxs-lookup"><span data-stu-id="f4854-184">The ER configuration that you uploaded should be listed.</span></span>

    <span data-ttu-id="f4854-185">De geüploade LCS-configuratie kan naar een ander exemplaar worden geïmporteerd als providers toegang tot dit LCS-project hebben.</span><span class="sxs-lookup"><span data-stu-id="f4854-185">Note that the uploaded LCS configuration can be imported into another instance if providers have access to this LCS project.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
