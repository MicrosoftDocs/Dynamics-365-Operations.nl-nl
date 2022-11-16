---
title: Een gecorrigeerde prognose autoriseren
description: Niet alle prognosegegevens moeten onmiddellijk worden geautoriseerd. In dit artikel wordt uitgelegd hoe u de periode kunt opgeven waarvoor een prognose is geautoriseerd. Het legt ook uit hoe u de prognose voor specifieke bedrijven en prognosemodellen kunt autoriseren.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4954b70e56482e419d81485b544cb5d0b4e4a3ce
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740706"
---
# <a name="authorize-an-adjusted-forecast"></a>Een gecorrigeerde prognose autoriseren

[!include [banner](../includes/banner.md)]

Niet alle prognosegegevens moeten onmiddellijk worden geautoriseerd. In dit artikel wordt uitgelegd hoe u de periode kunt opgeven waarvoor een prognose is geautoriseerd. Het legt ook uit hoe u de prognose voor specifieke bedrijven en prognosemodellen kunt autoriseren.

Niet alle prognosegegevens moeten onmiddellijk worden geautoriseerd. U kunt de begin- en einddatums van de periode opgeven waarvoor de prognose wordt geautoriseerd. Met deze functie kunt u specifieke buckets blokkeren. 

De begin- en einddatums die u opgeeft, moeten overeenkomen met de begin- en einddatums van de verzameling waarin de prognose is gegenereerd. Deze beperking wordt afgedwongen en de datums worden automatisch aangepast als een correctie nodig is. 

Op het **Details** tabblad van de **Autorisatie** pagina, kunt u details bekijken over de prognose die zonet is gegenereerd. 

U kunt de bedrijven en prognosemodellen selecteren om de prognose te autoriseren voor gebruik. Standaard bevat het raster alle bedrijven waarvoor vraagprognose is gemaakt. Voor elk bedrijf, wordt het prognosemodel dat correspondeert met het huidige prognoseplan dat wordt ingesteld in de parameters van de hoofdplanning, vooraf ingevuld. U kunt dit prognosemodel echter in elk prognosemodel wijzigen dat tot dat bedrijf behoort. Als geen prognosegegevens zijn gegenereerd voor een geselecteerd bedrijf, ontvangt u een waarschuwing tijdens importeren. 

Het is zeer belangrijk dat u begrijpt hoe het selectievakje **De handmatige correcties opslaan die in de basislijnvraagprognose zijn gemaakt** werkt. Als u handmatige aanpassingen hebt aangebracht in de statistische basislijnprognose, worden de aangepaste waarden geautoriseerd voor gebruik, zelfs als dit selectievakje is uitgeschakeld. De wijzigingen worden echter verwijderd na de autorisatie. Daarom is die prognose, de volgende keer dat een prognose wordt gegenereerd, alleen een statistische prognose zonder handmatig overschreven waarden, zelfs als **Handmatige correcties overbrengen naar de vraagprognose** is geselecteerd. Daarom kunt u het selectievakje **De handmatige correcties opslaan die in de basislijnvraagprognose zijn gemaakt** als mechanisme beschouwen voor het behouden of verwijderen van alle handmatige wijzigingen.

## <a name="additional-resources"></a>Aanvullende resources

- [Handmatige correcties aanbrengen in de basislijnprognose](manual-adjustments-baseline-forecast.md)
- [Prognosenauwkeurigheid controleren](monitor-forecast-accuracy.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]