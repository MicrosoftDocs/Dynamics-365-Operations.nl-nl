---
title: Time fences voor behoefteplanning
description: In dit artikel wordt beschreven hoe u time fences voor behoefteplanning instelt. Een time fence voor behoefteplanning geeft uw planningshorizon en -limiet aan.
author: t-benebo
ms.date: 01/18/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2021-01-18
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 987dea4c1b693fc1bb687f97d51288d5e51e7d4c
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740108"
---
# <a name="coverage-time-fences"></a>Time fences voor behoefteplanning

[!include [banner](../../includes/banner.md)]

In dit artikel wordt beschreven hoe u *time fences voor behoefteplanning* instelt. Planners kunnen de planningshorizon (de time fence voor behoefteplanning in dagen) definiëren en kunnen vraag en aanbod buiten die horizon uitsluiten. Daarom helpen time fences voor behoefteplanning 'ruis' voorkomen die wordt veroorzaakt door aanbodsuggesties waar u maanden niet op hoeft te reageren. Voorbeelden zijn de prognose van volgend jaar en de klantorders die veel verder zijn geplaatst dan de normale levertijd.

Een time fence voor behoefteplanning is het aantal dagen na de datum van vandaag (of om precies te zijn de datum waarop u de planning moet uitvoeren) dat vraag en aanbod zijn uitgesloten. Om vertragingen te voorkomen moet u ervoor zorgen dat de time fence voor behoefteplanning langer is dan de totale levertijd. De standaardsysteeminstelling is 100 dagen.

U kunt een time fence voor behoefteplanning opgeven op de volgende niveaus:

- **Behoefteplanningsgroep:** u kunt een standaard time fence voor behoefteplanning instellen voor elke behoefteplanningsgroep.
- **Artikelbehoefteplanning:** u kunt de time fence voor behoefteplanning overschrijven die is overgenomen van de behoefteplanningsgroep die aan een artikel is toegewezen.
- **Hoofdplan:** u kunt de time fences voor behoefteplanning overschrijven die zijn overgenomen van de instellingen voor de behoefteplanningsgroep en een artikel.

In de volgende secties wordt uitgelegd hoe u een behoefteplanningsgroep op elk niveau opgeeft.

## <a name="set-a-coverage-time-fence-for-a-coverage-group"></a>Een time fence voor behoefteplanning instellen voor een behoefteplanningsgroep

Wanneer u een time fence voor behoefteplanning voor een behoefteplanningsgroep opgeeft, is de instelling van toepassing op alle artikelen (producten) die tot die groep behoren. U kunt de instelling echter overschrijven voor specifieke artikelen of specifieke hoofdplannen.

Volg deze stappen om een time fence voor behoefteplanning voor een behoefteplanningsgroep op te geven.

1. Ga naar **Hoofdplanning \> Instellen \> Behoefteplanning \> Behoefteplanningsgroepen**.
1. Selecteer een bestaande behoefteplanningsgroep in de lijst of maak een nieuwe.
1. Stel op het sneltabblad **Algemeen** het veld **Time fence behoefteplanning (dagen)** in op het aantal dagen dat u wilt gebruiken als de time fence voor behoefteplanning voor de behoefteplanningsgroep.

## <a name="set-a-coverage-time-fence-for-a-specific-item"></a>Een time fence voor behoefteplanning instellen voor een specifiek artikel

Elk artikel (product) behoort tot een behoefteplanningsgroep. Als geen behoefteplanningsgroep expliciet aan een artikel is toegewezen, is een standaardbehoefteplanningsgroep van toepassing. Elk artikel neemt een time fence voor behoefteplanning van de bijbehorende behoefteplanningsgroep over. U kunt deze time fence echter zo nodig overschrijven voor specifieke artikelen.

Volg deze stappen om een time fence voor behoefteplanning voor een specifiek artikel op te geven.

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Selecteer een product in het raster.
1. Selecteer in het actievenster op het tabblad **Plannen** in de groep **Behoefteplanning** de optie **Artikelbehoefteplanning**.
1. Selecteer of maak op de pagina **Artikelbehoefteplanning** op het tabblad **Overzicht** een rij voor de site waar u een time fence voor behoefteplanning wilt instellen.
1. Selecteer het tabblad **Algemeen** om de instellingen voor de geselecteerde site te openen.
1. Schakel het selectievakje **Instellingen behoefteplanningsgroep negeren** in.
1. Stel het veld **Time fence behoefteplanning (dagen)** in op het aantal dagen dat u wilt gebruiken als de time fence voor behoefteplanning voor het artikel.

