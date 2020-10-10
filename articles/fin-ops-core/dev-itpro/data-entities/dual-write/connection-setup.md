---
title: Ondersteunde scenario's met instellingen voor twee keer wegschrijven
description: In dit onderwerp worden de scenario's beschreven die worden ondersteund voor instellingen voor twee keer wegschrijven.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/17/2020
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
ms.openlocfilehash: b4f69e7933bc5a50cccad6911c99cf08d2768578
ms.sourcegitcommit: b3df62842e62234e8eaa16992375582518976131
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/17/2020
ms.locfileid: "3818591"
---
# <a name="supported-scenarios-for-dual-write-setup"></a><span data-ttu-id="6a7c1-103">Ondersteunde scenario's met instellingen voor twee keer wegschrijven</span><span class="sxs-lookup"><span data-stu-id="6a7c1-103">Supported scenarios for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="6a7c1-104">U kunt een verbinding voor twee keer wegschrijven instellen tussen een Finance and Operations-omgeving en een Common Data Service-omgeving.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="6a7c1-105">Een **Finance and Operations-omgeving** levert het onderliggende platform voor **Finance and Operations-apps** (bijvoorbeeld Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management en Dynamics 365 Retail).</span><span class="sxs-lookup"><span data-stu-id="6a7c1-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, and Dynamics 365 Retail).</span></span>
+ <span data-ttu-id="6a7c1-106">Een **Common Data Service-omgeving** biedt het onderliggende platform voor **modelgestuurde apps in Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing en Dynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="6a7c1-106">A **Common Data Service environment** provides the underlying platform for **model-driven apps in Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

