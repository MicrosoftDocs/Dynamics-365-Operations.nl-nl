---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources 22 februari 2021
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 22 februari 2021.
author: marcelbf
ms.date: 02/22/2021
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
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cac3c188e372521a1f63833cd0032f0e9ff7ebe3
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052380"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-22-2021"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources 22 februari 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn of die binnenkort worden vrijgegeven in Dynamics 365 Human Resources.

Zie [Updateproces](hr-admin-setup-update-process.md) voor meer informatie over het updateproces en de planning.

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) voor meer informatie over nieuwe functies en de verwachte algemene beschikbaarheidsdatums ervan.

## <a name="in-this-release"></a>In deze versie

Deze versie bevat de volgende nieuwe functies en correcties. Wijzigingen die van toepassing zijn op buildnummer 8.1.3988.

### <a name="new-features"></a>Nieuwe functies

De volgende functie zijn algemeen beschikbaar in deze release.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Dynamics 365 Human Resources-app voor Microsoft Teams | [Verlof en verzuim van werknemers in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Human Resources-app in Teams](./hr-admin-teams-leave-app.md)<br>[Verlofaanvragen beheren in Teams](hr-teams-leave-app.md) |

### <a name="bug-fixes"></a>Correcties

Deze versie bevat de volgende correcties.

> [!NOTE]
> Ons doel is om deze informatie zo snel mogelijk bij u te krijgen. Mogelijk wordt dit onderwerp gewijzigd om correcties op te nemen die in de build zijn gemaakt nadat dit onderwerp oorspronkelijk werd gepubliceerd.

| Probleemnummer | Uitgeven |  Beschrijving |
| --- | --- | --- |
| 529994 | Het wijzigen van het veld **Bekend als** in het formulier **Werknemer** activeert geen Dataverse-update | Een probleem oplossen waarbij Dataverse niet wordt bijgewerkt als het veld **Bekend als** op het formulier **Werknemer** wordt bijgewerkt. |
| 532651 | PBI-rapport compensatieanalyse gebruikt geen valutaconversie bij het berekenen van meetgegevens voor alle bedrijven | Een probleem opgelost waarbij het PBI-rapport voor compensatieanalyses niet correct valutaomrekeningen heeft gedaan. |
| 552226 | Bij het verwerken van levensgebeurtenissen worden plannen meerdere keren gesloten en opnieuw geopend voor één levensgebeurtenis  | Een probleem opgelost waarbij een werknemer in meerdere rechtspersonen is en een levensgebeurtenis zich voordoet, een levensgebeurtenisrecord wordt gegenereerd voor elke rechtspersoon waarin de werknemer zich in bevindt. Bij het verwerken van levensgebeurtenissen moet de te verwerken rechtspersoon worden geselecteerd. De verwerkingslogica beperkt zich echter niet tot deze rechtspersoon. In plaats daarvan verwerkt het de plannen voor alle rechtspersonen en worden de plannen in de geselecteerde rechtspersoon gesloten en opnieuw geopend. Dit leidt ertoe dat een levensgebeurtenis meerdere keren wordt verwerkt in dezelfde rechtspersoon, wat resulteert in meerdere keren sluiten en opnieuw openen van elk plan dat door de levensgebeurtenis wordt beïnvloed. |
| 518064 | Slechts één afhankelijke die is geselecteerd voor in aanmerking komende plannen als meer dan één is gemarkeerd als standaardbegunstigden | Een probleem opgelost waarbij meerdere standaardbegunstigden niet automatisch worden geselecteerd in kwalificerende plannen. U kunt nu ook een primaire begunstigde voor een persoonlijke contactpersoon aanwijzen. De primaire begunstigde wordt vermeld als 100% in kwalificerende plannen als er meerdere begunstigden zijn. |
| 552365 | Uw eigen database (BYOD)-exporttaken kunnen niet worden uitgevoerd nadat u een upgrade voor platformupdate 40 hebt uitgevoerd | Een probleem opgelost waarbij BYOD niet exporteert nadat platformupdate 40 op de omgeving is toegepast. |
| 547123 | Het aantal taken beperken dat in takenlijst op dashboard wordt opgevraagd | Het aantal taken dat wordt weergegeven in de takenlijst is nu beperkt tot 15 om een prestatieprobleem op te lossen dat wordt veroorzaakt doordat te veel taken proberen te laden. |

## <a name="in-preview"></a>Preview

Van de volgende nieuwe functies kan een voorbeeld worden bekeken. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het in- en uitschakelen van functies.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Bedrijfsweergave van verlof voor managers | [Bedrijfsweergave van werknemersverlof voor managers](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Parameters voor verlof en verzuim configureren](./hr-leave-and-absence-parameters.md) |
| Werkgebied voor vergoedingenbeheer | [Werkruimte Vergoedingenbeheer (preview)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Werkgebied voor vergoedingenbeheer](hr-benefits-management-workspace.md) |
| Voorkomen dat werknemers zakelijke contactgegevens bewerken | [Voorkomen dat werknemers zakelijke contactgegevens bewerken](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Bewerken van persoonlijke gegevens beperken](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>Binnenkort beschikbaar

| Functie | Gegevens |
| --- | --- |
| Vaardigheden die een manager voor diens werknemers invoert, kunnen automatisch worden goedgekeurd door een workflow | Binnenkort beschikbaar. |

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) voor een volledige lijst met geplande functies en de bijbehorende geplande versies.

## <a name="terminology-updates-for-microsoft-dataverse"></a>Terminologiewijzigingen voor Microsoft Dataverse

Met ingang van november 2020 is Common Data Service omgedoopt tot [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro). Zie voor meer informatie de [officiële aankondiging](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) op het Power Apps-blog. Met deze naamswijziging is een aantal termen in Dataverse bijgewerkt. *Entiteit* is nu bijvoorbeeld *tabel* en *veld* is nu *kolom*. Zie [Terminologiewijzigingen](/powerapps/maker/data-platform/data-platform-intro#terminology-updates) voor meer informatie.

In deze versie is de terminologie met betrekking tot de Dynamics 365 Human Resources-integratie met Dataverse in de hele toepassing bijgewerkt om deze wijzigingen weer te geven. Het formulier **Common Data Service-integratie** heet nu bijvoorbeeld **Microsoft Dataverse-integratie**.

Meer informatie over de integratie van Dynamics 365 Human Resources met Microsoft Dataverse vindt u in [De Microsoft Dataverse-integratie configureren](./hr-admin-integration-common-data-service.md) en [De virtuele Microsoft Dataverse-tabellen configureren](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="updates-to-service-deployment"></a>Updates voor service-implementatie

Vanaf de release van 22 februari 2021 passen wij onze regionale service update-implementatie aan. De aanpassingen omvatten het bijwerken van de volgorde waarin mondiale regio's updates voor de Human Resources-service ontvangen, en wijzigingen in de wachttijd tussen updatefasen. Deze wijzigingen brengen ons meer in overeenstemming met Safe Deployment Practices (SDP) om de betrouwbaarheid, kwaliteit en ondersteuning van de service te verbeteren.

We blijven het implementatieritme van twee weken volgen. Het kan klanten echter bekend zijn dat updates meestal op een andere dag van de cyclus van twee weken op hun Human Resources-omgevingen worden toegepast dan in vorige versies.

Zie het [Updateproces](./hr-admin-setup-update-process.md) voor meer informatie over het updateproces voor de service.

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van Dynamics 365 Human Resources 2021 release wave 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]