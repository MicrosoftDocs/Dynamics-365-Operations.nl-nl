---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources 22 maart 2021
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 22 maart 2021.
author: marcelbf
ms.date: 03/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-03-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2cfdd0fc1ca7ba206b0f447ecabd801a5a4e8c57
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859483"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-22-2021"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources 22 maart 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit artikel worden de functies beschreven die in Dynamics 365 Human Resources nieuw, gewijzigd of binnenkort beschikbaar zijn.

Zie [Updateproces](hr-admin-setup-update-process.md) voor meer informatie over het updateproces en de planning.

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) voor meer informatie over nieuwe functies en de verwachte algemene beschikbaarheidsdatums ervan.

## <a name="in-this-release"></a>In deze versie

Deze versie bevat de volgende nieuwe functies en correcties. Wijzigingen die van toepassing zijn op buildnummer 8.1.4049.

### <a name="new-features"></a>Nieuwe functies

De volgende functie zijn algemeen beschikbaar in deze release.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Optie om de annulering en reset van vastgelopen batchtaken af te dwingen (560976) | NA | [Vastgelopen batchtaken opnieuw instellen](./hr-admin-troubleshooting-batch-execution.md) |
| Kleine UX-updates voor het maken van een nieuw vergoedingsplan (419941) | NA | [Een nieuw vergoedingsplan maken](hr-benefits-plans-setup.md) |

### <a name="bug-fixes"></a>Correcties

Deze versie bevat de volgende correcties.

> [!NOTE]
> Ons doel is om deze informatie zo snel mogelijk bij u te krijgen. Mogelijk wordt dit artikel gewijzigd om correcties op te nemen die in de build zijn gemaakt nadat dit artikel oorspronkelijk werd gepubliceerd.

| Probleemnummer | Probleem |  Description |
| --- | --- | --- |
| 554239 | Prestatieverbeteringen voor entiteiten gerelateerd aan de tabel **BusinessProcessTaskAssignment** | Verbeter de prestaties van entiteiten die zijn gerelateerd aan de tabel **BusinessProcessTaskAssignment** door voorgestelde indexen aan de tabel toe te voegen. |
| 566061 | V2-terugvalcode voor entiteiten verwijderen uit nachtelijke synchronisatie | Verwijder de V2-terugvalcode voor nachtelijke Dataverse-synchronisaties. De terugvalmogelijkheid is niet langer nodig en voorkomt dat gefilterde synchronisatie werkt zoals verwacht. De wijziging verbetert de consistentie van de Dataverse-gegevenssynchronisatie. |
| 538024 | Vergoedingsplannen voor medewerker > Kassafout verwijderen | Oplossing voor de fout bij het verwijderen van de optie voor afrekenen voor de optie Vergoedingsplan in het formulier Medewerkersvergoedingen. |
| 557965 | De werkruimte **Vergoedingen**: de koppeling **Actieve levensgebeurtenissen** moet altijd zichtbaar zijn in de sectie **Koppelingen** | Oplossing voor het probleem waarbij de koppeling **Actieve levensgebeurtenissen** zichtbaar was in de sectie **Koppelingen**, maar een fout genereerde tijdens het navigeren als de functie **(Preview) Werkgebied voor vergoedingenbeheer** niet was ingeschakeld. Zie [Werkgebied voor vergoedingenbeheer](hr-benefits-management-workspace.md) voor meer informatie over het inschakelen van de werkruimte. |
| 556672 | Toerekeningen kunnen niet worden verwerkt voor een beëindigde werknemer wanneer **Gestroomlijnde invoer voor werknemers** is ingeschakeld in Functiebeheer | De optie om verlof- en verzuimplannen toe te rekenen, is toegevoegd aan **Meer opties** onder **Werkgeschiedenis** voor werknemers wanneer **Gestroomlijnde invoer voor werknemers** is ingeschakeld in Functiebeheer. |
| 562656 | Het menu-item **SysRecordChangeLogValidTimeState** item moet worden opgenomen in een beveiligingsmachtiging en een uitbreiding van de beveiligingsfunctie **SystemExternalBasicMaintain** | Voor niet-systeembeheerdersrollen ontbrak de knop **Wijzigingen weergeven** op de formulieren voor datumbeheer. |
| 505989 | Verwerking van levensgebeurtenissen: wijziging van geschiktheid niet correct verwerkt vanwege de gebruikte datum | Oplossing voor probleem waarbij een wijziging in de geschiktheidsverwerking afhankelijk was van de begindatum van de positie en niet alleen van de huidige positie. |
| 562286 | Met Medewerker ontslaan worden meerdere updates naar Dataverse verzonden | Wanneer een medewerker wordt ontslagen, wordt meer dan één updatebewerking verzonden naar Dataverse, wat resulteert in twee updatemeldingen voor dezelfde wijziging. Dit kan meerdere triggers veroorzaken als een Power Automate-stroom is geconfigureerd om te worden geactiveerd op basis van de actie. |
| 527340 | De fout Niet-representatieve datum/tijd wordt weergegeven bij het openen van verlof- en verzuiminschrijvingen | De fout wordt niet meer weergegeven wanneer u een verlof- en verzuiminschrijving selecteert. |
| 561663 | Wachttijdinterval voor clusterinrichting verhogen | Verbeter de stabiliteit van de infrastructuur en de consistentie van inrichtingen met updates voor clusterinrichting. |
| 486129 | Kan aangepaste velden niet bewerken in **Posities > Wijzigingen beheren** | Er is een probleem opgelost waarbij aangepaste velden niet konden worden bewerkt op het tabblad **Wijzigingen beheren** voor **Posities**. |

## <a name="in-preview"></a>Preview

Van de volgende nieuwe functies kan een voorbeeld worden bekeken. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het in- en uitschakelen van functies.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Werkgebied voor vergoedingenbeheer | [Werkruimte Vergoedingenbeheer (preview)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Werkgebied voor vergoedingenbeheer](hr-benefits-management-workspace.md) |
| Voorkomen dat werknemers zakelijke contactgegevens bewerken | [Voorkomen dat werknemers zakelijke contactgegevens bewerken](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Bewerken van persoonlijke gegevens beperken](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>Binnenkort beschikbaar

| Functie | Gegevens |
| --- | --- |
| Vaardigheden die een manager voor diens werknemers invoert, kunnen automatisch worden goedgekeurd door een workflow | Binnenkort beschikbaar. |

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) voor een volledige lijst met geplande functies en de bijbehorende geplande versies.

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van Dynamics 365 Human Resources 2021 release wave 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]