>[!IMPORTANT]
><span data-ttu-id="6a7c1-107">Human resources in Finance and Operations ondersteunt dual-write-verbindingen, maar de Dynamics 365 Human Resources-app ondersteunt dat niet.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-107">Human Resources in Finance and Operations supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="6a7c1-108">Het installatiemechanisme varieert afhankelijk van uw abonnement en de omgeving.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-108">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="6a7c1-109">Voor nieuwe exemplaren van Finance and Operations-apps begint het instellen van een verbinding voor twee keer wegschrijven met Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="6a7c1-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="6a7c1-110">Als u een licentie hebt voor Power Platform, krijgt u een nieuwe Common Data Service-omgeving als uw tenant er geen heeft.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-110">If you have a license for Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="6a7c1-111">Voor bestaande exemplaren van Finance and Operations-apps begint het instellen van een verbinding voor twee keer wegschrijven in de Finance and Operations-omgeving.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="6a7c1-112">De volgende scenario's met instellingen worden ondersteund:</span><span class="sxs-lookup"><span data-stu-id="6a7c1-112">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="6a7c1-113">Een nieuw Finance and Operations-app-exemplaar en een nieuw, model gestuurd app-exemplaar</span><span class="sxs-lookup"><span data-stu-id="6a7c1-113">A new Finance and Operations app instance and a new model-driven app instance</span></span>](#new-new)
+ [<span data-ttu-id="6a7c1-114">Een nieuw Finance and Operations-app-exemplaar en een bestaand, model gestuurd app-exemplaar</span><span class="sxs-lookup"><span data-stu-id="6a7c1-114">A new Finance and Operations app instance and an existing model-driven app instance</span></span>](#new-existing)
+ [<span data-ttu-id="6a7c1-115">Een nieuw Finance and Operations-app-exemplaar met demogegevens en een nieuw, model gestuurd app-exemplaar</span><span class="sxs-lookup"><span data-stu-id="6a7c1-115">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>](#new-demo-new)
+ [<span data-ttu-id="6a7c1-116">Een nieuw Finance and Operations-app-exemplaar met demogegevens en een bestaand, model gestuurd app-exemplaar</span><span class="sxs-lookup"><span data-stu-id="6a7c1-116">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>](#new-demo-existing)
+ [<span data-ttu-id="6a7c1-117">Een bestaand Finance and Operations-app-exemplaar en een nieuw of bestaand, model gestuurd app-exemplaar</span><span class="sxs-lookup"><span data-stu-id="6a7c1-117">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a><span data-ttu-id="6a7c1-118">Een nieuw Finance and Operations-app-exemplaar en een nieuw, model gestuurd app-exemplaar</span><span class="sxs-lookup"><span data-stu-id="6a7c1-118">A new Finance and Operations app instance and a new model-driven app instance</span></span>

<span data-ttu-id="6a7c1-119">Als u een verbinding voor twee keer wegschrijven wilt instellen tussen een nieuw exemplaar van een Finance and Operations-app zonder gegevens en een nieuw exemplaar van een modelgestuurde app in Dynamics 365, volgt u de stappen in [Instellingen voor twee keer wegschrijven in Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="6a7c1-119">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="6a7c1-120">Wanneer de configuratie van de verbinding is voltooid, worden automatisch de volgende acties uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="6a7c1-120">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="6a7c1-121">Er wordt een nieuwe, lege Finance and Operations-omgeving ingericht.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-121">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="6a7c1-122">Er wordt een nieuw, leeg exemplaar van een modelgestuurde app ingericht, waarbij de CRM Prime-oplossing wordt geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-122">A new, empty instance of a model-driven app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="6a7c1-123">Er wordt een verbinding voor twee keer wegschrijven tot stand gebracht met DAT-bedrijfsgegevens.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-123">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="6a7c1-124">Entiteitstoewijzingen worden ingeschakeld voor live migratie.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-124">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="6a7c1-125">Beide omgevingen zijn vervolgens gereed voor synchronisatie met live gegevens.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-125">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a><span data-ttu-id="6a7c1-126">Een nieuw Finance and Operations-app-exemplaar en een bestaand, model gestuurd app-exemplaar</span><span class="sxs-lookup"><span data-stu-id="6a7c1-126">A new Finance and Operations app instance and an existing model-driven app instance</span></span>

<span data-ttu-id="6a7c1-127">Als u een verbinding voor twee keer wegschrijven wilt instellen tussen een nieuw exemplaar van een Finance and Operations-app zonder gegevens en een bestaand exemplaar van een modelgestuurde app in Dynamics 365, volgt u de stappen in [Instellingen voor twee keer wegschrijven in Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="6a7c1-127">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="6a7c1-128">Wanneer de configuratie van de verbinding is voltooid, worden automatisch de volgende acties uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="6a7c1-128">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="6a7c1-129">Er wordt een nieuwe, lege Finance and Operations-omgeving ingericht.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-129">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="6a7c1-130">Er wordt een verbinding voor twee keer wegschrijven tot stand gebracht met DAT-bedrijfsgegevens.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-130">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="6a7c1-131">Entiteitstoewijzingen worden ingeschakeld voor live migratie.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-131">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="6a7c1-132">Beide omgevingen zijn vervolgens gereed voor synchronisatie met live gegevens.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-132">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="6a7c1-133">Voer de volgende stappen uit om de bestaande Common Data Service-gegevens te synchroniseren met de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-133">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="6a7c1-134">Maak een nieuw bedrijf maken in de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-134">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="6a7c1-135">Voeg het bedrijf toe aan de instellingen van de verbinding voor twee keer wegschrijven.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-135">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="6a7c1-136">[Laad](bootstrap-company-data.md) de Common Data Service-gegevens automatisch met de ISO-bedrijfscode (International Organization for Standardization) van drie letters.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-136">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>

<span data-ttu-id="6a7c1-137">Omdat voor twee keer wegschrijven wordt uitgevoerd in de modus voor live synchronisatie, beginnen de Common Data Service-gegevens automatisch te stromen naar de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-137">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a><span data-ttu-id="6a7c1-138">Een nieuw Finance and Operations-app-exemplaar met demogegevens en een nieuw, model gestuurd app-exemplaar</span><span class="sxs-lookup"><span data-stu-id="6a7c1-138">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>

<span data-ttu-id="6a7c1-139">Als u een verbinding voor twee keer wegschrijven wilt instellen tussen een nieuw exemplaar van een Finance and Operations-app met demogegevens en een nieuw exemplaar van een modelgestuurde app in Dynamics 365, volgt u de stappen in de sectie [Een nieuw Finance and Operations-app-exemplaar en een nieuw modelgestuurd app-exemplaar](#new-new) dat eerder in dit onderwerp is beschreven.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-139">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and a new instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and a new model-driven app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="6a7c1-140">Wanneer de verbinding is voltooid en u de demogegevens wilt synchroniseren met de modelgestuurde app, voert u de volgende stappen uit.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-140">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="6a7c1-141">Open de Finance and Operations-app via de LCS-pagina, meld u aan en ga naar **Gegevensbeheer \> Twee keer wegschrijven**.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-141">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="6a7c1-142">Voer de functie **Initiële synchronisatie** uit voor de entiteiten waarvoor u gegevens wilt synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-142">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a><span data-ttu-id="6a7c1-143">Een nieuw Finance and Operations-app-exemplaar met demogegevens en een bestaand, model gestuurd app-exemplaar</span><span class="sxs-lookup"><span data-stu-id="6a7c1-143">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>

<span data-ttu-id="6a7c1-144">Als u een verbinding voor twee keer wegschrijven wilt instellen tussen een nieuw exemplaar van een Finance and Operations-app met demogegevens en een bestaand exemplaar van een modelgestuurde app in Dynamics 365, volgt u de stappen in de sectie [Een nieuw Finance and Operations-app-exemplaar en een bestaand modelgestuurd app-exemplaar](#new-existing) dat eerder in dit onderwerp is beschreven.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-144">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and an existing instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and an existing model-driven app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="6a7c1-145">Wanneer de verbinding is voltooid en u de demogegevens wilt synchroniseren met de modelgestuurde app, voert u de volgende stappen uit.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-145">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="6a7c1-146">Open de Finance and Operations-app via de LCS-pagina, meld u aan en ga naar **Gegevensbeheer \> Twee keer wegschrijven**.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-146">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="6a7c1-147">Voer de functie **Initiële synchronisatie** uit voor de entiteiten waarvoor u gegevens wilt synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-147">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="6a7c1-148">Voer de volgende stappen uit om de bestaande Common Data Service-gegevens te synchroniseren met de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-148">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="6a7c1-149">Maak een nieuw bedrijf maken in de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-149">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="6a7c1-150">Voeg het bedrijf toe aan de instellingen van de verbinding voor twee keer wegschrijven.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-150">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="6a7c1-151">[Laad](bootstrap-company-data.md) de Common Data Service-gegevens automatisch met de ISO-bedrijfscode van drie letters.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-151">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="6a7c1-152">Omdat voor twee keer wegschrijven wordt uitgevoerd in de modus voor live synchronisatie, beginnen de Common Data Service-gegevens automatisch te stromen naar de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-152">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="6a7c1-153">Een bestaand Finance and Operations-app-exemplaar en een nieuw of bestaand, model gestuurd app-exemplaar</span><span class="sxs-lookup"><span data-stu-id="6a7c1-153">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>

<span data-ttu-id="6a7c1-154">Het instellen van een verbinding voor twee keer wegschrijven tussen een bestaand exemplaar van een Finance and Operations-app en een nieuw of bestaand exemplaar van een modelgestuurde app in Dynamics 365 vindt plaats in de Finance and Operations-omgeving.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-154">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new or existing instance of a model-driven app in Dynamics 365 occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="6a7c1-155">Stel de verbinding in vanuit de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-155">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="6a7c1-156">Als u de bestaande Common Data Service-gegevens wilt synchroniseren met de Finance and Operations-app, [laadt](bootstrap-company-data.md) u de Common Data Service-gegevens automatisch met de ISO-bedrijfscode van drie letters.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-156">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="6a7c1-157">Omdat voor twee keer wegschrijven wordt uitgevoerd in de modus voor live synchronisatie, beginnen de Common Data Service-gegevens automatisch te stromen naar de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-157">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>
