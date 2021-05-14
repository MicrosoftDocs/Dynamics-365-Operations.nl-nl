---
title: Stuklijst voor een productconfiguratiemodel onderhouden
description: Het uitvoeren van deze procedure vereist een bestaand productconfiguratiemodel.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b4ad73265e321b6339c061a7866b55cb2769954b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921312"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a>Stuklijst voor een productconfiguratiemodel onderhouden

[!include [banner](../../includes/banner.md)]

Het uitvoeren van deze procedure vereist een bestaand productconfiguratiemodel. Het model Geavanceerde luidspreker in het demobedrijf USMF wordt gebruikt voor het maken van deze procedure.

## <a name="add-a-bom-line"></a>Een stuklijstregel toevoegen

1. Ga naar **Productgegevensbeheer \> Producten \> Productconfiguratiemodellen**.
1. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer de Geavanceerde luidspreker voor deze procedure.  
1. Selecteer in de lijst de koppeling in de geselecteerde rij.
1. Vouw de sectie **Stuklijstregels** uit.
1. Selecteer **Toevoegen**.
1. Typ een waarde in het veld **Naam**.
1. Typ een waarde in het veld **Beschrijving**.
1. Selecteer **Opslaan**.

## <a name="add-bom-line-details"></a>Regeldetails van stuklijst toevoegen

1. Selecteer **Details van stuklijstregel**.
2. Typ of selecteer een waarde in het veld **Artikelnummer**.
    * Zo kunt u bijvoorbeeld het artikel M0055 selecteren.  
    * Voor elke regeleigenschap van de stuklijst kunt u selecteren of deze een vaste waarde heeft of aan een kenmerk is toegewezen.  
3. Schakel het selectievakje **Instellen** in.
4. Selecteer *Ja* in het veld **Berekening**.
    * Als u de eigenschap **Berekening** instelt op *Ja*, wordt de stuklijstregel in kostenberekeningen opgenomen.  
5. Selecteer het tabblad **Instellingen**.
6. Schakel het selectievakje **Instellen** in.
7. Voer een getal in het veld **Hoeveelheid** in.
    * Het hoeveelheidsveld bepaalt hoeveel van het artikel in de stuklijst wordt opgenomen. Dit moet een duidelijke kandidaat zijn voor een kenmerktoewijzing.  
8. Selecteer het tabblad **Dimensie**.
    * Controleer of een van de productdimensies actief is en daardoor een waarde of kenmerk moeten toegewezen krijgen.  
9. Selecteer **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]