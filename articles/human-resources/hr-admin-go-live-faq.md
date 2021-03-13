---
title: Veelgestelde vragen over go-live
description: Dit onderwerp bevat veelgestelde vragen over hoe u live kunt gaan werken met een Dynamics 365 Human Resources-implementatieproject.
author: rachel-profitt
manager: tfehr
ms.date: 10/13/2020
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
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c5041d515b261bb3e4b14885e0ec0ce788edf729
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112059"
---
# <a name="go-live-faq"></a><span data-ttu-id="5511f-103">Veelgestelde vragen over go-live</span><span class="sxs-lookup"><span data-stu-id="5511f-103">Go-live FAQ</span></span> 

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="5511f-104">Dit onderwerp bevat veelgestelde vragen over hoe u live kunt gaan werken met een Dynamics 365 Human Resources-implementatieproject.</span><span class="sxs-lookup"><span data-stu-id="5511f-104">This topic lists frequently asked questions about how to go live with a Dynamics 365 Human Resources implementation project.</span></span> 

## <a name="when-can-i-configure-and-request-my-production-environment"></a><span data-ttu-id="5511f-105">Wanneer kan ik mijn productieomgeving configureren en aanvragen?</span><span class="sxs-lookup"><span data-stu-id="5511f-105">When can I configure and request my production environment?</span></span> 

<span data-ttu-id="5511f-106">Een productieomgeving wordt meestal geïmplementeerd als aan de volgende criteria is voldaan:</span><span class="sxs-lookup"><span data-stu-id="5511f-106">Typically, a production environment is deployed after meeting the following criteria:</span></span>

- <span data-ttu-id="5511f-107">Voor alle aanpassingen is de code voltooid.</span><span class="sxs-lookup"><span data-stu-id="5511f-107">All customizations are code-complete.</span></span>
- <span data-ttu-id="5511f-108">Acceptatietesten door gebruiker (UAT) zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="5511f-108">User acceptance testing (UAT) is complete.</span></span>
- <span data-ttu-id="5511f-109">De klant heeft zich afgemeld bij de oplossing.</span><span class="sxs-lookup"><span data-stu-id="5511f-109">The customer has signed off on the solution.</span></span>
- <span data-ttu-id="5511f-110">Er zijn geen problemen die het live gaan in de weg staan.</span><span class="sxs-lookup"><span data-stu-id="5511f-110">There are no blocking issues for go-live.</span></span> 

<span data-ttu-id="5511f-111">Wanneer gekwalificeerde klanten zich in deze fase bevinden, werkt het Microsoft FastTrack-team samen met het projectteam om een go-live-beoordeling uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="5511f-111">When qualified customers are at this stage, the Microsoft FastTrack team will work with the project team to do a go-live assessment.</span></span> 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a><span data-ttu-id="5511f-112">Wat zijn de vereisten voor de implementatie van een productieomgeving?</span><span class="sxs-lookup"><span data-stu-id="5511f-112">What are the prerequisites to deploying a production environment?</span></span> 

<span data-ttu-id="5511f-113">Zie  [Voorbereiden op go-live](hr-admin-go-live-prepare.md) voor een lijst met de vereisten.</span><span class="sxs-lookup"><span data-stu-id="5511f-113">For a list of the prerequisites, see [Prepare for go-live](hr-admin-go-live-prepare.md).</span></span> 

## <a name="what-is-a-go-live-assessment"></a><span data-ttu-id="5511f-114">Wat is een go-live-beoordeling?</span><span class="sxs-lookup"><span data-stu-id="5511f-114">What is a go-live assessment?</span></span>  

<span data-ttu-id="5511f-115">De go-live-beoordeling maakt deel uit van het  [Microsoft FastTrack-programma](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview).</span><span class="sxs-lookup"><span data-stu-id="5511f-115">The go-live assessment is part of the [Microsoft FastTrack program](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview).</span></span> <span data-ttu-id="5511f-116">Tijdens deze evaluatie beoordeelt een oplossingsarchitect of een implementatieproject gereed is voor een geslaagde cutover en go-live.</span><span class="sxs-lookup"><span data-stu-id="5511f-116">During this review, a solution architect assesses whether an implementation project is ready for a successful cutover and go-live.</span></span> <span data-ttu-id="5511f-117">Deze evaluatie is verplicht voor elk implementatieproject voordat u in een productieomgeving kunt verzoeken om live te gaan.</span><span class="sxs-lookup"><span data-stu-id="5511f-117">This review is mandatory for every implementation project before you can request to go live in a production environment.</span></span> 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a><span data-ttu-id="5511f-118">Onze Sandbox-omgevingen zijn geïmplementeerd in het Central US-datacenter.</span><span class="sxs-lookup"><span data-stu-id="5511f-118">Our Sandbox environments are deployed in the Central US datacenter.</span></span> <span data-ttu-id="5511f-119">We willen dat onze productieomgevingen in het West US-datacenter worden geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="5511f-119">We want our Production environments to be deployed in the West US datacenter.</span></span> <span data-ttu-id="5511f-120">Kan ik West US als het datacenter selecteren in mijn productieconfiguratie?</span><span class="sxs-lookup"><span data-stu-id="5511f-120">Can I select West US as the datacenter in my Production configuration?</span></span> 

