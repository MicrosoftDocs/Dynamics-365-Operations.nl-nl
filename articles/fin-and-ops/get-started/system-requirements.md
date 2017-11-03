---
title: Systeemvereisten voor cloudimplementaties
description: In dit onderwerp worden systeemvereisten voor de actuele versie van Microsoft Dynamics 365 for Finance and Operations beschreven voor cloudimplementaties.
author: sericks007
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 83637b4b2ccc01950e68569b3b8bee1a7cd69855
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="system-requirements-for-cloud-deployments"></a><span data-ttu-id="ddcf6-103">Systeemvereisten voor cloudimplementaties</span><span class="sxs-lookup"><span data-stu-id="ddcf6-103">System requirements for cloud deployments</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ddcf6-104">In dit onderwerp worden systeemvereisten voor de actuele versie van Microsoft Dynamics 365 for Finance and Operations beschreven voor cloudimplementaties.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-104">This topic lists the system requirements for the current version of Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, for cloud deployments.</span></span> <span data-ttu-id="ddcf6-105">Voordat u Finance and Operations installeert, controleert u indien deze stap van toepassing is, of het systeem waarmee u werkt, voldoet aan de minimale vereisten voor netwerk, hardware en software.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-105">Before you install Finance and Operations, when this step is appropriate, verify that the system that you're working with meets or exceeds the minimum network, hardware, and software requirements.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="ddcf6-106">Ondersteunde webbrowsers</span><span class="sxs-lookup"><span data-stu-id="ddcf6-106">Supported web browsers</span></span>
<span data-ttu-id="ddcf6-107">De webtoepassing kan worden uitgevoerd in alle onderstaande webbrowsers die op de opgegeven besturingssystemen draaien:</span><span class="sxs-lookup"><span data-stu-id="ddcf6-107">The web application can run in any of the following web browsers that run on the specified operating systems:</span></span>

-   <span data-ttu-id="ddcf6-108">Microsoft Edge (meest recente openbaar beschikbare release) op Windows 10</span><span class="sxs-lookup"><span data-stu-id="ddcf6-108">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
-   <span data-ttu-id="ddcf6-109">Internet Explorer 11 op Windows 10, Windows 8.1 of Windows 7</span><span class="sxs-lookup"><span data-stu-id="ddcf6-109">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
-   <span data-ttu-id="ddcf6-110">Google Chrome (meest recente openbaar beschikbare release) op Windows 10, Windows 8.1, Windows 8, Windows 7 of Google Nexus 10-tablet</span><span class="sxs-lookup"><span data-stu-id="ddcf6-110">Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet</span></span>
-   <span data-ttu-id="ddcf6-111">Apple Safari (meest recente openbaar beschikbare release) op Mac OS X 10.10 (Yosemite), 10.11 (El Capitan), 10.12 (Sierra) of Apple iPad</span><span class="sxs-lookup"><span data-stu-id="ddcf6-111">Apple Safari (latest publicly available version) on Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) or 10.12 (Sierra), or Apple iPad</span></span>

