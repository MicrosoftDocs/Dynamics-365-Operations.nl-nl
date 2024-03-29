---
title: Lean tracering van de behoefte vanuit verkooporders
description: Deze procedure is gericht op het valideren van de behoeftetraceringsstructuur van een verkoopregel waarin het artikel met kanbans wordt geproduceerd.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8eca21f8bd988ca352c07e839295b3edd9669929
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580619"
---
# <a name="lean-pegging-from-sales-orders"></a>Lean tracering van de behoefte vanuit verkooporders

[!include [banner](../../includes/banner.md)]

Deze procedure is gericht op het valideren van de behoeftetraceringsstructuur van een verkoopregel waarin het artikel met kanbans wordt geproduceerd. Nadat de behoeftetraceringsstructuur is gevalideerd, zijn alle kanbantaken gepland. Dit is handig voor orderscenario's waarbij de ordermedewerker ervoor moet zorgen dat de productie direct kan starten. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Deze procedure is bedoeld voor de gevorderde ordermedewerker die in lean bedrijf werkt.


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a>Een verkooporder maken voor een door kanban gestuurd artikel
1. Ga naar Alle verkooporders.
2. Klik op Nieuw.
3. Typ of selecteer een waarde in het veld Klantrekening.
    * Gebruik US-001.  
4. Klik op OK.
5. Typ in het veld Artikelnummer de waarde 'L0001'.
6. Stel Hoeveelheid in op '30'.
    * Het is belangrijk dat de hoeveelheid hoger is dan 24 om de gebeurteniskanbanregel te activeren.  

## <a name="open-a-pegging-tree"></a>Een behoeftetraceringsstructuur openen 
1. Klik op Product en voorraad.
2. Klik op Behoeftetraceringsstructuur weergeven.
    * De behoeftetraceringsstructuur toont alle niveaus van de tracering van de behoefte die nodig is voor de verkooporderregel. In dit geval zijn er twee niveaus van kanbans en alle vereiste onderdelen.  

## <a name="plan-the-pegging-tree"></a>De behoeftetraceringsstructuur plannen
1. Selecteer in de structuur 'Verkoopregel 000832\Kanban 000558'.
2. Vouw de sectie Kanbantaken uit.
    * De taakstatus voor de kanbantaak is Niet gepland.  
3. Klik op Volledige behoeftetraceringsstructuur plannen.
    * Op die manier worden alle kanbantaken in de behoeftetraceringsstructuur gepland, wat de taakstatus wijzigt van Niet gepland in Gepland.  
4. Vernieuw de pagina.
    * De kanbantaakstatus is gewijzigd van Niet gepland in Gepland.  
5. Selecteer in de structuur 'Verkoopregel 000832\Kanban 000558\Probleem voor L0001\Kanban 000559'.
    * De taak voor de tweede kanban is ook gepland, omdat de volledige behoeftetraceringsstructuur is gepland. De kanbantaakstatus is gewijzigd van Niet gepland in Gepland.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]