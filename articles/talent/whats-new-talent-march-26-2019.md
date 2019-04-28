---
title: Wat is nieuw of gewijzigd in Dynamics 365 for Talent (26 maart 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/26/2019
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
ms.search.validFrom: 2019-03-26
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 568a16a17ed3269c7b72f27f0d4b7bbdbd56630e
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/12/2019
ms.locfileid: "949823"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-26-2019"></a>Wat is nieuw of gewijzigd in Dynamics 365 for Talent (26 maart 2019)

[!include [banner](includes/banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Wijzigingen in Attract

### <a name="enhancements-to-interview-scheduling"></a>Verbeteringen voor het plannen van sollicitatiegesprekken
De volgende verbeteringen zijn beschikbaar bij het plannen van sollicitatiegesprekken.

- Wervers of aanstellende managers kunnen nu handmatig een herinnering om feedback in te dienen activeren voor een interviewer. De bijbehorende e-mailsjabloon voor de herinnering kan ook worden geconfigureerd.
- Bij het delen van het overzicht van het sollicitatiegesprek met de kandidaat, kan de planner van sollicitatiegesprekken ervoor kiezen de namen van de interviewers te verbergen en ook om rijen uit de overzichtsweergave van het gesprek te verbergen.

## <a name="changes-in-onboard"></a>Wijzigingen in Onboard

### <a name="embedded-images-in-activities"></a>Ingesloten afbeeldingen in activiteiten
U kunt nu afbeeldingen rechtstreeks insluiten in activiteiten. U kunt afbeeldingen nu niet alleen kopiëren en plakken vanaf het web, maar u kunt afbeeldingen uploaden vanaf uw lokale bestandssysteem. De grootte van de activiteit is beperkt tot 1 MB. Als de afbeelding te groot is, past u de grootte aan en probeert u opnieuw te uploaden.

[![Toewijzing](./media/embedimages.png)](./media/embedimages.png)

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Wijzigingen in Core HR
**Build 8.1.2210**

### <a name="custom-field-support-available-for-select-entities-in-common-data-service"></a>Ondersteuning van aangepaste velden beschikbaar voor bepaalde entiteiten in Common Data Service 

De volgende Common Data Service-entiteiten bieden voortaan ondersteuning aan aangepaste velden die zijn gemaakt in Dynamics 365 for Talent:

- Medewerker
- Etnische afkomst
- Oorlogsveteraanstatus
- Taalcode
- Taak
- Taaktype
- Taakfunctie
- Positie
- Positietype
 
### <a name="employment-history-not-displayed-chronologically"></a>Dienstverbandhistorie wordt niet chronologisch weergegeven
Met deze wijziging worden op de pagina met dienstverbandhistorie dienstverbandrecords nu chronologisch weergegeven, onafhankelijk van het bedrijf. U kunt ook sorteeropties gebruiken om te sorteren op bedrijf.

### <a name="fixed-compensation-plans-dont-appear-when-restricting-user-by-company-in-security"></a>Vastecompensatieplannen worden niet weergegeven wanneer gebruikers per bedrijf in de beveiliging worden beperkt.
In deze release worden vastecompensatieplannen nu weergegeven wanneer gebruikers per bedrijf in beveiliging worden beperkt. Alle beveiligingsinstellingen worden gehonoreerd en vaste plannen worden weergegeven voor de bedrijven waarvoor de gebruiker toegangsrechten heeft. 

### <a name="cant-delete-job-records-using-open-in-excel-option-in-talent"></a>Functierecords kunnen niet worden verwijderd met de optie Openen in Excel
Met deze versie kunt u nu functierecords verwijderen met de optie **Openen in Excel** in Dynamics 365 for Talent.

### <a name="upgrade-to-common-data-service"></a>Upgrade naar Common Data Service
Uiterste datums voor een upgrade naar Common Data Service naderen snel. Meld u aan bij het PowerApps-beheercentrum om te bepalen of een upgrade op uw database moet worden uitgevoerd. Zie voor meer informatie over uiterste datums en de nodige stappen om te upgraden [Upgraden naar Common Data Service](https://docs.microsoft.com/en-us/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="in-preview"></a>Preview

Zie voor informatie over het inschakelen van voorbeeldfuncties  [Toegang tot voorbeeldfuncties in Talent](./access-preview-feature.md).

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Toestaan dat redencodes voor verloftypen worden opgegeven
Organisaties hebben mogelijk extra informatie met betrekking tot verlofaanvragen nodig. Om deze informatie te verkrijgen, moeten werknemers een redencode voor hun verlofaanvragen opnemen. Met deze release kunt u nu de redencodes opgeven die zijn gekoppeld aan een bepaald verloftype en kunnen werknemers een redencode in hun verlofaanvragen selecteren.

### <a name="configure-reason-codes-to-be-required-when-submitting-time-off-for-certain-leave-types"></a>Redencodes configureren die moeten worden opgegeven bij het indienen van verlofaanvragen voor bepaalde verloftypen
Organisaties kunnen vereisen dat redencodes worden ingesteld voor specifieke verloftypen wanneer werknemers verlofaanvragen indienen. Dit kan worden vereist op basis van een wettelijke vereiste in hun land/regio of een bedrijfsbeleid. Deze versie biedt de mogelijkheid voor HR om op te geven voor welke verloftypen een redencode is vereist. Dit wordt afgedwongen wanneer werknemers verlofaanvragen indienen waarbij voor het verlof een redencode is vereist.

## <a name="coming-soon"></a>Binnenkort beschikbaar

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Geavanceerde compensatiebeveiliging (vast en variabel)
In veel organisaties hebben managers voor compensaties en vergoedingen mogelijk alleen toegang tot bepaalde compensatierecords. Dit kan voor leidinggevenden of regionale werknemers zijn. Met deze wijziging kan HR de compensatieplannen beheren en onderhouden voor verschillende werknemersgroepen in de organisatie. U kunt aan vaste en variabele plannen beveiligingsrollen toewijzen waarmee de toegang wordt bepaald tot de plannen en de werknemersgegevens die zijn gerelateerd aan de plannen, zoals salaris- of bonusrecords. Alleen de rollen waaraan toegangsrechten zijn verleend, kunnen compensatie voor deze werknemers verwerken.

###  <a name="email-support-for-alerts"></a>E-ondersteuning voor waarschuwingen
Met platformupdate 25 kunnen gebruikers waarschuwingsregels maken waarmee automatisch e-mailmeldingen worden verzonden naar contactpersonen wanneer deze door een gebeurtenis worden geactiveerd. 

### <a name="duplicate-employee-checks-user-interface-changes"></a>Controles of dubbele werknemers: gebruikersinterfacewijzigingen
Met deze wijziging worden dubbele records gedetecteerd wanneer u naamvelden invoert en met een status wordt het aantal dubbelen weergegeven. U kunt de opgegeven koppeling selecteren om een nieuwe pagina te openen om te beoordelen of de gedetecteerde overeenkomst moet worden gebruikt. Om te voorkomen dat gegevensinvoer wordt onderbroken, wordt het formulier met dubbele records niet automatisch geopend.
