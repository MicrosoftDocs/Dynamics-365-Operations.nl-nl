---
title: Wat is nieuw of gewijzigd in Dynamics 365 Talent - Core HR (6 december 2018)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 12/07/2018
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
ms.search.validFrom: 2018-12-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 462b87a655e3e4017cffd2ba41cb6d1f18de3e50
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529157"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-december-6-2018"></a>Wat is nieuw of gewijzigd in Dynamics 365 Talent - Core HR (6 december 2018)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**Build 8.1.2071**

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Core HR.


## <a name="platform-update-22-for-finance-and-operations"></a>Platformupdate 22 voor Finance and Operations

### <a name="export-up-to-1-million-rows-to-excel"></a>Tot 1 miljoen rijen naar Excel exporteren

De functie Exporteren naar Excel kan nu zo worden geconfigureerd dat gebruikers maximaal 1 miljoen rijen vanuit een raster in Talent kunnen exporteren, een aanzienlijke toename ten opzichte van de limiet van 10.000 rijen. 

### <a name="restyled-personalization-toolbar"></a>Aanpassingswerkbalk opnieuw vormgegeven

De aanpassingswerkbalk is opnieuw vormgegeven in platformupdate 22 voor Finance and Operations om gebruikers te helpen hun eigen ervaringen gemakkelijker aan te passen in Talent. De volgende wijzigingen zijn aangebracht: 

-  De naam van elk aanpassingsprogramma wordt nu weergegeven met een pictogram, zodat gebruikers de programma's die ze willen gebruiken snel herkennen.
-  De beschrijving voor het gebruik van het huidige programma wordt nu ook weergegeven, zodat gebruikers begrijpen hoe ze de nodige aanpassingen doorvoeren.  
-  De hele aanpassingswerkbalk kan worden verplaatst over het scherm door het gedeelte uiterst links van de werkbalk naar een bepaald gebied te slepen. Zo kunnen gebruikers elementen aanpassen die eerder werden verborgen door de werkbalk.   

### <a name="optimized-is-one-of-filtering-experience"></a>Ervaring 'is een van' geoptimaliseerd

De filteroperator 'is een van' is beschikbaar voor de meeste velden bij het gebruik van het filterdeelvenster en de vervolgkeuzelijsten in de koptekst van het raster. Met deze operator kan een gebruiker een veld op basis van meerdere waarden filteren. Een nieuwe en verbeterde ervaring voor de operator 'is een van' is beschikbaar in platformupdate 22 voor Finance and Operations. Zie [Geoptimaliseerde filterervaring "is één van" ingeschakeld](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/improved-isoneof-filtering) voor meer informatie.

### <a name="paste-lists-from-excel-into-filter-fields-with-the-is-one-of-operator"></a>Lijsten vanuit Excel in filtervelden plakken met de operator 'is een van'

Voor sommige taken hebben gebruikers wellicht een lijst met waarden in Excel die ze willen gebruiken voor het filteren van gegevens in Talent. Een Human Resource-gebruiker kan bijvoorbeeld in een rapport een aantal werknemers hebben geïdentificeerd waarvoor aanvullend onderzoek in het systeem nodig is en het zou voor deze gebruiker ideaal zijn als de lijst rechtstreeks vanuit Excel naar een filterveld in Talent kon worden gekopieerd.

Vanaf platformupdate 22 voor Finance and Operations herkent de operator 'is een van' in het filterdeelvenster en de rasterkolomfilters nu lijsten die worden gekopieerd vanuit Excel, zodat deze rechtstreeks in een filterveld kunnen worden geplakt. Het gaat hierbij om een verzameling waarden die uit verschillende rijen en kolommen in Excel worden gekopieerd. Zie [Lijsten vanuit Excel in filtervelden plakken met de operator 'is een van'](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/paste-filter-lists-from-excel) voor meer informatie over deze functie.

## <a name="in-preview"></a>Preview

### <a name="configure-uk-payroll-integration-between-talent-and-dayforce"></a>De integratie van de VK-salarisadministratie tussen Talent en Dayforce configureren

