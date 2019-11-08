---
title: Wat is nieuw of gewijzigd in Dynamics 365 Talent - Core HR (16 oktober 2018)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
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
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0d7c6562ca8b5e7cfa0071ec408955e13a46cb6e
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551698"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-16-2018"></a>Wat is nieuw of gewijzigd in Dynamics 365 Talent - Core HR (16 oktober 2018)

[!include[banner](includes/banner.md)]

**Build 8.1.1067**

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Core HR.

## <a name="allow-managers-to-update-time-off-requests"></a>Managers toestaan verlofaanvragen bij te werken

Verlofaanvragen van werknemers moeten mogelijk worden bijgewerkt nadat ze zijn goedgekeurd via de workflow. In veel gevallen brengt de manager deze updates aan namens de werknemer. Deze nieuwe functie biedt de mogelijkheid voor managers om verlof bij te werken of verlofaanvragen te annuleren namens hun werknemers. Deze mogelijkheid wordt bepaald door de parameter **Werken namens** die kan worden ingesteld op de pagina **Parameters personeel**. 
 
## <a name="allow-hr-to-update-time-off-requests"></a>HR-managers toestaan verlofaanvragen bij te werken

Net als bij de bovenstaande functie moeten verlofaanvragen van werknemers mogelijk door HR worden bijgewerkt nadat ze eerder zijn goedgekeurd via de werkstroom. Deze functie biedt de mogelijkheid voor HR-gebruikers om verlofaanvragen bij te werken. De mogelijkheid wordt ingeschakeld in het werkgebied **Mensen** en op de pagina **Medewerker** met behulp van een nieuwe optie genaamd **Tijd vrijaf weergeven**. Op deze pagina's kunnen HR-gebruikers aanvragen weergeven en verloftransacties bijwerken, net zoals managers deze acties kunnen uitvoeren.

Dit is de beveiligingsfunctie die toegang tot deze functionaliteit bepaalt:
- Functie: medewerkerspecifieke verlof- en verzuimprocessen onderhouden.
- Bevoegdheid: verlof- en verzuimaanvragen onderhouden voor alle medewerkers.

## <a name="other-changes"></a>Andere wijzigingen
De volgende updates zijn aangebracht in deze release:
- Wijzigingen in acties voor het aanstellen van medewerkers, zodat ze niet meer "vastzitten" in de status **Workflow voltooid**.
- Dienstverbandrecord kan nu worden gemaakt zonder een begindatum van het dienstverband.
- De registratiedatum van Dynamics 365 Talent voor een cursus die wordt weergegeven in de Werknemers-self-service past nu de tijdzoneverschuiving op de datum toe.
- Excel-bestanden kunnen meerdere keren worden geïmporteerd zonder fouten met **Werknemersentiteit**.

## <a name="known-issue"></a>Bekend probleem

- **Probleem**: bij het toevoegen van een nieuwe bijlage aan een werknemer zijn de knoppen **Nieuw** en **Bewerken** niet beschikbaar. 
- **Tijdelijke oplossing:** voordat u de bijlagepagina opent, controleert u of de feitenvakken op de pagina **Werknemer** zijn gesloten. Als de feitenvakken worden gesloten wanneer de pagina **Werknemer** wordt geladen, worden de bijlageknoppen ingeschakeld. (Dit probleem wordt opgelost in de volgende platformupdate.)
