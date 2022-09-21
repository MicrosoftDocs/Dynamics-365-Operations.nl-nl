---
title: Koptekstbesturingselement voor medewerker
description: Dit artikel biedt informatie over het aanpasbare besturingselement voor kopteksten in Werknemerselfservice, in de personenhub en op de pagina Medewerker in Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 09/06/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2867a952df79161aaee657dbc3df1f3298294dd5
ms.sourcegitcommit: 167f73a834629752c6b79c312d744e52df7f0927
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/08/2022
ms.locfileid: "9445944"
---
# <a name="worker-header-control"></a>Koptekstbesturingselement voor medewerker

Microsoft Dynamics 365 Human Resources biedt een aanpasbaar besturingselement voor kopteksten in **Werknemerselfservice**, in de hub **Personen** en op de gestroomlijnde pagina **Medewerker**. De koptekst bevat belangrijke informatie over de werknemer en acties met één klik, zoals e-mailen, telefoneren of berichten sturen. U kunt de koptekst aanpassen door velden te verwijderen of velden, ook aangepaste velden, toe te voegen om extra informatie weer te geven. Als u het nieuwe besturingselement voor kopteksten wilt gebruiken, gaat u naar **Functiebeheer** en schakelt u de functie **Koptekstbesturingselement voor medewerker** in.

## <a name="personalization"></a>Personaliseren

Een van de belangrijkste voordelen van het besturingselement voor werknemerskopteksten is de mogelijkheid om gegevens in de koptekst te personaliseren.

Rechtsboven in de koptekst bevindt zich een groep van drie velden met verschillende gegevens, afhankelijk van de status van de werknemer. Deze groep velden wordt het Spotlight-gedeelte van de koptekst genoemd. U kunt het Spotlight-gedeelte van de koptekst personaliseren door de bestaande velden te verwijderen of velden toe te voegen. De velden die kunnen worden toegevoegd aan het gedeelte Werknemer in het koptekstbesturingselement, verschillen voor **Werknemersself-service**, de hub **Personen** en de pagina **Werknemer**.

## <a name="employee-self-service"></a>Selfservice werknemer

De koptekst voor de werknemer op de pagina **Werknemerselfservice** bevat de volgende informatie:

- Naam werknemer
- Personeelsnummer
- Positienaam
- Afdelingen
- Medewerkertype
- Rechtspersoon van het dienstverband
- Jaren van service
- Rapporteert aan (manager)
- Positietype

De koptekst bevat ook een actie met één klik voor het bewerken van de persoonlijke gegevens van de persoon. Selecteer **Persoonlijke gegevens bewerken** om de pagina **Persoonlijke gegevens** te openen in de **Werknemersself-service**.

## <a name="people-hub"></a>Personenhub

De koptekst van de werknemer in de hub **Personen** (de pagina **Werkgebied personen**) bevat de volgende informatie:

- Naam werknemer
- Personeelsnummer
- Positienaam
- Afdelingen
- Medewerkertype
- Rechtspersoon van het dienstverband
- Jaren van service
- Rapporteert aan (manager)
- Positietype

De koptekst bevat ook acties met één klik, zoals e-mailen, telefoneren of berichten. Als een gebruiker zijn eigen gegevens bekijkt op de pagina **Werkgebied personen**, bevat de sectie met actie met één klik de knop **Persoonlijke gegevens bewerken**. De gebruiker kan op deze knop klikken om de pagina **Persoonlijke gegevens** te openen in de **Werknemersself-service**.

## <a name="streamlined-worker-page"></a>Gestroomlijnde medewerkerpagina

De koptekst voor de werknemer op de gestroomlijnde pagina **Medewerker** bevat de volgende informatie:

- Naam werknemer
- Personeelsnummer
- Positienaam
- Afdelingen
- Medewerkertype
- Rechtspersoon van het dienstverband

Afhankelijk van de status van de werknemer, kunnen andere gegevens worden getoond in de koptekst. Als de werknemer bijvoorbeeld het bedrijf heeft verlaten, bevat het koptekstbesturingselement een badge **Vertrokken**, de einddatum van het dienstverband en de reden voor beëindiging.

In de volgende tabel worden de gegevens getoond die in de koptekst staan voor verschillende werknemerstatussen.

| Werknemerstatus | Getoonde gegevens | Notitie |
|-----------------|--------------------|------|
| In behandeling | <ul><li>Name</li><li>Personeelsnummer</li><li>Positienaam</li><li>Afdeling</li><li>Medewerkertype</li><li>Rechtspersoon</li><li>Badge In behandeling</li><li>Begindatum</li><li>Rapporteert aan</li><li>Positietype</li></ul> | |
| Recente aanstelling | <ul><li>Name</li><li>Personeelsnummer</li><li>Positienaam</li><li>Afdeling</li><li>Medewerkertype</li><li>Rechtspersoon</li><li>Badge Recente aanstelling</li><li>Jaren van service</li><li>Rapporteert aan</li><li>Positietype</li></ul> | De badge voor **Recente aanstelling** wordt standaard getoond voor werknemers die in de afgelopen zeven dagen zijn aangenomen. Als u deze instelling wilt wijzigen, voert u op de pagina **Human Resources-parameters** op het tabblad **Algemeen** in het veld **Datumbereik voor recente aanstellingen** een tijdsperiode in. Als u bijvoorbeeld de badge **Recente aanstelling** wilt weergeven met medewerkers die in de afgelopen 14 dagen zijn aangenomen, stelt u het veld **Periode** in op **14** en stelt u het veld **Eenheid** in op **Dagen**. |
| Actieve werknemer | <ul><li>Name</li><li>Personeelsnummer</li><li>Positienaam</li><li>Afdeling</li><li>Medewerkertype</li><li>Rechtspersoon</li><li>Begindatum</li><li>Rapporteert aan</li><li>Positietype</li></ul> | |
| Afsluiten | <ul><li>Name</li><li>Personeelsnummer</li><li>Positienaam</li><li>Afdeling</li><li>Medewerkertype</li><li>Rechtspersoon</li><li>Badge Vertrekt</li><li>Jaren van service</li><li>Rapporteert aan</li><li>Positietype</li></ul> | Standaard wordt de badge **Vertrekt** getoond voor werknemers waarvan in de volgende zeven dagen het dienstverband afloopt. Als u deze instelling wilt wijzigen, voert u op de pagina **Human Resources-parameters** op het tabblad **Algemeen** in het veld **Datumbereik voor vertrekkende medewerkers** een tijdsperiode in. Als u bijvoorbeeld de badge **Vertrekt** wilt weergeven met medewerkers die in de komende 14 dagen het bedrijf verlaten, stelt u het veld **Periode** in op **14** en stelt u het veld **Eenheid** in op **Dagen**. |
| Vertrokken | <ul><li>Badge Vertrokken</li><li>Personeelsnummer</li><li>Einddatum dienstverband</li><li>Redencode</li></ul> | Standaard wordt de badge **Vertrokken** getoond voor werknemers die in de afgelopen zeven dagen het bedrijf hebben verlaten. Als u deze instelling wilt wijzigen, voert u op de pagina **Human Resources-parameters** op het tabblad **Algemeen** in het veld **Datumbereik voor vertrokken medewerkers** een tijdsperiode in. Als u bijvoorbeeld de badge **Vertrokken** wilt weergeven met medewerkers die in de afgelopen 14 dagen het bedrijf hebben verlaten, stelt u het veld **Periode** in op **14** en stelt u het veld **Eenheid** in op **Dagen**. |
