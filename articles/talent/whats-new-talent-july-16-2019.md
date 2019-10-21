---
title: Nieuwe of gewijzigde functies in Dynamics 365 Talent (16 juli 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 07/16/2019
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
ms.search.validFrom: 2019-07-16
ms.dyn365.ops.version: Talent
ms.openlocfilehash: fd70b29089a4bf05c8fa9e3591fdb22383ea0cdc
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009711"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-16-2019"></a>Nieuwe of gewijzigde functies in Dynamics 365 Talent (16 juli 2019)

[!include [banner](includes/banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Wijzigingen in Attract
Deze versie bevat kleine correcties voor Dynamics 365 Talent: Attract.

### <a name="coming-soon-in-attract"></a>Binnenkort in Attract
#### <a name="job-approvals-appear-on-the-home-page"></a>Functiegoedkeuringen worden weergegeven op de startpagina

Goedkeuringen worden weergegeven in de sectie **Goedkeuringen** op het dashboard. Fiatteurs kunnen hun goedkeuringen controleren onder **Aan u toegewezen**, waar de taak-ID, functietitel, andere fiatteurs en de toewijzingsdatum worden weergegeven. Gebruikers die een functie ter goedkeuring indienen, kunnen hun functies controleren onder **Aangevraagd door u**, waar de fiatteurs worden weergegeven die de ingediende functie nog moeten goedkeuren.

## <a name="changes-in-onboard"></a>Wijzigingen in Onboard
Deze versie bevat kleine correcties voor Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Wijzigingen in Core HR
Wijzigingen die worden beschreven in deze sectie, gelden voor buildnummer 8.1.2390.

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>Common Data Service-entiteiten die nu aangepaste velden ondersteunen

- BusinessProcessCalendar                     
- BusinessProcessGroupAssignment         
- BusinessProcessStage                          
- BusinessProcessTemplateHeader          
- BusinessProcessTemplateTask            
- HcmBenefitOption                              
- HcmBenefitType                                  
- HcmCompensationGrid                            
- HcmCompensationLevel                          
- HcmCompensationPayFrequency                 
- HcmCompensationReferencePointSetup        
- HcmCompensationReferencePointSetupLine 
- HcmCompensationRegion                     
- HcmCompFixedPlanTable                     
- HcmEmployment                                
- HcmEthnicOrigin                                
- HcmFixedCompensationEvent                 
- HcmJob                                           
- HcmJobFunction
- HcmJobType
- HcmLanguageCode
- HcmPayrollCalculationFrequency
- HcmPosition
- HcmPositionType
- HcmSkillType
- HcmVeteranStatus
- HcmWorkCalendarHoliday
- HcmWorkCalendarHolidayLine
- HcmWorker
- HcmWorkerPersonalDetail
- LeaveType
- OMDepartment
- OMLegalEntity
- PayCycle
- PayPeriod
- PayrollBenefitCalculationRate
- PayrollBenefitCalculationRateDetail
- PayrollEarningCode

### <a name="unable-to-see-goals-and-reviews-in-manager-self-service"></a>Doelstellingen en beoordelingen worden niet weergegeven in de selfservice-functionaliteit voor managers

Door de wijzigingen van deze week kunnen doelstellingen en beoordelingen nu door hogere managers worden weergegeven en bewerkt in de selfservice-functionaliteit voor managers.

### <a name="goal-form-cannot-be-closed-after-a-user-edits-any-goal-field"></a>Formulier voor doelstellingen kan niet worden gesloten nadat een gebruiker een veld voor doelstellingen heeft bewerkt

In deze release is een probleem gecorrigeerd waarbij het formulier voor doelstellingen niet wordt gesloten wanneer u **Sluiten** selecteert.

### <a name="creating-new-goals-and-saving-displays-error"></a>Wanneer na het maken van nieuwe doelstellingen wordt opgeslagen, wordt er een fout weergegeven

In deze release is een probleem bij het opslaan van doelstellingen in de selfservice-functionaliteit voor werknemer en manager gecorrigeerd.

### <a name="unable-to-add-a-field-to-position-details"></a>Kan geen veld toevoegen aan positiedetails 

In deze release worden aangepaste velden nu ondersteund voor positiedetails.
 
### <a name="unable-to-set-up-expiring-date-on-the-earning-code-through-data-management"></a>Kan geen vervaldatum voor de inkomstencode instellen via gegevensbeheer

Door wijzigingen kunt u nu wel vervaldatums instellen voor inkomstencodes in gegevensbeheer.

### <a name="new-custom-fields-dont-sync-quickly-enough"></a>Nieuwe aangepaste velden worden niet snel genoeg gesynchroniseerd

De prestaties van de synchronisatie van aangepaste velden naar Common Data Service zijn verbeterd met de release van deze week.

### <a name="entity-export-to-database-jobs-fail-with-error-message-format-of-the-initialization-string-does-not-conform-to-specification-starting-at-index-0"></a>Taken voor het exporteren van entiteiten naar de database mislukken met de fout: Indeling van de initialisatietekenreeks voldoet niet aan de specificatie die start bij index 0.

In deze release is het probleem opgelost waarbij databasebatchtaken mislukken. Handmatig bijwerken:

1. Ga naar **Gegevensbeheer**.
2. Selecteer **Entiteit naar database exporteren configureren**.
3. Voer de verbindingstekenreeks voor de doeldatabase opnieuw in en selecteer **Opslaan**.

### <a name="smtp-email-configuration-suddenly-fails-with-error-message-the-smtp-server-requires-a-secure-connection-or-the-client-was-not-authenticated"></a>Configuratie van SMTP-e-mail mislukt plotseling met het foutbericht: Voor de SMTP-server is een beveiligde verbinding vereist of de client is niet geverifieerd.

In deze release is een SMTP-e-mailconfiguratie die plotseling uitvalt gecorrigeerd. Handmatig bijwerken:

1. Ga naar **Systeembeheer**.
2. Selecteer **E-mailparameters**.
3. Selecteer **SMTP-instellingen**. 
4. Geef de gebruikersnaam en het wachtwoord voor de SMTP-server opnieuw op en selecteer **Opslaan**.

## <a name="in-preview"></a>Preview

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Preview-functies zijn alleen ingeschakeld in sandbox-exemplaren

Wanneer u een nieuw exemplaar van Talent inricht, kunt u opgeven of het exemplaartype **Productie** of **Sandbox** is. In exemplaren van het type **Sandbox** kunnen nieuwe functies vroegtijdig worden getest. Alle bestaande exemplaren van Talent worden bijgewerkt naar het exemplaartype **Productie**. Als u wilt dat een van de bestaande exemplaren wordt bijgewerkt naar het exemplaartype **Sandbox**, neemt u contact op met de [ondersteuning](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) om de wijzigingsaanvraag te initiëren.

Zie [Talent inrichten](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) voor meer informatie over hoe wijzigingen worden gepubliceerd.

### <a name="restrict-leave-types-in-time-off-requests"></a>Verloftypen in verlofaanvragen beperken

Organisaties kunnen veel verschillende verloftypen aanbieden aan werknemers. Sommige verloftypen zijn mogelijk niet geschikt voor werknemers . Deze verloftypen kunnen in plaats daarvan door HR worden beheerd. In deze versie kunt u configureren voor welke typen verlof werknemers verlofaanvragen kunnen indienen. 

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>Informatie over prestaties voor directe en indirecte ondergeschikten in de selfservice-functionaliteit voor managers weergeven

Met een nieuwe optie kunnen managers de prestaties van hun directe en indirecte ondergeschikten weergeven. Op dit moment kunnen lijnmanagers prestatiedoelstellingen toewijzen en bijwerken, en nieuwe beoordelingen uitgeven. Bovendien kunnen directe leidinggevenden en hun werknemers prestatiejournalen onderhouden en bijwerken om ervoor te zorgen dat het proces voor prestatiebeoordelingen soepel verloopt. Wanneer deze wijziging is geïmplementeerd, kunnen managers prestatiegerelateerde gegevens weergeven en beheren voor indirecte en directe ondergeschikten.
