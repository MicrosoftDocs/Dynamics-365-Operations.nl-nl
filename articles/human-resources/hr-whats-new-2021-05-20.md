---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources 20 mei 2021
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 20 mei 2021.
author: marcelbf
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-05-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4519e90e19d0652f855999d1a73ca64777b53b53465d6065987afc1cf2494187
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731932"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-20-2021"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources 20 mei 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn of die binnenkort worden vrijgegeven in Dynamics 365 Human Resources.

Zie [Updateproces](hr-admin-setup-update-process.md) voor meer informatie over het updateproces en de planning.

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) voor meer informatie over nieuwe functies en de verwachte algemene beschikbaarheidsdatums ervan.

## <a name="in-this-release"></a>In deze versie

Deze versie bevat de volgende nieuwe functies en correcties. Wijzigingen die van toepassing zijn op buildnummer 8.1.4189.

### <a name="new-features"></a>Nieuwe functies

De volgende functie zijn algemeen beschikbaar in deze release.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Platformupdate 10.0.18 (42) | -- | [Platformupdates voor versie 10.0.18 van Finance and Operations-apps (mei 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18) |
| De Human Resources-app voor Microsoft Teams ondersteunt nu definities voor halve dagen en de mogelijkheid van gesplitste dagen | -- | [Verlofaanvragen beheren in Teams](/dynamics365/human-resources/hr-teams-leave-app#create-a-new-request) |

### <a name="bug-fixes"></a>Correcties

Deze versie bevat de volgende correcties.

> [!NOTE]
> Ons doel is om deze informatie zo snel mogelijk bij u te krijgen. Mogelijk wordt dit onderwerp gewijzigd om correcties op te nemen die in de build zijn gemaakt nadat dit onderwerp oorspronkelijk werd gepubliceerd.

| Probleemnummer | Probleem |  Beschrijving |
| --- | --- | --- |
| 583776 | Een fout met dubbele records wordt veroorzaakt door massa-inschrijvingen van werknemers voor verlofplannen | Dit probleem is opgelost in de laatste release en massa-inschrijvingen voor verlofplannen worden met succes verwerkt. |
| 582263 | Kan verwerking van levensgebeurtenissen niet voor alle werknemers tegelijk uitvoeren | Als het veld **Werknemer** leeg is gelaten voor de verwerking van levensgebeurtenissen, worden alle werknemers verwerkt. |
| 558383 | Primaire begunstigde niet gemarkeerd als 100% als er geen standaardbegunstigde is geselecteerd | Het probleem is opgelost zodat de gebruiker alleen de schakeloptie voor primaire begunstigde hoeft te selecteren.|
| 509404 | Analyses van personeelsbezetting per afdeling waarbij geen rekening wordt gehouden met de verplaatsing van werknemers tussen afdelingen |De analyses zijn bijgewerkt zodat overplaatsingen van werknemers tussen afdelingen worden opgenomen|
| 579420 | De functie Kolommen in rasters blokkeren is nog niet beschikbaar | De functie **Kolommen in rasters blokkeren**, die niet beschikbaar is in Human Resources, werd als beschikbaar in Functiebeheer weergegeven. De functie is verwijderd uit de lijst met functies die kunnen worden ingeschakeld. |

## <a name="in-preview"></a>Preview

Van de volgende nieuwe functies kan een voorbeeld worden bekeken. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het in- en uitschakelen van functies.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Ondersteuning voor aangepaste velden in geschiktheidsregels in Vergoedingenbeheer | [Ondersteuning voor aangepaste velden voor verwerking van geschiktheid](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |[Geschiktheidsregels configureren](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules) |
| Werkgebied voor vergoedingenbeheer | [Werkruimte Vergoedingenbeheer (preview)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Werkgebied voor vergoedingenbeheer](hr-benefits-management-workspace.md) |
| Verbeteringen voor werken in de workflows voor verlof en verzuim | [Verbeteringen voor werken in de workflows voor verlof en verzuim](https://go.microsoft.com/fwlink/?linkid=2147528) | [Verlof aanvragen](hr-employee-self-service-request-time-off.md)|
| Vereenvoudigde integratie van de salarisadministratie inschakelen (API's voor integratie van de salarisadministratie) | [Vereenvoudigde integratie met externe salarisadministrateurs inschakelen](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [API voor integratie van salarisadministratie](hr-admin-integration-payroll-api-introduction.md)|
| Controleren van toerekeningstransacties voor verlof | - | [Controleren van toerekeningstransacties voor verlof](hr-leave-and-absence-accrue.md)|

## <a name="coming-soon"></a>Binnenkort beschikbaar

| Functie | Gegevens |
| --- | --- |
|  Verlof laten beheren door een verzuimmanager | [Verlof laten beheren door een verzuimmanager](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) |

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) voor een volledige lijst met geplande functies en de bijbehorende geplande versies.

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van Dynamics 365 Human Resources 2021 release wave 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
