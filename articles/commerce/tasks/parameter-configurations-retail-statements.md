---
title: Parameters configureren die gevolgen hebben voor detailhandeloverzichten
description: Dit onderwerp demonstreert configuraties voor Commerce-parameters die van invloed zijn op hoe overzichten worden gemaakt en geboekt.
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
ms.openlocfilehash: d8cae6d2fa7c469f50fa92141a6cb5a0af1df4b0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022117"
---
# <a name="configure-parameters-that-affect-retail-statements"></a>Parameters configureren die gevolgen hebben voor detailhandeloverzichten

[!include[task guide banner](../includes/task-guide-banner.md)]

Dit onderwerp demonstreert configuraties voor Commerce-parameters die van invloed zijn op hoe overzichten worden gemaakt en geboekt. Deze procedure gebruikt het demobedrijf USRT.

1. Ga in het navigatievenster naar **Modules > Retail en Commerce > Instelling van hoofdkantoor > Parameters > Commerce-parameters**.
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

