---
title: Stuklijst voor een productconfiguratiemodel onderhouden
description: Het uitvoeren van deze procedure vereist een bestaand productconfiguratiemodel.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd78b06f10d0c9b1df57dacdd824b06ebe414b3b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577283"
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