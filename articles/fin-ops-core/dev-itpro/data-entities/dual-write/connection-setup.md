---
title: Ondersteunde scenario's met instellingen voor twee keer wegschrijven
description: In dit onderwerp worden de scenario's beschreven die worden ondersteund voor instellingen voor twee keer wegschrijven.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 1319f1228b635e207754f7c2516cb2b5353a9edd
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112416"
---
# <a name="supported-scenarios-for-dual-write-setup"></a><span data-ttu-id="aa3f6-103">Ondersteunde scenario's met instellingen voor twee keer wegschrijven</span><span class="sxs-lookup"><span data-stu-id="aa3f6-103">Supported scenarios for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="aa3f6-104">U kunt een verbinding voor twee keer wegschrijven instellen tussen een Finance and Operations-omgeving en een Common Data Service-omgeving.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="aa3f6-105">Een **Finance and Operations-omgeving** levert het onderliggende platform voor **Finance and Operations-apps** (bijvoorbeeld Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Retail en Dynamics 365 Human Resources).</span><span class="sxs-lookup"><span data-stu-id="aa3f6-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Retail, and Dynamics 365 Human Resources).</span></span>
+ <span data-ttu-id="aa3f6-106">Een **Common Data Service-omgeving** biedt het onderliggende platform voor **modelgestuurde apps in Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing en Dynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="aa3f6-106">A **Common Data Service environment** provides the underlying platform for **model-driven apps in Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

