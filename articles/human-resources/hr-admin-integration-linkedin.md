---
title: Integreren met LinkedIn Talent Hub
description: In dit onderwerp wordt uitgelegd hoe u integratie instelt tussen Microsoft Dynamics 365 Human Resources en LinkedIn Talent Hub.
author: jaredha
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 208998b5c09416407612352da7a8ef5dd9491914
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889975"
---
# <a name="integrate-with-linkedin-talent-hub"></a><span data-ttu-id="caea0-103">Integreren met LinkedIn Talent Hub</span><span class="sxs-lookup"><span data-stu-id="caea0-103">Integrate with LinkedIn Talent Hub</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [banner](includes/preview-feature.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="caea0-104">[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) is een ATS-platform (Applicant Tracking System).</span><span class="sxs-lookup"><span data-stu-id="caea0-104">[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) is an applicant tracking system (ATS) platform.</span></span> <span data-ttu-id="caea0-105">Hier zijn sourcing, beheer en aanstelling van werknemers op één plaats mogelijk.</span><span class="sxs-lookup"><span data-stu-id="caea0-105">It lets you source, manage, and hire employees all in one place.</span></span> <span data-ttu-id="caea0-106">Door Microsoft Dynamics 365 Human Resources te integreren met LinkedIn Talent Hub kunt u eenvoudig werknemersrecords in Human Resources maken voor sollicitanten die voor een functie zijn aangesteld.</span><span class="sxs-lookup"><span data-stu-id="caea0-106">By integrating Microsoft Dynamics 365 Human Resources with LinkedIn Talent Hub, you can easily create employee records in Human Resources for applicants who have been hired for a position.</span></span>

## <a name="setup"></a><span data-ttu-id="caea0-107">Instelling</span><span class="sxs-lookup"><span data-stu-id="caea0-107">Setup</span></span>

<span data-ttu-id="caea0-108">Een systeembeheerder moet installatietaken voltooien om integratie met LinkedIn Talent Hub mogelijk te maken.</span><span class="sxs-lookup"><span data-stu-id="caea0-108">A system administrator must complete setup tasks to enable integration with LinkedIn Talent Hub.</span></span> <span data-ttu-id="caea0-109">Eerst moet u in de Power Apps-omgeving een gebruiker en beveiligingsrol instellen om LinkedIn Talent Hub de juiste machtigingen te geven om gegevens naar Human Resources te schrijven.</span><span class="sxs-lookup"><span data-stu-id="caea0-109">First, in the Power Apps environment, you must set up a user and security role to grant LinkedIn Talent Hub the appropriate permissions to write data into Human Resources.</span></span>

### <a name="link-your-environment-to-linkedin-talent-hub"></a><span data-ttu-id="caea0-110">Uw omgeving koppelen aan LinkedIn Talent Hub</span><span class="sxs-lookup"><span data-stu-id="caea0-110">Link your environment to LinkedIn Talent Hub</span></span>

1. <span data-ttu-id="caea0-111">Open [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).</span><span class="sxs-lookup"><span data-stu-id="caea0-111">Open [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).</span></span>

2. <span data-ttu-id="caea0-112">Selecteer **Productinstellingen** in het vervolgkeuzemenu voor gebruikers.</span><span class="sxs-lookup"><span data-stu-id="caea0-112">On the user drop-down menu, select **Product Settings**.</span></span>

3. <span data-ttu-id="caea0-113">Selecteer in het linkernavigatievenster in de sectie **Geavanceerd** de optie **Integraties**.</span><span class="sxs-lookup"><span data-stu-id="caea0-113">In the left navigation pane, in the **Advanced** section, select **Integrations**.</span></span>

4. <span data-ttu-id="caea0-114">Selecteer **Autoriseren** voor de integratie met Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="caea0-114">Select **Authorize** for the Microsoft Dynamics 365 Human Resources integration.</span></span>

