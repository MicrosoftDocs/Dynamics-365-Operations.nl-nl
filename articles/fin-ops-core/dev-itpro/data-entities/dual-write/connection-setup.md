---
title: Richtlijnen voor het instellen van twee keer wegschrijven
description: In dit onderwerp worden de scenario's beschreven die worden ondersteund voor instellingen voor twee keer wegschrijven.
author: RamaKrishnamoorthy
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
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
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 999b37970be1c10fd5e78c3d8ac6c1fb25cad367
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751381"
---
# <a name="guidance-for-dual-write-setup"></a><span data-ttu-id="6b14a-103">Richtlijnen voor het instellen van twee keer wegschrijven</span><span class="sxs-lookup"><span data-stu-id="6b14a-103">Guidance for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="6b14a-104">U kunt een verbinding voor twee keer wegschrijven instellen tussen een Finance and Operations-omgeving en een Dataverse-omgeving.</span><span class="sxs-lookup"><span data-stu-id="6b14a-104">You can set up a dual-write connection between a Finance and Operations environment and a Dataverse environment.</span></span>

+ <span data-ttu-id="6b14a-105">Een **Finance and Operations-omgeving** levert het onderliggende platform voor **Finance and Operations-apps** (bijvoorbeeld Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce en Dynamics 365 Human Resources).</span><span class="sxs-lookup"><span data-stu-id="6b14a-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources).</span></span>
+ <span data-ttu-id="6b14a-106">Een **Dataverse-omgeving** biedt het onderliggende platform voor **Customer Engagement-apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing en Dynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="6b14a-106">A **Dataverse environment** provides the underlying platform for **customer engagement apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6b14a-107">De module Human resources in Dynamics 365 Finance ondersteunt verbindingen voor twee keer wegschrijven, maar de Dynamics 365 Human Resources-app ondersteunt dat niet.</span><span class="sxs-lookup"><span data-stu-id="6b14a-107">The Human Resources module in Dynamics 365 Finance supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="6b14a-108">Het installatiemechanisme varieert afhankelijk van uw abonnement en de omgeving:</span><span class="sxs-lookup"><span data-stu-id="6b14a-108">The setup mechanism varies, depending on your subscription and the environment:</span></span>

+ <span data-ttu-id="6b14a-109">Voor nieuwe exemplaren van Finance and Operations-apps begint het instellen van een verbinding voor twee keer wegschrijven met Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="6b14a-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="6b14a-110">Als u een licentie hebt voor Microsoft Power Platform, krijgt u een nieuwe Dataverse-omgeving als uw tenant er geen heeft.</span><span class="sxs-lookup"><span data-stu-id="6b14a-110">If you have a license for Microsoft Power Platform, you will get a new Dataverse environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="6b14a-111">Voor bestaande exemplaren van Finance and Operations-apps begint het instellen van een verbinding voor twee keer wegschrijven in de Finance and Operations-omgeving.</span><span class="sxs-lookup"><span data-stu-id="6b14a-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="6b14a-112">Voordat u twee keer wegschrijven voor een entiteit start, kunt u een initiële synchronisatie uitvoeren om bestaande gegevens aan beide zijden van Finance and Operations-apps en Customer Engagement-apps te verwerken.</span><span class="sxs-lookup"><span data-stu-id="6b14a-112">Before you start dual-write on an entity, you can run an initial synchronization to handle existing data on both sides: Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="6b14a-113">U kunt de initiële synchronisatie overslaan als u geen gegevens tussen de twee omgevingen hoeft te synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="6b14a-113">You can skip the initial synchronization if you don't have to sync data between the two environments.</span></span>

<span data-ttu-id="6b14a-114">Met een initiële synchronisatie kunt u bestaande gegevens in twee richtingen van de ene naar de andere app kopiëren.</span><span class="sxs-lookup"><span data-stu-id="6b14a-114">An initial synchronization lets you copy existing data from one app to another bidirectionally.</span></span> <span data-ttu-id="6b14a-115">Er zijn verschillende instellingsscenario's afhankelijk van de omgevingen die u al hebt en het type gegevens dat deze omgevingen bevatten.</span><span class="sxs-lookup"><span data-stu-id="6b14a-115">There are several setup scenarios, depending on the environments that you already have and the type of data in them.</span></span>