## <a name="set-a-coverage-time-fence-for-a-specific-master-plan"></a>Een time fence voor behoefteplanning instellen voor een specifiek hoofdplan

U kunt een time fence voor behoefteplanning opgeven op hoofdplanniveau: Op deze manier definieert u het aantal dagen dat de hoofdplanberekening dekt voor een hoofdplan. Deze instelling heeft voorrang boven de tijdinstellingen voor de behoefte die voor elk relevant artikel en voor de desbetreffende behoefteplanningsgroep zijn gedefinieerd.

Volg deze stappen om een time fence voor behoefteplanning voor een specifiek hoofdplan op te geven.

1. Ga naar **Hoofdplanning \> Instellen \> Plannen \> Hoofdplannen**.
1. Selecteer een bestaand hoofdplan in de lijst of maak een nieuw hoofdplan.
1. Stel op het sneltabblad **Time fences in dagen** de optie **Behoefteplanning** in op *Ja*. Stel vervolgens in het veld onder de optie het aantal dagen in dat u wilt gebruiken als de time fence voor behoefteplanning voor het hoofdplan.

## <a name="considerations-for-coverage-time-fences"></a>Overwegingen voor time fences voor behoefteplanning

Houd rekening met de volgende punten terwijl u time fences voor behoefteplanning instelt:

- Time fences voor behoefteplanning zijn alleen van invloed op invoergegevens voor de hoofdplanning. Als er vertragingen optreden, hebben de resulterende geplande orders mogelijk een datum die later is dan de datum van vandaag plus de time fence voor behoefteplanning.
- Time fences voor behoefteplanning worden opgegeven in kalenderdagen. Kalenders die werkdagen gebruiken, hebben geen invloed op de berekening van de time fence. Een week wordt bijvoorbeeld altijd als zeven dagen beschouwd, zelfs als weekends als gesloten dagen worden ingesteld in de werktijdkalender.
- Behoeftetransacties worden niet gegenereerd voor vraag en aanbod die buiten de time fence voor behoefteplanning vallen.
- Als goedgekeurde vraag en aanbod buiten de time fence voor behoefteplanning vallen, worden deze niet in de engine geladen. Hierdoor wordt geen aanvulling getriggerd en wordt er geen vertraging berekend. Toch moeten deze vraag en aanbod niet van het systeem worden gewist.
- Variaties in veiligheidsvoorraadhoeveelheden (van minimumsleutels) worden genegeerd als deze buiten de time fence voor behoefteplanning vallen.
- De intercompany-vraag wordt genegeerd als de gewenste verzenddatum die is berekend niet binnen de time fence voor behoefteplanning ligt. Voor de afgeschafte hoofdplanningsengine wordt intercompany-vraag niet beperkt door de time fence voor behoefteplanning.
- Vraagprognoses worden genegeerd als de budgetdatum niet binnen de time fence voor behoefteplanning valt. Voor de afgeschafte hoofdplanningsengine worden vraagprognoses niet beperkt door de time fence voor behoefteplanning.
- Tijdens de planningsoptimalisatie wordt rekening met de tijdzone gehouden. Er wordt rekening met de tijdzone op de aanbod- en vraaglocaties en met de tijd van de planningsuitvoering gehouden. Bijvoorbeeld: hoofdplanning wordt getriggerd om 11 uur in de ochtend op 15 oktober vanaf een site in Denemarken (tijdzone GMT+1) en er wordt een time fence voor behoefteplanning van tien dagen gebruikt. In dit geval worden het aanbod en de vraag van een site in Seattle (tijdzone GMT-8) opgenomen tot 2 uur in de ochtend op 25 oktober (= tien 24-uur dagen nadat de hoofdplanning is getriggerd, minus het tijdzoneverschil van negen uur). Bij de afgeschafte hoofdplanningsengine wordt alleen rekening gehouden met de datum van de time fence. Het resultaat kan daarom verschillen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]