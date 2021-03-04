---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (7 februari 2020)
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 7 februari 2020.
author: Darinkramer
manager: AnnBe
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 42fac6e34db10efb047b4cb0fc3c7752330e5bcf
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2020
ms.locfileid: "4526829"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-7-2020"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (7 februari 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In dit artikel worden de functies beschreven die in Dynamics 365 Human Resources nieuw of gewijzigd zijn. Wijzigingen die van toepassing zijn op buildnummer 8.1.2835. De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in Microsoft Dynamics Lifecycle Services (LCS).

## <a name="learning-analytics-doesnt-show-the-course-if-the-classroom-is-blank-388289"></a>In trainingsanalyses wordt de cursus niet weergegeven als het leslokaal leeg is (388289)

Op de pagina trainingsanalyses wordt de cursus nu weergegeven als het leslokaal leeg is.

## <a name="position-lookup-doesnt-take-the-time-zone-into-account-405344"></a>Bij positie zoeken wordt geen rekening gehouden met de tijdzone (405344)

Bij het zoeken naar openstaande posities wordt nu rekening gehouden met de tijdzone wanneer wordt gecontroleerd of er een positie open is.

## <a name="current-balance-analysis-view-doesnt-update-with-the-correct-current-leave-balance-after-submitting-time-off-requests-409756"></a>De huidige weergave voor saldoanalyse wordt niet bijgewerkt met het juiste huidige verlofsaldo na het indienen van een verlofaanvragen (409756)

Het huidige saldo bevat nu de ingediende verlofaanvragen.

## <a name="in-preview"></a>Preview

De volgende voorbeeldfuncties zijn beschikbaar op 3 februari 2020:

- **Preview-functies voor verlof en verzuim** - Zie [Preview-functies voor verlof en verzuim](hr-leave-and-absence-overview.md?leave-and-absence-preview-features) voor meer informatie.

- **Preview-functie voor Vergoedingenbeheer** - Zie [Overzicht van Vergoedingenbeheer](hr-benefits-management-overview.md) voor meer informatie, inclusief bekende problemen.

## <a name="coming-soon"></a>Binnenkort beschikbaar

### <a name="platform-update-32"></a>Platformupdate 32 

Platform update 32 komt binnenkort beschikbaar. [Meer informatie over Platform update 32 vindt u hier](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).

### <a name="updated-common-data-service-solution"></a>Common Data Service-oplossing is bijgewerkt

Binnenkort komt een nieuwe Common Data Service-oplossing beschikbaar met de volgende wijzigingen:

| Beschrijving | Wisselgeld |
| ----------------------------------------- | --- |
| Wijzigingen in de entiteit **Functie/positie** | **Compensatieregio** toegevoegd</br>**Financiële dimensies** toegevoegd |
| Wijzigingen in entiteit **Medewerker** | **Naamsvolgorde** toegevoegd</br>**Werkt thuis** toegevoegd</br>**Taal** toegevoegd</br>**Anciënniteitsdatum** toegevoegd</br>**Jubileumdatum** toegevoegd</br>**Oorspronkelijke datum indiensttreding** toegevoegd |
| Wijzigingen in entiteit **Aanstelling** | **Financiële dimensies** toegevoegd</br>**Reden van ontslag** toegevoegd</br>**Ontslagdatum** gewijzigd van **Overgangsdatum**</br>**Proeftijddatum** toegevoegd |
| Wijzigingen in entiteit **Adres medewerker** | **Adres** toegevoegd</br>**Adresregel 1**, **Adresregel 2** en **Adresregel 3** gemarkeerd voor afschaffing |
| Entiteiten voor nieuwe instellingen voor variabele compensatie | **Type variabelecompensatieplan**</br>**Variabelecompensatieplan**</br>**Vestigingsregels**</br>**Niveau variabelecompensatieplan** |
| Nieuwe entiteit **Medewerkerkalender aanstelling** | Entiteit **Werkkalender** toegevoegd |
| Nieuwe entiteit **Salarispositiedetail** | **Salarispositiedetail** toegevoegd |
| Nieuwe entiteit **Titel** | **Titel** toegevoegd. De nieuwe entiteit **Titel** wordt opgenomen in het synchronisatie proces tussen Human Resources en Common Data Service. Er wordt niet eerst verwezen vanuit de entiteiten **Functiepositie** of **Functie**. |

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van releasewave 2 van Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]