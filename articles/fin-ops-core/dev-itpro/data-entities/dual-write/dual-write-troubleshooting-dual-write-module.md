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
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a>Problemen met de module Twee keer wegschrijven oplossen in Finance and Operations-apps

[!include [banner](../../includes/banner.md)]



Dit onderwerp bevat informatie voor het oplossen van problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Common Data Service. Dit onderwerp bevat specifieke informatie over het oplossen van problemen met betrekking tot de module **Twee keer wegschrijven** in Finance and Operations-apps.

> [!IMPORTANT]
> In sommige problemen die in dit onderwerp worden beschreven, is mogelijk de rol van systeembeheerder vereist of de referenties van de Microsoft Azure Active Directory-tenantbeheerder (Azure AD). In de sectie voor elk probleem wordt uitgelegd of een specifieke rol of referenties vereist zijn.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>U kunt de module voor Twee keer wegschrijven niet laden in een Finance and Operations-app

Als u de pagina **Twee keer wegschrijven** niet kunt openen door het selecteren van de tegel **Twee keer wegschrijven** in de werkruimte **Gegevensbeheer**, is de gegevensintegratieservice waarschijnlijk niet beschikbaar. Maak een ondersteuningsticket met een aanvraag voor het opnieuw starten van de gegevensintegratieservice.

## <a name="error-when-you-try-to-create-a-new-entity-mapping"></a>Fout bij het maken van een nieuwe entiteitstoewijzing

**Vereiste referenties om het probleem op te lossen:** Azure AD-tenantbeheerder

Het volgende foutbericht kan worden weergegeven wanneer u een nieuwe entiteit probeert te configureren voor Twee keer wegschrijven:

*Statuscode van antwoord geeft geen positief resultaat: 401 (Niet-geautoriseerd)*

Deze fout treedt op omdat alleen een Azure AD-tenantbeheerder een nieuwe entiteitstoewijzing kan toevoegen.

Als u het probleem wilt verhelpen, meldt u zich aan bij de Finance and Operations-app als een Azure AD-tenantbeheerder. Ga ook naar web.PowerApps.com en valideer de verbinding opnieuw.

## <a name="error-when-you-open-the-dual-write-user-interface"></a>Fout bij het openen van de gebruikersinterface voor twee keer wegschrijven

Het volgende foutbericht kan worden weergegeven wanneer u Twee keer wegschrijven probeert te openen vanuit de werkruimte **Gegevensbeheer**:

*login.microsoftonline.com heeft geen verbinding gemaakt.*

Meld u aan met een InPrivate-venster in Microsoft Edge, een incognito-venster in Chromium of een incognito-venster in Google Chrome om het probleem op te lossen. U moet ook de blokkering van cookies van derden opheffen of verwijderen.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a>Fout bij het koppelen van de omgeving voor twee keer wegschrijven of het toevoegen van een nieuwe entiteitstoewijzing

**Vereiste referenties om het probleem op te lossen:** Azure AD-tenantbeheerder

De volgende fout kan optreden bij het koppelen of maken van toewijzingen:

*Statuscode van antwoord geeft geen positief resultaat: 403 (tokenexchange).<br> Sessie-id: \<uw sessie-id\><br> Hoofdactiviteit-id: \<uw hoofdactiviteit-id\>*

Deze fout kan optreden als u niet over voldoende machtigingen beschikt om Twee keer wegschrijven te koppelen of toewijzingen te maken. U moet een Azure AD-tenantbeheerdersaccount gebruiken om omgevingen te koppelen en nieuwe entiteitstoewijzingen toe te voegen. Na de installatie kunt u echter een niet-beheerdersaccount gebruiken om de status te bewaken en de toewijzingen te bewerken.

## <a name="error-when-you-stop-the-entity-mapping"></a>Fout bij het stoppen van de entiteitstoewijzing

Mogelijk wordt het volgende foutbericht weergegeven wanneer u entiteitstoewijzingen probeert te stoppen:

*\[Verboden\], \[{"status":403,"bron":"","bericht":"Fout bij het uitwisselen van tokens: gebruiker heeft geen toegang tot verbinding dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], de externe server heeft een fout geretourneerd: (403) Verboden.*

Deze fout treedt op wanneer de gekoppelde Common Data Service-omgeving niet beschikbaar is.

Maak een ticket voor het gegevensintegratieteam om het probleem op te lossen. Koppel de netwerktracering zodat het gegevensintegratieteam de toewijzingen kan markeren als **Wordt niet uitgevoerd** in de backend.
