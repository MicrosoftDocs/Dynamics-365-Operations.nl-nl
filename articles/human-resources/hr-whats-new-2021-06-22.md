---
title: Nieuwe of gewijzigde functies in Dynamics 365 Human Resources 22 juni 2021
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 22 juni 2021.
author: marcelbf
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c2f362e71832d6f7b17e06ad98142019ced4df14
ms.sourcegitcommit: baad2723291774f610324a8054fc14abf3287fe1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/14/2021
ms.locfileid: "6560069"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-22-2021"></a>Nieuwe of gewijzigde functies in Dynamics 365 Human Resources 22 juni 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn of die binnenkort worden vrijgegeven in Dynamics 365 Human Resources.

Zie [Updateproces](hr-admin-setup-update-process.md) voor meer informatie over het updateproces en de planning.

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) voor meer informatie over nieuwe functies en de verwachte algemene beschikbaarheidsdatums ervan.

## <a name="in-this-release"></a>In deze versie

Deze versie bevat de volgende nieuwe functies en correcties. Wijzigingen die van toepassing zijn op buildnummer 8.1.4258.

### <a name="new-features"></a>Nieuwe functies

De volgende functie zijn algemeen beschikbaar in deze release.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Functie om gebruikers zonder dienstverband te informeren: wanneer de geavanceerde toegang is ingeschakeld en de functie **Alle medewerkers zonder dienstverband weergeven** is uitgeschakeld in Functiebeheer, wordt er een banner weergegeven in het formulier Alle medewerkers zonder dienstverband. De banner geeft de gebruiker aanwijzingen om de functie **Alle medewerkers zonder dienstverband weergeven** in te schakelen. | Niet van toepassing| [Medewerkers zonder dienstverband](/dynamics365/human-resources/hr-personnel-workers-without-employment)|
| Ondersteuning voor aangepaste velden in geschiktheidsregels voor Vergoedingenbeheer | [Ondersteuning voor aangepaste velden voor verwerking van geschiktheid](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |[Geschiktheidsregels configureren](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules) |
| Controleren van toerekeningstransacties voor verlof | Niet van toepassing | [Controleren van toerekeningstransacties voor verlof](hr-leave-and-absence-accrue.md)|
| Verbeteringen voor werken in de workflows voor verlof en verzuim | [Verbeteringen voor werken in de workflows voor verlof en verzuim](https://go.microsoft.com/fwlink/?linkid=2147528) | [Verlof aanvragen](hr-employee-self-service-request-time-off.md)|

### <a name="bug-fixes"></a>Correcties

Deze versie bevat de volgende correcties.

> [!NOTE]
> Ons doel is om deze informatie zo snel mogelijk bij u te krijgen. Mogelijk wordt dit onderwerp gewijzigd om correcties op te nemen die in de build zijn gemaakt nadat dit onderwerp oorspronkelijk werd gepubliceerd.

| Probleemnummer | Probleem |  Beschrijving |
| --- | --- | --- |
| 583052 | Gebruikers die feedback ontvangen, kunnen de ontvangen feedback bewerken | Wanneer een werknemer die feedback ontvangt op een prestatiejournaal **Externe koppeling toevoegen** selecteert, kan het formulier worden bewerkt, zodat de werknemer de ontvangen prestatiefeedback kan bewerken. |
| 522281 | Als u het aantal werknemers in de compensatiestructuur in Compensatiebeheer selecteert, resulteert dit in onjuiste resultaten| Wanneer er vanuit de compensatiewerkruimte wordt ingezoomd op de compensatieplannen, wordt nu het juiste aantal werknemers weergegeven. |
| 580683 | Gebruikers die aan de rollen Werknemer en Manager zijn toegewezen, kunnen geen notities toevoegen of een prestatiejournaal bijwerken | Gebruikers die aan de rollen Werknemer en Manager zijn toegewezen, kunnen geen notities toevoegen of een prestatiejournaal bijwerken. De gebruiker ontvangt het foutbericht: 'Kan geen record maken in prestatiejournaalinvoer (HcmPerfJournal). Machtiging voor beveiligingsbeleid geweigerd.' |
| 583077 | De geboortedatum van een werknemer in de verlof- en verzuimkalender van het bedrijf is een onjuiste datum. | Gebruikers kunnen de juiste geboortedatum van de werknemers in de verlof- en verzuimkalender van het bedrijf bekijken. |
| 586996 | De verlofweergavefunctie voor het hele bedrijf zorgt ervoor dat saldi leeg zijn wanneer de toegang tot één bedrijf is beperkt | Gebruikers kunnen de toekomstige verlofsaldi van de werknemer correct weergeven wanneer de verlofweergave voor het hele bedrijf is ingeschakeld. |
| 581014 | Als u de verlof- en verzuimweergave voor het hele bedrijf inschakelt, wordt er bij het bekijken van toekomstige saldi een foutmelding weergegeven | Fouten zijn hersteld als gebruikers de toekomstige verlofsaldi bekeken terwijl de verlofweergave voor het hele bedrijf was ingeschakeld. |
| 509404 | Analyses van personeelsbezetting per afdeling waarbij geen rekening wordt gehouden met de verplaatsing van werknemers tussen afdelingen. | Wanneer een werknemer van de ene afdeling naar de andere gaat, geven de personeelsbezettingsgegevens van de afdeling niet de oude afdeling weer waarvandaan de werknemer is gekomen als het positiedetail in het huidige jaar is vervallen. |
| 584851 | Vergoedingskredietregel 'Geen' geeft nooit krediet |De vergoedingskredietregel 'Geen' heeft tot gevolg gehad dat werknemers nul kredieten ontvangen voor de vergoedingsperiode, ongeacht wanneer ze zijn aangenomen. Dit is opgelost, zodat een werknemer volledige kredietvergoeding moet ontvangen als de werknemer vóór het begin van de vergoedingsperiode werd aangenomen en geen als hij of zij na het begin van de periode is aangenomen. |
| 584897 | Als u de functie 'Externe basisfunctionaliteit gebruiken' dupliceert, resulteert dit in een fout | Bij een poging om de functie 'Externe basisfunctionaliteit gebruiken' te dupliceren, heeft de gebruiker de fout 'Kan object niet vinden met id UserDefinedAppHostDialogView' ontvangen. |
| 575692 | Verlof en verzuim opbouwen is niet beschikbaar voor aankomende werknemers | Verlof- en verzuimopbouw kan worden uitgevoerd voor werknemers die in de toekomst zijn aangenomen wanneer **Gestroomlijnde invoer voor werknemers** is ingeschakeld. |
| 580110 | Wanneer u een bedrijf toevoegt aan de integratie van de salarisadministratie, wordt de integratie opnieuw ingesteld, omdat alle entiteiten worden gebruikt, zelfs als de optie is ingesteld op het niet vernieuwen van het project. | Als een klant entiteiten heeft verwijderd of het gegevensproject voor integratie van de salarisadministratie heeft gewijzigd en de optie is ingesteld om te voorkomen dat het project automatisch wordt vernieuwd, wordt de instelling genegeerd en wordt het project vernieuwd door een nieuw bedrijf aan de integratie toe te voegen.  |
| 584518 |Prestatieprobleem voor verwerking van inschrijven voor vergoedingen | Deze bug heeft prestatieproblemen in het verouderde inschrijvingsproces voor vergoedingen opgelost. |

## <a name="in-preview"></a>Preview

Van de volgende nieuwe functies kan een voorbeeld worden bekeken. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het in- en uitschakelen van functies.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Werkgebied voor vergoedingenbeheer | [Werkruimte Vergoedingenbeheer (preview)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Werkgebied voor vergoedingenbeheer](hr-benefits-management-workspace.md) |
| Vereenvoudigde integratie van de salarisadministratie inschakelen (API's voor integratie van de salarisadministratie) | [Vereenvoudigde integratie met externe salarisadministrateurs inschakelen](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [API voor integratie van salarisadministratie](hr-admin-integration-payroll-api-introduction.md)|


## <a name="coming-soon"></a>Binnenkort beschikbaar

| Functie | Gegevens |
| --- | --- |
| Platformupdate 10.0.19 (43) | Platformupdate 10.0.19 is gepland voor de uitrol met de volgende servicerelease op 28 juni 2021. Zie [Platformupdates voor versie 10.0.19 van Finance and Operations-apps (juni 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19) voor meer informatie. |
|  Dienstjarenweergave in-/uitschakelen | Met deze functie kunt u verschillende datums gebruiken om de dienstjaren te berekenen die worden weergegeven in het formulier **Gestroomlijnde invoer werknemer** en in het formulier **Personen**.  Dit is beschikbaar in de parameters van Human Resources. |
|  Verlof laten beheren door een verzuimmanager | [Verlof laten beheren door een verzuimmanager](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) |
|  Mandaatbijlagen voor specifieke verloftypen | Met deze functie kunnen beheerders vereisen dat bijlagen moeten worden toegevoegd bij het indienen van verlofaanvragen voor specifieke verloftypen. |
|  Verlofeenheden per verloftype configureren | Met deze functie kunnen beheerders verlofeenheden (uren of dagen) configureren voor elk verloftype.  |
| Toestaan dat werknemers kunnen worden gemarkeerd als gereed voor betalen | [Toestaan dat werknemers kunnen worden gemarkeerd als gereed voor betalen](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) |

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) voor een volledige lijst met geplande functies en de bijbehorende geplande versies.

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van Dynamics 365 Human Resources 2021 release wave 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
