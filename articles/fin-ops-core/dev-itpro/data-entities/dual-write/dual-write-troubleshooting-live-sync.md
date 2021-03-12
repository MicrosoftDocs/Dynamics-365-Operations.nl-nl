---
title: Problemen met live synchronisatie oplossen
description: Dit onderwerp bevat informatie over het oplossen van problemen met live synchronisatie.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 59c8bd80b167cdfaa7a65e469f4dc7ebf8f50844
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744608"
---
# <a name="troubleshoot-live-synchronization-issues"></a><span data-ttu-id="4c92b-103">Problemen met live synchronisatie oplossen</span><span class="sxs-lookup"><span data-stu-id="4c92b-103">Troubleshoot live synchronization issues</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="4c92b-104">Dit onderwerp bevat informatie voor het oplossen van problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Dataverse.</span><span class="sxs-lookup"><span data-stu-id="4c92b-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="4c92b-105">Dit onderwerp bevat specifieke informatie over het oplossen van problemen met live synchronisatie.</span><span class="sxs-lookup"><span data-stu-id="4c92b-105">Specifically, it provides information that can help you fix issues with live synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4c92b-106">In sommige problemen die in dit onderwerp worden beschreven, is mogelijk de rol van systeembeheerder vereist of de referenties van de Microsoft Azure Active Directory-tenantbeheerder (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="4c92b-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="4c92b-107">In de sectie voor elk probleem wordt uitgelegd of een specifieke rol of referenties vereist zijn.</span><span class="sxs-lookup"><span data-stu-id="4c92b-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-row-in-a-finance-and-operations-app"></a><span data-ttu-id="4c92b-108">Met live synchronisatie wordt een 403 Verboden-fout gegenereerd wanneer u een rij in een Finance and Operations-app maakt</span><span class="sxs-lookup"><span data-stu-id="4c92b-108">Live synchronization throws a 403 Forbidden error when you create a row in a Finance and Operations app</span></span>

<span data-ttu-id="4c92b-109">Mogelijk wordt het volgende foutbericht weergegeven wanneer u een rij in een Finance and Operations-app maakt:</span><span class="sxs-lookup"><span data-stu-id="4c92b-109">You might receive the following error message when you create a row in a Finance and Operations app:</span></span>

<span data-ttu-id="4c92b-110">*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"message\\":\\"De gebruiker is geen lid van de organisatie.\\"}}\], De externe server heeft een fout geretourneerd: (403) verboden."}}".*</span><span class="sxs-lookup"><span data-stu-id="4c92b-110">*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"message\\":\\"The user is not a member of the organization.\\"}}\], The remote server returned an error: (403) Forbidden."}}".*</span></span>

<span data-ttu-id="4c92b-111">Volg de stappen in [Systeemvereisten en vereisten vooraf](requirements-and-prerequisites.md) om het probleem op te lossen.</span><span class="sxs-lookup"><span data-stu-id="4c92b-111">To fix the issue, follow the steps in [System requirements and prerequisites](requirements-and-prerequisites.md).</span></span> <span data-ttu-id="4c92b-112">Om deze stappen te voltooien moeten de gebruikers van de toepassing voor twee keer wegschrijven die in Dataverse gemaakt zijn, beschikken over de rol systeembeheerder.</span><span class="sxs-lookup"><span data-stu-id="4c92b-112">To complete those steps, the dual-write application users who are created in Dataverse must have the system admin role.</span></span> <span data-ttu-id="4c92b-113">Het standaardteam van eigenaar moet ook de rol systeembeheerder hebben.</span><span class="sxs-lookup"><span data-stu-id="4c92b-113">The default owning team must also have the system admin role.</span></span>

## <a name="live-synchronization-for-any-table-consistently-throws-a-similar-error-when-you-create-a-row-in-a-finance-and-operations-app"></a><span data-ttu-id="4c92b-114">Met live synchronisatie voor een tabel wordt steeds een vergelijkbare fout gegenereerd wanneer u een rij in een Finance and Operations-app maakt</span><span class="sxs-lookup"><span data-stu-id="4c92b-114">Live synchronization for any table consistently throws a similar error when you create a row in a Finance and Operations app</span></span>

