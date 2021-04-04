---
title: Problemen tijdens de initiële instelling oplossen
description: In dit onderwerp vindt u informatie over het oplossen van problemen die optreden tijdens de eerste installatie van de integratie van twee keer wegschrijven.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
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
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f6ff9a304de8a94b86e6866d6d2cb65fbfdfb02f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561173"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>Problemen tijdens de initiële instelling oplossen

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Dit onderwerp bevat informatie voor het oplossen van problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Dataverse. In dit onderwerp vindt u specifieke informatie over het oplossen van problemen die kunnen optreden tijdens de eerste installatie van de integratie van twee keer wegschrijven.

> [!IMPORTANT]
> In sommige problemen die in dit onderwerp worden beschreven, is mogelijk de rol van systeembeheerder vereist of de referenties van de Microsoft Azure Active Directory-tenantbeheerder (Azure AD). In de sectie voor elk probleem wordt uitgelegd of een specifieke rol of referenties vereist zijn.

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a>U kunt een Finance and Operations-app niet koppelen met Dataverse

**Vereiste rol om twee keer wegschrijven in te stellen:** systeembeheerder in Finance and Operations-apps en Dataverse.

Fouten op de pagina **Koppeling instellen met Dataverse** worden meestal veroorzaakt door problemen met onvolledige instellingen of machtigingen. Controleer of de volledige statuscontrole is geslaagd op de pagina **Koppeling instellen met Dataverse**, zoals wordt weergegeven in de volgende afbeelding. U kunt twee keer wegschrijven niet koppelen, tenzij de hele statuscontrole is geslaagd.

![Geslaagde statuscontrole](media/health_check.png)

U moet beschikken over referenties als Azure AD-tenantbeheerder om te kunnen koppelen met de Finance and Operations-en Dataverse-omgevingen. Nadat u de omgevingen hebt gekoppeld, kunnen gebruikers zich aanmelden met hun accountreferenties en een bestaande tabeltoewijzing bijwerken.

## <a name="error-when-you-open-the-link-to-dataverse-page"></a>Fout wanneer u de pagina Koppeling met Dataverse opent

**Vereiste referenties om het probleem op te lossen:** Azure AD-tenantbeheerder

Mogelijk wordt het volgende foutbericht weergegeven wanneer u de pagina **Koppelen met Dataverse** opent in en Finance and Operations-app:

*Statuscode van antwoord geeft geen positief resultaat: 404 (niet gevonden).*

Deze fout treedt op wanneer de goedkeuringsstap niet is voltooid. Als u wilt controleren of de goedkeuringsstap is voltooid, meldt u zich aan bij portal.Azure.com met behulp van het Azure AD-tenantbeheerdersaccount en controleert u of de app van de andere leverancier met de id **33976c19-1db5-4c02-810e-c243db79efde** verschijnt in de lijst met Azure AD-**ondernemingstoepassingen**. Als dat niet zo is, moet u de app goedkeuren.

Voer de volgende stappen uit om een app goed te keuren.

1. Open de volgende URL met uw beheerdersreferenties. U moet om toestemming worden gevraagd.

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. Selecteer **Accepteren** om aan te geven dat u uw toestemming geeft om de app met de id **33976c19-1db5-4c02-810e-c243db79efde** in uw tenant te installeren.

    > [!TIP]
    > Deze app is vereist om de apps Dataverse en Finance and Operations te koppelen. Als u problemen ondervindt met deze stap, opent u de browser in de modus Incognito (in Google Chrome) of InPrivate-modus (in Microsoft Edge).

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a>Controleren of bedrijfsgegevens en teams voor twee keer wegschrijven op de juiste wijze zijn ingesteld tijdens het koppelen

Om er zeker van te zijn dat twee keer wegschrijven goed werkt, worden de bedrijven die u tijdens de configuratie selecteert, in de Dataverse-omgeving gemaakt. Standaard zijn deze bedrijven alleen-lezen en wordt de eigenschap **IsDualWriteEnable** ingesteld op **True**. Daarnaast worden de standaard bedrijfseenheid die eigenaar is en het team gemaakt en wordt de bedrijfsnaam opgenomen. Voordat u de toewijzingen inschakelt, controleert u of de standaard eigenaar van het team is opgegeven. Voer de volgende stappen uit om de tabel **Bedrijven (CDM\_Company)** te zoeken.

1. Selecteer in de modelgestuurde app in Dynamics 365 het filter in de rechterbovenhoek.
2. Selecteer **Bedrijf** in de vervolgkeuzelijst.
3. Selecteer **Uitvoeren** om de resultaten weer te geven.
4. Selecteer het bedrijf dat was gekoppeld tijdens het configureren van twee keer wegschrijven.
5. Controleer of de kolom **Standaardeigenaarsteam** een waarde heeft. In de volgende afbeelding is de kolom **Standaardeigenaarsteam** ingesteld op **USMF twee keer wegschrijven**.

    ![Het standaardeigenaarsteam controleren](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>De limiet zoeken voor het aantal rechtspersonen of bedrijven dat kan worden gekoppeld voor twee keer wegschrijven

Mogelijk wordt het volgende foutbericht weergegeven wanneer u toewijzingen probeert in te schakelen:

*Fout met twee keer wegschrijven - Registratie van invoegtoepassing mislukt: \[(Kan partitietoewijzing voor project DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea niet ophalen. Fout: de maximum toegestane partities overschreden voor toewijzing DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], Er zijn een of meer fouten opgetreden.*

De huidige limiet voor het koppelen van de omgevingen is ongeveer 40 rechtspersonen. Deze fout treedt op als u toewijzingen probeert in te schakelen en er meer dan 40 rechtspersonen tussen de omgevingen zijn gekoppeld.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]