---
title: Door het locatieprofiel wordt negatieve voorraad niet toegestaan, maar is negatieve voorhanden voorraad wel toegestaan
description: De optie Negatieve voorraad toestaan voor het locatieprofiel is ingesteld op Nee, maar negatieve voorhanden voorraad blijft toegestaan.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 356d2dd7853bf93250e14eb9bd28a8a145794584
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026403"
---
# <a name="location-profile-disallows-negative-inventory-but-negative-on-hand-inventory-is-permitted"></a>Door het locatieprofiel wordt negatieve voorraad niet toegestaan, maar is negatieve voorhanden voorraad wel toegestaan

KB-nummer: 4613622

## <a name="symptoms"></a>Symptomen

De optie **Negatieve voorraad toestaan** voor het locatieprofiel is ingesteld op *Nee*, maar negatieve voorhanden voorraad blijft toegestaan.

## <a name="example-scenario"></a>Voorbeeldscenario

Voor overheidstransacties met gereguleerde transacties moet het systeem negatieve voorraad kunnen registreren om verliezen te boeken. U wilt dat een artikel negatieve voorraad kan laten zien, maar alleen op bepaalde locaties, bijvoorbeeld op een bepaalde locatie, bijvoorbeeld containers. Als de artikelmodelgroep echter negatieve voorraad toestaat, maakt het u niet uit of de locatie is ingesteld op negatieve voorraad toestaan. Als het artikel zo is ingesteld dat negatieve voorraad niet is toegestaan, maakt het niet uit hoe het locatieprofiel is ingesteld.

## <a name="resolution"></a>Oplossing

De instelling **Negatieve voorraad toestaan** vanuit het locatieprofiel is alleen van toepassing op magazijnprocessen, zoals orderverzameling. Als artikelmodelgroepen echter zijn ingesteld op negatieve voorraad toestaan, is dit van invloed op alle processen van de modules Voorraadbeheer en Magazijnbeheer en het locatieprofiel heeft geen voorrang.

U kunt bepalen of in een magazijn negatieve voorraad is toegestaan. Stel de artikelmodelgroepen in op het niet toestaan van negatieve fysieke voorraad en stel alleen het relevante magazijn in op het toestaan van negatieve voorraad.
