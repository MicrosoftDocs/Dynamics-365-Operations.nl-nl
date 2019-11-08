---
title: Metagegevens van de toepassing openen door gebruik van verbonden toepassingen
description: In de stappen in dit onderwerp wordt uitgelegd hoe een gebruiker van de Regulatory Configuration Service (RCS) een nieuwe Elektronisch Rapportage modeltoewijzing kan ontwerpen met behulp van de metagegevens in Finance and Operations.
author: NickSelin
manager: AnnBe
ms.date: 06/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a476163ba6f66ab60ed8bfea6198d02f13ac5136
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182710"
---
# <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="1ae6e-103">Metagegevens van de toepassing openen door gebruik van verbonden toepassingen</span><span class="sxs-lookup"><span data-stu-id="1ae6e-103">Access application metadata by using connected applications</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1ae6e-104">In de volgende stappen wordt uitgelegd hoe een gebruiker van Regulatory Configuration Service (RCS) in de rol van systeembeheerder of ER-ontwikkelaar een nieuwe ER-modeltoewijzing kan maken met gebruik van de metagegevens van Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using metadata in Finance and Operations.</span></span> <span data-ttu-id="1ae6e-105">Toepassingsmetagegevens worden online benaderd via de met de toepassing RCS verbonden toepassing.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-105">Application metadata will be accessed online by using the RCS connected application.</span></span> <span data-ttu-id="1ae6e-106">Voorbeeld ER modeltoewijzing wordt geconfigureerd voor het openen van transacties van buitenlandse handel.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-106">Sample ER model mapping will be configured to access foreign trade transactions.</span></span> <span data-ttu-id="1ae6e-107">Als u deze stappen wilt uitvoeren, moet u eerst in RCS de stappen voltooien in het onderwerp [Een configuratieprovider maken en deze als actief markeren](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="1ae6e-107">To complete these steps, in RCS you must first complete the steps in the topic, [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="1ae6e-108">Als u de stappen in het onderwerp [Open toepassingsmetagegevens met gebruik van de ER‑configuratie](access-application-metadata-er-configuration.md)niet hebt voltooid, gaat u naar de [pagina voorbeelden van elektronische rapportage](https://go.microsoft.com/fwlink/?linkid=862266) voor het downloaden en opslaan van de volgende ER‑configuratie: Buitenlandse handel metagegevens.xml; Buitenlandse handel toewijzing.xml; . XML en voltooi dan de stappen van de procedure.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-108">If you have not completed the steps in the topic, [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md), go to the [Electronic reporting examples page](https://go.microsoft.com/fwlink/?linkid=862266) to download and save the following ER configurations: Foreign trade metadata.xml; Foreign trade model.xml; Foreign trade mapping.xml, and then complete the steps in the procedure.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1ae6e-109">Vereisten</span><span class="sxs-lookup"><span data-stu-id="1ae6e-109">Prerequisites</span></span>
1. <span data-ttu-id="1ae6e-110">Ga naar **Alle werkgebieden** > **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-110">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="1ae6e-111">Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als **Actief**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="1ae6e-112">Als u deze configuratieprovider niet ziet, voltooi dan de stappen in de procedure [Een configuratieprovider maken en deze als actief markeren](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="1ae6e-112">If you don’t see this configuration provider, complete the steps in the procedure [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="get-required-er-configurations"></a><span data-ttu-id="1ae6e-113">De vereiste ER-configuraties verkrijgen</span><span class="sxs-lookup"><span data-stu-id="1ae6e-113">Get required ER configurations</span></span>
1. <span data-ttu-id="1ae6e-114">Klik op **Rapportconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-114">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="1ae6e-115">Als u de stappen in de procedure [(RCS) Gebruik de toepassingsmetagegevens met gebruik van de ER‑configuratie](access-application-metadata-er-configuration.md) al hebt voltooid, beschikt u al over alle benodigde ER‑configuraties (metagegevens buitenlandse handel, model- en toewijzingsconfiguraties) in het huidige RCS‑exemplaar.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-115">If you already completed the steps in the [(RCS) Access application metadata by using ER configuration](access-application-metadata-er-configuration.md) procedure, you already have all necessary ER configurations (foreign trade metadata, model and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="1ae6e-116">U kunt alle overige stappen in deze subtaak overslaan.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-116">You can skip all the remaining steps of this sub-task.</span></span> 
3. <span data-ttu-id="1ae6e-117">Klik op **Uitwisselen**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-117">Click **Exchange**.</span></span> 
4. <span data-ttu-id="1ae6e-118">Klik op **Laden uit XML-bestand**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-118">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="1ae6e-119">Klik op **Bladeren** en selecteer het bestand **Buitenlandse handel metagegevens.xml**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-119">Click **Browse** and select the **Foreign trade metadata.xml** file.</span></span> 
6. <span data-ttu-id="1ae6e-120">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-120">Click **OK**.</span></span> 
7. <span data-ttu-id="1ae6e-121">Klik op **Uitwisselen**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-121">Click **Exchange**.</span></span> 
8. <span data-ttu-id="1ae6e-122">Klik op **Laden uit XML-bestand**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-122">Click **Load from XML file**.</span></span> 
9. <span data-ttu-id="1ae6e-123">Klik op **Bladeren** en selecteer het bestand **Buitenlandse handel model.xml**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-123">Click **Browse** and select the **Foreign trade model.xml** file.</span></span> 
10. <span data-ttu-id="1ae6e-124">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-124">Click **OK**.</span></span> 
11. <span data-ttu-id="1ae6e-125">Klik op **Uitwisselen**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-125">Click **Exchange**.</span></span> 
12. <span data-ttu-id="1ae6e-126">Klik op **Laden uit XML-bestand**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-126">Click **Load from XML file**.</span></span> 
13. <span data-ttu-id="1ae6e-127">Klik op **Bladeren** en selecteer het bestand **Buitenlandse handel toewijzing.xml**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-127">Click **Browse** and select the **Foreign trade mapping.xml** file.</span></span> 
14. <span data-ttu-id="1ae6e-128">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-128">Click **OK**.</span></span> 

## <a name="register-a-connected-application"></a><span data-ttu-id="1ae6e-129">Een verbonden toepassing registreren</span><span class="sxs-lookup"><span data-stu-id="1ae6e-129">Register a connected application</span></span>
1. <span data-ttu-id="1ae6e-130">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-130">Close the page.</span></span> 
2. <span data-ttu-id="1ae6e-131">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-131">Close the page.</span></span> 
3. <span data-ttu-id="1ae6e-132">Ga naar **Alle werkgebieden** > **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-132">Go to **All workspaces** > **Electronic reporting**.</span></span> 
4. <span data-ttu-id="1ae6e-133">Klik op **Verbonden toepassingen**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-133">Click **Connected applications**.</span></span> 
5. <span data-ttu-id="1ae6e-134">Controleer of de geconfigureerde toepassing op Azure gebaseerd is en toegankelijk is voor de huidige RCS-gebruiker.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-134">Make sure that the configured application is Azura based and accessible for the current RCS user.</span></span> <span data-ttu-id="1ae6e-135">Het is ook noodzakelijk dat de huidige RCS-gebruiker toegang heeft tot de geselecteerde toepassing en dat deze is geregistreerd als gebruiker van deze toepassing met een rol die hem de bevoegdheid geeft om de metagegevens van de toepassing te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-135">It is also required that the current RCS user has access to the selected application and has been registered as a user of this application playing a role giving him privileges to access application’s metadata.</span></span> 
6. <span data-ttu-id="1ae6e-136">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-136">Click **New**.</span></span> 
7. <span data-ttu-id="1ae6e-137">Typ 'MijnVerbondenApp' in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-137">In the **Name** field, type 'MyConnectedApp'.</span></span> 
8. <span data-ttu-id="1ae6e-138">Typ 'https://mycompany.operations.dynamics.com' in het veld **Toepassing**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-138">In the **Application** field, type 'https:// mycompany.operations.dynamics.com'.</span></span> 
9. <span data-ttu-id="1ae6e-139">Typ 'mycompany.onmicrosoft.com' in het veld **Tenant**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-139">In the **Tenant** field, type ‘mycompany.onmicrosoft.com’.</span></span> 
10. <span data-ttu-id="1ae6e-140">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-140">Click **Save**.</span></span> 
11. <span data-ttu-id="1ae6e-141">Wanneer u de verbinding met de geconfigureerde toepassing controleert, klikt u op de pagina **Maak verbinding met externe toepassing** op de link **Klik hier om verbinding te maken met de geselecteerde externe toepassing**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-141">When you check connection to configured application, on the **Connect to remote application** page click **Click here to connect to selected remote application** link.</span></span> 
12. <span data-ttu-id="1ae6e-142">Klik op **Verbinding controleren**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-142">Click **Check connection**.</span></span> 
13. <span data-ttu-id="1ae6e-143">Klik op **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-143">Click **Close**.</span></span> 
14. <span data-ttu-id="1ae6e-144">Wanneer de verbindingsvalidatie is geslaagd, worden de versie- en tenantgegevens bijgewerkt voor de geconfigureerde toepassing in het huidige raster.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-144">When the connection validation succeeded, version and tenant details will be updated for the configured application in the current grid.</span></span> 

## <a name="review-existing-model-mapping-configuration"></a><span data-ttu-id="1ae6e-145">Een bestaande modeltoewijzingsconfiguratie controleren</span><span class="sxs-lookup"><span data-stu-id="1ae6e-145">Review existing model mapping configuration</span></span>
1. <span data-ttu-id="1ae6e-146">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-146">Close the page.</span></span> 
2. <span data-ttu-id="1ae6e-147">Klik op **Rapportconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-147">Click **Reporting configurations**.</span></span> 
3. <span data-ttu-id="1ae6e-148">Vouw **Buitenlandse handel model** uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-148">In the tree, expand **Foreign trade model**.</span></span> 
4. <span data-ttu-id="1ae6e-149">Selecteer in de structuur **Buitenlandse handel model\Buitenlandse handel toewijzing**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-149">In the tree, select **Foreign trade model\Foreign trade mapping**.</span></span> 
5. <span data-ttu-id="1ae6e-150">Vouw de sectie **Vereisten** uit.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-150">Expand the **Prerequisites** section.</span></span> 

> [!NOTE]
> <span data-ttu-id="1ae6e-151">Deze toewijzing verwijst momenteel naar de metagegevensconfiguratie.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-151">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="1ae6e-152">De metagegevens van de toepassing van deze configuratie worden aangeboden wanneer deze modeltoewijzing wordt ontworpen.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-152">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

6. <span data-ttu-id="1ae6e-153">Klik op **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-153">Click **Designer**.</span></span> 
7. <span data-ttu-id="1ae6e-154">Klik op **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-154">Click **Designer**.</span></span> 
8. <span data-ttu-id="1ae6e-155">Selecteer in de structuur **Dynamics 365 for Operations'\Tabelrecords**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-155">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
9. <span data-ttu-id="1ae6e-156">Klik op **Basis toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-156">Click **Add root**.</span></span> 
10. <span data-ttu-id="1ae6e-157">Typ of selecteer een waarde in het veld **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-157">In the **Table** field, enter or select a value.</span></span> 

> [!NOTE]
> <span data-ttu-id="1ae6e-158">Deze toewijzing verwijst momenteel naar de metagegevensconfiguratie.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-158">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="1ae6e-159">De metagegevens van de toepassing van deze configuratie worden aangeboden wanneer deze modeltoewijzing wordt ontworpen.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-159">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

11. <span data-ttu-id="1ae6e-160">Klik op **Annuleren**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-160">Click **Cancel**.</span></span> 
12. <span data-ttu-id="1ae6e-161">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-161">Close the page.</span></span> 
13. <span data-ttu-id="1ae6e-162">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-162">Close the page.</span></span> 

## <a name="assign-connected-application-to-model-mapping"></a><span data-ttu-id="1ae6e-163">Verbonden toepassing toewijzen aan modeltoewijzing</span><span class="sxs-lookup"><span data-stu-id="1ae6e-163">Assign connected application to model mapping</span></span> 
1. <span data-ttu-id="1ae6e-164">Klik op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-164">Click **Edit**.</span></span> 
2. <span data-ttu-id="1ae6e-165">Selecteer de **MyConnectedApp** toepassing.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-165">Select **MyConnectedApp** application.</span></span> 

> [!NOTE]
> <span data-ttu-id="1ae6e-166">Op dit moment verwijst deze toewijzing naar de metagegevens van de geselecteerde gekoppelde toepassing.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-166">Currently, this mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="1ae6e-167">Wanneer dezelfde toewijzing tegelijkertijd verwijst naar de configuratie van de metagegevens en de gekoppelde toepassing, dan worden de metagegevens van de verbonden toepassing gebruikt.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-167">When the same mapping refers to metadata configuration and connected application at the same time, metadata of the connected application will be used.</span></span> 

3. <span data-ttu-id="1ae6e-168">Klik op **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-168">Click **Designer**.</span></span> 
4. <span data-ttu-id="1ae6e-169">Klik op **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-169">Click **Designer**.</span></span> 
5. <span data-ttu-id="1ae6e-170">Selecteer in de structuur **Dynamics 365 for Operations'\Tabelrecords**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
6. <span data-ttu-id="1ae6e-171">Klik op **Basis toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-171">Click **Add root**.</span></span> 
7. <span data-ttu-id="1ae6e-172">Typ of selecteer een waarde in het veld **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-172">In the **Table** field, enter or select a value.</span></span> 

> [!NOTE]
> <span data-ttu-id="1ae6e-173">Er zijn nu meer dan twee toepassingstabellen aangeboden, omdat deze toewijzing alle metagegevens van de verbonden toepassing gebruikt die hieraan is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-173">More than two application tables were offered now as this mapping uses all the metadata of the connected application that has been assigned for it.</span></span> 

8. <span data-ttu-id="1ae6e-174">Klik op **Annuleren**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-174">Click **Cancel**.</span></span> 
9. <span data-ttu-id="1ae6e-175">Klik op **Valideren**.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-175">Click **Validate**.</span></span> 

> [!NOTE]
> <span data-ttu-id="1ae6e-176">We hebben elementen van het gegevensmodel gebonden met items van gegevensbronnen die worden beschreven met behulp van details van metagegevens van de verbonden toepassing die is toegewezen voor deze toewijzing.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-176">We successfully bound elements of data model with items of data sources that are described by using details of metadata of the connected application that has been assigned for this mapping.</span></span> 

10. <span data-ttu-id="1ae6e-177">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-177">Close the page.</span></span> 
11. <span data-ttu-id="1ae6e-178">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-178">Close the page.</span></span> 

<span data-ttu-id="1ae6e-179">Wanneer u deze modeltoewijzing wilt evalueren door metagegevens van een andere toepassingsapplicatie te gebruiken, registreert u een andere gekoppelde toepassing, wijst u deze toe aan deze modeltoewijzing en valideert u deze tegen nieuwe metagegevens.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-179">When you need to evaluate this model mapping by using metadata of a different version application, register another connected application, assign it to this model mapping and validate it against new metadata.</span></span>