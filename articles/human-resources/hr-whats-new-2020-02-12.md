---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (12 februari 2020)
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 12 februari 2020.
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
ms.openlocfilehash: 7bcb77b74f6e484d68fd57fd1680e8c2d8c82bc4
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712057"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-12-2020"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (12 februari 2020)

In dit artikel worden de functies beschreven die in Dynamics 365 Human Resources nieuw of gewijzigd zijn. Wijzigingen die van toepassing zijn op buildnummer 8.1.2867. De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in Microsoft Dynamics Lifecycle Services (LCS).

## <a name="existing-entities-compfixedempls-and-hcmpersonimage-should-be-accessible-from-odata-414178"></a>Bestaande entiteiten CompFixedEmpls en HcmPersonImage moeten toegankelijk zijn vanuit OData (414178)

Met de release van deze week zijn de entiteiten **CompFixedEmpls** en **HcmPersonImage** nu openbaar en beschikbaar via ODAta.

## <a name="delete-employment-from-common-data-service-doesnt-work-when-employment-details-arent-active-403193"></a>Het verwijderen van een dienstverband uit Common Data Service werkt niet wanneer de details van het dienstverband niet actief zijn (403193)

Door deze wijziging kunnen dienstverbanden nu worden verwijderd via Common Data Service wanneer er geen actieve dienstverbanddetails beschikbaar zijn.

## <a name="course-registration-workflow-changes-status-to-complete-and-errors-after-second-approval-409749"></a>De werkstroom voor cursusregistratie wijzigt de status in voltooid en fouten na de tweede goedkeuring (409749)

De werkstroom voor cursusregistratie is bijgewerkt om meerdere goedkeurders mogelijk te maken.

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