<span data-ttu-id="ddcf6-112">Als u de laatste versie van elke webbrowser wilt opzoeken, gaat u naar de website van de softwarefabrikant.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-112">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> -   <span data-ttu-id="ddcf6-113">Installeer een voorlopige versie van een Chrome-invoegtoepassing om Taakrecorder in te schakelen en schermopnamen te laten vastleggen en deze te laten opnemen in gegenereerde Microsoft Word-documenten.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-113">You must install a pre-release Chrome extension to enable Task Recorder to capture screenshots and include them in Microsoft Word documents that are generated.</span></span> <!---For instructions about how to install the extension, see [Screenshot Extension setup](../../dev-itpro/user-interface/task-recorder).-->
> -   <span data-ttu-id="ddcf6-114">De workfloweditor wordt als ClickOnce-toepassing gestart.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-114">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="ddcf6-115">Alleen Microsoft Edge en Internet Explorer (op een ondersteunde versie van Microsoft Windows) ondersteunen ClickOnce-toepassingen.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-115">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="ddcf6-116">De ClickOnce-toepassing Workfloweditor vereist een compatibel 64-bits besturingssysteem.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-116">The Workflow Editor ClickOnce application requires a 64-bit-compatible operating system.</span></span>
> -   <span data-ttu-id="ddcf6-117">De Report Designer voor financiële rapportage wordt als ClickOnce-toepassing gestart.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-117">The Report Designer for Financial reporting is started as a ClickOnce application.</span></span> <span data-ttu-id="ddcf6-118">Hiervoor is een compatibel 64-bits besturingssysteem vereist.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-118">It requires a 64-bit-compatible operating system.</span></span> <span data-ttu-id="ddcf6-119">Als u Chrome gebruikt, moet u een ClickOnce-extensie installeren om de Report Designer-client te downloaden.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-119">If you’re using Chrome, you must install a ClickOnce extension to download the Report Designer client.</span></span> <span data-ttu-id="ddcf6-120">Als u in de Incognito-modus van Chrome werkt, moet u ervoor zorgen dat de ClickOnce-extensie ook voor de Incognito-modus is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-120">If you use Chrome in Incognito mode, make sure that the ClickOnce extension is also enabled for Incognito mode.</span></span>
> -   <span data-ttu-id="ddcf6-121">Als u PDF-bestanden wilt bekijken, raden wij u aan moderne browsers te gebruiken, zoals Microsoft Edge (meest recente openbaar beschikbare versie) op Windows 10 of Google Chrome (meest recente openbaar beschikbare versie) op Windows 10, Windows 8.1, Windows 8, Windows 7 of Google Nexus 10 tablet.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-121">To preview PDF files, we recommend that you use browsers such as Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>

### <a name="supported-web-browsers-for-retail-cloud-pos"></a><span data-ttu-id="ddcf6-122">Ondersteunde webbrowsers voor Retail Cloud POS</span><span class="sxs-lookup"><span data-stu-id="ddcf6-122">Supported web browsers for Retail Cloud POS</span></span>

<span data-ttu-id="ddcf6-123">Retail Cloud POS kan worden uitgevoerd in alle onderstaande webbrowsers die op de opgegeven besturingssystemen draaien:</span><span class="sxs-lookup"><span data-stu-id="ddcf6-123">Retail Cloud POS can run in any of the following web browsers that run on the specified operating systems:</span></span>

-   <span data-ttu-id="ddcf6-124">Microsoft Edge (meest recente openbaar beschikbare release) op Windows 10</span><span class="sxs-lookup"><span data-stu-id="ddcf6-124">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
-   <span data-ttu-id="ddcf6-125">Internet Explorer 11 op Windows 10, Windows 8.1 of Windows 7</span><span class="sxs-lookup"><span data-stu-id="ddcf6-125">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
-   <span data-ttu-id="ddcf6-126">Chroom (meest recente openbaar beschikbare versie) op Windows 10, Windows 8.1 of Windows 7</span><span class="sxs-lookup"><span data-stu-id="ddcf6-126">Chrome (latest publicly available version) on Windows 10, Windows 8.1, or Windows 7</span></span>

## <a name="network-requirements"></a><span data-ttu-id="ddcf6-127">Netwerkvereisten</span><span class="sxs-lookup"><span data-stu-id="ddcf6-127">Network requirements</span></span>
-   <span data-ttu-id="ddcf6-128">Finance and Operations is ontworpen voor netwerken met een vertragingstijd van 250-300 milliseconden (ms) of minder.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-128">Finance and Operations is designed for networks that have a latency of 250–300 milliseconds (ms) or less.</span></span> <span data-ttu-id="ddcf6-129">Dit is de latentie in een browserclient naar het Microsoft Azure-datacenter waar Finance and Operations wordt gehost.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-129">This latency is the latency from a browser client to the Microsoft Azure datacenter that hosts Finance and Operations.</span></span> <span data-ttu-id="ddcf6-130">Het wordt aangeraden om uw netwerklatentie te testen op <http://www.azurespeed.com>.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-130">We recommend that you test network latency at <http://www.azurespeed.com>.</span></span>
-   <span data-ttu-id="ddcf6-131">De bandbreedtevereisten voor Finance and Operations zijn afhankelijk van uw scenario.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-131">Bandwidth requirements for Finance and Operations depend on your scenario.</span></span> <span data-ttu-id="ddcf6-132">De meest voorkomende scenario's vereisen een bandbreedte van meer dan 50 kilobytes per seconde (kbps).</span><span class="sxs-lookup"><span data-stu-id="ddcf6-132">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span> <span data-ttu-id="ddcf6-133">Voor scenario's met hoge vereisten voor nettolading, zoals scenario's waarbij werkgebieden met uitgebreide aanpassingsmogelijkheden zijn betrokken, wordt extra bandbreedte aanbevolen.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-133">However, we recommend more bandwidth for scenarios that have high payload requirements, such as scenarios that involve workspaces or extensive customization.</span></span>

