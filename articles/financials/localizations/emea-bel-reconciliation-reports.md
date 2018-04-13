---
title: "Afstemmingsrapporten voor België"
description: In dit onderwerp worden de standaardrapporten beschreven die Microsoft Dynamics 365 for Finance and Operations biedt om u te helpen bij de INTERVAT-belastingaangifte en afstemmingsanalyse.
author: ShylaThompson
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxReportExtraFieldsBE
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 273103
ms.search.region: Belgium
ms.author: shylaw
ms.dyn365.ops.version: AX 7.0.1
ms.search.validFrom: 2016-05-31
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: b6268775c707a777a8391bcb41b061c1635b8942
ms.contentlocale: nl-nl
ms.lasthandoff: 03/26/2018

---

# <a name="reconciliation-reports-for-belgium"></a>Afstemmingsrapporten voor België

[!INCLUDE [banner](../includes/banner.md)]

In dit onderwerp worden de standaardrapporten beschreven die Microsoft Dynamics 365 for Finance and Operations biedt om u te helpen bij de INTERVAT-belastingaangifte en afstemmingsanalyse.

Op basis van de btw-posten voor geselecteerde perioden, combineert de Belgische periodieke btw-aangifte (belasting toegevoegde waarde) btw-bedragen in vakken (btw-aangiftecodes) door informatie op een bepaalde manier te sorteren, splitsen en totaliseren. Daarom zijn controlerapporten vereist, zodat de bedragen in de btw-aangifte in detail kunnen worden gecontroleerd. In de rest van dit onderwerp worden de rapporten beschreven die details bevatten van de gegevens in de btw-aangifte.

## <a name="sales-tax-correction"></a>Btw-correctie
Het rapport **Btw-correctie** biedt een afgedrukt overzicht van INTERVAT-belastingcorrecties. Het correctiebedrag wordt vermeld voor elk vereffeningsperiode en elk btw-vak. (Btw-vakken zijn velden die specifiek zijn voor België en worden gebruikt voor het groeperen van btw-bedragen in de btw-aangifte. U kunt deze vakken instellen in de tabel **Btw-aangiftecodes**.) Als u het rapport **Btw-correctie** wilt afdrukken, klikt u op **Btw** &gt; **Aangiften** &gt; **Btw** &gt; **Extra btw-aangiftevakken** en klikt u vervolgens op **Btw-correcties** &gt; **Afdrukken**.

## <a name="sales-tax-list---belgium"></a>Btw-lijst - België
Gebruik het rapport **Btw-lijst - België** om informatie te bekijken over geboekte btw. Het rapport bevat details over btw-code, naam, grootboekrekening, rekeningnaam, hoeveelheid, bedrag inclusief btw, oorsprong en btw-bedrag. De parameters voor dit rapport bieden u veel flexibiliteit. U kunt een zeer nauwkeurig rapport opvragen door de parameters boekstuk, datum of btw-code te selecteren. Gebruik een filter om rapportparameters in te stellen. Als u het rapport **Btw-lijst - België** wilt afdrukken, klikt u op **Btw** &gt; **Query's en rapporten** &gt; **Btw-aangiften** &gt; **Btw-lijst - België**.

## <a name="sales-tax-transactions---details--belgium"></a>Btw-transacties - Details - België
Gebruik het rapport **Btw-transacties - Details - België** om informatie weer te geven en af te drukken over geboekte btw-transacties voor een bepaalde periode en een specifiek bereik van btw-codes. De transacties worden opgesomd per btw-code. Voor elke transactie kunt u de klant of leverancier, het boekstuknummer, de rekening waarop het btw-basisbedrag (oorsprong) wordt geboekt, het bedrag waarover btw wordt berekend, het bedrag inclusief btw, het btw-bedrag, de btw-toeslag en de richting van de btw vermeld. De bedragen worden opgeteld voor elke btw-code. De bedragen voor de te ontvangen en te betalen btw worden opgeteld in een eindtotaal. Het rapport bevat ook btw-codes met andere btw-richtingen, zoals gebruiksbelasting. Als u het rapport **Btw-transacties - Details - België** wilt afdrukken, klikt u op **Btw** &gt; **Query's en rapporten** &gt; **Btw-aangiften** &gt; **Btw-transacties - Details - België**.

## <a name="sales-tax-transactions-re-sales"></a>Btw-transacties wederverkoop
U kunt het rapport **Btw-transacties wederverkoop** gebruiken voor het ophalen van wederverkoopgegevens voor de transactie die specifiek zijn voor België. Deze informatie omvat relevante details, zoals journaal, boekstuk, datum, klantrekening, naam, bedrag en btw-aangiftecodes. Dit rapport wordt gemaakt op btw-vrijstellingsnummer, ondernemingsnummer en periode. Accountmanagers en boekhouders genereren dit rapport periodiek of wanneer dit is vereist. **Opmerking:** het aantal vakken moet dynamisch worden toegevoegd op basis van het boeken van inkopen. Als u het rapport **Btw-transacties wederverkoop** wilt afdrukken, klikt u op **Btw** &gt; **Query's en rapporten** &gt; **Btw-aangiften** &gt; **Btw-transacties wederverkoop**.

