---
title: Talent uitbreiden met PowerApps en Microsoft Flow - voorbeeldscenario's
description: In dit onderwerp worden enkele voorbeelden beschreven van uitbreidbaarheidsscenario's voor Microsoft Dynamics 365 for Talent die gebruikmaken van Microsoft PowerApps en Microsoft Flow.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 for Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 0b455a8194f58b41a349f004ceda8183c7ee3f7c
ms.sourcegitcommit: 9f94eff93d29bc27352569824e00bbccc2f961b8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/22/2019
ms.locfileid: "1781437"
---
# <a name="extend-talent-by-using-powerapps-and-microsoft-flow---example-scenarios"></a>Talent uitbreiden met PowerApps en Microsoft Flow - voorbeeldscenario's

In dit onderwerp worden enkele voorbeelden beschreven van uitbreidbaarheidsscenario's voor Microsoft Dynamics 365 for Talent die gebruikmaken van Microsoft PowerApps en Microsoft Flow. U kunt het oplossingspakket importeren dat is gekoppeld aan elk voorbeeld in uw PowerApps-omgeving. Vervolgens kunt u de pakketten als richtlijn of als beginpunt gebruiken voor het implementeren van scenario's die van toepassing op uw organisatie.

> [!IMPORTANT]
> Als u de sjablonen en app die worden beschreven in dit onderwerp, 'as is' wilt gebruiken, moet u ze testen om er zeker van te zijn dat ze betrekking hebben op alle scenario's die specifiek voor uw implementatie zijn.


## <a name="prerequisites"></a>Vereisten

- Als u wilt pakketten wilt importeren, moeten gebruikers beschikken over de machtiging **Maker omgeving** beschikken.
- Als u apps wilt exporteren of importeren, moeten gebruikers een PowerApps Plan 2-licentie of een proeflicentie van PowerApps Plan 2 hebben.

## <a name="flow--form-connect"></a>Stroom: formulier verbinden

De sjabloon **Stroom: formulier verbinden** kan worden gebruikt om gegevens vanuit Microsoft Forms te lezen en deze op te slaan in een Common Data Service-entiteit.

Deze sjabloon kan worden uitgebreid, zodat deze kan worden gebruikt voor andere scenario's. Hieronder vindt u enkele voorbeelden:

- Kandidaatbeoordelingen vastleggen.
- Resultaten van cursusvragenlijsten vastleggen.
- Een bibliotheek samenstellen van sollicitatiegesprekvragen voor beheerders van Human resources (HR).
- De evaluatie van een kandidaat van het sollicitatiegesprekproces vastleggen.

In Microsoft Dynamics 365: Attract kunnen formulieren worden weergegeven in de portal Kandidaat en kunnen kandidaten details invullen. Formulieren kunnen ook als activiteiten worden ingesloten in een functiesjabloon.

Wanneer een kandidaat een formulier indient, wordt in Microsoft Flow de formulierindiening vastgelegd, de gegevens gelezen en opgeslagen in de Common Data Service-entiteit.

