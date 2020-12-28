---
title: Gestroomlijnde invoer en navigatie voor werknemers
description: De gegevensinvoer voor medewerkers in Dynamics 365 Talent is verbeterd om snelle invoer mogelijk te maken voor alle medewerkers (vroegere, actieve en toekomstige medewerkers). Een vereenvoudigd/geconsolideerd navigatiemodel is bijgewerkt om snel gerelateerde informatie te vinden en eventueel benodigde updates te bekijken en toe te passen.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent October 2019 update
ms.openlocfilehash: b73b420c2eb75077814fbfeb6cd17404c7efc11e
ms.sourcegitcommit: 436731d8b3889bebfe6f17922b0a31b1994f6796
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/26/2020
ms.locfileid: "4460866"
---
# <a name="streamlined-employee-entry-and-navigation"></a>Gestroomlijnde invoer en navigatie voor werknemers

In Dynamics 365 Talent kunnen van medewerkers- en aanstellingsgegevens efficiënt worden ingevoerd. U kunt werkhistoriegegevens snel bijwerken voor vroegere, actieve en toekomstige medewerkers en contractanten.

U kunt ook een vereenvoudigde navigatie-ervaring inschakelen om snel gerelateerde informatie te vinden en de nodige wijzigingen aan te brengen. Deze functionaliteit is nu beschikbaar in alle sandbox-omgevingen. Als u deze functie wilt inschakelen, navigeert u naar **Systeembeheer > Functiebeheer > Nieuw > Gestroomlijnde invoer voor werknemers > Inschakelen**. Hierdoor worden deze wijzigingen voor alle gebruikers ingeschakeld. U kunt deze optie op elk gewenst moment uitschakelen.

## <a name="view-options"></a>Opties weergeven

U kunt **Weergaveopties** in het medewerkersformulier gebruiken om een combinatie van medewerkers en contractanten in één lijst te selecteren. Met deze opties kunt u medewerkers in verschillende rechtspersonen of voor de rechtspersoon waarbij u momenteel bent aangemeld weergeven. U kunt ook actieve, in behandeling zijnde en afgesloten medewerkers weergeven en u kunt resultaten beperken op basis van het type medewerker (werknemer of contractant). Als geavanceerde beveiliging is ingeschakeld, worden alleen die medewerkers en contractanten weergegeven voor de rechtspersonen waartoe u toegang hebt.

De kolommen in de lijstweergave worden gewijzigd op basis van uw selecties. Wanneer u afgesloten medewerkers weergeeft, worden de ontslagdatum en redencodes weergegeven als extra kolommen in de lijst. 

[![Opties weergeven](./media/Worker-view-option.png)](./media/worker-view-option.png)

## <a name="navigation-and-banner"></a>Navigatie en banner

In een banner worden belangrijke gegevens voor elke medewerker weergegeven. In de banner voor actieve medewerkers worden de volgende velden weergegeven:

- **Titel**
- **Departement**
- **Positietype**
- **Type medewerker**
- **Manager**
- **Rechtspersoon**

In de banner voor afgesloten medewerkers worden de volgende velden weergegeven:

- **Datum afgesloten**
- **Reden**

In de banner voor medewerkers in behandeling worden de volgende velden weergegeven:

- **Titel**
- **Departement**
- **Positietype**
- **Manager**
- **Begindatum**
- **Rechtspersoon**

Het actievenster van de medewerkerspagina is opnieuw geordend zodat er minder opties worden weergegeven. Gegevens zijn nu ingedeeld in de volgende categorieën: 

- Werk
- Persoon
- Verlof
- Compensatie
- Voordelen
- Conformiteit

Daarnaast biedt een nieuw tabblad **Koppelingen** op de hoofdmedewerkerspagina gebruikers een centrale locatie voor toegang tot alle gerelateerde informatie voor een medewerker.

Door deze wijzigingen kan informatie op een andere locatie worden weergegeven dan u gewend bent. Salarisgegevens, die eerder in het medewerkersformulier werden weergegeven, worden nu weergegeven in het actievenster onder **Compensatie > Salaris** en op het tabblad **Persoonlijke informatie** bevindt zich nu een knop **Meer informatie** om velden te verbergen die vaak niet worden geopend.

[![Banner](./media/Banner.png)](./media/Banner.png)

## <a name="work-history"></a>Werkhistorie

Op het tabblad **Werkhistorie** wordt de werkhistorie voor alle rechtspersonen weergegeven en deze is beschikbaar voor afgesloten, actieve en in behandeling zijnde medewerkers en contractanten. U kunt nu de hele werkhistorie tegelijk bekijken voor de rechtspersonen waartoe u toegang hebt. Bovendien kunt u gegevens voor elk van de werkhistorie-items bewerken zonder de gegevenscontext te wijzigen. U kunt alle informatie rechtstreeks op de pagina bijwerken. 

[![Werkhistorie](./media/Worker-work-history.png)](./media/Worker-work-history.png)

## <a name="position-history"></a>Positiehistorie

Op het tabblad **Posities** op de hoofdpagina van een medewerker wordt een volledig overzicht weergegeven van alle posities binnen de organisatie, waaronder vroegere, huidige en toekomstige aanstellingen. U kunt ook nog steeds rechtstreeks naar de positiehistorie van de medewerker gaan vanuit het actievenster.

[![Posities](./media/Worker-position-history.png)](./media/Worker-position-history.png)

