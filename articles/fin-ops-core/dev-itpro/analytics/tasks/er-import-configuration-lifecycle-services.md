---
title: Een configuratie vanuit Lifecycle Services importeren
description: In dit onderwerp wordt beschreven hoe u een nieuwe versie van een ER-configuratie (Electronic Reporting) importeert vanuit Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
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
ms.openlocfilehash: 636ed27c157c8322cc1be4ca8eca10ef37eb8bbc
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569504"
---
# <a name="import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="822b1-103">Een configuratie vanuit Lifecycle Services importeren</span><span class="sxs-lookup"><span data-stu-id="822b1-103">Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="822b1-104">In dit onderwerp wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe versie van een [configuratie voor elektronische rapportage (ER)](../general-electronic-reporting.md#Configuration) vanuit de [activabibliotheek op projectniveau](../../lifecycle-services/asset-library.md) kan importeren in Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="822b1-104">This topic explains how a user in the System administrator or Electronic reporting developer role can import a new version of an [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) from the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="822b1-105">In dit voorbeeld selecteert u de gewenste versie van de ER-configuratie en importeert u deze voor het voorbeeldbedrijf, Litware, Inc. Deze stappen kunnen in elk bedrijf worden uitgevoerd aangezien ER-configuraties tussen bedrijven worden gedeeld.</span><span class="sxs-lookup"><span data-stu-id="822b1-105">In this example, you will select the desired version of the ER configuration and import it for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="822b1-106">Als u deze stappen wilt uitvoeren, moet u eerst de stappen in [Een configuratie in Lifecycle Services uploaden](er-upload-configuration-into-lifecycle-services.md) voltooien.</span><span class="sxs-lookup"><span data-stu-id="822b1-106">To complete these steps, you must first complete the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="822b1-107">Ook is toegang tot LCS vereist.</span><span class="sxs-lookup"><span data-stu-id="822b1-107">Access to LCS is also required.</span></span>

1. <span data-ttu-id="822b1-108">Meld u aan bij de toepassing met een van de volgende rollen:</span><span class="sxs-lookup"><span data-stu-id="822b1-108">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="822b1-109">Ontwikkelaar elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="822b1-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="822b1-110">Systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="822b1-110">System administrator</span></span>

