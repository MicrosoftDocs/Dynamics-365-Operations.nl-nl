---
title: Servicesjablonen
description: U kunt een serviceovereenkomst als sjabloon definiëren en de regels van de sjabloon later naar een andere serviceovereenkomst of serviceorder kopiëren.
author: ShylaThompson
manager: tfehr
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a8a92d67afe5fd427d1bc272c59e459cb1547d22
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983225"
---
# <a name="service-templates"></a>Servicesjablonen

[!include [banner](../includes/banner.md)]

U kunt een serviceovereenkomst als sjabloon definiëren en de regels van de sjabloon later naar een andere serviceovereenkomst of serviceorder kopiëren.

## <a name="example"></a>Voorbeeld

Een klant voor wie u een service levert, heeft identieke dienstliften op vijf verschillende locaties.

U wilt vijf serviceovereenkomsten instellen voor de klant, één overeenkomst voor elke locatie.
Als u de instellingen niet steeds wilt herhalen en ervoor wilt zorgen dat de instellingsgegevens in de serviceovereenkomsten gelijk zijn, kunt u een serviceovereenkomst maken en deze opgeven als sjabloon voor de servicewerkzaamheden aan de liften.

U kunt de sjabloonregels nu kopiëren naar de vijf nieuwe serviceovereenkomsten, zodat elke serviceovereenkomst wordt gevuld met de regels uit de sjabloon.

## <a name="create-a-template"></a>Een sjabloon maken

Wanneer u een servicesjabloon maakt, maakt u een serviceovereenkomst en de vereiste regels hierin en koppelt u de serviceovereenkomst naar een servicesjabloongroep.

> [!NOTE]
> U kunt een serviceovereenkomst alleen definiëren als sjabloon als hieraan geen serviceorders zijn gekoppeld. Daarnaast kunnen er geen serviceorders worden gegenereerd van een serviceovereenkomst die is gedefinieerd als sjabloon.

## <a name="copy-template-lines"></a>Sjabloonregels kopiëren

U kunt sjabloonregels uit een servicesjabloon kopiëren naar een andere serviceovereenkomst of naar een serviceorder.

Wanneer u sjabloonregels naar serviceorders of serviceovereenkomsten kopieert, worden de sjabloongroepen weergegeven in een structuurweergave waarin elke groep kan worden uitgevouwen. In deze weergave kunt u elke sjabloon en sjabloonregel bekijken.

U kunt eenvoudiger bepalen welke servicesjabloonregels u wilt kopiëren als u de sjablonen hebt gegroepeerd onder namen die het gebruik van de sjablonen aanduiden.

## <a name="related-topics"></a>Verwante onderwerpen

[Servicesjabloonregels kopiëren](copy-service-template-lines.md)
