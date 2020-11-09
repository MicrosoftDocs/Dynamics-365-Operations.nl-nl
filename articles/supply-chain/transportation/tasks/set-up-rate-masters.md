---
title: Tariefmodellen instellen
description: Deze procedure laat zien hoe u een tariefmodel instelt.
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRouteWorkbench, TMSRateMaster, TMSRateBaseType
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 72d71aa15f8cec532980f412ff1cb48e142c4cb1
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016465"
---
# <a name="set-up-rate-masters"></a>Tariefmodellen instellen

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u een tariefmodel instelt. De logistiek manager stelt meestal tariefmodellen in, afhankelijk van de contracten die met de vervoerders worden ondertekend. In dit scenario gaat u een tariefmodel instellen voor een luchtvaartmaatschappij. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.


## <a name="set-up-rate-master"></a>Tariefmodel instellen
1. Ga naar Transportbeheer > Instellingen > Beoordeling > Tariefmodel.
2. Klik op Nieuw.
3. Typ een waarde in het veld Tariefmodel.
4. Typ een waarde in het veld Naam.
5. Klik in het veld Id metagegevens beoordeling op de vervolgkeuzeknop om de zoekopdracht te openen.
    * De id metagegevens beoordeling bepaalt welke gegevens nodig zijn voor het tariefmodel, aangezien het de metagegevens definieert die de TMS-engine verwacht bij gebruik van dit tariefmodel.  
6. Selecteer voor dit voorbeeld de optie P2P
7. Klik in de lijst op de koppeling in de geselecteerde rij.
8. Klik op Opslaan.

## <a name="set-up-rate-base"></a>Tariefbasis instellen
1. Klik op Tariefbasis.
    * De tariefbasis bepaalt het tarief van de vervoerder en kan worden gebruikt voor het instellen van een tariefstructuur aangezien het de tarieven in de onderbrekingspunten structureert die in het pauzemodel zijn gedefinieerd.  
2. Klik op Nieuw.
3. Typ een waarde in het veld Tariefbasis.
4. Typ een waarde in het veld Naam.
5. Klik in het veld Pauzemodel op de vervolgkeuzeknop om de zoekopdracht te openen.
    * Pauzemodellen worden gebruikt om de prijsstructuur en de onderbrekingspunten te definiëren. De prijsstructuur maakt gebruik van gelaagde prijzen die op fysieke afmetingen zijn gebaseerd.  
6. Gebruik gewicht voor dit voorbeeld
7. Klik in de lijst op de koppeling in de geselecteerde rij.
8. Schakel de uitbreiding van de sectie Details om.
9. Klik op Nieuw.
10. Typ "30301" in het veld Postcode van aflevering van.
11. Typ "30318" in het veld Postcode van aflevering naar.
12. Typ "VS" in het veld Afleverland/regio.
13. Typ "100" in het veld "1,00 pond".
    * Voeg het tarief per pond in als het totale gewicht van de lading minder dan 1 pond is.  
14. Typ '300' in het veld < 5,00 pond.
    * Voeg het tarief per pond in als het totale gewicht van de lading minder dan 5 pond is.  
15. Typ '500' in het veld < 20,00 pond.
    * Voeg het tarief per pond in als het totale gewicht van de lading minder dan 20 pond is.  
16. Typ '1000' in het veld < 100,00 pond.
    * Voeg het tarief per pond in als het totale gewicht van de lading minder dan 100 pond is.  
17. Typ '3000' in het veld < 1.000,00 pond.
    * Voeg het tarief per pond in als het totale gewicht van de lading minder dan 1000 pond is.  
18. Klik op Opslaan.
19. Sluit de pagina.

## <a name="assign-rate-base"></a>Tariefbasis toewijzen
1. Schakel de uitbreiding van de sectie Toewijzingen tariefbasis om.
2. Klik op Nieuw.
    * U kunt verschillende toewijzingen tariefbasis hebben voor elk tariefmodel. Dit maakt het mogelijk om verschillende prijspunten voor elke vervoerder te maken afhankelijk van bestemmingen, services of verschillende tariefbasissen. In deze procedure kunt u alleen één toewijzing tariefbasis maken.  
3. Typ een waarde in het veld Naam.
4. Klik in het veld Tariefbasis op de vervolgkeuzeknop om de zoekopdracht te openen.
5. Klik in de lijst op de koppeling in de geselecteerde rij.
6. Klik in het veld Service op de vervolgkeuzeknop om de zoekopdracht te openen.
7. Zoek en selecteer het gewenste record in de lijst.
8. Klik in de lijst op de koppeling in de geselecteerde rij.
9. Typ "98052" in het veld Postcode voor ophalen.
    * Geef op vanaf welke postcode deze toewijzing van de tariefbasis geldig moet zijn.    
10. Typ "VS" in het veld Land/regio voor ophalen.
11. Klik op Opslaan.

