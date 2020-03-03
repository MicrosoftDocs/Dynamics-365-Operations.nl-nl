---
title: Human Resources inrichten
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f3a7987a9b385fb6ba0294dc46b0d66be8228f06
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026262"
---
# <a name="provision-human-resources"></a><span data-ttu-id="d5e52-102">Human Resources inrichten</span><span class="sxs-lookup"><span data-stu-id="d5e52-102">Provision Human Resources</span></span>

<span data-ttu-id="d5e52-103">In dit artikel wordt u door het proces van het inrichten van een nieuwe productieomgeving voor Microsoft Dynamics 365 Human Resources geleid.</span><span class="sxs-lookup"><span data-stu-id="d5e52-103">This article walks you through the process of provisioning a new production environment for Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="d5e52-104">In dit artikel wordt ervan uitgegaan dat u Human Resources hebt aangeschaft via een provider van cloudoplossingen of een EA-overeenkomst (Enterprise Architecture).</span><span class="sxs-lookup"><span data-stu-id="d5e52-104">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or enterprise architecture (EA) agreement.</span></span> <span data-ttu-id="d5e52-105">Als u een bestaande Microsoft Dynamics 365-licentie hebt waarin het Human Resources-serviceabonnement al is opgenomen en u de stappen in dit artikel niet kunt voltooien, neemt u contact op met de ondersteuning.</span><span class="sxs-lookup"><span data-stu-id="d5e52-105">If you have an existing Microsoft Dynamics 365 license that already includes the Human Resources service plan, and you can't complete the steps in this article, contact Support.</span></span>

<span data-ttu-id="d5e52-106">Om te beginnen, moet de globale beheerder zich aanmelden bij [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) en een nieuw Human Resources-project maken.</span><span class="sxs-lookup"><span data-stu-id="d5e52-106">To begin, the global administrator should sign in to [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) and create a new Human Resources project.</span></span> <span data-ttu-id="d5e52-107">Tenzij u vanwege een licentieprobleem Human Resources niet kunt inrichten, hebt u geen ondersteuning van vertegenwoordigers van de ondersteuning of DSE (Dynamics Service Engineering) nodig.</span><span class="sxs-lookup"><span data-stu-id="d5e52-107">Unless a licensing issue prevents you from provisioning Human Resource, assistance from Support or Dynamics Service Engineering (DSE) representatives isn't required.</span></span>

## <a name="create-an-lcs-project"></a><span data-ttu-id="d5e52-108">Een LCS-project maken</span><span class="sxs-lookup"><span data-stu-id="d5e52-108">Create an LCS project</span></span>

<span data-ttu-id="d5e52-109">Als u LCS wilt gebruiken om Human Resources-omgevingen te beheren, moet u eerst een LCS-project maken.</span><span class="sxs-lookup"><span data-stu-id="d5e52-109">To use LCS to manage your Human Resources environments, you must first create an LCS project.</span></span>

