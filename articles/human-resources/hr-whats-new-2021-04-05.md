---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources, 5 april 2021
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 5 april 2021.
author: marcelbf
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9388b2f43762bedf07c89a7a565935d2043ee90c
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067996"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-5-2021"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources, 5 april 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit artikel worden de functies beschreven die in Dynamics 365 Human Resources nieuw, gewijzigd of binnenkort beschikbaar zijn.

Zie [Updateproces](hr-admin-setup-update-process.md) voor meer informatie over het updateproces en de planning.

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) voor meer informatie over nieuwe functies en de verwachte algemene beschikbaarheidsdatums ervan.

## <a name="in-this-release"></a>In deze versie

Deze versie bevat de volgende nieuwe functies en correcties. Wijzigingen die van toepassing zijn op buildnummer 8.1.4074.

### <a name="new-features"></a>Nieuwe functies

De volgende functie zijn algemeen beschikbaar in deze release.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Voorkomen dat werknemers zakelijke contactgegevens bewerken | [Voorkomen dat werknemers zakelijke contactgegevens bewerken](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Het bewerken van persoonlijke gegevens beperken](./hr-employee-self-service-restrict-editing.md)|

### <a name="bug-fixes"></a>Correcties

Deze versie bevat de volgende correcties.

> [!NOTE]
> Ons doel is om deze informatie zo snel mogelijk bij u te krijgen. Mogelijk wordt dit artikel gewijzigd om correcties op te nemen die in de build zijn gemaakt nadat dit artikel oorspronkelijk werd gepubliceerd.

| Probleemnummer | Probleem |  Description |
| --- | --- | --- |
| 550852 | De knop **Goedkeuring** valideert niet met verplichte velden die zijn ingesteld op het formulier **Controleren**. | Wanneer u een veld in het formulier **Controleren** instelt als verplicht en de wijzigingen publiceert voor de rol Manager, wordt het formulier niet gevalideerd zoals verwacht. |
| 559564 | Historische werknemersacties voor wijziging van vaste compensatie geven foutmeldingen voor ontslagen gebruikers. | Een actie van een werknemer voor de compensatie na ontslag, levert een fout op. Nadat een werknemer is ontslagen, veroorzaakt de werknemeractie voor promotie voordat het ontslag inging, een fout. |
| 560074 | Vervolgkeuzelijst voor Aanstellingscategorie wordt niet gefilterd op **Werknemerstype** en geeft categorieën weer voor werknemers en contractanten. | In het formulier **Werknemer** moet de vervolgkeuzelijst **Aanstellingscategorie** de categorieën werknemer of contractant weergeven op basis van het werknemerstype. |
| 567388 | Sommige gegevens voor nieuwe werknemers worden niet direct gesynchroniseerd met de tabel **cdm_worker** in Dataverse. | Wanneer u een nieuwe werknemerrecord maakt, wordt de nieuwe record gesynchroniseerd met de tabel **cdm_worker** in Dataverse, maar worden niet alle eigenschappen in de Dataverse-record opgenomen. |
| 563837 | Functies die niet beschikbaar zijn in de weergave Human Resources. | Een aantal functies die niet van toepassing zijn op Human Resources-weergave in Functiebeheer. Deze functies worden nu verwijderd uit de lijst met functies die beschikbaar is voor inschakelen in Human Resources. |

## <a name="in-preview"></a>Preview

Van de volgende nieuwe functies kan een voorbeeld worden bekeken. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het in- en uitschakelen van functies.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Werkgebied voor vergoedingenbeheer | [Werkruimte Vergoedingenbeheer (preview)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Werkgebied voor vergoedingenbeheer](hr-benefits-management-workspace.md) |

## <a name="coming-soon"></a>Binnenkort beschikbaar

| Functie | Gegevens |
| --- | --- |
| Vaardigheden die een manager voor diens werknemers invoert, kunnen automatisch worden goedgekeurd door een workflow | Binnenkort beschikbaar. |
| Platformupdate 10.0.17 (41) | Platformupdate 10.0.17 is gepland voor de uitrol met de volgende versie op 19 april 2021. Zie voor meer informatie [Platformupdates voor versie 10.0.17 van apps voor financiën en bedrijfsactiviteiten (april 2021)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md). |

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) voor een volledige lijst met geplande functies en de bijbehorende geplande versies.

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van Dynamics 365 Human Resources 2021 release wave 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
