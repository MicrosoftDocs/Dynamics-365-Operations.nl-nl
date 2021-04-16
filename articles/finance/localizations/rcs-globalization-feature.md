---
title: Regulatory Configuration Services (RCS) - Globalisatiefuncties
description: In dit onderwerp wordt uitgelegd hoe u Microsoft Regulatory Configuration Services (RCS) en de algemene opslagplaats kunt gebruiken om globalisatiefuncties te maken en te gebruiken.
author: JaneA07
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, RCSWorkspace, e-Invoicing service
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: cbb1d9a53a7a09ab525532f08553898c4e40223a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822776"
---
# <a name="regulatory-configuration-services-rcs---globalization-features"></a><span data-ttu-id="d33ca-103">Regulatory Configuration Services (RCS) - Globalisatiefuncties</span><span class="sxs-lookup"><span data-stu-id="d33ca-103">Regulatory Configuration Services (RCS) - Globalization features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d33ca-104">U kunt Microsoft Regulatory Configuration Services (RCS) gebruiken om een globalisatiefunctie te maken die kan worden gebruikt in globalisatieservices, zoals een service voor e-facturen.</span><span class="sxs-lookup"><span data-stu-id="d33ca-104">You can use Microsoft Regulatory Configuration Services (RCS) to create a Globalization feature that can be used in Globalization services, such as an e-invoicing service.</span></span> <span data-ttu-id="d33ca-105">Met RCS kunt u de volgende taken uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="d33ca-105">RCS lets you perform these tasks:</span></span>

- <span data-ttu-id="d33ca-106">Verwante onderdelen van een functie definiëren.</span><span class="sxs-lookup"><span data-stu-id="d33ca-106">Define related components of a feature.</span></span>
- <span data-ttu-id="d33ca-107">De functielevenscyclus beheren via de status van een functie.</span><span class="sxs-lookup"><span data-stu-id="d33ca-107">Manage the feature lifecycle through a feature's status.</span></span>
- <span data-ttu-id="d33ca-108">Een functie beschikbaar maken voor gedefinieerde omgevingen.</span><span class="sxs-lookup"><span data-stu-id="d33ca-108">Make a feature available for defined environments.</span></span>
- <span data-ttu-id="d33ca-109">Een functie delen met andere organisaties.</span><span class="sxs-lookup"><span data-stu-id="d33ca-109">Share a feature with other organizations.</span></span>

<span data-ttu-id="d33ca-110">In de volgende procedures wordt uitgelegd hoe een gebruiker in RCS een globalisatiefunctie en verwante onderdelen kan toevoegen, de status van de functie kan bijwerken en de functie beschikbaar kan maken zodat deze kan worden gebruikt in globalisatieservices.</span><span class="sxs-lookup"><span data-stu-id="d33ca-110">The following procedures explain how a user in RCS can add a Globalization feature and related components, update the feature's status, and make the feature available so that it can be used in Globalization services.</span></span>

<span data-ttu-id="d33ca-111">Voordat u de procedures uitvoert, moet u de stappen uitvoeren die betrekking hebben op de volgende taken:</span><span class="sxs-lookup"><span data-stu-id="d33ca-111">Before you complete the procedures, you must complete the steps that are related to the following tasks:</span></span>

