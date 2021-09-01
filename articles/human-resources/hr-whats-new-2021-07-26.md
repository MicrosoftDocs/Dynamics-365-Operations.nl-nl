---
title: Nieuwe of gewijzigde functies in Dynamics 365 Human Resources 26 juli 2021
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 26 juli 2021.
author: marcelbf
ms.date: 07/12/2021
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
ms.search.validFrom: 2021-07-26
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 810511c42cd690579d8c8b6ebcc17b0cf7fcb9eb2b999822dc2226fabd127cc6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771510"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-26-2021"></a>Nieuwe of gewijzigde functies in Dynamics 365 Human Resources 26 juli 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn of die binnenkort worden vrijgegeven in Dynamics 365 Human Resources.

Zie [Updateproces](hr-admin-setup-update-process.md) voor meer informatie over het updateproces en de planning.

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/) voor meer informatie over nieuwe functies en de verwachte algemene beschikbaarheidsdatums ervan.

## <a name="in-this-release"></a>In deze versie

Deze versie bevat de volgende nieuwe functies en correcties. Wijzigingen die van toepassing zijn op buildnummer 8.1.4384.

### <a name="new-features"></a>Nieuwe functies

De volgende functie zijn algemeen beschikbaar in deze release.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Platformupdate 10.0.20 | -- | [Platformupdates voor versie 10.0.20 van Finance and Operations-apps (augustus 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20) |

### <a name="bug-fixes"></a>Correcties

Deze versie bevat de volgende correcties.

> [!NOTE]
> Ons doel is om deze informatie zo snel mogelijk bij u te krijgen. Mogelijk wordt dit onderwerp gewijzigd om correcties op te nemen die in de build zijn gemaakt nadat dit onderwerp oorspronkelijk werd gepubliceerd.

| Probleemnummer | Probleem |  Beschrijving |
| --- | --- | --- |
| 600422 | Validatie van salarisadres is niet mogelijk voor Gereed om te betalen. | Validatie is bijgewerkt, zodat slechts één adres van het type 'Salarislocatie' en slechts één adres van het type 'Salariswerklocatie' nodig zijn. |
| 601226 | Probleem met gegevensintegratie: het exportproject voor salarisintegratie kan geen volledige push uitvoeren | De salarisintegratie met Ceridian DayForce heeft een incrementele push gedaan in plaats van een volledige push. Ceridian moet altijd volledig vernieuwen. Dit probleem is nu verholpen, de entiteiten in het gegevensexportproject zullen niet langer wisselen naar incrementele push. |
| 602272 | Tegels die zijn toegevoegd aan de werkruimte Werknemerselfservice ontbreken nu en het is niet langer mogelijk om er tegels aan toe te voegen | Het probleem met de personalisatie van de werknemerselfservice is opgelost. Er kunnen nieuwe tegels aan de weergave worden toegevoegd en bestaande personalisaties zijn zichtbaar voor gebruikers |
| 600711 | Selectieveld halve dagdefinitie ingeschakeld voor verlofaanvragen voor volledige dag | Dit probleem is nu opgelost en het veld voor de definitie van een halve dag wordt alleen ingeschakeld als de werknemer een verloftype selecteert waarbij de definitie van een halve dag is ingeschakeld en een halve dag als hoeveelheid is geselecteerd |
| 602208 | Toerekeningstariefeenheden die uren in plaats van dagen weergeven | Dit probleem is nu opgelost. In het formulier **Verlof** wordt de juiste verlofeenheid (uren of dagen) weergegeven voor de kolom **Toerekeningstarief**. |

## <a name="in-preview"></a>Preview

Van de volgende nieuwe functies kan een voorbeeld worden bekeken. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het in- en uitschakelen van functies.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Werkgebied voor vergoedingenbeheer | [Werkruimte Vergoedingenbeheer (preview)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Werkgebied voor vergoedingenbeheer](hr-benefits-management-workspace.md) |
| Vereenvoudigde integratie van de salarisadministratie inschakelen (API's voor integratie van de salarisadministratie) | [Vereenvoudigde integratie met externe salarisadministrateurs inschakelen](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [API voor integratie van salarisadministratie](hr-admin-integration-payroll-api-introduction.md)|
|  Verlof laten beheren door een verzuimmanager | [Verlof laten beheren door een verzuimmanager](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | Met deze release werken we de weergave van de werkruimte Verzuimbeheer bij. Zie [Rol Verzuimbeheer configureren](https://go.microsoft.com/fwlink/?linkid=2168107) voor meer informatie.|
|  Bijlagenvereiste per verloftype configureren | [Bijlagenvereiste per verloftype configureren](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Verlof- en verzuimtypen configureren](https://go.microsoft.com/fwlink/?linkid=2168108)|
|  Verlofeenheden per verloftype configureren | [Verlofeenheden per verloftype configureren](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Verlof- en verzuimtypen configureren](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Toestaan dat werknemers kunnen worden gemarkeerd als gereed voor betalen | [Toestaan dat werknemers kunnen worden gemarkeerd als gereed voor betalen](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Gereed voor betaling](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Binnenkort beschikbaar

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/) voor een volledige lijst met geplande functies en de bijbehorende geplande versies.

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van Dynamics 365 Human Resources 2021 release wave 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