<span data-ttu-id="4c92b-115">**Vereiste rol om de fout op te lossen:** systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="4c92b-115">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="4c92b-116">Er wordt een foutbericht van de volgende strekking weergegeven wanneer u tabelgegevens wilt opslaan in een Finance and Operations-app:</span><span class="sxs-lookup"><span data-stu-id="4c92b-116">You might receive an error message like the following every time that you try to save table data in a Finance and Operations app:</span></span>

<span data-ttu-id="4c92b-117">*De wijzigingen in de database kunnen niet worden opgeslagen. Werkeenheid kan transactie niet doorvoeren. Kan geen gegevens schrijven in maateenheid van entiteit. Schrijven naar UnitOfMeasureEntity is mislukt met foutbericht Kan niet synchroniseren met maateenheden van entiteit.*</span><span class="sxs-lookup"><span data-stu-id="4c92b-117">*Cannot save the changes to the database. Unit of Work can not commit transaction. Unable to write data to entity uoms. Writes to UnitOfMeasureEntity failed with error message Unable to sync with entity uoms.*</span></span>

<span data-ttu-id="4c92b-118">Om het probleem op te lossen moet u ervoor zorgen dat de vereiste verwijzingsgegevens aanwezig zijn in de app Finance and Operations en in Dataverse.</span><span class="sxs-lookup"><span data-stu-id="4c92b-118">To fix the issue, you must make sure that the prerequisite reference data exists in both the Finance and Operations app and Dataverse.</span></span> <span data-ttu-id="4c92b-119">Als u als klant in de Finance and Operations-app bijvoorbeeld deel uitmaakt van een specifieke klantengroep, controleert u of de klantengroep ook bestaat in Dataverse.</span><span class="sxs-lookup"><span data-stu-id="4c92b-119">For example, if the customer that you're in the Finance and Operations app belongs to a specific customer group, make sure that the customer group exists in Dataverse.</span></span>

<span data-ttu-id="4c92b-120">Voer de volgende stappen uit als er aan beide zijden gegevens voorkomen en u hebt bevestigd dat het probleem niet samenhangt met gegevens:</span><span class="sxs-lookup"><span data-stu-id="4c92b-120">If data exists on both sides, and you've confirmed that the issue isn't data-related, follow these steps.</span></span>

1. <span data-ttu-id="4c92b-121">Stop de gerelateerde tabel.</span><span class="sxs-lookup"><span data-stu-id="4c92b-121">Stop the related table.</span></span>
2. <span data-ttu-id="4c92b-122">Meld u aan bij de Finance and Operations-app en zorg ervoor dat er rijen bestaan voor de tabel die de fout veroorzaakt in de tabellen DualWriteprojectConfiguration en DualWriteprojectFieldConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4c92b-122">Sign in to the Finance and Operations app, and make sure that rows for the failing table exist in the DualWriteProjectConfiguration and DualWriteProjectFieldConfiguration tables.</span></span> <span data-ttu-id="4c92b-123">Hier ziet u bijvoorbeeld hoe de query eruitziet als de tabel **Klanten** een fout veroorzaakt.</span><span class="sxs-lookup"><span data-stu-id="4c92b-123">For example, here is what the query looks like if the **Customers** table is failing.</span></span>

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. <span data-ttu-id="4c92b-124">Als er rijen zijn voor de foutieve tabel, zelfs nadat u de tabeltoewijzing hebt gestopt, verwijdert u de rijen die zijn gerelateerd aan de tabel die de fout veroorzaakt.</span><span class="sxs-lookup"><span data-stu-id="4c92b-124">If there are rows for the failing table even after you stop the table mapping, delete the rows that are related to the failing table.</span></span> <span data-ttu-id="4c92b-125">Noteer de kolom **projectnaam** in de tabel DualWriteprojectConfiguration en haal de rij op in de DualWriteprojectFieldConfiguration-tabel door de naam van het project te gebruiken om de rij te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="4c92b-125">Make a note of the **projectname** column in the DualWriteProjectConfiguration table, and fetch the row in the DualWriteProjectFieldConfiguration table by using the project name to delete the row.</span></span>
4. <span data-ttu-id="4c92b-126">Start de tabeltoewijzing.</span><span class="sxs-lookup"><span data-stu-id="4c92b-126">Start the table mapping.</span></span> <span data-ttu-id="4c92b-127">Controleer of de gegevens zonder problemen worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="4c92b-127">Validate whether the data is synced without any issues.</span></span>

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a><span data-ttu-id="4c92b-128">Fouten met lees- of schrijfbevoegdheid oplossen wanneer u gegevens maakt in een Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="4c92b-128">Handle read or write privilege errors when you create data in a Finance and Operations app</span></span>

