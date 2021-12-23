---
title: Btw-gegevens afdrukken op transferorderdocumenten
description: In dit onderwerp wordt uitgelegd hoe de belastinggegevens die worden bepaald door de btw-berekeningsservice, kunnen worden afgedrukt op transferorderdocumenten.
author: Kai-Cloud
ms.date: 10/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-10-12
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 174cbd85139db5cee75481041fb721dc7646ab66
ms.sourcegitcommit: eef5d9935ccd1e20e69a1d5b773956aeba4a46bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/11/2021
ms.locfileid: "7913597"
---
# <a name="print-tax-information-on-transfer-order-documents"></a>Btw-gegevens afdrukken op transferorderdocumenten

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u btw-gegevens op transferorderdocumenten afdrukt. U kunt het pro-forma factuurdocument afdrukken van een transferorder voor voorraadoverboekingen die worden beschouwd als intracommunautaire levering en intracommunautaire verwervingen onder de btw-regelgeving van de Europese Unie. 

Aan de transferorderdocumenten worden de volgende gegevens die relevant zijn voor de belasting, toegevoegd:

- De namen en de verzend- en doeladressen voor de voorraadoverdracht
- De belastingidentificatienummers van de leverancier en de ontvanger
- De eenheidsprijs en het belastbare bedrag van de geleverde goederen
- De btw-code, het btw-tarief, het btw-bedrag en de btw-richtlijnen

Om deze gegevens te configureren, moet u de volgende hoofdstappen voltooien.

1. [De btw-functie voor transferorders inschakelen en instellen](tasks/Tax-feature-support-for-transfer-order.md).
2. [Meerdere belastingregistratienummers maken en instellen voor een rechtspersoon](emea-multiple-vat-registration-numbers.md).
3. Stel de vrijstellingscode, omschrijving, belastingrichtlijnen en afdrukcode in btw-codes in. Voor dit voorbeeld worden drie belastingcodes gemaakt en gesynchroniseerd in Microsoft Dynamics 365 Finance: **NL-Vrijgesteld**, **BE-RC-21** en **BE-RC+21**.

    1. Ga in Finance naar **Belasting** \> **Instellingen** \> **Btw** \> **Btw-vrijstellingscodes**.
    2. Selecteer **Bewerken** en voer een omschrijving in voor de **EC**-vrijstellingscode. Voer bijvoorbeeld **Belastingvrije EC-zendingen met btw-registratienummer** in.
    3. Ga naar **Belasting** \> **Indirecte belastingen** \> **Btw** \> **Btw-codes**.
    4. Selecteer de **BE-RC-21**-btw-code en selecteer vervolgens **Btw-richtlijnen**.
    5. Selecteer **Nieuw**.
    6. Selecteer in het veld **Taal** de waarde **EN-US**. Voer vervolgens in het veld **Tekst** **Document voor de transfer van goederen in de zin van artikel 138. 2. c) van EU VAT Directive 2006/112/EC** in.
    7. Sluit de pagina.
    8. Selecteer op het sneltabblad **Algemeen** in het veld **Afdrukken** **Btw-tarief**.
    8. Selecteer de btw-code **NL-vrijstelling** en vervolgens op het sneltabblad **Algemeen** in het veld **Afdrukken** **Btw-tarief**.

    > [!NOTE] 
    > De btw-code, het btw-tarief en de btw-vrijstellingsomschrijving worden niet afgedrukt op transferorderdocumenten als er geen omschrijving van de vrijstellingscode of btw-richtlijnen voor de btw-code worden onderhouden.

## <a name="print-the-transfer-order---shipment-document"></a>Transferorder - verzendingsdocument afdrukken

Nadat een transfer is verzonden, volgt u deze stappen om het document transferorder - zending af te drukken.

1. Ga naar **Voorraadbeheer** \> **Query's en rapporten** \> **Overboekingsorders** \> **Zending**.
2. Schakel op het tabblad **Parameters** in de groep **Afdrukken** **Btw-gegevens** in.
3. Selecteer op het tabblad **Op te nemen records** de optie **Filter**, selecteer het transferordernummer en vervolgens **OK**.
4. Selecteer **OK** om het document transferorder - zending af te drukken.

## <a name="print-the-transfer-order---receipt-document"></a>Transferorder - ontvangstdocument afdrukken

Nadat een transfer is ontvangen, volgt u deze stappen om het document transferorder - ontvangst af te drukken.

1. Ga naar **Voorraadbeheer** \> **Query's en rapporten** \> **Overboekingsorders** \> **Ontvangen**.
2. Schakel op het tabblad **Parameters** in de groep **Afdrukken** **Btw-gegevens** in.
3. Selecteer op het tabblad **Op te nemen records** de optie **Filter**, selecteer het transferordernummer en selecteer vervolgens **OK**.
4. Selecteer **OK** om het document transferorder - ontvangst af te drukken.

## <a name="print-the-transfer-overview-document"></a>Het overzichtsdocument voor de overdracht afdrukken

Volg deze stappen om het overzichtsdocument voor de overdracht af te drukken.

> [!NOTE]
> Btw-gegevens zijn alleen beschikbaar wanneer de transferorder is verzonden of ontvangen.

1. Ga naar **Voorraadbeheer** \> **Query's en rapporten** \> **Overboekingsorders** \> **Overzicht van transfers**.
2. Schakel op het tabblad **Parameters** in de groep **Afdrukken** **Btw-gegevens** in.
3. Selecteer op het tabblad **Op te nemen records** de optie **Filter**, selecteer het transferordernummer en selecteer vervolgens **OK**.
4. Selecteer **OK** om het document overzicht van transfers af te drukken.

[!INCLUDE [footer-include](../../includes/footer-banner.md)]
