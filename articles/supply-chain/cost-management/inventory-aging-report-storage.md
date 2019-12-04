---
title: Naar ouderdom gerangschikt voorraadrapport
description: In dit onderwerp wordt de functionaliteit beschreven waarmee u een naar ouderdom gerangschikt voorraadrapport kunt uitvoeren en de uitvoer beschikbaar kunt maken als een formulier en een grafiek.
author: AndersGirke
manager: AnnBe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 21411c104c854224ff3689dc8e080b88d9fc7d23
ms.sourcegitcommit: 9267608347c9781fb4ba70f1384ca24da69c716d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/15/2019
ms.locfileid: "2810246"
---
# <a name="inventory-aging-report"></a>Naar ouderdom gerangschikt voorraadrapport


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

In Microsoft Dynamics 365 Supply Chain Management kunt u een rapport **Naar ouderdom rangschikken van voorraad** uitvoeren en de uitvoer beschikbaar maken als een formulier en een grafiek. In het formulier worden kolommen en samengevoegde balansen dynamisch aangepast, afhankelijk van de indeling die is geconfigureerd. De grafiek biedt een visueel overzicht dat filters ondersteunt en waarmee u op details kunt inzoomen. Daarnaast kunt u met de gegevensentiteit met de naam **Naar ouderdom gerangschikt voorraadrapport** de resultaten van een rapport **Naar ouderdom rangschikken van voorraad** uitvoeren naar een indeling zoals een Microsoft Excel-of PDF-bestand.

Deze methode voor het uitvoeren van een rapport **Naar ouderdom rangschikken van voorraad** is handig wanneer de uitvoer veel regels bevat. De uitvoer bevat bijvoorbeeld een groot aantal regels als u 50.000 artikelen en 300 winkels hebt die zijn gemaakt als magazijnen en u een naar ouderdom gerangschikte voorraad per artikel, locatie en magazijn aanvraagt.

## <a name="run-an-inventory-aging-report"></a>Een naar ouderdom gerangschikt voorraadrapport uitvoeren

1. Ga naar **Kostenbeheer \> Query's en rapporten \> Opslag naar ouderdom gerangschikt voorraadrapport**.
1. Selecteer **Nieuw**.
1. Geef in het veld **Proces-id – Naam** een unieke naam op voor het rapport op.
1. Selecteer het rapport **Identificatie-id** en filter het zo nodig.

    De rapportuitvoering wordt altijd uitgevoerd in een batchtaak.

1. Nadat de batchtaak is voltooid, wordt de uitvoer weergegeven op de pagina **Opslag naar ouderdom gerangschikt voorraadrapport**.
1. Als u de uitvoer wilt weergeven als een formulier met een traditionele rasterindeling, selecteert u **Details weergeven**. Als u de uitvoer als een samengevoegde grafiek wilt weergeven, selecteert u **Grafiek weergeven**.

    > [!NOTE]
    > In het formulier worden geen subtotalen opgenomen die zijn gedefinieerd in de rapportindeling.

Met de gegevensentiteit **Naar ouderdom gerangschikt voorraadrapport** kunt u de uitvoer van een rapport **Naar ouderdom rangschikken van voorraad** exporteren door een filter voor het veld **Proces-id – Naam** toe te passen op alle indelingen die door Gegevensbeheer worden ondersteund.
