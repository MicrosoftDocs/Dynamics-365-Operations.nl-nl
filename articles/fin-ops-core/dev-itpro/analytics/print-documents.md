---
title: Overzicht van Documenten afdrukken
description: U kunt documenten afdrukken met behulp van een lokale printer of een netwerkapparaat. In dit artikel vindt u een overzicht van hoe documenten worden afgedrukt.
author: TJVass
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro, Application User
ms.reviewer: kfend
ms.search.scope: Operations, Core
ms.custom: 69161
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8c8475e26d9a2234d4c429ef1b5e482ac06fde08
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182894"
---
# <a name="document-printing-overview"></a><span data-ttu-id="9f2ef-104">Overzicht van Documenten afdrukken</span><span class="sxs-lookup"><span data-stu-id="9f2ef-104">Document printing overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f2ef-105">U kunt documenten afdrukken met behulp van een lokale printer of een netwerkapparaat.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-105">You can print documents by using either a local printer or a network-connected device.</span></span> <span data-ttu-id="9f2ef-106">In dit artikel vindt u een overzicht van hoe documenten worden afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-106">This article provides an overview of how documents are printed.</span></span>

## <a name="printing-overview"></a><span data-ttu-id="9f2ef-107">Afdrukoverzicht</span><span class="sxs-lookup"><span data-stu-id="9f2ef-107">Printing overview</span></span>

<span data-ttu-id="9f2ef-108">De toepassing biedt geïntegreerde services en clienttoepassingen die het gemakkelijk maken om documenten die bedrijfsactiviteit ondersteunen, te genereren, op te slaan en te distribueren.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-108">The application provides integrated services and client applications that make it easy to generate, store, and distribute documents that support business activity.</span></span> <span data-ttu-id="9f2ef-109">U kunt documenten afdrukken met behulp van een lokale printer of een netwerkapparaat.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-109">You can print documents by using either a local printer or a network-connected device.</span></span> <span data-ttu-id="9f2ef-110">U kunt bovendien de pagina's en rapporten rechtstreeks exporteren vanaf de client als PDF-bestanden of Microsoft Office-documenten.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-110">In addition, you can export pages and reports directly from the client, as PDF files or Microsoft Office documents.</span></span> <span data-ttu-id="9f2ef-111">Ten slotte zorgt de gedistribueerde werkbelasting dat bedrijfsdocumenten rechtstreeks kunt afdrukken vanaf een mobiel apparaat met behulp van netwerkbronnen.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-111">Finally, the distributed workload lets you print business documents directly from a mobile device by using network resources.</span></span> <span data-ttu-id="9f2ef-112">Ook al variëren de afdrukeisen, in alle bedrijfstakken zijn gewoonlijk papieren exemplaren nodig van zakelijke documenten via de toepassing.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-112">Although printing requirements might vary, all industries typically must create hard copies of business documents by using the application.</span></span> <span data-ttu-id="9f2ef-113">Het afdrukken van documenten op netwerkapparaten via gehoste toepassingen vormt een unieke uitdaging.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-113">Printing documents on network devices from hosted applications presents a unique set of challenges.</span></span> <span data-ttu-id="9f2ef-114">Hieronder vindt u enkele voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="9f2ef-114">Here are some examples:</span></span>

- <span data-ttu-id="9f2ef-115">Printerstuurprogramma's zijn mogelijk niet beschikbaar op het apparaat van de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-115">Print drivers might not be available on the user's device.</span></span>
- <span data-ttu-id="9f2ef-116">Het apparaat van de gebruiker kan niet worden verbonden met het bedrijfsnetwerk.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-116">The user's device might not be connected to the corporate network.</span></span>

<span data-ttu-id="9f2ef-117">Door het toewijzen van een host en het uitvoeren van een paar eenvoudige stappen kunnen systeembeheerders implementaties configureren zodat gebruikers rechtstreeks vanuit bedrijfstoepassingen op netwerkapparaten kunnen afdrukken.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-117">By using a dedicated host and following a few easy steps, system administrators can configure deployments so that users can print directly from business applications on network devices.</span></span>

### <a name="application-printing-scenarios"></a><span data-ttu-id="9f2ef-118">Afdrukscenario's voor toepassingen</span><span class="sxs-lookup"><span data-stu-id="9f2ef-118">Application printing scenarios</span></span> 

