---
title: Gecombineerde nummerplaat ontvangen
description: In dit onderwerp wordt beschreven hoe u met ontvangst van gecombineerde nummerplaten werk kunt registreren en maken voor meerdere artikelen met een mobiel apparaat.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFAutoConfirm, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b17b3a4d704c5bfd051426e708d39022e59cc67a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810457"
---
# <a name="mixed-license-plate-receiving"></a>Gecombineerde nummerplaat ontvangen

[!include [banner](../includes/banner.md)]

Met gecombineerde nummerplaatontvangst kunt u een nummerplaat maken die meerdere artikelen omvat, voordat u wegzetwerk registreert en maakt. 

Een nummerplaat die meerdere artikelen omvat, hoeft niet te worden opgesplitst in de ontvangende dock om elk artikel te kunnen registreren. 

Als u een artikelgerelateerde stroom gebruikt om de brondocumentregels te identificeren, kunt u streepjescodes op het besturingselement van het artikel scannen. Als in de streepjescode een hoeveelheid en een maateenheid zijn geconfigureerd, worden het artikel en de hoeveelheid automatisch toegevoegd aan de gecombineerde nummerplaat en keert u terug naar het scherm om een ander artikel te scannen. Hiermee kunt u snel alle items scannen, zonder elke stap te hoeven bevestigen. 

In de stroom voor gecombineerde nummerplaatontvangst kunt u de lijst weergeven met artikelen die al zijn gescand naar de nummerplaat en van hieruit kunt u de hoeveelheid van een artikel aanpassen of corrigeren.

## <a name="where-it-applies"></a>Waar van toepassing

Ontvangst van gecombineerde nummerplaten is een ontvangststroom voor mobiele apparaten, waarmee u werk voor meerdere regels/artikelen tegelijkertijd kunt registreren en maken. Dit is handig als u binnenkomende nummerplaten met meerdere artikelen ontvangt. 

## <a name="how-to-set-up-mixed-license-plate-receiving"></a>Gecombineerde nummerplaatontvangst instellen
Gecombineerde nummerplaatontvangst wordt ingesteld als een menu-item voor mobiel apparaten.

U moet een nieuwe menuoptie maken met de modus werk, die geen bestaand werk gebruikt en een van de volgende methoden gebruikt:

- Gecombineerde nummerplaat ontvangen
- Nummerplaat ontvangen en wegzetten

De opties om de brondocumentregels te identificeren zijn inkooporderartikel, inkooporderregel, retourorder, overboekingsorderartikel en overboekingsorderregel. Deze opties kunnen de ontvangstvolgorde op een enkele nummerplaat wijzigen. De laatste optie is op ladingsartikel. U kunt meerdere artikelen toevoegen aan een nummerplaat, maar u kunt niet schakelen tussen meerdere ladingen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]