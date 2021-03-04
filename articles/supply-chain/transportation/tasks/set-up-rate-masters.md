---
title: Tariefmodellen instellen
description: Deze procedure laat zien hoe u een tariefmodel instelt.
author: ShylaThompson
manager: tfehr
ms.date: 10/16/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSBreakMaster,TMSRateMaster,TMSRateMasterBase,TMSRateBaseType, TMSRouteWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4cca9fd47a5d8c81d7b8a913d0a467bc113b584
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/29/2020
ms.locfileid: "4425905"
---
# <a name="set-up-rate-masters"></a>Tariefmodellen instellen

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u een tariefmodel instelt. De logistiek manager stelt meestal tariefmodellen in, afhankelijk van de contracten die met de vervoerders worden ondertekend. In dit scenario gaat u een tariefmodel instellen voor een luchtvaartmaatschappij. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.

## <a name="set-up-break-master"></a>Een pauzemodel instellen

1. Ga naar **Transportbeheer > Instellingen > Beoordeling > Pauzemodel**. Pauzemodellen worden gebruikt om de prijsstructuur en de onderbrekingspunten te definiëren. De prijsstructuur maakt gebruik van gelaagde prijzen die op fysieke afmetingen zijn gebaseerd.  
1. Selecteer **Nieuw**.
1. Voer een waarde in het veld **Pauzemodel** in.
1. Voer een waarde in het veld **Naam** in.
1. Selecteer in het veld **Gegevenstype** het gegevenstype.
1. Voer in het veld **Vergelijking** het gewenste type vergelijking in (met behulp van operatoren).
1. Voer in het veld **Pauze-eenheid** de pauze-eenheid in.
1. Maak in de sectie **Details** zoveel pauzes als nodig zijn voor de prijsstructuur.
1. Selecteer **Opslaan**.

## <a name="set-up-rate-master"></a>Tariefmodel instellen

1. Ga naar **Transportbeheer > Instellingen > Beoordeling > Tariefmodel**.
1. Selecteer **Nieuw**.
1. Typ een waarde in het veld **Tariefmodel**.
1. Typ een waarde in het veld **Naam**.
1. Selecteer in het veld **Id metagegevens beoordeling** de vervolgkeuzeknop om de zoekopdracht te openen. De metagegevens-id van de beoordeling bepaalt welke gegevens nodig zijn voor het tariefmodel, aangezien hiermee de metagegevens worden gedefinieerd die de Transportbeheerengine verwacht bij gebruik van dit tariefmodel.  
1. Selecteer voor dit voorbeeld de optie P2P. Dit is al gedefinieerd in de demogegevens.
1. Selecteer in de lijst de koppeling in de geselecteerde rij.
1. Selecteer **Opslaan**.

## <a name="set-up-rate-base"></a>Tariefbasis instellen

1. Selecteer **Tariefbasis**.
    * De tariefbasis bepaalt het tarief van de vervoerder en kan worden gebruikt voor het instellen van een tariefstructuur aangezien het de tarieven in de onderbrekingspunten structureert die in het pauzemodel zijn gedefinieerd.  
2. Selecteer **Nieuw**.
3. Typ een waarde in het veld **Tariefbasis**.
4. Typ een waarde in het veld **Naam**.
5. Selecteer in het veld **Pauzemodel** de vervolgkeuzeknop om de zoekopdracht te openen.
    * Pauzemodellen worden gebruikt om de prijsstructuur en de onderbrekingspunten te definiëren. De prijsstructuur maakt gebruik van gelaagde prijzen die op fysieke afmetingen zijn gebaseerd.  
6. Gebruik gewicht voor dit voorbeeld. Dit is al gedefinieerd in de demogegevens.
7. Selecteer in de lijst de koppeling in de gemarkeerde rij.
8. Vouw de sectie **Details** uit.
9. Selecteer **Nieuw**.
10. Typ "30301" in het veld **Postcode van aflevering van**.
11. Typ "30318" in het veld **Postcode van aflevering naar**.
12. Typ "VS" in het veld **Afleverland/regio**.
13. Typ "100" in het veld **< 1,00 pond**.
    * Voeg het tarief per pond in als het totale gewicht van de lading minder dan 1 pond is.  
14. Typ "300" in het veld **< 5,00 pond**.
    * Voeg het tarief per pond in als het totale gewicht van de lading minder dan 5 pond is.  
15. Typ "500" in het veld **< 20,00 pond**.
    * Voeg het tarief per pond in als het totale gewicht van de lading minder dan 20 pond is.  
16. Typ "1000" in het veld **< 100,00 pond**.
    * Voeg het tarief per pond in als het totale gewicht van de lading minder dan 100 pond is.  
17. Typ "3000" in het veld **< 1000,00 pond**.
    * Voeg het tarief per pond in als het totale gewicht van de lading minder dan 1000 pond is.  
18. Selecteer **Opslaan**.
19. Sluit de pagina.

## <a name="assign-rate-base"></a>Tariefbasis toewijzen

1. Vouw de sectie **Toewijzingen tariefbasis** uit.
2. Selecteer **Nieuw**.
    * U kunt verschillende toewijzingen tariefbasis hebben voor elk tariefmodel. Dit maakt het mogelijk om verschillende prijspunten voor elke vervoerder te maken afhankelijk van bestemmingen, services of verschillende tariefbasissen. In deze procedure kunt u alleen één toewijzing tariefbasis maken.  
3. Typ een waarde in het veld **Naam**.
4. Selecteer in het veld **Tariefbasis** de vervolgkeuzeknop om de zoekopdracht te openen.
5. Selecteer in de lijst de koppeling in de gemarkeerde rij.
6. Selecteer in het veld **Service** de vervolgkeuzeknop om de zoekopdracht te openen.
7. Zoek en selecteer de gewenste record in de lijst.
8. Selecteer in de lijst de koppeling in de gemarkeerde rij.
9. Typ "98052" in het veld **Postcode voor ophalen**.
    * Geef op vanaf welke postcode deze toewijzing van de tariefbasis geldig moet zijn.
10. Typ "VS" in het veld **Land/regio voor ophalen**.
11. Selecteer **Opslaan**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]