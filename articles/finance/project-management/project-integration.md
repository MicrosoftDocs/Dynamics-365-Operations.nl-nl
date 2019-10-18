---
title: Microsoft Project-clientintegratie
description: Een projectplanning plannen en onderhouden kan complex zijn, dus hebben projectmanagers hulpmiddelen nodig waarmee ze deze taak kunnen beheren. Integratie met Microsoft Project-client biedt ondersteuning voor het openen en beheren van een projectstructuur voor werkspecificatie.
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 610990612d5fb38025bf39cc648d0c9572da37b6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174807"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="c48c1-104">Microsoft Project-clientintegratie</span><span class="sxs-lookup"><span data-stu-id="c48c1-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c48c1-105">Een projectplanning plannen en onderhouden kan complex zijn, dus hebben projectmanagers hulpmiddelen nodig waarmee ze deze taak kunnen beheren.</span><span class="sxs-lookup"><span data-stu-id="c48c1-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="c48c1-106">Integratie met Microsoft Project-client biedt ondersteuning voor het openen en beheren van een projectstructuur voor werkspecificatie.</span><span class="sxs-lookup"><span data-stu-id="c48c1-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="c48c1-107">De projectmanager kan wijzigingen terug publiceren naar de projectstructuur voor werkspecificatie van Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="c48c1-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="c48c1-108">Als u de update van juli (versie 10.0.4) gebruikt, moet u KB 4054797 en 4055884 installeren.</span><span class="sxs-lookup"><span data-stu-id="c48c1-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="c48c1-109">De invoegtoepassing voor de Microsoft Project-client configureren</span><span class="sxs-lookup"><span data-stu-id="c48c1-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="c48c1-110">Om integratie met de Microsoft Project-client mogelijk te maken, is installatie van een Microsoft Dynamics 365-invoegtoepassing vereist in de Microsoft Project-clienttoepassing van de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="c48c1-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="c48c1-111">Dit wordt gedaan door de **werkruimte Projectbeheer** te openen.</span><span class="sxs-lookup"><span data-stu-id="c48c1-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="c48c1-112">•   Klik op **De invoegtoepassing voor de Microsoft Project-client configureren** vanuit het gedeelte **Koppelingen** > **Instelling** van de werkruimte.</span><span class="sxs-lookup"><span data-stu-id="c48c1-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="c48c1-113">•   Klik op **openen** en klik vervolgens op **Uitvoeren** wanneer dat wordt gevraagd.</span><span class="sxs-lookup"><span data-stu-id="c48c1-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="c48c1-114">Een bestaand concept van een structuur voor werkspecificatie openen en bewerken in de Microsoft project-client</span><span class="sxs-lookup"><span data-stu-id="c48c1-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="c48c1-115">Als een project in Dynamics 365 Finance al een structuur voor werkspecificatie heeft gemaakt, kan de structuur voor werkspecificatie worden geopend in de Microsoft Project Client-toepassing als de structuur voor werkspecificatie de conceptstatus heeft.</span><span class="sxs-lookup"><span data-stu-id="c48c1-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="c48c1-116">Om te openen vanuit de pagina **Project**, klikt u op de koppeling **Openen in Microsoft Project** vanaf het tabblad **Plan**. Deze pagina kan ook worden geopend vanuit de clienttoepassing van Microsoft Project door te klikken op **Openen** op het tabblad **Microsoft Dynamics 365**. Selecteer de **Rechtspersoon** en het **Project** in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c48c1-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="c48c1-117">Als u Internet Explorer als browser gebruikt, moet u klikken op **Opslaan** om handmatig te openen vanuit de locatie waarnaar het bestand is gedownload.</span><span class="sxs-lookup"><span data-stu-id="c48c1-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="c48c1-118">Of klik op **Opslaan en openen** om het bestand te openen in de Microsoft project-client.</span><span class="sxs-lookup"><span data-stu-id="c48c1-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="c48c1-119">Wijzig de bestandsnaam niet bij het opslaan.</span><span class="sxs-lookup"><span data-stu-id="c48c1-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="c48c1-120">Voordat u wijzigingen in het bestand aanbrengt met Microsoft Project Client, moet u het uitchecken. Klik op **Uitchecken** op het tabblad **Microsoft Dynamics 365**. Dit voorkomt dat andere gebruikers de structuur voor werkspecificatie tegelijkertijd bewerken vanuit Finance.</span><span class="sxs-lookup"><span data-stu-id="c48c1-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="c48c1-121">Als u de structuur voor werkspecificatie wilt publiceren na het voltooien van bewerkingen, klikt u op **Inchecken** op het tabblad **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="c48c1-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="c48c1-122">Als een projectteam al is toegevoegd aan het project in Finance, wordt de resourcelijst gevuld met de teamleden.</span><span class="sxs-lookup"><span data-stu-id="c48c1-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="c48c1-123">Als een projectteam nog niet is toegevoegd aan het project, kunt u resources selecteren en het team in de Microsoft Project-client maken door te klikken op de knop **Resources** op het tabblad **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="c48c1-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="c48c1-124">De volgende gegevens worden terug gesynchroniseerd naar Finance als onderdeel van het incheckproces:</span><span class="sxs-lookup"><span data-stu-id="c48c1-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="c48c1-125">•   Taaknaam</span><span class="sxs-lookup"><span data-stu-id="c48c1-125">•   Task name</span></span>

<span data-ttu-id="c48c1-126">•   Begindatum</span><span class="sxs-lookup"><span data-stu-id="c48c1-126">•   Start date</span></span>

