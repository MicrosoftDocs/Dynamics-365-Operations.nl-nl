---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (18 februari 2020)
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 02/18/2020
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
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 96e66c86e98cc1cfee82221da06f9c57a17d170b
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/20/2020
ms.locfileid: "3077456"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-18-2020"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (18 februari 2020)

In dit artikel worden de functies beschreven die in Dynamics 365 Human Resources nieuw of gewijzigd zijn. Wijzigingen die van toepassing zijn op buildnummer 8.1.2903. De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in LCS ter referentie.

## <a name="platform-update-32"></a>Platformupdate 32 

Platform update 32 is nu beschikbaar. Meer informatie vindt u in [Nieuw of gewijzigd in Platform update 32 voor Finance and Operations (februari 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).

## <a name="search-values-are-remembered-when-changing-view-options-in-streamlined-employee-form-383833"></a>Zoekwaarden worden onthouden bij het wijzigen van de weergaveopties in het gestroomlijnde formulier voor werknemers (383833)

Het nieuwe formulier **Medewerker** onthoudt nu zoekwaarden wanneer u de weergaveopties wijzigt en wijzigingen toepast.

## <a name="compensation-management-summary-tiles-in-preview-feature-redirect-to-wrong-form-401861"></a>Overzichtstegels voor compensatiebeheer in preview-functie leiden om naar verkeerd formulier (401861)

Met de tegels voor vaste- en variabele-compensatiebeheer worden nu de juiste records weergegeven in het nieuwe formulier **Medewerker**. Is alleen van toepassing op de preview-functie voor het gestroomlijnde formulier voor werknemers. U kunt deze preview-functie inschakelen in **Functiebeheer**. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie.

## <a name="empty-status-field-for-some-leave-request-records-in-common-data-service-414915"></a>Leeg veld Status voor sommige records voor verlofaaanvragen in Common Data Service (414915)

Met deze wijziging wordt een probleem in Common Data Service verholpen als het veld **Status** in een verlofaanvraag is ingesteld op **Controleren**. De status wordt nu weergegeven in Common Data Service.

## <a name="skill-gap-analysis-only-possible-for-assigned-job-411390"></a>Vaardigheidshiaatanalyse alleen mogelijk voor toegewezen taak (411390)

U kunt nu een Vaardigheidshiaatanalyse uitvoeren op elke taak die in Human Resources is gedefinieerd.

## <a name="system-currency-doesnt-sync-from-common-data-service-to-human-resources-in-new-environments-418011"></a>Systeemvaluta wordt niet gesynchroniseerd vanuit Common Data Service met Human Resources in nieuwe omgevingen (418011)

De systeemvaluta in Common Data Service kan nu worden gesynchroniseerd met Human Resources.

## <a name="in-preview"></a>Preview

- [Preview-functies voor verlof en verzuim](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- [Preview-functies voor vergoedingenbeheer](hr-benefits-management-overview.md)

## <a name="coming-soon"></a>Binnenkort beschikbaar

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
