---
title: Talent uitbreiden met Power Apps en Power Automate
description: In dit onderwerp worden enkele voorbeelden beschreven van uitbreidbaarheidsscenario's voor Microsoft Dynamics 365 Talent die gebruikmaken van Microsoft Power Apps en Microsoft Power Automate.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 Talent;PowerApps;Flow;Common Data Service
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
ms.openlocfilehash: 3bb61297e294aa3f2d06f542bebe29d7afae9c3b
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832833"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a>Talent uitbreiden met Power Apps en Power Automate

[!include [banner](includes/banner.md)]

In dit onderwerp worden enkele voorbeelden beschreven van uitbreidbaarheidsscenario's voor Microsoft Dynamics 365 Talent die gebruikmaken van Microsoft Power Apps en Microsoft Power Automate. U kunt het oplossingspakket importeren dat is gekoppeld aan elk voorbeeld in uw Power Apps-omgeving. Vervolgens kunt u de pakketten als richtlijn of als beginpunt gebruiken voor het implementeren van scenario's die van toepassing op uw organisatie.

> [!IMPORTANT]
> Als u de sjablonen en app die worden beschreven in dit onderwerp, 'as is' wilt gebruiken, moet u ze testen om er zeker van te zijn dat ze betrekking hebben op alle scenario's die specifiek voor uw implementatie zijn.


## <a name="prerequisites"></a>Vereisten

- Als u wilt pakketten wilt importeren, moeten gebruikers beschikken over de machtiging **Maker omgeving** beschikken.
- Als u apps wilt exporteren of importeren, moeten gebruikers een Power Apps Plan 2-licentie of een proeflicentie van Power Apps Plan 2 hebben.

## <a name="power-automate--form-connect"></a>Power Automate: formulier verbinden

De sjabloon **Power Automate: formulier verbinden** kan worden gebruikt om gegevens vanuit Microsoft Forms te lezen en deze op te slaan in een Common Data Service-entiteit.

Deze sjabloon kan worden uitgebreid, zodat deze kan worden gebruikt voor andere scenario's. Hieronder vindt u enkele voorbeelden:

- Kandidaatbeoordelingen vastleggen.
- Resultaten van cursusvragenlijsten vastleggen.
- Een bibliotheek samenstellen van sollicitatiegesprekvragen voor beheerders van Human resources (HR).
- De evaluatie van een kandidaat van het sollicitatiegesprekproces vastleggen.

In Microsoft Dynamics 365: Attract kunnen formulieren worden weergegeven in de portal Kandidaat en kunnen kandidaten details invullen. Formulieren kunnen ook als activiteiten worden ingesloten in een functiesjabloon.

Wanneer een kandidaat een formulier indient, wordt in Microsoft Power Automate de formulierindiening vastgelegd en worden de gegevens gelezen en opgeslagen in de Common Data Service-entiteit.

