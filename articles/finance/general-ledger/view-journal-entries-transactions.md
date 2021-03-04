---
title: Journaalboekingen en transacties weergeven
description: In dit artikel worden de verschillende manieren beschreven waarop u journaalposten en transacties kunt weergeven.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13031
ms.assetid: 281c7ea6-4dfd-4d1f-994f-c361ee299dbe
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 79329b60f0aa7ce196b55a1483b07f8b9ea7e3cf
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441965"
---
# <a name="view-journal-entries-and-transactions"></a>Journaalboekingen en transacties weergeven

[!include [banner](../includes/banner.md)]

In dit artikel worden de verschillende manieren beschreven waarop u journaalposten en transacties kunt weergeven. 

Gebruikers die journalen en transacties willen weergeven, hebben verschillende manieren om de gegevens te openen. Ze kunnen profiteren van querypagina's die inzoommogelijkheid bevatten of ze kunnen diverse rapportopties in het grootboek gebruiken.

## <a name="voucher-transactions"></a>Boekstuktransacties
**Boekstuktransacties** is een querypagina waar u een selectie kunt maken in verschillende tabellen en velden om criteria voor het saldo of de transactie op te geven waarnaar u zoekt. U kunt bijvoorbeeld alle transacties weergeven voor een bepaalde datum of account, maar u kunt ook alle transacties van het bewerkingstype **Bezig met uitvoeren** weergeven die zich in een bepaalde boekingslaag bevinden. Standaard worden op de pagina het journaalnummer, het boekstuk, de datum en de hoofdrekening weergegeven, maar u kunt aanvullende tabellen, velden en criteria toevoegen om uw zoekopdracht te beperken.

## <a name="audit-trail"></a>Audittrail
**Audittrail** is een querypagina die het volgende bevat: het type transacties, beschrijvingen, door wie de transacties zijn gemaakt en wanneer deze zijn gemaakt. Op de querypagina **Audittrail** kunt u de boekstuktransacties weergeven.

## <a name="financial-reports"></a>Financiële rapporten
U kunt ook grootboektransacties bekijken en analyseren door financiële rapporten uit te voeren. Omdat het ontwerp van financiële rapporten op rekeningen, dimensies, rekeningcategorieën of een combinatie van de drie kan worden gebaseerd, kunt u de transacties weergeven door op verschillende manieren in te zoomen. Als u meer gegevens voor grootboektransacties vereist, kunt u ook meerdere transactie-eigenschappen als onderdeel van het rapportontwerp opnemen. Als u bovendien de transacties wilt zien waaruit een grootboek bestaat, kunt u inzoomen op rekeningtransacties, net zoals u dat op de lijstpagina **Proefbalans** kunt doen.

## <a name="ledger-reports"></a>Grootboekrapporten
Naast de financiële rapporten kunt u de volgende grootboekrapporten gebruiken om grootboektransacties weer te geven:

-   **Dimensieoverzicht**: dit rapport bevat transacties per dag en rekening, en er zijn ook opties om transacties per dimensie en periode weer te geven.
-   **Lijst van grootboektransacties**: dit rapport bevat transacties in transactie-, boekhoudings- en aangiftevaluta voor een rekening.
-   **Journaal afdrukken:** Dit rapport bevat het resultaat van een geboekt journaal. U kunt het rapport uitvoeren op journaalbatchnummer of journaaltype of u kunt extra velden toevoegen.
-   **Geboekte transacties per journaal**: dit rapport bevat de transacties die naar een journaal zijn geboekt, gegroepeerd op boekstuk.
-   **Transactielijst per datum**: dit rapport bevat alle transacties op datum, samen met het journaalnummer, het boekstuk en de grootboekrekening. Ook bevat dit rapport de transacties in de transactie-, boekhoudings- en aangiftevaluta.
-   **Oorsprong van transactie**: in dit transactierapport wordt de rekening op journaal weergegeven en op basis van transactie-, boekhoudings- en aangiftevaluta. Ook bevat het rapport elke regel van het journaal dat als tegenrekening is gebruikt.


## <a name="additional-resources"></a>Aanvullende resources
- [Grootboekrekeningsaldi](general-ledger-account-balances.md) 
- [Bronverkenner voor boekhouding](../accounts-payable/accounting-source-explorer.md)
- [Overzicht van Financiële rapportage](financial-reporting-getting-started.md)
- [Journaalboekingen of transacties weergeven](tasks/view-journal-entries-or-transactions.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]