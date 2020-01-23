---
title: Wat is nieuw of gewijzigd in Dynamics 365 Talent - Core HR (15 november 2018)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
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
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1a7598db1dc4c11864cf5f5a73d00672ceb66e8c
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897461"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-november-15-2018"></a>Wat is nieuw of gewijzigd in Dynamics 365 Talent - Core HR (15 november 2018)

**Build 8.1.2045**

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Core HR.

## <a name="other-changesfixes"></a>Andere wijzigingen/oplossingen

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a>Kan de huidige positie van een werknemer niet wijzigen in een toekomstige open positie

Er is een wijziging doorgevoerd om positiewijzigingen mogelijk te maken wanneer de positie alleen in de toekomst beschikbaar is. 

### <a name="position-does-not-display-when-creating-a-new-employee"></a>De positie wordt niet weergegeven bij het maken van een nieuwe werknemer

Er is een wijziging doorgevoerd om alle openstaande posities weer te geven die beschikbaar zijn voor toewijzing wanneer er nieuwe werknemers worden aangenomen in Talent. Dit zijn ook historische posities of posities met een toekomstige datum. Posities worden nu correct weergegeven op basis van de begindatum van het dienstverband. 

### <a name="termination-date-is-displaying-based-on-user-settings"></a>De ontslagdatum wordt weergegeven op basis van gebruikersinstellingen

Er is een wijziging doorgevoerd in de lijst met vroegere werknemers om eventuele tijdzoneverschillen met de voorkeurstijdzone van werknemers bij het weergeven van de ontslagdatum te compenseren.

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a>De koppelingen Aan mij toegewezen werkitems bevatten niet de juiste informatie

Met deze wijziging wordt bij navigatie naar de details van de afzonderlijke werkitems in de lijst de juiste informatie voor het geselecteerde item weergegeven. Dit probleem trad alleen op bij geavanceerde beveiligingsopties.


## <a name="known-issue"></a>Bekend probleem

- **Probleem**: bij het toevoegen van een nieuwe bijlage aan een werknemer zijn de knoppen **Nieuw** en **Bewerken** niet beschikbaar. 
- **Tijdelijke oplossing:** voordat u de bijlagepagina opent, controleert u of de feitenvakken op de pagina **Werknemer** zijn gesloten. Als de feitenvakken worden gesloten wanneer de pagina **Werknemer** wordt geladen, worden de bijlageknoppen ingeschakeld. (Dit probleem wordt opgelost in de volgende platformupdate.)
