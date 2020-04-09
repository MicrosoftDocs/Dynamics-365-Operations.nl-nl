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
ms.openlocfilehash: 34c10e38400a72a670a93f2a72d0aa7a4aed561a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172755"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a><span data-ttu-id="3509f-103">Problemen met de module Twee keer wegschrijven oplossen in Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="3509f-103">Troubleshoot issues with the Dual-write module in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="3509f-104">Dit onderwerp bevat informatie voor het oplossen van problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3509f-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="3509f-105">Dit onderwerp bevat specifieke informatie over het oplossen van problemen met betrekking tot de module **Twee keer wegschrijven** in Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="3509f-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3509f-106">In sommige problemen die in dit onderwerp worden beschreven, is mogelijk de rol van systeembeheerder vereist of de referenties van de Microsoft Azure Active Directory-tenantbeheerder (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="3509f-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="3509f-107">In de sectie voor elk probleem wordt uitgelegd of een specifieke rol of referenties vereist zijn.</span><span class="sxs-lookup"><span data-stu-id="3509f-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="3509f-108">U kunt de module voor Twee keer wegschrijven niet laden in een Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="3509f-108">You can't load the Dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="3509f-109">Als u de pagina **Twee keer wegschrijven** niet kunt openen door het selecteren van de tegel **Twee keer wegschrijven** in de werkruimte **Gegevensbeheer**, is de gegevensintegratieservice waarschijnlijk niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="3509f-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="3509f-110">Maak een ondersteuningsticket met een aanvraag voor het opnieuw starten van de gegevensintegratieservice.</span><span class="sxs-lookup"><span data-stu-id="3509f-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-entity-mapping"></a><span data-ttu-id="3509f-111">Fout bij het maken van een nieuwe entiteitstoewijzing</span><span class="sxs-lookup"><span data-stu-id="3509f-111">Error when you try to create a new entity mapping</span></span>

<span data-ttu-id="3509f-112">**Vereiste referenties om het probleem op te lossen:** Azure AD-tenantbeheerder</span><span class="sxs-lookup"><span data-stu-id="3509f-112">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="3509f-113">Het volgende foutbericht kan worden weergegeven wanneer u een nieuwe entiteit probeert te configureren voor Twee keer wegschrijven:</span><span class="sxs-lookup"><span data-stu-id="3509f-113">You might receive the following error message when you try to configure a new entity for dual-write:</span></span>

<span data-ttu-id="3509f-114">*Statuscode van antwoord geeft geen positief resultaat: 401 (Niet-geautoriseerd)*</span><span class="sxs-lookup"><span data-stu-id="3509f-114">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>

<span data-ttu-id="3509f-115">Deze fout treedt op omdat alleen een Azure AD-tenantbeheerder een nieuwe entiteitstoewijzing kan toevoegen.</span><span class="sxs-lookup"><span data-stu-id="3509f-115">This error occurs because only an Azure AD tenant admin can add a new entity mapping.</span></span>

<span data-ttu-id="3509f-116">Als u het probleem wilt verhelpen, meldt u zich aan bij de Finance and Operations-app als een Azure AD-tenantbeheerder.</span><span class="sxs-lookup"><span data-stu-id="3509f-116">To fix the issue, sign in to the Finance and Operations app as an Azure AD admin tenant.</span></span> <span data-ttu-id="3509f-117">Ga ook naar web.PowerApps.com en valideer de verbinding opnieuw.</span><span class="sxs-lookup"><span data-stu-id="3509f-117">You must also go to web.PowerApps.com and revalidate your connection.</span></span>

## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="3509f-118">Fout bij het openen van de gebruikersinterface voor twee keer wegschrijven</span><span class="sxs-lookup"><span data-stu-id="3509f-118">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="3509f-119">Het volgende foutbericht kan worden weergegeven wanneer u Twee keer wegschrijven probeert te openen vanuit de werkruimte **Gegevensbeheer**:</span><span class="sxs-lookup"><span data-stu-id="3509f-119">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="3509f-120">*login.microsoftonline.com heeft geen verbinding gemaakt.*</span><span class="sxs-lookup"><span data-stu-id="3509f-120">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="3509f-121">Meld u aan met een InPrivate-venster in Microsoft Edge, een incognito-venster in Chromium of een incognito-venster in Google Chrome om het probleem op te lossen.</span><span class="sxs-lookup"><span data-stu-id="3509f-121">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="3509f-122">U moet ook de blokkering van cookies van derden opheffen of verwijderen.</span><span class="sxs-lookup"><span data-stu-id="3509f-122">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a><span data-ttu-id="3509f-123">Fout bij het koppelen van de omgeving voor twee keer wegschrijven of het toevoegen van een nieuwe entiteitstoewijzing</span><span class="sxs-lookup"><span data-stu-id="3509f-123">Error when you link the environment for dual-write or add a new entity mapping</span></span>

<span data-ttu-id="3509f-124">**Vereiste referenties om het probleem op te lossen:** Azure AD-tenantbeheerder</span><span class="sxs-lookup"><span data-stu-id="3509f-124">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="3509f-125">De volgende fout kan optreden bij het koppelen of maken van toewijzingen:</span><span class="sxs-lookup"><span data-stu-id="3509f-125">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="3509f-126">*Statuscode van antwoord geeft geen positief resultaat: 403 (tokenexchange).<br> Sessie-id: \<uw sessie-id\><br> Hoofdactiviteit-id: \<uw hoofdactiviteit-id\>*</span><span class="sxs-lookup"><span data-stu-id="3509f-126">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="3509f-127">Deze fout kan optreden als u niet over voldoende machtigingen beschikt om Twee keer wegschrijven te koppelen of toewijzingen te maken.</span><span class="sxs-lookup"><span data-stu-id="3509f-127">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="3509f-128">U moet een Azure AD-tenantbeheerdersaccount gebruiken om omgevingen te koppelen en nieuwe entiteitstoewijzingen toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="3509f-128">You must use an Azure AD tenant admin account to link environments and add new entity mappings.</span></span> <span data-ttu-id="3509f-129">Na de installatie kunt u echter een niet-beheerdersaccount gebruiken om de status te bewaken en de toewijzingen te bewerken.</span><span class="sxs-lookup"><span data-stu-id="3509f-129">However, after setup, you can use a non-admin account to monitor status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-entity-mapping"></a><span data-ttu-id="3509f-130">Fout bij het stoppen van de entiteitstoewijzing</span><span class="sxs-lookup"><span data-stu-id="3509f-130">Error when you stop the entity mapping</span></span>

<span data-ttu-id="3509f-131">Mogelijk wordt het volgende foutbericht weergegeven wanneer u entiteitstoewijzingen probeert te stoppen:</span><span class="sxs-lookup"><span data-stu-id="3509f-131">You might receive the following error message when you try to stop the entity mappings:</span></span>

<span data-ttu-id="3509f-132">*\[Verboden\], \[{"status":403,"bron":"","bericht":"Fout bij het uitwisselen van tokens: gebruiker heeft geen toegang tot verbinding dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], de externe server heeft een fout geretourneerd: (403) Verboden.*</span><span class="sxs-lookup"><span data-stu-id="3509f-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="3509f-133">Deze fout treedt op wanneer de gekoppelde Common Data Service-omgeving niet beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="3509f-133">This error occurs when the linked Common Data Service environment isn't available.</span></span>

<span data-ttu-id="3509f-134">Maak een ticket voor het gegevensintegratieteam om het probleem op te lossen.</span><span class="sxs-lookup"><span data-stu-id="3509f-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="3509f-135">Koppel de netwerktracering zodat het gegevensintegratieteam de toewijzingen kan markeren als **Wordt niet uitgevoerd** in de backend.</span><span class="sxs-lookup"><span data-stu-id="3509f-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>