- <span data-ttu-id="d33ca-112">Een RCS-exemplaar openen.</span><span class="sxs-lookup"><span data-stu-id="d33ca-112">Accessing an RCS instance.</span></span>
- <span data-ttu-id="d33ca-113">Een configuratieprovider maken en activeren.</span><span class="sxs-lookup"><span data-stu-id="d33ca-113">Creating and activating a configuration provider.</span></span> <span data-ttu-id="d33ca-114">Zie [Configuratieproviders maken en deze als actief markeren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d33ca-114">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="d33ca-115">Voer de volgende stappen uit in uw exemplaar van Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="d33ca-115">In your Finance and Operations apps instance, follow these steps.</span></span>

1. <span data-ttu-id="d33ca-116">Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="d33ca-116">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="d33ca-117">Als er geen RCS-omgeving is ingericht voor uw bedrijf, selecteert u **Regulatory services ‑ Configuratie** en volgt u de instructies om een RCS-omgeving in te richten.</span><span class="sxs-lookup"><span data-stu-id="d33ca-117">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration**, and follow the instructions to provision one.</span></span>

> [!NOTE]
> <span data-ttu-id="d33ca-118">Als er al een RCS-omgeving is ingericht voor uw bedrijf, gebruikt u de pagina-URL om deze te openen door de aanmeldingsoptie te selecteren.</span><span class="sxs-lookup"><span data-stu-id="d33ca-118">If an RCS environment has already been provisioned for your company, use the page URL to access the environment by selecting the sign-in option.</span></span>

## <a name="turn-on-the-globalization-features"></a><span data-ttu-id="d33ca-119">De globalisatiefuncties inschakelen</span><span class="sxs-lookup"><span data-stu-id="d33ca-119">Turn on the Globalization features</span></span>

1. <span data-ttu-id="d33ca-120">Selecteer de tegel **Functiebeheer** in uw RCS-exemplaar.</span><span class="sxs-lookup"><span data-stu-id="d33ca-120">In your RCS instance, select the **Feature management** tile.</span></span>
2. <span data-ttu-id="d33ca-121">Selecteer in het werkgebied **Functiebeheer** de optie **Globalisatiefuncties** in de lijst en selecteer **Nu inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="d33ca-121">In the **Feature management** workspace, select **Globalization features** in the list, and then select **Enable now**.</span></span>

    ![Globalisatiefuncties in Functiebeheer](./media/RCS_GlobalF_1%20Feature%20mgmt.JPG)

## <a name="globalization-features"></a><span data-ttu-id="d33ca-123">Globalisatiefuncties</span><span class="sxs-lookup"><span data-stu-id="d33ca-123">Globalization features</span></span>

<span data-ttu-id="d33ca-124">Als u een globalisatiefunctie wilt gebruiken, moet u deze eerst vanuit de globale opslagplaats importeren en uw eigen versie maken.</span><span class="sxs-lookup"><span data-stu-id="d33ca-124">To use a Globalization feature, you must first import it from the the Global repository and create your own version of it.</span></span> <span data-ttu-id="d33ca-125">Er zijn twee manieren om globalisatiefuncties toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="d33ca-125">There are two ways to add Globalization features:</span></span>

- <span data-ttu-id="d33ca-126">Voeg een afgeleide functie toe die is gebaseerd op een bestaande functie die is gepubliceerd of gedeeld.</span><span class="sxs-lookup"><span data-stu-id="d33ca-126">Add a derived feature that is based on an existing feature that has been published or shared.</span></span>
- <span data-ttu-id="d33ca-127">Voeg een nieuwe functie toe die u geheel zelf hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d33ca-127">Add a new feature that you've created from scratch.</span></span>

## <a name="access-globalization-features"></a><span data-ttu-id="d33ca-128">Globalisatiefuncties openen</span><span class="sxs-lookup"><span data-stu-id="d33ca-128">Access Globalization features</span></span>

1. <span data-ttu-id="d33ca-129">Zorg dat de functie **Globalisatiefuncties** is ingeschakeld in Functiebeheer, zoals eerder in dit onderwerp wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="d33ca-129">Make sure that the **Globalization features** feature is turned on in Feature management, as described earlier in this topic.</span></span>
2. <span data-ttu-id="d33ca-130">Open het nieuwe werkgebied **Globalisatiefuncties** en selecteer vervolgens onder **Functies** de tegel **E-facturering**.</span><span class="sxs-lookup"><span data-stu-id="d33ca-130">Open the new **Globalization Features** workspace, and then, under **Features**, select the **e-Invoicing** tile.</span></span>

    ![Werkgebied Globale functies](./media/RCS_GlobalF_2%20Feature%20wrkspace.JPG)

    <span data-ttu-id="d33ca-132">De pagina **Functies voor e-Facturering** wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="d33ca-132">The **e-Invoicing Features** page is opened.</span></span>

    ![De pagina Functies voor e-Facturering](./media/RCS_GlobalF_3%20Feature%20form.JPG)

## <a name="add-a-derived-globalization-feature"></a><span data-ttu-id="d33ca-134">Een afgeleide globalisatiefunctie toevoegen</span><span class="sxs-lookup"><span data-stu-id="d33ca-134">Add a derived Globalization feature</span></span>

<span data-ttu-id="d33ca-135">U kunt een nieuwe globalisatiefunctie toevoegen door deze af te leiden van een bestaande functie die is gepubliceerd of gedeeld.</span><span class="sxs-lookup"><span data-stu-id="d33ca-135">You can add a new Globalization feature by deriving it from an existing feature that has been published or shared.</span></span>

1. <span data-ttu-id="d33ca-136">Selecteer **Importeren** om de pagina **Functie importeren uit algemene opslagplaats** te openen.</span><span class="sxs-lookup"><span data-stu-id="d33ca-136">Select **Import** to open the **Import feature from Global repository** page.</span></span>

    ![De pagina Functie importeren uit algemene opslagplaats](./media/RCS_GlobalF_4%20Feature%20import%20form%20GR.JPG)

2. <span data-ttu-id="d33ca-138">Selecteer **Synchroniseren** om de nieuwste functies te downloaden.</span><span class="sxs-lookup"><span data-stu-id="d33ca-138">Select **Synchronize** to get the latest features.</span></span>

    <span data-ttu-id="d33ca-139">De gesynchroniseerde lijst bevat functies die beschikbaar zijn voor u, omdat deze door Microsoft zijn gepubliceerd of omdat ze door een andere configuratieprovider met u zijn gedeeld.</span><span class="sxs-lookup"><span data-stu-id="d33ca-139">The synced list includes features that are available to you either because they were published by Microsoft or because they were shared with you by another configuration provider.</span></span>

    ![Gesynchroniseerde lijst met functies](./media/RCS_GlobalF_5%20Feature%20GR%20sync.JPG)

3. <span data-ttu-id="d33ca-141">Selecteer in de lijst de functies die u wilt importeren en selecteer **Importeren**.</span><span class="sxs-lookup"><span data-stu-id="d33ca-141">In the list, select the features to import, and then select **Import**.</span></span> <span data-ttu-id="d33ca-142">U ontvangt een bericht wanneer de geselecteerde functies zijn geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="d33ca-142">You receive a message when the selected features have been successfully imported.</span></span>

    ![Bericht over geslaagde import](./media/RCS_GlobalF_6%20Feature%20GR%20import%20success.JPG)

4. <span data-ttu-id="d33ca-144">Selecteer **Toevoegen** en selecteer vervolgens in het dialoogvenster met vervolgkeuzemenu de optie **Op basis van bestaande versie**.</span><span class="sxs-lookup"><span data-stu-id="d33ca-144">Select **Add**, and then, in the drop-down dialog box, select the **Based on existing version** option.</span></span>
5. <span data-ttu-id="d33ca-145">Voer een naam en beschrijving voor de functie in.</span><span class="sxs-lookup"><span data-stu-id="d33ca-145">Enter a name and description for the feature.</span></span>
6. <span data-ttu-id="d33ca-146">Selecteer de basisversie van de functie in de lijst met beschikbare functies en selecteer vervolgens **Functie maken**.</span><span class="sxs-lookup"><span data-stu-id="d33ca-146">In the list of available features, select the base version of the feature, and then select **Create feature**.</span></span>

    ![Een afgeleide functie toevoegen](./media/RCS_GlobalF_7%20Feature%20create%20derived.JPG)

    <span data-ttu-id="d33ca-148">De functie die u hebt toegevoegd, wordt gemaakt met de status **Concept**.</span><span class="sxs-lookup"><span data-stu-id="d33ca-148">The feature that you added is created and has a status of **Draft**.</span></span>

    ![Afgeleide functie met status Concept](./media/RCS_GlobalF_8%20Feature%20draft%20create.JPG)

7. <span data-ttu-id="d33ca-150">Controleer de functieonderdelen om te bepalen of er updates nodig zijn:</span><span class="sxs-lookup"><span data-stu-id="d33ca-150">Review the feature components to determine whether updates are required:</span></span>

    - <span data-ttu-id="d33ca-151">Bekijk de configuraties voor het geval u de ER-indelingen (Elektronische rapportage) en hun binding met indelingstoewijzingen voor de functieversie wilt aanpassen.</span><span class="sxs-lookup"><span data-stu-id="d33ca-151">Review the configurations, in case you need to customize the Electronic reporting (ER) formats and their binding with format mappings for the feature version.</span></span>
    - <span data-ttu-id="d33ca-152">Controleer de instellingen voor het geval u het tabblad **Acties**, **Toepasbaarheidregels** of **Variabelen** voor de functieversie wilt aanpassen.</span><span class="sxs-lookup"><span data-stu-id="d33ca-152">Review the setup, in case you need to customize the **Actions** tab, **Applicability rules** tab, or **Variables** tab for the feature version.</span></span>

8. <span data-ttu-id="d33ca-153">Selecteer op het tabblad **Versies** een **ingangsdatum** en voer een omschrijving in als het veld **Omschrijving** leeg is.</span><span class="sxs-lookup"><span data-stu-id="d33ca-153">On the **Versions** tab, select an **Effective from** date, and enter a description if the **Description** field is blank.</span></span>
9. <span data-ttu-id="d33ca-154">Selecteer **Status wijzigen** om de functie te voltooien.</span><span class="sxs-lookup"><span data-stu-id="d33ca-154">Select **Change status** to complete the feature.</span></span> <span data-ttu-id="d33ca-155">Voltooide functies kunnen voor een specifieke omgeving beschikbaar worden gemaakt, zodat deze kunnen worden gebruikt in globalisatieservices, of kunnen worden gepubliceerd naar de algemene opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="d33ca-155">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="d33ca-156">Functies waarvoor **Status van functieversie** is ingesteld op **Gepubliceerd** kunnen worden gedeeld met externe organisaties.</span><span class="sxs-lookup"><span data-stu-id="d33ca-156">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="add-a-new-globalization-feature"></a><span data-ttu-id="d33ca-157">Een nieuwe globalisatiefunctie toevoegen</span><span class="sxs-lookup"><span data-stu-id="d33ca-157">Add a new Globalization feature</span></span>

<span data-ttu-id="d33ca-158">U kunt een nieuwe globalisatiefunctie toevoegen door deze helemaal opnieuw te maken.</span><span class="sxs-lookup"><span data-stu-id="d33ca-158">You can add a new Globalization feature by creating it from scratch.</span></span>

1. <span data-ttu-id="d33ca-159">Selecteer op de pagina **Functie importeren uit algemene opslagplaats** de optie **Toevoegen** en selecteer vervolgens in het dialoogvenster met vervolgkeuzemenu de optie **Nieuwe functie**.</span><span class="sxs-lookup"><span data-stu-id="d33ca-159">On the **Import feature from Global repository** page, select **Add**, and then, in the drop-down dialog box, select the **New feature** option.</span></span>
2. <span data-ttu-id="d33ca-160">Voer een naam en beschrijving voor de functie in.</span><span class="sxs-lookup"><span data-stu-id="d33ca-160">Enter a name and description for the feature.</span></span>
3. <span data-ttu-id="d33ca-161">Selecteer **Functie maken**.</span><span class="sxs-lookup"><span data-stu-id="d33ca-161">Select **Create feature**.</span></span>

    ![Een nieuwe functie toevoegen](./media/RCS_GlobalF_9%20Feature%20create%20new.JPG)

4. <span data-ttu-id="d33ca-163">Selecteer op het tabblad **Versies** een **ingangsdatum** en selecteer vervolgens **Status wijzigen** om de functie te voltooien.</span><span class="sxs-lookup"><span data-stu-id="d33ca-163">On the **Versions** tab, select an **Effective from** date, and then select **Change status** to complete the feature.</span></span> <span data-ttu-id="d33ca-164">Voltooide functies kunnen voor een specifieke omgeving beschikbaar worden gemaakt, zodat deze kunnen worden gebruikt in globalisatieservices, of kunnen worden gepubliceerd naar de algemene opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="d33ca-164">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="d33ca-165">Functies waarvoor **Status van functieversie** is ingesteld op **Gepubliceerd** kunnen worden gedeeld met externe organisaties.</span><span class="sxs-lookup"><span data-stu-id="d33ca-165">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="feature-component-overview"></a><span data-ttu-id="d33ca-166">Overzicht van functieonderdelen</span><span class="sxs-lookup"><span data-stu-id="d33ca-166">Feature component overview</span></span>

<span data-ttu-id="d33ca-167">Globalisatiefuncties bestaan uit verschillende onderdelen:</span><span class="sxs-lookup"><span data-stu-id="d33ca-167">Globalization features have several components:</span></span>

- <span data-ttu-id="d33ca-168">**Versie**: dit onderdeel ondersteunt het beheer van de functielevenscyclus en stelt gebruikers in staat om de status voor verschillende versies van de functie te beheren.</span><span class="sxs-lookup"><span data-stu-id="d33ca-168">**Version** – This component supports feature lifecycle management and lets users manage the status for different versions of the feature.</span></span>
- <span data-ttu-id="d33ca-169">**Configuraties**: met dit onderdeel kunnen gebruikers gerelateerde ER-indelingen en indelingstoewijzingen beheren, weergeven en bewerken.</span><span class="sxs-lookup"><span data-stu-id="d33ca-169">**Configurations** – This component lets users manage, view, and edit related ER formats and format mappings.</span></span>
- <span data-ttu-id="d33ca-170">**Instellingen**: hiermee kunnen gebruikers van globalisatieservices, zoals een e-factureringsservice, de instellingen van de gerelateerde functieversie beheren.</span><span class="sxs-lookup"><span data-stu-id="d33ca-170">**Setups** – This component lets users of Globalization services, such as an e-invoicing service, manage the setup of the related feature version.</span></span> <span data-ttu-id="d33ca-171">Daarom ondersteunt deze de flexibele constructie van communicatie- en antwoordregels.</span><span class="sxs-lookup"><span data-stu-id="d33ca-171">Therefore, it supports the flexible construction of communication and responses rules.</span></span>
- <span data-ttu-id="d33ca-172">**Omgeving**: met dit onderdeel kunnen gebruikers van globalisatieservices, zoals een e-factureringsservice, de omgeving beheren waarin de versie-instellingen van de functie worden gebruikt en machtigingen toekennen aan gebruikers die toegang hebben tot de service.</span><span class="sxs-lookup"><span data-stu-id="d33ca-172">**Environment** – This component lets users of Globalization services, such as an e-invoicing service, manage the environment where the feature version setup is used and grant authorization to the users who will have access to it.</span></span>
- <span data-ttu-id="d33ca-173">**Organisaties**: met dit onderdeel kunnen gebruikers de functie delen met externe organisaties.</span><span class="sxs-lookup"><span data-stu-id="d33ca-173">**Organizations** – This component lets users to share the feature with external organizations.</span></span>

## <a name="configuring-feature-components"></a><span data-ttu-id="d33ca-174">Functieonderdelen configureren</span><span class="sxs-lookup"><span data-stu-id="d33ca-174">Configuring feature components</span></span>

### <a name="version-and-status"></a><span data-ttu-id="d33ca-175">Versie en status</span><span class="sxs-lookup"><span data-stu-id="d33ca-175">Version and status</span></span>

<span data-ttu-id="d33ca-176">De versie wordt gebruikt om de levenscyclus van de globalisatiefunctie te beheren.</span><span class="sxs-lookup"><span data-stu-id="d33ca-176">The version is used to manage the Globalization feature lifecycle.</span></span>

<span data-ttu-id="d33ca-177">U kunt de status wijzigen in het veld **Status** op het tabblad **Versie**. De volgende statussen zijn beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="d33ca-177">The status can be changed in the **Status** field on the **Version** tab. The following statuses are available:</span></span>

- <span data-ttu-id="d33ca-178">**Concept**: de functie kan alleen worden bewerkt in deze status.</span><span class="sxs-lookup"><span data-stu-id="d33ca-178">**Draft** – The feature can be edited only when it's in this status.</span></span>
- <span data-ttu-id="d33ca-179">**Voltooid**: de functie en alle gerelateerde onderdelen zijn voltooid (voltooid) en kunnen niet worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="d33ca-179">**Complete** – The feature and all related components have been finalized (completed) and can't be edited.</span></span>
- <span data-ttu-id="d33ca-180">**Gepubliceerd**: de functie en alle gerelateerde onderdelen zijn gepubliceerd naar de algemene opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="d33ca-180">**Published** – The feature and all related components have been published to the Global repository.</span></span>
- <span data-ttu-id="d33ca-181">**Gedeeld**: de functie en alle gerelateerde onderdelen zijn met externe organisaties gedeeld.</span><span class="sxs-lookup"><span data-stu-id="d33ca-181">**Shared** – The feature and all related components have been shared with external organizations.</span></span>
- <span data-ttu-id="d33ca-182">**Ingeschakeld**: de functie en alle gerelateerde onderdelen zijn ingeschakeld voor gebruik in een globalisatieservice, zoals een e-factureringsservice.</span><span class="sxs-lookup"><span data-stu-id="d33ca-182">**Enabled** – The feature and all related components have been enabled for use in a Globalization service, such as an e-invoicing service.</span></span>

> [!NOTE]
> <span data-ttu-id="d33ca-183">Functies moeten opeenvolgend door een aantal van deze statussen worden geleid.</span><span class="sxs-lookup"><span data-stu-id="d33ca-183">Features must move sequentially through some of these statuses.</span></span> <span data-ttu-id="d33ca-184">Daarom is mogelijk niet elke status beschikbaar in elke levenscyclus.</span><span class="sxs-lookup"><span data-stu-id="d33ca-184">Therefore, not every status might be available at every lifecycle stage.</span></span>

### <a name="configurations"></a><span data-ttu-id="d33ca-185">Configuraties</span><span class="sxs-lookup"><span data-stu-id="d33ca-185">Configurations</span></span>

<span data-ttu-id="d33ca-186">De volgende acties zijn beschikbaar voor configuraties:</span><span class="sxs-lookup"><span data-stu-id="d33ca-186">The following actions are available for configurations:</span></span>

- <span data-ttu-id="d33ca-187">**Weergeven**: geef de onderliggende functieconfiguraties weer waarvoor geen updates nodig zijn.</span><span class="sxs-lookup"><span data-stu-id="d33ca-187">**View** – View the underlying feature configurations that don't require any update.</span></span>
- <span data-ttu-id="d33ca-188">**Bewerken**: maak een conceptversie van een geselecteerde configuratie, zodat u de indeling of indelingstoewijzing in de indelingsontwerper kunt bewerken.</span><span class="sxs-lookup"><span data-stu-id="d33ca-188">**Edit** – Create a draft version of a selected configuration so that you can edit the format or format mapping in the Format designer.</span></span>
- <span data-ttu-id="d33ca-189">**Verwijderen**: verwijder een geselecteerde configuratie uit de functie.</span><span class="sxs-lookup"><span data-stu-id="d33ca-189">**Delete** – Delete a selected configuration from the feature.</span></span>
- <span data-ttu-id="d33ca-190">**Rebase**: rebase de functie.</span><span class="sxs-lookup"><span data-stu-id="d33ca-190">**Rebase** – Rebase the feature.</span></span> <span data-ttu-id="d33ca-191">Zie de sectie [Afgeleide globalisatiefuncties rebasen](#rebase) verderop in dit onderwerp voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d33ca-191">For more information, see the [Rebase derived Globalization features](#rebase) section later in this topic.</span></span>

### <a name="setups"></a><span data-ttu-id="d33ca-192">Instellingen</span><span class="sxs-lookup"><span data-stu-id="d33ca-192">Setups</span></span>

<span data-ttu-id="d33ca-193">De volgende acties zijn beschikbaar voor functie-instellingen:</span><span class="sxs-lookup"><span data-stu-id="d33ca-193">The following actions are available for feature setups:</span></span>

- <span data-ttu-id="d33ca-194">**Toevoegen**: maak een nieuwe functie-instelling.</span><span class="sxs-lookup"><span data-stu-id="d33ca-194">**Add** – Create a new feature setup.</span></span> <span data-ttu-id="d33ca-195">Deze functie-instelling kan worden afgeleid van een bestaande functie-instelling of geheel nieuw zijn.</span><span class="sxs-lookup"><span data-stu-id="d33ca-195">This feature setup can be derived from an existing feature setup or created from scratch.</span></span>
- <span data-ttu-id="d33ca-196">**Verwijderen**: verwijder een geselecteerde functie-instelling.</span><span class="sxs-lookup"><span data-stu-id="d33ca-196">**Delete** – Delete a selected feature setup.</span></span>
- <span data-ttu-id="d33ca-197">**Weergeven**: geef een onderliggende functie-instelling weer waarvoor geen wijzigingen nodig zijn.</span><span class="sxs-lookup"><span data-stu-id="d33ca-197">**View** – View an underlying feature setup that doesn't require any changes.</span></span>
- <span data-ttu-id="d33ca-198">**Bewerken**: maak, verwijder of wijzig de kenmerken van de drie hoofdonderdelen van een functie-instelling:</span><span class="sxs-lookup"><span data-stu-id="d33ca-198">**Edit** – Create, delete, or modify the attributes of the three main components of a feature setup:</span></span>

    - <span data-ttu-id="d33ca-199">Acties en hun parameters</span><span class="sxs-lookup"><span data-stu-id="d33ca-199">Actions and their parameters</span></span>
    - <span data-ttu-id="d33ca-200">Toepasbaarheidsregels</span><span class="sxs-lookup"><span data-stu-id="d33ca-200">Applicability rules</span></span>
    - <span data-ttu-id="d33ca-201">Variabelen</span><span class="sxs-lookup"><span data-stu-id="d33ca-201">Variables</span></span>

![De pagina voor functieversie-instellingen](./media/RCS_GlobalF_10%20Feature%20set%20up.JPG)

### <a name="environments"></a><span data-ttu-id="d33ca-203">Omgevingen</span><span class="sxs-lookup"><span data-stu-id="d33ca-203">Environments</span></span>

<span data-ttu-id="d33ca-204">De volgende acties zijn beschikbaar voor omgevingen:</span><span class="sxs-lookup"><span data-stu-id="d33ca-204">The following actions are available for environments:</span></span>

- <span data-ttu-id="d33ca-205">**Inschakelen**: selecteer voor een geselecteerde versie een gepubliceerde omgeving en selecteer een **ingangsdatum** wanneer deze beschikbaar moet zijn.</span><span class="sxs-lookup"><span data-stu-id="d33ca-205">**Enable** – For a selected feature version, select a published environment, and select an **Effective from** date when it should be available.</span></span> <span data-ttu-id="d33ca-206">Zie de sectie [Omgevingen configureren voor inschakelen](#configureenvironment) verderop in dit onderwerp voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d33ca-206">For more information, see the [Configure environments for enablement](#configureenvironment) section later in this topic.</span></span>
- <span data-ttu-id="d33ca-207">**Annuleren**: verwijder een omgeving voor een functie-instelling.</span><span class="sxs-lookup"><span data-stu-id="d33ca-207">**Cancel** – Remove an environment for a feature setup.</span></span>

### <a name="organizations"></a><span data-ttu-id="d33ca-208">Organisaties</span><span class="sxs-lookup"><span data-stu-id="d33ca-208">Organizations</span></span>

<span data-ttu-id="d33ca-209">Voer de volgende stappen om een globalisatiefunctie te delen met een externe organisatie.</span><span class="sxs-lookup"><span data-stu-id="d33ca-209">Follow these steps to share a Globalization feature with an external organization.</span></span>

1. <span data-ttu-id="d33ca-210">Selecteer op de pagina **Functies voor e-Facturering** de functie en de versie van de functie die u wilt delen.</span><span class="sxs-lookup"><span data-stu-id="d33ca-210">On the **e-Invoicing features** page, select the feature and the feature version to share.</span></span>
2. <span data-ttu-id="d33ca-211">Selecteer op het tabblad **Organisaties** de optie **Delen met** en voer vervolgens in het dialoogvenster met vervolgkeuzemenu de domeinnaam van de organisatie in.</span><span class="sxs-lookup"><span data-stu-id="d33ca-211">On the **Organizations** tab, select **Share with**, and then, in the drop-down dialog box, enter the organization's domain name.</span></span>
3. <span data-ttu-id="d33ca-212">Selecteer **Delen**.</span><span class="sxs-lookup"><span data-stu-id="d33ca-212">Select **Share**.</span></span>

    ![Een functie delen met een organisatie](./media/RCS_GlobalF_20%20Feature%20orgn_share%20with.JPG)

<span data-ttu-id="d33ca-214">De functie wordt gedeeld met de geselecteerde organisatie en is beschikbaar voor die organisatie in de algemene opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="d33ca-214">The feature is shared with the selected organization and is available for that organization in the Global repository.</span></span> <span data-ttu-id="d33ca-215">Hier kunt u de functie importeren in het RCS- of Dynamics 365 Finance-exemplaar van de organisatie, zodat dit kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d33ca-215">From there, the feature can be imported into the organization's instance of RCS or Dynamics 365 Finance so that it can be used.</span></span>

## <a name="rebase-derived-globalization-features"></a><a name="rebase"></a><span data-ttu-id="d33ca-216">Afgeleide globalisatiefuncties rebasen</span><span class="sxs-lookup"><span data-stu-id="d33ca-216">Rebase derived Globalization features</span></span>

<span data-ttu-id="d33ca-217">U kunt een afgeleide globalisatiefunctie rebasen naar de nieuwe of bijgewerkte versie van de basisfunctie.</span><span class="sxs-lookup"><span data-stu-id="d33ca-217">You can rebase a derived Globalization feature to the new or updated base feature version.</span></span> <span data-ttu-id="d33ca-218">Op deze manier kunnen wijzigingen die in de basisversie zijn opgetreden automatisch worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="d33ca-218">In this way, changes that have occurred in the base version can be automatically updated.</span></span> <span data-ttu-id="d33ca-219">De bijgewerkte versie van de basisfunctie wordt gemaakt door de oorspronkelijke configuratieprovider en wordt vervolgens gepubliceerd of gedeeld.</span><span class="sxs-lookup"><span data-stu-id="d33ca-219">The updated base feature version is created by the originating configuration provider, and it's then published or shared.</span></span>

![Bijgewerkte versie van basisfunctie](./media/RCS_GlobalF_12%20Feature%20new%20version.JPG)

<span data-ttu-id="d33ca-221">Als u bijvoorbeeld de afgeleide versie wilt rebasen van een functie die u hebt gemaakt, haalt u eerst de meest recente versie van de functie op door deze te importeren uit de globale opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="d33ca-221">For example, if you want to rebase the derived version of a feature that you created, you first get the latest version of the feature by importing it from the Global repository.</span></span>

1. <span data-ttu-id="d33ca-222">Selecteer **Importeren** op de pagina **Functies voor e-Facturering**.</span><span class="sxs-lookup"><span data-stu-id="d33ca-222">On the **e-Invoicing features** page, select **Import**.</span></span>
2. <span data-ttu-id="d33ca-223">Selecteer **Synchroniseren** om de nieuwste functies te downloaden.</span><span class="sxs-lookup"><span data-stu-id="d33ca-223">Select **Synchronize** to get the latest features.</span></span>
3. <span data-ttu-id="d33ca-224">Selecteer in de lijst met functies de functies die u wilt importeren en selecteer **Importeren**.</span><span class="sxs-lookup"><span data-stu-id="d33ca-224">In the list of features, select the features to import, and then select **Import**.</span></span>

    ![De nieuwste versie van een functie importeren](./media/RCS_GlobalF_13%20Feature%20new%20version%20import.JPG)

4. <span data-ttu-id="d33ca-226">Selecteer in de lijst met functies de functie die u wilt rebasen.</span><span class="sxs-lookup"><span data-stu-id="d33ca-226">In the list of features, select the feature to rebase.</span></span>
5. <span data-ttu-id="d33ca-227">Selecteer op het tabblad **Versie** de optie **Nieuw** om een conceptversie te maken.</span><span class="sxs-lookup"><span data-stu-id="d33ca-227">On the **Version** tab, select **New** to create a draft version.</span></span>

    ![Nieuwe conceptversie gemaakt](./media/RCS_GlobalF_14%20Feature%20new%20base%20version.JPG)

6. <span data-ttu-id="d33ca-229">Selecteer **Rebase**.</span><span class="sxs-lookup"><span data-stu-id="d33ca-229">Select **Rebase**.</span></span>
7. <span data-ttu-id="d33ca-230">Selecteer in het dialoogvenster **Rebase** de nieuwste versie van de functie waarnaar u wilt rebasen.</span><span class="sxs-lookup"><span data-stu-id="d33ca-230">In the **Rebase** dialog box, select the latest version of the feature to rebase to.</span></span>

    ![Het dialoogvenster Rebase](./media/RCS_GlobalF_15%20Feature%20rebase%20version.JPG)

8. <span data-ttu-id="d33ca-232">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d33ca-232">Select **OK**.</span></span>
9. <span data-ttu-id="d33ca-233">Controleer de functieonderdelen en breng eventueel vereiste wijzigingen aan.</span><span class="sxs-lookup"><span data-stu-id="d33ca-233">Review the feature components, and make any changes that are required.</span></span>
10. <span data-ttu-id="d33ca-234">Selecteer **Status wijzigen** om de functie te voltooien waarvoor een rebase is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="d33ca-234">Select **Change status** to complete the rebased feature.</span></span> <span data-ttu-id="d33ca-235">Wanneer de rebase is voltooid, kunt u extra acties uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="d33ca-235">When the rebase is completed, you can perform additional actions.</span></span> <span data-ttu-id="d33ca-236">U kunt de functie bijvoorbeeld publiceren en beschikbaar maken voor gebruik in globalisatieservices.</span><span class="sxs-lookup"><span data-stu-id="d33ca-236">For example, you can publish the feature and make it available for use in Globalization services.</span></span>

    ![Functiestatus bijgewerkt naar Voltooid](./media/RCS_GlobalF_16%20Feature%20rebase%20version%20complete.JPG)

## <a name="configure-environments-for-globalization-features"></a><a name="configureenvironment"></a><span data-ttu-id="d33ca-238">Omgevingen configureren voor globalisatiefuncties</span><span class="sxs-lookup"><span data-stu-id="d33ca-238">Configure environments for Globalization features</span></span>

<span data-ttu-id="d33ca-239">Gebruikers van globalisatieservices kunnen de omgeving beheren om een globalisatiefunctie in te stellen en autorisatie te verlenen aan andere gebruikers die hiertoe toegang hebben.</span><span class="sxs-lookup"><span data-stu-id="d33ca-239">Users of Globalization services can manage the environment to set up a Globalization feature and grant authorization to other users who will have access to it.</span></span>

1. <span data-ttu-id="d33ca-240">In het werkgebied **Globalisatiefuncties** selecteert u onder **Omgevingen** de tegel **E-facturering**.</span><span class="sxs-lookup"><span data-stu-id="d33ca-240">In the **Globalization Features** workspace, under **Environments**, select the **e-Invoicing** tile.</span></span>

    ![Het werkgebied Globalisatiefuncties](./media/RCS_GlobalF_17%20Feature%20environment.JPG)

2. <span data-ttu-id="d33ca-242">Selecteer **Sleutelkluisparameters** en vervolgens **Nieuw** om een Azure-sleutelkluisgeheim te maken.</span><span class="sxs-lookup"><span data-stu-id="d33ca-242">Select **Key Vault parameters**, and then select **New** to create an Azure Key Vault secret.</span></span>
3. <span data-ttu-id="d33ca-243">Voer een naam en omschrijving voor de sleutelkluis in en voer in het veld **URI sleutelkluis** de URL in waarmee de sleutelkluisresource in Azure wordt aangeduid.</span><span class="sxs-lookup"><span data-stu-id="d33ca-243">Enter a name and description for the key vault, and then, in the **Key Vault URI** field, enter the URL that identifies the Key Vault resource in Azure.</span></span>
4. <span data-ttu-id="d33ca-244">Selecteer op het sneltabblad **Certificaten** de optie **Toevoegen** om het certificaat toe te voegen en voer een naam en omschrijving voor elk certificaat in.</span><span class="sxs-lookup"><span data-stu-id="d33ca-244">On the **Certificates** FastTab, select **Add** to add the certificate, and enter a name and description for each certificate.</span></span>

    ![Certificaat toegevoegd](./media/RCS_GlobalF_18%20Feature%20envn%20key%20vault%20parameter.JPG)

5. <span data-ttu-id="d33ca-246">Selecteer **Nieuw** om een nieuwe omgeving te maken.</span><span class="sxs-lookup"><span data-stu-id="d33ca-246">Select **New** to create a new environment.</span></span>
6. <span data-ttu-id="d33ca-247">Voer een naam, een beschrijving en het geheime token voor handtekeningen voor gedeelde toegang in dat vereist is voor de opslag.</span><span class="sxs-lookup"><span data-stu-id="d33ca-247">Enter a name, a description, and the shared access signature token secret required for the storage.</span></span>
7. <span data-ttu-id="d33ca-248">Selecteer op het sneltabblad **Gebruikers** de optie **Nieuw** om een gebruiker toe te voegen die toegang heeft tot deze omgeving.</span><span class="sxs-lookup"><span data-stu-id="d33ca-248">On the **Users** FastTab, select **New** to add a user who will have permission to access this environment.</span></span>
8. <span data-ttu-id="d33ca-249">Voer de gebruikers-id en het e-mailadres van de gebruiker in.</span><span class="sxs-lookup"><span data-stu-id="d33ca-249">Enter the user's user ID and email address.</span></span>
9. <span data-ttu-id="d33ca-250">Herhaal stap 7 en 8 om nog meer gebruikers toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="d33ca-250">Repeat steps 7 and 8 to add more users.</span></span>
10. <span data-ttu-id="d33ca-251">Selecteer **Publiceren** om de omgeving te publiceren.</span><span class="sxs-lookup"><span data-stu-id="d33ca-251">Select **Publish** to publish the environment.</span></span>

    ![Gepubliceerde omgeving](./media/RCS_GlobalF_19%20Feature%20envn%20publishing.JPG)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]