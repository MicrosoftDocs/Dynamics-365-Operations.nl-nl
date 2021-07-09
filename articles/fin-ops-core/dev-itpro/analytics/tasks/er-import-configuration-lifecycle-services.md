---
title: Een configuratie vanuit Lifecycle Services importeren
description: In dit onderwerp wordt beschreven hoe u een nieuwe versie van een ER-configuratie (Electronic Reporting) importeert vanuit Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b58ecb8a7d6f52631dbca7642a4acbcf6ff895a3
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270832"
---
# <a name="import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="07de3-103">Een configuratie vanuit Lifecycle Services importeren</span><span class="sxs-lookup"><span data-stu-id="07de3-103">Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="07de3-104">In dit onderwerp wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe versie van een [configuratie voor elektronische rapportage (ER)](../general-electronic-reporting.md#Configuration) vanuit de [activabibliotheek op projectniveau](../../lifecycle-services/asset-library.md) kan importeren in Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="07de3-104">This topic explains how a user in the System administrator or Electronic reporting developer role can import a new version of an [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) from the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="07de3-105">Het gebruik van LCS als opslagplaats voor ER-configuraties wordt [afgeschaft](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span><span class="sxs-lookup"><span data-stu-id="07de3-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="07de3-106">Zie [Afschaffing Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) Storage](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="07de3-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

<span data-ttu-id="07de3-107">In dit voorbeeld selecteert u de gewenste versie van de ER-configuratie en importeert u deze voor het voorbeeldbedrijf, Litware, Inc. Deze stappen kunnen in elk bedrijf worden uitgevoerd aangezien ER-configuraties tussen bedrijven worden gedeeld.</span><span class="sxs-lookup"><span data-stu-id="07de3-107">In this example, you will select the desired version of the ER configuration and import it for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="07de3-108">Als u deze stappen wilt uitvoeren, moet u eerst de stappen in [Een configuratie in Lifecycle Services uploaden](er-upload-configuration-into-lifecycle-services.md) voltooien.</span><span class="sxs-lookup"><span data-stu-id="07de3-108">To complete these steps, you must first complete the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="07de3-109">Ook is toegang tot LCS vereist.</span><span class="sxs-lookup"><span data-stu-id="07de3-109">Access to LCS is also required.</span></span>

1. <span data-ttu-id="07de3-110">Meld u aan bij de toepassing met een van de volgende rollen:</span><span class="sxs-lookup"><span data-stu-id="07de3-110">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="07de3-111">Ontwikkelaar elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="07de3-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="07de3-112">Systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="07de3-112">System administrator</span></span>

