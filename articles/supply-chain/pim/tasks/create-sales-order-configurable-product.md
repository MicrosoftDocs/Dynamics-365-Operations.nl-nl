---
title: Een verkooporder voor een configureerbaar product maken
description: Deze procedure laat zien hoe u een configuratiesjabloon toepast op een product in een verkooporder.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cafd6e01800b55f316179c481aaa110b2cbcbc80
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150029"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a>Een verkooporder voor een configureerbaar product maken

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u een configuratiesjabloon toepast op een product in een verkooporder. In dit voorbeeld wordt het model D0006-luidspreker gebruikt in het demobedrijf USMF. Gewoonlijk gebruikt een verkooporderbewerker deze procedure.


## <a name="create-a-sales-order"></a>Verkooporder maken
1. Klik op Verkooporderverwerking en -onderzoek.
2. Klik op Nieuw.
3. Klik op Verkooporder.
4. Selecteer US-001 in het veld Klantrekening. 
5. Klik op OK.
6. Selecteer D0006 in het veld Artikelnummer.
    * Voor deze taak moet u een configureerbaar product selecteren.  
7. Klik op Product en voorraad.
8. Klik op Regel configureren.
    * Merk op dat de prijs is gewijzigd, op basis van de configuratie die is geselecteerd, en dat het veld Met kabel nu op Waar is ingesteld.  
    * Let op de standaardprijs en de instellingen die voor de kabel worden geselecteerd.  
9. Klik op Sjabloon laden.
    * Dit voorbeeld laat zien hoe u een sjabloon kunt toepassen om een vooraf gedefinieerde configuratie te selecteren. Als u deze procedure als taakbegeleider gebruikt en de andere kenmerkwaarden wilt weergeven die beschikbaar zijn, moet u op de knop Ontgrendelen klikken.  
10. Klik op OK.
11. Klik op OK.
12. Vouw de sectie Regeldetails uit.
13. Klik op het tabblad Product.
    * De configuratie van het artikel wordt nu vermeld onder productdimensies.  
14. Sluit de pagina.

## <a name="select-the-product-configuration"></a>Selecteer de productconfiguratie

