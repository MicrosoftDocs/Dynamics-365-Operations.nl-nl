---
title: Vooruitbetalingen door klanten
description: In dit artikel wordt uitgelegd hoe u vooruitbetalingen van klanten (ook wel klantdeposito's genoemd) kunt instellen en verwerken.
author: twheeloc
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, LedgerJournalTransCustPaym, CustParameters
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f085d45895530aaf0a16439f62dfc13b27da84b6
ms.sourcegitcommit: fb9b6969218f2b82f0a4c72bfad75387fe00395c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/22/2022
ms.locfileid: "9799428"
---
# <a name="customer-prepayments"></a>Vooruitbetalingen door klanten

[!include [banner](../includes/banner.md)]

Vooruitbetalingen van klanten worden gebruikt wanneer u een betaling ontvangt van een klant, maar er geen factuur is waarmee de betaling kan worden vereffend. Dit type betalingen wordt ook wel klantdeposito's of klantstortingen genoemd.

Het proces van het instellen en werken met vooruitbetalingen van klanten bestaat uit de volgende basisstappen.

1. Maak een klantboekingsprofiel voor vooruitbetalingen.
2. Stel de parameter **Boekingsprofiel met journaalboekstuk van vooruitbetaling** in.
3. Maak een klantbetalingsjournaal en schakel op elke regel het selectievakje **Journaalboekstuk van vooruitbetaling** in.
4. Boek het klantbetalingsjournaal.
5. Nadat een factuur is gegenereerd, vereffent u de vooruitbetaling met deze met de pagina **Openstaande transacties vereffenen**.

## <a name="create-a-customer-posting-profile-for-prepayments"></a>Een klantboekingsprofiel voor vooruitbetalingen maken

Doorgaans wilt u, wanneer u vooruitbetalingen of stortingen van uw klanten accepteert voordat goederen of services worden geleverd, of voordat er een factuur in het systeem bestaat, het contante geld registreren als een passivum in plaats van een activum in het rekeningschema. De vereisten voor het registreren van deze bedragen in uw grootboek kunnen echter verschillen, afhankelijk van uw land of regio. Raadpleeg daarom uw accountants over eventuele lokale regelgeving.

In het algemeen is het proces voor het maken van een boekingsprofiel dat kan worden gebruikt voor vooruitbetalingen hetzelfde als het proces voor het maken van andere boekingsprofielen. Het belangrijkste verschil is de hoofdrekening die u selecteert in het veld **Totaalrekening**. Zie [Boekingsprofielen van klant](customer-posting-profiles.md) voor meer informatie.

## <a name="define-parameters-for-customer-prepayments"></a>Parameters voor vooruitbetalingen van klanten definiëren

Er zijn twee belangrijke parameters voor klanten waar u rekening mee moet houden wanneer u het systeem voor vooruitbetalingen voor klanten configureert. Ga als volgt te werk om de parameters te configureren.

1. Ga naar **Klanten \> Instellen \> Parameters van module Klanten**.
2. Optioneel: stel op het tabblad **Grootboek en btw** op het sneltabblad **Betaling** de optie **BTW op journaalboekstuk van vooruitbetaling** in op **Ja**.
3. Selecteer in het veld **Boekingsprofiel met journaalboekstuk van vooruitbetaling** het klantboekingsprofiel dat moet worden gebruikt wanneer vooruitbetalingen van klanten worden geboekt.
4. Sluit de pagina.

## <a name="create-customer-prepayment-vouchers"></a>Journaalboekstukken van vooruitbetaling van klanten maken

Wanneer u het klantbetalingsjournaal maakt, moet u voor elke vooruitbetaling de optie **Journaalboekstuk van vooruitbetaling** instellen op **Ja** op de pagina **Journaal met betalingen van klant**. Volg deze stappen om een klantbetaling te maken.

1. Ga naar **Klanten \> Betalingen \> Journaal met betalingen van klant**.
2. Selecteer **Nieuw** om een journaal te maken.
3. Selecteer in het veld **Naam** de journaalnaam die u wilt gebruiken.

    > [!IMPORTANT]
    > Als u de optie **BTW op journaalboekstuk van vooruitbetaling** in de vorige procedure op **Ja** instelt, moet u een journaalnaam selecteren waarbij de parameter **Btw is inbegrepen in bedrag** is geselecteerd. 

4. Optioneel: voer in het veld **Omschrijving** een uitgebreide omschrijving in.
5. Selecteer **Regels**
6. Als er geen lege regel bestaat, selecteert u **Nieuw** om een regel te maken.
7. Voer in het veld **Datum** de datum in waarop de vooruitbetaling moet worden geboekt.
8. Selecteer in het veld **Rekening** de klant voor de vooruitbetaling.
9. Optioneel: voer in het veld **Omschrijving** een uitgebreide omschrijving van de transactie in.
10. Voer in het veld **Credit** het bedrag van de vooruitbetaling in.
11. Selecteer in het veld **Tegenrekening** de rekening waar de betaling mee moet worden verrekend. Selecteer bijvoorbeeld de bank of hoofdrekening waar u de betaling naar wilt boeken.
12. Selecteer in het veld **Betalingsmethode** de betalingsmethode van de klant.
13. Stel op het tabblad **Betaling** de optie **Journaalboekstuk van vooruitbetaling** in op **Ja**.
14. Herhaal stap 7 t/m 13 voor elke extra vooruitbetaling die moet worden geboekt.
15. Selecteer **Boeken** om het journaal te voltooien.

## <a name="settle-prepayments-with-invoices"></a>Vooruitbetalingen met facturen vereffenen

U kunt de werkruimte **Klantbetalingen** gebruiken om eenvoudig betalingen te vinden en te vereffenen die nog niet volledig zijn vereffend.

1. Selecteer in het dashboard **Start** de tegel **Klantbetalingen**.
2. Zoek in de sectie **Klanttransacties** op het tabblad **Betalingen niet vereffend** naar de te vereffenen betaling en selecteer deze.
3. Selecteer **Transacties vereffenen**.
4. Schakel het selectievakje **Markeren** in voor de factuur en de betaling die wordt vereffend.
5. Selecteer **Boeken**.

Zie [Vereffeningsoverzicht](/dynamics365/finance/cash-bank-management/settlement-overview) voor meer informatie over het vereffenen van openstaande transacties.
