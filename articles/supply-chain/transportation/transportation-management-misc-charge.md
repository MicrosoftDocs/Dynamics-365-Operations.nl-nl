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
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 53c25f204e98a911e9697f5bb950706555749a55
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828303"
---
# <a name="transportation-management-miscellaneous-charges"></a>Diverse toeslagen voor Transportbeheer

[!include [banner](../includes/banner.md)]

Zoals met alle diverse toeslagen, moeten door transport veroorzaakte toeslagen worden gekoppeld aan een toeslagcode. Anders worden deze niet weer als divers toeslagbedrag aan de order toegevoegd. De **toeslagcode** bepaalt hoe de toeslag wordt verwerkt in relatie tot de order en orderregel waaraan de toeslag wordt toegevoegd.

Ga naar **Transportbeheer > Instellingen > Beoordeling > Diverse toeslagen** om de kwalificatiecriteria te definiëren die bepalen wanneer een specifieke **toeslagcode** op een toeslag wordt toegepast.

U moet minimaal één instellen voor elke relevante **Toeslagmodule**-instelling (*Klant* en *Leverancier*) waarvoor **Type diverse toeslagen** is ingesteld op *Geen*. Als deze ontbreekt, worden het diverse toeslagbedag *niet* aan de order toegevoegd.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]