<span data-ttu-id="9f2ef-119">In de volgende tabel worden de drie primaire afdrukscenario's beschreven.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-119">The following table describes the three primary printing scenarios.</span></span>

| <span data-ttu-id="9f2ef-120">Scenario</span><span class="sxs-lookup"><span data-stu-id="9f2ef-120">Scenario</span></span>                        | <span data-ttu-id="9f2ef-121">Doelstelling</span><span class="sxs-lookup"><span data-stu-id="9f2ef-121">Goal</span></span>                                                      | <span data-ttu-id="9f2ef-122">Oplossing</span><span class="sxs-lookup"><span data-stu-id="9f2ef-122">Solution</span></span> |
|---------------------------------|-----------------------------------------------------------|----------|
| <span data-ttu-id="9f2ef-123">1. Afdrukken wat u ziet</span><span class="sxs-lookup"><span data-stu-id="9f2ef-123">1. Printing what you see</span></span>        | <span data-ttu-id="9f2ef-124">De huidige inhoud van de browser afdrukken.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-124">Print what is currently shown in the browser.</span></span>             | <span data-ttu-id="9f2ef-125">Een afdrukversie van de webpagina wordt gegenereerd voor de browser.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-125">A "print-friendly" version of the webpage is generated for the browser.</span></span> |
| <span data-ttu-id="9f2ef-126">2. interactief afdrukken</span><span class="sxs-lookup"><span data-stu-id="9f2ef-126">2. Interactive printing</span></span>         | <span data-ttu-id="9f2ef-127">Een precisiedocument afdrukken op een lokaal aangesloten apparaat.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-127">Print a precision document on a locally connected device.</span></span> | <span data-ttu-id="9f2ef-128">U kunt een PDF-versie van het rapport exporteren en deze downloaden naar de browser.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-128">You can export a PDF version of the report and download it to the browser.</span></span> |
| <span data-ttu-id="9f2ef-129">3. Afdrukken op een netwerkapparaat</span><span class="sxs-lookup"><span data-stu-id="9f2ef-129">3. Printing on a network device</span></span> | <span data-ttu-id="9f2ef-130">Een precisiedocument verzenden naar een printer voor het domein.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-130">Send a precision document to a domain printer device.</span></span>     | <span data-ttu-id="9f2ef-131">Een precisiedocument wordt verzonden naar een clienttoepassing die wordt uitgevoerd op een server die wordt gehost in een domein van de klant.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-131">A precision document is sent to a client application that runs on a server that is hosted in the customer's domain.</span></span> |

<span data-ttu-id="9f2ef-132">Omdat de oplossing afhankelijk van het scenario verschilt, bevatten toepassingen van Finance geïntegreerde services en functies waarmee gebruikers hun doelen kunnen bereiken:</span><span class="sxs-lookup"><span data-stu-id="9f2ef-132">Because the solution varies, depending on the scenario, applications provide built-in services and tooling to help users accomplish their goals:</span></span>

- <span data-ttu-id="9f2ef-133">**Scenario 1** wordt ondersteund door de weergave in de browser van de HTML5-client.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-133">**Scenario 1** is supported by the browser's rendering of the HTML5 client.</span></span>
- <span data-ttu-id="9f2ef-134">**Scenario 2** maakt gebruik van clienttoepassingen en services van Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-134">**Scenario 2** uses client applications and Microsoft Office 365 services.</span></span>
- <span data-ttu-id="9f2ef-135">**Scenario 3** vereist ondersteuning van clienttoepassingen en services die worden gehost in Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-135">**Scenario 3** requires support from client applications and from services that are hosted in Microsoft Azure.</span></span>

<span data-ttu-id="9f2ef-136">Naast het platform dat in het Azure-abonnement is geïmplementeerd, bevatten Finance and Operations-toepassingen een geïntegreerde, directe Azure-toepassing waarmee ze makkelijker in het domein gehoste apparaten kunnen gebruiken om documenten af te drukken.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-136">In addition to the platform that is deployed to the Azure subscription, Finance and Operations applications provide customers with an integrated, first-party Azure application that helps them more easily use domain-hosted devices to print documents.</span></span>

