---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources 6 september 2021
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 6 september 2021.
author: marcelbf
ms.date: 09/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 776498b32f8323b1a06f39b518cdc1ae534f9bcc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872147"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-6-2021"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources 6 september 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit artikel worden de functies beschreven die nieuw, gewijzigd of binnenkort beschikbaar zijn in Microsoft Dynamics 365 Human Resources.

Zie [Updateproces](hr-admin-setup-update-process.md) voor meer informatie over het updateproces en de planning.

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/) voor meer informatie over nieuwe functies en de verwachte algemene beschikbaarheidsdatums ervan.

## <a name="in-this-release"></a>In deze versie

Deze versie bevat de volgende nieuwe functies en correcties. Wijzigingen die van toepassing zijn op buildnummer 8.1.4443.

### <a name="new-features"></a>Nieuwe functies

De volgende functie zijn algemeen beschikbaar in deze release.

| Functie | Vrijgaveplan | Documentatie |
|---|---|---|
| Verlof laten beheren door een verzuimmanager | [Verlof laten beheren door een verzuimmanager](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | In deze release werken we de weergave van de werkruimte Verzuimbeheer bij. Zie [Rol Verzuimbeheer configureren](https://go.microsoft.com/fwlink/?linkid=2168107) voor meer informatie. |
| Bijlagenvereiste per verloftype configureren | [Bijlagenvereiste per verloftype configureren](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) | [Verlof- en verzuimtypen configureren](https://go.microsoft.com/fwlink/?linkid=2168108) |
| Verlofeenheden per verloftype configureren | [Verlofeenheden per verloftype configureren](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) | [Verlof- en verzuimtypen configureren](https://go.microsoft.com/fwlink/?linkid=2168215) |

### <a name="bug-fixes"></a>Correcties

Deze versie bevat de volgende correcties.

> [!NOTE]
> Ons doel is om deze informatie zo snel mogelijk bij u te krijgen. Mogelijk wordt dit artikel gewijzigd om correcties op te nemen die in de build zijn gemaakt nadat dit artikel oorspronkelijk werd gepubliceerd.

| Probleemnummer | Probleem | Description |
|---|---|---|
| 610128 | Fout bij het publiceren van gegevens bij het gebruik van HcmDiscussionOverallCommentEntity | Wanneer gegevens worden gepubliceerd vanuit een Excel-werkmap naar de entiteit HcmDiscussionOverralCommentEntity, verschijnt de volgende foutmelding: "Kan de gegevensbronrecord van het type HcmTopicOverrall niet vinden." |
| 589073 | EEO-1-rapport telt "Niet specifiek" en lege waarden bij het veld **Geslacht** als de waarde "Vrouwelijk". | Als niet **Mannelijk** is opgegeven voor het veld **Geslacht**, genereert het rapport EEO-1 een standaardwaarde van **Vrouwelijk**. |
| 589617 | Saldi van Verlofkaart, Beschikbaar voor kopen en Beschikbaar voor verkopen worden niet weergegeven wanneer gebruikersrollen beperkt zijn tot een specifieke rechtspersoon. | Als de gebruiker (werknemerrol) beperkt is tot een specifieke rechtspersoon, worden saldi niet juist weergegeven op de kaart **Verlofsaldi** en in de velden **Beschikbaar voor kopen** en **Beschikbaar voor verkopen**. |
| 604310 | Het tabblad Verzuimbeheer moet worden verborgen wanneer de gebruiker niet is toegewezen aan een verzuimhiërarchie. | Voor een bepaalde rechtspersoon moet het tabblad **Verzuimbeheer** worden verborgen in de self-serviceportal, tenzij de parameter voor meerdere bedrijven is ingeschakeld en er minimaal één verzuimhiërarchie is toegewezen aan de gebruiker. |

## <a name="in-preview"></a>Preview

Van de volgende nieuwe functies kan een voorbeeld worden bekeken. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het in- en uitschakelen van functies.

| Functie | Vrijgaveplan | Documentatie |
|---|---|---|
| Vereenvoudigde integratie van de salarisadministratie inschakelen (API's voor integratie van de salarisadministratie) | [Vereenvoudigde integratie met externe salarisadministrateurs inschakelen](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [API voor integratie van salarisadministratie](hr-admin-integration-payroll-api-introduction.md) |
| Werkgebied voor vergoedingenbeheer | [Werkruimte Vergoedingenbeheer (preview)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Werkgebied voor vergoedingenbeheer](hr-benefits-management-workspace.md) |
| Toestaan dat werknemers kunnen worden gemarkeerd als gereed voor betalen | [Toestaan dat werknemers kunnen worden gemarkeerd als gereed voor betalen](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Gereed voor betaling](/dynamics365/human-resources/hr-compensation-payroll) |
| Aangepaste velden in Geschiktheid |[Ondersteuning voor aangepaste velden in verwerking van geschiktheid](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management) | [Aangepaste velden in verwerking van geschiktheid gebruiken](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules#using-custom-fields-in-eligibility-rules) |

## <a name="coming-soon"></a>Binnenkort beschikbaar

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/) voor een volledige lijst met geplande functies en de bijbehorende geplande versies.

| Functie | Gegevens |
|---|---|
| Platformupdate 10.0.21 (45) | Implementatie van platformupdate 10.0.21 is gepland voor de volgende servicerelease op 4 oktober 2021. Zie voor meer informatie [Platformupdates voor versie 10.0.21 van apps voor financiële en bedrijfsactiviteiten (oktober 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |
| Vergoedingenoverzicht | Vergoedingenoverzicht voor het weergeven van de huidige vergoedingskeuzes van een werknemer. Zie [vergoedingenverklaring](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/benefits-summary-statement) in het document releasewave voor meer informatie. |

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van Dynamics 365 Human Resources 2021 release wave 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
