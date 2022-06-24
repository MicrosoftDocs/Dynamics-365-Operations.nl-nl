---
title: Diverse toeslagen voor Transportbeheer
description: In dit artikel wordt uitgelegd hoe door transport veroorzaakte toeslagen moeten worden gekoppeld aan een toeslagcode.
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
ms.openlocfilehash: 8cc4c595d8b61cb9b6c81af4bf7f03faa1a12960
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849208"
---
# <a name="transportation-management-miscellaneous-charges"></a>Diverse toeslagen voor Transportbeheer

[!include [banner](../includes/banner.md)]

Zoals met alle diverse toeslagen, moeten door transport veroorzaakte toeslagen worden gekoppeld aan een toeslagcode. Anders worden deze niet weer als divers toeslagbedrag aan de order toegevoegd. De **toeslagcode** bepaalt hoe de toeslag wordt verwerkt in relatie tot de order en orderregel waaraan de toeslag wordt toegevoegd.

Ga naar **Transportbeheer > Instellingen > Beoordeling > Diverse toeslagen** om de kwalificatiecriteria te definiëren die bepalen wanneer een specifieke **toeslagcode** op een toeslag wordt toegepast.

U moet minimaal één instellen voor elke relevante **Toeslagmodule**-instelling (*Klant* en *Leverancier*) waarvoor **Type diverse toeslagen** is ingesteld op *Geen*. Als deze ontbreekt, worden het diverse toeslagbedag *niet* aan de order toegevoegd.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]