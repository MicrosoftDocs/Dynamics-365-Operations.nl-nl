---
title: Bijgewerkte versies van ER-configuraties importeren
description: In dit onderwerp wordt uitgelegd hoe u ER-configuraties (Electronic Reporting) importeert uit de algemene opslagplaats van de configuratieservice.
author: NickSelin
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 724048991fc8864ef72a5155af66b9c709f4b875
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893951"
---
# <a name="import-updated-versions-of-er-configurations"></a><span data-ttu-id="cb2f3-103">Bijgewerkte versies van ER-configuraties importeren</span><span class="sxs-lookup"><span data-stu-id="cb2f3-103">Import updated versions of ER configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb2f3-104">Om [ER-configuraties](general-electronic-reporting.md#Configuration) (Electronic Reporting) te delen, wordt gebruik gemaakt van [ER-opslagplaatsen](general-electronic-reporting.md#Repository).</span><span class="sxs-lookup"><span data-stu-id="cb2f3-104">Electronic reporting (ER) [repositories](general-electronic-reporting.md#Repository) are used to share [ER configurations](general-electronic-reporting.md#Configuration).</span></span> <span data-ttu-id="cb2f3-105">U kunt configuraties vanuit verschillende opslagplaatsen [importeren](download-electronic-reporting-configuration-lcs.md) in uw exemplaar van Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-105">You can [import](download-electronic-reporting-configuration-lcs.md) ER configurations from different repositories into your instance of Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="cb2f3-106">Wanneer u configuraties importeert, kunnen [configuratie providers](general-electronic-reporting.md#Provider) nieuwe [versies](general-electronic-reporting.md#component-versioning) van opslagplaatsen publiceren zodat deze kunnen worden gedeeld.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-106">When you import ER configurations, [configuration providers](general-electronic-reporting.md#Provider) can publish new [versions](general-electronic-reporting.md#component-versioning) repositories so that they can be shared.</span></span>

<span data-ttu-id="cb2f3-107">In dit onderwerp wordt uitgelegd hoe u ER-configuraties importeert uit de algemene opslagplaats van de configuratieservice.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-107">This topic explains how to import updated versions of ER configurations from the Global repository of the Configuration service.</span></span> <span data-ttu-id="cb2f3-108">Zie [Microsoft Dynamics 365 for Finance and Operations - Regulatory services, configuratieservice](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-108">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="review-the-available-updated-versions"></a><span data-ttu-id="cb2f3-109">Controleren welke bijgewerkte versies beschikbaar zijn</span><span class="sxs-lookup"><span data-stu-id="cb2f3-109">Review the available updated versions</span></span>

1. <span data-ttu-id="cb2f3-110">Meld u aan bij Finance met een van de volgende rollen:</span><span class="sxs-lookup"><span data-stu-id="cb2f3-110">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="cb2f3-111">Ontwikkelaar elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="cb2f3-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="cb2f3-112">Functioneel consultant elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="cb2f3-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="cb2f3-113">Systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="cb2f3-113">System administrator</span></span>

2. <span data-ttu-id="cb2f3-114">Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-114">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="cb2f3-115">Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Verwante koppelingen** de tegel **Versie-updates van configuraties importeren**.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-115">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>

    ![Pagina Lokalisatieconfiguraties](./media/er-download-updated-versions-global-repo1.png)

4. <span data-ttu-id="cb2f3-117">Selecteer in het dialoogvenster **Versie-updates van ER-configuraties importeren** in het veld **Uitvoeringsmodus** de optie **Alleen beschikbare updates weergeven**.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-117">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Only show available updates**.</span></span> <span data-ttu-id="cb2f3-118">Selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-118">Then select **OK**.</span></span> 

    ![Veld voor uitvoeringsmodus ingesteld op Alleen beschikbare updates weergeven](./media/er-download-updated-versions-global-repo2.png)

