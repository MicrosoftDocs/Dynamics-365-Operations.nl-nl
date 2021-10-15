---
title: Diverse toeslagen voor Transportbeheer
description: In dit onderwerp wordt uitgelegd hoe door transport veroorzaakte toeslagen moeten worden gekoppeld aan een toeslagcode.
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 776c73b1a29666e393bed7c40059a578fe86cb0d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576179"
---
# <a name="transportation-management-miscellaneous-charges"></a>Diverse toeslagen voor Transportbeheer

[!include [banner](../includes/banner.md)]

Zoals met alle diverse toeslagen, moeten door transport veroorzaakte toeslagen worden gekoppeld aan een toeslagcode. Anders worden deze niet weer als divers toeslagbedrag aan de order toegevoegd. De **toeslagcode** bepaalt hoe de toeslag wordt verwerkt in relatie tot de order en orderregel waaraan de toeslag wordt toegevoegd.

Ga naar **Transportbeheer > Instellingen > Beoordeling > Diverse toeslagen** om de kwalificatiecriteria te definiëren die bepalen wanneer een specifieke **toeslagcode** op een toeslag wordt toegepast.

U moet minimaal één instellen voor elke relevante **Toeslagmodule**-instelling (*Klant* en *Leverancier*) waarvoor **Type diverse toeslagen** is ingesteld op *Geen*. Als deze ontbreekt, worden het diverse toeslagbedag *niet* aan de order toegevoegd.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]