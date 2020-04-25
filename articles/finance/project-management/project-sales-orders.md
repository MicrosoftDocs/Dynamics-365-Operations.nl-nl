---
title: Projectverkooporders voor tijd- en materiaalprojecten
description: In dit onderwerp wordt uitgelegd hoe u op projecten gebaseerde verkooporders voor tijd- en materiaalprojecten maakt.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: d19ee9de70cd14c78a997b7a87c10b53ab3917b0
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249088"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projectverkooporders voor tijd- en materiaalprojecten

[!include[banner](../includes/banner.md)]

Dit onderwerp beschrijft hoe u een verkooporder voor een project maakt. Verkooporders kunnen alleen worden gemaakt voor projecten van het type **Tijd en materiaal**.

Als een tijd- en materiaalproject meerdere financieringsbronnen heeft in het projectcontract, moet u de parameter **Verkooporders toestaan voor projecten met meerdere financieringsbronnen** op de pagina **Parameters voor Projectbeheer en boekhouding** inschakelen. 

> [!NOTE]
> - Ondersteuning voor projectverkooporders met meerdere financieringsbronnen is beschikbaar vanaf toepassingsversie 10.0.2 en hoger.
> - De parameter om de ondersteuning voor projectverkooporders met meerdere financieringsbronnen in te schakelen, wordt verwijderd in de releasewave van april 2020, waarna de functionaliteit altijd wordt ingeschakeld.

U kunt verkooporders op basis van een project op twee manieren maken:

- Ga naar het project zelf. Selecteer in het actievenster **Beheren > Artikeltaken > Verkooporder**. De projectgegevens worden standaard ingesteld op de verkooporder van het project. Als het projectcontract meer dan één financieringsbron heeft, moet u de financieringsbron selecteren om de klant voor de verkooporder te selecteren. Als er maar één financieringsbron voor het project is, wordt de klant automatisch ingesteld.
- Ga naar de lijstpagina **Alle verkooporders** en maak een nieuwe verkooporder. U moet het project selecteren voor de verkooporder. Nadat het project is geselecteerd, wordt de klant via de financieringsbron ingesteld of moet u de financieringsbron selecteren als het projectcontract meerdere financieringsbronnen heeft.