<span data-ttu-id="c48c1-127">•   Einddatum</span><span class="sxs-lookup"><span data-stu-id="c48c1-127">•   Finish date</span></span>

<span data-ttu-id="c48c1-128">•   Voorgangers</span><span class="sxs-lookup"><span data-stu-id="c48c1-128">•   Predecessors</span></span>

<span data-ttu-id="c48c1-129">•   Bronnamen</span><span class="sxs-lookup"><span data-stu-id="c48c1-129">•   Resource names</span></span>

<span data-ttu-id="c48c1-130">•   Categorie</span><span class="sxs-lookup"><span data-stu-id="c48c1-130">•   Category</span></span>

<span data-ttu-id="c48c1-131">•   Resourcecategorie</span><span class="sxs-lookup"><span data-stu-id="c48c1-131">•   Resource category</span></span>

<span data-ttu-id="c48c1-132">•   Werkuren</span><span class="sxs-lookup"><span data-stu-id="c48c1-132">•   Work hours</span></span>

<span data-ttu-id="c48c1-133">•   Notities</span><span class="sxs-lookup"><span data-stu-id="c48c1-133">•   Notes</span></span>

<span data-ttu-id="c48c1-134">•   Prioriteit</span><span class="sxs-lookup"><span data-stu-id="c48c1-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="c48c1-135">Als u meer kolommen aan het bestand Microsoft Project-clientbestand toevoegt, worden ze niet naar het bestand opgeslagen en worden ze niet weergegeven als het bestand opnieuw wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="c48c1-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="c48c1-136">De structuur voor werkspecificatie voor een bestaand project maken met behulp van de Microsoft Project-client</span><span class="sxs-lookup"><span data-stu-id="c48c1-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="c48c1-137">Als u een nieuwe structuur voor werkspecificatie wilt maken met Microsoft Project-client, volgt u deze stappen:</span><span class="sxs-lookup"><span data-stu-id="c48c1-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="c48c1-138">Open de Microsoft Project-client.</span><span class="sxs-lookup"><span data-stu-id="c48c1-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="c48c1-139">Klik op het tabblad **Microsoft Dynamics 365** op **Openen**.</span><span class="sxs-lookup"><span data-stu-id="c48c1-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="c48c1-140">Selecteer de **rechtspersoon** voor het project.</span><span class="sxs-lookup"><span data-stu-id="c48c1-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="c48c1-141">Selecteer het **Project**.</span><span class="sxs-lookup"><span data-stu-id="c48c1-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="c48c1-142">Klik op **Uitchecken** op het tabblad **Microsoft Dynamics365**.</span><span class="sxs-lookup"><span data-stu-id="c48c1-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="c48c1-143">Als u klaar bent om te publiceren naar Finance, klikt u op **Inchecken** op het tabblad **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="c48c1-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="c48c1-144">De bestaande structuur voor werkspecificatie voor een bestaand project vervangen met de Microsoft Project-client</span><span class="sxs-lookup"><span data-stu-id="c48c1-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="c48c1-145">Als u een nieuwe structuur voor werkspecificatie wilt maken met behulp van de Microsoft Project-client en een bestaande structuur voor werkspecificatie voor een bestaand project wilt vervangen, gaat u als volgt te werk:</span><span class="sxs-lookup"><span data-stu-id="c48c1-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="c48c1-146">Open de Microsoft Project-client.</span><span class="sxs-lookup"><span data-stu-id="c48c1-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="c48c1-147">Maak de planning in de Microsoft Project-client.</span><span class="sxs-lookup"><span data-stu-id="c48c1-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="c48c1-148">Klik op het tabblad **Microsoft Dynamics 365** op **Wijzigingen opslaan** > **Bestaand project vervangen**.</span><span class="sxs-lookup"><span data-stu-id="c48c1-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="c48c1-149">Selecteer de **rechtspersoon** voor het project.</span><span class="sxs-lookup"><span data-stu-id="c48c1-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="c48c1-150">Selecteer het **Project**.</span><span class="sxs-lookup"><span data-stu-id="c48c1-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="c48c1-151">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="c48c1-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="c48c1-152">Een nieuw project maken vanuit de Microsoft project-client</span><span class="sxs-lookup"><span data-stu-id="c48c1-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="c48c1-153">Open de Microsoft Project-client.</span><span class="sxs-lookup"><span data-stu-id="c48c1-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="c48c1-154">Maak de planning in de Microsoft Project-client.</span><span class="sxs-lookup"><span data-stu-id="c48c1-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="c48c1-155">Klik op het tabblad **Microsoft Dynamics 365** op **Wijzigingen opslaan** > **Opslaan in nieuw project**.</span><span class="sxs-lookup"><span data-stu-id="c48c1-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="c48c1-156">Selecteer de **rechtspersoon** voor het project.</span><span class="sxs-lookup"><span data-stu-id="c48c1-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="c48c1-157">Voer indien nodig de **project-id** in.</span><span class="sxs-lookup"><span data-stu-id="c48c1-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="c48c1-158">Voer de **projectnaam** in.</span><span class="sxs-lookup"><span data-stu-id="c48c1-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="c48c1-159">Selecteer het **projecttype**, de **projectgroep** en de **projectcontract-id**.</span><span class="sxs-lookup"><span data-stu-id="c48c1-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="c48c1-160">U kunt ook een nieuw projectcontract maken door te klikken op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="c48c1-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="c48c1-161">Selecteer de **kalender** die voor resourcing moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c48c1-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="c48c1-162">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="c48c1-162">Click **OK**.</span></span>
