---
title: Indelingen voor elektronische rapportage wijzigen door Excel-sjablonen opnieuw toe te passen
description: In dit onderwerp wordt beschreven hoe u de indeling voor elektronische rapportage, die wordt gebruikt voor het genereren van bedrijfsdocumenten, kunt wijzigen door een gewijzigde Excel-sjabloon opnieuw toe te passen.
author: NickSelin
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d828412e0d804acf6e6141778512e899bc78a7d
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092839"
---
# <a name="modify-electronic-reporting-formats-by-reapplying-excel-templates"></a>Indelingen voor elektronische rapportage wijzigen door Excel-sjablonen opnieuw toe te passen

[!include [banner](../includes/banner.md)]

Het hulpmiddel Elektronische rapportage (ER) wordt gebruikt voor het genereren van bedrijfsdocumenten in elektronische vorm. Als u een bedrijfsdocument wilt genereren, moet u een indeling voor elektronische rapportage maken en vervolgens de ER-ontwerper gebruiken om de indeling van het bedrijfsdocument te bepalen en op te geven welke gegevens moeten worden opgenomen. Vervolgens kunt u de ER-indeling uitvoeren om het bedrijfsdocument te genereren.

Het ER-hulpmiddel kan worden gebruikt om bedrijfsdocumenten als Microsoft Excel-bestanden te genereren. U kunt een Excel-document als sjabloon gebruiken voor deze documenten. U geeft de documentindeling in de ER-ontwerper op door in de opgegeven ER-indeling de inhoud te importeren van het Excel-document dat u wilt gebruiken als sjabloon. Speel de taakbegeleiding **ER Een configuratie ontwerpen voor het genereren van rapporten in OPENXML-indeling** (onderdeel van het bedrijfsproces 7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)) af voor meer informatie en en om te oefenen met dit scenario.

Als u het Excel-document bewerkt dat wordt gebruikt als een sjabloon voor een bedrijfsdocument, kunt u met nieuwe ER-functionaliteit de bijgewerkte sjabloon opnieuw toepassen op de ER-indeling. De ER-indeling wordt vervolgens bijgewerkt zodat deze in overeenstemming is met de bijgewerkte sjabloon. Speel de taakbegeleiding **Een indeling voor elektronische aangifte wijzigen door een Excel-sjabloon opnieuw toe te passen** (onderdeel van het bedrijfsproces 7.5.5.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10683)) af voor meer informatie over deze functionaliteit. Als onderdeel van de taakbegeleidingsstap voor het importeren van een bijgewerkte sjabloon gebruikt u de gewijzigde sjabloon van het Excel-bestand met het betalingsrapport (SampleVendPaymWsReport2) als sjabloon.
