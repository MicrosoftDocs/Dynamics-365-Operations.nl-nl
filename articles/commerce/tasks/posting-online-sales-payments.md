---
title: Boeking van online verkopen en betalingen
description: Deze procedure doorloopt de configuratie en uitvoering van een terugkerende batchtaak om verkooporders en betalingen voor online winkeltransacties te maken.
author: jashanno
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.industry: Retail
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
ms.openlocfilehash: 0db3414a41a27b5c383eddd4c3e7650fb828b422
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285681"
---
# <a name="posting-of-online-sales-and-payments"></a>Boeking van online verkopen en betalingen

[!include [banner](../includes/banner.md)]

Deze procedure doorloopt de configuratie en uitvoering van een terugkerende batchtaak om verkooporders en betalingen voor online winkeltransacties te maken.

Het boeken van online verkopen en betalingen bestaat uit twee stappen.

- Online gegevens van de Commerce-transactiegegevens ophalen in HQ.
- Orders synchroniseren voor het maken van verkooporders in HQ.

U kunt de gegevens van de online transactie ophalen door de P-taak handmatig uit te voeren of door een periodieke batchtaak te maken.

### <a name="manually-running-the-p-job"></a>De P-taak hand matiguitvoeren

1. Ga naar Alle werkgebieden > Retail en Commerce IT.
2. Klik op Distributieplanning.
3. Selecteer P-0001.
4. Pas indien nodig de kanaaldatabasegroepen aan.
5. Klik op Nu uitvoeren.
6. Klik op Ja.

### <a name="scheduling-a-recurring-p-job"></a>Een periodieke P-taak plannen

1. Ga naar Alle werkgebieden > Retail en Commerce IT.
2. Klik op Distributieplanning.
3. Selecteer P-0001.
4. Klik op Batchtaak maken.
5. Klik op Op de achtergrond uitvoeren.
5. Schakel Batchverwerking in.
6. Klik op Terugkeerpatroon.
7. Selecteer de optie Geen einddatum.
8. Voer in het veld Telling de interval tussen de uitvoeringen in minuten in. Dit is meestal 5-10.
9. Klik op OK.
10. Klik op OK.

U kunt orders synchroniseren door handmatig de taak "Orders synchroniseren" uit te voeren of door een periodieke batchtaak te maken.

### <a name="manually-running-order-synchronization"></a>Ordersynchronisatie handmatig uitvoeren 

Volg deze stappen om de taak "Orders synchroniseren" één keer handmatig uit te voeren.

1. Ga naar Alle werkruimten > Financiën van winkel.
2. Klik op Orders synchroniseren.
3. Selecteer in het veld Organisatiehiërarchie de optie 'Winkels per regio'.
    * Selecteer een specifieke online winkel of een knooppunt als u de batchtaak wilt maken voor een groep winkels.  
    * Klik op de pijl om uw selectie toe te voegen.  
4. Klik op het tabblad Op de achtergrond uitvoeren.
5. Schakel Batchverwerking uit.
6. Klik op Terugkeerpatroon.
7. Optie Beëindigen na selecteren
8. In het veld Beëindigen na voert u 1 in.
9. Klik op OK.
10. Klik op OK.

### <a name="scheduling-recurring-order-synchronization"></a>Een periodieke ordersynchronisatie plannen

Deze procedure doorloopt de configuratie en uitvoering van een terugkerende batchtaak om verkooporders en betalingen voor online winkeltransacties te maken. Deze procedure gebruikt het demobedrijf USRT.

1. Ga naar Alle werkruimten > Financiën van winkel.
2. Klik op Orders synchroniseren.
3. Selecteer in het veld Organisatiehiërarchie de optie 'Winkels per regio'.
    * Selecteer een specifieke online winkel of een knooppunt als u de batchtaak wilt maken voor een groep winkels.  
    * Klik op de pijl om uw selectie toe te voegen.  
4. Klik op het tabblad Op de achtergrond uitvoeren.
5. Schakel Batchverwerking in
6. Klik op Terugkeerpatroon.
7. Selecteer de optie Geen einddatum.
8. Voer in het veld Telling de interval tussen de uitvoeringen in minuten in. Dit is meestal 2-20
9. Klik op OK.
10. Klik op OK.

## <a name="data-entities-involved-in-the-process"></a>Gegevensentiteiten die betrokken zijn bij het proces

- RetailTransactionTable
- RetailTransactionAddressTrans
- RetailTransactionInfocodeTrans
- RetailTransactionTaxTrans
- RetailTransactionSalesTrans
- RetailTransactionTaxMeasure
- RetailTransactionDiscountTrans
- RetailTransactionTaxTransGTE
- RetailTransactionMarkupTrans
- RetailTransactionPaymentTrans
- RetailTransactionAttributeTrans


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