<span data-ttu-id="ddcf6-134">Over het algemeen is Finance and Operations geoptimaliseerd voor het internet.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-134">In general, Finance and Operations is optimized for the internet.</span></span> <span data-ttu-id="ddcf6-135">Het aantal roundtrips vanuit een browserclient naar het Azure-datacenter is erg klein en de gehele nettolading is gecomprimeerd.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-135">The number of round trips from a browser client to the Azure datacenter is very small, and the whole payload is compressed.</span></span> 

> [!WARNING]
> <span data-ttu-id="ddcf6-136">Bereken de bandbreedtevereisten vanaf een clientlocatie niet door het aantal gebruikers te vermenigvuldigen met de minimale bandbreedte-vereisten.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-136">Don't calculate bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="ddcf6-137">Het gelijktijdige gebruik van een bepaalde locatie is zeer lastig te berekenen.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-137">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="ddcf6-138">Klanten die zich zorgen maken over de bandbreedtevereisten, kunnen het beste een evaluatieversie van Finance and Operations gebruiken.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-138">Customers who are concerned about bandwidth requirements should use a preview version of Finance and Operations.</span></span>

## <a name="net-framework-requirements"></a><span data-ttu-id="ddcf6-139">.NET Framework-vereisten</span><span class="sxs-lookup"><span data-stu-id="ddcf6-139">.NET Framework requirements</span></span>
<span data-ttu-id="ddcf6-140">Finance and Operations vereist Microsoft .NET Framework versie 4.6.2 voor alle ClickOnce-toepassingen, zoals de documentrouterinsgagent.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-140">Finance and Operations requires the Microsoft .NET Framework version 4.6.2 for all ClickOnce applications, such as the document routing agent.</span></span> <span data-ttu-id="ddcf6-141">Zie voor de installatie-instructies [.NET Framework installeren](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="ddcf6-141">For installation instructions, see [Installing the .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="ddcf6-142">Ondersteunde Microsoft Office-toepassingen</span><span class="sxs-lookup"><span data-stu-id="ddcf6-142">Supported Microsoft Office applications</span></span>
<span data-ttu-id="ddcf6-143">De volgende Microsoft Office-toepassingen worden ondersteund in implementaties van Finance and Operations in de cloud:</span><span class="sxs-lookup"><span data-stu-id="ddcf6-143">The following Microsoft Office applications are supported in cloud and on-premises deployments of Finance and Operations:</span></span>

-   <span data-ttu-id="ddcf6-144">Als u de invoegtoepassingen voor Microsoft Word en Microsoft Excel wilt uitvoeren, moet Microsoft Office 2016 voor Windows of Mac zijn geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-144">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="ddcf6-145">Zie voor meer informatie over de versievereisten [Probleemoplossing voor Office-integratie](../../dev-itpro/office-integration/office-integration-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="ddcf6-145">For more information about version requirements, see [Office integration troubleshooting](../../dev-itpro/office-integration/office-integration-troubleshooting.md).</span></span>
-   <span data-ttu-id="ddcf6-146">Als u documenten wilt weergeven die worden gegenereerd door de functie Exporteren naar Excel of Exporteren naar Word, moet Microsoft Office 2007 of hoger zijn geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-146">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="retail-modern-pos-requirements"></a><span data-ttu-id="ddcf6-147">Vereisten voor Retail Modern POS</span><span class="sxs-lookup"><span data-stu-id="ddcf6-147">Retail Modern POS requirements</span></span>

