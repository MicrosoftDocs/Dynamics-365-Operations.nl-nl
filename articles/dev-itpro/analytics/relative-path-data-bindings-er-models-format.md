---
title: Een relatief pad gebruiken in gegevensbindingen van ER-modellen en -indelingen
description: .
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable , ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6582cca9b912868f88de2770a17cbb6e67328660
ms.sourcegitcommit: d0fa7eb2166a30314205e7f70bbeaff6fbd5fb55
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/03/2019
ms.locfileid: "1726547"
---
# <a name="use-a-relative-path-in-data-bindings-of-er-models-and-formats"></a>Een relatief pad gebruiken in gegevensbindingen van ER-modellen en -indelingen

[!include[banner](../includes/banner.md)]

Met het hulpprogramma voor elektronische rapportage (ER) kunnen gebruikers elektronische indelingsstructuren definiëren en vervolgens beschrijven hoe deze structuren moeten worden gevuld met behulp van gegevens en algoritmen uit Dynamics 365 for Finance and Operations. Zie [ER-configuraties (Elektronische rapportage) maken](electronic-reporting-configuration.md) voor meer informatie. Als u de gegevensstroom wilt opgeven voor het ophalen van gegevens uit Finance and Operations en het gebruik ervan om een elektronisch document te genereren, moet u het volgende doen:

- De geconfigureerde gegevensbronnen binden aan elementen van het ontworpen domeinspecifieke gegevensmodel. De modelstructuur en de geselecteerde gegevensbronnen kunnen deel uitmaken van een complexe hiërarchische structuur. Hierdoor kunnen eindbindingen vrij groot zijn en vele elementen van verschillende typen bevatten (bijvoorbeeld relaties, tabellen en methoden). De bindingen kunnen minder goed leesbaar worden en zijn zeer ingewikkeld om te controleren en te begrijpen, vooral voor niet-eigenaars. 
- Gegevensmodelelementen binden met indelingscomponenten om te definiëren welke gegevens uit het gegevensmodel de gegenereerde indelingsoutput zullen vullen.

De functie relatief pad is vrijgegeven om de bruikbaarheid van ontwerpers van ER‑toewijzing te verbeteren. De optie relatief pad weergave is standaard ingeschakeld voor elk nieuw exemplaar van Finance and Operations waarvoor de ER‑ontwerpervaring is ingeschakeld (Microsoft Dynamics 365 for Finance and Operations, Microsoft Regulatory Configuration Service). We hebben de relatieve pad parameter geïmplementeerd, zodat gebruikers het volledige pad kunnen blijven gebruiken wanneer ze met deze weergave van ER-bindingen werken.

[![Gebruikersparameters](./media/relative-path-01.png)](./media/relative-path-01.png)

 
Wanneer de gebruiksparameter van het relatieve pad is ingeschakeld, vervangt een enkel @-teken het pad naar het bovenliggende item in de binding van het huidige modelelement. Het gehele bindingstraject wordt korter, waardoor de volledige toewijzing duidelijker en begrijpelijker wordt. In de meeste gevallen is er geen extra scrollen nodig in de ER-ontwerper om alle bindingen van het datamodel te bekijken.

[![Ontwerper modeltoewijzing](./media/relative-path-02.png)](./media/relative-path-02.png)
 
Wanneer u begint met het ontwerpen van een nieuwe ER-expressie, hoeft u slechts één teken in te voeren om een binding te definiëren met een veld van het bovenliggende item.

[![Formuleontwerper](./media/relative-path-03.png)](./media/relative-path-03.png)
 
Wanneer u besluit de gegeven bron van het bovenliggende model te wijzigen, met gebruik van absolute paden, moet u dit modelitem, evenals alle geneste items, handmatig opnieuw binden aan een nieuwe gegevensbron. Wanneer het gebruik van een relatief pad is ingeschakeld en u selecteert een nieuwe gegevensbron die aan een bovenliggend item moet worden gebonden, krijgt u de mogelijkheid om alle geneste elementen van dit bovenliggende item automatisch opnieuw te binden met één klik.

[![Bericht bestaand pad vervangen](./media/relative-path-04.png)](./media/relative-path-04.png)
 
Als u de rebinding van geneste items bevestigt, wordt het nieuwe bovenliggende item geplaatst in het pad van elk genest item dat het bestaande bovenliggende item bevat.
Deze functie verbreekt niet de achterwaartse compatibiliteit van het ER-raamwerk. Alle eerder ontworpen ER‑configuraties werken met deze nieuwe functie en er zijn geen upgrades of conversies vereist.

> [!NOTE]
> Alle wijzigingen die worden geïntroduceerd door het groepsgewijs wijzigen van bindingen van geneste elementen in modeltoewijzingen worden correct opgeslagen in een configuratiedelta (tracering van wijzigingen). Hierdoor kunnen klanten de afgeleide versie van modeltoewijzingen opnieuw baseren op een nieuwe basisversie die is gewijzigd door deze nieuwe functie te gebruiken.