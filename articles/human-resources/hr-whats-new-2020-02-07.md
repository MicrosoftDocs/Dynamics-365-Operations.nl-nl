---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (7 februari 2020)
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 7 februari 2020.
author: andreabichsel
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e58ab3ffc215a340dca694aee7cf04c65303b65b
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687947"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-7-2020"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (7 februari 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



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

Platform update 32 komt binnenkort beschikbaar. [Meer informatie over Platform update 32 vindt u hier](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32.md).

### <a name="updated-dataverse-solution"></a>Dataverse-oplossing is bijgewerkt

Binnenkort komt een nieuwe Dataverse-oplossing beschikbaar met de volgende wijzigingen:

| Beschrijving | Wisselgeld |
| ----------------------------------------- | --- |
| Wijzigingen in de entiteit **Functie/positie** | **Compensatieregio** toegevoegd</br>**Financiële dimensies** toegevoegd |
| Wijzigingen in entiteit **Medewerker** | **Naamsvolgorde** toegevoegd</br>**Werkt thuis** toegevoegd</br>**Taal** toegevoegd</br>**Anciënniteitsdatum** toegevoegd</br>**Jubileumdatum** toegevoegd</br>**Oorspronkelijke datum indiensttreding** toegevoegd |
| Wijzigingen in entiteit **Aanstelling** | **Financiële dimensies** toegevoegd</br>**Reden van ontslag** toegevoegd</br>**Ontslagdatum** gewijzigd van **Overgangsdatum**</br>**Proeftijddatum** toegevoegd |
| Wijzigingen in entiteit **Adres medewerker** | **Adres** toegevoegd</br>**Adresregel 1**, **Adresregel 2** en **Adresregel 3** gemarkeerd voor afschaffing |
| Entiteiten voor nieuwe instellingen voor variabele compensatie | **Type variabelecompensatieplan**</br>**Variabelecompensatieplan**</br>**Vestigingsregels**</br>**Niveau variabelecompensatieplan** |
| Nieuwe entiteit **Medewerkerkalender aanstelling** | Entiteit **Werkkalender** toegevoegd |
| Nieuwe entiteit **Salarispositiedetail** | **Salarispositiedetail** toegevoegd |
| Nieuwe entiteit **Titel** | **Titel** toegevoegd. De nieuwe entiteit **Titel** wordt opgenomen in het synchronisatie proces tussen Human Resources en Dataverse. Er wordt niet eerst verwezen vanuit de entiteiten **Functiepositie** of **Functie**. |

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van releasewave 2 van Dynamics 365 Human Resources](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]