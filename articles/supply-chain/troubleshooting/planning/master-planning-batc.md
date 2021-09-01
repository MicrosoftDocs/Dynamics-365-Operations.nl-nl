---
title: U kunt hoofdplanningsartikelen niet filteren op de gerelateerde waarden van de behoefteplanningsgroep
description: U kunt hoofdplanningsartikelen niet filteren op de gerelateerde waarden van de behoefteplanningsgroep.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 9750a73f0962179512c5e21a614a276c313ff975b7494f31589ca936886ecf6e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781388"
---
# <a name="you-cant-filter-master-planning-items-by-their-related-coverage-group-values"></a>U kunt hoofdplanningsartikelen niet filteren op de gerelateerde waarden van de behoefteplanningsgroep

KB-nummer: 4612572

## <a name="symptoms"></a>Symptomen

U wilt de artikelen filteren die worden opgenomen in een batchtaak voor de hoofdplanning op basis van de waarden van gerelateerde records uit de tabel voor artikelbehoefteplanning. (U wilt artikelen bijvoorbeeld filteren op de waarde die ervoor is ingesteld bij **Leverancier** en/of **Behoefteplanningsgroep**). Met de filterinstellingen voor de batchtaak kunt u een join maken vanuit de tabel **Artikelen** naar de tabel **Artikelbehoefteplanning** en vervolgens veldwaarden opgeven vanuit de tabel voor artikelbehoefteplanning in uw query. Nadat u deze instelling hebt voltooid, worden echter nog steeds geplande orders gemaakt voor de volledige artikelbehoefteplanning, niet alleen voor de artikelen die overeenkomen met de opgegeven veldwaarden uit de tabel voor artikelbehoefteplanning.

## <a name="resolution"></a>Oplossing

Het batchtaakfilter kan alleen op artikelen filteren. Hoewel u een join kunt toevoegen aan de tabel **Artikelbehoefteplanning**, zijn filterinstellingen die u voor die tabel maakt, niet van invloed op de query-uitvoer. Tijdens de uitvoering wordt de planning uitgevoerd voor alle behoefteplanningsgroepen en alle variaties die de gefilterde artikelen hebben. Nadat een artikel al is opgenomen in de uitvoering, zijn behoefteplanningsgroepen die zijn opgenomen in het artikelfilter, niet van invloed op de planningsuitvoer.