2. <span data-ttu-id="822b1-111">Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="822b1-111">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="822b1-112">Selecteer **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="822b1-112">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="822b1-113">Zorg ervoor dat de huidige Dynamics 365 Finance-gebruiker lid is van het LCS-project dat de activabibliotheek bevat waartoe de gebruiker [toegang](../../lifecycle-services/asset-library.md#asset-library-support) wil hebben voor het importeren van ER-configuraties.</span><span class="sxs-lookup"><span data-stu-id="822b1-113">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the Asset library that the user wants to [access](../../lifecycle-services/asset-library.md#asset-library-support) to import ER configurations.</span></span>
>
> <span data-ttu-id="822b1-114">U hebt geen toegang tot een LCS-project vanuit een ER-opslagplaats voor een ander domein dan het domein dat in Finance wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="822b1-114">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="822b1-115">Als u het probeert, wordt een lege lijst met LCS-projecten weergegeven en kunt u geen ER-configuraties importeren uit de activabibliotheek op projectniveau in LCS.</span><span class="sxs-lookup"><span data-stu-id="822b1-115">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="822b1-116">Als u activabibliotheken op projectniveau wilt openen vanuit een ER-opslagplaats die wordt gebruikt voor het importeren van ER-configuraties, meldt u zich aan bij Finance met de referenties van een gebruiker die hoort bij de tenant (domein) waarvoor het huidige Finance-exemplaar is ingericht.</span><span class="sxs-lookup"><span data-stu-id="822b1-116">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a><span data-ttu-id="822b1-117">Een gedeelde versie van een gegevensmodelconfiguratie verwijderen</span><span class="sxs-lookup"><span data-stu-id="822b1-117">Delete a shared version of a data model configuration</span></span>

1. <span data-ttu-id="822b1-118">Selecteer op de pagina **Configuraties** in de configuratiestructuur het item **Voorbeeldmodelconfiguratie**.</span><span class="sxs-lookup"><span data-stu-id="822b1-118">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="822b1-119">U hebt de eerste versie van een voorbeeldgegevensmodelconfiguratie gemaakt en gepubliceerd naar LCS tijdens de procedure in [Een configuratie in Lifecycle Services uploaden](er-upload-configuration-into-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="822b1-119">You created the first version of a sample data model configuration and published it to LCS when you completed the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="822b1-120">In deze procedure verwijdert u deze versie van de ER-configuratie.</span><span class="sxs-lookup"><span data-stu-id="822b1-120">In this procedure, you will delete that version of the ER configuration.</span></span> <span data-ttu-id="822b1-121">Vervolgens importeert u die versie uit LCS verderop in dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="822b1-121">You will then import that version from LCS later in this topic.</span></span>

2. <span data-ttu-id="822b1-122">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="822b1-122">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="822b1-123">Selecteer voor dit voorbeeld de versie van de configuratie die de status **Gedeeld** heeft.</span><span class="sxs-lookup"><span data-stu-id="822b1-123">For this example, select the version of the configuration that has a status of **Shared**.</span></span> <span data-ttu-id="822b1-124">Deze status geeft aan dat de configuratie is gepubliceerd naar LCS.</span><span class="sxs-lookup"><span data-stu-id="822b1-124">This status indicates that the configuration has been published to LCS.</span></span>

3. <span data-ttu-id="822b1-125">Selecteer **Status wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="822b1-125">Select **Change status**.</span></span>
4. <span data-ttu-id="822b1-126">Selecteer **Beëindigen**.</span><span class="sxs-lookup"><span data-stu-id="822b1-126">Select **Discontinue**.</span></span>

    <span data-ttu-id="822b1-127">Door de status van de geselecteerde versie van **Gedeeld** in **Beëindigd** te wijzigen, maakt u de versie beschikbaar voor verwijdering.</span><span class="sxs-lookup"><span data-stu-id="822b1-127">By changing the status of the selected version from **Shared** to **Discontinued**, you make the version available for deletion.</span></span>

5. <span data-ttu-id="822b1-128">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="822b1-128">Select **OK**.</span></span>
6. <span data-ttu-id="822b1-129">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="822b1-129">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="822b1-130">Selecteer voor dit voorbeeld de versie van de configuratie die de status **Beëindigd** heeft.</span><span class="sxs-lookup"><span data-stu-id="822b1-130">For this example, select the version of the configuration that has a status of **Discontinued**.</span></span>

7. <span data-ttu-id="822b1-131">Selecteer **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="822b1-131">Select **Delete**.</span></span>
8. <span data-ttu-id="822b1-132">Selecteer **Ja**.</span><span class="sxs-lookup"><span data-stu-id="822b1-132">Select **Yes**.</span></span>

    <span data-ttu-id="822b1-133">De enige conceptversie 2 van de geselecteerde gegevensmodelconfiguratie is nu beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="822b1-133">Notice that the only draft version 2 of the selected data model configuration is now available.</span></span>

9. <span data-ttu-id="822b1-134">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="822b1-134">Close the page.</span></span>

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a><span data-ttu-id="822b1-135">Een gedeelde versie van een gegevensmodelconfiguratie importeren vanuit LCS</span><span class="sxs-lookup"><span data-stu-id="822b1-135">Import a shared version of a data model configuration from LCS</span></span>

1. <span data-ttu-id="822b1-136">Ga naar **Organisatiebeheer \> Werkgebieden \> Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="822b1-136">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="822b1-137">Selecteer in de sectie **Configuratieproviders** de tegel **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="822b1-137">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="822b1-138">Klik op de tegel **Litware, Inc.** op **Opslagplaatsen**.</span><span class="sxs-lookup"><span data-stu-id="822b1-138">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="822b1-139">U kunt nu de lijst met opslagplaatsen voor de configuratieprovider Litware, Inc. openen.</span><span class="sxs-lookup"><span data-stu-id="822b1-139">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="822b1-140">Selecteer **Openen**.</span><span class="sxs-lookup"><span data-stu-id="822b1-140">Select **Open**.</span></span>

    <span data-ttu-id="822b1-141">Selecteer voor dit voorbeeld de opslaglocatierecord **LCS** en open deze.</span><span class="sxs-lookup"><span data-stu-id="822b1-141">For this example, select the **LCS** repository, and open it.</span></span> <span data-ttu-id="822b1-142">U moet [toegang](#accessconditions) hebben tot het LCS-project en de activabibliotheek die wordt geopend door de geselecteerde ER-opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="822b1-142">You must have [access](#accessconditions) to the LCS project and to the Asset library that is accessed by the selected ER repository.</span></span>

5. <span data-ttu-id="822b1-143">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="822b1-143">In the list, mark the selected row.</span></span>

    <span data-ttu-id="822b1-144">Selecteer de eerste versie van **Voorbeeldmodelconfiguratie** in de lijst met versies.</span><span class="sxs-lookup"><span data-stu-id="822b1-144">For this example, select the first version of **Sample model configuration** in the version list.</span></span>

6. <span data-ttu-id="822b1-145">Selecteer **Importeren**.</span><span class="sxs-lookup"><span data-stu-id="822b1-145">Select **Import**.</span></span>
7. <span data-ttu-id="822b1-146">Selecteer **Ja** om de import van de geselecteerde versie van LCS te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="822b1-146">Select **Yes** to confirm the import of the selected version from LCS.</span></span>

    <span data-ttu-id="822b1-147">Een informatief bericht bevestigt dat de geselecteerde versie is geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="822b1-147">An informational message confirms that the selected version was successfully imported.</span></span>

8. <span data-ttu-id="822b1-148">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="822b1-148">Close the page.</span></span>
9. <span data-ttu-id="822b1-149">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="822b1-149">Close the page.</span></span>
10. <span data-ttu-id="822b1-150">Selecteer **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="822b1-150">Select **Configurations**.</span></span>
11. <span data-ttu-id="822b1-151">Selecteer **Voorbeeldmodelconfiguratie** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="822b1-151">In the tree, select **Sample model configuration**.</span></span>
12. <span data-ttu-id="822b1-152">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="822b1-152">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="822b1-153">Selecteer voor dit voorbeeld de versie van de configuratie die de status **Gedeeld** heeft.</span><span class="sxs-lookup"><span data-stu-id="822b1-153">For this example, select the version of the configuration that has a status of **Shared**.</span></span>

    <span data-ttu-id="822b1-154">De gedeelde versie 1 van de geselecteerde gegevensmodelconfiguratie is nu ook beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="822b1-154">Notice that shared version 1 of the selected data model configuration is also available now.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]