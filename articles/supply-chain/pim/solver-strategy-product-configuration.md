---
title: Oplossingsstrategie voor productconfiguratie
description: In dit onderwerp wordt beschreven hoe u oplossingsstrategie kunt gebruiken voor het verbeteren van de prestaties van productconfiguratie.
author: cvocph
ms.date: 02/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PCCreateProductConfigurationModel, PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 38755cc224ee2ae642d3caf7ad8ffea61f987206efc3ecd2ef81ecaf21cd6f4e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765973"
---
# <a name="solver-strategy-for-product-configuration"></a>Oplossingsstrategie voor productconfiguratie

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u oplossingsstrategie kunt gebruiken voor het verbeteren van de prestaties van productconfiguratie.

Het concept van oplossingsstrategieën is voor het eerst geïntroduceerd in cumulatieve update 7 (CU7) voor Microsoft Dynamics AX 2012 R2. Het is verlengd in cumulatieve update 8 (CU8) voor Microsoft Dynamics AX 2012 R3 en Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.

Het concept van de oplossingsstrategie bestaat nu uit de volgende strategieën:

- Standaard
- Minimale domeinen eerst
- Van boven naar beneden
- Z3

## <a name="solver-strategy"></a>Oplossingsstrategie 

Een productconfiguratiemodel kan worden geformuleerd als een [probleem met voldoen aan een beperking (CSP)](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf). Microsoft Solver Foundation (MSF) biedt twee soorten oplossingsstrategieën om de CSP's op te lossen die kunnen worden gebruikt in productconfiguratiemodellen. Deze oplossingsstrategieën vertrouwen op [heuristiek](https://techterms.com/definition/heuristic), die wordt gebruikt om de volgorde te bepalen waarin de variabelen van de CSP's worden beschouwd wanneer het probleem wordt opgelost. Heuristiek kan aanzienlijke invloed op de prestaties hebben als een probleem of klasse problemen wordt opgelost.

De oplossingsstrategie voor productconfiguratiemodellen bepaalt welke oplossing met heuristiek wordt gebruikt. De strategieën **Standaard**, **Minimale domeinen eerst** en **Van boven naar beneden** gebruiken de twee oplossingen van MSF, terwijl de strategie **Z3** de oplossing Z3 gebruikt. 

Werkelijke klantimplementaties hebben aangetoond dat een wijziging in de oplossingsstrategie voor een productconfiguratiemodel de responstijd van minuten tot milliseconden kan reduceren. Daarom is het de moeite waard verschillende oplossingsstrategieën te proberen om de efficiëntste strategie voor uw productconfiguratiemodel te zoeken.

## <a name="change-the-settings-for-the-solver-strategy"></a>De instellingen wijzigen voor de oplossingsstrategie

Als u de oplossingsstrategie wilt wijzigen, selecteert u op de pagina **Productconfiguratiemodellen** in het actiedeelvenster **Modeleigenschappen**. Selecteer vervolgens in het dialoogvenster **De details van het model bewerken** een oplossingsstrategie.

[![De oplossingsstrategie kiezen.](./media/solver-strategy.png)](./media/solver-strategy.png)

Er is momenteel geen logica die automatisch vaststelt welke oplossingsstrategie het efficiëntst is voor op beperkingen gebaseerde productconfiguratie. Daarom moet u de oplossingsstrategieën een voor een proberen.

De volgende tabel geeft aanbevelingen over de oplossingsstrategie die moet worden gebruikt in diverse scenario's.

| Oplossingsstrategie      | De strategie in dit scenario gebruiken |
|----------------------|-----------------------------------|
| Standaard              | De **standaard** strategie is geoptimaliseerd om modellen op te lossen die afhankelijk zijn van tabelbeperkingen. Klantimplementatieonderzoeken hebben uitgewezen dat deze strategie het efficiëntst is in scenario's waarin tabelbeperkingen veel worden gebruikt. |
| Minimale domeinen eerst | De strategieën **Minimale domeinen eerst** en **Van boven naar beneden** zijn nauw verwant. Klantimplementatieonderzoeken hebben uitgewezen dat de strategie **Van boven naar beneden** beter presteert dan de strategie **Minimale domeinen eerst**. De strategie **Minimale domeinen eerst** wordt echter in het product aangehouden voor achterwaartse compatibiliteit. Beide oplossingsstrategieën zijn efficiënter gebleken bij het oplossen van modellen die meerdere rekenkundige expressies bevatten waarin geen tabelbeperkingen worden gebruikt. In sommige gevallen presteert de strategie **Standaard** echter beter dan deze twee strategieën. Daarom moet u elke strategie proberen. |
| Van boven naar beneden             | De strategieën **Minimale domeinen eerst** en **Van boven naar beneden** zijn nauw verwant. Klantimplementatieonderzoeken hebben uitgewezen dat de strategie **Van boven naar beneden** beter presteert dan de strategie **Minimale domeinen eerst**. De strategie **Minimale domeinen eerst** wordt echter in het product aangehouden voor achterwaartse compatibiliteit. Beide oplossingsstrategieën zijn efficiënter gebleken bij het oplossen van modellen die meerdere rekenkundige expressies bevatten waarin geen tabelbeperkingen worden gebruikt. In sommige gevallen presteert de strategie **Standaard** echter beter dan deze twee strategieën. Daarom moet u elke strategie proberen. |
| Z3                   | Wij raden aan dat u de strategie **Z3** als de standaardoplossingsstrategie gebruikt. Als u zich zorgen maakt over prestaties en schaalbaarheid, kunt u de andere strategieën evalueren. |

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van Productconfiguratie](build-product-configuration-model.md)

[Heuristiek](https://techterms.com/definition/heuristic)

[Probleem met voldoen aan beperking](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]