Voor het downloaden van de sjabloon **Stroom: formulier verbinden** en de structuur van aangepaste entiteiten gaat u naar [Stroom: formulier verbinden](https://go.microsoft.com/fwlink/?linkid=2081988) in het Microsoft Downloadcentrum.

## <a name="initiate-and-extract-parameters-passed-to-powerapps"></a>Aan PowerApps doorgegeven parameters initiëren en extraheren

De sjabloon **Aan PowerApps doorgegeven parameters initiëren en extraheren** kan worden gebruikt als uitgangspunt voor elk PowerApps-scenario dat specifiek is voor Attract. De sjabloon bevat alle standaardparameters die worden doorgegeven door Attract, zoals **Sollicitatie**, **Kandidaat-id** en **Functie-id**.

Deze sjabloon kan worden gebruikt om formulier voor kandidaatbeoordeling op te halen, zodat een aanstellende manager de beoordeling kan bekijken die een kandidaat heeft ingevuld.

Apps die zijn gemaakt met behulp van PowerApps, kunnen worden ingesloten in de functiesjabloon in Attract.

Voor het downloaden van de sjabloon **Aan PowerApps doorgegeven parameters initiëren en extraheren** en de structuur voor aangepaste entiteiten, gaat u naar [Aan PowerApps doorgegeven parameters initiëren en extraheren](https://go.microsoft.com/fwlink/?linkid=2081991) in het Microsoft Downloadcentrum.

## <a name="integration-with-office-365"></a>Integratie met Office 365

De app **Integratie met Office 365** kan worden gebruikt voor het ophalen van teamgegevens voor aangemelde gebruikers vanuit Microsoft Office 365. Hiermee wordt verwezen naar werknemers in Talent voor het ophalen van inklok- en uitklokdetails en uitzonderingsregistraties. Inklok- en uitklokdetails worden opgeslagen in de aangepaste Common Data Service-entiteiten. De veronderstelling is dat deze details worden ingevuld via systemen van derden via integratie.

Deze app kan worden uitgebreid, zodat deze kan worden gebruikt voor andere scenario's. Deze app kan bijvoorbeeld worden gebruikt om teamvakantiegegevens, agenda-items en teamspecifieke gebeurtenissen weer te geven.

Voor het downloaden van de app **Integratie met Office 365** app en de structuur voor aangepaste entiteiten, gaat u naar [Integratie met Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) in het Microsoft Downloadcentrum.

## <a name="flow--email-notification"></a>Stroom: e-mailmelding

De sjabloon **Stroom: e-mailwaarschuwing** kan worden gebruikt voor e-mailmeldingsscenario's. De sjabloon kan worden gebruikt voor het activeren van e-mailberichten aan kandidaten die het aanstellingsteam afwijst tijdens elke fase van het wervingsproces.

Deze sjabloon kan worden uitgebreid voor het bijhouden van wijzigingen in de kandidaatfase gedurende het wervingsproces en voor het verzenden van meldingen aan het aanstellingsteam en de kandidaat.

In het algemeen kunnen voor entiteiten die zijn opgeslagen in Common Data Service, stromen worden ingesteld voor het verzenden van meldingen voor gebeurtenissen die in Core HR, Attract of Dynamics 365 Talent: Onboard plaatsvinden.

Voor het downloaden van de sjabloon **Stroom: e-mailwaarschuwing** gaat u naar [Stroom: e-mailwaarschuwing](https://go.microsoft.com/fwlink/?linkid=2082103) in het Microsoft Downloadcentrum.

## <a name="flow--sql-connect-and-execute"></a>Stroom: verbinding maken met SQL en SQL-query´s uitvoeren

Met de sjabloon **Stroom: verbinding maken met SQL en SQL-query´s uitvoeren** wordt verbinding gemaakt met Microsoft SQL Server en kunnen SQL-query's worden uitgevoerd.

Hoewel deze sjabloon is ontworpen voor het lezen en bijwerken van SQL-tabellen, kan deze worden uitgebreid zodat deze kan worden gebruikt voor andere scenario's. Zo kan de sjabloon worden gebruikt voor het invullen van een faseringstabel in Common Data Service met records van SQL Server en voor het periodiek synchroniseren van de faseringstabel met behulp van een incrementele push van SQL Server.

Voor het downloaden van de sjabloon **Stroom: verbinding maken met SQL en SQL-query´s uitvoeren** gaat u naar [Stroom: verbinding maken met SQL en SQL-query´s uitvoeren](https://go.microsoft.com/fwlink/?linkid=2081789) in het Microsoft Downloadcentrum.

## <a name="flow--sharepoint-integration"></a>Stroom: SharePoint-integratie

De sjabloon **Stroom: SharePoint-integratie** kan worden gebruikt voor het lezen van gegevens vanuit een Microsoft SharePoint-lijst, voor het vergelijken van de lijst met veldwaarden voor elke Common Data Service-entiteit en voor het verzenden van de resultaten van de vergelijking als een melding per e-mail. 

Een organisatie kan een set vaardigheden dringend nodig hebben. Deze vaardigheden kunnen zijn opgeslagen in SharePoint als een SharePoint-lijst. Wanneer een kandidaat solliciteert op een functie waarvoor een set vereiste vaardigheden wordt vermeld en de vaardigheden van de kandidaat en de vaardigheden die zijn opgeslagen in SharePoint, grotendeels overeenkomen, wordt een melding per e-mail wordt verzonden. Op deze manier worden dringende posities sneller ingevuld, omdat de wervers met de meldingen kandidaten sneller kunnen bereiken en aanstellen in de hele organisatie.

Deze sjabloon kan worden uitgebreid, zodat deze kan worden gebruikt voor elk scenario dat betrekking heeft op SharePoint-integratie.

Voor het downloaden van de sjabloon **Stroom: SharePoint-integratie** gaat u naar [Stroom: SharePoint-integratie](https://go.microsoft.com/fwlink/?linkid=2082109) in het Microsoft Downloadcentrum.

## <a name="referral-app"></a>De app Referral
U kunt de app Referral gebruiken om kandidaten toe te voegen aan een gedeelde talentenpool. De verwijzer kan waarden voor **Voornaam**, **Achternaam**, **E-mail** en **Linkedln-URL** opgeven bij het indienen van een kandidaat. De bronmetagegevens van de kandidaat worden vervolgens gevuld met de gegevens van de verwijzer.

U kunt deze app insluiten in Selfservice werknemer voor het indienen van verwijzingen of u kunt deze app als hyperlink gebruiken in de bedrijfsportal en uitvoeren als een zelfstandige app.

Als u de app **Referral** wil downloaden, gaat u naar [Dynamics 365 for Talent extensibility solution: Referral App](http://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) in het Microsoft Downloadcentrum. U kunt deze app importeren en aanpassen om extra functionaliteit toe te voegen.

## <a name="additional-resources"></a>Aanvullende resources

[Het Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[App tussen tenants en omgevingen migreren](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
