---
title: Problemen met de module Twee keer wegschrijven oplossen in Finance and Operations-apps
description: Dit onderwerp bevat informatie over het oplossen van problemen met betrekking tot de module Twee keer wegschrijven in Finance and Operations-apps.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
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
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 853791d5ffc1d92b9fbafa2acc13cd5543c38196
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275528"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a><span data-ttu-id="12781-103">Problemen met de module Twee keer wegschrijven oplossen in Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="12781-103">Troubleshoot issues with the dual-write module in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="12781-104">Dit onderwerp bevat informatie voor het oplossen van problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="12781-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="12781-105">Dit onderwerp bevat specifieke informatie over het oplossen van problemen met betrekking tot de module **Twee keer wegschrijven** in Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="12781-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="12781-106">In sommige problemen die in dit onderwerp worden beschreven, is mogelijk de rol van systeembeheerder vereist of de referenties van de Microsoft Azure Active Directory-tenantbeheerder (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="12781-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="12781-107">In de sectie voor elk probleem wordt uitgelegd of een specifieke rol of referenties vereist zijn.</span><span class="sxs-lookup"><span data-stu-id="12781-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="12781-108">U kunt de module voor Twee keer wegschrijven niet laden in een Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="12781-108">You can't load the dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="12781-109">Als u de pagina **Twee keer wegschrijven** niet kunt openen door het selecteren van de tegel **Twee keer wegschrijven** in de werkruimte **Gegevensbeheer**, is de gegevensintegratieservice waarschijnlijk niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="12781-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="12781-110">Maak een ondersteuningsticket met een aanvraag voor het opnieuw starten van de gegevensintegratieservice.</span><span class="sxs-lookup"><span data-stu-id="12781-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-entity-map"></a><span data-ttu-id="12781-111">Fout bij het maken van een nieuwe entiteitstoewijzing</span><span class="sxs-lookup"><span data-stu-id="12781-111">Error when you try to create a new entity map</span></span>

<span data-ttu-id="12781-112">**Vereiste referenties om het probleem op te lossen:** dezelfde gebruiker die Twee keer wegschrijven heeft ingesteld.</span><span class="sxs-lookup"><span data-stu-id="12781-112">**Required credentials to fix the issue:** The same user that setup dual-write.</span></span>

<span data-ttu-id="12781-113">Het volgende foutbericht kan worden weergegeven wanneer u een nieuwe entiteit probeert te configureren voor Twee keer wegschrijven.</span><span class="sxs-lookup"><span data-stu-id="12781-113">You might receive the following error message when you try to configure a new entity for dual-write.</span></span> <span data-ttu-id="12781-114">De enige gebruiker die een toewijzing kan maken, is de gebruiker die de verbinding voor Twee keer wegschrijven heeft ingesteld.</span><span class="sxs-lookup"><span data-stu-id="12781-114">The only user that can create a map is the user who setup the dual-write connection.</span></span>

<span data-ttu-id="12781-115">*Statuscode van antwoord geeft geen positief resultaat: 401 (Niet-geautoriseerd)*</span><span class="sxs-lookup"><span data-stu-id="12781-115">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>


## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="12781-116">Fout bij het openen van de gebruikersinterface voor twee keer wegschrijven</span><span class="sxs-lookup"><span data-stu-id="12781-116">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="12781-117">Het volgende foutbericht kan worden weergegeven wanneer u Twee keer wegschrijven probeert te openen vanuit de werkruimte **Gegevensbeheer**:</span><span class="sxs-lookup"><span data-stu-id="12781-117">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="12781-118">*login.microsoftonline.com heeft geen verbinding gemaakt.*</span><span class="sxs-lookup"><span data-stu-id="12781-118">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="12781-119">Meld u aan met een InPrivate-venster in Microsoft Edge, een incognito-venster in Chromium of een incognito-venster in Google Chrome om het probleem op te lossen.</span><span class="sxs-lookup"><span data-stu-id="12781-119">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="12781-120">U moet ook de blokkering van cookies van derden opheffen of verwijderen.</span><span class="sxs-lookup"><span data-stu-id="12781-120">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a><span data-ttu-id="12781-121">Fout bij het koppelen van de omgeving voor twee keer wegschrijven of het toevoegen van een nieuwe entiteitstoewijzing</span><span class="sxs-lookup"><span data-stu-id="12781-121">Error when you link the environment for dual-write or add a new entity mapping</span></span>

<span data-ttu-id="12781-122">**Vereiste rol om het probleem op te lossen:** systeembeheerder in Finance and Operations-apps en Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="12781-122">**Required role to fix the issue:** System administrator in both Finance and Operations apps and Common Data Service.</span></span>