<span data-ttu-id="6b14a-116">De volgende scenario's met instellingen worden ondersteund:</span><span class="sxs-lookup"><span data-stu-id="6b14a-116">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="6b14a-117">Een nieuw exemplaar van de Finance and Operations-app en een nieuw exemplaar van de Customer Engagement-app</span><span class="sxs-lookup"><span data-stu-id="6b14a-117">A new Finance and Operations app instance and a new customer engagement app instance</span></span>](#new-new)
+ [<span data-ttu-id="6b14a-118">Een nieuw exemplaar van de Finance and Operations-app en een bestaand exemplaar van de Customer Engagement-app</span><span class="sxs-lookup"><span data-stu-id="6b14a-118">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>](#new-existing)
+ [<span data-ttu-id="6b14a-119">Een nieuw exemplaar van de Finance and Operations-app en een nieuw exemplaar van de Customer Engagement-app</span><span class="sxs-lookup"><span data-stu-id="6b14a-119">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>](#new-data-new)
+ [<span data-ttu-id="6b14a-120">Een nieuw exemplaar van de Finance and Operations-app en een bestaand exemplaar van de Customer Engagement-app</span><span class="sxs-lookup"><span data-stu-id="6b14a-120">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>](#new-data-existing)
+ [<span data-ttu-id="6b14a-121">Een bestaand exemplaar van de Finance and Operations-app en een nieuw exemplaar van de Customer Engagement-app</span><span class="sxs-lookup"><span data-stu-id="6b14a-121">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>](#existing-new)
+ [<span data-ttu-id="6b14a-122">Een bestaand exemplaar van de Finance and Operations-app en een bestaand exemplaar van de Customer Engagement-app</span><span class="sxs-lookup"><span data-stu-id="6b14a-122">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a><span data-ttu-id="6b14a-123">Een nieuw exemplaar van de Finance and Operations-app en een nieuw exemplaar van de Customer Engagement-app</span><span class="sxs-lookup"><span data-stu-id="6b14a-123">A new Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="6b14a-124">Als u een verbinding voor twee keer wegschrijven wilt instellen tussen een nieuw exemplaar van een Finance and Operations-app zonder gegevens en een nieuw exemplaar van een Customer Engagement-app, voert u de stappen uit in [Instellingen voor twee keer wegschrijven in Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="6b14a-124">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="6b14a-125">Wanneer de configuratie van de verbinding is voltooid, worden automatisch de volgende acties uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="6b14a-125">When the connection setup is completed, the following actions automatically occur:</span></span>

- <span data-ttu-id="6b14a-126">Er wordt een nieuwe, lege Finance and Operations-omgeving ingericht.</span><span class="sxs-lookup"><span data-stu-id="6b14a-126">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="6b14a-127">Er wordt een nieuw, leeg exemplaar van een Customer Engagement-app ingericht, waarbij de CRM Prime-oplossing wordt geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="6b14a-127">A new, empty instance of a customer engagement app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="6b14a-128">Er wordt een verbinding voor twee keer wegschrijven tot stand gebracht met DAT-bedrijfsgegevens.</span><span class="sxs-lookup"><span data-stu-id="6b14a-128">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="6b14a-129">Tabeltoewijzingen worden ingeschakeld voor live migratie.</span><span class="sxs-lookup"><span data-stu-id="6b14a-129">Table maps are enabled for live synchronization.</span></span>

<span data-ttu-id="6b14a-130">Beide omgevingen zijn vervolgens gereed voor synchronisatie met live gegevens.</span><span class="sxs-lookup"><span data-stu-id="6b14a-130">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a><span data-ttu-id="6b14a-131">Een nieuw exemplaar van de Finance and Operations-app en een bestaand exemplaar van de Customer Engagement-app</span><span class="sxs-lookup"><span data-stu-id="6b14a-131">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="6b14a-132">Als u een verbinding voor twee keer wegschrijven wilt instellen tussen een nieuw exemplaar van een Finance and Operations-app zonder gegevens en een bestaand exemplaar van een Customer Engagement-app, voert u de stappen uit in [Instellingen voor twee keer wegschrijven in Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="6b14a-132">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="6b14a-133">Wanneer de configuratie van de verbinding is voltooid, worden automatisch de volgende acties uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="6b14a-133">When the connection setup is completed, the following actions automatically occur:</span></span>

- <span data-ttu-id="6b14a-134">Er wordt een nieuwe, lege Finance and Operations-omgeving ingericht.</span><span class="sxs-lookup"><span data-stu-id="6b14a-134">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="6b14a-135">Er wordt een verbinding voor twee keer wegschrijven tot stand gebracht met DAT-bedrijfsgegevens.</span><span class="sxs-lookup"><span data-stu-id="6b14a-135">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="6b14a-136">Tabeltoewijzingen worden ingeschakeld voor live migratie.</span><span class="sxs-lookup"><span data-stu-id="6b14a-136">Table maps are enabled for live synchronization.</span></span>

<span data-ttu-id="6b14a-137">Beide omgevingen zijn vervolgens gereed voor synchronisatie met live gegevens.</span><span class="sxs-lookup"><span data-stu-id="6b14a-137">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="6b14a-138">Voer de volgende stappen uit om de bestaande Dataverse-gegevens te synchroniseren met de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="6b14a-138">To sync the existing Dataverse data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="6b14a-139">Maak een nieuw bedrijf maken in de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="6b14a-139">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="6b14a-140">Voeg het bedrijf toe aan de instellingen van de verbinding voor twee keer wegschrijven.</span><span class="sxs-lookup"><span data-stu-id="6b14a-140">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="6b14a-141">[Laad](bootstrap-company-data.md) de Dataverse-gegevens automatisch met de ISO-bedrijfscode (International Organization for Standardization) van drie letters.</span><span class="sxs-lookup"><span data-stu-id="6b14a-141">[Bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>
4. <span data-ttu-id="6b14a-142">Voer de functie **Initiële synchronisatie** uit voor de tabellen waarvoor u gegevens wilt synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="6b14a-142">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="6b14a-143">Zie de sectie [Voorbeeld](#example) verderop in dit onderwerp voor koppelingen naar een voorbeeld en een alternatieve aanpak.</span><span class="sxs-lookup"><span data-stu-id="6b14a-143">For links to an example and an alternative approach, see the [Example](#example) section later in this topic.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a><span data-ttu-id="6b14a-144">Een nieuw exemplaar van de Finance and Operations-app met gegevens en een nieuw exemplaar van de Customer Engagement-app</span><span class="sxs-lookup"><span data-stu-id="6b14a-144">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>

<span data-ttu-id="6b14a-145">Als u een verbinding voor twee keer wegschrijven wilt instellen tussen een nieuw exemplaar van een Finance and Operations-app met gegevens en een nieuw exemplaar van een Customer Engagement-app, voert u de stappen in de sectie [Een nieuw exemplaar van de Finance and Operations-app en een nieuw exemplaar van de Customer Engagement-app](#new-new) eerder in dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="6b14a-145">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and a new instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and a new customer engagement app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="6b14a-146">Wanneer de verbinding is voltooid en u de gegevens wilt synchroniseren met de Customer Engagement-app, voert u de volgende stappen uit.</span><span class="sxs-lookup"><span data-stu-id="6b14a-146">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="6b14a-147">Open de Finance and Operations-app via de LCS-pagina, meld u aan en ga naar **Gegevensbeheer \> Twee keer wegschrijven**.</span><span class="sxs-lookup"><span data-stu-id="6b14a-147">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="6b14a-148">Voer de functie **Initiële synchronisatie** uit voor de tabellen waarvoor u gegevens wilt synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="6b14a-148">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="6b14a-149">Zie de sectie [Voorbeeld](#example) voor koppelingen naar een voorbeeld en een alternatieve aanpak.</span><span class="sxs-lookup"><span data-stu-id="6b14a-149">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a><span data-ttu-id="6b14a-150">Een nieuw exemplaar van de Finance and Operations-app met gegevens en een bestaand exemplaar van de Customer Engagement-app</span><span class="sxs-lookup"><span data-stu-id="6b14a-150">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>

<span data-ttu-id="6b14a-151">Als u een verbinding voor twee keer wegschrijven wilt instellen tussen een nieuw exemplaar van een Finance and Operations-app met gegevens en een bestaand exemplaar van een Customer Engagement-app, voert u de stappen in de sectie [Een nieuw exemplaar van de Finance and Operations-app en een bestaand exemplaar van de Customer Engagement-app](#new-existing) eerder in dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="6b14a-151">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and an existing instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and an existing customer engagement app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="6b14a-152">Wanneer de verbinding is voltooid en u de gegevens wilt synchroniseren met de Customer Engagement-app, voert u de volgende stappen uit.</span><span class="sxs-lookup"><span data-stu-id="6b14a-152">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="6b14a-153">Open de Finance and Operations-app via de LCS-pagina, meld u aan en ga naar **Gegevensbeheer \> Twee keer wegschrijven**.</span><span class="sxs-lookup"><span data-stu-id="6b14a-153">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="6b14a-154">Voer de functie **Initiële synchronisatie** uit voor de tabellen waarvoor u gegevens wilt synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="6b14a-154">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="6b14a-155">Voer de volgende stappen uit om de bestaande Dataverse-gegevens te synchroniseren met de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="6b14a-155">To sync the existing Dataverse data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="6b14a-156">Maak een nieuw bedrijf maken in de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="6b14a-156">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="6b14a-157">Voeg het bedrijf toe aan de instellingen van de verbinding voor twee keer wegschrijven.</span><span class="sxs-lookup"><span data-stu-id="6b14a-157">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="6b14a-158">[Laad](bootstrap-company-data.md) de Dataverse-gegevens automatisch met de ISO-bedrijfscode van drie letters.</span><span class="sxs-lookup"><span data-stu-id="6b14a-158">[Bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter ISO company code.</span></span>
4. <span data-ttu-id="6b14a-159">Voer de functie **Initiële synchronisatie** uit voor de tabellen waarvoor u gegevens wilt synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="6b14a-159">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="6b14a-160">Zie de sectie [Voorbeeld](#example) voor koppelingen naar een voorbeeld en een alternatieve aanpak.</span><span class="sxs-lookup"><span data-stu-id="6b14a-160">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a><span data-ttu-id="6b14a-161">Een bestaand exemplaar van de Finance and Operations-app en een nieuw exemplaar van de Customer Engagement-app</span><span class="sxs-lookup"><span data-stu-id="6b14a-161">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="6b14a-162">Het instellen van een verbinding voor twee keer wegschrijven tussen een bestaand exemplaar van een Finance and Operations-app en een nieuw exemplaar van een Customer Engagement-app in de Finance and Operations-omgeving.</span><span class="sxs-lookup"><span data-stu-id="6b14a-162">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="6b14a-163">[Stel de verbinding vanuit de Finance and Operations-app](enable-dual-write.md) op.</span><span class="sxs-lookup"><span data-stu-id="6b14a-163">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="6b14a-164">Voer de functie **Initiële synchronisatie** uit voor de tabellen waarvoor u gegevens wilt synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="6b14a-164">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="6b14a-165">Zie de sectie [Voorbeeld](#example) voor koppelingen naar een voorbeeld en een alternatieve aanpak.</span><span class="sxs-lookup"><span data-stu-id="6b14a-165">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="6b14a-166">Een bestaand exemplaar van de Finance and Operations-app en een bestaand exemplaar van de Customer Engagement-app</span><span class="sxs-lookup"><span data-stu-id="6b14a-166">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="6b14a-167">Het instellen van een verbinding voor twee keer wegschrijven tussen een bestaand exemplaar van een Finance and Operations-app en een bestaand exemplaar van een Customer Engagement-app in de Finance and Operations-omgeving.</span><span class="sxs-lookup"><span data-stu-id="6b14a-167">The setup of a dual-write connection between an existing instance of a Finance and Operations app and an existing instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="6b14a-168">[Stel de verbinding vanuit de Finance and Operations-app](enable-dual-write.md) op.</span><span class="sxs-lookup"><span data-stu-id="6b14a-168">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="6b14a-169">Als u de bestaande Dataverse-gegevens wilt synchroniseren met de Finance and Operations-app, [laadt](bootstrap-company-data.md) u de Dataverse-gegevens automatisch met de ISO-bedrijfscode van drie letters.</span><span class="sxs-lookup"><span data-stu-id="6b14a-169">To sync the existing Dataverse data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter ISO company code.</span></span>
3. <span data-ttu-id="6b14a-170">Voer de functie **Initiële synchronisatie** uit voor de tabellen waarvoor u gegevens wilt synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="6b14a-170">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="6b14a-171">Zie de sectie [Voorbeeld](#example) voor koppelingen naar een voorbeeld en een alternatieve aanpak.</span><span class="sxs-lookup"><span data-stu-id="6b14a-171">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="example"></a><span data-ttu-id="6b14a-172">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="6b14a-172">Example</span></span>

<span data-ttu-id="6b14a-173">Zie voor een voorbeeld [De tabeltoewijzing Klanten V3—contactpersonen inschakelen](enable-entity-map.md#enable-table-map)</span><span class="sxs-lookup"><span data-stu-id="6b14a-173">For an example, see [Enabling the Customers V3—Contacts table map](enable-entity-map.md#enable-table-map)</span></span>

<span data-ttu-id="6b14a-174">Zie [Overwegingen voor initiële synchronisatie](initial-sync-guidance.md) voor een alternatieve aanpak die is gebaseerd op gegevensvolumes in elke entiteit waarvoor een initiële synchronisatie moet worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="6b14a-174">For an alternative approach that is based on data volumes in each entity that must run an initial synchronization, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]