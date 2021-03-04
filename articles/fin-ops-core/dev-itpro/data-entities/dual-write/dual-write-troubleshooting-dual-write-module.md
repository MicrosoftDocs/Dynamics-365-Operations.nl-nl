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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2241e7e6219f95115f55bc45a4d94550276e1e21
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683618"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a>Problemen met de module Twee keer wegschrijven oplossen in Finance and Operations-apps

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dit onderwerp bevat informatie voor het oplossen van problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Dataverse. Dit onderwerp bevat specifieke informatie over het oplossen van problemen met betrekking tot de module **Twee keer wegschrijven** in Finance and Operations-apps.

> [!IMPORTANT]
> In sommige problemen die in dit onderwerp worden beschreven, is mogelijk de rol van systeembeheerder vereist of de referenties van de Microsoft Azure Active Directory-tenantbeheerder (Azure AD). In de sectie voor elk probleem wordt uitgelegd of een specifieke rol of referenties vereist zijn.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>U kunt de module voor Twee keer wegschrijven niet laden in een Finance and Operations-app

Als u de pagina **Twee keer wegschrijven** niet kunt openen door het selecteren van de tegel **Twee keer wegschrijven** in de werkruimte **Gegevensbeheer**, is de gegevensintegratieservice waarschijnlijk niet beschikbaar. Maak een ondersteuningsticket met een aanvraag voor het opnieuw starten van de gegevensintegratieservice.

## <a name="error-when-you-try-to-create-a-new-table-map"></a>Fout bij het maken van een nieuwe tabeltoewijzing

**Vereiste referenties om het probleem op te lossen:** dezelfde gebruiker die Twee keer wegschrijven heeft ingesteld.

Het volgende foutbericht kan worden weergegeven wanneer u een nieuwe entiteit probeert te configureren voor Twee keer wegschrijven. De enige gebruiker die een toewijzing kan maken, is de gebruiker die de verbinding voor Twee keer wegschrijven heeft ingesteld.

*Statuscode van antwoord geeft geen positief resultaat: 401 (Niet-geautoriseerd)*


## <a name="error-when-you-open-the-dual-write-user-interface"></a>Fout bij het openen van de gebruikersinterface voor twee keer wegschrijven

Het volgende foutbericht kan worden weergegeven wanneer u Twee keer wegschrijven probeert te openen vanuit de werkruimte **Gegevensbeheer**:

*login.microsoftonline.com heeft geen verbinding gemaakt.*

Meld u aan met een InPrivate-venster in Microsoft Edge, een incognito-venster in Chromium of een incognito-venster in Google Chrome om het probleem op te lossen. U moet ook de blokkering van cookies van derden opheffen of verwijderen.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a>Fout bij het koppelen van de omgeving voor twee keer wegschrijven of het toevoegen van een nieuwe tabeltoewijzing

**Vereiste rol om het probleem op te lossen:** systeembeheerder in Finance and Operations-apps en Dataverse.

De volgende fout kan optreden bij het koppelen of maken van toewijzingen:

*Statuscode van antwoord geeft geen positief resultaat: 403 (tokenexchange).<br> Sessie-id: \<your session id\><br> Hoofdactiviteit-id: \<your root activity id\>*

Deze fout kan optreden als u niet over voldoende machtigingen beschikt om Twee keer wegschrijven te koppelen of toewijzingen te maken. Deze fout kan ook optreden als de Dataverse-omgeving opnieuw is ingesteld zonder het ontkoppelen van twee keer wegschrijven. Alle gebruikers met de rol van systeembeheerder in Finance and Operations-apps en Dataverse kunnen de omgevingen koppelen. Alleen de gebruiker die de verbinding voor Twee keer wegschrijven heeft ingesteld, kan nieuwe tabeltoewijzingen toevoegen. Na de installatie kunnen alle gebruikers met de rol van systeembeheerder de status controleren en de toewijzingen bewerken.

## <a name="error-when-you-stop-the-table-mapping"></a>Fout bij het stoppen van de tabeltoewijzing

Mogelijk wordt het volgende foutbericht weergegeven wanneer u tabeltoewijzingen probeert te stoppen:

*\[Verboden\], \[{"status":403,"bron":"","bericht":"Fout bij het uitwisselen van tokens: gebruiker heeft geen toegang tot verbinding dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], de externe server heeft een fout geretourneerd: (403) Verboden.*

Deze fout treedt op wanneer de gekoppelde Dataverse-omgeving niet beschikbaar is.

Maak een ticket voor het gegevensintegratieteam om het probleem op te lossen. Koppel de netwerktracering zodat het gegevensintegratieteam de toewijzingen kan markeren als **Wordt niet uitgevoerd** in de backend.

## <a name="error-while-trying-to-start-an-table-mapping"></a>Fout tijdens het starten van een tabeltoewijzing

Er wordt een foutbericht van de volgende strekking weergegeven wanneer u deze status van een toewijzing probeert in te stellen op **Wordt uitgevoerd**:

*Kan de initiële gegevenssynchronisatie niet voltooien. Fout: Twee keer wegschrijven mislukt - registratie van de invoegtoepassing is mislukt: kan geen opzoekmetagegevens maken voor Twee keer wegschrijven. De verwijzing naar een object is niet ingesteld op een exemplaar van een object.*

De correctie voor deze fout is afhankelijk van de oorzaak van de fout:

+ Als de toewijzing afhankelijke toewijzingen heeft, moet u ervoor zorgen dat u de afhankelijke toewijzingen van deze tabeltoewijzing inschakelt.
+ Er zijn mogelijk geen bron- of doelvelden toegewezen aan de toewijzing. Als een veld in de Finance and Operations-app ontbreekt, volgt u de stappen in de sectie [Probleem met ontbrekende entiteitsvelden in toewijzingen](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps). Als een veld in Dataverse ontbreekt, klikt u op de knop **Tabellen vernieuwen** in de toewijzing, zodat de velden automatisch opnieuw worden gevuld in de toewijzing.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]