## <a name="service-overview"></a><span data-ttu-id="9f2ef-137">Serviceoverzicht</span><span class="sxs-lookup"><span data-stu-id="9f2ef-137">Service overview</span></span>
<span data-ttu-id="9f2ef-138">Documenten die worden geproduceerd door de gehoste toepassingen en die wachten om te worden afgedrukt op een netwerkapparaat, worden opgeslagen in de Azure-blobopslag.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-138">While documents that are produced by the hosted applications are waiting to be printed on a network-connected device, they are stored in Azure blob storage.</span></span> <span data-ttu-id="9f2ef-139">De [Documentrouteringsagent](install-document-routing-agent.md) gebruikt Azure-verificatie om een beveiligde verbinding met de Azure-services tot stand te brengen.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-139">The [Document Routing Agent](install-document-routing-agent.md) uses Azure authentication to establish a secure channel to the Azure services.</span></span>

<span data-ttu-id="9f2ef-140">**Uitvoeringsreeks**</span><span class="sxs-lookup"><span data-stu-id="9f2ef-140">**Execution sequence**</span></span>

1. <span data-ttu-id="9f2ef-141">Het rapport wordt gegenereerd door Microsoft SQL Server Reporting Services (SSRS) en opgeslagen in Azure-blobopslag.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-141">The report is generated by Microsoft SQL Server Reporting Services (SSRS) and stored in Azure blob storage.</span></span> <span data-ttu-id="9f2ef-142">Gekoppelde printerinstellingen worden samen met het document opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-142">Attached printer settings are stored together with the document.</span></span>
2. <span data-ttu-id="9f2ef-143">De Documentrouteringsagent voert een query uit in de Azure Service Bus-wachtrij voor actieve taken.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-143">The Document Routing Agent queries the Azure Service Bus queue for active jobs.</span></span>
3. <span data-ttu-id="9f2ef-144">Het document wordt gedownload door de Documentrouteringsagent en in de netwerkprinterwachtrij geplaatst.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-144">The document is downloaded by the Document Routing Agent and spooled to the network printer.</span></span>

<span data-ttu-id="9f2ef-145">Met de clientoplossing kunnen klanten hun afdrukeisen naar wens beheren.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-145">The client-based solution lets customers manage the scale of their printing needs.</span></span> <span data-ttu-id="9f2ef-146">Klanten met een groot volume afdruktaken kunnen veel Documentrouteringsagenten installeren om het aantal gelijktijdige afdrukbewerkingen te vergroten.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-146">Customers who have heavy-volume printing workloads can install many Document Routing Agents to increase the number of concurrent printing operations.</span></span> <span data-ttu-id="9f2ef-147">Andere klanten vereisen mogelijk slechts een paar Documentrouteringsagenten voor het verwerken van hun verwachte afdrukbehoefte.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-147">Alternatively, some customers require very few installations of the Document Routing Agent to handle their anticipated printing needs.</span></span>

### <a name="service-components-for-network-printing"></a><span data-ttu-id="9f2ef-148">Serviceonderdelen voor netwerkafdrukken</span><span class="sxs-lookup"><span data-stu-id="9f2ef-148">Service components for network printing</span></span>

<span data-ttu-id="9f2ef-149">Het volgende diagram toont de basisonderdelen voor het ondersteunen van netwerkafdrukfuncties.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-149">The following diagram shows the basic components that help support network printing operations.</span></span>

<span data-ttu-id="9f2ef-150">[![service-components-for-network-printing\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)</span><span class="sxs-lookup"><span data-stu-id="9f2ef-150">[![service-components-for-network-printing\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)</span></span>

<span data-ttu-id="9f2ef-151">Houd er rekening mee dat één printer kan worden geregistreerd met meerdere documentrouteringsagents.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-151">Note that a single printer can be registered with multiple Document Routing Agents.</span></span> <span data-ttu-id="9f2ef-152">Om te voldoen aan de printervoorkeuren gebruikt de gehoste service het netwerkpad dat een unieke identificatie is voor elke netwerkprinter.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-152">To resolve the printer preferences, the hosted service uses the network path that uniquely identifies every network printer.</span></span> <span data-ttu-id="9f2ef-153">Hierdoor wordt zelfs een printer die door meerdere clients is geregistreerd, als één selectie weergegeven in de lijst met printers die beschikbaar zijn in toepassingen van Finance.</span><span class="sxs-lookup"><span data-stu-id="9f2ef-153">As a result, even when a printer is registered by multiple clients, it appears as a single selection in the list of printers available in applications.</span></span>