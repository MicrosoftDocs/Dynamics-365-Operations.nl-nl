---
title: Dimensies van kostenobject
description: Wanneer u kosten analyseert, gebruikt u elementendimensies om te bepalen waarheen de kosten stromen. U gebruikt kostenobjectdimensies om te bepalen waaraan u kosten moet toewijzen. Dit onderwerp biedt informatie over kostenobjectdimensies.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimensionMember, CAMCostObject
audience: Application User
ms.reviewer: roschlom
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e266a9ee2f47b819a4074291ad4a52d8df46ce1abe4f16308a3645375cd2dd80
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727391"
---
# <a name="cost-object-dimensions"></a>Dimensies van kostenobject

[!include [banner](../includes/banner.md)]

Wanneer u kosten analyseert, gebruikt u elementendimensies om te bepalen waarheen de kosten stromen. U gebruikt kostenobjectdimensies om te bepalen waaraan u kosten moet toewijzen. Dit onderwerp biedt informatie over kostenobjectdimensies.

Een kostenobject kan elk type object zijn dat u wilt ramen, waaraan u kosten wilt toewijzen of dat u rechtstreeks wilt meten. Veel gebruikte kostenobjecten zijn bijvoorbeeld producten, projecten, bronnen, afdelingen, kostenplaatsen en geografische regio's. Met kostenobjecten kan het management kosten kwantificeren en ook winstgevendheidsanalyses uitvoeren.

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a>Kostenobjectdimensies en leden van kostenobjectdimensies
Kostenobjecten worden ook wel *kostenobjectdimensies* genoemd. Nadat u hebt bepaald naar welke entiteit de kostenobjectdimensie moet verwijzen, moet u de afzonderlijke dimensiewaarden opgeven of deze in Kostprijsboekhouding importeren vanuit andere bronsystemen. Deze individuele dimensiewaarden staan bekend als *kostenobjectdimensieleden*. Stel dat u de financiële dimensie met de naam Kostenplaats gebruiken als de kostenobjectdimensie. Om te zien hoe kosten naar de individuele kostenplaatsen doorstromen, moet u de leden van de kostenobjectdimensie importeren. In dit geval zijn de leden van de kostenobjectdimensie de daadwerkelijke kostenplaatsen, zoals Verkoop, Productie, Administratie en Geografische locaties. In de onderstaande schermopname ziet u een voorbeeld van Kostenplaatsen als de kostenobjectdimensie met de werkelijke kostenplaatsen als kostenobjectdimensieleden. 

[![Schermopname met kostenplaatsen als dimensie van kostenobject.](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)

## <a name="import-cost-object-dimension-members-through-data-connectors"></a>Kostenobjectdimensieleden importeren door middel van gegevensconnectors
Om het importeren van kostenobjectdimensieleden eenvoudiger te maken, gebruikt u gegevensconnectors om de waarden op te halen uit de entiteiten die u wilt gebruiken als kostenobjectdimensies. U kunt de vooraf aangemaakte gegevensconnectors gebruiken, of aangepaste gegevensconnectors die u zelf samenstelt.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]