<span data-ttu-id="12781-123">De volgende fout kan optreden bij het koppelen of maken van toewijzingen:</span><span class="sxs-lookup"><span data-stu-id="12781-123">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="12781-124">*Statuscode van antwoord geeft geen positief resultaat: 403 (tokenexchange).<br> Sessie-id: \<uw sessie-id\><br> Hoofdactiviteit-id: \<uw hoofdactiviteit-id\>*</span><span class="sxs-lookup"><span data-stu-id="12781-124">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="12781-125">Deze fout kan optreden als u niet over voldoende machtigingen beschikt om Twee keer wegschrijven te koppelen of toewijzingen te maken.</span><span class="sxs-lookup"><span data-stu-id="12781-125">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="12781-126">Deze fout kan ook optreden als de Common Data Service-omgeving opnieuw is ingesteld zonder het ontkoppelen van twee keer wegschrijven.</span><span class="sxs-lookup"><span data-stu-id="12781-126">This error can also occur if the Common Data Service environment was reset without unlinking dual-write.</span></span> <span data-ttu-id="12781-127">Alle gebruikers met de rol van systeembeheerder in Finance and Operations-apps en Common Data Service kunnen de omgevingen koppelen.</span><span class="sxs-lookup"><span data-stu-id="12781-127">Any user with system administrator role in both Finance and Operations apps and Common Data Service can link the environments.</span></span> <span data-ttu-id="12781-128">Alleen de gebruiker die de verbinding voor Twee keer wegschrijven heeft ingesteld, kan nieuwe entiteitstoewijzingen toevoegen.</span><span class="sxs-lookup"><span data-stu-id="12781-128">Only the user who setup the dual-write connection can add new entity maps.</span></span> <span data-ttu-id="12781-129">Na de installatie kunnen alle gebruikers met de rol van systeembeheerder de status controleren en de toewijzingen bewerken.</span><span class="sxs-lookup"><span data-stu-id="12781-129">After setup, any user with system administrator role can monitor the status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-entity-mapping"></a><span data-ttu-id="12781-130">Fout bij het stoppen van de entiteitstoewijzing</span><span class="sxs-lookup"><span data-stu-id="12781-130">Error when you stop the entity mapping</span></span>

<span data-ttu-id="12781-131">Mogelijk wordt het volgende foutbericht weergegeven wanneer u entiteitstoewijzingen probeert te stoppen:</span><span class="sxs-lookup"><span data-stu-id="12781-131">You might receive the following error message when you try to stop the entity mappings:</span></span>

<span data-ttu-id="12781-132">*\[Verboden\], \[{"status":403,"bron":"","bericht":"Fout bij het uitwisselen van tokens: gebruiker heeft geen toegang tot verbinding dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], de externe server heeft een fout geretourneerd: (403) Verboden.*</span><span class="sxs-lookup"><span data-stu-id="12781-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="12781-133">Deze fout treedt op wanneer de gekoppelde Common Data Service-omgeving niet beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="12781-133">This error occurs when the linked Common Data Service environment isn't available.</span></span>

<span data-ttu-id="12781-134">Maak een ticket voor het gegevensintegratieteam om het probleem op te lossen.</span><span class="sxs-lookup"><span data-stu-id="12781-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="12781-135">Koppel de netwerktracering zodat het gegevensintegratieteam de toewijzingen kan markeren als **Wordt niet uitgevoerd** in de backend.</span><span class="sxs-lookup"><span data-stu-id="12781-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>

## <a name="error-while-trying-to-start-an-entity-mapping"></a><span data-ttu-id="12781-136">Fout tijdens het starten van een entiteitstoewijzing</span><span class="sxs-lookup"><span data-stu-id="12781-136">Error while trying to start an entity mapping</span></span>

<span data-ttu-id="12781-137">Er wordt een foutbericht van de volgende strekking weergegeven wanneer u deze status van een toewijzing probeert in te stellen op **Wordt uitgevoerd**:</span><span class="sxs-lookup"><span data-stu-id="12781-137">You might receive an error like the following when you try to set that state of a mapping to **Running**:</span></span>

<span data-ttu-id="12781-138">*Kan de initiële gegevenssynchronisatie niet voltooien. Fout: Twee keer wegschrijven mislukt - registratie van de invoegtoepassing is mislukt: kan geen opzoekmetagegevens maken voor Twee keer wegschrijven. De verwijzing naar een object is niet ingesteld op een exemplaar van een object.*</span><span class="sxs-lookup"><span data-stu-id="12781-138">*Unable to complete initial data sync. Error: dual-write failure - plugin registration failed: Unable to build dual-write lookup metadata. Error object reference not set to an instance of an object.*</span></span>

<span data-ttu-id="12781-139">De correctie voor deze fout is afhankelijk van de oorzaak van de fout:</span><span class="sxs-lookup"><span data-stu-id="12781-139">The fix for this error depends on the cause of the error:</span></span>

+ <span data-ttu-id="12781-140">Als de toewijzing afhankelijke toewijzingen heeft, moet u ervoor zorgen dat u de afhankelijke toewijzingen van deze entiteitstoewijzing inschakelt.</span><span class="sxs-lookup"><span data-stu-id="12781-140">If the mapping has dependent mappings, then make sure to enable the dependent mappings of this entity mapping.</span></span>
+ <span data-ttu-id="12781-141">Er zijn mogelijk geen bron- of doelvelden toegewezen aan de toewijzing.</span><span class="sxs-lookup"><span data-stu-id="12781-141">The mapping might be missing source or destination fields.</span></span> <span data-ttu-id="12781-142">Als een veld in de Finance and Operations-app ontbreekt, volgt u de stappen in de sectie [Probleem met ontbrekende entiteitsvelden in toewijzingen](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps).</span><span class="sxs-lookup"><span data-stu-id="12781-142">If a field in the Finance and Operations app is missing, then follow the steps in the section [Missing entity fields issue on maps](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps).</span></span> <span data-ttu-id="12781-143">Als een veld in Common Data Service ontbreekt, klikt u op de knop **Entiteiten vernieuwen** in de toewijzing, zodat de velden automatisch opnieuw worden gevuld in de toewijzing.</span><span class="sxs-lookup"><span data-stu-id="12781-143">If a field in Common Data Service is missing, then click **Refresh entities** button on the mapping so that the fields are automatically populated back into the mapping.</span></span>