<span data-ttu-id="4c92b-129">Wanneer u gegevens in een Finance and Operations-app maakt, wordt het foutbericht "Ongeldige aanvraag" weergegeven, zoals in het volgende voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="4c92b-129">You might receive a "Bad Request" error message that resembles the following example when you create data in a Finance and Operations app.</span></span>

![Voorbeeld van foutbericht Ongeldige aanvraag](media/error_record_id_source.png)

<span data-ttu-id="4c92b-131">Om het probleem op te lossen moet u de juiste beveiligingsrol toewijzen aan het team van de toegewezen Dynamics 365 Sales- of Dynamics 365 Customer Service-bedrijfseenheid om de ontbrekende bevoegdheid in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="4c92b-131">To fix the issue, you must assign the correct security role to the team of the mapped Dynamics 365 Sales or Dynamics 365 Customer Service business unit to enable the missing privilege.</span></span>

1. <span data-ttu-id="4c92b-132">Zoek in de Finance and Operations-app de bedrijfseenheid die is toegewezen in de verbindingsset Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="4c92b-132">In the Finance and Operations app, find the business unit that is mapped in the Data Integration connection set.</span></span>

    ![Organisatietoewijzing](media/mapped_business_unit.png)

2. <span data-ttu-id="4c92b-134">Meld u aan bij de omgeving in de modelgestuurde app in Dynamics 365, navigeer naar **Instelling \> Beveiliging** en zoek het team van de toegewezen bedrijfseenheid.</span><span class="sxs-lookup"><span data-stu-id="4c92b-134">Sign in to the environment in the model-driven app in Dynamics 365, navigate to **Setting \> Security**, and find the team of the mapped business unit.</span></span>

    ![Team van de toegewezen bedrijfseenheid](media/setting_security_page.png)

3. <span data-ttu-id="4c92b-136">Open de pagina voor het team voor bewerking en selecteer **Rollen beheren** om het dialoogvenster **Teamrollen beheren** te openen.</span><span class="sxs-lookup"><span data-stu-id="4c92b-136">Open the page for the team for editing, and then select **Manage roles** to open the **Manage Team Roles** dialog box.</span></span>

    ![De knop Rollen beheren](media/manage_team_roles.png)

4. <span data-ttu-id="4c92b-138">Wijs de rol met de bevoegdheid voor lezen/schrijven toe voor de relevante tabellen en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c92b-138">Assign the role that has the read/write privilege for the relevant tables, and then select **OK**.</span></span>

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a><span data-ttu-id="4c92b-139">Synchronisatie problemen oplossen in een omgeving met een recent gewijzigde Dataverse-omgeving</span><span class="sxs-lookup"><span data-stu-id="4c92b-139">Fix synchronization issues in an environment that has a recently changed Dataverse environment</span></span>

<span data-ttu-id="4c92b-140">**Vereiste rol om de fout op te lossen:** systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="4c92b-140">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="4c92b-141">Mogelijk wordt het volgende foutbericht weergegeven wanneer u gegevens in een Finance and Operations-app maakt:</span><span class="sxs-lookup"><span data-stu-id="4c92b-141">You might receive the following error message when you create data in a Finance and Operations app:</span></span>

<span data-ttu-id="4c92b-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Kan geen nettolading genereren voor entiteit CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Het maken van de nettolading is mislukt met fout Ongeldige URI: de URI is leeg."}\],"isErrorCountUpdated":true}*</span><span class="sxs-lookup"><span data-stu-id="4c92b-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Unable to generate payload for entity CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Payload creation failed with error Invalid URI: The URI is empty."}\],"isErrorCountUpdated":true}*</span></span>