5. <span data-ttu-id="cb2f3-120">Controleer de meldingen die u krijgt.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-120">Review the messages that you receive.</span></span> <span data-ttu-id="cb2f3-121">Deze meldingen leveren de volgende informatie over de ER-configuraties in het huidige Finance-exemplaar en hoe deze overeenkomen met of afwijken van de inhoud van de algemene opslagplaats:</span><span class="sxs-lookup"><span data-stu-id="cb2f3-121">These messages provide the following information about the ER configurations in the current Finance instance and how they compare to the content of the Global repository:</span></span>

    - <span data-ttu-id="cb2f3-122">Het totale aantal ER-configuraties</span><span class="sxs-lookup"><span data-stu-id="cb2f3-122">The total number of ER configurations</span></span>
    - <span data-ttu-id="cb2f3-123">ER-configuraties die niet aanwezig zijn in de globale opslagplaats</span><span class="sxs-lookup"><span data-stu-id="cb2f3-123">ER configurations that aren't present in the Global repository</span></span>
    - <span data-ttu-id="cb2f3-124">ER-configuraties waarvoor de meest recente versie al beschikbaar is in het huidige Finance-exemplaar (om de volledige lijst met deze ER-configuraties weer te geven, selecteert u de koppeling **Berichtdetails**).</span><span class="sxs-lookup"><span data-stu-id="cb2f3-124">ER configurations for which the latest version is already available in the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        ![Bericht "De meest recente versies van de volgende configuraties zijn al geïmporteerd" en berichtdetails](./media/er-download-updated-versions-global-repo3.png)

    - <span data-ttu-id="cb2f3-126">ER-configuraties waarvoor de meest recente versie beschikbaar is in de algemene opslagplaats en geïmporteerd kan worden in het huidige Finance-exemplaar (om de volledige lijst met deze ER-configuraties weer te geven, selecteert u de koppeling **Berichtdetails**).</span><span class="sxs-lookup"><span data-stu-id="cb2f3-126">ER configurations for which the latest version is available in the Global repository and can be imported into the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        ![Bericht "Updates beschikbaar" en berichtdetails](./media/er-download-updated-versions-global-repo4.png)

## <a name="import-available-updated-versions"></a><span data-ttu-id="cb2f3-128">Beschikbare bijgewerkte versies importeren</span><span class="sxs-lookup"><span data-stu-id="cb2f3-128">Import available updated versions</span></span>

1. <span data-ttu-id="cb2f3-129">Meld u aan bij Finance met een van de volgende rollen:</span><span class="sxs-lookup"><span data-stu-id="cb2f3-129">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="cb2f3-130">Ontwikkelaar elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="cb2f3-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="cb2f3-131">Functioneel consultant elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="cb2f3-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="cb2f3-132">Systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="cb2f3-132">System administrator</span></span>

2. <span data-ttu-id="cb2f3-133">Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-133">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="cb2f3-134">Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Verwante koppelingen** de tegel **Versie-updates van configuraties importeren**.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-134">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>
4. <span data-ttu-id="cb2f3-135">Selecteer in het dialoogvenster **Versie-updates voor ER-configuraties importeren** in het veld **Uitvoeringsmodus** de optie **Meest recente updates importeren** om de meest recente versies van ER-configuraties te importeren vanuit de globale opslagplaats in het huidige Finance-exemplaar.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-135">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Import latest updates** to import the latest versions of ER configurations from the Global repository into the current Finance instance.</span></span>
5. <span data-ttu-id="cb2f3-136">Als u een batchtaak voor de import wilt plannen, stelt u op het sneltabblad **Uitvoeren in de achtergrond** de optie **Batchverwerking** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-136">To schedule a batch job for the import, on the **Run in the background** FastTab, set the **Batch processing** option to **Yes**.</span></span> <span data-ttu-id="cb2f3-137">Als u de import regelmatig wilt herhalen, configureert u het vereiste herhalingspatroon.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-137">If you want to repeat the import periodically, configure the required recurrence.</span></span>

    ![Veld Uitvoeringsmodus ingesteld op Meest recente updates importeren](./media/er-download-updated-versions-global-repo5.png)

