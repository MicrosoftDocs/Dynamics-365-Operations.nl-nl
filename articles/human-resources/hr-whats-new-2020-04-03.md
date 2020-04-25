---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (3 april 2020)
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 04/03/2020
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
ms.author: dkrame
ms.search.validFrom: 2020-04-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ab732853a2c37338d8003c5f8911c011aa8ffc60
ms.sourcegitcommit: 724f5b400a4e7c385da9d8b22db416ebc3623b93
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/03/2020
ms.locfileid: "3225146"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-3-2020"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (3 april 2020)

In dit artikel worden de functies beschreven die in Dynamics 365 Human Resources nieuw of gewijzigd zijn. Wijzigingen die van toepassing zijn op buildnummer 8.1.3111. De getallen tussen haakjes in sommige koppen verwijzen ter referentie naar ondersteuningsnummers in Lifecycle Services (LCS).

## <a name="features-that-are-generally-available-the-week-of-april-6"></a>Functies die in het algemeen beschikbaar zijn in de week van 6 april

- **Functies voor verlof en verzuim**: zie [Overzicht van verlof en verzuim](hr-leave-and-absence-overview.md) voor meer informatie.

- **Functies van Vergoedingenbeheer**: zie [Overzicht van Vergoedingenbeheer](hr-benefits-management-overview.md) voor meer informatie.

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>De limieten van Human Resources-omgevingen zijn nu gebaseerd op bijgewerkte licentie (394595)

De limiet aan het aantal omgevingen per project in Lifecycle Services (LCS) is gewijzigd. De vorige limiet was twee omgevingen. De limiet aan het aantal productie- en sandbox-omgevingen dat u kunt maken voor Human Resources in LCS is nu gebaseerd op bijgewerkte licenties. U kunt nu zoveel omgevingen maken als u nodig hebt per LCS-project, afhankelijk van het aantal aangeschafte licenties. Met de nieuwe licentie, die op 1 februari 2020 is bijgewerkt, kunnen klanten aanvullende omgevingen kopen. Zie de [licentiehandleiding voor Dynamics 365](https://dynamics.microsoft.com/pricing/#HumanResources) voor meer informatie over licentievereisten voor aanvullende omgevingen.
 
## <a name="error-when-trying-to-delete-a-questionnaire-428603"></a>Fout bij het verwijderen van een vragenlijst (428603)

De update van deze week corrigeert een probleem waarbij de volgende fout wordt weergegeven wanneer u een vragenlijst probeert te verwijderen:

Er is een ongelijk X++ TTSBEGIN/TTSCOMMIT-paar gedetecteerd.

## <a name="performance-journal-and-professional-certificates-security-issue-428499"></a>Beveiligingsprobleem met prestatiejournaal en professionele certificaten (428499)

Deze wijziging beperkt de zichtbaarheid van zowel prestatiejournalen als professionele certificaten op basis van de bedrijven waartoe ze toegang hebben. 

## <a name="the-abbreviation-for-quebec-and-manitoba-387510"></a>De afkorting voor Quebec en Manitoba (387510)

De begingegevens zijn bijgewerkt om de juiste afkorting weer te geven voor Manitoba en Quebec.

## <a name="new-entities-available-in-data-management-framework"></a>Nieuwe entiteiten beschikbaar in Data Management Framework

De volgende entiteiten zijn nu beschikbaar. Als deze entiteiten niet worden weergegeven in de lijst met entiteiten, gebruikt u de optie **Entiteiten vernieuwen** in **Raamwerkparameters >Entiteitsinstellingen > Entiteitslijst vernieuwen**.

 - Verlof- en verzuimbanktransactie V2
 - Inschrijving voor verlof en verzuim V2
 - Niveau van verlof- en verzuimplan V2
 - Verlof- en verzuimplan V2

## <a name="common-data-service-solution-is-now-available-with-the-following-changes"></a>Common Data Service-oplossing is nu beschikbaar met de volgende wijzigingen:

| Omschrijving | Wisselgeld |
| --- | --- |
| Wijzigingen in de entiteit **Functie/positie** | <ul><li>**Compensatieregio** toegevoegd</li>|
| Entiteit **Dimensie van taakpositie** toegevoegd | <ul><li>**Financiële dimensies** toegevoegd</li>
| Wijzigingen in entiteit **Medewerker** | <ul><li>**Naamsvolgorde** toegevoegd</li><li>**Werkt thuis** toegevoegd</li><li>**Taal** toegevoegd</li><li>**Anciënniteitsdatum** toegevoegd</li><li>**Jubileumdatum** toegevoegd</li><li>**Oorspronkelijke datum indiensttreding** toegevoegd</li></ul> |
| Wijzigingen in entiteit **Aanstelling** | <ul><li>**Financiële dimensies** toegevoegd</li><li>**Reden van ontslag** toegevoegd</li><li>**Ontslagdatum** gewijzigd van **Overgangsdatum**</li><li>**Proeftijddatum** toegevoegd</li></ul> |
| Wijzigingen in entiteit **Adres medewerker** | <ul><li>**Adres** toegevoegd</li><li>**Adresregel 1**, **Adresregel 2** en **Adresregel 3** gemarkeerd voor afschaffing</li></ul> |
| Entiteiten voor nieuwe instellingen voor variabele compensatie | <ul><li>**Type variabelecompensatieplan**</li><li>**Variabelecompensatieplan**</li><li>**Vestigingsregels**</li><li>**Niveau variabelecompensatieplan**</li></ul> |
| Nieuwe entiteit **Medewerkerkalender aanstelling** | <ul><li>Entiteit **Werkkalender** toegevoegd</li></ul> |
| Nieuwe entiteit **Salarispositiedetail** | <ul><li>**Salarispositiedetail** toegevoegd</li></ul> |
| Nieuwe entiteit **Titel** | <ul><li>**Titel** toegevoegd</li></ul>De nieuwe entiteit **Titel** wordt opgenomen in Common Data Service maar er wordt nu niet naar verwezen in de entiteiten **Taakpositie** of **Functie**. |

> [!NOTE]
> Financiële dimensies voor zowel posities als aanstellingen zorgen voor integratie in één richting voor updates van Human Resources naar Common Data Service. Voor updates van financiële dimensies wordt Common Data Service momenteel niet gesynchroniseerd met Human Resources.

In de komende weken zijn deze entiteitswijzigingen beschikbaar in alle omgevingen. Handmatig de meest recente Common Data Service-oplossing voor Human Resources installeren:

1.  Ga naar het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com).

