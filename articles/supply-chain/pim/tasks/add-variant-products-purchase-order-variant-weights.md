---
title: Productvarianten toevoegen aan inkooporder met verschillende gewichten
description: Deze procedure doorloopt de stappen voor het gebruik van variantgewichten om inkooporderregels automatisch te vullen voor elke variant van een product.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27ff3784074a36d073930ba68c8dec8b1121356e
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018279"
---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a>Productvarianten toevoegen aan inkooporder met verschillende gewichten

[!include [banner](../../includes/banner.md)]

Deze procedure doorloopt de stappen voor het gebruik van variantgewichten om inkooporderregels automatisch te vullen voor elke variant van een product. Wanneer u de hoeveelheid selecteert van het product dat u wilt aanschaffen, worden inkooporderregels gemaakt voor alle varianten van het product met voorgestelde hoeveelheden op basis van de gewichten die zijn geconfigureerd voor de productvarianten. Deze procedure omvat geen stappen voor het configureren van gewichtwaarden voor productdimensies en productvarianten. Deze procedure gebruikt het demobedrijf USRT.

1. Ga naar Leveranciers > Inkooporders > Alle inkooporders.
2. Klik op Nieuw.
3. Klik in het veld Leverancierrekening op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Klik in de lijst op de koppeling in de geselecteerde rij.
5. Schakel de uitbreiding van de sectie Algemeen om.
6. Klik in het veld Locatie op de vervolgkeuzeknop om de zoekopdracht te openen.
7. Klik in de lijst op de koppeling in de geselecteerde rij.
8. Klik in het veld Magazijn op de vervolgkeuzeknop om de zoekopdracht te openen.
9. Zoek en selecteer de gewenste record in de lijst.
10. Klik in de lijst op de koppeling in de geselecteerde rij.
11. Klik op OK.
12. Schakel de uitbreiding van de sectie Regeldetails om.
13. Klik op het tabblad Varianten.
14. Klik op Regel toevoegen.
15. Markeer in de lijst de geselecteerde rij.
16. Typ '0140' in het veld Artikelnummer.
17. Stel Hoeveelheid in op '1000'.
18. Klik op Opslaan.

