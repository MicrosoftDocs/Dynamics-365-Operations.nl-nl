---
title: Btw-betalingen en afrondingsregels
description: In dit artikel wordt uitgelegd hoe de instelling van afrondingregels voor de btw-dienst werkt en afronding van het btw-saldo tijdens de taak Btw vereffenen en boeken.
author: ShylaThompson
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: pacheren
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1838666b57bf2ce4eb78f5d3486c03e4c2447646a121a537efd6bffa0019b96f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760681"
---
# <a name="sales-tax-payments-and-rounding-rules"></a>Btw-betalingen en afrondingsregels

[!include [banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe de instelling van afrondingregels voor de btw-dienst werkt en afronding van het btw-saldo tijdens de taak Btw vereffenen en boeken.

Periodiek moet btw worden aangegeven en betaald aan de belastingdienst. Dit kan worden uitgevoerd door het proces Btw vereffenen en boeken op de pagina Btw. Btw voor een periode wordt vereffend voor de btw-rekeningen en het btw-saldo wordt naar de rekening Btw-vereffening geboekt. Het btw-saldo, dat op de rekening Btw-vereffening wordt geboekt, kan worden afgerond zoals vereist wordt door de belastingdienst door een afrondingregel in te stellen op de pagina Btw. 

Het afrondingsverschil wordt geboekt naar de rekening Btw-afronding die is geselecteerd in het veld Rekeningen voor automatische transacties in het Grootboek.

Het onderstaande voorbeeld illustreert hoe de afrondingregel op Btw-dienst werkt.

## <a name="examples"></a>Voorbeelden

De totale btw voor een periode toont een creditsaldo van -98.765,43. De rechtspersoon inde meer btw dan dat betaald werd. Daarom is de rechtspersoon geld verschuldigd aan de belastingsdienst. 

De rechtspersoon wil een afrondingsmethode gebruiken waarmee het saldo wordt afgerond naar de dichtstbijzijnde 1,00. De gebruiker die verantwoordelijk is voor de btw-boekhouding voert de volgende stappen uit.

1. Klik op **Belasting** > **Indirecte belastingen** > **Btw** > **Btw-dienst**.
2. Selecteer op het sneltabblad **Algemeen** in het veld **Afrondingstype** de optie **Normaal**.
3. Typ 1,00 in het veld **Afronden**.
4. Wanneer het tijd is om de btw te betalen aan de belastingdienst, opent u de pagina **Belasting** > **Aangiften** > **Btw** > **Btw vereffenen en boeken**. Op de btw-vereffeningsrekening ziet u dat het bedrag van uw btw-belastingschuld van **98.765,43** is afgerond naar **98.765**.

In de volgende tabel ziet u hoe een bedrag van 98.765,43 wordt afgerond met behulp van elke afrondingsmethode die beschikbaar is in het veld **Afrondingstype** op de pagina **Btw-dienst**.

> [!NOTE]                                                                                  
> Als de afrondingswaarde is ingesteld op 0,00, geldt het volgende:
>
> - Voor normale afronding werkt het afronden hetzelfde als voor **afronden = 0,01**.
> - Voor de **opties Afrondingstype** **Omlaag**, **Omhoog** en **Eigen voordeel** is het gedrag hetzelfde als voor **Afronden = 1,00**.

| Optie Afrondingstype                | Afrondingswaarde = 0,01 | Afrondingswaarde = 0,10 | Afrondingswaarde = 1,00 | Afrondingswaarde = 100,00 | Afrondingswaarde = 0,00   |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|--------------------------|
| Normaal                              | 98,765.43              | 98,765.40              | 98,765.00              | 98,800.00                | 98,765.43                |
| Naar beneden afronden                            | 98,765.43              | 98,765.40              | 98,765.00              | 98,700.00                | 98,765.00                |
| Naar boven afronden                         | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                | 98,766.00                |
| Eigen voordeel, voor een creditsaldo | 98,765.43              | 98,765.40              | 98,765.00              | 98,700.00                | 98,765.00                |
| Eigen voordeel, voor een debitsaldo  | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                | 98,766.00                |

### <a name="normal-round-and-round-precision-is-001"></a>Normale afronding en afrondingsprecisie is 0,01

<table>
  <tr>
    <td>Afronding
    </td>
    <td>Berekeningsproces
    </td>
  </tr>
    <tr>
    <td>afronding (1,015, 0,01) = 1,02
    </td>
    <td>
      <ol>
        <li>afronding (1,015 / 0,01, 0) = afronding (101,5, 0) = 102
        </li>
        <li>102 * 0,01 = 1,02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>afronding (1,014, 0,01) = 1,01
    </td>
    <td> <ol>
        <li>afronding (1,014 / 0,01, 0) = afronding (101,4, 0) = 101
        </li>
        <li>101 * 0,01 = 1,01
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>afronding (1,011, 0,02) = 1,02
    </td>
    <td> <ol>
        <li>afronding (1,011 / 0,02, 0) = afronding (50,55, 0) = 51
        </li>
        <li>51 * 0,02 = 1,02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>afronding (1,009, 0,02) = 1,00
    </td>
    <td> <ol>
        <li>afronding (1,009 / 0,02, 0) = afronding (50,45, 0) = 50
        </li>
        <li>50 * 0,02 = 1,00
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> Als u Eigen voordeel selecteert, is de afronding altijd in het voordeel van de rechtspersoon. 

Zie de volgende onderwerpen voor meer informatie:
- [Btw-overzicht](indirect-taxes-overview.md)
- [Een btw-betaling maken](tasks/create-sales-tax-payment.md)
- [Btw-transacties maken in documenten](tasks/create-sales-tax-transactions-documents.md)
- [Geboekte btw-transacties weergeven](tasks/view-posted-sales-tax-transactions.md)
- [Afrondingsfunctie](/previous-versions/dynamics/ax-2012/reference/aa850656(v=ax.60))




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
