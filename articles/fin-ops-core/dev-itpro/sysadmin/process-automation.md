---
title: Procesautomatisering
description: Dit onderwerp biedt informatie over de manier waarop procesautomatisering eenvoudige planning van processen voor de batchserver mogelijk maakt.
author: RyanCCarlson2
manager: tonyafehr
ms.date: 08/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 320e18f7fc61300ed2966afef530907fc9fc5ca5
ms.sourcegitcommit: e2a47d31175bbd60acfd7a23ffea70c669358572
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2020
ms.locfileid: "3690041"
---
# <a name="process-automation"></a>Procesautomatisering

[!include[banner](../includes/banner.md)]

Procesautomatisering maakt eenvoudige planning van processen voor de batchserver mogelijk. De bijgewerkte kalenderweergave van het geplande werk maakt het eindgebruikers mogelijk geplande en voltooide werkzaamheden weer te geven en daarop actie te ondernemen.

## <a name="administration"></a>Administratie

De centrale beheerpagina voor alle procesautomatiseringen vindt u in de module Systeembeheer onder het menu **Instellingen**. Op deze pagina worden alle geautomatiseerde processen (reeksen) vermeld die in het systeem zijn ingesteld. U kunt hiermee ook rechtstreeks vanaf deze pagina nieuwe procesautomatiseringen toevoegen. Nadat u een reeks hebt ingesteld, kunt u elke reeks in deze lijst beheren. U kunt ervoor kiezen om de gehele reeks te bewerken, deze te verwijderen, alle exemplaren weer te geven in een lijstweergave of de reeks uit te schakelen als u het geplande werk gedurende een bepaalde periode wilt onderbreken. 

Alle processen die in functiebeheer zijn uitgeschakeld, worden niet weergegeven wanneer de functie is uitgeschakeld. Bovendien zal de planningsengine voor procesautomatisering geen exemplaren of achtergrondprocessen plannen voor een uitgeschakelde functie. Als u de functie opnieuw inschakelt, worden alle in het verleden geplande gebeurtenissen of achtergrondprocessen onmiddellijk uitgevoerd.

## <a name="calendar-view"></a>Kalenderweergave 
Een van de belangrijkste voordelen van procesautomatisering is de mogelijkheid om het geplande werk in een eenvoudige kalenderweergave te bekijken.  In deze weergave kunt u het werk per week bekijken. Deze weergave wordt aan de rechterkant van de pagina **Procesautomatisering** weergegeven. De weergave wordt gevuld met het geplande werk voor de geselecteerde reeks. 

[![Kalender met procesautomatisering](./media/CalendarView2.png)](./media/CalendarView2.png)

## <a name="occurrence-changes"></a>Wijzigingen in exemplaren
Elk exemplaar kan worden gewijzigd zonder dat dit gevolgen heeft voor andere exemplaren die zijn gedefinieerd in de reeks waaruit ze afkomstig zijn. U kunt exemplaren van gepland werk bewerken vanuit de kalenderweergave door de knop **Weergeven/bewerken** te selecteren en op **Exemplaar** te klikken. Op deze manier hebt u toegang tot alle instellingen die oorspronkelijk werden weergegeven in de configuratiewizard van de reeks. U kunt hier een eenmalige wijziging aanbrengen in het geselecteerde exemplaar. U kunt gepland werk ook uitschakelen door de knop **Uitschakelen** te selecteren in de kalenderweergave. 

## <a name="developer-documentation"></a>Documentatie voor ontwikkelaars 
Documentatie voor ontwikkelaars wordt momenteel geschreven om ontwikkelaars in staat te stellen het raamwerk voor procesautomatisering uit te breiden. In deze documentatie vindt u informatie over de manier waarop u aangepaste processen kunt maken, die moeten worden uitgevoerd door de batchserver die is gepland met de wizard voor procesautomatisering en die automatisch in de kalenderweergave wordt weergegeven.