> [!NOTE]
> <span data-ttu-id="ddcf6-148">Als Retail Modern POS een offlinedatabase gebruikt, moet de computer voldoen aan alle systeemvereisten voor Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-148">If Retail Modern POS will use an offline database, the computer must meet all system requirements for Microsoft SQL Server.</span></span> <span data-ttu-id="ddcf6-149">Een offlinedatabase voor Retail Modern POS werkt op Microsoft SQL Server 2012 met Service Pack 3 of hoger, Microsoft SQL Server-2014 met Service Pack 2 of hoger en Microsoft SQL Server 2016.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-149">A Retail Modern POS offline database will work on Microsoft SQL Server 2012 with Service Pack 3 or later, Microsoft SQL Server 2014 with Service Pack 2 or later, and Microsoft SQL Server 2016.</span></span> <span data-ttu-id="ddcf6-150">U kunt het beste altijd de meest recente versie gebruiken die beschikbaar is en de meest recente servicepacks installeren.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-150">We recommend that you always use the latest version that is available, and that you install all the latest service packs.</span></span>

### <a name="supported-operating-systems"></a><span data-ttu-id="ddcf6-151">Ondersteunde besturingssystemen</span><span class="sxs-lookup"><span data-stu-id="ddcf6-151">Supported operating systems</span></span>

-   <span data-ttu-id="ddcf6-152">Retail Modern POS is een 32-bits toepassing, maar deze kan worden uitgevoerd op zowel x86- als ook x64-architectuur.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-152">Retail Modern POS is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="ddcf6-153">Retail Modern POS wordt alleen ondersteund op de Windows 10-versies Pro, Enterprise, and Enterprise Long Term Servicing Branch (LTSB).</span><span class="sxs-lookup"><span data-stu-id="ddcf6-153">Retail Modern POS is supported only on Windows 10 Pro, Enterprise, and Enterprise Long Term Servicing Branch (LTSB) editions.</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="ddcf6-154">Minimale systeemvereisten</span><span class="sxs-lookup"><span data-stu-id="ddcf6-154">Minimum system requirements</span></span>

-   <span data-ttu-id="ddcf6-155">De minimale ondersteunde resolutie is 1280 × 1024.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-155">The minimum supported resolution is 1,280 × 1,024.</span></span>
-   <span data-ttu-id="ddcf6-156">De computer waarop de Retail Modern POS wordt uitgevoerd, moet aan deze vereisten voldoen:</span><span class="sxs-lookup"><span data-stu-id="ddcf6-156">The computer that Retail Modern POS runs on must meet these requirements:</span></span>

    -   <span data-ttu-id="ddcf6-157">Tenminste een dual core-processor, die wordt uitgevoerd met minstens 2 GHz.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-157">It must have, at a minimum, a dual-core processor that runs at no less than 2 gigahertz (GHz).</span></span>
    -   <span data-ttu-id="ddcf6-158">Er moet minimaal 3 gigabytes (GB) random-access memory (RAM) beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-158">It must have, at a minimum, 3 gigabytes (GB) of random-access memory (RAM).</span></span>
    -   <span data-ttu-id="ddcf6-159">Er moet een internetverbinding zijn.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-159">It must have internet access.</span></span>

## <a name="retail-hardware-station-requirements"></a><span data-ttu-id="ddcf6-160">Vereisten voor Retail Hardware Station</span><span class="sxs-lookup"><span data-stu-id="ddcf6-160">Retail hardware station requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="ddcf6-161">Ondersteunde besturingssystemen</span><span class="sxs-lookup"><span data-stu-id="ddcf6-161">Supported operating systems</span></span>

-   <span data-ttu-id="ddcf6-162">Retail Hardware Station is een 32-bits toepassing, maar deze kan worden uitgevoerd op zowel x86- als ook x64-architectuur.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-162">Retail hardware station is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="ddcf6-163">Retail Hardware Station wordt ondersteund op de volgende besturingssystemen:</span><span class="sxs-lookup"><span data-stu-id="ddcf6-163">Retail hardware station is supported on the following operating systems:</span></span>

    -   <span data-ttu-id="ddcf6-164">De Windows 7-versies Professional, Enterprise en Ultimate</span><span class="sxs-lookup"><span data-stu-id="ddcf6-164">Windows 7 Professional, Enterprise, and Ultimate editions</span></span> 
    
        > [!NOTE]
        > <span data-ttu-id="ddcf6-165">Windows 7 wordt alleen ondersteund als Internet Explorer 11 handmatig op het systeem is geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-165">Windows 7 is supported only if Internet Explorer 11 is manually installed on the system.</span></span>

    -   <span data-ttu-id="ddcf6-166">De Windows 8.1-versies Update 1 Professional, Enterprise en Embedded</span><span class="sxs-lookup"><span data-stu-id="ddcf6-166">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="ddcf6-167">De Windows 10-versies Pro, Enterprise en Enterprise LTSB</span><span class="sxs-lookup"><span data-stu-id="ddcf6-167">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="ddcf6-168">Minimale systeemvereisten</span><span class="sxs-lookup"><span data-stu-id="ddcf6-168">Minimum system requirements</span></span>

