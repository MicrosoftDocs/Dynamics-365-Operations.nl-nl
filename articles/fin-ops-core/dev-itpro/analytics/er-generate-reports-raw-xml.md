---
title: Rapporten genereren door inhoud toe te voegen als onbewerkte XML
description: U kunt ER-indelingen (elektronische rapportage) ontwerpen die uitgaande documenten genereren in XML-indeling.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 07fb63f7d4255ca4f693e399a066fe3952e3df1b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566669"
---
# <a name="generate-reports-by-adding-content-as-raw-xml"></a>Rapporten genereren door inhoud toe te voegen als onbewerkte XML

[!include[banner](../includes/banner.md)]

U kunt het nieuwe indelingselement **RAW XML** gebruiken om ER-indelingen te ontwerpen die uitgaande documenten in XML-indeling genereren. In sommige gevallen wilt u wellicht liever onbewerkte XML-gegevens toevoegen aan deze rapporten om een of meer van de volgende redenen:

- Het is handiger om onbewerkte XML te gebruiken voor het oorspronkelijke ontwerp en doorlopend onderhoud van een rapport, omdat de XML-structuur automatisch kan worden gegenereerd door het uitvoeren van een runtime-expressie. Meerdere bindingen hoeven daarom niet te worden bepaald voor meerdere indelingselementen tijdens het ontwerpen. Het is mogelijk wanneer de gegevensbronnen die u gebruikt, informatie bevatten die kan worden gebruikt voor het maken van XML-elementen terwijl het rapport wordt gegenereerd.
- Er kan geen andere methode worden gebruikt voor het vullen van het rapport met XML-inhoud die eerder is ontvangen en opgeslagen in het systeem. Bijvoorbeeld, de XML-respons die wordt gegenereerd, kan de inhoud van een XML-aanvraag bevatten die eerder is verzonden.
- Er kan geen andere methode worden gebruikt voor het invoegen van tekens in het gegenereerde document op basis van hun numerieke codes. Voor sommige talen en tekens bestaan geen codes van dit type. Voorbeelden zijn de Griekse letter rho (ρ) en HTML-entiteitcodes, zoals \&eacute; voor een *e* met een accent aigu (é).

> [!NOTE]
> Houd er rekening mee dat het raamwerk niet bepaalt of de XML-inhoud die in het gegenereerde document wordt geplaatst met behulp van het indelingselement **RAW XML**, juist is.

Als u meer wilt weten over deze functie, speelt u de taakbegeleidingen **ER onbewerkte XML-gegevens gebruiken om XML-rapporten te genereren (deel 1: Ontwerpgegevensmodel)** en **ER onbewerkte XML-gegevens gebruiken om XML-rapporten te genereren (deel 2: Rapport ontwerpen en uitvoeren)** af, die deel uitmaken van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)** en kunnen worden gedownload uit het [Microsoft Downloadcentrum](https://go.microsoft.com/fwlink/?linkid=874684). Deze taakbegeleidingen begeleiden u door het proces van het configureren van een ER-indeling om onbewerkte XML-gegevens in gegenereerde bestanden in te voegen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]