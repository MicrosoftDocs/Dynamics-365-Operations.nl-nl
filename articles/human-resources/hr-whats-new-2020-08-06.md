---
title: Nieuwe of gewijzigde functies in Dynamics 365 Human Resources (06 augustus 2020)
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 06 augustus 2020.
author: andreabichsel
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-08-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 07aeecaeb6605ab48c0ae9c41c95939fbc706a02
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070107"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-06-2020"></a>Nieuwe of gewijzigde functies in Dynamics 365 Human Resources (06 augustus 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



In dit artikel worden de functies beschreven die in Dynamics 365 Human Resources nieuw of gewijzigd zijn. Wijzigingen die van toepassing zijn op buildnummer 8.1.3444. De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in LCS ter referentie.

## <a name="platform-update-1001236-is-now-available"></a>Platform update 10.0.12(36) is nu beschikbaar

Zie voor meer informatie [Platformupdates voor versie 10.0.12 van apps voor financiën en bedrijfsactiviteiten (augustus 2020)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-10-0-12.md).

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>DMF-entiteiten (framework voor gegevensbeheer) voor vergoedingenbeheer
 
Entiteiten voor vergoedingenbeheer worden vrijgegeven. DMF-entiteiten staan het importeren en exporteren van gegevens toe om het configureren van vergoedingenbeheer te vereenvoudigen. Er is een sjabloon voor vergoedingenbeheer beschikbaar voor het verplaatsen van gegevens. De sjabloon exporteert en importeert de gegevens op volgorde om gegevensafhankelijkheden te behouden. Ga voor meer informatie naar:

- [DMF-entiteitsondersteuning](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/dmf-entity-support) in het Dynamics 365 2020 releasewave 1-plan
- [Overzicht van Gegevensbeheer](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md)


## <a name="claire-creates-a-workflow-for-buying-and-selling-leave-requests-446557"></a>Claire maakt een werkstroom voor het kopen en verkopen van verlofaanvragen (446557)

Ga voor meer informatie naar:

- [Toestaan dat werknemers verlof kopen en verkopen](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave) in het Dynamics 365 2020 releasewave 2-plan
- [Beleid voor verlof inkopen/verkopen beheren](./hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Verlof inkopen en verkopen](./hr-employee-self-service-buy-sell-leave.md)


## <a name="worker-postal-addresses-v2-entity-has-access-across-legal-entities-with-restricted-access-459126"></a>Postadressen van werknemer v2-entiteit heeft toegang voor rechtspersonen met beperkte toegang (459126)

Met deze wijziging wordt de entiteit **Postadres van werknemer v2** beperkt op basis van de toegang van de rechtspersoon die aan de gebruiker is gegeven.

## <a name="workflow-email-hyperlink-fails-to-open-relevant-reviews-437398"></a>E-mail met hyperlink naar werkstroom kan geen relevante beoordelingen openen (437398)

Wanneer u de tijdelijke aanduiding gebruikt om een prestatiebeoordeling te openen in de revisiewerkstroom, wordt nu de geselecteerde record geopend via de hyperlink die in het e-mailbericht is gegenereerd.

## <a name="new-entities-for-buying-and-selling-leave-473180"></a>Nieuwe entiteiten voor verlof kopen en verkopen (473180)

De entiteiten van het framework voor gegevensbeheer zijn nu beschikbaar voor verlof kopen en verkopen. Zie [Overzicht van Gegevensbeheer](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md) voor meer informatie.

## <a name="when-viewing-record-information-and-using-advanced-filters-a-user-could-gain-access-to-other-employees-records-472490"></a>Bij het weergeven van recordgegevens en het gebruik van geavanceerde filters kan een gebruiker toegang krijgen tot de records van andere werknemers (472490)

Bij deze wijziging hebben gebruikers van de werknemerselfservice alleen toegang tot hun eigen records. Als u recordgegevens weergeeft terwijl u de filteroptie wijzigt, worden er geen extra gegevens meer weergegeven.

## <a name="personnel-management-analytics-include-exited-worker-records-382893"></a>De analyses voor personeelsbeheer omvatten afgesloten werknemerregistraties (382893)

Met deze versie bevatten de analyses voor personeelsbeheer nu alleen actieve werknemers. 
 
## <a name="unable-to-process-a-merit-increase-for-an-employee-473125"></a>Kan een salarisverhoging voor een werknemer niet verwerken (473125)

Met deze wijziging kunt u salarisverhogingen invoeren wanneer u de ingangsdatum voor de nieuwe salarisverhoging wijzigt.

## <a name="review-workflow-can-be-started-more-than-once-467541"></a>De revisiewerkstroom kan meerdere keren worden gestart (467541)

Met deze wijziging kunt u de werkstroom voor prestatiebeoordelingen slechts eenmaal starten. De status voor de manager geeft de optie om de controle te starten niet langer weer.

## <a name="leave-request-work-flow-ends-in-error-when-canceling-an-approved-leave-request-472063"></a>Werkstroom voor verlofaanvraag eindigt met een fout bij het annuleren van een goedgekeurde verlofaanvraag (472063)

Wanneer u in deze versie een goedgekeurde verlofaanvraag annuleert, blijft de status van de aanvraag niet langer goedgekeurd en wordt de werkstroom voortgezet.

## <a name="system-suggests-exited-workers-when-creating-a-new-review-form-the-template-460624"></a>Er worden vertrokken werknemers voorgesteld wanneer een nieuwe revisie wordt gemaakt op basis van de sjabloon (460624)

Met deze wijziging zijn de vertrokken werknemers niet langer beschikbaar wanneer u nieuwe beoordelingen maakt op basis van een sjabloon. U kunt geen werknemerbeoordelingen maken die buiten de datums van hun dienstverband vallen.

## <a name="position-hierarchy-circular-reference-detection-415879"></a>Detectie van circulaire verwijzingen in positiehiërarchie (415879)

Met deze wijziging wordt de detectie van circulaire verwijzingen in de positiehiërarchie beperkt tot één punt in de tijd. U kunt de detectie van circulaire verwijzingen voor verschillende datums uitvoeren om na te gaan of de rapportstructuur geen circulaire verwijzingen bevat.

## <a name="buy-and-sell-leave"></a>Verlof inkopen en verkopen 

Sommige organisaties bieden een werknemers de mogelijkheid om hun verlof te kopen of verkopen. Dit proces wordt vaak handmatig beheerd. Deze functie automatiseert het beheer van beleidsregels en aanvragen voor de HR-afdeling. Het beheerproces voor verlof wordt gestroomlijnd en fouten worden geëlimineerd. Ga voor meer informatie naar:

- [Toestaan dat werknemers verlof kopen en verkopen](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave) in het Dynamics 365 2020 releasewave 2-plan
- [Beleid voor verlof inkopen/verkopen beheren](./hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Verlof inkopen en verkopen](./hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Toerekening van verlof voor één bedrijf of één plan

Klanten kunnen toerekeningen verwerken voor één bedrijf of voor één verlof- en verzuimplan. Dit schept duidelijkheid voor het toerekenproces voor klanten met verschillende regels voor verlof- of verzuimtoerekening. Zie [Verlof per bedrijf of per verlofplan toerekenen](hr-leave-and-absence-accrue.md) voor meer informatie.

## <a name="add-attachments-to-time-off-requests"></a>Bijlagen toevoegen aan verlofaanvraagen

De mogelijkheid om bijlagen toe te voegen aan goedgekeurde verlofaanvragen is van cruciaal belang in de huidige COVID-19-omgeving. Werknemers kunnen deze bijlagen nu toevoegen. Ze hebben ook meer inzicht in de manier waarop updates worden uitgevoerd in verlofaanvragen. Zie [Een bijlage toevoegen aan een bestaande aanvraag](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request) voor meer informatie.

## <a name="add-reason-code-to-accrual-suspensions"></a>Redencode toevoegen voor opschorten van toerekeningen 

Er zijn redencodes toegevoegd voor het opschorten van de toerekening.

## <a name="carry-forward-rules"></a>Regels voor transporteren 

U kunt een verloftype voor transporteren opgeven voor verlofsaldi waarvoor transportcorrecties worden overgeboekt. Als een werknemer bijvoorbeeld 10 dagen transporteert, kunt u voor deze 10 dagen een ander verloftype kiezen. Zie [Verlof- en verzuimtypen configureren](hr-leave-and-absence-types.md) voor meer informatie.

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>Toerekening voor verlof voor opgegeven verloftypen opschorten

In deze versie kunt u een regel maken voor het opschorten van verloftoerekeningen voor werknemers met verlofaanvragen voor onbetaald verlof. Onbetaald verlof kan een type zijn, maar dat hoeft niet. U kunt elk verlof uitstellen op basis van een ander verloftype.

## <a name="in-preview"></a>Preview

### <a name="mandatory-fields"></a>Verplichte velden

U kunt velden verplicht maken met behulp van de aanpassingsmogelijkheden van Human Resources. Voor deze functie zijn **Opgeslagen weergaven** vereist. Voor meer informatie over opgeslagen weergaven zie:

- [Opgeslagen weergaven - algemene beschikbaarheid](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) in het Dynamics 365 2020 releasewave 2-plan
- [Formulieren maken waarin opgeslagen weergaven volledig worden gebruikt](../fin-ops-core/dev-itpro/user-interface/understanding-saved-views.md)

### <a name="human-resources-application-in-teams"></a>Human Resources-toepassing in Teams

Werknemers kunnen vrije tijd bekijken en aanvragen in Microsoft Teams. Ze kunnen met een bot werken om verlofaanvragen te maken. Ga voor meer informatie naar:

- [Voorziening voor verlof en verzuim van werknemers in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in het Dynamics 365 2020 releasewave 1-plan
- [Human Resources-app in Teams](./hr-admin-teams-leave-app.md)

### <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF-entiteit beschikbaar voor opschorten van toerekeningen

Een DMF-entiteit is nu beschikbaar voor opschorten van toerekeningen.

## <a name="coming-soon"></a>Binnenkort beschikbaar

## <a name="checklist-entities-included-in-dataverse"></a>Check List-entiteiten opgenomen in Dataverse

Controlelijstentiteiten voor de processen Onboarding, Offboarding, Overdracht en Bedrijfs zijn binnenkort beschikbaar in Dataverse.

## <a name="known-issues"></a>Bekende problemen

In het werkgebied voor **Functiebeheer** kunnen functies worden weergegeven die zijn uitgeschakeld als preview-functies wanneer ze algemeen beschikbaar zijn. Hieronder ziet u een lijst met algemeen beschikbare functies waarvoor een onjuiste status wordt weergegeven. 

1.  Vergoedingenbeheer
2.  Casebeheer
3.  Databaselogboeken (controle)
4.  Verloftoerekening voor één bedrijf of één plan
5.  Uitstel van toerekening van verlof en verzuim
6.  Redencode en opmerking voor saldocorrectie
7.  Verlof inkopen en verkopen
8.  Verlof- en verzuimkalender
9.  Transportregels voor verlof
10. Controleren van verloftoerekeningen
11. Verwijderen van verloftoerekeningen
12. Afronding voor verloftoerekening
13. Meerdere verloftypen configureren voor één verlofplan
14. Verbeteringen voor vrije tijd bijwerken
15. De FTE voor toerekeningen van een werknemer gebruiken
16. Compensatieweergave voor meerdere bedrijven
17. Prestatiebeoordelingen afdrukken
18. Feestdagcorrecties voor verloftoerekening

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van releasewave 2 van Dynamics 365 Human Resources](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
