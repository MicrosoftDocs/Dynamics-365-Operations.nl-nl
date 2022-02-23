---
title: Boeking van online verkopen en betalingen
description: Deze procedure doorloopt de configuratie en uitvoering van een terugkerende batchtaak om verkooporders en betalingen voor online winkeltransacties te maken.
author: psimolin
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3bac0cab764436a618fa570901c84ab720dbc86
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411419"
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
