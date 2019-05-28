---
title: Stuklijst voor een productconfiguratiemodel onderhouden
description: Het uitvoeren van deze procedure vereist een bestaand productconfiguratiemodel.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 457aa5720919d8455a3099b200980bb36f60577f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567717"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a>Stuklijst voor een productconfiguratiemodel onderhouden

[!include [task guide banner](../../includes/task-guide-banner.md)]

Het uitvoeren van deze procedure vereist een bestaand productconfiguratiemodel. Het model Geavanceerde luidspreker in het demobedrijf USMF wordt gebruikt voor het maken van deze procedure.


## <a name="add-a-bom-line"></a>Een stuklijstregel toevoegen
1. Klik op Definitie van productvariantmodel.
2. Klik op Productconfiguratiemodellen.
3. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer de Geavanceerde luidspreker voor deze procedure.  
4. Klik in de lijst op de koppeling in de geselecteerde rij.
5. Vouw de sectie Stuklijstregels uit.
6. Klik op Toevoegen.
7. Typ een waarde in het veld Naam.
8. Typ een waarde in het veld Omschrijving.
9. Klik op Opslaan.

## <a name="add-bom-line-details"></a>Regeldetails van stuklijst toevoegen
1. Klik op Regeldetails van stuklijst.
2. Typ of selecteer een waarde in het veld Artikelnummer.
    * Zo kunt u bijvoorbeeld het artikel M0055 selecteren.  
    * Voor elke regeleigenschap van de stuklijst kunt u selecteren of deze een vaste waarde heeft of aan een kenmerk is toegewezen.  
3. Schakel het selectievakje Instellen in.
4. Selecteer Ja in het veld Berekening.
    * Het instellen van de eigenschap Berekening op Ja zorgt ervoor dat de stuklijstregel in kostenberekeningen wordt opgenomen.  
5. Klik op het tabblad Instellingen.
6. Schakel het selectievakje Instellen in.
7. Voer in het veld Hoeveelheid een getal in.
    * Het hoeveelheidsveld bepaalt hoeveel van het artikel in de stuklijst wordt opgenomen. Dit moet een duidelijke kandidaat zijn voor een kenmerktoewijzing.  
8. Klik op het tabblad Dimensies.
    * Controleer of een van de productdimensies actief is en daardoor een waarde of kenmerk moeten toegewezen krijgen.  
9. Klik op OK.

