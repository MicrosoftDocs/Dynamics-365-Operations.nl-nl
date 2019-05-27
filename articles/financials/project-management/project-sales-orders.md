---
title: Projectverkooporders
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
ms.openlocfilehash: 1d54c98a08dc7cccb5cafbbe401d0ce25a276c25
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1529897"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projectverkooporders voor tijd- en materiaalprojecten

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Dit onderwerp beschrijft hoe u een verkooporder voor een project maakt. Verkooporders kunnen alleen worden gemaakt voor projecten van het type **Tijd en materiaal**.

Als een tijd- en materiaalproject meerdere financieringsbronnen heeft in het projectcontract, moet u de parameter **Verkooporders toestaan voor projecten met meerdere financieringsbronnen** op de pagina **Parameters voor Projectbeheer en boekhouding** inschakelen. 

> [!NOTE]
> - Ondersteuning voor projectverkooporders met meerdere financieringsbronnen is beschikbaar vanaf toepassingsversie 10.0.2 en hoger.
> - De parameter om de ondersteuning voor projectverkooporders met meerdere financieringsbronnen in te schakelen, wordt verwijderd in de releasewave van april 2020, waarna de functionaliteit altijd wordt ingeschakeld.

U kunt verkooporders op basis van een project op twee manieren maken:

- Ga naar het project zelf. Selecteer in het actievenster **Beheren > Artikeltaken > Verkooporder**. De projectgegevens worden standaard ingesteld op de verkooporder van het project. Als het projectcontract meer dan één financieringsbron heeft, moet u de financieringsbron selecteren om de klant voor de verkooporder te selecteren. Als er maar één financieringsbron voor het project is, wordt de klant automatisch ingesteld.
- Ga naar de lijstpagina **Alle verkooporders** en maak een nieuwe verkooporder. U moet het project selecteren voor de verkooporder. Nadat het project is geselecteerd, wordt de klant via de financieringsbron ingesteld of moet u de financieringsbron selecteren als het projectcontract meerdere financieringsbronnen heeft.