6. <span data-ttu-id="cb2f3-139">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-139">Select **OK**.</span></span>
7. <span data-ttu-id="cb2f3-140">Als u wilt weten welke configuratieversies zijn geïmporteerd, voert u een van de volgende stappen uit:</span><span class="sxs-lookup"><span data-stu-id="cb2f3-140">To learn what configuration versions have been imported, follow one of these steps:</span></span>

    - <span data-ttu-id="cb2f3-141">Als u de importfunctie interactief uitvoert in plaats van een batchtaak te gebruiken, controleert u de meldingen die u ontvangt.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-141">If you run the import interactively instead of using a batch job, review the messages that you receive.</span></span>

        ![Meldingen die zijn ontvangen tijdens een interactieve importbewerking](./media/er-download-updated-versions-global-repo6.png)

    - <span data-ttu-id="cb2f3-143">Als u de import uitvoert in de batchmodus, volgt u deze stappen:</span><span class="sxs-lookup"><span data-stu-id="cb2f3-143">If you run the import in batch mode, follow these steps:</span></span>

        1. <span data-ttu-id="cb2f3-144">Ga naar **Algemeen** \> **Query's** \> **Batchtaken** \> **Mijn batchtaken**.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-144">Go to **Common** \> **Inquiries** \> **Batch jobs** \> **My batch jobs**.</span></span>
        2. <span data-ttu-id="cb2f3-145">Zoek en selecteer de taak **Versie-updates van ER-configuraties importeren** en selecteer vervolgens in het actievenster op het tabblad **Batchtaak** de optie **Batchtaakhistorie** om de taakhistorie weer te geven.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-145">Find and select the **Import electronic reporting configurations versions updates** job, and then, on the Action Pane, on the **Batch job** tab, select **Batch job history** to view the job history.</span></span>
        3. <span data-ttu-id="cb2f3-146">Selecteer op de pagina **Batchtaakhistorie** de optie **Logboek**.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-146">On the **Batch job history** page, select **Log**.</span></span> <span data-ttu-id="cb2f3-147">Selecteer vervolgens in de melding die u ontvangt de koppeling **Berichtdetails** om het taaklogboek weer te geven.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-147">Then, in the message that you receive, select the **Message details** link to view the job log.</span></span>

        ![Taaklogboek](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> <span data-ttu-id="cb2f3-149">Het wordt niet aangeraden een terugkerende batch taak te plannen om bijgewerkte versies van de ER-configuraties rechtstreeks vanuit de globale opslagplaats te importeren in een productieomgeving, omdat de geïmporteerde versies meteen beschikbaar zijn voor gebruik.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-149">We don't recommend that you schedule a recurring batch job to import updated versions of ER configurations directly from the Global repository into a production environment, because the imported versions will immediately be available for use.</span></span> <span data-ttu-id="cb2f3-150">Gebruik in plaats daarvan deze aanpak om versies van ER-configuraties te implementeren in een sandbox-omgeving.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-150">Instead, use this approach to deploy versions of ER configurations to a sandbox environment.</span></span> <span data-ttu-id="cb2f3-151">Ze kunnen vervolgens worden geëvalueerd in de sandbox-omgeving, voordat u ze naar een productie omgeving distribueert.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-151">They can then be evaluated in the sandbox environment before they are deployed to a production environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cb2f3-152">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="cb2f3-152">Additional resources</span></span>

- [<span data-ttu-id="cb2f3-153">Overzicht van elektronische rapportage (ER)</span><span class="sxs-lookup"><span data-stu-id="cb2f3-153">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="cb2f3-154">ER-configuraties downloaden uit de algemene opslagplaats van de configuratieservice</span><span class="sxs-lookup"><span data-stu-id="cb2f3-154">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]