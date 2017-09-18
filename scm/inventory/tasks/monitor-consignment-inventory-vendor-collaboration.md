---
title: Consignmentvoorraad bewaken door middel van leverancierssamenwerking
description: Deze procedure laat zien hoe u leverancierssamenwerking gebruikt om gegevens weer te geven over het voorraadniveau van het product dat u in consignatie bij een klant hebt geplaatst.
author: mkirknel
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: ad4868991226aef21a0410860e3f98d11901ffbb
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a>Consignmentvoorraad bewaken door middel van leverancierssamenwerking

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u leverancierssamenwerking gebruikt om gegevens weer te geven over het voorraadniveau van het product dat u in consignatie bij een klant hebt geplaatst. U kunt ook het verbruik van de voorraad controleren wanneer de klant eigenaar wordt van de voorraad. U kunt deze procedure gebruiken in het demobedrijf USMF. Deze procedure is voor een functie die in versie 1611 van Dynamics 365 for Operations is toegevoegd.


## <a name="view-consumed-inventory"></a>Verbruikte voorraad weergeven
1. Ga naar Leverancierssamenwerking > Consignatievoorraad > Producten ontvangen uit consignatievoorraad.
    * De lijst geeft de productontvangstbonregels weer die zijn gegenereerd toen het eigendom van de consignatievoorraad is gewijzigd van de leverancier in de klant. Mogelijk moet u naar rechts schuiven om hoeveelheden en andere informatie weer te geven. U kunt de informatie in deze lijst gebruiken om facturen voor de klant te genereren. U kunt ook de gegevens naar Microsoft Excel exporteren.   
2. Klik op Inkooporder weergeven.
3. Vouw de sectie Regeldetails uit.
    * De regel wordt gemarkeerd als Consignatie en in de koptekstsectie wordt aangegeven dat de status van de inkooporder Ontvangen is.  
4. Sluit de pagina.

## <a name="view-on-hand-inventory"></a>Voorhanden voorraad weergeven
1. Ga naar Leverancierssamenwerking > Consignatievoorraad > Voorhanden consignatievoorraad.
    * De pagina Voorhanden consignatievoorraad geeft de voorraad weer die u bezit in het magazijn van de klant. U kunt extra dimensies weergeven, zoals de locatie en het magazijn, door op het tabblad Dimensies weergeven te klikken.   
