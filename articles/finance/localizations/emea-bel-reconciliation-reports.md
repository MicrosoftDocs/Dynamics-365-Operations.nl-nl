---
title: Afstemmingsrapporten voor België
description: In dit onderwerp worden de standaardrapporten beschreven die Microsoft Dynamics 365 Finance biedt om u te helpen bij de INTERVAT-belastingaangifte en afstemmingsanalyse.
author: anasyash
manager: AnnBe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxReportExtraFieldsBE
audience: Application User
ms.reviewer: kfend
ms.custom: 273103
ms.search.region: Belgium
ms.author: roschlom
ms.dyn365.ops.version: AX 7.0.1
ms.search.validFrom: 2016-05-31
ms.openlocfilehash: 8958185ce13cad773f22239c74962ede142659eb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988330"
---
# <a name="reconciliation-reports-for-belgium"></a>Afstemmingsrapporten voor België

[!include [banner](../includes/banner.md)]

Dynamics 365 Finance omvat diverse speciaal gebouwde toepassingen die u helpen bij het beheren van specifieke bedrijfsfuncties. Zie [Dynamics 365-licentiehandleiding](https://go.microsoft.com/fwlink/?LinkId=866544) voor meer informatie over deze licentiewijzigingen.

In dit onderwerp worden de standaardrapporten beschreven die u helpen bij de INTERVAT-belastingaangifte en afstemmingsanalyse.

Op basis van de btw-posten voor geselecteerde perioden, combineert de Belgische periodieke btw-aangifte (belasting toegevoegde waarde) btw-bedragen in vakken (btw-aangiftecodes) door informatie op een bepaalde manier te sorteren, splitsen en totaliseren. Daarom zijn controlerapporten vereist, zodat de bedragen in de btw-aangifte in detail kunnen worden gecontroleerd. In de rest van dit onderwerp worden de rapporten beschreven die details bevatten van de gegevens in de btw-aangifte.

Schermafbeeldingen die in dit onderwerp worden weergegeven, bevatten gegevens op basis van transacties uit een voorbeeld in het onderwerp [INTERVAT-belastingaangifte](emea-bel-intervat-tax-declaration.md).


## <a name="sales-tax-correction"></a>Btw-correctie
Het rapport **Btw-correctie** biedt een afgedrukt overzicht van INTERVAT-belastingcorrecties. Het correctiebedrag wordt vermeld voor elk vereffeningsperiode en elk btw-vak. (Btw-vakken zijn velden die specifiek zijn voor België en worden gebruikt voor het groeperen van btw-bedragen in de btw-aangifte. U stelt deze vakken in in de tabel **Btw-aangiftecodes**.)

Als u het rapport **Btw-correctie** wilt afdrukken, gaat u naar **Belasting** \> **Aangiften** \> **Btw** \> **Aanvullende btw-rapportvakken** en klikt u op **Btw-correcties** \> **Afdrukken.**

![Gegenereerd rapport Btw-correcties](media/1_Sales_tax_corrections.png)

## <a name="sales-tax-list---belgium"></a>Btw-lijst - België
Gebruik het rapport **Btw-lijst - België** om informatie te bekijken over geboekte btw. Het rapport bevat details over btw-code, naam, grootboekrekening, rekeningnaam, hoeveelheid, bedrag inclusief btw, oorsprong en btw-bedrag. De parameters voor dit rapport bieden u veel flexibiliteit. U kunt een zeer nauwkeurig rapport opvragen door de parameters boekstuk, datum of btw-code te selecteren. Gebruik een filter om rapportparameters in te stellen.

Als u het rapport **Btw-lijst - België** wilt afdrukken, gaat u naar **Btw** \> **Query's en rapporten** \> **Btw-aangiften** \> **Btw-lijst - België**.

![Gegenereerd rapport Btw-lijst](media/2_Sales_tax_list.png)

## <a name="sales-tax-transactions---details--belgium"></a>Btw-transacties - Details - België
Gebruik het rapport **Btw-transacties - Details - België** om informatie weer te geven en af te drukken over geboekte btw-transacties voor een bepaalde periode en een specifiek bereik van btw-codes. De transacties worden opgesomd per btw-code. Voor elke transactie kunt u de klant of leverancier, het boekstuknummer, de rekening waarop het btw-basisbedrag (oorsprong) wordt geboekt, het bedrag waarover btw wordt berekend, het bedrag inclusief btw, het btw-bedrag, de btw-toeslag en de richting van de btw vermeld. De bedragen worden opgeteld voor elke btw-code. De bedragen voor de te ontvangen en te betalen btw worden opgeteld in een eindtotaal. Het rapport bevat ook btw-codes met andere btw-richtingen, zoals gebruiksbelasting.

Als u het rapport **Btw-transacties - Details - België** wilt afdrukken, gaat u naar **Btw** \> **Query's en rapporten** \> **Btw-aangiften** \> **Btw-transacties - Details - België**.

![Gegenereerd rapport Btw-transacties - Details - België](media/3_Sales_tax_transactions_details.png)

## <a name="sales-tax-transactions-re-sales"></a>Btw-transacties wederverkoop
U kunt het rapport **Btw-transacties wederverkoop** gebruiken voor het ophalen van wederverkoopgegevens voor de transactie die specifiek zijn voor België. Deze informatie omvat relevante details, zoals journaal, boekstuk, datum, klantrekening, naam, bedrag en btw-aangiftecodes. Dit rapport wordt gemaakt op btw-vrijstellingsnummer, ondernemingsnummer en periode. Accountmanagers en boekhouders genereren dit rapport periodiek of wanneer dit is vereist.

> [!NOTE]
> Opmerking: het aantal vakken moet dynamisch worden toegevoegd op basis van de boeking van inkopen.

Als u het rapport **Btw-transacties wederverkoop** wilt afdrukken, gaat u naar **Btw** \> **Query's en rapporten** \> **Btw-aangiften** \> **Btw-transacties wederverkoop**.

![Gegenereerd rapport Btw-transacties wederverkoop](media/4_Sales_tax_transactions_re_sales.png)


## <a name="sales-tax-transactions---belgium"></a>Btw-transacties - België

Het rapport **Btw-transacties - België** geeft de Belgische btw-transacties weer die zijn geboekt. Het rapport bevat gegevens over datum, boekstuk, btw-code, naam, bron, factuur, bedrag, netto btw-bedrag in de bedrijfsvaluta, netto btw-bedrag in de boekstukvaluta en boekstukvaluta.

U kunt het rapport sorteren op boekstuk, datum, boekstukvaluta, btw-code en bron. De velden **Boekstuk**, **Btw-code** en **Boekstukvaluta** bevatten detailanalyse. De parameters voor dit rapport bieden u veel flexibiliteit. U kunt een zeer nauwkeurig rapport opvragen door de parameters boekstuk, datum of btw-code te selecteren. Gebruik een filter om rapportparameters in te stellen.

Als u het rapport **Btw-transacties België** wilt afdrukken, gaat u naar **Btw** \> **Query's en rapporten** \> **Btw-aangiften** \> **Btw-transacties - België**.

![Gegenereerd rapport Btw-transacties](media/5_Sales_tax_transactions.png)

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

De parameters voor dit rapport bieden u veel flexibiliteit. U kunt een zeer nauwkeurig rapport opvragen door de parameters klantrekening, datum of btw-code te selecteren. Gebruik een filter om rapportparameters nauwkeuriger in te stellen.  Als u het rapport **Btw** **per klant - België** wilt afdrukken, klikt u op **Btw** &gt; **Query's en rapporten** &gt; **Btw-aangiften** &gt; **Btw** **per klant - België**.

![Belgisch gegenereerd rapport Btw per klant](media/6_Sales_tax_by_customer.png)

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

![Belgisch gegenereerd rapport Btw per leverancier](media/7_Sales_tax_by_vendor.png)

## <a name="purchase-sales-tax-transactions"></a>Btw-inkooptransacties
Het rapport **btw-transacties voor inkoop** bevat transacties met een inkoopheffing. De inkoopheffing wordt berekend en geboekt samen met btw-betalingen. Inkoopheffingen en btw worden beide aangegeven voor de vereffeningsperiode. De vereffeningsperiode wordt gedefinieerd per btw-dienst op de pagina **Btw-vereffeningsperioden**. De informatie in het koptekstdeel van het rapport bevat relevante gegevens zoals btw-nummer, ondernemingsnummer en periode. De informatie in de detailsectie omvat journaal, boekstuk, datum, leveranciersrekening, naam, bedrag inclusief btw en btw-aangiftecodes. Dit rapport is een extern rapport. De boekhouder of accountingmanager genereert en dient dit periodiek in bij de desbetreffende instanties. Als u het rapport **Btw-transacties voor inkoop** wilt afdrukken, klikt u op **Btw** &gt; **Query's en rapporten** &gt; **Btw-aangiften** &gt;**Btw-transacties voor inkoop**.

![Gegenereerd rapport Btw-inkooptransacties](media/8_Purchase_sales_tax_transactions.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]