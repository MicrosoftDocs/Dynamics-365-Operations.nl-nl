---
title: Nieuwe of gewijzigde functies in Dynamics 365 Human Resources (08 juli 2020)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 8 juli 2020.
author: andreabichsel
manager: tfehr
ms.date: 07/08/2020
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
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9715f332088b7b5340f4252af5f789d226d90ff2
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463593"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-8-2020"></a>Nieuwe of gewijzigde functies in Dynamics 365 Human Resources (8 juli 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 Human Resources. Wijzigingen die van toepassing zijn op buildnummer 8.1.3382. De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in LCS ter referentie.

## <a name="database-logging"></a>Databaseaanmelding

Met databaselogboeken kunt u bepalen welke tabellen en velden moeten worden bewaakt. U kunt hiermee ook bepalen welke gebeurtenissen het bijhouden van wijzigingen moeten activeren. U gebruikt de functies van databaselogboeken om deze wijzigingen in de loop van de tijd weer te geven. Zie [Databaselogboeken configureren en beheren](hr-admin-database-logging.md) voor meer informatie.

## <a name="configure-the-name-of-employee-self-service"></a>De naam van de werknemerselfservice configureren

In de **HR-parameters** kunt u nu de naam van het werkgebied **Selfservice werknemer** wijzigen in **Selfservice**. Zie voor meer informatie [Naam van het werkgebied Selfservice werknemer](hr-employee-self-service-workspace-name.md)

## <a name="benefits-management-open-enrollment-access-outside-of-period"></a>Toegang tot open inschrijving Vergoedingenbeheer buiten periode

Deze release corrigeert een bug waarbij werknemers toegang hebben tot open inschrijving voor vergoedingen buiten de inschrijvingsperiode of zonder een levensgebeurtenis. Daarom moet u bij een demo voor de open inschrijving in Selfservice voor werknemers de open inschrijvingsdatums wijzigen in vandaag (of eerder) om deze toegankelijk te maken. U kunt deze instelling wijzigen onder **Vergoedingenbeheer > Regels en optieperioden**.

## <a name="email-employee-enrollment-confirmation"></a>Bevestiging per e-mail van inschrijving werknemer

U kunt nu een e-mail verzenden naar werknemers nadat ze hun vergoedingenelectie hebben voltooid. U kunt een standaardbericht verzenden of een e-mailsjabloon van de organisatie gebruiken. Deze instellingen zijn te vinden onder **Human Resource-parameters > Vergoedingenbeheer**.

## <a name="canceled-leave-still-appears-in-upcoming-time-off-on-people-workspace-441358"></a>Geannuleerd verlof wordt nog steeds weergegeven als gepland verlof in het werkgebied Personen (441358)

Geannuleerd verlof wordt niet langer weergegeven als gepland verlof op de verlofkaarten in het werkgebied **Personen**.

## <a name="unable-to-use-the-department-entity-property-in-the-positionv2-entity-456486"></a>De eigenschap afdelingsentiteit kan niet worden gebruikt in de PositionV2-entiteit (456486)

U kunt nu een afdeling toevoegen zonder een dubbele relatie te maken.

## <a name="payrollworkerenrolledbenefitdetailentity-should-only-use-calculated-field-for-retirement-plans-459779"></a>PayrollWorkerEnrolledBenefitDetailEntity kan alleen een berekend veld gebruiken voor pensioenregelingen (459779)

Bij het exporteren van de entiteit **PayrollWorkerEnrolledBenefitDetailEntity** wordt door de export bepaald of een berekend veld moet worden gebruikt op basis van een tarieventabel of dat u het veld **ContributionAmountCur** in de archieftabel gebruikt. De logica die door de gegevensentiteit wordt gebruikt, gebruikt de tarieventabel in situaties waarin de toepassing normaal gesproken niet doet. Deze logica zorgt ervoor dat de entiteit wordt geëxporteerd om een nulwaarde voor deze kolom te retourneren, omdat er geen berekeningstarieventabel is en het product niet toestaat dat de klant een waarde opgeeft.
 
## <a name="confusing-translations-in-czech-language-in-personnel-management-and-employee-self-service-400276"></a>Verwarrende vertalingen in Tsjechisch in personeelsbeheer en selfservice voor werknemers (400276)

In deze release zijn de vertalingen gecorrigeerd voor **Adresboek van bedrijf**, **Volgende geregistreerde cursus**, **Functie** en **Positie**.
 
## <a name="the-workcalendaremployment-table-doesnt-have-the-created-and-modified-system-fields-enabled-460171"></a>Voor de tabel WorkCalendarEmployment zijn de gemaakte en gewijzigde systeemvelden niet ingeschakeld (460171)

De gemaakte en gewijzigde systeemvelden zijn nu ingeschakeld in de tabel **WorkCalendarEmployment** in HR.
 
## <a name="null-reference-exception-for-hire-and-add-details-for-future-employee-455475"></a>Uitzondering met null-referentie voor Aanstelling en details toevoegen voor toekomstige werknemer (455475)

In deze release is een fout (null-referentie) gecorrigeerd in de gestroomlijnde werknemersgegevens wanneer u een werknemer aanneemt met behulp van de optie **Aanstelling en details toevoegen**.

## <a name="changes-made-in-the-dataverse-worker-entity-dont-reflect-in-human-resources-455652"></a>Wijzigingen die in de entiteit Dataverse-medewerker zijn aangebracht, zijn niet zichtbaar in Human Resources (455652)

Wijzigingen in de volgende velden in de entiteit **Medewerker** in Dataverse worden nu in Human Resources weergegeven:

- **Werkt thuis**
- **Anciënniteitsdatum**
- **Jubileumdatum**
- **Oorspronkelijke datum indiensttreding**

## <a name="correct-compensation-level-doesnt-default-based-on-the-job-assigned-to-the-position-394136"></a>Het juiste compensatieniveau wordt niet standaard gebaseerd op de taak die is toegewezen aan de positie (394136)

Met deze wijziging wordt het correcte compensatieniveau standaard ingesteld op basis van de records met de **ingangsdatum** voor de **Positiedetails** en de **begindatum** van **toewijzing van het compensatieplan**.

## <a name="in-preview"></a>Preview

## <a name="mandatory-fields"></a>Verplichte velden 

U kunt nu velden verplicht maken met behulp van de aanpassingsmogelijkheden van Human Resources. Voor deze functie zijn **Opgeslagen weergaven** vereist.

## <a name="human-resources-application-in-teams"></a>Human Resources-toepassing in Teams

Werknemers kunnen vrije tijd bekijken en aanvragen in Microsoft Teams. Ze kunnen met een bot werken om verlofaanvragen te maken. Zie [Human resources-app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841) voor meer informatie. 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>DMF-entiteiten (Data Management Framework) voor vergoedingenbeheer
 
Entiteiten voor vergoedingenbeheer worden vrijgegeven. DMF-entiteiten staan het importeren en exporteren van gegevens toe om het configureren van vergoedingenbeheer te vereenvoudigen. Er is een sjabloon voor vergoedingenbeheer beschikbaar voor het verplaatsen van gegevens. De sjabloon exporteert en importeert de gegevens op volgorde om gegevensafhankelijkheden te behouden.

## <a name="buy-and-sell-leave"></a>Verlof inkopen en verkopen 

Sommige organisaties bieden een werknemers de mogelijkheid om hun verlof te kopen of verkopen. Dit proces wordt vaak handmatig beheerd. Deze functie automatiseert het beheer van beleidsregels en aanvragen voor de HR-afdeling. Het beheerproces voor verlof wordt gestroomlijnd en fouten worden geëlimineerd. Ga voor meer informatie naar:

- [Beleid voor verlof inkopen/verkopen beheren](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Verlof inkopen en verkopen](hr-employee-self-service-buy-sell-leave.md)

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

## <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF-entiteit beschikbaar voor opschorten van toerekeningen 

Een DMF-entiteit is nu beschikbaar voor opschorten van toerekeningen.

## <a name="coming-soon"></a>Binnenkort beschikbaar

## <a name="checklist-entities-included-in-dataverse"></a>Check List-entiteiten opgenomen in Dataverse

Controlelijstentiteiten voor de processen Onboarding, Offboarding, Overdracht en Bedrijfs zijn binnenkort beschikbaar in Dataverse.

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van releasewave 2 van Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]