1. <span data-ttu-id="d5e52-110">Meld u aan bij [LCS](https://lcs.dynamics.com/Logon/Index) met de account waarmee u zich hebt geabonneerd op Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d5e52-110">Sign in to [LCS](https://lcs.dynamics.com/Logon/Index) by using the account that you used to subscribe to Human Resources.</span></span>

2. <span data-ttu-id="d5e52-111">Selecteer het plusteken (**+**) om een project te maken.</span><span class="sxs-lookup"><span data-stu-id="d5e52-111">Select the plus sign (**+**) to create a project.</span></span>

3. <span data-ttu-id="d5e52-112">Selecteer **Microsoft Dynamics 365 Human Resources** als de productnaam en -versie.</span><span class="sxs-lookup"><span data-stu-id="d5e52-112">Select **Microsoft Dynamics 365 Human Resources** as the product name and product version.</span></span>

4. <span data-ttu-id="d5e52-113">Selecteer de **Dynamics 365 Human Resources**-methodologie.</span><span class="sxs-lookup"><span data-stu-id="d5e52-113">Select the **Dynamics 365 Human Resources** methodology.</span></span>

5. <span data-ttu-id="d5e52-114">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="d5e52-114">Select **Create**.</span></span>

<span data-ttu-id="d5e52-115">Zie de **Human Resources**-methodologie die u hebt gemaakt in het nieuwe project voor informatie over hoe u aan de slag gaat met Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d5e52-115">For information about how to get started with Human Resources, see the **Human Resources** methodology that you created in your new project.</span></span> <span data-ttu-id="d5e52-116">Wanneer u het project hebt gemaakt, voert u de volgende procedure uit om uw Human Resources-omgeving in te richten.</span><span class="sxs-lookup"><span data-stu-id="d5e52-116">After you've finished creating the project, complete the following procedure to provision your Human Resources environment.</span></span>

## <a name="provision-a-human-resources-project"></a><span data-ttu-id="d5e52-117">Een Human Resources-project inrichten</span><span class="sxs-lookup"><span data-stu-id="d5e52-117">Provision a Human Resources project</span></span>

<span data-ttu-id="d5e52-118">Nadat u een LCS-project hebt gemaakt, kunt u Human Resources inrichten in een omgeving.</span><span class="sxs-lookup"><span data-stu-id="d5e52-118">After you've created an LCS project, you can provision Human Resources into an environment.</span></span>

1. <span data-ttu-id="d5e52-119">Selecteer in uw LCS-project de tegel **Beheer Human Resources-app**.</span><span class="sxs-lookup"><span data-stu-id="d5e52-119">In your LCS project, select the **Human Resources App Management** tile.</span></span>

2. <span data-ttu-id="d5e52-120">Geef aan of dit een sandbox- of productie-exemplaar van Human Resources is.</span><span class="sxs-lookup"><span data-stu-id="d5e52-120">Indicate whether this is a Sandbox or Production instance of Human Resource.</span></span> <span data-ttu-id="d5e52-121">Vroege previewfuncties kunnen beschikbaar zijn in sandbox-exemplaren om in een vroeg stadium feedback te krijgen en tests uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="d5e52-121">Early preview features may be available in Sandbox instances to allow for early feedback and testing.</span></span>
   
    > [!NOTE]
    > <span data-ttu-id="d5e52-122">Het exemplaartype voor Talent kan niet meer dan één keer worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="d5e52-122">The Talent instance type cannot be changed once set.</span></span> <span data-ttu-id="d5e52-123">Controleer of het juiste exemplaartype is geselecteerd voordat u doorgaat.</span><span class="sxs-lookup"><span data-stu-id="d5e52-123">Verify the correct instance type is selected before continuing.</span></span></br></br>
    > <span data-ttu-id="d5e52-124">Het Human Resources-exemplaar type staat los van het exemplaartype van de Microsoft Power Apps-omgeving dat u instelt in het Power Apps-beheercentrum.</span><span class="sxs-lookup"><span data-stu-id="d5e52-124">The Human Resources instance type is separate from the instance type of the Microsoft Power Apps environment, which you set in the Power Apps Admin center.</span></span>
    
3. <span data-ttu-id="d5e52-125">Selecteer de optie **Demogegevens opnemen** als u wilt dat in uw omgeving dezelfde demogegevensset wordt opgenomen die is gebruikt in de Human Resources-testdrive.</span><span class="sxs-lookup"><span data-stu-id="d5e52-125">Select the **Include Demo Data** option if you want your environment to include the same demo data set used in the Human Resources Test Drive experience.</span></span> <span data-ttu-id="d5e52-126">Dit is nuttig voor de langetermijndemo of -trainingsomgevingen en mag nooit worden gebruikt voor productieomgevingen.</span><span class="sxs-lookup"><span data-stu-id="d5e52-126">This is beneficial for long-term demo or training environments, and should never be used for production environments.</span></span>  <span data-ttu-id="d5e52-127">Houd er rekening mee dat u deze optie bij de aanvankelijke implementatie moet kiezen.</span><span class="sxs-lookup"><span data-stu-id="d5e52-127">Note that you must choose this option upon initial deployment.</span></span> <span data-ttu-id="d5e52-128">U kunt een bestaande implementatie niet later bijwerken.</span><span class="sxs-lookup"><span data-stu-id="d5e52-128">You cannot update an existing deployment later.</span></span>

4. <span data-ttu-id="d5e52-129">Human Resources wordt altijd ingericht in een Microsoft Power Apps-omgeving om de Power Apps-integratie en -uitbreidbaarheid mogelijk te maken.</span><span class="sxs-lookup"><span data-stu-id="d5e52-129">Human Resources is always provisioned into a Microsoft Power Apps environment to enable Power Apps integration and extensibility.</span></span> <span data-ttu-id="d5e52-130">Lees de sectie 'Een Power Apps-omgeving selecteren' van dit artikel voor u doorgaat.</span><span class="sxs-lookup"><span data-stu-id="d5e52-130">Read the “Selecting a Power Apps environment” section of this article before you continue.</span></span> <span data-ttu-id="d5e52-131">Als u nog geen Power Apps-omgeving hebt, selecteert u Omgevingen beheren in LCS of gaat u naar het Power Apps-beheercentrum.</span><span class="sxs-lookup"><span data-stu-id="d5e52-131">If you don't already have a Power Apps environment, select Manage environments in LCS or navigate to the Power Apps Admin center.</span></span> <span data-ttu-id="d5e52-132">Volg daarna de stappen voor [Een Power Apps-omgeving maken](https://docs.microsoft.com/powerapps/administrator/create-environment).</span><span class="sxs-lookup"><span data-stu-id="d5e52-132">Then follow the steps to [Create a Power Apps environment](https://docs.microsoft.com/powerapps/administrator/create-environment).</span></span>

    > [!NOTE]
    > <span data-ttu-id="d5e52-133">Om bestaande omgevingen weer te geven of nieuwe omgevingen te maken, moet de tenantbeheerder die Human Resources inricht, worden toegewezen aan de Power Apps P2-licentie.</span><span class="sxs-lookup"><span data-stu-id="d5e52-133">To view existing environments or create new environments, the tenant admin who provisions Human Resources must be assigned to the Power Apps P2 license.</span></span> <span data-ttu-id="d5e52-134">Als uw organisatie geen Power Apps P2-licentie heeft, kunt u er een krijgen van uw provider van cloudoplossingen of downloaden via de [pagina met Power Apps-prijzen](https://powerapps.microsoft.com/pricing/).</span><span class="sxs-lookup"><span data-stu-id="d5e52-134">If your organization doesn't have a Power Apps P2 license, you can get one from your CSP or from the [Power Apps pricing page](https://powerapps.microsoft.com/pricing/).</span></span>

5. <span data-ttu-id="d5e52-135">Selecteer de omgeving waarin Human Resources moet worden ingericht.</span><span class="sxs-lookup"><span data-stu-id="d5e52-135">Select the environment to provision Human Resources into.</span></span>

6. <span data-ttu-id="d5e52-136">Selecteer **Ja** om akkoord te gaan met de voorwaarden en te beginnen met implementeren.</span><span class="sxs-lookup"><span data-stu-id="d5e52-136">Select **Yes** to agree to the terms and begin deployment.</span></span>

   <span data-ttu-id="d5e52-137">Uw nieuwe omgeving wordt weergegeven in de lijst met omgevingen in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="d5e52-137">Your new environment appears in the list of environments in the navigation pane on the left.</span></span> <span data-ttu-id="d5e52-138">U kunt de omgeving echter pas gebruiken als de implementatiestatus is bijgewerkt naar **Geïmplementeerd**.</span><span class="sxs-lookup"><span data-stu-id="d5e52-138">However, you can't start to use the environment until the deployment status is updated to **Deployed**.</span></span> <span data-ttu-id="d5e52-139">Dit proces duurt meestal een paar minuten.</span><span class="sxs-lookup"><span data-stu-id="d5e52-139">This process typically takes a few minutes.</span></span> <span data-ttu-id="d5e52-140">Als het inrichtingsproces mislukt, moet u contact opnemen met de ondersteuning.</span><span class="sxs-lookup"><span data-stu-id="d5e52-140">If the provisioning process is unsuccessful, you must contact Support.</span></span>

7. <span data-ttu-id="d5e52-141">Selecteer **Aanmelden bij Human Resources** om uw nieuwe omgeving te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="d5e52-141">Select **Log on to Human Resource** to use your new environment.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d5e52-142">Als u de definitieve vereisten nog niet hebt goedgekeurd, kunt u een testexemplaar van Human Resources in het project implementeren.</span><span class="sxs-lookup"><span data-stu-id="d5e52-142">If you haven't yet signed off on the final requirements, you can deploy a test instance of Human Resources in the project.</span></span> <span data-ttu-id="d5e52-143">Vervolgens kunt u deze instantie gebruiken om uw oplossing te testen tot u uw goedkeuring geeft.</span><span class="sxs-lookup"><span data-stu-id="d5e52-143">You can then use this instance to test your solution until you sign off.</span></span> <span data-ttu-id="d5e52-144">Als u uw nieuwe omgeving voor tests gebruikt, moet u deze procedure herhalen om een productieomgeving te maken.</span><span class="sxs-lookup"><span data-stu-id="d5e52-144">If you use your new environment for testing, you must repeat this procedure to create a production environment.</span></span>

    > <span data-ttu-id="d5e52-145">Omdat er slechts twee LCS-omgevingen zijn toegestaan als onderdeel van het Human Resources-abonnement, kunt u ook overwegen gebruik te maken van gratis 60 dagen [Human Resources-proefomgeving](https://dynamics.microsoft.com/talent/overview/).</span><span class="sxs-lookup"><span data-stu-id="d5e52-145">Because only two LCS environments are allowed as part of the Human Resources subscription, you might consider leveraging a free 60-day [Human Resources trial environment](https://dynamics.microsoft.com/talent/overview/).</span></span> <span data-ttu-id="d5e52-146">Hoewel een proefomgeving eigendom is van de gebruiker die hierom heeft verzocht, kunnen andere gebruikers worden uitgenodigd via de systeembeheerervaring voor Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d5e52-146">Although a trial environment is owned by the user who requested it, other users can be invited through the system administration experience for Human Resources.</span></span> <span data-ttu-id="d5e52-147">Proefomgevingen bevatten fictieve gegevens die kunnen worden gebruikt om het programma op een veilige manier te verkennen.</span><span class="sxs-lookup"><span data-stu-id="d5e52-147">Trial environments contain fictitious data that can be used to explore the program in a safe manner.</span></span> <span data-ttu-id="d5e52-148">Ze zijn niet bedoeld als productieomgevingen.</span><span class="sxs-lookup"><span data-stu-id="d5e52-148">They aren't intended to be used as production environments.</span></span> <span data-ttu-id="d5e52-149">Wanneer een proefomgeving na 60 dagen verloopt, worden alle gegevens erin permanent verwijderd.</span><span class="sxs-lookup"><span data-stu-id="d5e52-149">Note that when a trial environment expires after 60 days, all the data that's in it is deleted and can't be recovered.</span></span> <span data-ttu-id="d5e52-150">Nadat de bestaande omgeving is verlopen, kunt u zich aanmelden voor een nieuwe proefomgeving.</span><span class="sxs-lookup"><span data-stu-id="d5e52-150">You can sign up for a new trial environment after the existing environment expires.</span></span>

## <a name="select-a-power-apps-environment"></a><span data-ttu-id="d5e52-151">Een Power Apps-omgeving selecteren</span><span class="sxs-lookup"><span data-stu-id="d5e52-151">Select a Power Apps environment</span></span>

<span data-ttu-id="d5e52-152">Dankzij de integratie tussen Human Resources en de Power Apps-omgevingen kunt u Human Resources-gegevens integreren en het gebruik ervan uitbreiden met Power Apps-tools.</span><span class="sxs-lookup"><span data-stu-id="d5e52-152">The integration between Human Resources and the Power Apps environments lets you integrate and extend the use of Human Resources data using Power Apps tools.</span></span> <span data-ttu-id="d5e52-153">Informatie over dat het doel van Power Apps-omgevingen helpt niet alleen bij het maken van toepassingen om Human Resources uit te breiden, maar ook bij het selecteren van de juiste omgeving voor Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d5e52-153">Understanding the purpose of Power Apps environments will not only help you build apps to extend Human Resource, but will also help you select the correct environment when provisioning Human Resource.</span></span> <span data-ttu-id="d5e52-154">Zie voor meer informatie over Power Apps-omgevingen, inclusief het omgevingsbereik, omgevingstoegang en het maken en kiezen van een omgeving [Aankondiging van Power Apps-omgevingen](https://powerapps.microsoft.com/blog/powerapps-environments/).</span><span class="sxs-lookup"><span data-stu-id="d5e52-154">For information about Power Apps environments, including environment scope, environment access, and creating and choosing an environment, see [Announcing Power Apps environments](https://powerapps.microsoft.com/blog/powerapps-environments/).</span></span> 

<span data-ttu-id="d5e52-155">Gebruik de volgende richtlijnen bij het bepalen in welke Power Apps-omgeving u Human Resources wilt implementeren:</span><span class="sxs-lookup"><span data-stu-id="d5e52-155">Use the following guidance when determining which Power Apps environment to deploy Human Resources into:</span></span> 

1. <span data-ttu-id="d5e52-156">Selecteer in LCS **Omgevingen beheren** of ga rechtstreeks naar het Power Apps-beheercentrum waar u bestaande omgevingen weergeeft en nieuwe omgevingen maakt.</span><span class="sxs-lookup"><span data-stu-id="d5e52-156">In LCS, select **Manage environments**, or go directly to the Power Apps Admin center where you can view existing environments and create new environments.</span></span>

2. <span data-ttu-id="d5e52-157">Eén Human Resources-omgeving wordt toegewezen aan één Power Apps-omgeving.</span><span class="sxs-lookup"><span data-stu-id="d5e52-157">A single Human Resources environment is mapped to a single Power Apps environment.</span></span>

3. <span data-ttu-id="d5e52-158">Een Power Apps-omgeving bevat de toepassing Human Resources samen met de bijbehorende Power Apps-, Power Automate- en Common Data Service-toepassingen.</span><span class="sxs-lookup"><span data-stu-id="d5e52-158">A Power Apps environment contains Human Resources, along with the corresponding Power Apps, Power Automate, and Common Data Service applications.</span></span> <span data-ttu-id="d5e52-159">Als de Power Apps-omgeving wordt verwijderd, worden ook de toepassingen erin gewist.</span><span class="sxs-lookup"><span data-stu-id="d5e52-159">If the Power Apps environment is deleted, so are the apps within it.</span></span> <span data-ttu-id="d5e52-160">Tijdens het inrichten van een Human Resources-omgeving kunt u een omgeving **Proef** of **Productie** inrichten.</span><span class="sxs-lookup"><span data-stu-id="d5e52-160">When provisioning a Human Resources environment, you can provision either a **Trial** or **Production** environment.</span></span> <span data-ttu-id="d5e52-161">Kies het type omgeving op basis van hoe de omgeving wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d5e52-161">Choose the type of environment based on how the environment will be used.</span></span> 

4. <span data-ttu-id="d5e52-162">Gegevensintegratie en teststrategieën moeten worden overwogen, zoals Sandbox, UAT of Productie.</span><span class="sxs-lookup"><span data-stu-id="d5e52-162">Data integration and testing strategies should be considered, such as Sandbox, UAT, or Production.</span></span> <span data-ttu-id="d5e52-163">Het is raadzaam dat u rekening houdt met de verschillende gevolgen voor uw implementatie, aangezien de toewijzing van een Human Resources-omgeving aan een Power Apps-omgeving later niet eenvoudig te wijzigen is.</span><span class="sxs-lookup"><span data-stu-id="d5e52-163">We recommend that you consider the various implications for your deployment, because it isn't easy to later change which Human Resources environment is mapped to a Power Apps environment.</span></span>

5. <span data-ttu-id="d5e52-164">De volgende Power Apps-omgevingen kunnen niet worden gebruikt voor Human Resources en worden gefilterd in de selectielijst binnen LCS:</span><span class="sxs-lookup"><span data-stu-id="d5e52-164">The following Power Apps environments cannot be used for Human Resources and will be filtered from the selection list within LCS:</span></span>
 
    - <span data-ttu-id="d5e52-165">**Standaard Power Apps-omgevingen** - hoewel elke tenant automatisch een standaard Power Apps-omgeving heeft, wordt gebruik niet aanbevolen met Human Resources omdat alle tenantgebruikers toegang hebben tot de Power Apps-omgeving. Ze kunnen bij het testen en verkennen van de Power Apps- of Power Automate-integraties per ongeluk productiegegevens beschadigen.</span><span class="sxs-lookup"><span data-stu-id="d5e52-165">**Default Power Apps environments** - Although each tenant is automatically provisioned with a default Power Apps environment, we don't recommend using them with Human Resources because all tenant users have access to the Power Apps environment and could unintentionally corrupt production data when testing and exploring with Power Apps or Power Automate integrations.</span></span>
   
    - <span data-ttu-id="d5e52-166">**Proefomgevingen** - deze omgevingen worden gemaakt met een vervaldatum en verlopen na die tijd, waardoor uw omgeving en alle Human Resources-exemplaren in de omgeving automatisch worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="d5e52-166">**Trial environments** - These environments are created with an expiration date and will expire after that time, causing your environment and any Human Resources instances contained within to be removed automatically.</span></span>
   
    - <span data-ttu-id="d5e52-167">**Niet-ondersteunde regio's** - momenteel wordt Human Resources alleen ondersteund in de volgende gebieden: Verenigde Staten, Europa, Verenigd Koninkrijk, Australië, Canada en Azië.</span><span class="sxs-lookup"><span data-stu-id="d5e52-167">**Unsupported regions** - Currently Human Resources is only supported in the following regions: United States, Europe, United Kingdom, Australia, Canada and Asia.</span></span>
  
6. <span data-ttu-id="d5e52-168">Nadat u hebt vastgesteld welke omgeving de juiste is om te gebruiken, kunt u doorgaan met het inrichtingsproces.</span><span class="sxs-lookup"><span data-stu-id="d5e52-168">After you have determined the correct environment to use, you can continue with the provisioning process.</span></span> 
 
## <a name="grant-access-to-the-environment"></a><span data-ttu-id="d5e52-169">Toegang verlenen tot de omgeving</span><span class="sxs-lookup"><span data-stu-id="d5e52-169">Grant access to the environment</span></span>

<span data-ttu-id="d5e52-170">Standaard heeft de globale beheerder die de omgeving heeft gemaakt toegang tot deze omgeving.</span><span class="sxs-lookup"><span data-stu-id="d5e52-170">By default, the global administrator who created the environment has access to it.</span></span> <span data-ttu-id="d5e52-171">Aan alle overige gebruikers van de toepassing moet echter uitdrukkelijk toestemming worden verleend.</span><span class="sxs-lookup"><span data-stu-id="d5e52-171">However, additional application users must be explicitly granted access.</span></span> <span data-ttu-id="d5e52-172">Om toegang te verlenen moet u gebruikers toevoegen en de juiste rollen aan deze gebruikers toewijzen in de Human Resources-omgeving.</span><span class="sxs-lookup"><span data-stu-id="d5e52-172">To grant access, you need to add users and assign the appropriate roles to them in the Human Resources environment.</span></span> <span data-ttu-id="d5e52-173">De globale beheerder die Human Resources heeft geïmplementeerd, moet ook Attract en Onboard starten om de initialisatie te voltooien en toegang in te schakelen voor andere tenantgebruikers.</span><span class="sxs-lookup"><span data-stu-id="d5e52-173">The global administrator that deployed Human Resources must also launch both Attract and Onboard to complete the initialization and enable access for other tenant users.</span></span>  <span data-ttu-id="d5e52-174">Totdat dit gebeurt, kunnen andere gebruikers geen toegang krijgen tot Attract en Onboard en krijgen ze toegangsovertredingsfouten.</span><span class="sxs-lookup"><span data-stu-id="d5e52-174">Until this happens, other users will not be able to access Attract and Onboard and will get access violation errors.</span></span> <span data-ttu-id="d5e52-175">Zie voor meer informatie [Nieuwe gebruikers maken](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) en [Gebruikers toewijzen aan beveiligingsrollen](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles).</span><span class="sxs-lookup"><span data-stu-id="d5e52-175">For more information, see [Create new users](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) and [Assign users to security roles](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles).</span></span> 