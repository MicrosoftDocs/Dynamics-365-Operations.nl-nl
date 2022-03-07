---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources 2 december 2020
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 2 december 2020.
author: marcelbf
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6e02586ad3e6b4428f2ba826851db6ebc3172bdf1760b483032f5159e7864a81
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782654"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-december-2-2020"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources 2 december 2020

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn of die binnenkort worden vrijgegeven in Dynamics 365 Human Resources.

Zie [Updateproces](hr-admin-setup-update-process.md) voor meer informatie over het updateproces en de planning.

Zie [Overzicht van Dynamics 365 Human Resources 2020 release wave 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/) voor meer informatie over nieuwe functies en de verwachte algemene beschikbaarheidsdatums ervan.

## <a name="in-this-release"></a>In deze versie

Deze versie bevat de volgende nieuwe functies en correcties. Wijzigingen die van toepassing zijn op buildnummer 8.1.3788.

### <a name="new-features"></a>Nieuwe functies

De volgende functie zijn algemeen beschikbaar in deze release.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Managers kunnen wervingsaanvragen voor functies indienen | [Managers kunnen een wervingsaanvraag voor open functies indienen](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Een wervingsaanvraag toevoegen](./hr-personnel-recruit.md#add-a-recruiting-request) |
| Uitgebreid kandidaatprofiel in Personeelsbeheer | [Uitgebreid kandidaatprofiel in Personeelsbeheer](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Een kandidaatprofiel toevoegen of bewerken](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| Vereenvoudigde integraties met wervingsproviders inschakelen | [Vereenvoudigde integraties met wervingsproviders inschakelen](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Kandidaten werven](./hr-personnel-recruit.md) |
| Aangepaste koppelingen in Selfservice manager | [Aangepaste koppelingen in Selfservice manager](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [Aangepaste koppelingen in Selfservice manager](./hr-employee-manager-self-service-custom-links.md) |


### <a name="bug-fixes"></a>Correcties

Deze versie bevat de volgende correcties.

> [!NOTE]
> Ons doel is om deze informatie zo snel mogelijk bij u te krijgen. Mogelijk wordt dit onderwerp gewijzigd om correcties op te nemen die in de build zijn gemaakt nadat dit onderwerp oorspronkelijk werd gepubliceerd.

| Probleemnummer | Uitgeven | Beschrijving |
| --- | --- | --- |
| 514087 | BenefitEligibilityProcessResult moet de datum/tijd bevatten die bij de verwerking is gebruikt. | BenefitEligibity-verwerkingsresultaat bevat nu de datum/tijd voor de laatste verwerking, die eerder ontbrak. |
| 526903 | De inschrijving van vergoedingen is mislukt voor programma's met afhankelijken wanneer **Begunstigden automatisch selecteren** is ingeschakeld in **Gedeelde Human Resources-parameters**. | Het probleem is opgelost waarbij de inschrijving van vergoedingen is mislukt voor programma's met afhankelijken wanneer de optie **Begunstigden automatisch selecteren** is ingeschakeld voor standaard begunstigden. |
| 521922 | De parameter **Afwezigheid tonen zonder details** geeft details weer over verlofaanvragen in de verzuimkalender van het team. | Het type verlof, het kleurtype verlof en de details worden per dag weergegeven in de verzuimkalender van het team wanneer **Afwezigheid tonen zonder details** is ingesteld op **Ja** in de **Verlof- en verzuimparameters**. Dit is opgelost en nu wordt het type verlof niet weergegeven en wordt de standaardkleur voor verlof (donkerblauw) gebruikt voor alle types verlof in de verzuimkalender van het team. |
| 527316 | Titelwijzigingen voor vacatures, functies en werknemersmeldingen worden niet gesynchroniseerd. | Er is eerder een titelrelatie toegevoegd aan de entiteiten Vacature, Functie en Werknemer. De synchronisatie voor deze relatie werkt voor de synchronisatie van Human Resources naar Dataverse, maar niet voor meldingen van Dataverse. Dit is opgelost. |
| 512275 | Verwijder de kleuropties van **Verlof- en verzuimparameters**. | Nu de kleuren voor het verloftype zijn bepaald, zijn de kleuropties niet langer nodig in de **Verlof- en verzuimparameters**. Daarom zijn deze verwijderd. |
| 437112 | Misleidend foutbericht tijdens het toewijzen van werknemersfuncties. | Het foutbericht is bijgewerkt bij het aannemen van een werknemer en bij het toewijzen van de werknemer aan een niet-actieve functie. Bijgewerkt bericht **De opgegeven functie is niet actief vanaf de begindatum van de aanstelling. Controleer de duur van deze functie.** |
| 527816 | Prestatieproblemen met de pagina **Verlof**. | De prestaties zijn verbeterd op de pagina **Verlof**. |
| 523158 | BenefitPeriodMigrationUpgrade en BenefitPlanMigrationUpgrade zijn niet uitgevoerd. | Vaste problemen met migratievacatures voor vergoedingen die zijn gerelateerd aan een **Periode** en **Programma** worden niet correct uitgevoerd. |

## <a name="in-preview"></a>Preview

Van de volgende nieuwe functies kan een voorbeeld worden bekeken. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het in- en uitschakelen van functies.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Human Resources-app in Microsoft Teams | [Verlof en verzuim van werknemers in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Human Resources-app in Teams](./hr-admin-teams-leave-app.md)<br>[Verlofaanvragen beheren in Teams](hr-teams-leave-app.md) |
| Uitgebreide aanvragen en goedkeuringen voor werkstromen | [Verbeteringen in de ervaring van werkstromen voor organisatie en personeelsbeheer](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Configuratieoptie om de lijst Aan mij toegewezen werkitems te positioneren](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Integratie met LinkedIn Talent Hub | [Integratie met LinkedIn Talent Hub](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [Integreren met LinkedIn Talent Hub](./hr-admin-integration-linkedin.md) |
|Bedrijfsweergave van verlof voor managers | [Bedrijfsweergave van werknemersverlof voor managers](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Parameters voor verlof en verzuim configureren](./hr-leave-and-absence-parameters.md) |
|Meer inzicht in verlofsaldi bieden| [Meer inzicht in verlofsaldi bieden](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [Werknemerverlof beheren](./hr-leave-and-absence-manage-employee-leave.md) |
| Managers kunnen wervingsaanvragen voor functies indienen | [Managers kunnen een wervingsaanvraag voor open functies indienen](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Een wervingsaanvraag toevoegen](./hr-personnel-recruit.md#add-a-recruiting-request) |
| Uitgebreid kandidaatprofiel in Personeelsbeheer | [Uitgebreid kandidaatprofiel in Personeelsbeheer](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Een kandidaatprofiel toevoegen of bewerken](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| Vereenvoudigde integraties met wervingsproviders inschakelen | [Vereenvoudigde integraties met wervingsproviders inschakelen](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Kandidaten werven](./hr-personnel-recruit.md) |

## <a name="coming-soon"></a>Binnenkort beschikbaar

Zie [Overzicht van Dynamics 365 Human Resources 2020 release wave 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/) voor een volledige lijst met geplande functies en de bijbehorende geplande versies.

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van Dynamics 365 Human Resources 2020 release wave 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]