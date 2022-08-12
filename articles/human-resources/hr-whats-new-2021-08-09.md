---
title: Nieuwe of gewijzigde functies in Dynamics 365 Human Resources, 9 augustus 2021
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 9 augustus 2021.
author: marcelbf
ms.date: 08/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-08-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 58926e5a6c1476db84fa41945dc92196eb24f4bf
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068449"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-9-2021"></a>Nieuwe of gewijzigde functies in Dynamics 365 Human Resources, 9 augustus 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit artikel worden de functies beschreven die nieuw, gewijzigd of binnenkort beschikbaar zijn in Microsoft Dynamics 365 Human Resources.

Zie [Updateproces](hr-admin-setup-update-process.md) voor meer informatie over het updateproces en de planning.

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/) voor meer informatie over nieuwe functies en de verwachte algemene beschikbaarheidsdatums ervan.

## <a name="in-this-release"></a>In deze versie

Deze versie bevat de volgende nieuwe functies en correcties. Wijzigingen die van toepassing zijn op buildnummer 8.1.4393.

### <a name="bug-fixes"></a>Correcties

Deze versie bevat de volgende correcties.

> [!NOTE]
> Ons doel is om deze informatie zo snel mogelijk bij u te krijgen. Mogelijk wordt dit artikel gewijzigd om correcties op te nemen die in de build zijn gemaakt nadat dit artikel oorspronkelijk werd gepubliceerd.

| Probleemnummer | Probleem | Description |
| --- | --- | --- |
| 558385 | De standaardbegunstigde is niet geselecteerd wanneer de optie **Begunstigden automatisch selecteren** is ingeschakeld voor standaardbegunstigden. | Dit probleem is nu opgelost. Er worden automatisch meerdere standaardbegunstigden geselecteerd in geschikte abonnementen wanneer de optie **Begunstigden automatisch selecteren** op de pagina **Gedeelde Human Resources-parameters** wordt ingeschakeld. |
| 589617 | Op de pagina **Verlof** zijn de saldi voor **Beschikbaar voor kopen** en **Beschikbaar voor verkopen** leeg als de toegang tot een specifiek bedrijf is beperkt. | Dit probleem is nu opgelost. Op de pagina **Verlof** worden de juiste saldi voor **Beschikbaar voor kopen** en **Beschikbaar voor verkopen** weergegeven als de gebruiker tot een specifiek bedrijf is beperkt. |

## <a name="in-preview"></a>Preview

Van de volgende nieuwe functies kan een voorbeeld worden bekeken. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het in- en uitschakelen van functies.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Werkgebied voor vergoedingenbeheer | [Werkruimte Vergoedingenbeheer (preview)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Werkgebied voor vergoedingenbeheer](hr-benefits-management-workspace.md) |
| Vereenvoudigde integratie van de salarisadministratie inschakelen (API's voor integratie van de salarisadministratie) | [Vereenvoudigde integratie met externe salarisadministrateurs inschakelen](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [API voor integratie van salarisadministratie](hr-admin-integration-payroll-api-introduction.md)|
| Verlof laten beheren door een verzuimmanager | [Verlof laten beheren door een verzuimmanager](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | In deze release werken we de weergave van de werkruimte Verzuimbeheer bij. Zie [Rol Verzuimbeheer configureren](https://go.microsoft.com/fwlink/?linkid=2168107) voor meer informatie. |
| Bijlagenvereiste per verloftype configureren | [Bijlagenvereiste per verloftype configureren](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Verlof- en verzuimtypen configureren](https://go.microsoft.com/fwlink/?linkid=2168108)|
| Verlofeenheden per verloftype configureren | [Verlofeenheden per verloftype configureren](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Verlof- en verzuimtypen configureren](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Toestaan dat werknemers kunnen worden gemarkeerd als gereed voor betalen | [Toestaan dat werknemers kunnen worden gemarkeerd als gereed voor betalen](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Gereed voor betaling](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Binnenkort beschikbaar

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/) voor een volledige lijst met geplande functies en de bijbehorende geplande versies.

| Functie | Gegevens |
| --- | --- |
| Platformupdate 10.0.21 (45) | Implementatie van platformupdate 10.0.21 is gepland voor de volgende servicerelease op 4 oktober 2021. Zie voor meer informatie [Platformupdates voor versie 10.0.21 van apps voor financiën en bedrijfsactiviteiten (oktober 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van Dynamics 365 Human Resources 2021 release wave 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

