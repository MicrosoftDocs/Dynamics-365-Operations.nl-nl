---
title: Diverse toeslagen voor Transportbeheer
description: In dit onderwerp wordt uitgelegd hoe door transport veroorzaakte toeslagen moeten worden gekoppeld aan een toeslagcode.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2b703d770c7f9ea684716368cf1e7dbe5fec8710
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/29/2020
ms.locfileid: "4425913"
---
# <a name="transportation-management-miscellaneous-charges"></a>Diverse toeslagen voor Transportbeheer

[!include [banner](../includes/banner.md)]

Zoals met alle diverse toeslagen, moeten door transport veroorzaakte toeslagen worden gekoppeld aan een toeslagcode. Anders worden deze niet weer als divers toeslagbedrag aan de order toegevoegd. De **toeslagcode** bepaalt hoe de toeslag wordt verwerkt in relatie tot de order en orderregel waaraan de toeslag wordt toegevoegd.

Ga naar **Transportbeheer > Instellingen > Beoordeling > Diverse toeslagen** om de kwalificatiecriteria te definiëren die bepalen wanneer een specifieke **toeslagcode** op een toeslag wordt toegepast.

U moet minimaal één instellen voor elke relevante **Toeslagmodule**-instelling (*Klant* en *Leverancier*) waarvoor **Type diverse toeslagen** is ingesteld op *Geen*. Als deze ontbreekt, worden het diverse toeslagbedag *niet* aan de order toegevoegd.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]