<span data-ttu-id="ddcf6-169">De computer moet voldoen aan alle systeemvereisten voor het installeren en gebruiken van de volgende opties:</span><span class="sxs-lookup"><span data-stu-id="ddcf6-169">The computer must meet all system requirements for installing and using the following items:</span></span>

-   <span data-ttu-id="ddcf6-170">Internet Information Services (IIS)</span><span class="sxs-lookup"><span data-stu-id="ddcf6-170">Internet Information Services (IIS)</span></span>
-   <span data-ttu-id="ddcf6-171">Hardware van derden</span><span class="sxs-lookup"><span data-stu-id="ddcf6-171">Third-party hardware</span></span>

## <a name="retail-store-scale-unit-requirements"></a><span data-ttu-id="ddcf6-172">Vereisten voor Retail Store Scale Unit</span><span class="sxs-lookup"><span data-stu-id="ddcf6-172">Retail Store Scale Unit requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="ddcf6-173">Ondersteunde besturingssystemen</span><span class="sxs-lookup"><span data-stu-id="ddcf6-173">Supported operating systems</span></span>

-   <span data-ttu-id="ddcf6-174">Retail Store Scale Unit is een 32-bits toepassing, maar deze kan worden uitgevoerd op zowel x86- als ook x64-architectuur.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-174">Retail Store Scale Unit is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="ddcf6-175">Retail Store Scale Unit wordt ondersteund op de volgende besturingssystemen:</span><span class="sxs-lookup"><span data-stu-id="ddcf6-175">Retail Store Scale Unit is supported on the following operating systems:</span></span>

    -   <span data-ttu-id="ddcf6-176">De Windows 7-versies Professional, Enterprise en Ultimate</span><span class="sxs-lookup"><span data-stu-id="ddcf6-176">Windows 7 Professional, Enterprise, and Ultimate editions</span></span>
    -   <span data-ttu-id="ddcf6-177">De Windows 8.1-versies Update 1 Professional, Enterprise en Embedded</span><span class="sxs-lookup"><span data-stu-id="ddcf6-177">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="ddcf6-178">De Windows 10-versies Pro, Enterprise en Enterprise LTSB</span><span class="sxs-lookup"><span data-stu-id="ddcf6-178">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="ddcf6-179">Minimale systeemvereisten</span><span class="sxs-lookup"><span data-stu-id="ddcf6-179">Minimum system requirements</span></span>

-   <span data-ttu-id="ddcf6-180">4 GB RAM</span><span class="sxs-lookup"><span data-stu-id="ddcf6-180">4 GB of RAM</span></span>
-   <span data-ttu-id="ddcf6-181">1,6 GHz piekprocessorsnelheid per core (twee cores minimaal)</span><span class="sxs-lookup"><span data-stu-id="ddcf6-181">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
-   <span data-ttu-id="ddcf6-182">Ten minste 10 GB vrije ruimte (de afzetkanaaldatabase kan veel opslagruimte nodig hebben).</span><span class="sxs-lookup"><span data-stu-id="ddcf6-182">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

### <a name="recommended-system-requirements"></a><span data-ttu-id="ddcf6-183">Aanbevolen systeemvereisten</span><span class="sxs-lookup"><span data-stu-id="ddcf6-183">Recommended system requirements</span></span>

-   <span data-ttu-id="ddcf6-184">6 GB RAM</span><span class="sxs-lookup"><span data-stu-id="ddcf6-184">6 GB of RAM</span></span>
-   <span data-ttu-id="ddcf6-185">2,4 GHz i7 (of equivalent) piekprocessorsnelheid per core (vier cores aanbevolen)</span><span class="sxs-lookup"><span data-stu-id="ddcf6-185">2.4 GHz i7 (or equivalent) peak CPU speed per core (Four cores are recommended.)</span></span>
-   <span data-ttu-id="ddcf6-186">Ten minste 10 GB vrije ruimte (de afzetkanaaldatabase kan veel opslagruimte nodig hebben).</span><span class="sxs-lookup"><span data-stu-id="ddcf6-186">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

