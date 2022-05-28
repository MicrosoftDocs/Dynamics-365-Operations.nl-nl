---
title: Een btw-betaling maken
description: De procedure voor de taak Btw vereffenen en boeken vereffent btw-saldi op de btw-rekeningen en tegenboekt ze naar de btw-vereffeningsrekening voor een bepaalde periode.
author: twheeloc
ms.date: 01/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c388a8f98cd4581abe2ec13d8922e232321e4039
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735931"
---
# <a name="create-a-sales-tax-payment"></a>Een btw-betaling maken

[!include [banner](../../includes/banner.md)]

De procedure voor de taak Btw vereffenen en boeken vereffent btw-saldi op de btw-rekeningen en tegenboekt ze naar de btw-vereffeningsrekening voor een bepaalde periode.

1. Ga naar **Belasting > Aangiften > Btw > Btw vereffenen en boeken**.
2. Selecteer in het veld **Vereffeningsperiode** de vervolgkeuzeknop om de zoekopdracht te openen.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Voer een datum in het veld **Begindatum** in. Als u de optie **Correcties opnemen** op de pagina **Grootboekparameters** niet selecteert, kan de vereffening voor verschillende versies worden verwerkt. **Oorspronkelijk** is de eerste vereffening voor een periode-interval en kan slechts eenmaal worden verwerkt voor een periode-interval. De laatste correcties vereffenen btw-transacties die zijn geboekt nadat de oorspronkelijke versie is gemaakt.
5. Voer in het veld **Transactiedatum** een datum in.
6. Selecteer **OK**. Het rapport **Btw-betalingen** wordt afgedrukt om de vereffende btw-transacties in de periode te controleren.

Vanaf versie 10.0.24 van Finance kunt u het rapport **Btw-betalingen** weglaten dat direct wordt gegenereerd nadat de periodieke procedure **Btw vereffenen en boeken** is geïmplementeerd onder de functie **Btw-betalingsrapport afzonderlijk genereren van btw-vereffening** in de werkruimte **Functiebeheer**.

Wanneer de functie is ingeschakeld, wordt er geen btw-betalingsrapport afgedrukt nadat het vereffeningsproces is voltooid. In plaats wordt het volgende bericht weergegeven: De btw-vereffening en -boeking zijn voltooid. Het boekstuk 'xxxx, m/d/yyy' is geboekt.

U kunt het btw-betalingsrapport nog handmatig uitvoeren via **Belasting** > **Query's en rapporten** > **Vragen over btw** > **Btw-betalingen**.

## <a name="performance-consideration"></a>Prestatieoverwegingen

De voltooiing van de btw-betalingsprocedure kan veel tijd in beslag nemen. De belangrijkste factoren die van invloed zijn op de prestaties van de procedure, zijn het aantal facturen in de vereffeningsperiode en het aantal vermeldingen dat moet worden geboekt in het btw-vereffeningsboekstuk. U kunt ervoor zorgen dat de prestaties worden verbeterd door bepaalde functionaliteit te omzeilen die niet vereist is in het proces.

### <a name="enable-the-sales-tax-payment-performance-improvement-feature"></a>De functie Prestatieverbetering van btw-betalingen inschakelen

Met de functie **Prestatieverbetering van btw-betalingen** kunnen de prestaties van de btw-betalingsprocedure worden verbeterd door op één regel het bedrag in de valuta van de boekhouding en het bedrag in de valuta van de aangifte op boekstukregels van btw-betaling samen te voegen met dezelfde hoofdrekening, grootboekdimensie en valuta.

1. Ga naar **Systeembeheer** \> **Werkruimten** \> **Functiebeheer**.
2. Zoek op het tabblad **Alle** naar **Prestatieverbeteringen voor btw-betalingen** en selecteer deze optie.
3. Selecteer **Inschakelen**.

### <a name="prevent-generation-of-offset-tax-transactions"></a>Genereren van tegengerekende btw-transacties voorkomen

Standaard boekt het boekstuk van de btw-betaling tegengerekende btw-transacties voor elke btw-transactie die wordt vereffend in de btw-betalingsprocedure. Deze tegengerekende btw-transacties worden opgenomen in het rapport **Afstemming btw/grootboek**. Ze laten het uitstaande saldo van de btw-transacties zien die niet zijn vereffend tijdens de periode.

De btw-tegenrekeningtransacties kunnen echter de last op de btw-betalingsprocedure verhogen. Daarom kan een flighting met de naam **TaxReportGenOffsetTaxTransPerRecordSetFlighting** op aanvraag worden geactiveerd. Deze flighting kan voor betere prestaties zorgen bij het genereren van tegenbelastingtransacties voor landen en regio's, behalve voor Thailand, Polen, Hongarije, Litouwen, Maleisië, India, Italië, Rusland, Tsjechische Republiek, Estland en Letland.

> [!NOTE]
> Als er aangepaste velden in de tabel voor belastingtransacties zijn, kan de flighting niet worden geactiveerd.

Omdat het rapport **Afstemming btw/grootboek** over het algemeen alleen wordt gebruikt voor interne controle en niet is vereist voor veel belastingregimes, kunt u ervoor kiezen om geen tegengerekende btw-transacties op het boekstuk van de btw-betaling te genereren.

1. Ga naar **Belasting** \> **Indirecte belastingen** \> **Btw** \> **Btw-vereffeningsperioden**.
2. Selecteer een vereffeningsperiode.
3. Stel op het sneltabblad **Algemeen** de optie **Genereren van tegengerekende btw-transacties voorkomen** in op **Ja**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
