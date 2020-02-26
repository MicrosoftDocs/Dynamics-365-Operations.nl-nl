---
title: Talent uitbreiden met Power Apps en Power Automate
description: In dit artikel worden enkele voorbeelden beschreven van uitbreidbaarheidsscenario's voor Microsoft Dynamics 365 Talent Attract die gebruikmaken van Microsoft Power Apps en Microsoft Power Automate.
author: negudava
manager: Annbe
ms.date: 02/06/2020
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 1051fa4db16bb94cc9d60a91fc3637d7e5305cc2
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029906"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a>Talent uitbreiden met Power Apps en Power Automate

In dit artikel worden enkele voorbeelden beschreven van uitbreidbaarheidsscenario's voor Microsoft Dynamics 365 Talent: Attract die gebruikmaken van Microsoft Power Apps en Microsoft Power Automate. U kunt het oplossingspakket importeren dat is gekoppeld aan elk voorbeeld in uw Power Apps-omgeving. Vervolgens kunt u de pakketten als richtlijn of als beginpunt gebruiken voor het implementeren van scenario's die van toepassing op uw organisatie.

> [!IMPORTANT]
> Als u de sjablonen en app die worden beschreven in dit artikel, 'as is' wilt gebruiken, moet u ze testen om er zeker van te zijn dat ze betrekking hebben op alle scenario's die specifiek voor uw implementatie zijn.


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

In Microsoft Dynamics 365: Attract kunt u formulieren gebruiken in de portal Kandidaat, waar kandidaten details invullen. U kunt ook formulieren insluiten als activiteiten in een functiesjabloon.

Wanneer een kandidaat een formulier indient, wordt in Microsoft Power Automate de formulierindiening vastgelegd en worden de gegevens gelezen en opgeslagen in de Common Data Service-entiteit.

Voor het downloaden van de sjabloon **Power Automate: formulier verbinden** en de structuur van aangepaste entiteiten gaat u naar [Power Automate: formulier verbinden](https://go.microsoft.com/fwlink/?linkid=2081988) in het Microsoft Downloadcentrum.

## <a name="power-automate--sharepoint-integration"></a>Power Automate: SharePoint-integratie

De sjabloon **Power Automate: SharePoint-integratie** kan worden gebruikt voor het lezen van gegevens vanuit een Microsoft SharePoint-lijst, voor het vergelijken van de lijst met veldwaarden voor elke Common Data Service-entiteit en voor het verzenden van de resultaten van de vergelijking als een melding per e-mail. 

Een organisatie kan een set vaardigheden dringend nodig hebben. Deze vaardigheden kunnen zijn opgeslagen in SharePoint als een SharePoint-lijst. Wanneer een kandidaat solliciteert op een functie waarvoor een set vereiste vaardigheden wordt vermeld en de vaardigheden van de kandidaat en de vaardigheden die zijn opgeslagen in SharePoint, grotendeels overeenkomen, wordt een melding per e-mail wordt verzonden. Dit helpt dringende posities sneller in te vullen, omdat de wervers met de meldingen kandidaten sneller kunnen bereiken en aanstellen in de hele organisatie.

Deze sjabloon kan worden uitgebreid, zodat deze kan worden gebruikt voor elk scenario dat betrekking heeft op SharePoint-integratie.

Voor het downloaden van de sjabloon **Power Automate: SharePoint-integratie** gaat u naar [Power Automate: SharePoint-integratie](https://go.microsoft.com/fwlink/?linkid=2082109) in het Microsoft Downloadcentrum.

## <a name="referral-app"></a>De app Referral

U kunt de app Referral gebruiken om kandidaten toe te voegen aan een gedeelde talentenpool. De verwijzer kan waarden voor **Voornaam**, **Achternaam**, **E-mail** en **Linkedln-URL** opgeven bij het indienen van een kandidaat. De bronmetagegevens van de kandidaat worden vervolgens gevuld met de gegevens van de verwijzer.

U kunt deze app insluiten in Werknemerselfservice voor het indienen van verwijzingen of u kunt deze app als hyperlink gebruiken in de bedrijfsportal en uitvoeren als een zelfstandige app.

Als u de app **Referral** wil downloaden, gaat u naar [Dynamics 365 Talent extensibility solution: Referral App](https://www.microsoft.com/download/details.aspx?id=58497) in het Microsoft Downloadcentrum. U kunt deze app importeren en aanpassen om extra functionaliteit toe te voegen.

## <a name="additional-resources"></a>Aanvullende resources

[Het Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[App tussen tenants en omgevingen migreren](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
