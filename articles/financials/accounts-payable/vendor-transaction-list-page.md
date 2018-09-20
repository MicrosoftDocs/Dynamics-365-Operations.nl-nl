---
title: Lijstpagina met leverancierstransacties
description: Dit onderwerp bevat informatie over de lijstpagina met leverancierstransacties voor Microsoft Dynamics 365 for Finance and Operations.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: 1ef7d97f059801f2fb2c0d451546b57055208f81
ms.contentlocale: nl-nl
ms.lasthandoff: 08/31/2018

---

# <a name="vendor-transaction-list-page"></a>Lijstpagina met leverancierstransacties

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a>Vereffeningen weergeven

Het tabblad **Vereffeningen weergeven** in het actievenster biedt snelle toegang tot de vereffeningshistorie en meer informatie over de gehele vereffeningstransactie. U kunt ook extra transacties weergeven die zijn gerelateerd aan de geselecteerde transactie, omdat ze deel uitmaakten van dezelfde vereffening of omdat dit betalingen zijn die zijn gemaakt in hetzelfde betalingsjournaal.

1. Selecteer **Leveranciers \> Alle leveranciers**.
2. Selecteer een leverancier die transacties heeft en selecteer vervolgens **Leverancier \> Transacties**.
3. Selecteer een transactie om te onderzoeken.
4. Selecteer het tabblad **Vereffeningen weergeven** in het actievenster.

    Het dialoogvenster **Vereffeningen weergeven** wordt geopend bevat de geselecteerde transactie en alle documenten die ervoor zijn vereffend. Dit dialoogvenster lijkt op de weergave van de vereffeningshistorie, maar het bevat alle gerelateerde documenten.

5. In dit dialoogvenster kunt u verschillende taken uitvoeren. Selecteer een of meer boekstukken en selecteer een van de volgende menu´s:

   - **Boekhouding weergeven**: alle boekstukken die zijn gerelateerd aan de geselecteerde documenten, worden weergegeven. Selecteer **Sluiten** om het dialoogvenster te sluiten.
   - **Exporteren** : de geselecteerde boekstukken naar Microsoft Excel exporteren.
   - **Verwante betalingen weergeven**: alle betalingsjournaaltransacties weergeven die zijn gemaakt in het betalingsjournaal dat is gerelateerd aan het geselecteerde document. Bovendien worden alle vereffeningen weergegeven die zijn gerelateerd aan deze betalingen. Het label van dit menu wordt ook gewijzigd in **Vereffeningen weergeven**. Selecteer **Vereffeningen weergeven** om alleen de transacties te tonen die werden weergegeven toen u voor het eerst het dialoogvenster **Vereffeningen weergeven** opende.
    - **Transacties vereffenen**: dit menu wordt weergegeven als het oorspronkelijke document dat is geselecteerd, niet volledig is vereffend. Wanneer u het menu selecteert, verschijnt het dialoogvenster **Transacties vereffenen**. Hierin kunt u transacties voor vereffening selecteren.
    - **Vereffening ongedaan maken**: dit menu wordt weergegeven als het oorspronkelijke document dat is geselecteerd, volledig is vereffend. Wanneer u het menu selecteert, verschijnt het dialoogvenster **Vereffening ongedaan maken**. Hierin kunt u de vereffeningen ongedaan maken die zijn uitgevoerd voor dat document.

