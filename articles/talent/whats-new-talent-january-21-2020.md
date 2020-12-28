---
title: Wat is nieuw of gewijzigd in Dynamics 365 Talent (21 januari 2020)
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e9dee64e94c904cfe07c6a7766f6a60b1d60a2db
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528117"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-21-2020"></a>Wat is nieuw of gewijzigd in Dynamics 365 Talent (21 januari 2020)

[!include [banner](includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In dit artikel worden de functies beschreven die in Dynamics 365 Talent nieuw of gewijzigd zijn.

## <a name="changes-in-attract"></a>Wijzigingen in Attract

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Attract. We hebben functionaliteit toegevoegd aan Attract, ter ondersteuning van onze recente aankondiging [Building a more successful workforce withEen succesvoller personeelsbestand opbouwen met Dynamics 365 Human Resources](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources/) (Een succesvoller personeelsbestand opbouwen met Dynamics 365 Human Resources).

### <a name="download-environment-data"></a>Omgevingsgegevens downloaden

Beheerders kunnen gegevens van hun omgevingen downloaden. De gegevens worden in de standaard-JSON-indeling geëxporteerd met alle functies, kandidaten en configuratie in één zip-bestand. Meer informatie over dit onderwerp vindt u in [Gegevens exporteren uit Attract en Onboard](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data).

### <a name="restricting-access-to-environments-for-non-admin-users"></a>Toegang tot omgevingen beperken voor gebruikers die geen beheerder zijn

Beheerders kunnen de toegang tot de omgeving nu beperken voor gebruikers die geen beheerder zijn. Deze actie kan niet ongedaan worden gemaakt. Meer informatie over dit onderwerp vindt u in Zie [Toegang tot Attract beperken](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data#restrict-access-to-attract).

## <a name="changes-in-onboard"></a>Wijzigingen in Onboard

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Onboard.

### <a name="exporting-onboarding-guides"></a>Onboardingguides exporteren

Gebruikers kunnen nu al hun onboardingguides en -sjablonen exporteren in Word-indeling. Meer informatie over dit onderwerp vindt u in [Gegevens exporteren uit Attract en Onboard](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data).

## <a name="changes-in-core-hr"></a>Wijzigingen in Core HR

Wijzigingen die worden beschreven in deze sectie, gelden voor buildnummer 8.1.2726. De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in Microsoft Dynamics Lifecycle Services (LCS).

### <a name="most-recent-annual-compensation-field-in-verify-employment-form-isnt-consistent-392092"></a>Het veld voor meest recente jaarlijkse compensatie in het formulier Dienstverband controleren is niet consistent (392092)

Deze versie bevat een wijziging waarmee consistent de meest recente valuta wordt weer gegeven, op basis van de bedrijvenkiezer op het formulier **Dienstverband controleren**.

### <a name="known-as-field-added-to-the-feedback-recipient-lookup-407789"></a>Het veld Bekend als toegevoegd aan het opzoekveld Feedbackontvanger (407789)

Bij het geven van feedback over functioneren biedt het opzoekveld voor medewerkers onvoldoende informatie om te bepalen of feedback naar de juiste persoon wordt verzonden. We hebben een kolom **Bekend als** toegevoegd om de unieke naam van de werknemer te identificeren.
 
### <a name="hcmworkerpayrollinfo-record-is-created-without-an-association-to-a-worker-394526"></a>HcmWorkerPayrollInfo-record wordt gemaakt zonder koppeling met een werknemer (394526)

Deze versie bevat een wijziging waarmee geen HCMWorkerPayrollInfo-records worden aangemaakt zonder verwijzing naar een werknemer.

### <a name="able-to-edit-department-when-navigating-from-position-hierarchy-341001"></a>Afdeling kan worden bewerkt tijdens het navigeren vanuit de positiehiërarchie (341001)

Als de beveiliging is ingesteld om de toegang tot het bewerken van afdelingen te weigeren, wordt bewerken uitgeschakeld wanneer u in alle scenario's naar het formulier **Afdelingen** navigeert.

## <a name="coming-soon"></a>Binnenkort beschikbaar

Binnenkort komt een nieuwe Common Data Service-oplossing beschikbaar met de volgende wijzigingen:

| Beschrijving | Wisselgeld |
| --- | --- |
| Wijzigingen in de entiteit **Functie/positie** | <ul><li>**Compensatieregio** toegevoegd</li><li>**Financiële dimensies** toegevoegd</li></ul> |
| Wijzigingen in entiteit **Medewerker** | <ul><li>**Naamsvolgorde** toegevoegd</li><li>**Werkt thuis** toegevoegd</li><li>**Taal** toegevoegd</li><li>**Anciënniteitsdatum** toegevoegd</li><li>**Jubileumdatum** toegevoegd</li><li>**Oorspronkelijke datum indiensttreding** toegevoegd</li></ul> |
| Wijzigingen in entiteit **Aanstelling** | <ul><li>**Financiële dimensies** toegevoegd</li><li>**Reden van ontslag** toegevoegd</li><li>**Ontslagdatum** gewijzigd van **Overgangsdatum**</li><li>**Proeftijddatum** toegevoegd</li></ul> |
| Wijzigingen in entiteit **Adres medewerker** | <ul><li>**Adres** toegevoegd</li><li>**Adresregel 1**, **Adresregel 2** en **Adresregel 3** gemarkeerd voor afschaffing</li></ul> |
| Entiteiten voor nieuwe instellingen voor variabele compensatie | <ul><li>**Type variabelecompensatieplan**</li><li>**Variabelecompensatieplan**</li><li>**Vestigingsregels**</li><li>**Niveau variabelecompensatieplan**</li></ul> |
| Nieuwe entiteit **Medewerkerkalender aanstelling** | <ul><li>Entiteit **Werkkalender** toegevoegd</li></ul> |
