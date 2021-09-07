---
title: Verschillen tussen ingebouwde hoofdplanning en Planningsoptimalisatie
description: In dit onderwerp worden functies weergegeven die nog niet worden ondersteund door Planningsoptimalisatie en die niet worden weergegeven op de pagina voor het aanpassen van de analyse aan Planningsoptimalisatie.
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a102f1d77362f650c060ce5d0aee5b62d2102532
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344949"
---
# <a name="differences-between-built-in-master-planning-and-planning-optimization"></a>Verschillen tussen ingebouwde hoofdplanning en Planningsoptimalisatie

[!include [banner](../../includes/banner.md)]

De resultaten van de Planningsoptimalisatie kunnen afwijken van de resultaten van de ingebouwde hoofdplannings-engine. De verschillen kunnen worden veroorzaakt door functies die in behandeling zijn. In dit onderwerp worden functies weergegeven die nog niet worden ondersteund door Planningsoptimalisatie en die niet worden weergegeven op de pagina **[Analyse aanpassen aan Planningsoptimalisatie](planning-optimization-fit-analysis.md)**.

| Functie | Huidig gedrag in planningsoptimalisatie |
|---|---|
| Catch weight-producten | Catch-weight-producten worden beschouwd als normale producten.|
| Uitbreidbare dimensies | Uitbreidbare dimensies zijn op geplande orders leeg, zelfs wanneer het selectievakje **Dekkingsplan volgens dimensie** is aangevinkt op de pagina **Opslagdimensiegroepen** of **Traceringsdimensiegroepen**. |
| Gefilterde productieruns | Raadpleeg [Productieplanning - filters](production-planning.md#filters) voor meer informatie. |
| Prognoseplanning | Prognoseplanning wordt niet ondersteund. Wij raden aan dat u hoofdplanning gebruikt waarbij een prognosemodel aan het hoofdplan is toegewezen. |
| Nummerreeksen voor geplande orders | Nummerreeksen voor geplande orders worden niet ondersteund. Geplande ordernummers worden aan de servicekant gegenereerd. |
| Plan kopiëren, plan verwijderen en planversie opschonen | <p>De volgende items zijn uitgeschakeld onder **Hoofdplanning \> Hoofdplanning \> Plannen onderhouden** in het deelvenster voor navigatie:</p><ul><li>Plan kopiëren</li><li>Plan verwijderen</li><li>Versie-opschoning plannen</li></ul> |
| Retourorders | Er wordt geen rekening gehouden met retourorders. |
| Aan planning gerelateerde functies | Raadpleeg [Plannen met onbeperkte capaciteit](infinite-capacity-planning.md#limitations) voor informatie. |
| Transportkalenders | De waarde in de kolom **Transportkalender** op de pagina **Leveringsmethoden** wordt genegeerd. |

## <a name="additional-resources"></a>Aanvullende bronnen

- [Analyse aanpassen aan Planningsoptimalisatie](planning-optimization-fit-analysis.md)
- [Parameters die niet worden gebruikt door Planningsoptimalisatie](not-used-parameters.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