Voor het downloaden van de sjabloon **Power Automate: formulier verbinden** en de structuur van aangepaste entiteiten gaat u naar [Power Automate: formulier verbinden](https://go.microsoft.com/fwlink/?linkid=2081988) in het Microsoft Downloadcentrum.

## <a name="initiate-and-extract-parameters-passed-to-power-apps"></a>Aan Power Apps doorgegeven parameters initiëren en extraheren

De sjabloon **Aan Power Apps doorgegeven parameters initiëren en extraheren** kan worden gebruikt als uitgangspunt voor elk Power Apps-scenario dat specifiek is voor Attract. De sjabloon bevat alle standaardparameters die worden doorgegeven door Attract, zoals **Sollicitatie**, **Kandidaat-id** en **Functie-id**.

Deze sjabloon kan worden gebruikt om formulier voor kandidaatbeoordeling op te halen, zodat een aanstellende manager de beoordeling kan bekijken die een kandidaat heeft ingevuld.

Apps die zijn gemaakt met behulp van Power Apps, kunnen worden ingesloten in de functiesjabloon in Attract.

Voor het downloaden van de sjabloon **Aan Power Apps doorgegeven parameters initiëren en extraheren** en de structuur voor aangepaste entiteiten gaat u naar [Aan Power Apps doorgegeven parameters initiëren en extraheren](https://go.microsoft.com/fwlink/?linkid=2081991) in het Microsoft Downloadcentrum.

## <a name="integration-with-office-365"></a>Integratie met Office 365

De app **Integratie met Office 365** kan worden gebruikt voor het ophalen van teamgegevens voor aangemelde gebruikers vanuit Microsoft Office 365. Hiermee wordt verwezen naar werknemers in Talent voor het ophalen van inklok- en uitklokdetails en uitzonderingsregistraties. Inklok- en uitklokdetails worden opgeslagen in de aangepaste Common Data Service-entiteiten. De veronderstelling is dat deze details worden ingevuld via systemen van derden via integratie.

Deze app kan worden uitgebreid, zodat deze kan worden gebruikt voor andere scenario's. Deze app kan bijvoorbeeld worden gebruikt om teamvakantiegegevens, agenda-items en teamspecifieke gebeurtenissen weer te geven.

Voor het downloaden van de app **Integratie met Office 365** app en de structuur voor aangepaste entiteiten, gaat u naar [Integratie met Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) in het Microsoft Downloadcentrum.

## <a name="power-automate--email-notification"></a>Power Automate: e-mailmelding

De sjabloon **Power Automate: e-mailwaarschuwing** kan worden gebruikt voor e-mailmeldingsscenario's. De sjabloon kan worden gebruikt voor het activeren van e-mailberichten aan kandidaten die het aanstellingsteam afwijst tijdens elke fase van het wervingsproces.

Deze sjabloon kan worden uitgebreid voor het bijhouden van wijzigingen in de kandidaatfase gedurende het wervingsproces en voor het verzenden van meldingen aan het aanstellingsteam en de kandidaat.

In het algemeen kunnen voor entiteiten die zijn opgeslagen in Common Data Service, stromen worden ingesteld voor het verzenden van meldingen voor gebeurtenissen die in Core HR, Attract of Onboard plaatsvinden.

Voor het downloaden van de sjabloon **Power Automate: e-mailwaarschuwing** gaat u naar [Power Automate: e-mailwaarschuwing](https://go.microsoft.com/fwlink/?linkid=2082103) in het Microsoft Downloadcentrum.

## <a name="power-automate--sql-connect-and-execute"></a>Power Automate: verbinding maken met SQL en SQL-query´s uitvoeren

Met de sjabloon **Power Automate: verbinding maken met SQL en SQL-query´s uitvoeren** wordt verbinding gemaakt met Microsoft SQL Server en kunnen SQL-query's worden uitgevoerd.

Hoewel deze sjabloon is ontworpen voor het lezen en bijwerken van SQL-tabellen, kan deze worden uitgebreid zodat deze kan worden gebruikt voor andere scenario's. Zo kan de sjabloon worden gebruikt voor het invullen van een faseringstabel in Common Data Service met records van SQL Server en voor het periodiek synchroniseren van de faseringstabel met behulp van een incrementele push van SQL Server.

Voor het downloaden van de sjabloon **Power Automate: verbinding maken met SQL en SQL-query´s uitvoeren** gaat u naar [Power Automate: verbinding maken met SQL en SQL-query´s uitvoeren](https://go.microsoft.com/fwlink/?linkid=2081789) in het Microsoft Downloadcentrum.

## <a name="power-automate--sharepoint-integration"></a>Power Automate: SharePoint-integratie

De sjabloon **Power Automate: SharePoint-integratie** kan worden gebruikt voor het lezen van gegevens vanuit een Microsoft SharePoint-lijst, voor het vergelijken van de lijst met veldwaarden voor elke Common Data Service-entiteit en voor het verzenden van de resultaten van de vergelijking als een melding per e-mail. 

Een organisatie kan een set vaardigheden dringend nodig hebben. Deze vaardigheden kunnen zijn opgeslagen in SharePoint als een SharePoint-lijst. Wanneer een kandidaat solliciteert op een functie waarvoor een set vereiste vaardigheden wordt vermeld en de vaardigheden van de kandidaat en de vaardigheden die zijn opgeslagen in SharePoint, grotendeels overeenkomen, wordt een melding per e-mail wordt verzonden. Op deze manier worden dringende posities sneller ingevuld, omdat de wervers met de meldingen kandidaten sneller kunnen bereiken en aanstellen in de hele organisatie.

Deze sjabloon kan worden uitgebreid, zodat deze kan worden gebruikt voor elk scenario dat betrekking heeft op SharePoint-integratie.

Voor het downloaden van de sjabloon **Power Automate: SharePoint-integratie** gaat u naar [Power Automate: SharePoint-integratie](https://go.microsoft.com/fwlink/?linkid=2082109) in het Microsoft Downloadcentrum.

## <a name="referral-app"></a>De app Referral
U kunt de app Referral gebruiken om kandidaten toe te voegen aan een gedeelde talentenpool. De verwijzer kan waarden voor **Voornaam**, **Achternaam**, **E-mail** en **Linkedln-URL** opgeven bij het indienen van een kandidaat. De bronmetagegevens van de kandidaat worden vervolgens gevuld met de gegevens van de verwijzer.

U kunt deze app insluiten in Selfservice werknemer voor het indienen van verwijzingen of u kunt deze app als hyperlink gebruiken in de bedrijfsportal en uitvoeren als een zelfstandige app.

Als u de app **Referral** wil downloaden, gaat u naar [Dynamics 365 Talent extensibility solution: Referral App](http://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) in het Microsoft Downloadcentrum. U kunt deze app importeren en aanpassen om extra functionaliteit toe te voegen.

## <a name="additional-resources"></a>Aanvullende resources

[Het Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[App tussen tenants en omgevingen migreren](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
