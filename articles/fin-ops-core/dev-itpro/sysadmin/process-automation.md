---
title: Procesautomatisering
description: Dit artikel biedt informatie over de manier waarop procesautomatisering eenvoudige planning van processen voor de batchserver mogelijk maakt.
author: RyanCCarlson2
ms.date: 06/29/2022
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
ms.openlocfilehash: 1a1d152a01e0ebe6a20e2e6b31f12ed7b8deb024
ms.sourcegitcommit: 07ed6f04dcf92a2154777333651fefe3206a817a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2022
ms.locfileid: "9423954"
---
# <a name="process-automation"></a>Procesautomatisering

[!include[banner](../includes/banner.md)]

Procesautomatisering maakt eenvoudige planning van processen voor de batchserver mogelijk. De bijgewerkte kalenderweergave van het geplande werk maakt het eindgebruikers mogelijk geplande en voltooide werkzaamheden weer te geven en daarop actie te ondernemen.

## <a name="administration"></a>Administratie

De centrale beheerpagina voor alle procesautomatiseringen vindt u in de module Systeembeheer onder het menu **Instellingen**. Op deze pagina worden alle geautomatiseerde processen (reeksen) vermeld die in het systeem zijn ingesteld. U kunt hiermee ook rechtstreeks vanaf deze pagina nieuwe procesautomatiseringen toevoegen. Nadat u een reeks hebt ingesteld, kunt u elke reeks in deze lijst beheren. U kunt ervoor kiezen om de gehele reeks te bewerken, deze te verwijderen, alle exemplaren weer te geven in een lijstweergave of de reeks uit te schakelen als u het geplande werk voor een tijdje wilt onderbreken. 

Met het tabblad **Achtergrondprocessen** op deze pagina kunt u achtergrondprocessen beheren die in uw omgeving worden uitgevoerd. Selecteer **Bewerken** om planningswijzigingen aan te brengen voor een achtergrondproces. Deze wijzigingen kunnen een slaapstandperiode bevatten waardoor het proces elke dag sluimert of wordt onderbroken voor een bepaalde periode. Selecteer **Meest recente resultaten weergeven** om de uitvoeringsresultaten voor elk achtergrondproces weer te geven.

Alle processen die in functiebeheer zijn uitgeschakeld, worden niet weergegeven wanneer de functie is uitgeschakeld. Bovendien worden met de planningsengine voor procesautomatisering geen exemplaren of achtergrondprocessen gepland voor een uitgeschakelde functie. Als u de functie opnieuw inschakelt, worden alle in het verleden geplande gebeurtenissen of achtergrondprocessen onmiddellijk uitgevoerd. De planningsengine voor procesautomatisering is afhankelijk van de systeembatchtaak **Procesautomatisering navragen systeemtaak** die moet worden uitgevoerd. De taak mag op geen enkel moment worden gewijzigd of aan de taak worden geknoeid. Als deze batchtaak niet wordt uitgevoerd of als de batch een foutstatus heeft, selecteert u **Procesautomatisering initialiseren** om de batchtaak opnieuw in te stellen. Door deze reset worden alle nieuwe geautomatiseerde programma's die in een recentere versie van de toepassing zijn vrijgegeven, geïnitialiseerd. 

## <a name="calendar-view"></a>Kalenderweergave

Een van de belangrijkste voordelen van procesautomatisering is de mogelijkheid om het geplande werk in een eenvoudige kalenderweergave te bekijken.  In deze weergave kunt u het werk per week bekijken. U ziet deze weergave wordt aan de rechterkant van de pagina **Procesautomatisering**. De weergave wordt gevuld met het geplande werk voor de geselecteerde reeks. 

[![Kalender met procesautomatisering.](./media/CalendarView2.png)](./media/CalendarView2.png)

## <a name="occurrence-changes"></a>Wijzigingen in exemplaren

Elk exemplaar kan worden gewijzigd zonder dat dit gevolgen heeft voor andere exemplaren die zijn gedefinieerd in de reeks waaruit ze afkomstig zijn. U kunt exemplaren van gepland werk bewerken vanuit de kalenderweergave door de knop **Weergeven/bewerken** te selecteren en op **Exemplaar** te klikken. Op deze pagina hebt u toegang tot alle instellingen die oorspronkelijk werden weergegeven in de configuratiewizard van de reeks. U kunt hier een eenmalige wijziging aanbrengen in het geselecteerde exemplaar. U kunt gepland werk ook uitschakelen door de knop **Uitschakelen** te selecteren in de kalenderweergave.

## <a name="developer-documentation"></a>Documentatie voor ontwikkelaars

Met het raamwerk voor procesautomatisering kunnen ontwikkelaars het raamwerk voor procesautomatisering uitbreiden. De documentatie van [Raamwerk voor procesautomatisering](../process-automation/process-automation-framework.md) bevat informatie over de manier waarop u aangepaste processen kunt maken die moeten worden uitgevoerd door de batchserver die is gepland met de wizard voor procesautomatisering en die automatisch in de kalenderweergave wordt weergegeven.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
