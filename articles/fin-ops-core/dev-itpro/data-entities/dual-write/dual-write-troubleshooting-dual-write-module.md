---
title: Problemen met twee keer wegschrijven oplossen in de apps voor financiën en bedrijfsactiviteiten
description: Dit artikel bevat informatie over het oplossen van problemen met betrekking tot de module Twee keer wegschrijven in apps voor financiële en bedrijfsactiviteiten.
author: RamaKrishnamoorthy
ms.date: 04/18/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 36f7969eb0bdbc64ade14a5bb97b4b708486d226
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864567"
---
# <a name="troubleshoot-dual-write-issues-in-finance-and-operations-apps"></a>Problemen met twee keer wegschrijven oplossen in de apps voor financiën en bedrijfsactiviteiten

[!include [banner](../../includes/banner.md)]



Dit artikel bevat informatie voor het oplossen van problemen met de integratie van Twee keer wegschrijven tussen apps voor financiële en bedrijfsactiviteiten en Dataverse. Dit onderwerp bevat met name informatie over het oplossen van problemen met betrekking tot de module **Twee keer wegschrijven** in apps voor financiële en bedrijfsactiviteiten.

> [!IMPORTANT]
> In sommige problemen die in dit artikel worden beschreven, is mogelijk de rol van systeembeheerder vereist of de referenties van de Microsoft Azure Active Directory-tenantbeheerder (Azure AD). In de sectie voor elk probleem wordt uitgelegd of een specifieke rol of referenties vereist zijn.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>U kunt de module voor Twee keer wegschrijven niet laden in een app voor financiële en bedrijfsactiviteiten

Als u de pagina **Twee keer wegschrijven** niet kunt openen door het selecteren van de tegel **Twee keer wegschrijven** in de werkruimte **Gegevensbeheer**, is de gegevensintegratieservice waarschijnlijk niet beschikbaar. Maak een ondersteuningsticket met een aanvraag voor het opnieuw starten van de gegevensintegratieservice.

## <a name="error-when-you-try-to-create-a-new-table-map"></a>Fout bij het maken van een nieuwe tabeltoewijzing

**Vereiste referenties om het probleem op te lossen:** dezelfde gebruiker die Twee keer wegschrijven heeft ingesteld.

Het volgende foutbericht kan worden weergegeven wanneer u een nieuwe tabel probeert te configureren voor Twee keer wegschrijven. De enige gebruiker die een toewijzing kan maken, is de gebruiker die de verbinding voor Twee keer wegschrijven heeft ingesteld.

*Statuscode van antwoord geeft geen positief resultaat aan: 401 (Niet-geautoriseerd).*

## <a name="error-when-you-open-the-dual-write-user-interface"></a>Fout bij het openen van de gebruikersinterface voor twee keer wegschrijven

Het volgende foutbericht kan worden weergegeven wanneer u Twee keer wegschrijven probeert te openen vanuit de werkruimte **Gegevensbeheer**:

*login.microsoftonline.com heeft geen verbinding gemaakt.*

Meld u aan met een InPrivate-venster in Microsoft Edge, een incognito-venster in Chromium of een incognito-venster in Google Chrome om het probleem op te lossen. U moet ook de blokkering van cookies van derden opheffen of verwijderen.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a>Fout bij het koppelen van de omgeving voor twee keer wegschrijven of het toevoegen van een nieuwe tabeltoewijzing

**Vereiste rol om het probleem op te lossen:** systeembeheerder voor zowel apps voor financiële en bedrijfsactiviteiten als Dataverse.

De volgende fout kan optreden bij het koppelen of maken van toewijzingen:

```dos
Response status code does not indicate success: 403 (tokenexchange).
Session ID: \<your session id\>
Root activity ID: \<your root activity\> id
```

Deze fout kan optreden als u niet over voldoende machtigingen beschikt om Twee keer wegschrijven te koppelen of toewijzingen te maken. Deze fout kan ook optreden als de Dataverse-omgeving opnieuw is ingesteld zonder het ontkoppelen van twee keer wegschrijven. Alle gebruikers met de rol van systeembeheerder in apps voor financiële en bedrijfsactiviteiten en Dataverse kunnen de omgevingen koppelen. Alleen de gebruiker die de verbinding voor Twee keer wegschrijven heeft ingesteld, kan nieuwe tabeltoewijzingen toevoegen. Na de installatie kunnen alle gebruikers met de rol van systeembeheerder de status controleren en de toewijzingen bewerken.

## <a name="error-when-you-stop-the-table-mapping"></a>Fout bij het stoppen van de tabeltoewijzing

Mogelijk wordt het volgende foutbericht weergegeven wanneer u tabeltoewijzingen probeert te stoppen:

*\[Verboden\], \[{"status":403,"bron":"","bericht":"Fout bij het uitwisselen van tokens: gebruiker heeft geen toegang tot verbinding dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], de externe server heeft een fout geretourneerd: (403) Verboden.*

Deze fout treedt op wanneer de gekoppelde Dataverse-omgeving niet beschikbaar is.

Maak een ticket voor het gegevensintegratieteam om het probleem op te lossen. Koppel de netwerktracering zodat het gegevensintegratieteam de toewijzingen kan markeren als **Wordt niet uitgevoerd** in de backend.

## <a name="enable-parallel-processing-in-finance-and-operations-apps-to-improve-performance"></a>Parallelle verwerking in apps voor financiën en bedrijfsactiviteiten inschakelen om de prestaties te verbeteren

Het inschakelen van parallelle verwerking kan de tijd beperken die nodig is om gegevens vanuit Dynamics 365 Customer Engagement en Microsoft Dataverse in apps voor financiën en bedrijfsactiviteiten. 

Ga als volgt te werk om parallelle verwerking in apps voor financiën en bedrijfsactiviteiten in te schakelen.

1. Log in bij uw omgeving voor financiën en bedrijfsactiviteiten.
2. Ga naar **Gegevensbeheer > Raamwerkparameters**.
3. Selecteer **Entiteitsinstellingen** en **Uitvoeringsparameters voor entiteiten configureren**.
4. Voeg de parameters voor parallelle verwerking toe:
    - **Aantal records van importdrempel**: het aantal records dat moet worden uitgevoerd voordat parallelle verwerking wordt ingeschakeld.
    - **Aantal importtaken**: het aantal threads (taken) dat parallel moet worden uitgevoerd.
5. Selecteer **Opslaan**.


## <a name="errors-while-trying-to-start-a-table-mapping"></a>Fouten tijdens het starten van een tabeltoewijzing

### <a name="unable-to-complete-initial-data-sync"></a>Kan initiële gegevenssynchronisatie niet voltooien

Het volgende foutbericht kan worden weergegeven wanneer u probeert de initiële gegevenssynchronisatie uit te voeren:

*Kan de initiële gegevenssynchronisatie niet voltooien. Fout: Twee keer wegschrijven mislukt - registratie van de invoegtoepassing is mislukt: kan geen opzoekmetagegevens maken voor Twee keer wegschrijven. De verwijzing naar een object is niet ingesteld op een exemplaar van een object.*

Wanneer u deze status van een toewijzing probeert in te stellen op **Wordt uitgevoerd**, kan dit foutbericht worden weergegeven. De correctie is afhankelijk van de oorzaak van de fout:

+ Als de toewijzing afhankelijke toewijzingen heeft, moet u ervoor zorgen dat u de afhankelijke toewijzingen van deze tabeltoewijzing inschakelt.
+ De toewijzing mist mogelijk bron- of doelkolommen. Als een kolom in de app voor financiële en bedrijfsactiviteiten ontbreekt, voert u de stappen uit in de sectie [Probleem met ontbrekende tabelkolommen in toewijzingen](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps). Als een kolom in Dataverse ontbreekt, klikt u op de knop **Tabellen vernieuwen** in de toewijzing, zodat de kolommen automatisch opnieuw worden gevuld in de toewijzing.

### <a name="version-mismatch-error-and-upgrading-dual-write-solutions"></a>Fout voor niet-overeenkomende versies en het upgraden van dubbele-schrijfoplossingen

Mogelijk worden de volgende foutberichten weergegeven wanneer u de tabeltoewijzingen probeert uit te voeren:

+ *Klantengroepen (msdyn_customergroups): fout met twee keer wegschrijven - Dynamics 365 for Sales-oplossing 'Dynamics365Company' komt niet overeen met versie. Versie: '2.0.2.10' Vereiste versie: '2.0.133'*
+ *Dynamics 365 for Sales-oplossing 'Dynamics365FinanceExtended' komt niet overeen met versie. Versie: '1.0.0.0' Vereiste versie: '2.0.227'*
+ *Dynamics 365 for Sales-oplossing 'Dynamics365FinanceAndOperationsCommon' komt niet overeen met versie. Versie: '1.0.0.0' Vereiste versie: '2.0.133'*
+ *Dynamics 365 for Sales-oplossing 'CurrencyExchangeRates' komt niet overeen met versie. Versie: '1.0.0.0' Vereiste versie: '2.0.133'*
+ *Dynamics 365 for Sales-oplossing 'Dynamics365SupplyChainExtended' komt niet overeen met versie. Versie: '1.0.0.0' Vereiste versie: '2.0.227'*

Werk de oplossingen voor twee keer wegschrijven in Dataverse bij om de problemen op te lossen. Zorg ervoor dat u een upgrade naar de meest recente oplossing uitvoert die overeenkomt met de vereiste oplossingsversie.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