5. <span data-ttu-id="caea0-115">Selecteer op de pagina **Dynamics 365 Human Resources** de omgeving waaraan u LinkedIn Talent Hub wilt koppelen en selecteer vervolgens **Koppelen**.</span><span class="sxs-lookup"><span data-stu-id="caea0-115">On the **Dynamics 365 Human Resources** page, select the environment to link LinkedIn Talent Hub to, and then select **Link**.</span></span>

    ![LinkedIn Talent Hub-onboarding](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > <span data-ttu-id="caea0-117">U kunt alleen koppelingen maken naar omgevingen waarin uw gebruikersaccount beheerderstoegang heeft tot zowel de Human Resources-omgeving als de bijbehorende Power Apps-omgeving.</span><span class="sxs-lookup"><span data-stu-id="caea0-117">You can link only to environments where your user account has administrator access to both the Human Resources environment and the associated Power Apps environment.</span></span> <span data-ttu-id="caea0-118">Als er geen omgevingen worden weergegeven op de koppelingspagina Human Resources, controleert u of u een gelicentieerde Human Resources-omgeving hebt op de tenant en of de gebruiker die u op de koppelingspagina hebt aangemeld, beheerdersrechten heeft voor zowel de Human Resources-omgeving als de Power Apps-omgeving.</span><span class="sxs-lookup"><span data-stu-id="caea0-118">If no environments are listed on the Human Resources link page, make sure that you have licensed Human Resources environments on the tenant, and that the user that you signed in to the link page as has administrator permissions to both the Human Resources environment and the Power Apps environment.</span></span>

### <a name="create-a-power-apps-security-role"></a><span data-ttu-id="caea0-119">Een Power Apps-beveiligingsrol maken</span><span class="sxs-lookup"><span data-stu-id="caea0-119">Create a Power Apps security role</span></span>

1. <span data-ttu-id="caea0-120">Open het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="caea0-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="caea0-121">Selecteer in de lijst **Omgevingen** de omgeving die is gekoppeld aan de Human Resources-omgeving waaraan u uw exemplaar van LinkedIn Talent Hub wilt koppelen.</span><span class="sxs-lookup"><span data-stu-id="caea0-121">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="caea0-122">Selecteer **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="caea0-122">Select **Settings**.</span></span>

4. <span data-ttu-id="caea0-123">Vouw het knooppunt **Gebruikers en machtigingen** uit en selecteer **Beveiligingsrollen**.</span><span class="sxs-lookup"><span data-stu-id="caea0-123">Expand the **Users + Permissions** node, and select **Security Roles**.</span></span>

5. <span data-ttu-id="caea0-124">Selecteer op de pagina **Beveiligingsrollen** op de werkbalk de optie **Nieuwe rol**.</span><span class="sxs-lookup"><span data-stu-id="caea0-124">On the **Security Roles** page, on the toolbar, select **New role**.</span></span>

6. <span data-ttu-id="caea0-125">Voer op het tabblad **Details** een naam in voor de rol, zoals **HRIS-integratie met LinkedIn Talent Hub.**</span><span class="sxs-lookup"><span data-stu-id="caea0-125">On the **Details** tab, enter a name for the role, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>

7. <span data-ttu-id="caea0-126">Selecteer op het tabblad **Aanpassing** de machtiging **Lezen** op organisatieniveau voor de volgende entiteiten:</span><span class="sxs-lookup"><span data-stu-id="caea0-126">On the **Customization** tab, select organization-level **Read** permission for the following entities:</span></span>

    - <span data-ttu-id="caea0-127">Entiteit</span><span class="sxs-lookup"><span data-stu-id="caea0-127">Entity</span></span>
    - <span data-ttu-id="caea0-128">Veld</span><span class="sxs-lookup"><span data-stu-id="caea0-128">Field</span></span>
    - <span data-ttu-id="caea0-129">Relatie</span><span class="sxs-lookup"><span data-stu-id="caea0-129">Relationship</span></span>

8. <span data-ttu-id="caea0-130">Sla de beveiligingsrol op en sluit deze.</span><span class="sxs-lookup"><span data-stu-id="caea0-130">Save and close the security role.</span></span>

### <a name="create-a-power-apps-application-user"></a><span data-ttu-id="caea0-131">Een Power Apps-toepassingsgebruiker maken</span><span class="sxs-lookup"><span data-stu-id="caea0-131">Create a Power Apps application user</span></span>

<span data-ttu-id="caea0-132">Er moet een toepassingsgebruiker worden gemaakt voor de LinkedIn Talent Hub-adapter om machtigingen te verlenen aan de adapter om kandidaatrecords naar de Power Apps-omgeving te schrijven.</span><span class="sxs-lookup"><span data-stu-id="caea0-132">An application user must be created for the LinkedIn Talent Hub adapter to grant permissions to the adapter to write candidate records into the Power Apps environment.</span></span>

1. <span data-ttu-id="caea0-133">Open het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="caea0-133">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="caea0-134">Selecteer in de lijst **Omgevingen** de omgeving die is gekoppeld aan de Human Resources-omgeving waaraan u uw exemplaar van LinkedIn Talent Hub wilt koppelen.</span><span class="sxs-lookup"><span data-stu-id="caea0-134">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="caea0-135">Selecteer **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="caea0-135">Select **Settings**.</span></span>

4. <span data-ttu-id="caea0-136">Vouw het knooppunt **Gebruikers en machtigingen** uit en selecteer **Gebruikers**.</span><span class="sxs-lookup"><span data-stu-id="caea0-136">Expand the **Users + Permissions** node, and select **Users**.</span></span>

5. <span data-ttu-id="caea0-137">Selecteer **Gebruikers beheren in Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="caea0-137">Select **Manage users in Dynamics 365**.</span></span>

6. <span data-ttu-id="caea0-138">Gebruik het vervolgkeuzemenu boven de lijst om de weergave te wijzigen van de standaardweergave **Ingeschakelde gebruikers** in **Toepassingsgebruikers**.</span><span class="sxs-lookup"><span data-stu-id="caea0-138">Use the drop-down menu above the list to change the view from the default **Enabled Users** view to **Application Users**.</span></span>

    ![Weergave van toepassingsgebruikers](./media/hr-admin-integration-power-apps-application-users.jpg)

7. <span data-ttu-id="caea0-140">Selecteer **Nieuw** op de werkbalk.</span><span class="sxs-lookup"><span data-stu-id="caea0-140">On the toolbar, select **New**.</span></span>

8. <span data-ttu-id="caea0-141">Voer op de pagina **Nieuwe gebruiker** de volgende stappen uit:</span><span class="sxs-lookup"><span data-stu-id="caea0-141">On the **New user** page, follow these steps:</span></span>

    1. <span data-ttu-id="caea0-142">Wijzig de waarde van het veld **Gebruikerstype** in **Toepassingsgebruiker**.</span><span class="sxs-lookup"><span data-stu-id="caea0-142">Change the value of the **User type** field to **Application User**.</span></span>
    2. <span data-ttu-id="caea0-143">Stel het veld **Gebruikersnaam** in op **HRIS-integratie met Dynamics365 HR LinkedIn**.</span><span class="sxs-lookup"><span data-stu-id="caea0-143">Set the **User Name** field to **Dynamics365 HR LinkedIn HRIS Integration**.</span></span>
    3. <span data-ttu-id="caea0-144">Stel het veld **Toepassings-ID** in op **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span><span class="sxs-lookup"><span data-stu-id="caea0-144">Set the **Application ID** field to **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    4. <span data-ttu-id="caea0-145">Voer een waarde in de velden **Voornaam**, **Achternaam** en **Primaire e-mail** in.</span><span class="sxs-lookup"><span data-stu-id="caea0-145">Enter any value in the **First Name**, **Last Name**, and **Primary Email** fields.</span></span>
    5. <span data-ttu-id="caea0-146">Selecteer **Opslaan \& sluiten** op de werkbalk.</span><span class="sxs-lookup"><span data-stu-id="caea0-146">On the toolbar, select **Save \& Close**.</span></span>

### <a name="assign-a-security-role-to-the-new-user"></a><span data-ttu-id="caea0-147">Een beveiligingsrol toewijzen aan de nieuwe gebruiker</span><span class="sxs-lookup"><span data-stu-id="caea0-147">Assign a security role to the new user</span></span>

<span data-ttu-id="caea0-148">Nadat u de nieuwe toepassingsgebruiker in de vorige sectie hebt opgeslagen en gesloten, komt u terug op de pagina **Gebruikerslijst**.</span><span class="sxs-lookup"><span data-stu-id="caea0-148">After you save and close the new application user in the previous section, you're returned to the **Users list** page.</span></span>

1. <span data-ttu-id="caea0-149">Wijzig op de pagina **Gebruikerslijst** de weergave in **Toepassingsgebruikers**.</span><span class="sxs-lookup"><span data-stu-id="caea0-149">On the **Users list** page, change the view to **Application Users**.</span></span>

2. <span data-ttu-id="caea0-150">Selecteer de toepassingsgebruiker die u hebt gemaakt in de vorige sectie.</span><span class="sxs-lookup"><span data-stu-id="caea0-150">Select the application user that you created in the previous section.</span></span>

3. <span data-ttu-id="caea0-151">Selecteer **Rollen beheren** op de werkbalk.</span><span class="sxs-lookup"><span data-stu-id="caea0-151">On the toolbar, select **Manage Roles**.</span></span>

4. <span data-ttu-id="caea0-152">Selecteer de beveiligingsrol die u eerder hebt gemaakt voor de integratie.</span><span class="sxs-lookup"><span data-stu-id="caea0-152">Select the security role that you created earlier for the integration.</span></span>

5. <span data-ttu-id="caea0-153">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="caea0-153">Select **OK**.</span></span>

### <a name="add-an-azure-active-directory-app-in-human-resources"></a><span data-ttu-id="caea0-154">Een Azure Active Directory-app in Human Resources toevoegen</span><span class="sxs-lookup"><span data-stu-id="caea0-154">Add an Azure Active Directory app in Human Resources</span></span>

1. <span data-ttu-id="caea0-155">Open in Dynamics 365 Human Resources de pagina **Azure Active Directory-toepassingen**.</span><span class="sxs-lookup"><span data-stu-id="caea0-155">In Dynamics 365 Human Resources, open the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="caea0-156">Voeg een nieuwe record toe aan de lijst en stel de volgende velden in:</span><span class="sxs-lookup"><span data-stu-id="caea0-156">Add a new record to the list, and set the following fields:</span></span>

    - <span data-ttu-id="caea0-157">**Client-ID**: voer **3a225c96-d62a-44ce-b3ec-bd4e8e9befef** in.</span><span class="sxs-lookup"><span data-stu-id="caea0-157">**Client ID**: Enter **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    - <span data-ttu-id="caea0-158">**Naam**: voer de naam in van de Power Apps-beveiligingsrol die u eerder hebt gemaakt, zoals **HRIS-integratie met LinkedIn Talent Hub**.</span><span class="sxs-lookup"><span data-stu-id="caea0-158">**Name**: Enter the name of the Power Apps security role that you created earlier, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>
    - <span data-ttu-id="caea0-159">**Gebruikers-ID**: selecteer een gebruiker met machtigingen voor het schrijven van gegevens in Personeelsbeheer.</span><span class="sxs-lookup"><span data-stu-id="caea0-159">**User ID**: Select a user who has permissions to write data in Personnel Management.</span></span>

### <a name="create-the-table-in-dataverse"></a><span data-ttu-id="caea0-160">De tabel maken in Dataverse</span><span class="sxs-lookup"><span data-stu-id="caea0-160">Create the table in Dataverse</span></span>

> [!IMPORTANT]
> <span data-ttu-id="caea0-161">De integratie met de LinkedIn Talent Hub is afhankelijk van virtuele tabellen in Dataverse voor Human Resources.</span><span class="sxs-lookup"><span data-stu-id="caea0-161">The integration with LinkedIn Talent Hub depends on virtual tables in Dataverse for Human Resources.</span></span> <span data-ttu-id="caea0-162">Als een voorwaarde voor deze stap in de instellingen moet u virtuele tabellen configureren.</span><span class="sxs-lookup"><span data-stu-id="caea0-162">As a prerequisite for this step in the setup, you must configure virtual tables.</span></span> <span data-ttu-id="caea0-163">Zie [Virtuele tabellen in Dataverse configureren](./hr-admin-integration-common-data-service-virtual-entities.md) voor informatie over het configureren van virtuele tabellen.</span><span class="sxs-lookup"><span data-stu-id="caea0-163">For information about how to configure virtual tables, see [Configure Dataverse virtual tables](./hr-admin-integration-common-data-service-virtual-entities.md).</span></span>

1. <span data-ttu-id="caea0-164">Open in Human Resources de pagina **Integratie met Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="caea0-164">In Human Resources, open the **Dataverse integration** page.</span></span>

2. <span data-ttu-id="caea0-165">Selecteer het tabblad **Virtuele tabellen**.</span><span class="sxs-lookup"><span data-stu-id="caea0-165">Select the **Virtual tables** tab.</span></span>

3. <span data-ttu-id="caea0-166">Filter de lijst met entiteiten op entiteitslabel om te zoeken naar **Geëxporteerde kandidaten voor LinkedIn**.</span><span class="sxs-lookup"><span data-stu-id="caea0-166">Filter the entity list by entity label to find **LinkedIn exported candidate**.</span></span>

4. <span data-ttu-id="caea0-167">Selecteer de entiteit en selecteer vervolgens **Genereren/vernieuwen**.</span><span class="sxs-lookup"><span data-stu-id="caea0-167">Select the entity, and then select **Generate/refresh**.</span></span>

## <a name="exporting-candidate-records"></a><span data-ttu-id="caea0-168">Kandidaatrecords exporteren</span><span class="sxs-lookup"><span data-stu-id="caea0-168">Exporting candidate records</span></span>

<span data-ttu-id="caea0-169">Nadat de instellingen zijn voltooid, kunnen wervers en HR-professionals gebruikmaken van de functie **Exporteren naar HRIS** in LinkedIn Talent Hub om records van aangestelde kandidaten te exporteren vanuit LinkedIn Talent Hub naar Human Resources.</span><span class="sxs-lookup"><span data-stu-id="caea0-169">After the setup is completed, recruiters and human resources (HR) professionals can use the **Export to HRIS** function in LinkedIn Talent Hub to export hired candidate records from LinkedIn Talent Hub to Human Resources.</span></span>

### <a name="export-records-from-linkedin-talent-hub"></a><span data-ttu-id="caea0-170">Records exporteren vanuit LinkedIn Talent Hub</span><span class="sxs-lookup"><span data-stu-id="caea0-170">Export records from LinkedIn Talent Hub</span></span>

<span data-ttu-id="caea0-171">Nadat een kandidaat is verplaatst via het wervingsproces en is aangesteld, kunt u de kandidaatrecord exporteren vanuit LinkedIn Talent Hub naar Human Resources.</span><span class="sxs-lookup"><span data-stu-id="caea0-171">After a candidate has moved through the recruiting process and has been hired, you can export the candidate record from LinkedIn Talent Hub to Human Resources.</span></span>

1. <span data-ttu-id="caea0-172">Open in LinkedIn Talent Hub het project waarvoor u de nieuwe werknemer hebt aangesteld.</span><span class="sxs-lookup"><span data-stu-id="caea0-172">In LinkedIn Talent Hub, open the project that you hired the new employee for.</span></span>

2. <span data-ttu-id="caea0-173">Selecteer een kandidaatrecord.</span><span class="sxs-lookup"><span data-stu-id="caea0-173">Select a candidate record.</span></span>

3. <span data-ttu-id="caea0-174">Selecteer **Fase wijzigen** en selecteer vervolgens **Aangesteld**.</span><span class="sxs-lookup"><span data-stu-id="caea0-174">Select **Change stage**, and then select **Hired**.</span></span>

4. <span data-ttu-id="caea0-175">Selecteer in het menu met het weglatingsteken (**...**) voor de kandidaat de optie **Exporteren naar HRIS**.</span><span class="sxs-lookup"><span data-stu-id="caea0-175">On the ellipsis menu (**...**) for the candidate, select **Export to HRIS**.</span></span>

5. <span data-ttu-id="caea0-176">Voer in het deelvenster **Exporteren naar HRIS** de gegevens in die moeten worden geëxporteerd:</span><span class="sxs-lookup"><span data-stu-id="caea0-176">In the **Export to HRIS** pane, enter the information that must be exported:</span></span>

    - <span data-ttu-id="caea0-177">Selecteer **Microsoft Dynamics 365 Human Resources** in het veld **HRIS-provider**.</span><span class="sxs-lookup"><span data-stu-id="caea0-177">In the **HRIS provider** field, select **Microsoft Dynamics 365 Human Resources**.</span></span>
    - <span data-ttu-id="caea0-178">Selecteer een waarde voor de nieuwe werknemer in het veld **Begindatum**.</span><span class="sxs-lookup"><span data-stu-id="caea0-178">In the **Start date** field, select a value for the new employee.</span></span>
    - <span data-ttu-id="caea0-179">Voer in het veld **Functie** een functie in voor de functie van de nieuwe werknemer.</span><span class="sxs-lookup"><span data-stu-id="caea0-179">In the **Job title** field, enter a job title for the new employee's job.</span></span>
    - <span data-ttu-id="caea0-180">Voer in het veld **Locatie** de locatie in waar de werknemer wordt geplaatst.</span><span class="sxs-lookup"><span data-stu-id="caea0-180">In the **Location** field, enter the location where the employee will be based.</span></span>
    - <span data-ttu-id="caea0-181">Voer het e-mailadres van de werknemer in of verifieer het.</span><span class="sxs-lookup"><span data-stu-id="caea0-181">Enter or verify the employee's email address.</span></span>

![Deelvenster Exporteren naar HRIS in LinkedIn Talent Hub](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a><span data-ttu-id="caea0-183">Onboarding in Human Resources voltooien</span><span class="sxs-lookup"><span data-stu-id="caea0-183">Complete onboarding in Human Resources</span></span>

<span data-ttu-id="caea0-184">Kandidaatrecords die worden geëxporteerd vanuit LinkedIn Talent Hub naar Human Resources, worden weergegeven in de sectie **Aan te stellen kandidaten** op de pagina **Personeelsbeheer**.</span><span class="sxs-lookup"><span data-stu-id="caea0-184">Candidate records that are exported from LinkedIn Talent Hub to Human Resources appear in the **Candidates to hire** section of the **Personnel management** page.</span></span>

1. <span data-ttu-id="caea0-185">Open in Human Resources de pagina **Personeelsbeheer**.</span><span class="sxs-lookup"><span data-stu-id="caea0-185">In Human Resources, open the **Personnel management** page.</span></span>

2. <span data-ttu-id="caea0-186">Selecteer in de sectie **Aan te stellen kandidaten** **Aanstellen** voor de geselecteerde kandidaat.</span><span class="sxs-lookup"><span data-stu-id="caea0-186">In the **Candidates to hire** section, select **Hire** for the selected candidate.</span></span>

3. <span data-ttu-id="caea0-187">Bekijk de record in het dialoogvenster **Nieuwe werknemer aanstellen** en voeg alle vereiste gegevens toe.</span><span class="sxs-lookup"><span data-stu-id="caea0-187">In the **Hire new worker** dialog box, review the record, and add any required information.</span></span> <span data-ttu-id="caea0-188">U kunt ook het positienummer selecteren waarvoor de kandidaat is aangesteld.</span><span class="sxs-lookup"><span data-stu-id="caea0-188">You can also select the position number that the candidate has been hired for.</span></span>

<span data-ttu-id="caea0-189">Nadat u de vereiste informatie hebt ingevoerd, kunt u doorgaan met uw standaardprocessen voor het maken van werknemersrecords en de onboarding van werknemers.</span><span class="sxs-lookup"><span data-stu-id="caea0-189">After the required information has been entered, you can continue with your standard processes for creating employee records and onboarding employees.</span></span>

<span data-ttu-id="caea0-190">De volgende details worden geïmporteerd en opgenomen in de nieuwe werknemersrecord:</span><span class="sxs-lookup"><span data-stu-id="caea0-190">The following details are imported and included on the new employee record:</span></span>

- <span data-ttu-id="caea0-191">Voornaam</span><span class="sxs-lookup"><span data-stu-id="caea0-191">First name</span></span>
- <span data-ttu-id="caea0-192">Achternaam</span><span class="sxs-lookup"><span data-stu-id="caea0-192">Last name</span></span>
- <span data-ttu-id="caea0-193">Begindatum dienstverband</span><span class="sxs-lookup"><span data-stu-id="caea0-193">Employment start date</span></span>
- <span data-ttu-id="caea0-194">E-mailadres</span><span class="sxs-lookup"><span data-stu-id="caea0-194">Email address</span></span>
- <span data-ttu-id="caea0-195">Telefoonnummer</span><span class="sxs-lookup"><span data-stu-id="caea0-195">Phone number</span></span>

## <a name="see-also"></a><span data-ttu-id="caea0-196">Zie ook</span><span class="sxs-lookup"><span data-stu-id="caea0-196">See also</span></span>

[<span data-ttu-id="caea0-197">Virtuele Dataverse-entiteiten configureren</span><span class="sxs-lookup"><span data-stu-id="caea0-197">Configure Dataverse virtual tables</span></span>](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="caea0-198">Wat is Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="caea0-198">What is Microsoft Dataverse?</span></span>](/powerapps/maker/common-data-service/data-platform-intro)


[!INCLUDE[footer-include](../includes/footer-banner.md)]