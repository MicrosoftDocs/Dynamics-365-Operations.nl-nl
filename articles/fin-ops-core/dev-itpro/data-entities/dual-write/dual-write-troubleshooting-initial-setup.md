---
title: Problemen tijdens de initiële instelling oplossen
description: In dit onderwerp vindt u informatie over het oplossen van problemen die optreden tijdens de eerste installatie van de integratie van twee keer wegschrijven.
author: RamaKrishnamoorthy
ms.date: 08/10/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 9a70de253eff2a3273be4a31ab32757bb014328f
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061462"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>Problemen tijdens de initiële instelling oplossen

[!include [banner](../../includes/banner.md)]



Dit onderwerp bevat informatie voor het oplossen van problemen met de integratie van Twee keer wegschrijven tussen apps voor financiële en bedrijfsactiviteiten en Dataverse. In dit onderwerp vindt u specifieke informatie over het oplossen van problemen die kunnen optreden tijdens de eerste installatie van de integratie van twee keer wegschrijven.

> [!IMPORTANT]
> In sommige problemen die in dit onderwerp worden beschreven, is mogelijk de rol van systeembeheerder vereist of de referenties van de Microsoft Azure Active Directory-tenantbeheerder (Azure AD). In de sectie voor elk probleem wordt uitgelegd of een specifieke rol of referenties vereist zijn.

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a>U kunt een app voor financiële en bedrijfsactiviteiten niet koppelen aan Dataverse

**Vereiste rol om twee keer wegschrijven in te stellen**: systeembeheerder in apps voor financiële en bedrijfsactiviteiten en Dataverse.

Fouten op de pagina **Koppeling instellen met Dataverse** worden meestal veroorzaakt door problemen met onvolledige instellingen of machtigingen. Controleer of de volledige statuscontrole is geslaagd op de pagina **Koppeling instellen met Dataverse**, zoals wordt weergegeven in de volgende afbeelding. U kunt twee keer wegschrijven niet koppelen, tenzij de hele statuscontrole is geslaagd.

![Geslaagde statuscontrole.](media/health_check.png)

U moet beschikken over referenties als Azure AD-tenantbeheerder om te kunnen koppelen met de Finance and Operations- en Dataverse-omgevingen. Nadat u de omgevingen hebt gekoppeld, kunnen gebruikers zich aanmelden met hun accountreferenties en een bestaande tabeltoewijzing bijwerken.

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>De limiet zoeken voor het aantal rechtspersonen of bedrijven dat kan worden gekoppeld voor twee keer wegschrijven

Mogelijk wordt het volgende foutbericht weergegeven wanneer u toewijzingen probeert in te schakelen:

*Fout met twee keer wegschrijven - Registratie van invoegtoepassing mislukt: [(Kan partitietoewijzing voor project DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260 7f12cb89-1550-42e2-858e-4761fc1443ea niet ophalen. Fout: het maximumaantal toegestane partities is overschreden voor toewijzing van DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)]. Er zijn een of meer fouten opgetreden.*

De huidige limiet voor het koppelen van de omgevingen is ongeveer 40 rechtspersonen. Deze fout treedt op als u toewijzingen probeert in te schakelen en er meer dan 40 rechtspersonen tussen de omgevingen zijn gekoppeld.

## <a name="connection-set-failed-while-linking-environment"></a>Verbindingsset mislukt tijdens het koppelen van omgeving

Tijdens het koppelen van de omgeving voor twee keer wegschrijven mislukt de actie met een foutbericht:

*Verbindingsset opslaan is mislukt. Er is al een artikel met dezelfde sleutel toegevoegd.*

Twee keer wegschrijven biedt geen ondersteuning voor meerdere rechtspersonen/bedrijven met dezelfde naam. Als u bijvoorbeeld twee bedrijven hebt met de naam 'DAT' in Dataverse, wordt dit foutbericht weergegeven.

Als u de blokkering van de klant wilt opheffen, verwijdert u dubbele records uit de tabel **cdm_company** in Dataverse. Verwijder of corrigeer die records ook als de tabel **cdm_company** records bevat waarvan de naam leeg is.

## <a name="error-when-opening-the-dual-write-page-in-finance-and-operations-apps"></a>Fout bij het openen van de pagina Twee keer wegschrijven in apps voor financiële en bedrijfsactiviteiten

Het volgende foutbericht kan worden weergegeven wanneer u een Dataverse-omgeving voor twee keer wegschrijven probeert te koppelen.

*Statuscode van antwoord geeft geen positief resultaat: 404 (niet gevonden).*

Deze fout treedt op wanneer de stap voor toestemming van de app niet is voltooid. U kunt de validatie uitvoeren als er toestemming is gegeven door u met de beheerdersaccount van de tenant aan te melden bij `portal.azure.com` en te controleren of de app van de derde partij met id `33976c19-1db5-4c02-810e-c243db79efde` wordt weergegeven in de lijst met ondernemingstoepassingen van AAD. Als dit niet het geval i s, keert u terug naar de stap voor toestemming, zoals wordt beschreven in het volgende gedeelte.

### <a name="providing-app-consent"></a>App-toestemming verlenen

+ Open de volgende URL met uw beheerdersreferenties.

    `https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent`

+ Selecteer **Accepteren** om toestemming te verlenen. U geeft de toestemming om de app te installeren (met `id=33976c19-1db5-4c02-810e-c243db79efde`) in uw tenant.
+ Deze app is vereist voor Dataverse om te communiceren met apps voor financiële en bedrijfsactiviteiten.

    ![Problemen oplossen tijdens de initiële synchronisatie](media/Initial-sync-setup-troubleshooting-1.png)

> [!NOTE]
> Als dit niet werkt, opent u de URL in de privémodus van Microsoft Edge of in de incognitomodus van Chrome.

## <a name="finance-and-operations-environment-is-not-discoverable"></a>De client voor financiële en bedrijfsactiviteiten is niet te vinden

Mogelijk wordt het volgende foutbericht weergegeven:

*Omgeving van apps voor financiële en bedrijfsactiviteiten \*\*\*.cloudax.dynamics.com is niet te vinden.*

Er zijn twee zaken die een probleem kunnen veroorzaken met een omgeving die niet detecteerbaar is:

+ De gebruiker die voor het aanmelden wordt gebruikt, bevindt zich niet in dezelfde tenant als het Finance and Operations-exemplaar.
+ Er zijn enkele verouderde exemplaren van Finance and Operations die door Microsoft werden gehost en waarbij een probleem optrad bij de detectie. U kunt dit verhelpen door het exemplaar van Finance and Operations bij te werken. De omgeving is bij elke update detecteerbaar.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
