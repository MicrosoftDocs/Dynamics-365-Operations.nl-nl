---
title: Talent uitbreiden met Power Apps en Power Automate
description: In dit artikel worden enkele voorbeelden beschreven van uitbreidbaarheidsscenario's voor Microsoft Dynamics 365 Talent Attract die gebruikmaken van Microsoft Power Apps en Microsoft Power Automate.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: cfdf36e9486aa4853d3bf674afa73ec3a4d1c161
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529629"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a><span data-ttu-id="dbe7f-103">Talent uitbreiden met Power Apps en Power Automate</span><span class="sxs-lookup"><span data-stu-id="dbe7f-103">Extend Talent with Power Apps and Power Automate</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="dbe7f-104">In dit artikel worden enkele voorbeelden beschreven van uitbreidbaarheidsscenario's voor Microsoft Dynamics 365 Talent: Attract die gebruikmaken van Microsoft Power Apps en Microsoft Power Automate.</span><span class="sxs-lookup"><span data-stu-id="dbe7f-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Talent: Attract that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="dbe7f-105">U kunt het oplossingspakket importeren dat is gekoppeld aan elk voorbeeld in uw Power Apps-omgeving.</span><span class="sxs-lookup"><span data-stu-id="dbe7f-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="dbe7f-106">Vervolgens kunt u de pakketten als richtlijn of als beginpunt gebruiken voor het implementeren van scenario's die van toepassing op uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="dbe7f-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dbe7f-107">Als u de sjablonen en app die worden beschreven in dit artikel, 'as is' wilt gebruiken, moet u ze testen om er zeker van te zijn dat ze betrekking hebben op alle scenario's die specifiek voor uw implementatie zijn.</span><span class="sxs-lookup"><span data-stu-id="dbe7f-107">If you want to use the templates and app that are described in this article "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="dbe7f-108">Vereisten</span><span class="sxs-lookup"><span data-stu-id="dbe7f-108">Prerequisites</span></span>

- <span data-ttu-id="dbe7f-109">Als u wilt pakketten wilt importeren, moeten gebruikers beschikken over de machtiging **Maker omgeving** beschikken.</span><span class="sxs-lookup"><span data-stu-id="dbe7f-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="dbe7f-110">Als u apps wilt exporteren of importeren, moeten gebruikers een Power Apps Plan 2-licentie of een proeflicentie van Power Apps Plan 2 hebben.</span><span class="sxs-lookup"><span data-stu-id="dbe7f-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="power-automate--form-connect"></a><span data-ttu-id="dbe7f-111">Power Automate: formulier verbinden</span><span class="sxs-lookup"><span data-stu-id="dbe7f-111">Power Automate – Form Connect</span></span>

<span data-ttu-id="dbe7f-112">De sjabloon **Power Automate: formulier verbinden** kan worden gebruikt om gegevens vanuit Microsoft Forms te lezen en deze op te slaan in een Common Data Service-entiteit.</span><span class="sxs-lookup"><span data-stu-id="dbe7f-112">The **Power Automate – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="dbe7f-113">Deze sjabloon kan worden uitgebreid, zodat deze kan worden gebruikt voor andere scenario's.</span><span class="sxs-lookup"><span data-stu-id="dbe7f-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="dbe7f-114">Hieronder vindt u enkele voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="dbe7f-114">Here are some examples:</span></span>

- <span data-ttu-id="dbe7f-115">Kandidaatbeoordelingen vastleggen.</span><span class="sxs-lookup"><span data-stu-id="dbe7f-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="dbe7f-116">Resultaten van cursusvragenlijsten vastleggen.</span><span class="sxs-lookup"><span data-stu-id="dbe7f-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="dbe7f-117">Een bibliotheek samenstellen van sollicitatiegesprekvragen voor beheerders van Human resources (HR).</span><span class="sxs-lookup"><span data-stu-id="dbe7f-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="dbe7f-118">De evaluatie van een kandidaat van het sollicitatiegesprekproces vastleggen.</span><span class="sxs-lookup"><span data-stu-id="dbe7f-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="dbe7f-119">In Microsoft Dynamics 365: Attract kunt u formulieren gebruiken in de portal Kandidaat, waar kandidaten details invullen.</span><span class="sxs-lookup"><span data-stu-id="dbe7f-119">In Microsoft Dynamics 365: Attract, you can use forms in the candidate portal, where candidates fill in details.</span></span> <span data-ttu-id="dbe7f-120">U kunt ook formulieren insluiten als activiteiten in een functiesjabloon.</span><span class="sxs-lookup"><span data-stu-id="dbe7f-120">You can also embed forms as activities in a job template.</span></span>