<span data-ttu-id="5511f-121">LCS weerhoudt u er niet van een ander datacenter te selecteren wanneer u een HRM-omgeving implementeert, maar het wordt nadrukkelijk afgeraden om een ander datacenter te selecteren.</span><span class="sxs-lookup"><span data-stu-id="5511f-121">LCS doesn't restrict you from selecting a different data center when you deploy a Human Resources environment, but we strongly recommend not selecting a different data center.</span></span>  

<span data-ttu-id="5511f-122">Als u het West US-datacenter voor uw productieomgeving wilt, moet u eerst uw Sandbox-omgevingen opnieuw implementeren voor het West US-datacenter, deze testen en afmelden.</span><span class="sxs-lookup"><span data-stu-id="5511f-122">If you want your Production environment to be in the West US datacenter, you should first redeploy your Sandbox environments to the West US datacenter, test them, and sign off.</span></span> 

<span data-ttu-id="5511f-123">Zie [Netwerkvereisten](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements#network-requirements) voor informatie over het selecteren van het juiste datacenter.</span><span class="sxs-lookup"><span data-stu-id="5511f-123">For information about selecting the correct datacenter, see [Network requirements](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements#network-requirements).</span></span> 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a><span data-ttu-id="5511f-124">Welk toegangsniveau heb ik nodig voor de Azure-resources voor mijn Human Resources-omgevingen?</span><span class="sxs-lookup"><span data-stu-id="5511f-124">What level of access do I have to the Azure resources for my Human Resources environments?</span></span>  

<span data-ttu-id="5511f-125">De toegang tot de Human Resources-omgevingen is beperkt.</span><span class="sxs-lookup"><span data-stu-id="5511f-125">Access to the Human Resources environments is limited.</span></span> <span data-ttu-id="5511f-126">U hebt geen toegang tot de virtuele machine (VM) of Microsoft internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="5511f-126">You can't access the virtual machine (VM) or Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="5511f-127">U kunt ook geen toegang krijgen tot de database via Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="5511f-127">You also can't access the database through Microsoft SQL Server Management Studio.</span></span> 

<span data-ttu-id="5511f-128">Hoewel u niet direct toegang kunt krijgen tot de Azure-resources of Dynamics 365 Human Resources-omgeving, zijn er aanvullende functies die u kunt gebruiken om toegang te krijgen tot uw gegevens:</span><span class="sxs-lookup"><span data-stu-id="5511f-128">Although you can't access your Azure resources or Dynamics 365 Human Resources environment directly, there are additional features you can use to access your data:</span></span>

- <span data-ttu-id="5511f-129">U kunt een Azure SQL-database implementeren in uw eigen Azure-tenant en de BYOD-functie (Bring Your Own Database) gebruiken om gegevens te synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="5511f-129">You can deploy an Azure SQL database in your own Azure tenant and use the Bring Your Own Database (BYOD) feature to synchronize data.</span></span> <span data-ttu-id="5511f-130">Meer informatie over BYOD vindt u in [Uw eigen database gebruiken (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span><span class="sxs-lookup"><span data-stu-id="5511f-130">For more information, see [Bring your own database (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span></span>

- <span data-ttu-id="5511f-131">U kunt Dataverse-integratie gebruiken om geselecteerde entiteiten te synchroniseren met de Dataverse-database.</span><span class="sxs-lookup"><span data-stu-id="5511f-131">You can use Dataverse integration to synchronize select entities into the Dataverse database.</span></span> <span data-ttu-id="5511f-132">Zie [Dataverse-tabellen](hr-developer-entities.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="5511f-132">For more information, see [Dataverse tables](hr-developer-entities.md).</span></span> 

## <a name="how-often-is-my-production-database-backed-up"></a><span data-ttu-id="5511f-133">Hoe vaak wordt er een back-up van mijn productiedatabase gemaakt?</span><span class="sxs-lookup"><span data-stu-id="5511f-133">How often is my production database backed up?</span></span> 

<span data-ttu-id="5511f-134">Databases worden met de volgende frequenties beschermd door middel van automatische back-ups:</span><span class="sxs-lookup"><span data-stu-id="5511f-134">Databases are protected by automatic backups at the following frequencies:</span></span>

| <span data-ttu-id="5511f-135">Type back-up</span><span class="sxs-lookup"><span data-stu-id="5511f-135">Type of backup</span></span> | <span data-ttu-id="5511f-136">Frequentie</span><span class="sxs-lookup"><span data-stu-id="5511f-136">Frequency</span></span> |
| --- | --- |
| <span data-ttu-id="5511f-137">Volledige databaseback-up</span><span class="sxs-lookup"><span data-stu-id="5511f-137">Full database backup</span></span> | <span data-ttu-id="5511f-138">Wekelijks</span><span class="sxs-lookup"><span data-stu-id="5511f-138">Weekly</span></span> |
| <span data-ttu-id="5511f-139">Differentiële databaseback-up</span><span class="sxs-lookup"><span data-stu-id="5511f-139">Differential database backup</span></span> | <span data-ttu-id="5511f-140">Elke 12-24 uur</span><span class="sxs-lookup"><span data-stu-id="5511f-140">Every 12-24 hours</span></span> |
| <span data-ttu-id="5511f-141">Back-up van transactielogboek</span><span class="sxs-lookup"><span data-stu-id="5511f-141">Transaction log backup</span></span> | <span data-ttu-id="5511f-142">Elke 5 tot 10 minuten</span><span class="sxs-lookup"><span data-stu-id="5511f-142">Every 5 to 10 minutes</span></span> |

<span data-ttu-id="5511f-143">Microsoft bewaart voldoende back-ups zodat PITR (Point in Time Restore) binnen de afgelopen 14 dagen mogelijk is.</span><span class="sxs-lookup"><span data-stu-id="5511f-143">Microsoft retains sufficient backups to allow for Point in Time Restore (PITR) within the last 14 days.</span></span> 

<span data-ttu-id="5511f-144">Zie  [Meer informatie over automatische back-ups van SQL-database](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="5511f-144">For more information, see [Learn about automatic SQL Database backups](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database).</span></span> 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a><span data-ttu-id="5511f-145">Kan ik een kopie van de back-up van mijn productiedatabase aanvragen?</span><span class="sxs-lookup"><span data-stu-id="5511f-145">Can I request a copy of the backup of my production database?</span></span> 

<span data-ttu-id="5511f-146">Nr.</span><span class="sxs-lookup"><span data-stu-id="5511f-146">No.</span></span> <span data-ttu-id="5511f-147">U kunt echter een serviceaanvraag voor het vernieuwen van de database indienen om uw productieomgeving naar uw Sandbox-omgeving te kopiëren.</span><span class="sxs-lookup"><span data-stu-id="5511f-147">You can submit a database refresh service request to copy your Production environment to your Sandbox environment, however.</span></span> <span data-ttu-id="5511f-148">U kunt een Azure SQL-database implementeren in uw eigen Azure-tenant en de BYOD-functie gebruiken om gegevens te synchroniseren vanuit uw productieomgeving.</span><span class="sxs-lookup"><span data-stu-id="5511f-148">You can deploy an Azure SQL database in your own Azure tenant and use the BYOD feature to synchronize data from your Production environment.</span></span> <span data-ttu-id="5511f-149">Meer informatie over BYOD vindt u in [Uw eigen database gebruiken (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span><span class="sxs-lookup"><span data-stu-id="5511f-149">For more information, see [Bring your own database (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span></span> 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a><span data-ttu-id="5511f-150">Hoe verplaats ik mijn Sandbox-omgeving naar productie voor een go-live?</span><span class="sxs-lookup"><span data-stu-id="5511f-150">How do I move my Sandbox environment to Production for go-live?</span></span> 

<span data-ttu-id="5511f-151">Omdat er geen kopieerfunctie beschikbaar is om uw omgeving te verplaatsen vanuit een Sandbox- naar een productieomgeving, moet u gegevenspakketten gebruiken om gegevens naar uw productieomgeving te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="5511f-151">Because a copy feature isn't available to move your environment from a Sandbox to a Production environment, you must use data packages to move data into your Production environment.</span></span>  

<span data-ttu-id="5511f-152">Het is raadzaam een duidelijke lijst met entiteiten die in uw Sandbox zijn geconfigureerd in het hele project bij te houden.</span><span class="sxs-lookup"><span data-stu-id="5511f-152">We recommend maintaining a clear list of entities configured in your Sandbox throughout the project.</span></span> <span data-ttu-id="5511f-153">Test vervolgens het proces van wijziging en migratie van alle gegevenspakketten die nodig zijn voor uw go-live.</span><span class="sxs-lookup"><span data-stu-id="5511f-153">Then test the process of cutover and migration of any data packages needed for your go-live.</span></span> <span data-ttu-id="5511f-154">U moet gegevenspakketten handmatig naar de productieomgeving verplaatsen als u klaar bent om live te gaan.</span><span class="sxs-lookup"><span data-stu-id="5511f-154">You must manually move any data packages into the Production environment when you are ready to go live.</span></span> 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a><span data-ttu-id="5511f-155">Wat moet ik doen als er een storing in mijn productieomgeving is?</span><span class="sxs-lookup"><span data-stu-id="5511f-155">What should I do if my Production environment is down?</span></span> 

<span data-ttu-id="5511f-156">Als u een storing in de productie wilt rapporteren, volgt u het proces dat wordt beschreven in  [Een storing in de productie rapporteren](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage).</span><span class="sxs-lookup"><span data-stu-id="5511f-156">To report a Production outage, follow the process described in [Report a production outage](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage).</span></span> 

 ## <a name="see-also"></a><span data-ttu-id="5511f-157">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5511f-157">See also</span></span>

 [<span data-ttu-id="5511f-158">Voorbereiden voor go-live</span><span class="sxs-lookup"><span data-stu-id="5511f-158">Prepare for go-live</span></span>](hr-admin-go-live-prepare.md)