## <a name="sales-tax-transactions---belgium"></a>Btw-transacties - België
Het rapport **Btw-transacties - België** geeft de Belgische btw-transacties weer die zijn geboekt. Het rapport bevat gegevens over datum, boekstuk, btw-code, naam, bron, factuur, bedrag, netto btw-bedrag in de bedrijfsvaluta, netto btw-bedrag in de boekstukvaluta en boekstukvaluta. U kunt het rapport sorteren op boekstuk, datum, boekstukvaluta, btw-code en bron. De velden **Boekstuk**, **Btw-code** en **Boekstukvaluta** bevatten detailanalyse. De parameters voor dit rapport bieden u veel flexibiliteit. U kunt een zeer nauwkeurig rapport opvragen door de parameters boekstuk, datum of btw-code te selecteren. Gebruik een filter om rapportparameters in te stellen. Als u het rapport **Btw-transacties België** wilt afdrukken, klikt u op **Btw** &gt; **Query's en rapporten** &gt; **Btw-aangiften** &gt; **Btw-transacties - België**.

## <a name="sales-tax-by-customer---belgium"></a>Btw per klant - België
Controlerapporten zijn vereist, zodat de bedragen in de btw-aangifte in detail kunnen worden gecontroleerd voor een klant. Voor elke klantrekening en btw-code kunnen de volgende gegevens worden afgedrukt:

-   Klantrekeningnummer
-   Btw-code
-   Bedrag inclusief btw
-   Oorsprong
-   Btw-bedrag
-   Totaal per klantrekening
-   Eindtotaal voor alle klantenrekeningen

Dit rapport kan als volgt worden gegenereerd:

-   Voor één klantrekening of voor alle klantrekeningen
-   Voor één btw-code of voor alle btw-codes
-   Voor één specifieke datum of voor een reeks datums

De parameters voor dit rapport bieden u veel flexibiliteit. U kunt een zeer nauwkeurig rapport opvragen door de parameters klantrekening, datum of btw-code te selecteren. Gebruik een filter om rapportparameters nauwkeuriger in te stellen. Als u het rapport **Btw** **per klant - België** wilt afdrukken, klikt u op **Btw** &gt; **Query's en rapporten** &gt; **Btw-aangiften** &gt; **Btw** **per klant - België**.

## <a name="sales-tax-by-vendor---belgium"></a>Btw per leverancier - België
Controlerapporten zijn vereist, zodat de bedragen in de btw-aangifte in detail kunnen worden gecontroleerd voor een leverancier. Voor elke leveranciersrekening en btw-code kunnen de volgende gegevens worden afgedrukt:

-   Nummer leveranciersrekening
-   Btw-code
-   Bedrag inclusief btw
-   Oorsprong
-   Btw-bedrag
-   Totaal per leveranciersrekening
-   Eindtotaal voor alle leveranciersrekeningen

Dit rapport kan als volgt worden gegenereerd:

-   Voor één leveranciersrekening of voor alle leveranciersrekeningen
-   Voor één btw-code of voor alle btw-codes
-   Voor één specifieke datum of voor een reeks datums

De parameters voor dit rapport bieden u veel flexibiliteit. U kunt een zeer nauwkeurig rapport opvragen door de parameters leveranciersrekening, datum of btw-code te selecteren. Gebruik een filter om rapportparameters nauwkeuriger in te stellen. Als u het rapport **Btw** **per leverancier - België** wilt afdrukken, klikt u op **Btw** &gt; **Query's en rapporten** &gt; **Btw-aangiften** &gt; **Btw** **per leverancier - België**.

## <a name="purchase-sales-tax-transactions"></a>Btw-inkooptransacties
Het rapport **btw-transacties voor inkoop** bevat transacties met een inkoopheffing. De inkoopheffing wordt berekend en geboekt samen met btw-betalingen. Inkoopheffingen en btw worden beide aangegeven voor de vereffeningsperiode. De vereffeningsperiode wordt gedefinieerd per btw-dienst op de pagina **Btw-vereffeningsperioden**. De informatie in het koptekstdeel van het rapport bevat relevante gegevens zoals btw-nummer, ondernemingsnummer en periode. De informatie in de detailsectie omvat journaal, boekstuk, datum, leveranciersrekening, naam, bedrag inclusief btw en btw-aangiftecodes. Dit rapport is een extern rapport. De boekhouder of accountingmanager genereert en dient dit periodiek in bij de desbetreffende instanties. Als u het rapport **Btw-transacties voor inkoop** wilt afdrukken, klikt u op **Btw** &gt; **Query's en rapporten** &gt; **Btw-aangiften** &gt;  **Btw-transacties voor inkoop**.





