---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (3 maart 2020)
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 3 maart 2020.
author: andreabichsel
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5370beb099318094ff5bc5885374bcca39ca0a30
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894625"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-3-2020"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (3 maart 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In dit artikel worden de functies beschreven die in Dynamics 365 Human Resources nieuw of gewijzigd zijn. Wijzigingen die van toepassing zijn op buildnummer 8.1.2955. De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in LCS ter referentie.

## <a name="dataverse-solution-is-now-available-with-the-following-changes"></a>Dataverse-oplossing is nu beschikbaar met de volgende wijzigingen:

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

In de komende weken zijn deze entiteitswijzigingen beschikbaar in alle omgevingen. Handmatig de meest recente Dataverse-oplossing voor Human Resources installeren:

1.  Ga naar het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com).

2.  Selecteer **Omgevingen**.

3.  Zoek de omgeving die u wilt bijwerken. De omgeving moet overeenkomen met **Omgevingsnaam**  in de sectie **Common Data Service-gegevens** in het formulier **Info** in Human Resources.

4.  Selecteer de omgeving waarin u de omgevingsdetails wilt weergeven.

5.  Selecteer **Oplossingen beheren** op de actiebalk bovenaan. Er wordt een nieuw browservenster geopend waarin u naar **Dynamics 365-beheercentrum** gaat in de context van uw omgeving.

6.  Selecteer in de lijst **Oplossing** **Dynamics 365 Human Resources verankeren**.

7.  Selecteer **Upgraden** om de meest recente oplossing toe te passen.

## <a name="import-issues-with-the-leave-enrollment-data-entity-406082"></a>Importproblemen met de gegevensentiteit Verlofinschrijving (406082)

U kunt nu een werknemer inschrijven voor een nieuw verlofplan van hetzelfde type, zolang de nieuwe inschrijvingsdatum later is dan de vervaldatum van de inschrijving van het vorige plan.

## <a name="issue-with-exporting-contribution-rates-in-the-401k-payrollworkerenrolledbenefitdetail-entity-in-dmf-420700"></a>Probleem met het exporteren van bijdragepercentages in de entiteit 401k payrollWorkerEnrolledBenefitDetail in DMF (420700)

Deze wijziging corrigeert de exportfunctionaliteit voor de entiteit **payrollWorkerEnrolledBenefitDetail** om de huidige waarden voor de bijdrage van de werkgever weer te geven.

## <a name="searching-in-the-streamlined-worker-form-causes-message-saying-person-field-must-be-filled-in-402525"></a>Als u zoekt in het gestroomlijnde werknemerformulier, wordt een bericht weergegeven dat het veld Persoon moet worden ingevuld (402525)

Wanneer u naar een werknemer zoekt, ontvangt u geen bericht meer waarin wordt gemeld dat u het veld **Persoon** moet invullen.

## <a name="note-field-value-doesnt-render-on-the-add-more-skills-form-380134"></a>De waarde van het opmerkingenveld wordt niet weergegeven in het formulier Meer vaardigheden toevoegen (380134)

Deze wijziging corrigeert het probleem wanneer u het formulier **Meer vaardigheden toevoegen** aanpast in de Werknemerselfservice.

## <a name="multiple-fixed-compensation-plans-dont-expire-when-transferring-employees-389466"></a>Meerdere vaste compensatieplannen verlopen niet bij het overboeken van werknemers (389466)

Met deze wijziging vervallen alle actieve records met vaste compensatie voor de oude positie op de overgangsdatum.

## <a name="in-preview"></a>Preview

De volgende voorbeeldfuncties zijn beschikbaar vanaf 3 februari 2020:

- **Preview-functies voor verlof en verzuim** - Zie [Preview-functies voor verlof en verzuim](hr-leave-and-absence-overview.md?leave-and-absence-preview-features) voor meer informatie.

- **Preview-functie voor Vergoedingenbeheer** - Zie [Overzicht van Vergoedingenbeheer](hr-benefits-management-overview.md) voor meer informatie, inclusief bekende problemen.

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van releasewave 2 van Dynamics 365 Human Resources](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]