--- 
title: Consignmentvoorraad bewaken door middel van leverancierssamenwerking
description: Deze procedure laat zien hoe u leverancierssamenwerking gebruikt om gegevens weer te geven over het voorraadniveau van het product dat u in consignatie bij een klant hebt geplaatst.
author: mkirknel
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ConsignmentProductReceiptLines, PurchVendorPortalConfirmedOrders, DefaultDashboard, ConsignmentVendorPortalOnhand
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 567be29bd9989b3471b22d5a970ed0e51e4549ec
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a>Consignmentvoorraad bewaken door middel van leverancierssamenwerking

[!include [task guide banner](../../includes/task-guide-banner.md)]

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