<span data-ttu-id="dbe7f-121">Wanneer een kandidaat een formulier indient, wordt in Microsoft Power Automate de formulierindiening vastgelegd en worden de gegevens gelezen en opgeslagen in de Common Data Service-entiteit.</span><span class="sxs-lookup"><span data-stu-id="dbe7f-121">When a candidate submits a form, Microsoft Power Automate captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="dbe7f-122">Voor het downloaden van de sjabloon **Power Automate: formulier verbinden** en de structuur van aangepaste entiteiten gaat u naar [Power Automate: formulier verbinden](https://go.microsoft.com/fwlink/?linkid=2081988) in het Microsoft Downloadcentrum.</span><span class="sxs-lookup"><span data-stu-id="dbe7f-122">To download the **Power Automate – Form Connect** template and Custom Entity Structure, go to [Power Automate – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sharepoint-integration"></a><span data-ttu-id="dbe7f-123">Power Automate: SharePoint-integratie</span><span class="sxs-lookup"><span data-stu-id="dbe7f-123">Power Automate – SharePoint Integration</span></span>

<span data-ttu-id="dbe7f-124">De sjabloon **Power Automate: SharePoint-integratie** kan worden gebruikt voor het lezen van gegevens vanuit een Microsoft SharePoint-lijst, voor het vergelijken van de lijst met veldwaarden voor elke Common Data Service-entiteit en voor het verzenden van de resultaten van de vergelijking als een melding per e-mail.</span><span class="sxs-lookup"><span data-stu-id="dbe7f-124">The **Power Automate – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="dbe7f-125">Een organisatie kan een set vaardigheden dringend nodig hebben.</span><span class="sxs-lookup"><span data-stu-id="dbe7f-125">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="dbe7f-126">Deze vaardigheden kunnen zijn opgeslagen in SharePoint als een SharePoint-lijst.</span><span class="sxs-lookup"><span data-stu-id="dbe7f-126">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="dbe7f-127">Wanneer een kandidaat solliciteert op een functie waarvoor een set vereiste vaardigheden wordt vermeld en de vaardigheden van de kandidaat en de vaardigheden die zijn opgeslagen in SharePoint, grotendeels overeenkomen, wordt een melding per e-mail wordt verzonden.</span><span class="sxs-lookup"><span data-stu-id="dbe7f-127">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="dbe7f-128">Dit helpt dringende posities sneller in te vullen, omdat de wervers met de meldingen kandidaten sneller kunnen bereiken en aanstellen in de hele organisatie.</span><span class="sxs-lookup"><span data-stu-id="dbe7f-128">This helps fill positions that are urgently required faster, because the notifications help recruiters cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="dbe7f-129">Deze sjabloon kan worden uitgebreid, zodat deze kan worden gebruikt voor elk scenario dat betrekking heeft op SharePoint-integratie.</span><span class="sxs-lookup"><span data-stu-id="dbe7f-129">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="dbe7f-130">Voor het downloaden van de sjabloon **Power Automate: SharePoint-integratie** gaat u naar [Power Automate: SharePoint-integratie](https://go.microsoft.com/fwlink/?linkid=2082109) in het Microsoft Downloadcentrum.</span><span class="sxs-lookup"><span data-stu-id="dbe7f-130">To download the **Power Automate – SharePoint Integration** template, go to [Power Automate – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="referral-app"></a><span data-ttu-id="dbe7f-131">De app Referral</span><span class="sxs-lookup"><span data-stu-id="dbe7f-131">Referral App</span></span>

<span data-ttu-id="dbe7f-132">U kunt de app Referral gebruiken om kandidaten toe te voegen aan een gedeelde talentenpool.</span><span class="sxs-lookup"><span data-stu-id="dbe7f-132">You can use the Referral App to add candidates to a shared talent pool.</span></span> <span data-ttu-id="dbe7f-133">De verwijzer kan waarden voor **Voornaam**, **Achternaam**, **E-mail** en **Linkedln-URL** opgeven bij het indienen van een kandidaat.</span><span class="sxs-lookup"><span data-stu-id="dbe7f-133">The referrer can enter **Firstname**, **Lastname**, **Email**, and **LinkedIn URL** when submitting a candidate.</span></span> <span data-ttu-id="dbe7f-134">De bronmetagegevens van de kandidaat worden vervolgens gevuld met de gegevens van de verwijzer.</span><span class="sxs-lookup"><span data-stu-id="dbe7f-134">The candidate source metadata is then populated with the referrer’s information.</span></span>

<span data-ttu-id="dbe7f-135">U kunt deze app insluiten in Werknemerselfservice voor het indienen van verwijzingen of u kunt deze app als hyperlink gebruiken in de bedrijfsportal en uitvoeren als een zelfstandige app.</span><span class="sxs-lookup"><span data-stu-id="dbe7f-135">You can embed this app in Employee self service for submitting referrals, or you can use it as a hyperlink in the corporate portal and run it as a stand-alone app.</span></span>

<span data-ttu-id="dbe7f-136">Als u de app **Referral** wil downloaden, gaat u naar [Dynamics 365 Talent extensibility solution: Referral App](https://www.microsoft.com/download/details.aspx?id=58497) in het Microsoft Downloadcentrum.</span><span class="sxs-lookup"><span data-stu-id="dbe7f-136">To download **Referral App**, go to [Dynamics 365 Talent extensibility solution: Referral App](https://www.microsoft.com/download/details.aspx?id=58497) on the Microsoft Download Center.</span></span> <span data-ttu-id="dbe7f-137">U kunt deze app importeren en aanpassen om extra functionaliteit toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="dbe7f-137">You can import this app and customize it to add additional functionality.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dbe7f-138">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="dbe7f-138">Additional resources</span></span>

[<span data-ttu-id="dbe7f-139">Het Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="dbe7f-139">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[<span data-ttu-id="dbe7f-140">App tussen tenants en omgevingen migreren</span><span class="sxs-lookup"><span data-stu-id="dbe7f-140">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
