---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources 3 mei 2021
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 3 mei 2021.
author: marcelbf
ms.date: 05/03/2021
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
ms.search.validFrom: 2021-05-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4fd0d0d39d19634498f9313aeda4143f9ec81e8f
ms.sourcegitcommit: f3c28f57d997e824a64485d9a4ce8f198e3bcf23
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059624"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-3-2021"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources 3 mei 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn of die binnenkort worden vrijgegeven in Dynamics 365 Human Resources.

Zie [Updateproces](hr-admin-setup-update-process.md) voor meer informatie over het updateproces en de planning.

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) voor meer informatie over nieuwe functies en de verwachte algemene beschikbaarheidsdatums ervan.

## <a name="in-this-release"></a>In deze versie

Deze versie bevat de volgende nieuwe functies en correcties. Wijzigingen die van toepassing zijn op buildnummer 8.1.4140.

### <a name="new-features"></a>Nieuwe functies

De volgende functie zijn algemeen beschikbaar in deze release.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Informatiebalk toevoegen bij het maken van levensgebeurtenissen. | - | Wanneer u een levensgebeurtenis maakt, wordt op de informatiebalk een bericht weergegeven waarin het type levensgebeurtenis wordt aangegeven dat is gemaakt.

### <a name="bug-fixes"></a>Correcties

Deze versie bevat de volgende correcties.

> [!NOTE]
> Ons doel is om deze informatie zo snel mogelijk bij u te krijgen. Mogelijk wordt dit onderwerp gewijzigd om correcties op te nemen die in de build zijn gemaakt nadat dit onderwerp oorspronkelijk werd gepubliceerd.

| Probleemnummer | Uitgeven |  Beschrijving |
| --- | --- | --- |
| 559312 |  Het niveau wordt niet weergegeven wanneer een vast compensatieplan voor een werknemer wordt gemaakt. |  Als de tijdzone van de gebruiker en de tijdzone van het bedrijf niet overeenkomen, kan het compensatieniveau voor de taak niet worden gelezen. De query is bijgewerkt om op basis van de UTC-tijd op te halen. |
| 573676  | Kan geen nieuwe periode toevoegen in het formulier **Vergoedingenplan**. | Het formulier is bijgewerkt, zodat de knop **Nieuw** is ingeschakeld onder het sneltabblad **Periode** in **Vergoedingsplannen**. |

## <a name="in-preview"></a>Preview

Van de volgende nieuwe functies kan een voorbeeld worden bekeken. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het in- en uitschakelen van functies.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Werkgebied voor vergoedingenbeheer | [Werkruimte Vergoedingenbeheer (preview)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Werkgebied voor vergoedingenbeheer](hr-benefits-management-workspace.md) |
| Verbeteringen voor werken in de workflows voor verlof en verzuim | [Verbeteringen voor werken in de workflows voor verlof en verzuim](https://go.microsoft.com/fwlink/?linkid=2147528) | [Verlof aanvragen](hr-employee-self-service-request-time-off.md)|
| Vereenvoudigde integratie van de salarisadministratie inschakelen (API's voor integratie van de salarisadministratie) | [Vereenvoudigde integratie met externe salarisadministrateurs inschakelen](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [API voor integratie van salarisadministratie](hr-admin-integration-payroll-api-introduction.md)|
| Controleren van toerekeningstransacties voor verlof | - | [Controleren van toerekeningstransacties voor verlof](hr-leave-and-absence-accrue.md#preview-leave-accrual-transaction-auditing)|

## <a name="coming-soon"></a>Binnenkort beschikbaar

| Functie | Gegevens |
| --- | --- |
| Platformupdate 10.0.18 (42) | Platformupdate 10.0.18 is gepland voor de uitrol met de volgende servicerelease op 17 mei 2021. Zie [Platformupdates voor versie 10.0.18 van Finance and Operations-apps (mei 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18) voor meer informatie. |
| Ondersteuning voor aangepaste velden in geschiktheidsregels in Vergoedingenbeheer  | [Ondersteuning voor aangepaste velden voor verwerking van geschiktheid](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) voor een volledige lijst met geplande functies en de bijbehorende geplande versies.

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van Dynamics 365 Human Resources 2021 release wave 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
