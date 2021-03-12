---
title: De klantportal installeren, instellen en bijwerken
description: In dit onderwerp vindt u instructies voor licenties en instelling voor de klantportal.
author: dasani-madipalli
manager: tfehr
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 2153bbca2be7c72e48b9dc51b1f7fdbe2ab89903
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977733"
---
# <a name="install-set-up-and-update-the-customer-portal"></a><span data-ttu-id="de267-103">De klantportal installeren, instellen en bijwerken</span><span class="sxs-lookup"><span data-stu-id="de267-103">Install, set up, and update the Customer portal</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="licensing-requirements"></a><span data-ttu-id="de267-104">Licentievereisten</span><span class="sxs-lookup"><span data-stu-id="de267-104">Licensing requirements</span></span>

<span data-ttu-id="de267-105">Voor het implementeren van de klantportal hebt u de volgende licenties nodig:</span><span class="sxs-lookup"><span data-stu-id="de267-105">To implement the Customer portal, you must have the following licenses:</span></span>

- <span data-ttu-id="de267-106">**Power Apps-portals**: deze licentie is vereist om de klantportal te hosten.</span><span class="sxs-lookup"><span data-stu-id="de267-106">**Power Apps portals** – This license is required to host the Customer portal.</span></span> <span data-ttu-id="de267-107">Portals worden op basis van gebruik in licentie gegeven.</span><span class="sxs-lookup"><span data-stu-id="de267-107">Portals are licensed based on usage.</span></span> <span data-ttu-id="de267-108">Zie [Licentievereisten voor Power Apps-portals](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="de267-108">For more information, see the [Power Apps portals licensing requirements](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).</span></span>
- <span data-ttu-id="de267-109">**Twee keer wegschrijven**: u moet over de vereiste licenties beschikken om twee keer wegschrijven in te schakelen voor Supply Chain Management-tabellen.</span><span class="sxs-lookup"><span data-stu-id="de267-109">**Dual-write** – You must have the necessary licenses to enable dual-write for Supply Chain Management tables.</span></span> <span data-ttu-id="de267-110">Zie [Systeemvereisten voor twee keer wegschrijven](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="de267-110">For more information, see the [system requirements for dual-write](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span></span>

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a><span data-ttu-id="de267-111">Afhankelijkheden voor twee keer wegschrijven en Power Apps-portals</span><span class="sxs-lookup"><span data-stu-id="de267-111">Dependencies on dual-write and Power Apps portals</span></span>

<span data-ttu-id="de267-112">De klantportal is afhankelijk van Power Apps-portals en bewerkingen voor twee keer wegschrijven, zoals wordt weer gegeven in de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="de267-112">The Customer portal depends on Power Apps portals and dual-write, as shown in the following illustration.</span></span>

<span data-ttu-id="de267-113">![Afhankelijkheden van klantportal](media/customer-portal-elements.png "Afhankelijkheden van klantportal")</span><span class="sxs-lookup"><span data-stu-id="de267-113">![Customer portal dependencies](media/customer-portal-elements.png "Customer portal dependencies")</span></span>

<span data-ttu-id="de267-114">In tegenstelling tot andere functies van Supply Chain Management, bevindt de klantportalsjabloon zich in Power Apps-portals.</span><span class="sxs-lookup"><span data-stu-id="de267-114">Unlike other features from Supply Chain Management, the Customer portal template resides in Power Apps portals.</span></span> <span data-ttu-id="de267-115">Daarom wordt de klantportal beperkt door de functionaliteit en capaciteiten die door Power Apps-portals en de tabellen in twee keer wegschrijven worden geleverd.</span><span class="sxs-lookup"><span data-stu-id="de267-115">Therefore, the Customer portal is limited by the functionality and capabilities that are provided by Power Apps portals and the tables in dual-write.</span></span>

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a><span data-ttu-id="de267-116">Vereiste instellingen om de klantportal in te schakelen</span><span class="sxs-lookup"><span data-stu-id="de267-116">Required setup to enable the Customer portal</span></span>

<span data-ttu-id="de267-117">Nadat u hebt vastgesteld dat u over de vereiste licenties beschikt, kunt u Twee keer wegschrijven instellen zoals beschreven in de [Initiële synchronisatie-instructies voor Twee keer wegschrijven](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).</span><span class="sxs-lookup"><span data-stu-id="de267-117">After you've made sure that you have the required licenses, you can set up dual-write as described in the [dual-write initial synchronization instructions](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).</span></span>

<span data-ttu-id="de267-118">Zorg ervoor dat u de volgende tabeltoewijzingen in twee keer wegschrijven inschakelt:</span><span class="sxs-lookup"><span data-stu-id="de267-118">Be sure to enable the following table mappings in dual-write:</span></span>

- <span data-ttu-id="de267-119">Koptekst van verkooporder</span><span class="sxs-lookup"><span data-stu-id="de267-119">Sales Order Header</span></span>
- <span data-ttu-id="de267-120">Details verkooporder</span><span class="sxs-lookup"><span data-stu-id="de267-120">Sales Order Details</span></span>
- <span data-ttu-id="de267-121">Rekeningen</span><span class="sxs-lookup"><span data-stu-id="de267-121">Accounts</span></span>
- <span data-ttu-id="de267-122">Contactpersonen</span><span class="sxs-lookup"><span data-stu-id="de267-122">Contacts</span></span>
- <span data-ttu-id="de267-123">Producten</span><span class="sxs-lookup"><span data-stu-id="de267-123">Products</span></span>

<span data-ttu-id="de267-124">Nadat deze instellingen zijn voltooid, kunt u de sjabloon voor de klantportal inrichten.</span><span class="sxs-lookup"><span data-stu-id="de267-124">After this setup is completed, you can provision the Customer portal template.</span></span>

## <a name="provision-the-customer-portal"></a><span data-ttu-id="de267-125">De klantportal inrichten</span><span class="sxs-lookup"><span data-stu-id="de267-125">Provision the Customer portal</span></span>

<span data-ttu-id="de267-126">Controleer voordat u begint of u de [vereiste instellingen](#required-setup) al hebt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="de267-126">Before you begin, make sure that you've already completed the [required setup](#required-setup).</span></span> <span data-ttu-id="de267-127">Voer vervolgens de volgende stappen uit om de klantportal in te richten.</span><span class="sxs-lookup"><span data-stu-id="de267-127">Then follow these steps to provision the Customer portal.</span></span>

1. <span data-ttu-id="de267-128">Ga naar [make.powerapps.com](https://make.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="de267-128">Go to [make.powerapps.com](https://make.powerapps.com/).</span></span>
2. <span data-ttu-id="de267-129">Controleer of u de omgeving gebruikt waarin u twee keer wegschrijven hebt ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="de267-129">Make sure that you're using the environment where you enabled dual-write.</span></span>
3. <span data-ttu-id="de267-130">Ga naar het tabblad **Maken**, blader naar de sectie **Beginnen bij sjabloon** en selecteer de sjabloon met de naam **Klantportal**.</span><span class="sxs-lookup"><span data-stu-id="de267-130">On the **Create** tab, scroll down to the **Start from template** section, and select the template that is named **Customer Portal**.</span></span>
4. <span data-ttu-id="de267-131">Volg de instructies op het scherm.</span><span class="sxs-lookup"><span data-stu-id="de267-131">Follow the on-screen instructions.</span></span>

<span data-ttu-id="de267-132">Nadat de inrichting is voltooid, kunt u de klantportal openen via de sectie **Uw apps** op de **Startpagina**.</span><span class="sxs-lookup"><span data-stu-id="de267-132">After provisioning is completed, you can access the Customer portal in the **Your apps** section of the **Home** page.</span></span>

> [!NOTE]
> <span data-ttu-id="de267-133">Als de oplossing voor dubbel schrijven niet is geïnstalleerd in de omgeving waarin u werkt, wordt er een foutbericht weergegeven en wordt de klantportal niet ingericht.</span><span class="sxs-lookup"><span data-stu-id="de267-133">If the dual-write solution isn't installed in the environment that you're working in, you will receive an error message, and the Customer portal won't be provisioned.</span></span>

## <a name="update-the-customer-portal"></a><span data-ttu-id="de267-134">De klantportal bijwerken</span><span class="sxs-lookup"><span data-stu-id="de267-134">Update the Customer portal</span></span>

<span data-ttu-id="de267-135">Later wordt mogelijk meer functionaliteit aan de klantportal toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="de267-135">More functionality might be added to the Customer portal later.</span></span> <span data-ttu-id="de267-136">Eventuele wijzigingen die Microsoft in de onderliggende oplossingsonderdelen aanbrengt, worden automatisch weergegeven in uw omgeving.</span><span class="sxs-lookup"><span data-stu-id="de267-136">Any changes that Microsoft makes to the underlying solution components will automatically appear in your environment.</span></span> <span data-ttu-id="de267-137">Op de website die in uw omgeving wordt ingericht, worden echter niet automatisch wijzigingen weergegeven die in de configuratiegegevens zijn aangebracht.</span><span class="sxs-lookup"><span data-stu-id="de267-137">However, the website that is provisioned in your environment won't automatically reflect changes that are made to the configuration data.</span></span> <span data-ttu-id="de267-138">U moet deze wijzigingen handmatig toepassen door de code op te halen uit de nieuwe sjabloon en deze samen te voegen met de ingerichte website.</span><span class="sxs-lookup"><span data-stu-id="de267-138">You will have to manually apply those changes by getting the code from the new template and merging it with the provisioned website.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="de267-139">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="de267-139">Additional resources</span></span>

<span data-ttu-id="de267-140">Als u wilt weten hoe u de klantportal kunt instellen en aanpassen, moet u eerst de volgende documentatie voor de onderliggende technologieën controleren:</span><span class="sxs-lookup"><span data-stu-id="de267-140">To learn how you can set up and customize the Customer portal, you should start by reviewing the following documentation for the underlying technologies:</span></span>

- [<span data-ttu-id="de267-141">Documentatie over Power Apps-portals</span><span class="sxs-lookup"><span data-stu-id="de267-141">Power Apps portals documentation</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [<span data-ttu-id="de267-142">Documentatie over twee keer wegschrijven</span><span class="sxs-lookup"><span data-stu-id="de267-142">Dual-write documentation</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

<span data-ttu-id="de267-143">Om uw portals effectief te beheren, moet u inzicht hebben in de Power Apps-portals en Microsoft Dataverse-levenscyclus.</span><span class="sxs-lookup"><span data-stu-id="de267-143">To effectively manage your portals, you must understand the Power Apps portals and Microsoft Dataverse lifecycle.</span></span> <span data-ttu-id="de267-144">Voor meer informatie raadpleegt u de volgende bronnen:</span><span class="sxs-lookup"><span data-stu-id="de267-144">For more information, see the following resources:</span></span>

- [<span data-ttu-id="de267-145">Informatie over Portallevenscyclus</span><span class="sxs-lookup"><span data-stu-id="de267-145">About portal lifecycle</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [<span data-ttu-id="de267-146">Een portal bijwerken</span><span class="sxs-lookup"><span data-stu-id="de267-146">Upgrade a portal</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [<span data-ttu-id="de267-147">Portalconfiguratie migreren</span><span class="sxs-lookup"><span data-stu-id="de267-147">Migrate portal configuration</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [<span data-ttu-id="de267-148">Solution Lifecycle Management: Dynamics 365 voor Customer Engagement-apps</span><span class="sxs-lookup"><span data-stu-id="de267-148">Solution Lifecycle Management: Dynamics 365 for Customer Engagement apps</span></span>](https://www.microsoft.com/download/details.aspx?id=57777)
