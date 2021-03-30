---
title: Een statistische basislijnprognose genereren
description: Dit onderwerp bevat informatie over de parameters en de filters die in de berekening van de vraagprognose worden gebruikt.
author: roxanadiaconu
manager: tfehr
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9257f54080eed6c066f10eeb0cddb12a96e08817
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204659"
---
# <a name="generate-a-statistical-baseline-forecast"></a>Een statistische basislijnprognose genereren

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat informatie over de parameters en de filters die in de berekening van de vraagprognose worden gebruikt. 

Wanneer u een basislijnprognose maakt, moet u eerst de parameters en filters opgeven die worden gebruikt in de berekening. U kunt bijvoorbeeld u een basislijnprognose maken die de vraag raamt op basis van transactiegegevens van het afgelopen jaar voor een specifiek bedrijf, voor de volgende maand, en voor een geselecteerde groep artikelen. 

Ga om een vraagprognose te genereren naar **Hoofdplanning &gt; Prognose &gt; Vraagprognose &gt; Statistische basislijnprognose maken**. 

De prognoseverzameling kan worden geselecteerd in de prognosegeneratietijd. De beschikbare waarden zijn Dag, Week en Maand. 

Het aantal verzamelingen waarvoor u een prognose wilt genereren is ingesteld in het veld **Prognoseperiode**. 

Wanneer de prognosestrategie is ingesteld **Kopieer over historische vraag**, wordt het einde van de historische periode genegeerd. Het aantal prognoseverzamelingen dat is opgegeven in het veld **Prognoseperiode**, wordt gekopieerd naar de prognosevraag, te beginnen met de datum die is ingesteld in het veld **Begindatum** onder **Historische periode**. Door historische vraag van een bepaalde datum voorwaarts te kopiëren kunnen productieplanners het plan voor het kwartaal op twee manieren maken:

-   Door de vraag van hetzelfde kwartaal van het vorige jaar te kopiëren.
-   Door de vraag van het voorafgaande kwartaal te kopiëren.

Om verwarring in de productieplannen te vermijden, kan een bepaald aantal prognoseverzamelingen worden vergrendeld. Dit aantal wordt ingesteld in het veld **Blokkering van de tijdlimiet**. Op de **Aangepaste vraagprognose** pagina, worden de cellen voor de stilgezette verzamelingen uitgeschakeld, om een grafische indicatie te geven dat deze waarden niet moeten worden gewijzigd. 

De begindatum voor de basislijnvraagprognose hoeft niet de huidige datum of een datum in de toekomst te zijn. Om een andere begindatum in te stellen, gebruikt u het veld **De begindatum van de basislijnprognose - Begindatum**. In juni kunnen gebruikers bijvoorbeeld een prognose voor het volgende jaar genereren. Omdat de prognoseverzamelingen tussen het einde van historische vraag en het begin van de basislijn ontbreken, zijn de voorspellingen mogelijk niet nauwkeurig. Als u de vraagprognoseservice gebruikt, zijn er vier manieren waarop u de lacunes kunt invullen. U kunt de gewenste methode selecteren door de parameter MISSING\_VALUE\_SUBSTITUTION in te stellen op de pagina **Parameters voor vraagprognose**. 

> [!NOTE]
> Ontbrekende waardevervanging werkt alleen voor gaten in gegevens tussen de begin- en eind datum van historische gegevens. Er worden geen gegevens ingevuld voor of na het laatste fysieke gegevenspunt, het fungeert alleen als extrapolatie tussen werkelijk bestaande gegevenspunten. 

Het veld **Begindatum van basislijnprognose** - **Begindatum** moet worden ingesteld aan het begin van een prognoseverzameling, bijvoorbeeld in de Verenigde Staten op een zondag als de prognoseverzameling de week is. Het veld **Begindatum van basislijnprognose** - **Begindatum** wordt automatisch aan het begin van een prognoseverzameling aangepast. 