2. <span data-ttu-id="07de3-113">Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="07de3-113">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="07de3-114">Selecteer **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="07de3-114">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="07de3-115">Zorg ervoor dat de huidige Dynamics 365 Finance-gebruiker lid is van het LCS-project dat de activabibliotheek bevat waartoe de gebruiker [toegang](../../lifecycle-services/asset-library.md#asset-library-support) wil hebben voor het importeren van ER-configuraties.</span><span class="sxs-lookup"><span data-stu-id="07de3-115">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the Asset library that the user wants to [access](../../lifecycle-services/asset-library.md#asset-library-support) to import ER configurations.</span></span>
>
> <span data-ttu-id="07de3-116">U hebt geen toegang tot een LCS-project vanuit een ER-opslagplaats voor een ander domein dan het domein dat in Finance wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="07de3-116">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="07de3-117">Als u het probeert, wordt een lege lijst met LCS-projecten weergegeven en kunt u geen ER-configuraties importeren uit de activabibliotheek op projectniveau in LCS.</span><span class="sxs-lookup"><span data-stu-id="07de3-117">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="07de3-118">Als u activabibliotheken op projectniveau wilt openen vanuit een ER-opslagplaats die wordt gebruikt voor het importeren van ER-configuraties, meldt u zich aan bij Finance met de referenties van een gebruiker die hoort bij de tenant (domein) waarvoor het huidige Finance-exemplaar is ingericht.</span><span class="sxs-lookup"><span data-stu-id="07de3-118">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a><span data-ttu-id="07de3-119">Een gedeelde versie van een gegevensmodelconfiguratie verwijderen</span><span class="sxs-lookup"><span data-stu-id="07de3-119">Delete a shared version of a data model configuration</span></span>

1. <span data-ttu-id="07de3-120">Selecteer op de pagina **Configuraties** in de configuratiestructuur het item **Voorbeeldmodelconfiguratie**.</span><span class="sxs-lookup"><span data-stu-id="07de3-120">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="07de3-121">U hebt de eerste versie van een voorbeeldgegevensmodelconfiguratie gemaakt en gepubliceerd naar LCS tijdens de procedure in [Een configuratie in Lifecycle Services uploaden](er-upload-configuration-into-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="07de3-121">You created the first version of a sample data model configuration and published it to LCS when you completed the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="07de3-122">In deze procedure verwijdert u deze versie van de ER-configuratie.</span><span class="sxs-lookup"><span data-stu-id="07de3-122">In this procedure, you will delete that version of the ER configuration.</span></span> <span data-ttu-id="07de3-123">Vervolgens importeert u die versie uit LCS verderop in dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="07de3-123">You will then import that version from LCS later in this topic.</span></span>

2. <span data-ttu-id="07de3-124">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="07de3-124">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="07de3-125">Selecteer voor dit voorbeeld de versie van de configuratie die de status **Gedeeld** heeft.</span><span class="sxs-lookup"><span data-stu-id="07de3-125">For this example, select the version of the configuration that has a status of **Shared**.</span></span> <span data-ttu-id="07de3-126">Deze status geeft aan dat de configuratie is gepubliceerd naar LCS.</span><span class="sxs-lookup"><span data-stu-id="07de3-126">This status indicates that the configuration has been published to LCS.</span></span>

3. <span data-ttu-id="07de3-127">Selecteer **Status wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="07de3-127">Select **Change status**.</span></span>
4. <span data-ttu-id="07de3-128">Selecteer **Beëindigen**.</span><span class="sxs-lookup"><span data-stu-id="07de3-128">Select **Discontinue**.</span></span>

    <span data-ttu-id="07de3-129">Door de status van de geselecteerde versie van **Gedeeld** in **Beëindigd** te wijzigen, maakt u de versie beschikbaar voor verwijdering.</span><span class="sxs-lookup"><span data-stu-id="07de3-129">By changing the status of the selected version from **Shared** to **Discontinued**, you make the version available for deletion.</span></span>

5. <span data-ttu-id="07de3-130">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="07de3-130">Select **OK**.</span></span>
6. <span data-ttu-id="07de3-131">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="07de3-131">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="07de3-132">Selecteer voor dit voorbeeld de versie van de configuratie die de status **Beëindigd** heeft.</span><span class="sxs-lookup"><span data-stu-id="07de3-132">For this example, select the version of the configuration that has a status of **Discontinued**.</span></span>

7. <span data-ttu-id="07de3-133">Selecteer **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="07de3-133">Select **Delete**.</span></span>
8. <span data-ttu-id="07de3-134">Selecteer **Ja**.</span><span class="sxs-lookup"><span data-stu-id="07de3-134">Select **Yes**.</span></span>

    <span data-ttu-id="07de3-135">De enige conceptversie 2 van de geselecteerde gegevensmodelconfiguratie is nu beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="07de3-135">Notice that the only draft version 2 of the selected data model configuration is now available.</span></span>

9. <span data-ttu-id="07de3-136">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="07de3-136">Close the page.</span></span>

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a><span data-ttu-id="07de3-137">Een gedeelde versie van een gegevensmodelconfiguratie importeren vanuit LCS</span><span class="sxs-lookup"><span data-stu-id="07de3-137">Import a shared version of a data model configuration from LCS</span></span>

1. <span data-ttu-id="07de3-138">Ga naar **Organisatiebeheer \> Werkgebieden \> Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="07de3-138">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="07de3-139">Selecteer in de sectie **Configuratieproviders** de tegel **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="07de3-139">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="07de3-140">Klik op de tegel **Litware, Inc.** op **Opslagplaatsen**.</span><span class="sxs-lookup"><span data-stu-id="07de3-140">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="07de3-141">U kunt nu de lijst met opslagplaatsen voor de configuratieprovider Litware, Inc. openen.</span><span class="sxs-lookup"><span data-stu-id="07de3-141">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="07de3-142">Selecteer **Openen**.</span><span class="sxs-lookup"><span data-stu-id="07de3-142">Select **Open**.</span></span>

    <span data-ttu-id="07de3-143">Selecteer voor dit voorbeeld de opslaglocatierecord **LCS** en open deze.</span><span class="sxs-lookup"><span data-stu-id="07de3-143">For this example, select the **LCS** repository, and open it.</span></span> <span data-ttu-id="07de3-144">U moet [toegang](#accessconditions) hebben tot het LCS-project en de activabibliotheek die wordt geopend door de geselecteerde ER-opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="07de3-144">You must have [access](#accessconditions) to the LCS project and to the Asset library that is accessed by the selected ER repository.</span></span>

5. <span data-ttu-id="07de3-145">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="07de3-145">In the list, mark the selected row.</span></span>

    <span data-ttu-id="07de3-146">Selecteer de eerste versie van **Voorbeeldmodelconfiguratie** in de lijst met versies.</span><span class="sxs-lookup"><span data-stu-id="07de3-146">For this example, select the first version of **Sample model configuration** in the version list.</span></span>

6. <span data-ttu-id="07de3-147">Selecteer **Importeren**.</span><span class="sxs-lookup"><span data-stu-id="07de3-147">Select **Import**.</span></span>
7. <span data-ttu-id="07de3-148">Selecteer **Ja** om de import van de geselecteerde versie van LCS te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="07de3-148">Select **Yes** to confirm the import of the selected version from LCS.</span></span>

    <span data-ttu-id="07de3-149">Een informatief bericht bevestigt dat de geselecteerde versie is geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="07de3-149">An informational message confirms that the selected version was successfully imported.</span></span>

8. <span data-ttu-id="07de3-150">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="07de3-150">Close the page.</span></span>
9. <span data-ttu-id="07de3-151">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="07de3-151">Close the page.</span></span>
10. <span data-ttu-id="07de3-152">Selecteer **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="07de3-152">Select **Configurations**.</span></span>
11. <span data-ttu-id="07de3-153">Selecteer **Voorbeeldmodelconfiguratie** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="07de3-153">In the tree, select **Sample model configuration**.</span></span>
12. <span data-ttu-id="07de3-154">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="07de3-154">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="07de3-155">Selecteer voor dit voorbeeld de versie van de configuratie die de status **Gedeeld** heeft.</span><span class="sxs-lookup"><span data-stu-id="07de3-155">For this example, select the version of the configuration that has a status of **Shared**.</span></span>

    <span data-ttu-id="07de3-156">De gedeelde versie 1 van de geselecteerde gegevensmodelconfiguratie is nu ook beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="07de3-156">Notice that shared version 1 of the selected data model configuration is also available now.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
