---
title: Overzicht van DDMRP (Demand Driven Material Requirements Planning)
description: Dit artikel biedt informatie over DDMRP (Demand Driven Material Requirements Planning), een planningsmethodologie die is gebaseerd op de ontkoppeling van vraag en aanbod.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 31b45fdb92cf8a590ff77104f0c8015fb4d329d5
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689483"
---
# <a name="demand-driven-material-requirements-planning-ddmrp-overview"></a>Overzicht van DDMRP (Demand Driven Material Requirements Planning)

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Bedrijven hebben jaren de planning van materiaalbehoeften (MRP) gebruikt als een systeem voor het berekenen van de materialen en onderdelen die nodig zijn om een product te produceren. Toeleveringsketens zijn nu echter gewijzigd. Onderdelen hebben langere doorlooptijden omdat ze steeds vaker van overzee komen. Daarom geven veel bedrijven aan dat ze te maken hebben met voorraadoverschotten of -tekorten, omdat ze niet weten hoeveel er op voorraad moet worden gehouden. Er is ook sprake van meer marktfluctuaties (soms onnauwkeurige prognoses) en van klanten die om producten met korte doorlooptijd vragen. Daarom is er in de hele wereld sprake van tekorten in de toeleveringsketen. Bovendien geven MRP-hulpprogramma's planners vaak duizenden acties die ze moeten uitvoeren. Daarom is het moeilijk om te weten waar de focus moet liggen. Vaak is de oplossing voor een groot aantal van deze problemen overschakeling naar DDMRP (Demand Driven Material Requirements Planning).

DDMRP is een planningsmethodologie die is gebaseerd op de ontkoppeling van vraag en aanbod. Deze ontkoppeling wordt bereikt door ontkoppelingspuntartikelen in te stellen. Voor deze artikelen worden buffers onderhouden om ervoor te zorgen dat de juiste hoeveelheid voorraad wordt behouden. De ontkoppeling van vraag en aanbod helpt het 'zweepslageffect' te voorkomen, omdat variabiliteit niet door de hele keten heen wordt doorgegeven. (Het *zweepslageffect* verwijst naar hoe kleine schommelingen in de vraag op detailhandelniveau kunnen zorgen voor progressief grotere schommelingen in de vraag op het niveau van groothandel, distributeur, fabrikant en leverancier van grondstoffen.) Elke buffer is bedoeld voor het gemiddelde gebruik van een onderdeel en kan ook worden gecorrigeerd om pieken in de vraag te dekken.

DDMRP is een waardevolle planningsmethodologie gebleken voor variabele omgevingen waarin klanttolerantietijden korter zijn dan cumulatieve doorlooptijden.

## <a name="the-five-components-of-ddmrp"></a>De vijf onderdelen van DDMRP

DDMRP heeft vijf opeenvolgende onderdelen (stappen). De eerste drie onderdelen bepalen in wezen de initiële en veranderende configuratie van een model voor een vraaggestuurde materiaalbehoefteplanning. De laatste twee onderdelen bepalen de dagelijkse werking van de methodologie.

1. **[Strategische voorraadpositionering](ddmrp-inventory-positioning.md)**: ontkoppelingspunten identificeren in het toeleveringsketennetwerk. Ontkoppelingspunten zijn specifieke punten van uw toeleveringsketen waar u een voorraadbuffer plaatst die u controleert en aanvult.
2. **[Bufferprofielen en -niveaus](ddmrp-buffer-profile-and-levels.md)**: voor elk ontkoppelingspunt de buffergrootten (minimumhoeveelheid, maximumhoeveelheid en bestelpunt) en de bestelhoeveelheid aangeven.
3. **[Dynamische buffercorrecties](ddmrp-buffer-profile-and-levels.md#dynamic-adjustments)**: bufferniveaus aanpassen op basis van wisselende operationele parameters of geplande toekomstige gebeurtenissen.
4. **[Vraaggestuurde planning](ddmrp-planning.md)**: aanbodorders genereren wanneer deze nodig zijn. Deze aanbodorders omvatten productieorders, inkooporders en voorraadtransferorders
5. **[Zeer samenwerkende en zichtbare uitvoering](ddmrp-visual-and-collaborative-execution.md)**: de aanbodorders uitvoeren met behulp van visualisatie.

DDMRP wordt meestal gebruikt door fabrikanten die een stuklijst met meerdere niveaus hebben. DDMRP kan echter ook worden toegepast op distributie- en detailhandelnetwerken.

## <a name="ddmrp-in-dynamics-365-supply-chain-management"></a>DDMRP in Dynamics 365 Supply Chain Management

DDMRP wordt meegeleverd met Microsoft Dynamics 365 Supply Chain Management zonder extra licentiekosten. In Supply Chain Management is de DDMRP-functionaliteit toegevoegd aan de bestaande module **Hoofdplanning**. U moet hiervoor echter de invoegtoepassing Planningsoptimalisatie gebruiken. 

DDMRP is geïntegreerd met de bestaande planningsinstellingen in Supply Chain Management en wordt samen met deze instellingen gebruikt om tot de juiste planningsconfiguratie voor uw bedrijf te komen. DDMRP wordt beheerd door een nieuwe behoefteplanningscode die totaal verschilt van periode, min/max, behoefte, enzovoort. Het is geen nieuwe module en vervangt geen bestaande planningsfunctionaliteit. Het geeft u echter meer functionaliteit die u kunt toepassen.