## <a name="connector-requirements"></a><span data-ttu-id="ddcf6-187">Connectorvereisten</span><span class="sxs-lookup"><span data-stu-id="ddcf6-187">Connector requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="ddcf6-188">Ondersteunde besturingssystemen</span><span class="sxs-lookup"><span data-stu-id="ddcf6-188">Supported operating systems</span></span>

-   <span data-ttu-id="ddcf6-189">De connector voor Microsoft Dynamics AX heeft twee afzonderlijke installatieprogramma's, één voor Async Server Connector-service en één voor Real-time service voor Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-189">The Connector for Microsoft Dynamics AX has two separate installers, one for Async Server Connector service and one for Real-time service for Dynamics AX 2012 R3.</span></span>
-   <span data-ttu-id="ddcf6-190">Beide componenten zijn 32-bits toepassingen, maar kunnen worden uitgevoerd op zowel x86- als ook x64-architectuur.</span><span class="sxs-lookup"><span data-stu-id="ddcf6-190">Both components are 32-bit applications, but they will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="ddcf6-191">Beide onderdelen worden op de volgende besturingssystemen ondersteund:</span><span class="sxs-lookup"><span data-stu-id="ddcf6-191">Both components are supported on the following operating systems:</span></span>

    -   <span data-ttu-id="ddcf6-192">De Windows 7-versies Professional, Enterprise en Ultimate</span><span class="sxs-lookup"><span data-stu-id="ddcf6-192">Windows 7 Professional, Enterprise, and Ultimate editions</span></span>
    -   <span data-ttu-id="ddcf6-193">De Windows 8.1-versies Update 1 Professional, Enterprise en Embedded</span><span class="sxs-lookup"><span data-stu-id="ddcf6-193">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="ddcf6-194">De Windows 10-versies Pro, Enterprise en Enterprise LTSB</span><span class="sxs-lookup"><span data-stu-id="ddcf6-194">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>
    -   <span data-ttu-id="ddcf6-195">Microsoft Windows Server 2012 R2 en Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ddcf6-195">Microsoft Windows Server 2012 R2 and Microsoft Windows Server 2016</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="ddcf6-196">Minimale systeemvereisten</span><span class="sxs-lookup"><span data-stu-id="ddcf6-196">Minimum system requirements</span></span>
-   <span data-ttu-id="ddcf6-197">2 GB RAM (4 GB RAM aanbevolen)</span><span class="sxs-lookup"><span data-stu-id="ddcf6-197">2 GB of RAM (4 GB of RAM are recommended.)</span></span>
-   <span data-ttu-id="ddcf6-198">1,6 GHz piekprocessorsnelheid per core (twee cores minimaal)</span><span class="sxs-lookup"><span data-stu-id="ddcf6-198">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
-   <span data-ttu-id="ddcf6-199">Ten minste 10 GB vrije ruimte (de afzetkanaaldatabase kan veel opslagruimte nodig hebben).</span><span class="sxs-lookup"><span data-stu-id="ddcf6-199">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

## <a name="requirements-for-development-on-local-vms"></a><span data-ttu-id="ddcf6-200">Vereisten voor ontwikkeling op lokale VM's</span><span class="sxs-lookup"><span data-stu-id="ddcf6-200">Requirements for development on local VMs</span></span>
<span data-ttu-id="ddcf6-201">Zie voor informatie over de vereisten voor de ontwikkeling op lokale virtuele machines (VM's) [VM on-premises uitvoeren](../../dev-itpro/dev-tools/access-instances.md).</span><span class="sxs-lookup"><span data-stu-id="ddcf6-201">For information about the requirements for development on local virtual machines (VMs), see [VM running on-premises](../../dev-itpro/dev-tools/access-instances.md).</span></span>


## <a name="see-also"></a><span data-ttu-id="ddcf6-202">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ddcf6-202">See also</span></span>

[<span data-ttu-id="ddcf6-203">Een evaluatie-exemplaar van Dynamics 365 for Finance and Operations, Enterprise-editie krijgen</span><span class="sxs-lookup"><span data-stu-id="ddcf6-203">Get an evaluation copy of Dynamics 365 for Finance and Operations, Enterprise edition</span></span>](../../dev-itpro/dev-tools/get-evaluation-copy.md)

