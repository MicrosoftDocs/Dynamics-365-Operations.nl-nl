---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (16 september 2020)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 16 september 2020.
author: jcart1106
ms.date: 09/16/2020
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
ms.author: jcart
ms.search.validFrom: 2020-09-16
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6b07bfb27bbe5e546dac9d72666b3225cc202670
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890694"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-16-2020"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (16 september 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 Human Resources. Wijzigingen die van toepassing zijn op buildnummer 8.1.3557. De getallen tussen haakjes naast sommige functies verwijzen ter referentie naar ondersteuningsnummers in Lifecycle Services (LCS).

## <a name="included-in-this-release"></a>Functies in deze versie

-  [Opgeslagen weergaven - algemene beschikbaarheid](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)<br>- Zie [Opgeslagen weergaven](../fin-ops-core/fin-ops/get-started/saved-views.md) voor meer informatie. 

- Het formulier **Positieacties** heeft een bijgewerkt dimensieraster en een nieuw dialoogvenster (469495).

- Als u de instelling **Toegang tot medewerkersgegevens beperken** instelt op Ja in **Geavanceerde toegang** in **Gedeelde parameters voor Human Resources**, worden in vergoedingsformulieren nu alleen de desbetreffende medewerkers weergegeven (393384).

- Nieuwe opties voor het genereren van kalenders in de entiteit **WorkCalendar** (477055):<br>- Standaardeindtijd<br>- Standaardbegintijd<br>- Is vrijdag werkdag<br>- Is maandag werkdag<br>- Is zaterdag werkdag<br>- Is zondag werkdag<br>- Is donderdag werkdag<br>- Is dinsdag werkdag<br>- Is woensdag werkdag<br>- ID feestdag werkkalender

- De entiteit **LeaveBankTransactionV1** bevat nu de redencode (477823).

- U kunt nu taakregistraties opslaan (492923).

- Gegevens worden nu met succes gepubliceerd vanuit **HCMWorkerContactEntity** (427620).

- Het sneltabblad **Compensatie** wordt nu weergegeven voor het medewerkerstype contractant in het formulier **Medewerkersacties** (482494).

- De velden **Niveau** en **Plan** zijn nu verplicht als u **Vaste compensatie** instelt. Er wordt een foutbericht weergegeven als u deze velden leeg laat (482497).

- Het veld **Plantype** in **Vergoedingen** is nu een vervolgkeuzelijst (488768).

- Systeembeheerders ontvangen nu een melding als een aangepast veld wordt verwijderd uit Human Resources (481408).

- Tijdens het ontslagproces van werknemers gedraagt Human Resources zich zoals verwacht en wordt het geselecteerde bedrijf niet gewijzigd nadat het vergrendeld leek (479877). 

- Managers kunnen geen kolom met nummers meer toevoegen via personalisatie (485317).

- Managers kunnen het gegevensbereikfilter niet meer verwijderen uit identificatienummers die verlopen (485321).

- Wanneer het veld **Rapporteert aan** leeg is, worden de positiedetails nog steeds weergegeven wanneer de positie wordt aangewezen (433328).

- Werknemers kunnen nu informatie over vergoedingsplannen weergeven in Selfservice werknemer (481676).

- Werknemers kunnen nu alle geregistreerde cursussen zien (429048).

- U kunt nu weergaveopties beperken voor de pagina **Professionele certificaten**. U kunt weergaveopties beperken tot de huidige rechtspersoon op basis van status van medewerker en op basis van type medewerker (451501). 


## <a name="in-preview"></a>Preview

### <a name="human-resources-app-in-teams"></a>Human Resources-app in Teams

Werknemers kunnen vrije tijd bekijken en aanvragen in Microsoft Teams. Ze kunnen met een bot werken om verlofaanvragen te maken. Ga voor meer informatie naar:

- [Voorziening voor verlof en verzuim van werknemers in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in het Dynamics 365 2020 releasewave 1-plan
- [Human Resources-app in Teams](./hr-admin-teams-leave-app.md) in Human Resources-documentatie

### <a name="human-resources-app-in-teams-preview-features"></a>Preview-functies op Human Resources-app in Teams
 
-  **Meldingen**: inzenders en goedkeurders van verlofaanvragen worden in de Human Resources-app in Teams geïnformeerd. Fiatteurs kunnen verlofaanvragen goedkeuren of weigeren. Voor indieners wordt een melding weergegeven als de aanvraag is goedgekeurd of geweigerd. Ga voor meer informatie naar:
   - [Voorziening voor verlof en verzuim van werknemers in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in het Dynamics 365 2020 releasewave 2-plan
   - [Meldingen inschakelen voor de Human Resources-app in Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) in Human Resources-documentatie
   - [Teams-meldingen in- of uitschakelen voor individuele gebruikers](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) in Human Resources-documentatie
   - [Teams-meldingen](./hr-teams-leave-app.md#respond-to-teams-notifications) in Human Resources-documentatie
   - [De verlofkalender van uw team weergeven](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources-documentatie
 
- **Verlofagenda van manager**: managers kunnen goedgekeurde en in behandeling zijnde verlofaanvragen van hun ondergeschikten in een kalenderweergave bekijken. Deze weergave geeft duidelijk weer wanneer teamleden afwezig zijn. Ga voor meer informatie naar:
   - [Voorziening voor verlof en verzuim van werknemers in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in het Dynamics 365 2020 releasewave 2-plan
   - [De verlofkalender van uw team weergeven](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources-documentatie

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a>Configuratieoptie om de lijst Aan mij toegewezen werkitems te positioneren (477004)

Er is nu een nieuwe optie beschikbaar om de lijst **Aan mij toegewezen werkitems** in de rechterkolom van het dashboard te positioneren. Met deze wijziging worden alle werkitems en takenlijsten in hetzelfde gebied weergegeven. Schakel deze functionaliteit in door **Preview - Verbeteringen in werkstroomervaring** in Functiebeheer in te schakelen. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het inschakelen van preview-functies.

Deze functie bevordert ook de werkstroomopties die worden weergegeven in de formulieren voor personeelsacties. Werkstroomopties worden ook boven het sneltabblad Actie weergegeven voor snelle toegang. Ga voor meer informatie naar: 

- [Verbeteringen in de werkstroom voor organisatie- en personeelsbeheer](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) in het Dynamics 365 2020 releasewave 2-abonnement

![Aan mij toegewezen werkitems](./media/hr-workflow-work-items-assigned-to-me.png)

![Snelle toegang tot werkstroomitems](./media/hr-workflow-quick-access.png)

### <a name="leave-and-absence-calendar"></a>Verlof- en verzuimkalender

Deze release bevat aanvullende kalenderopties voor verlof- en afwezigheidskalenders. Zie [Team- en bedrijfsagenda's weergeven](./hr-employee-self-service-calendar.md) voor meer informatie.

## <a name="coming-soon"></a>Binnenkort beschikbaar

### <a name="checklist-entities-included-in-dataverse"></a>Check List-entiteiten opgenomen in Dataverse

Controlelijstentiteiten voor de processen Onboarding, Offboarding, Overdracht en Bedrijfs zijn binnenkort beschikbaar in Dataverse.

### <a name="benefits-management-reason-codes"></a>Redencodes voor vergoedingenbeheer

Redencodes voor vergoedingenbeheer worden binnenkort gecombineerd met bestaande redencodes in Human Resources. Als u redencodes van meer dan 15 tekens hebt gemaakt in Vergoedingenbeheer, moet u de naam van de redencodes in het formulier **Redencodes** wijzigen in een code van maximaal 15 tekens. Nadat u de naam hebt bijgewerkt, wordt de redencode weergegeven onder het bestaande redencodeformulier in Personeelsbeheer. Deze wijziging wordt in de toekomst beschikbaar en heeft geen invloed op bestaande functionaliteit.

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van releasewave 2 van Dynamics 365 Human Resources](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
