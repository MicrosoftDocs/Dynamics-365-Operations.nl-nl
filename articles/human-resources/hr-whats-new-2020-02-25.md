---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (25 februari 2020)
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 25 februari 2020.
author: andreabichsel
manager: tfehr
ms.date: 02/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4faecb83518f3ef8af825872abc2a6ffb94162fc
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/06/2021
ms.locfileid: "5128017"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (25 februari 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In dit artikel worden de functies beschreven die in Dynamics 365 Human Resources nieuw of gewijzigd zijn. Wijzigingen die van toepassing zijn op buildnummer 8.1.2927. De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in LCS ter referentie.

## <a name="enable-case-management-navigation-and-data-management-framework-dmf-entity-414754"></a>Navigatie voor Casebeheer en DMF-entiteit (Data Management Framework) inschakelen (414754)

Met deze preview-functie wordt extra navigatie voor casebeheer ingeschakeld. U kunt deze preview-functie inschakelen in het werkgebied **Functiebeheer**. Deze menuopdrachten worden weergegeven in het werkgebied **Conformiteit** van Dynamics 365 Human Resources. Met deze wijziging heeft Human Resources toegang tot:

- Alle cases
- Mijn cases
- Mijn openstaande cases
- Mijn achterstallige cases
- Via werkstroom aan mij toegewezen aanvragen

Naast deze nieuwe weergaven voor cases is de DMF-entiteit **Casedetails** ook beschikbaar.

## <a name="enable-relationship-definitions-in-global-address-bbook-414762"></a>Relatiedefinities in Globaal adresboek inschakelen (414762)

Relaties zijn nu ingeschakeld in het globale adresboek. Vóór de release van deze week werden in het feitenvak **Relatie** eventuele door het systeem gedefinieerde relaties weergegeven. U kunt deze relaties nu definiëren binnen de pagina Globaal adresboek.

## <a name="a-position-can-be-removed-when-active-compensation-records-exist-for-the-position-414568"></a>Een positie kan worden verwijderd wanneer actieve compensatierecords bestaan voor de positie (414568)

Met deze wijziging wordt een waarschuwing weergegeven wanneer u een positie probeert te verwijderen en een werknemer voor diezelfde positie een actieve compensatierecord heeft. In dat geval moet u de vaste compensatierecord voor de werknemer bijwerken voordat u de positie verwijdert.

## <a name="performance-review-workflow-occasionally-adds-sign-offs-from-people-who-are-not-part-of-the-process-414171"></a>De werkstroom Prestatieoverzicht voegt soms afmeldingen toe van mensen die geen deel uitmaken van het proces (414171)

Deze wijziging corrigeert het probleem waarbij extra afmeldingen van deelnemers aan het prestatieoverzicht worden toegevoegd.

## <a name="worker-position-assignment-not-created-in-dataverse-when-selected-on-the-new-worker-dialog-413479"></a>De toewijzing van de werknemerpositie wordt niet gemaakt in Dataverse, wanneer deze is geselecteerd in het dialoogvenster Nieuwe werknemer (413479)

Deze wijziging corrigeert het probleem bij het aanstellen van een nieuwe werknemer en het toewijzen van de nieuwe aanstelling aan een positie via het dialoogvenster **Nieuwe werknemer**. De positietoewijzing wordt nu weerspiegeld in Dataverse.

## <a name="coming-soon"></a>Binnenkort beschikbaar

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

In de komende weken zijn deze entiteitswijzigingen beschikbaar in alle omgevingen. Handmatig de meest recente Dataverse-oplossing voor Human Resources installeren:

1.  Ga naar het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com).

2.  Selecteer **Omgevingen**.

3.  Zoek de omgeving die u wilt bijwerken. Dit moet overeenkomen met **Omgevingsnaam**  in de sectie **Common Data Service-gegevens** in het formulier **Info** in Human Resources.

4.  Selecteer de omgeving waarin u de omgevingsdetails wilt weergeven.

5.  Selecteer **Oplossingen beheren** op de actiebalk bovenaan. Er wordt een nieuw browservenster geopend waarin u naar **Dynamics 365-beheercentrum** gaat in de context van uw omgeving.

6.  Selecteer in de lijst **Oplossing** **Dynamics 365 Human Resources verankeren**.

7.  Selecteer **Upgraden** om de meest recente oplossing toe te passen.

## <a name="in-preview"></a>Preview

De volgende voorbeeldfuncties zijn beschikbaar vanaf 3 februari 2020:

- **Preview-functies voor verlof en verzuim** - Zie [Preview-functies voor verlof en verzuim](hr-leave-and-absence-overview.md?leave-and-absence-preview-features) voor meer informatie.

- **Preview-functie voor Vergoedingenbeheer** - Zie [Overzicht van Vergoedingenbeheer](hr-benefits-management-overview.md) voor meer informatie, inclusief bekende problemen.

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van releasewave 2 van Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]