<span data-ttu-id="4c92b-143">Zo ziet de fout eruit in de modelgestuurde app in Dynamics 365:</span><span class="sxs-lookup"><span data-stu-id="4c92b-143">Here is what the error looks like in the model-driven app in Dynamics 365:</span></span>

<span data-ttu-id="4c92b-144">*Er is een onverwachte fout opgetreden vanuit de ISV-code. (Fouttype = ClientError) Onverwachte uitzondering in invoegtoepassing: (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: verwerken van entiteitsaccount mislukt - een verbindingspoging is mislukt omdat de verbonden partij niet correct reageert na een bepaalde tijd of de tot stand gebrachte verbinding is mislukt omdat de verbonden host niet heeft gereageerd*</span><span class="sxs-lookup"><span data-stu-id="4c92b-144">*An unexpected error occurred from ISV code. (ErrorType = ClientError) Unexpected exception from plug-in (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: failed to process entity account - (A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond*</span></span>

<span data-ttu-id="4c92b-145">Deze fout treedt op wanneer de Dataverse-omgeving onjuist opnieuw wordt ingesteld op het moment dat u probeert gegevens te maken in de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="4c92b-145">This error occurs when the Dataverse environment is incorrectly reset at the same time that you try to create data in the Finance and Operations app.</span></span>

<span data-ttu-id="4c92b-146">Volg deze stappen om het probleem op te lossen.</span><span class="sxs-lookup"><span data-stu-id="4c92b-146">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="4c92b-147">Meld u aan bij de virtuele machine (VM) voor Finance and Operations, open SQL Server Management Studio (SSMS) en zoek naar rijen in de tabel DUALWRITEPROJECTCONFIGURATIONENTITY, waarbij **internalentityname** gelijk is aan **Klanten v3** en **externalentityname** gelijk is aan **accounts**.</span><span class="sxs-lookup"><span data-stu-id="4c92b-147">Sign in to the Finance and Operations virtual machine (VM), open SQL Server Management Studio (SSMS), and look for rows in the DUALWRITEPROJECTCONFIGURATIONENTITY table where **internalentityname** equals **Customers V3** and **externalentityname** equals **accounts**.</span></span> <span data-ttu-id="4c92b-148">De query ziet er dan als volgt uit.</span><span class="sxs-lookup"><span data-stu-id="4c92b-148">Here is what the query looks like.</span></span>

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. <span data-ttu-id="4c92b-149">Gebruik de projectnaam uit de resultaten van de vorige query om de volgende query uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="4c92b-149">Use the project name from the results of the previous query to run the following query.</span></span>

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. <span data-ttu-id="4c92b-150">Controleer of de kolom **externalenvironmentURL** de juiste URL voor Dataverse of de app heeft.</span><span class="sxs-lookup"><span data-stu-id="4c92b-150">Make sure that the **externalenvironmentURL** column has the correct Dataverse or app URL.</span></span> <span data-ttu-id="4c92b-151">Verwijder dubbele rijen die naar de verkeerde Dataverse-URL verwijzen.</span><span class="sxs-lookup"><span data-stu-id="4c92b-151">Delete any duplicate rows that point to the wrong Dataverse URL.</span></span> <span data-ttu-id="4c92b-152">Verwijder de overeenkomstige rijen uit de tabellen DUALWRITEPROJECTFIELDCONFIGURATION en DUALWRITEPROJECTCONFIGURATION.</span><span class="sxs-lookup"><span data-stu-id="4c92b-152">Delete the corresponding rows in the DUALWRITEPROJECTFIELDCONFIGURATION and DUALWRITEPROJECTCONFIGURATION tables.</span></span>
4. <span data-ttu-id="4c92b-153">De tabeltoewijzing stoppen en vervolgens opnieuw starten</span><span class="sxs-lookup"><span data-stu-id="4c92b-153">Stop the table mapping, and then restart it</span></span>
