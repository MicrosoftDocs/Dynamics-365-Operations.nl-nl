---
title: Tijdvensters
description: U kunt tijdvensters gebruiken voor het optimaliseren van de planning van serviceorderregels.
author: YuyuScheller
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 4ea10e4c0fbfd21538bba16d2b01deb3e4b3a10d
ms.openlocfilehash: b7268870aa9065e4e52d936e819107094bad3663
ms.contentlocale: nl-nl
ms.lasthandoff: 02/20/2018

---

# <a name="time-windows"></a>Tijdvensters  

[!INCLUDE [banner](../includes/banner.md)]

U kunt tijdvensters gebruiken voor het optimaliseren van de planning van serviceorderregels. U kunt het systeem zo instellen dat het automatisch serviceorders maakt. Op basis van de criteria die door een tijdvenster zijn opgegeven, kunt u zoveel mogelijk serviceorderregels verbinden aan zo weinig mogelijk serviceorders.

Door tijdvensters wordt opgegeven in hoeverre een serviceorderregel ten opzichte van de berekende datum kan worden verplaatst. De berekende datum is de datum waarop de serviceorderregel is gepland. De datum is gebaseerd op de instelling van het interval en de serviceperiode die u hebt gedefinieerd op de pagina **Serviceorders maken**. U definieert een tijdvenster door de waarden uit de volgende tabel te gebruiken:

| methode | Omschrijving                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Week   | De datum waarop de serviceorderregel kan worden verplaatst naar een willekeurige open dag in dezelfde week als de oorspronkelijk berekende datum.                                                                                                                                                                                    |
| Maand  | De datum waarop de serviceorderregel kan worden verplaatst naar een willekeurige open dag in dezelfde maand als de oorspronkelijk berekende datum. Stel dat de berekende datum voor een serviceorderregel 15 februari 2017 is. In dat geval kan de serviceorderregel worden gepland voor elke willekeurige werkdag tussen 1 februari en 28 februari 2017. |
| Handmatig | U definieert het maximum aantal dagen voor of na de oorspronkelijk berekende datum waarop de serviceorderregel verplaatst kan worden.                                                                                                                                                                           |

Indien u geen tijdvenster opgeeft voor een serviceovereenkomstregel, moet de serviceorderregel die is afgeleid van de serviceovereenkomst op de precieze datum plaatsvinden waarop deze oorspronkelijk was gepland.

## <a name="related-topics"></a>Verwante onderwerpen

[Tijdvensters maken](create-time-windows.md)

