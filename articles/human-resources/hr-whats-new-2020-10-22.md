---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources 22 oktober 2020
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 22 oktober 2020.
author: jcart1106
manager: tfehr
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 41b4e92720c6a9f830d940900c3c6e5b0a173de0
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130826"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-22-2020"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources 22 oktober 2020

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn of die binnenkort worden vrijgegeven in Dynamics 365 Human Resources. Zie [Updateproces](hr-admin-setup-update-process.md) voor meer informatie over het updateproces en de planning.

Zie [Overzicht van Dynamics 365 Human Resources 2020 release wave 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/) voor meer informatie over nieuwe functies en de verwachte algemene beschikbaarheidsdatums ervan.

## <a name="in-this-release"></a>In deze versie

Deze versie bevat de volgende nieuwe functies en correcties. Wijzigingen die van toepassing zijn op buildnummer 8.1.3680.

### <a name="new-features"></a>Nieuwe functies

De volgende functie zijn algemeen beschikbaar in deze release.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Platformupdate 10.0.14(38) | -- | [Platformupdates voor versie 10.0.14 van Finance and Operations-apps (november 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-14) |
| Verbeteringen in de ervaring van werkstromen voor organisatie en personeelsbeheer | [Verbeteringen in de ervaring van werkstromen voor organisatie en personeelsbeheer](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Configuratieoptie om de lijst Aan mij toegewezen werkitems te positioneren](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |


### <a name="bug-fixes"></a>Correcties

Deze versie bevat de volgende correcties.

> [!NOTE]
> Ons doel is om deze informatie zo snel mogelijk bij u te krijgen. Mogelijk wordt dit onderwerp gewijzigd om correcties op te nemen die in de build zijn gemaakt nadat dit onderwerp oorspronkelijk werd gepubliceerd.

| Probleemnummer| Uitgeven  | Beschrijving|
| --- | --- | --- |
| 437922 | Het importeren van FMLA-uren met de DMF-entiteit resulteert in een alleen-lezenfout. | Het gebruik van de entiteit FMLA-uren om uren te importeren die aan een FMLA-case zijn gekoppeld, mislukt. Er is logica toegevoegd om ervoor te zorgen dat het aantal geïmporteerde uren niet groter is dan het aantal resterende uren voor de case. |
| 512019 | Onjuist bedrag voor **Laatste transport**. | Als op de pagina **Verlof** de datum bij **Datum vanaf** werd gewijzigd in de eerste dag van de volgende boekperiode, werd er een onjuist bedrag bij **Laatste transport** voor het type **Jaarlijks verlof** weergegeven. Nu wordt het juiste bedrag weergegeven. |
| 458639 | Voor de entiteit **Contactpersonen werknemer** wordt de modus voor het bijhouden van wijzigingen niet ondersteund. | De entiteit **Contactpersonen werknemer** is bijgewerkt , zodat u deze kunt gebruiken in BYOD-scenario´s (Bring You Own Database).|
| 505347 | Trainingsmanagers konden een verlofaanvraag indienen voor een werknemer wanneer de functie Gestroomlijnde werknemer was ingeschakeld. | Andere rollen dan HR-assistent en HR-manager mogen geen verlofaanvragen indienen voor werknemers. |
| 513490 | Logboekregistratie van vergoedingenbeheer: logboekregistratie toevoegen voor plannen zonder opties voor dekking. | Er zijn nu logboekregistratieresultaten voor **Plan zonder opties voor dekking** ingeschakeld. Ze worden nu weergegeven in de tabel **Procesresultaten** en worden correct gesorteerd zodat ze bovenaan worden weergegeven. |
| 517021 | Er kunnen niet meerdere plannen met dezelfde code voor **Plantype** worden geselecteerd als het **Plantype** één inschrijving per type heeft. | De beperkingen voor het selecteren van plannen waarvoor slechts één inschrijving is toegestaan, zijn gewijzigd. De beperkingen zijn nu op het niveau van **Plantypecode** in plaats van **Plantype**. Door deze wijziging zijn plannen zoals HSA en FSA mogelijk, die beide van hetzelfde type zijn, maar u kunt ze wel een aparte **Plantypecode** geven. Op deze manier kunt u beide voor dezelfde inschrijvingsperiode selecteren. |
| 444791 | Compensatie in Selfservice werknemer kan niet worden weergegeven wanneer **Toegang beperken** wordt ingeschakeld in het compensatieplan. | In de kaart **Compensatie** van de Selfservice werknemer werden het huidige compensatiebedrag en het verhogingspercentage weergegeven als "0" als de werknemer was ingeschreven voor een plan waarvoor **Toegang beperken** was ingeschakeld en toegewezen aan specifieke rollen. Dit probleem is opgelost, zodat de werknemer en manager altijd compensatiedetails kunnen zien voor zichzelf en hun directe ondergeschikten. |
| 457542 | Als cursusdetails worden bijgewerkt nadat de cursus is gesloten, wordt dezelfde informatie niet ook bijgewerkt voor de werknemer die de cursus heeft gevolgd. | De werknemersgegevens worden nu correct bijgewerkt wanneer u cursusdetails wijzigt nadat een cursus is gesloten en opnieuw is geopend. |
| 515342 | Er kunnen geen gegevens worden ingevoegd via **CDSLeaveRequestDetailEntity**. Bedrijf is niet gevonden of bestaat niet. | U kunt nu **CDSLeaveRequestDetailEntity** gebruiken om gegevens in te voegen. |
| 514743 | Fout in het formulier **E-mailparameter** bij het gebruik van Microsoft Exchange. | Het bericht "Kan bestanden of assembly niet laden..." werd weergegeven op de pagina **E-mail parameters** wanneer de e-mailprovider werd ingesteld op **Exchange**. Deze oplossing zorgt ervoor dat de pagina **E-mailparameters** wordt geladen en opgeslagen zoals verwacht. |


## <a name="in-preview"></a>Preview

Van de volgende nieuwe functies kan een voorbeeld worden bekeken. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het in- en uitschakelen van functies.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Human Resources-app in Microsoft Teams | [Verlof en verzuim van werknemers in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Human Resources-app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Verlofaanvragen beheren in Teams](hr-teams-leave-app.md) |
| Uitgebreide aanvragen en goedkeuringen voor werkstromen | [Verbeteringen in de ervaring van werkstromen voor organisatie en personeelsbeheer](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Configuratieoptie om de lijst Aan mij toegewezen werkitems te positioneren](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Virtuele entiteiten in Dataverse voor Human Resources | [Dynamics 365 Human Resources-kerngegevens in Dataverse uitbreiden](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [Virtuele entiteiten van Dataverse configureren](hr-admin-integration-common-data-service-virtual-entities.md) |
| Integratie met LinkedIn Talent Hub | [Integratie met LinkedIn Talent Hub](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [Integreren met LinkedIn Talent Hub](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-linkedin) |
| Aangepaste koppelingen in Selfservice manager | [Aangepaste koppelingen in Selfservice manager](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [Aangepaste koppelingen in Selfservice manager](https://aka.ms/MSSCustomLinks) |

## <a name="coming-soon"></a>Binnenkort beschikbaar

Zie [Overzicht van Dynamics 365 Human Resources 2020 release wave 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/) voor een volledige lijst met geplande functies en de bijbehorende geplande versies.


## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van Dynamics 365 Human Resources 2020 release wave 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)