<span data-ttu-id="aa3f6-107">Het installatiemechanisme varieert afhankelijk van uw abonnement en de omgeving.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-107">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="aa3f6-108">Voor nieuwe exemplaren van Finance and Operations-apps begint het instellen van een verbinding voor twee keer wegschrijven met Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="aa3f6-108">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="aa3f6-109">Als u een licentie hebt voor Microsoft Power Platform, krijgt u een nieuwe Common Data Service-omgeving als uw tenant er geen heeft.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-109">If you have a license for Microsoft Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="aa3f6-110">Voor bestaande exemplaren van Finance and Operations-apps begint het instellen van een verbinding voor twee keer wegschrijven in de Finance and Operations-omgeving.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-110">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="aa3f6-111">De volgende scenario's met instellingen worden ondersteund:</span><span class="sxs-lookup"><span data-stu-id="aa3f6-111">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="aa3f6-112">Een nieuw Finance and Operations-app-exemplaar en een nieuw, model gestuurd app-exemplaar</span><span class="sxs-lookup"><span data-stu-id="aa3f6-112">A new Finance and Operations app instance and a new model-driven app instance</span></span>](#new-new)
+ [<span data-ttu-id="aa3f6-113">Een nieuw Finance and Operations-app-exemplaar en een bestaand, model gestuurd app-exemplaar</span><span class="sxs-lookup"><span data-stu-id="aa3f6-113">A new Finance and Operations app instance and an existing model-driven app instance</span></span>](#new-existing)
+ [<span data-ttu-id="aa3f6-114">Een nieuw Finance and Operations-app-exemplaar met demogegevens en een nieuw, model gestuurd app-exemplaar</span><span class="sxs-lookup"><span data-stu-id="aa3f6-114">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>](#new-demo-new)
+ [<span data-ttu-id="aa3f6-115">Een nieuw Finance and Operations-app-exemplaar met demogegevens en een bestaand, model gestuurd app-exemplaar</span><span class="sxs-lookup"><span data-stu-id="aa3f6-115">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>](#new-demo-existing)
+ [<span data-ttu-id="aa3f6-116">Een bestaand Finance and Operations-app-exemplaar en een nieuw of bestaand, model gestuurd app-exemplaar</span><span class="sxs-lookup"><span data-stu-id="aa3f6-116">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a><span data-ttu-id="aa3f6-117">Een nieuw Finance and Operations-app-exemplaar en een nieuw, model gestuurd app-exemplaar</span><span class="sxs-lookup"><span data-stu-id="aa3f6-117">A new Finance and Operations app instance and a new model-driven app instance</span></span>

<span data-ttu-id="aa3f6-118">Als u een verbinding voor twee keer wegschrijven wilt instellen tussen een nieuw exemplaar van een Finance and Operations-app zonder gegevens en een nieuw exemplaar van een modelgestuurde app in Dynamics 365, volgt u de stappen in [Instellingen voor twee keer wegschrijven in Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="aa3f6-118">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="aa3f6-119">Wanneer de configuratie van de verbinding is voltooid, worden automatisch de volgende acties uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="aa3f6-119">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="aa3f6-120">Er wordt een nieuwe, lege Finance and Operations-omgeving ingericht.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-120">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="aa3f6-121">Er wordt een nieuw, leeg exemplaar van een modelgestuurde app ingericht, waarbij de CRM Prime-oplossing wordt geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-121">A new, empty instance of a model-driven app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="aa3f6-122">Er wordt een verbinding voor twee keer wegschrijven tot stand gebracht met DAT-bedrijfsgegevens.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-122">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="aa3f6-123">Entiteitstoewijzingen worden ingeschakeld voor live migratie.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-123">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="aa3f6-124">Beide omgevingen zijn vervolgens gereed voor synchronisatie met live gegevens.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-124">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a><span data-ttu-id="aa3f6-125">Een nieuw Finance and Operations-app-exemplaar en een bestaand, model gestuurd app-exemplaar</span><span class="sxs-lookup"><span data-stu-id="aa3f6-125">A new Finance and Operations app instance and an existing model-driven app instance</span></span>

<span data-ttu-id="aa3f6-126">Als u een verbinding voor twee keer wegschrijven wilt instellen tussen een nieuw exemplaar van een Finance and Operations-app zonder gegevens en een bestaand exemplaar van een modelgestuurde app in Dynamics 365, volgt u de stappen in [Instellingen voor twee keer wegschrijven in Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="aa3f6-126">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="aa3f6-127">Wanneer de configuratie van de verbinding is voltooid, worden automatisch de volgende acties uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="aa3f6-127">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="aa3f6-128">Er wordt een nieuwe, lege Finance and Operations-omgeving ingericht.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-128">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="aa3f6-129">Er wordt een verbinding voor twee keer wegschrijven tot stand gebracht met DAT-bedrijfsgegevens.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-129">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="aa3f6-130">Entiteitstoewijzingen worden ingeschakeld voor live migratie.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-130">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="aa3f6-131">Beide omgevingen zijn vervolgens gereed voor synchronisatie met live gegevens.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-131">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="aa3f6-132">Voer de volgende stappen uit om de bestaande Common Data Service-gegevens te synchroniseren met de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-132">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="aa3f6-133">Maak een nieuw bedrijf maken in de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-133">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="aa3f6-134">Voeg het bedrijf toe aan de instellingen van de verbinding voor twee keer wegschrijven.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-134">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="aa3f6-135">[Laad](bootstrap-company-data.md) de Common Data Service-gegevens automatisch met de ISO-bedrijfscode (International Organization for Standardization) van drie letters.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-135">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>

<span data-ttu-id="aa3f6-136">Omdat voor twee keer wegschrijven wordt uitgevoerd in de modus voor live synchronisatie, beginnen de Common Data Service-gegevens automatisch te stromen naar de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-136">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a><span data-ttu-id="aa3f6-137">Een nieuw Finance and Operations-app-exemplaar met demogegevens en een nieuw, model gestuurd app-exemplaar</span><span class="sxs-lookup"><span data-stu-id="aa3f6-137">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>

<span data-ttu-id="aa3f6-138">Als u een verbinding voor twee keer wegschrijven wilt instellen tussen een nieuw exemplaar van een Finance and Operations-app met demogegevens en een nieuw exemplaar van een modelgestuurde app in Dynamics 365, volgt u de stappen in de sectie [Een nieuw Finance and Operations-app-exemplaar en een nieuw modelgestuurd app-exemplaar](#new-new) dat eerder in dit onderwerp is beschreven.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-138">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and a new instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and a new model-driven app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="aa3f6-139">Wanneer de verbinding is voltooid en u de demogegevens wilt synchroniseren met de modelgestuurde app, voert u de volgende stappen uit.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-139">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="aa3f6-140">Open de Finance and Operations-app via de LCS-pagina, meld u aan en ga naar **Gegevensbeheer \> Twee keer wegschrijven**.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-140">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="aa3f6-141">Voer de functie **Initiële synchronisatie** uit voor de entiteiten waarvoor u gegevens wilt synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-141">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a><span data-ttu-id="aa3f6-142">Een nieuw Finance and Operations-app-exemplaar met demogegevens en een bestaand, model gestuurd app-exemplaar</span><span class="sxs-lookup"><span data-stu-id="aa3f6-142">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>

<span data-ttu-id="aa3f6-143">Als u een verbinding voor twee keer wegschrijven wilt instellen tussen een nieuw exemplaar van een Finance and Operations-app met demogegevens en een bestaand exemplaar van een modelgestuurde app in Dynamics 365, volgt u de stappen in de sectie [Een nieuw Finance and Operations-app-exemplaar en een bestaand modelgestuurd app-exemplaar](#new-existing) dat eerder in dit onderwerp is beschreven.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-143">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and an existing instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and an existing model-driven app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="aa3f6-144">Wanneer de verbinding is voltooid en u de demogegevens wilt synchroniseren met de modelgestuurde app, voert u de volgende stappen uit.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-144">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="aa3f6-145">Open de Finance and Operations-app via de LCS-pagina, meld u aan en ga naar **Gegevensbeheer \> Twee keer wegschrijven**.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-145">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="aa3f6-146">Voer de functie **Initiële synchronisatie** uit voor de entiteiten waarvoor u gegevens wilt synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-146">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="aa3f6-147">Voer de volgende stappen uit om de bestaande Common Data Service-gegevens te synchroniseren met de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-147">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="aa3f6-148">Maak een nieuw bedrijf maken in de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-148">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="aa3f6-149">Voeg het bedrijf toe aan de instellingen van de verbinding voor twee keer wegschrijven.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-149">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="aa3f6-150">[Laad](bootstrap-company-data.md) de Common Data Service-gegevens automatisch met de ISO-bedrijfscode van drie letters.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-150">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="aa3f6-151">Omdat voor twee keer wegschrijven wordt uitgevoerd in de modus voor live synchronisatie, beginnen de Common Data Service-gegevens automatisch te stromen naar de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-151">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="aa3f6-152">Een bestaand Finance and Operations-app-exemplaar en een nieuw of bestaand, model gestuurd app-exemplaar</span><span class="sxs-lookup"><span data-stu-id="aa3f6-152">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>

<span data-ttu-id="aa3f6-153">Het instellen van een verbinding voor twee keer wegschrijven tussen een bestaand exemplaar van een Finance and Operations-app en een nieuw of bestaand exemplaar van een modelgestuurde app in Dynamics 365 vindt plaats in de Finance and Operations-omgeving.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-153">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new or existing instance of a model-driven app in Dynamics 365 occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="aa3f6-154">Stel de verbinding in vanuit de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-154">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="aa3f6-155">Als u de bestaande Common Data Service-gegevens wilt synchroniseren met de Finance and Operations-app, [laadt](bootstrap-company-data.md) u de Common Data Service-gegevens automatisch met de ISO-bedrijfscode van drie letters.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-155">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="aa3f6-156">Omdat voor twee keer wegschrijven wordt uitgevoerd in de modus voor live synchronisatie, beginnen de Common Data Service-gegevens automatisch te stromen naar de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="aa3f6-156">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>