De integratie tussen Talent en Ceridian Dayforce is als preview beschikbaar voor het Verenigd Koninkrijk. Raadpleeg het onderwerp [De integratie van de salarisadministratie tussen Talent en Dayforce configureren](https://docs.microsoft.com/dynamics365/unified-operations/talent/configure-payroll-integration) voor meer informatie.

## <a name="coming-soon"></a>Binnenkort beschikbaar

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a>Verlof en verzuim: toekomstig verlof en prognoses van verlofsaldi

Naast de wijzigingen om werknemers in staat te stellen verlof te voorspellen en toekomstige verlofaanvragen aan te vragen zonder dat dit invloed heeft op hun huidige verlofsaldi, wordt ook de wijze aangepast waarop verlofsaldi worden weergegeven. 

Het beschikbare saldo dat momenteel wordt weergegeven, is de hoeveelheid verlof die beschikbaar is voor aanvragen, met inbegrip van toerekeningen tot en met vandaag en alle goedgekeurde aanvragen tot en met het einde van de tijd. 

Wanneer de functie voor voorspellen wordt vrijgegeven, wordt het huidige verlofsaldo weergegeven, inclusief toerekeningen en verzoeken tot en met vandaag. Werknemers en managers zien deze bijgewerkte saldi in de selfservice-functionaliteit voor werknemer en manager op de kaart **Verlof** en in het venster **Verlofsaldi**. Voor HR-managers worden deze bijgewerkte saldi weergegeven in het werkgebied **Mensen** en in het venster **Toegewezen verlofplannen** van de werknemer.

## <a name="other-changes"></a>Andere wijzigingen 

### <a name="termination-code-is-not-populated-to-the-worker-position-assignment-record"></a>Ontslagcode wordt niet ingevuld in de positietoewijzingsecord van de werknemer

Er is een wijziging geïmplementeerd waardoor de redencode wordt ingevuld in de positietoewijzingsrecord tijdens het ontslagproces.

### <a name="validation-for-personnel-number-being-in-use-needs-additional-details"></a>Voor validatie voor personeelsnummers in gebruik is aanvullende informatie nodig

Er wordt aanvullende informatie weergegeven wanneer nummerreeksen worden gebruikt, om meer inzicht te krijgen in problemen wanneer geen nieuw nummer kan worden gegenereerd.
 
### <a name="attachments-buttons-not-available-for-workers"></a>Bijlageknoppen niet beschikbaar voor werknemers

Er zijn wijzigingen aangebracht om bijlagen te corrigeren. Wanneer u een nieuwe bijlage aan een werknemer toevoegt, zijn nu de knoppen **Nieuw** en **Bewerken** beschikbaar wanneer feitenblokken zijn geopend in het werknemersvenster. 

## <a name="known-issues"></a>Bekende problemen

### <a name="mapping-errors-in-the-integration-with-finance"></a>Toewijzingsfouten in de integratie met Finance

De volgende problemen kunnen optreden in de huidige sjabloon voor het integreren van Talent met Finance. Binnenkort wordt een nieuwe sjabloon gepubliceerd om toe te passen op alle nieuwe integratieprojecten die zijn gemaakt. Voor bestaande integratieprojecten kunnen de taaktoewijzingen worden bijgewerkt. Raadpleeg de volgende tabel voor bijgewerkte toewijzingen. 

>[!NOTE]
> Met de taak voor het toewijzen van taken aan bovenliggende posities worden geen gegevens geïntegreerd. Dit probleem wordt momenteel onderzocht. Er is geen oplossing in de huidige toewijzing. 

Voor de taak Afdelingen naar Operationele eenheid moeten de volgende toewijzingen worden bijgewerkt.

| Bestaand bronveld          | Nieuw bronveld |
| -------------------------------|------------------|
| cdm_description (omschrijving)  | cdm_name (naam)  |

Daarnaast moet een aanvullende toewijzing worden toegevoegd. Selecteer het laatste veld **Geen** om de volgende toewijzing toe te voegen.

| Bronveld                   | Doelveld    |
| -------------------------------|----------------------|
| cdm_description (omschrijving)  | NAMEALIAS (NAMEALIAS)|

De bijgewerkte toewijzingen moeten hierop lijken.

![Taak Afdelingen naar Operationele eenheden](./media/DepartmentMapping.png)


Voor de taak Taken naar Taakdetails moeten de volgende toewijzingen worden bijgewerkt.

| Bestaand bronveld          | Nieuw bronveld                   |
| -------------------------------|------------------------------------|
| cdm_name (naam)                | cdm_description (omschrijving)      |
| cdm_name (omschrijving)         | cdm_jobdescription (taakomschrijving)|


De bijgewerkte toewijzingen moeten hierop lijken.

![Taak Taken naar Taakdetails](./media/JobMapping.png)

Voor de taak Medewerkers naar Werk moeten de volgende toewijzingen worden bijgewerkt.

| Bestaand bronveld                 | Nieuw bronveld                               |
| --------------------------------------|------------------------------------------------|
| cdm_emailaddress1 (e-mailadres 1)   | cdm_primaryemailaddress (primair e-mailadres) |
| cdm_telephone1 (telefoon 1)          | cdm_primarytelephone (primaire telefoon)       |

De transformatie van het veld Geslacht moet ook worden bijgewerkt. Selecteer het toewijzingtype **fn** (functie) voor Geslacht en werk de volgende waardetoewijzingen bij.

| Common Data Service Waarde   | Finance and Operations waarde | | ------------|------------------ -----------| | 75440000 | Mannelijk                         | | 75440001 | Vrouwelijk                      | | 75440002 | Geen                         | | 75440003    | Niet-specifieke                  |

De bijgewerkte toewijzingen moeten hierop lijken.

![Taak Werknemers naar Werknemer.](./media/WorkerMapping.png)

![Transformatie van veld Geslacht](./media/WorkerTransform.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]