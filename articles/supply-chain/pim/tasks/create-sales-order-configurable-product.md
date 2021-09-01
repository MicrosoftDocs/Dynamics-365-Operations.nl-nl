---
title: Een verkooporder voor een configureerbaar product maken
description: Deze procedure laat zien hoe u een configuratiesjabloon toepast op een product in een verkooporder.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f128518af01911a29ae297670883ef425f9117d65cc952cc1ffdb044c4ce085f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781897"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a>Een verkooporder voor een configureerbaar product maken

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u een configuratiesjabloon toepast op een product in een verkooporder. In dit voorbeeld wordt het model D0006-luidspreker gebruikt in het demobedrijf USMF. Gewoonlijk gebruikt een verkooporderbewerker deze procedure.

## <a name="create-a-sales-order"></a>Verkooporder maken

1. Ga naar **Verkoop en marketing \> Werkgebieden \> Verkooporderverwerking en -onderzoek**.
1. Selecteer **Nieuw**.
1. Selecteer **Verkooporders**.
1. Selecteer *US-001* in het veld **Klantrekening**. 
1. Selecteer **OK**.
1. Selecteer in het veld **Artikelnummer** de optie *D0006*.
    * Voor deze taak moet u een configureerbaar product selecteren.  
1. Selecteer **Product en voorraad**.
1. Selecteer **Regel configureren**.
    * Merk op dat de prijs is gewijzigd, op basis van de configuratie die is geselecteerd, en dat het veld **Met kabel** nu op *Waar* is ingesteld.  
    * Let op de standaardprijs en de instellingen die voor de kabel worden geselecteerd.  
1. Selecteer **Sjabloon laden**.
    * Dit voorbeeld laat zien hoe u een sjabloon kunt toepassen om een vooraf gedefinieerde configuratie te selecteren. Als u deze procedure als taakbegeleider gebruikt en de andere kenmerkwaarden wilt weergeven die beschikbaar zijn, moet u op de knop **Ontgrendelen** klikken.  
1. Selecteer **OK**.
1. Selecteer **OK**.
1. Vouw de sectie **Regeldetails** uit.
1. Selecteer het tabblad **Product**.
    * De configuratie van het artikel wordt nu vermeld onder productdimensies.  
1. Sluit de pagina.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]