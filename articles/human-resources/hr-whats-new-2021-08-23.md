---
title: Nieuwe of gewijzigde functies in Dynamics 365 Human Resources, 23 augustus 2021
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 23 augustus 2021.
author: marcelbf
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-08-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a6c92167a9b67c3be1cdad18293e8ab6d2ba03d4
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069841"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-23-2021"></a>Nieuwe of gewijzigde functies in Dynamics 365 Human Resources, 23 augustus 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit artikel worden de functies beschreven die nieuw, gewijzigd of binnenkort beschikbaar zijn in Microsoft Dynamics 365 Human Resources.

Zie [Updateproces](hr-admin-setup-update-process.md) voor meer informatie over het updateproces en de planning.

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/) voor meer informatie over nieuwe functies en de verwachte algemene beschikbaarheidsdatums ervan.

## <a name="in-this-release"></a>In deze versie

Deze versie bevat de volgende nieuwe functies en correcties. Wijzigingen die van toepassing zijn op buildnummer 8.1.4419.

### <a name="bug-fixes"></a>Correcties

Deze versie bevat de volgende correcties.

> [!NOTE]
> Ons doel is om deze informatie zo snel mogelijk bij u te krijgen. Mogelijk wordt dit artikel gewijzigd om correcties op te nemen die in de build zijn gemaakt nadat dit artikel oorspronkelijk werd gepubliceerd.

| Probleemnummer | Probleem | Description |
| --- | --- | --- |
| 594066 | Contactgegevens kunnen niet worden verwijderd | Wanneer u een andere record voor contactinformatie voor een werknemer selecteert dan de geselecteerde record, wordt deze verwijderd. |
| 611339 | Wanneer u een personalisatie toevoegt, negeert de bankrekening het filter en wordt de eerste record opgehaald | Als u een personalisatie toevoegt, wordt er door de bankrekeninglijst een personalisatiequery uitgevoerd nadat de gegevensbronquery is uitgevoerd, wat tot gevolg heeft dat de bovenste record wordt opgehaald, ongeacht de werknemer voor wie de gegevens worden weergegeven. |
| 591806 | Taken voor onboarding van vervaldatums worden onjuist berekend | Datums worden onjuist berekend wanneer aan de volgende voorwaarden wordt voldaan: voor de controlelijsten die worden aangemaakt, wordt gebruikgemaakt van een kalender met een uitgebreid tijdbereik (bijvoorbeeld van 2005 tot 2050) en voor de gebruikersvoorkeuren wordt een andere tijdzone gebruikt dan Centrale standaardtijd. |   
| 592749 | Verlofsaldo is onjuist in **Selfservice werknemer** | Als de werknemer een dienstverband heeft bij meer dan één rechtspersoon en verlofweergave voor meerdere bedrijven is ingeschakeld, is het verlofsaldo mogelijk onjuist. |
| 603133 | Onverwachte waarschuwing bij het aanvragen van vrije tijd | Wanneer u vrije tijd aanvraagt en het veld **Halve dag** invult voordat het veld **Hoeveelheid** is ingevuld, veroorzaakt dit een onverwachte waarschuwing. |
| 606546 | Veld selecteren niet zichbaar in Goedgekeurde vrije tijd | Het selectievakje om meerdere goedgekeurde verlofaanvragen te selecteren was niet zichtbaar. |
| 597059 | Werknemer niet zichtbaar in **Verlof- en verzuimkalender bedrijf** | Een werknemer is niet zichtbaar in de **Verlof- en verzuimkalender bedrijf** als het toegepaste datumbereik een dag omvat waarvoor een verlofaanvraag is geweigerd. |


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

