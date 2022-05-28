---
title: Intercompany-toeslagen synchroniseren
description: In dit onderwerp wordt de synchronisatie van intercompany-toeslagen beschreven.
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 2c7f60786743cf750b2bb17ccc0dadf71d859766
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678570"
---
# <a name="synchronize-intercompany-charges"></a>Intercompany-toeslagen synchroniseren

[!include [banner](../../includes/banner.md)]

Toeslagen worden alleen gesynchroniseerd tussen de intercompany-verkooporder en de intercompany-inkooporder, en synchronisatie vindt altijd plaats.

Als het veld **Bewerking van prijs toestaan** is geselecteerd op de intercompany-inkooporder of de intercompany-verkooporder, kunt u handmatig een toeslag toevoegen aan de intercompany-verkooporder of de intercompany-inkooporder. Als dit veld niet is geselecteerd, kunt u dit niet.

Als het veld **Bewerking van prijs toestaan** niet is geselecteerd op de intercompany-verkooporder, kunt u niet handmatig een toeslag aan een intercompany-verkooporder toevoegen.

Als het veld **Bewerking van prijs toestaan** niet is geselecteerd op de intercompany-inkooporder, kunt u geen toeslag aan de intercompany-inkooporder toevoegen.

Als het veld **Bewerking van prijs toestaan** zowel op de intercompany-inkooporder als de intercompany-verkooporder is ingeschakeld, kunt u toeslagen handmatig aan beide orders toevoegen. Dit kan echter tot gevolg hebben dat veel toeslagen ten onrechte worden toegevoegd.

De beste manier om dergelijke conflicten te voorkomen is om toe te staan dat toeslagen worden toegevoegd aan de intercompany-verkooporder of aan de intercompany-inkooporder, maar niet aan beide.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
