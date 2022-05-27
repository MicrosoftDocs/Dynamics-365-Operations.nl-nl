---
title: Samenvoeging van Dynamics 365 Human Resources-infrastructuur - update van release 10.0.25
description: Dit onderwerp bevat informatie over Microsoft Dynamics 365 Human Resources release 10.0.25, die de eerste wave met mogelijkheden bevat voor de infrastructuursamenvoeging.
author: twheeloc
ms.date: 01/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bf7ce43785e3ef485074f2b0294caea381f8f726
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688087"
---
# <a name="dynamics-365-human-resources-infrastructure-merge---release-10025-update"></a>Samenvoeging van Dynamics 365 Human Resources-infrastructuur - update van release 10.0.25

De release 10.0.25 bevat de eerste wave met functies voor de infrastructuursamenvoeging. Tijdens de infrastructuursamenvoeging wordt Microsoft Dynamics 365 Human Resources samengevoegd met de infrastructuur voor Finance and Operations. Er worden echter ook licenties verleend voor de onafhankelijke toepassing, zoals Dynamics 365 Finance en Dynamics 365 Supply Chain Management. Zie voor meer informatie over de infrastructuursamenvoeging [Veelgestelde vragen over Dynamics 365 Human Resources-infrastructuursamenvoeging](../human-resources/hr-infrastructure-merge-faq.md).

De samenvoeging zorgt voor consistentie voor gebruikers van Human Resources op de volgende manieren:

- [Omgevingsbeheer en integraties zijn consistent tussen de toepassingen Human Resources en Finance and Operations.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/consistent-environment-management-integrations-between-human-resources-finance-operations-apps)

    - Beheer omgevingen in Microsoft Dynamics Lifecycle Services, Problemen zoeken en Regression Suite Automation Tool.
    - Er is één codebasis, waarbij de nieuwe functionaliteit voor Human Resources wordt vrijgegeven als onderdeel van het normale updateproces van One Version.
    - De manier waarop upgrades, updates en hotfixes op omgevingen worden toegepast, is consistent.

- [De uitbreidbaarheidsopties worden verbeterd.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/improve-extensibility-options)

    - U kunt indien nodig Microsoft Power Platform-hulpmiddelen blijven gebruiken om uit te breiden.
    - U kunt functionaliteit uitbreiden via formulieren, tabellen, methoden en Application Programming Interfaces (API's).
    - U kunt entiteiten maken en uitbreiden.

    Zie [Overzicht van uitbreidbaarheid in Dynamics 365](../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) voor meer informatie over de beschikbare uitbreidingsopties.

- [Eén set Human Resources-mogelijkheden maken in Dynamics 365.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/create-one-set-human-resources-capabilities-within-dynamics-365)

    In de versie 10.0.25 zijn functionele mogelijkheden die alleen in Human Resources bestonden, beschikbaar gemaakt in de infrastructuur voor Finance and Operations. Als klanten kunnen profiteren van deze mogelijkheden in een client voor financiële en bedrijfsactiviteiten, moeten de volgende Human Resources-functies zijn ingeschakeld in Functiebeheer.

    | Functienaam | Overzicht | Vrijgavestatus | 
    |--------------|----------|----------------| 
    | Berekening van dienstjaren | Met een instelling kunt u de datum selecteren voor de berekening van **Dienstjaren**. | Algemeen beschikbaar | 
    | Verbeteringen van de werkstroomervaring | Deze functie biedt een verbeterde gebruikerservaring bij het indienen en goedkeuren van werkstromen. | Algemeen beschikbaar | 
    | Prestatiebeoordelingen afdrukken | U kunt prestatiebeoordelingen afdrukken in de PDF-indeling. | Algemeen beschikbaar | 
    | Aangepaste koppelingen in **Selfservice manager** | U kunt aangepaste koppelingen maken die worden weergegeven in de sectie **Verwante koppelingen** van **Selfservice manager**. | Algemeen beschikbaar | 
    | Compensatieweergave voor meerdere bedrijven | Gebruikers kunnen in **Selfservice manager** compensatieplannen voor alle rechtspersonen bekijken, zonder dat ze van bedrijf moeten wisselen. | Algemeen beschikbaar | 
    | Meerdere compensatieniveaus configureren per functie\*&dagger; | Functies ondersteunen nu meerdere compensatieniveaus. | Preview | 
    | Taakbeheer\* | U kunt controlelijsten en taken maken voor onboarding, offboarding en het overgangsproces. | Preview | 
    | Gestroomlijnde werknemerinvoer | Deze functie biedt een bijgewerkte gebruikerservaring op de bestaande pagina **Werknemer**. | Preview | 
    | Verbeteringen in gebruikerservaring voor Human Resources | Zie de tabel in het volgende gedeelte.  | Preview | 

\* Deze functie moet zijn ingeschakeld voordat de functie **Verbetering van de Human Resources-gebruikerservaring** wordt ingeschakeld.

&dagger; Deze functie kan niet worden uitgeschakeld nadat deze is ingeschakeld.

## <a name="human-resource-user-experience-enhancements"></a>Verbeteringen in de Human Resources-gebruikerservaring

| Functienaam | Overzicht | 
|--------------|----------| 
| Aanstelling verwijderen | U kunt een dienstverband van een werknemer verwijderen. | 
| Taakgroepen | U kunt een taakgroep volgen waarin gelijksoortige werkzaamheden worden verricht en waarvoor vergelijkbare training, vaardigheden, kennis en expertise nodig zijn. | 
| Extra dienstverbandvelden | De volgende velden zijn toegevoegd: **Dienstverbandcategorie**, **Type dienstverband** en **Aanstellingsstatus**. | 
| Pagina **Medewerkers zonder dienstverband** | Op deze pagina wordt een lijst weergegeven met werknemers zonder dienstverbandrecord. | 
| Update van gebruikerservaring voor positiedimensies | Er is een verbeterde gebruikerservaring voor het toewijzen van positiedimensies per rechtspersoon. | 
| Adreswijzigingen in het werkgebied **Personeelsbeheer** | Deze functie bevat een telling van alle adreswijzigingen die hebben plaatsgevonden gedurende een aantal dagen dat is opgegeven op de pagina **Human Resources-parameters**. | 
| Vervallen records in het werkgebied **Personeelsbeheer** | Deze functie biedt een lijst met artikelen die zijn vervallen of bijna vervallen voor certificaten, identificaties, proefperioden, screenings of tests. | 
| Pagina **Validatie van positiehiërarchie** | Er wordt een controle uitgevoerd op cirkelverwijzingen in de positieregelhiërarchie. | 
| Landspecifieke salarisgegevens | Er zijn aanvullende salarisvelden beschikbaar op de pagina **Dienstverband werknemer**, afhankelijk van het land of de regio van de rechtspersoon waar de werknemers werken. | 
| Verbeteringen in conformiteitsrapportages | Er zijn aanvullende rapportopties beschikbaar voor EEO-1, Vets 4212 en OSHA300a. | 
| Updates voor het werkgebied **Personeelsbeheer** | Er zijn updates aangebracht om adreswijzigingen en vervaldatums van records bij te houden. Daarnaast worden er nieuwe tabbladen weergegeven met acties voor werknemers en posities. | 
