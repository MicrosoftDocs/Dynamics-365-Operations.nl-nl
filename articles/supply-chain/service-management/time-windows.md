---
title: Tijdvensters
description: U kunt tijdvensters gebruiken voor het optimaliseren van de planning van serviceorderregels.
author: sorenva
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 857e9e023aa5648a06ae564936f06c491ea7cefc
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678089"
---
# <a name="time-windows"></a>Tijdvensters  

[!include [banner](../includes/banner.md)]

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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]