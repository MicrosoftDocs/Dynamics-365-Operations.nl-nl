---
title: Onkostentypen instellen
description: In dit artikel wordt uitgelegd hoe u onkostentypen instelt in Activa leasen.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseExpenseTypeTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9978041059437d5d3556236c7ac02c00db93f933
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908033"
---
# <a name="set-up-expense-types"></a>Onkostentypen instellen

[!include [banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u onkostentypen instelt in Activa leasen. Kosten die niet in het betalingsschema worden vertegenwoordigd, worden *onkosten* genoemd. Voorbeelden van deze kosten zijn: onroerendgoedbelastingen, onderhoudskosten van algemene ruimten en verzekeringskosten.

## <a name="add-an-administrative-expense-type"></a>Een administratief onkostentype toevoegen

1. Ga naar **Activa leasen \> Instellingen \> Onkostentypen**.
2. Selecteer **Nieuw**.
3. Voer in de betreffende velden het nieuwe onkostentype en een omschrijving in.

## <a name="assign-accounts-to-administrative-costs"></a>Rekeningen toewijzen aan administratieve kosten

Vervolgens koppelt u rekeningen aan de onkostentypen. Deze rekeningen worden gedebiteerd wanneer er onkostenschemaposten worden geboekt. De tegenrekening wordt opgegeven op de regels **Betalingschema voor administratieve kosten** van elke lease.

1. Ga naar **Activa leasen \> Instellingen \> Parameters voor activa leasen**.
2. Selecteer het onkostentype op het tabblad **Rekeningen**, op het sneltabblad **Administratieve kosten**, in het veld **Onkosten type**.
3. Selecteer **Toevoegen**.
4. Selecteer in het veld **Boektype** het boektype dat u wilt koppelen aan de administratieve kosten.

    > [!NOTE]
    > U kunt meerdere boektypen aan dezelfde onkostenrekening koppelen.

5. Geef in het veld **Rekeningcode** op voor welke leases u het boek wilt toepassen:

    - **Alle**: pas het boek toe op alle leases.
    - **Groep**: pas het boek toe op een specifieke groep leases.
    - **Tabel**: pas het boek toe op specifieke leases.

6. Als u **Groep** of **Tabel** hebt geselecteerd in het veld **Rekeningcode**, selecteert u een rekeningnummer of groepnummer in het veld **Rekening-/groepnummer**.
7. Selecteer in de desbetreffende velden de hoofdrekening voor financiële leases en de hoofdrekening voor operationele leases.

Wanneer u deze stappen hebt voltooid, kunt u onkosten toevoegen via de regels **Betalingsschema voor administratieve kosten** op de pagina **Leasedetails** van een geselecteerde lease. U kunt ook onkosten toevoegen wanneer u een nieuwe lease maakt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
