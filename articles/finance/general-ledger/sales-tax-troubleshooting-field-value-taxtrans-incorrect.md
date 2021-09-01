---
title: Onjuiste veldwaarde in TaxTrans
description: Dit onderwerp bevat informatie over het oplossen van problemen met onjuiste veldwaarden in TaxTrans.
author: bijian
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 5c1c034c6037d2e8920d9744903debebb2dc537f2644093d5e1eef66f2681191
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746339"
---
# <a name="incorrect-field-value-in-taxtrans"></a>Onjuiste veldwaarde in TaxTrans

[!include [banner](../includes/banner.md)]

Als een veldwaarde in **TaxTrans** onjuist is, gebruikt u de informatie in dit onderwerp om het probleem op te lossen.

## <a name="overview-of-values"></a>Overzicht van waarden
In de volgende lijst wordt weergegeven dat **TaxTrans**, **TaxUncommitted** en **TmpTaxWorkTrans** gelijksoortige gegevenssets zijn, maar verschillend werken.

  - **TaxTrans** is het definitieve geboekte resultaat van een belastingtransactie dat in de database blijft staan.
  - **TaxUncommitted** is het tussenliggende berekende belastingresultaat dat in de database blijft staan (indien van toepassing), dat later wordt gebruikt bij het boeken.
  - **TmpTaxWorkTrans** is het tijdelijke berekende belastingresultaat in de geheugentabel (Tabeltype = InMemory).

Als u de hoofdoorzaak van een onjuiste **TaxTrans**-kolom hebt gevonden, hebt u ook de hoofdoorzaak van een onjuiste **TaxUncommitted**- of **TmpTaxWorkTrans**-kolom gevonden. Dit komt omdat de drie kolommen van elkaar zijn gekopieerd.

Normaal gesproken wordt tijdens de belastingberekening **TmpTaxWorkTrans** gegenereerd en vervolgens, indien van toepassing, wordt **TaxUncommitted** gegenereerd. Tijdens het boeken van belasting wordt **TaxTrans** gegenereerd.


## <a name="add-breakpoints"></a>Onderbrekingspunten toevoegen
Voer de volgende stappen uit om onderbrekingspunten toe te voegen: 

1. Voeg extensies en onderbrekingspunten toe in *insert()* en *update()* in de extensies zoals hieronder weergegeven.

     - **TaxTrans**

        ```x++
        [ExtensionOf(tableStr(TaxTrans))]
        public final class TaxTrans_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - **TaxUncommitted**

        ```x++
        [ExtensionOf(tableStr(TaxUncommitted))]
        public final class TaxUncommitted_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - **TmptaxWorkTrans**

        ```x++
        [ExtensionOf(tableStr(TmpTaxWorkTrans))]
        public final class TmpTaxWorkTrans_Extension
        {
            public void insert(boolean _ignoreCalculatedSalesTax)
            {
                next insert(_ignoreCalculatedSalesTax);
            }
        
            public void update(boolean _ignoreCalculatedSalesTax)
            {
                next update(_ignoreCalculatedSalesTax);
            }
        
        }
        
        ```

2. U kunt ook direct onderbrekingspunten toevoegen wanneer **TaxUncommitted** niet is opgenomen.

     - *TaxTrans.insert()*, *TaxTrans.update()*
     - *TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*

## <a name="reproduce-and-debug"></a>Reproduceren en fouten opsporen

Nadat de onderbrekingspunten zijn ingesteld, is elke wijziging van de gegevenspersistentie zichtbaar tijdens foutopsporing. Als u de hoofdoorzaak wilt vinden van een onjuiste kolom met **TaxTrans**, **TaxUncommitted** of **TmpTaxWorkTrans**, controleert en noteert u de volgende punten:

- Het laatste onderbrekingspunt waar de kolom juist is.
- Het eerste onderbrekingspunt waar de kolom onjuist is.
- Wat er tussen deze twee punten gebeurt.

## <a name="determine-whether-customization-exists"></a>Bekijk of er een aanpassing bestaat
Als u de stappen in de vorige secties hebt voltooid, maar het probleem niet hebt kunnen oplossen, bekijkt u of er aanpassing bestaat. Neem, als er geen aanpassing bestaat, contact op met Microsoft Ondersteuning voor hulp.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

