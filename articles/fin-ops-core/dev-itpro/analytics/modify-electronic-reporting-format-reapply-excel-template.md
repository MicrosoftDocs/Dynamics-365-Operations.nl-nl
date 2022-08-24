---
title: Indelingen voor elektronische rapportage wijzigen door Excel-sjablonen opnieuw toe te passen
description: In dit artikel wordt beschreven hoe u de indeling voor elektronische rapportage, die wordt gebruikt voor het genereren van bedrijfsdocumenten, kunt wijzigen door een gewijzigde Excel-sjabloon opnieuw toe te passen.
author: kfend
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
ms.openlocfilehash: 02423a75d96bef0452b8555f8c7a9f0aca0b6771
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283523"
---
# <a name="modify-electronic-reporting-formats-by-reapplying-excel-templates"></a>Indelingen voor elektronische rapportage wijzigen door Excel-sjablonen opnieuw toe te passen

[!include [banner](../includes/banner.md)]

Het hulpmiddel Elektronische rapportage (ER) wordt gebruikt voor het genereren van bedrijfsdocumenten in elektronische vorm. Als u een bedrijfsdocument wilt genereren, moet u een indeling voor elektronische rapportage maken en vervolgens de ER-ontwerper gebruiken om de indeling van het bedrijfsdocument te bepalen en op te geven welke gegevens moeten worden opgenomen. Vervolgens kunt u de ER-indeling uitvoeren om het bedrijfsdocument te genereren.

Het ER-hulpmiddel kan worden gebruikt om bedrijfsdocumenten als Microsoft Excel-bestanden te genereren. U kunt een Excel-document als sjabloon gebruiken voor deze documenten. U geeft de documentindeling in de ER-ontwerper op door in de opgegeven ER-indeling de inhoud te importeren van het Excel-document dat u wilt gebruiken als sjabloon. Speel de taakbegeleiding **ER Een configuratie ontwerpen voor het genereren van rapporten in OPENXML-indeling** (onderdeel van het bedrijfsproces 7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)) af voor meer informatie en en om te oefenen met dit scenario. Als onderdeel van de taakbegeleidingsstap voor het importeren van een Excel-sjabloon gebruikt u de oorspronkelijke sjabloon van het Excel-bestand met het betalingsrapport [SampleVendPaymWsReport](https://download.microsoft.com/download/e/6/b/e6bb79f0-cc08-44af-96fa-49c7929d4fb8/SampleVendPaymWsReport.xlsx).

Als u het Excel-document bewerkt dat wordt gebruikt als een sjabloon voor een bedrijfsdocument, kunt u met nieuwe ER-functionaliteit de bijgewerkte sjabloon opnieuw toepassen op de ER-indeling. De ER-indeling wordt vervolgens bijgewerkt zodat deze in overeenstemming is met de bijgewerkte sjabloon. Speel de taakbegeleiding **Een indeling voor elektronische aangifte wijzigen door een Excel-sjabloon opnieuw toe te passen** (onderdeel van het bedrijfsproces 7.5.5.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10683)) af voor meer informatie over deze functionaliteit. Als onderdeel van de taakbegeleidingsstap voor het importeren van een bijgewerkte sjabloon gebruikt u de gewijzigde sjabloon van het Excel-bestand met het betalingsrapport [SampleVendPaymWsReport2](https://download.microsoft.com/download/3/1/0/3104d397-c9c5-4227-b68e-f98625313801/SampleVendPaymWsReport2.xlsx).

## <a name="additional-resources"></a>Aanvullende bronnen

[Een sjabloon bewerken](er-fillable-excel.md#update-a-template)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
