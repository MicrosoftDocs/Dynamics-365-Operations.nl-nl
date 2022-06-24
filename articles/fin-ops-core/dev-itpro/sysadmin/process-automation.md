---
title: Procesautomatisering
description: Dit artikel biedt informatie over de manier waarop procesautomatisering eenvoudige planning van processen voor de batchserver mogelijk maakt.
author: RyanCCarlson2
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: f13392fd6610735f8c539d42b62cf71cece71fba
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898604"
---
# <a name="process-automation"></a>Procesautomatisering

[!include[banner](../includes/banner.md)]

Procesautomatisering maakt eenvoudige planning van processen voor de batchserver mogelijk. De bijgewerkte kalenderweergave van het geplande werk maakt het eindgebruikers mogelijk geplande en voltooide werkzaamheden weer te geven en daarop actie te ondernemen.

## <a name="administration"></a>Administratie

De centrale beheerpagina voor alle procesautomatiseringen vindt u in de module Systeembeheer onder het menu **Instellingen**. Op deze pagina worden alle geautomatiseerde processen (reeksen) vermeld die in het systeem zijn ingesteld. U kunt hiermee ook rechtstreeks vanaf deze pagina nieuwe procesautomatiseringen toevoegen. Nadat u een reeks hebt ingesteld, kunt u elke reeks in deze lijst beheren. U kunt ervoor kiezen om de gehele reeks te bewerken, deze te verwijderen, alle exemplaren weer te geven in een lijstweergave of de reeks uit te schakelen als u het geplande werk voor een tijdje wilt onderbreken. 

Alle processen die in functiebeheer zijn uitgeschakeld, worden niet weergegeven wanneer de functie is uitgeschakeld. Bovendien worden met de planningsengine voor procesautomatisering geen exemplaren of achtergrondprocessen gepland voor een uitgeschakelde functie. Als u de functie opnieuw inschakelt, worden alle in het verleden geplande gebeurtenissen of achtergrondprocessen onmiddellijk uitgevoerd. De planningsengine voor procesautomatisering is afhankelijk van de systeembatchtaak **Procesautomatisering navragen systeemtaak** die moet worden uitgevoerd. De taak mag op geen enkel moment worden gewijzigd of aan de taak worden geknoeid. 

## <a name="calendar-view"></a>Kalenderweergave

Een van de belangrijkste voordelen van procesautomatisering is de mogelijkheid om het geplande werk in een eenvoudige kalenderweergave te bekijken.  In deze weergave kunt u het werk per week bekijken. U ziet deze weergave wordt aan de rechterkant van de pagina **Procesautomatisering**. De weergave wordt gevuld met het geplande werk voor de geselecteerde reeks. 

[![Kalender met procesautomatisering.](./media/CalendarView2.png)](./media/CalendarView2.png)

## <a name="occurrence-changes"></a>Wijzigingen in exemplaren

Elk exemplaar kan worden gewijzigd zonder dat dit gevolgen heeft voor andere exemplaren die zijn gedefinieerd in de reeks waaruit ze afkomstig zijn. U kunt exemplaren van gepland werk bewerken vanuit de kalenderweergave door de knop **Weergeven/bewerken** te selecteren en op **Exemplaar** te klikken. Op deze pagina hebt u toegang tot alle instellingen die oorspronkelijk werden weergegeven in de configuratiewizard van de reeks. U kunt hier een eenmalige wijziging aanbrengen in het geselecteerde exemplaar. U kunt gepland werk ook uitschakelen door de knop **Uitschakelen** te selecteren in de kalenderweergave.

## <a name="developer-documentation"></a>Documentatie voor ontwikkelaars

Met het raamwerk voor procesautomatisering kunnen ontwikkelaars het raamwerk voor procesautomatisering uitbreiden. De documentatie van [Raamwerk voor procesautomatisering](../process-automation/process-automation-framework.md) bevat informatie over de manier waarop u aangepaste processen kunt maken die moeten worden uitgevoerd door de batchserver die is gepland met de wizard voor procesautomatisering en die automatisch in de kalenderweergave wordt weergegeven.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
