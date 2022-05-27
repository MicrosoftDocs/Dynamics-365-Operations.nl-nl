---
title: Diverse toeslagen voor Transportbeheer
description: In dit onderwerp wordt uitgelegd hoe door transport veroorzaakte toeslagen moeten worden gekoppeld aan een toeslagcode.
author: Weijiesa
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e54c94baeba487ccd8fe26e58d3e891e5e3a1088
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672593"
---
# <a name="transportation-management-miscellaneous-charges"></a>Diverse toeslagen voor Transportbeheer

[!include [banner](../includes/banner.md)]

Zoals met alle diverse toeslagen, moeten door transport veroorzaakte toeslagen worden gekoppeld aan een toeslagcode. Anders worden deze niet weer als divers toeslagbedrag aan de order toegevoegd. De **toeslagcode** bepaalt hoe de toeslag wordt verwerkt in relatie tot de order en orderregel waaraan de toeslag wordt toegevoegd.

Ga naar **Transportbeheer > Instellingen > Beoordeling > Diverse toeslagen** om de kwalificatiecriteria te definiëren die bepalen wanneer een specifieke **toeslagcode** op een toeslag wordt toegepast.

U moet minimaal één instellen voor elke relevante **Toeslagmodule**-instelling (*Klant* en *Leverancier*) waarvoor **Type diverse toeslagen** is ingesteld op *Geen*. Als deze ontbreekt, worden het diverse toeslagbedag *niet* aan de order toegevoegd.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]