2.  Selecteer **Omgevingen**.

3.  Zoek de omgeving die u wilt bijwerken. De omgeving moet overeenkomen met **Omgevingsnaam**  in de sectie **Common Data Service-gegevens** in het formulier **Info** in Human Resources.

4.  Selecteer de omgeving waarin u de omgevingsdetails wilt weergeven.

5.  Selecteer **Oplossingen beheren** op de actiebalk bovenaan. Er wordt een nieuw browservenster geopend waarin u naar **Dynamics 365-beheercentrum** gaat in de context van uw omgeving.

6.  Selecteer in de lijst **Oplossing** **Dynamics 365 Human Resources verankeren**.

7.  Selecteer **Upgraden** om de meest recente oplossing toe te passen.

## <a name="in-preview"></a>Preview

## <a name="leave-suspension"></a>Verlof opschorten

U kunt verlof en verzuim in Human Resources opschorten voor een werknemer. Als u het verlof opschort, wordt het toegerekende verlof stopgezet voor de geselecteerde verloftypen. Als het opschorten plaatsvindt nadat een toerekening is verwerkt, wordt door het onderbreken van het verlof een evenredige correctie in het verlof van de werknemer gemaakt. Zie [Verlof opschorten](hr-leave-and-absence-suspend-leave.md) voor meer informatie.

## <a name="carry-forward-rules"></a>Regels voor transporteren

U kunt een verloftype voor transporteren opgeven voor verlofsaldi waarvoor transportcorrecties worden overgeboekt. Als een werknemer bijvoorbeeld 10 dagen transporteert, kunt u voor deze 10 dagen een ander verloftype kiezen. Zie [Verlof- en verzuimtypen configureren](hr-leave-and-absence-types.md) voor meer informatie.

## <a name="coming-soon"></a>Binnenkort beschikbaar

## <a name="new-production-release-cadence"></a>Nieuwe tempo voor productiereleases

Vanaf april wordt het releasetempo voor Human Resources van wekelijks in tweewekelijks gewijzigd. De service-updates in alle regio's volgt nu een implementatie per twee weken om een aanpassing met veilige implementatiemethoden en het bijhouden van hoge standaarden voor stabiliteit en betrouwbaarheid in de service te garanderen. Er worden extra tests en controles uitgevoerd om de implementatie in elke fase van het proces te controleren. Zie [Het updateproces](hr-admin-setup-update-process.md) voor meer informatie over het releasetempo.

## <a name="known-issues"></a>Bekende problemen

## <a name="employment-detail-entity"></a>Entiteit Details dienstverband

De entiteit **Details dienstverband** is bijgewerkt met de volgende velden: **Betalingsfrequentie**, **Aanstellingscategorie-id**, **Type dienstverband**, **Type dienstverband-id** en **Status van vergoeding voor aanstelling**. De instellingsgegevens voor deze velden zijn afhankelijk van het vergoedingenbeheer dat is ingeschakeld in Functiebeheer. Vul deze velden niet in of werk ze niet bij in de entiteit **Details dienstverband**, omdat deze tijdens het importeren fouten zullen opleveren.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>SharePoint-voorbeeld werkt niet in sommige omgevingen

Als het documentvoorbeeld voor documenten opgeslagen in SharePoint niet werkt, voert u de volgende procedure uit:

1. Controleer voor de gebruikersaccount Beheerder of er een e-mailadres is gekoppeld aan de gebruikersrecord. Deze gegevens worden weergegeven op de pagina **Gebruiker**. Als er geen e-mailadres is ingesteld, moet u het e-mailadres en de provider toevoegen met de Excel-invoegtoepassing OData. Standaard is het e-mailadres niet aanwezig in het Excel-ontwerp. U moet het Excel-ontwerp bewerken, alle velden toevoegen, toepassen en vernieuwen. Wanneer u deze stappen hebt voltooid, kunt u de beheerdersaccount bijwerken.

2. Nadat aan de beheerdersaccount een e-mailaccount is gekoppeld, meldt u zich aan bij Human Resources met beheerdersreferenties.

3. Open een bijlage in SharePoint om de voorbeeldweergave van documenten te starten.

4. Meld u aan met een andere gebruikersaccount die toegang heeft tot bijlagen en controleer of het voorbeeld werkt zoals verwacht.