Het veld **Begindatum van basislijnprognose** - **Begindatum** kan worden ingesteld op een datum in het verleden. Met andere woorden, het is mogelijk om een vraagprognose in het verleden te genereren. Dit is handig, omdat het gebruikers in staat stelt de parameters van de prognoseservice aan te passen zodat de statistische prognose die in het verleden is gegenereerd overeenkomt met de werkelijke historische vraag. Gebruikers kunnen vervolgens deze parameterinstellingen blijven gebruiken om een statistische basislijnprognose te genereren voor de toekomst. 

Handmatige correcties die bij vorige iteraties van vraagprognoses zijn aangebracht, kunnen automatisch worden toegepast op de nieuwe basislijnprognose als het selectievakje **Handmatige correcties overbrengen naar de vraagprognose** is ingeschakeld. Als het selectievakje is uitgeschakeld, worden handmatige aanpassingen niet toegevoegd aan de basislijnprognose, maar ze worden niet verwijderd. Handmatige correcties die in een prognose zijn aangebracht, kunnen alleen op het moment van importeren van de prognose worden verwijderd door het selectievakje **De handmatige correcties opslaan die in de basislijnvraagprognose zijn gemaakt** te wissen. Handmatige aanpassingen worden opgeslagen op het moment van autorisatie. Daarom gaan de wijzigingen verloren als een gebruiker handmatig aanpassingen uitvoert in de prognose, maar de prognose niet opnieuw autoriseert in Supply Chain Management. Zie [De gecorrigeerde prognose autoriseren](authorize-adjusted-forecast.md) voor meer informatie over handmatige correcties en hoe deze werken. 

Het genereren van een vraagprognose kan een naam en opmerkingen hebben om gebruikers te helpen de gegenereerde prognose te identificeren. Deze waarden zijn zichtbaar in de historie voor het genereren van prognoses op de pagina **Historie van genereren van statistische basislijnprognose**. 

De intercompany-planninggroep, de artikeltoewijzingssleutels, en andere filters kunnen in de prognosegeneratietijd worden toegepast. Deze kunnen worden gebruikt om de prestaties te verbeteren of de gegevens op te splitsen in werkbare brokken. Er wordt echter geen vraagprognose gegenereerd voor de leden van een artikeltoewijzingssleutel die niet zijn gekoppeld aan een intercompany-planningsgroep, zelfs als de artikeltoewijzingssleutel in de query wordt geselecteerd. 

> [!TIP]
> Soms kunnen gebruikers fouten krijgen tijdens het genereren van een vraagprognose, of wordt het maken van de prognose voltooid zonder sessielogboek. Dit kan gebeuren vanwege resterende gegevens in de query die eerder werd gebruikt voor het genereren van een prognose. U kunt dit probleem oplossen door te klikken op **Selecteren** om de pagina **Query** te openen, op **Opnieuw instellen** te selecteren en vervolgens de basislijnprognose opnieuw te genereren. 

Als de prognose niet wordt gegenereerd voor een grote set artikelen, maar bijvoorbeeld voor één artikel of artikeltoewijzingssleutel tegelijk, kunt u om betere prestaties te krijgen het selectievakje **Aanvraagreactiemodus gebruiken** op het tabblad **Hoofdplanning - Instellingen - Vraagprognose** - **Parameters voor vraagprognose - Azure Machine Learning** inschakelen.

> [!NOTE]
> Een potentieel vlakke prognose kan het gevolg zijn van de historische gegevens die een langere historische periode moeten omvatten (minimaal drie tijdsperioden om patronen te kunnen zien, bijvoorbeeld 3 jaar met maandelijkse prognose). U kunt proberen de nauwkeurigheid van het tijdsbereik te wijzigen of het tijdsbereik te vergroten om een beter resultaat te krijgen.

<a name="additional-resources"></a>Aanvullende bronnen
--------

- [Instelling van Vraagprognose](demand-forecasting-setup.md)

- [Handmatige correcties aanbrengen in de basislijnprognose](manual-adjustments-baseline-forecast.md)

- [Een gecorrigeerde vraagprognose autoriseren](authorize-adjusted-forecast.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]