---
title: Detailhandelparameters configureren die gevolgen hebben voor detailhandeloverzichten
description: Dit onderwerp demonstreert configuraties voor detailhandelparameters die van invloed zijn op hoe detailhandelsoverzichten worden gemaakt en geboekt.
author: josaw1
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b9a0386a4d61395903e82d988244dd131c1febaf
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867266"
---
# <a name="configure-retail-parameters-that-affect-retail-statements"></a>Detailhandelparameters configureren die gevolgen hebben voor detailhandeloverzichten

[!include[task guide banner](../includes/task-guide-banner.md)]

Dit onderwerp demonstreert configuraties voor detailhandelparameters die van invloed zijn op hoe detailhandelsoverzichten worden gemaakt en geboekt. Deze procedure gebruikt het demobedrijf USRT.

1. Ga in het navigatievenster naar **Modules > Detailhandel en commerce > Instelling van hoofdkantoor > Parameters > Detailhandelparameters**.
2. Selecteer het tabblad **Boeking**.
    - Selecteer **Ja** als u de periodieke kortingsbedragen specifiek wilt boeken.  
    - Selecteer **Standaard** om standaardrekeningen te gebruiken of selecteer **Periodiek** als u wilt definiëren welke rekening moet worden gebruikt voor elke periodieke rekening.  
      - Selecteer **Overzicht** als voorraadregels moeten worden samengevoegd indien mogelijk.  
      - Selecteer **Ja** als facturen en betalingen automatisch moeten worden vereffend als onderdeel van het overzichtsboekingsproces.  
      - Selecteer **Ja** als kluisstortingstransacties moeten worden samengevoegd.  
      - Selecteer **Ja** als bankstortingstransacties moeten worden samengevoegd.  
      - Selecteer **Ja** om samenvoeging in te schakelen voor overzichtsboeking.  
      - Selecteer **Ja** om orders parallel te maken en te verwerken wanneer overzichten worden geboekt.  
      - Voer de maximale orders in die moeten worden verwerkt in elke batchtaak.  
3. Selecteer **Opslaan**.

