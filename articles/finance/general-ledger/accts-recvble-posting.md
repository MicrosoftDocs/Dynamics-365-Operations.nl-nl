---
title: Boeken in Klanten
description: In dit artikel wordt uitgelegd hoe boekingen worden geconfigureerd in Klanten met voorbeelden van boekingsconfiguraties.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustPaymMode, CustCashDiscount, CommissionPosting, MarkupTable\_Cust, CustPaymFee
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d679595a1f702c4e3ade138a87c817d245fcf79
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324324"
---
# <a name="accounts-receivable-posting"></a>Boeken voor Klanten

[!include [banner](../includes/banner.md)]

Het primaire boekingsprofiel voor de module **Klanten** is het boekingsprofiel van de klant. Dit boekingsprofiel bepaalt welke overzichtsrekening wordt gebruikt wanneer klantsaldi naar het grootboek worden geboekt. Een overzichtsrekening is een hoofdrekening. Dit wordt ook wel de handelsrekening voor Klanten genoemd.

Het rapport **Afstemming van klant met grootboek** kan na het boeken worden gebruikt om de saldi van klant- en grootboekrekeningen beter af te stemmen. Het rapport gebruikt de informatie die is gevonden in de overzichtsrekening voor het boekingsprofiel van de klant. De overzichtsrekening van de boekhouding die voor het document is gemaakt, wordt niet gebruikt. Als u wijzigingen aanbrengt in het klantboekingsprofiel of de klantengroep die aan de klant is toegewezen nadat u transacties hebt geboekt, kan het rapport verschillen weergeven tussen het saldo van de klant en grootboekrekening. Als u alleen de regels met verschillen wilt weergeven en de regels waarvoor de klant- en grootboekrekening beide nul zijn, selecteert u de parameter **Alleen verschillen** wanneer u het rapport afdrukt.

Zie [Boekingsprofielen van klant](../accounts-receivable/customer-posting-profiles.md) voor meer informatie.

Er zijn verschillende boekingsconfiguraties naast het boekingsprofiel van de klant beschikbaar in Klanten. De volgende secties bevatten meer informatie over deze andere configuraties.

## <a name="posting-accounts-for-methods-of-payment"></a>Boekingsrekeningen voor betalingsmethoden

Betalingsmethoden bepalen hoe een betaling naar het grootboek wordt geboekt. Ze bepalen ook het gedrag van de betalingsuitvoer. Gewoonlijk wordt er één betalingsmethode gemaakt voor elk betalingstype dat uw organisatie accepteert (bijvoorbeeld contant, cheque, creditcard, geldorder en overboeking).

De velden in de sectie **Boeking** op het sneltabblad **Algemeen** bepalen hoe een betaling naar het grootboek wordt geboekt. U moet eerst een waarde selecteren in het veld **Rekeningtype**. Het rekeningtype dat u selecteert, bepaalt het gedrag van het veld **Betalingsrekening**. Het is raadzaam om **Bank** te selecteren in het veld **Rekeningtype** en vervolgens de bankrekening te selecteren in het veld **Betalingsrekening**. Het voordeel van deze aanpak is dat het systeem de betaling naar de Banksubadministratie boekt, dat afstemming en andere kasgerelateerde processen ondersteunt. In de volgende tabel ziet u een voorbeeld van de boekingsprofielconfiguratie als u de module **Contanten en bankbeheer** gebruikt.

| Boekingstype | Rekeningtype | Voorbeeld van hoofdrekeningnaam | Rekeningtype | Debet/Credit? | Vereffeningsrekening | Description |
|--------------|--------------|---------------------------|--------------|---------------|------------------|-------------|
| Bank | Bank | Bank van Contoso | Bankrekening die aan een activum is gekoppeld | Krediet | Nr. | Voer voor elke betalingsmethode de hoofdrekening in het veld **Betalingsrekening** in. |

Als u niet van plan bent Contanten en bankbeheer te gebruiken, selecteert u **Grootboek** in het veld **Rekeningtype** en selecteert u vervolgens de hoofdrekening in het veld **Betalingsrekening**. In de volgende tabel ziet u een voorbeeld van de boekingsprofielconfiguratie als u de module Contanten en bankbeheer niet gebruikt.

| Boekingstype | Rekeningtype | Voorbeeld van hoofdrekeningnaam | Rekeningtype | Debet/Credit? | Vereffeningsrekening | Description |
|--------------|--------------|---------------------------|--------------|---------------|------------------|-------------|
| Ledger | Ledger | 100100: Bank van Contoso | Activum | Krediet | Nr. | Voer voor elke betalingsmethode de hoofdrekening in het veld **Betalingsrekening** in. |

## <a name="bridging-accounts"></a>Overbruggingsrekeningen

Overbruggingsboeking is een proces met twee stappen dat wordt gebruikt wanneer betalingen worden geboekt. Dit is een optionele functie die bijvoorbeeld kan worden gebruikt bij bankrekeningen met een nulsaldo. Dit bevordert een probleemloos en snel bankafstemmingsproces. In de eerste stap wordt een betaling geboekt naar een tijdelijke rekening (de overbruggingsrekening). In de tweede stap wordt de geboekte post omgekeerd en geboekt naar de bankrekening wanneer de betaling door de bank wordt verwerkt. In de volgende tabel ziet u een voorbeeld van de boekingsprofielconfiguratie voor overbruggingsboekingen.

| Boekingstype | Voorbeeld van hoofdrekening | Voorbeeld van hoofdrekeningnaam | Rekeningtype | Debet/Credit? | Vereffeningsrekening | Description |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Grootboekjournaal | 130725 | Niet-verrekend bedrag | Aansprakelijkheid | Debet | Ja | Voer voor elke betalingsmethode de hoofdrekening in het veld **Overbruggingsrekening** in. |

Zie [Overbruggingsbetalingen instellen en verwerken](../accounts-receivable/set-up-and-process-bridged-payments.md) voor meer informatie.

## <a name="posting-accounts-for-customer-cash-discounts"></a>Boekingsrekeningen voor contantkortingen van klant

Als uw organisatie contantkortingen aanbiedt aan klanten in ruil voor snelle betaling, moet u contantkortingscodes configureren en opgeven hoe de kortingen naar het grootboek moeten worden geboekt. Er zijn verschillende opties beschikbaar voor het opgeven van de hoofdrekening die wordt gebruikt om een contantkorting voor klanten te boeken.

Zie [Contantkortingen](../cash-bank-management/cash-discounts.md) voor meer informatie.

## <a name="posting-accounts-for-payment-fees"></a>Boekingsrekeningen voor betalingskosten

Met betalingskosten kunt u automatisch kosten toevoegen aan een klantbetaling wanneer een set voorwaarden van toepassing is. Betalingskosten kunnen bij de klant in rekening worden gebracht of kunnen als onkosten naar uw bankrekening worden geboekt. Hieronder volgen een aantal voorbeelden:

- U brengt 3 procent van het betalingstotaal bij klanten in rekening als ze met een creditcard betalen.
- Uw bank brengt $1,00 in rekening voor elke overboeking die u verwerkt, en de kosten van de overboeking worden als onkosten betaald.

Wanneer u klantbetalingskosten configureert en het veld **Toeslag** instelt op **Klant**, is het veld **Hoofdrekening** niet beschikbaar en wordt het boekingsprofiel van de klant gebruikt om de kosten te boeken. Als u het veld **Toeslag** instelt op **Grootboek**, moet u het veld **Hoofdrekening** instellen op de hoofdrekening waar de betalingskosten worden geboekt. Deze hoofdrekening is doorgaans een onkostenrekening. In de volgende tabel ziet u een voorbeeld van de boekingsprofielconfiguratie voor boekingen van betalingskosten.

| Boekingstype | Voorbeeld van hoofdrekening | Voorbeeld van hoofdrekeningnaam | Rekeningtype | Debet/Credit? | Vereffeningsrekening | Description |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Grootboekjournaal | 618190 | Bankkosten | Onkosten | Debet | Nee |  Als **Grootboek** is geselecteerd in het veld **Toeslag**, selecteert u deze rekening in het veld **Hoofdrekening** voor de betalingskosten. |

Zie [Betalingskosten van klant vaststellen](../accounts-receivable/tasks/establish-customer-payment-fees.md) voor meer informatie.

## <a name="posting-accounts-for-charges-codes"></a>Boekingsrekeningen voor toeslagcodes

Als u verkoopbedragen moet bijhouden naast regelartikelen, kunt u toeslagcodes gebruiken. U kunt bijvoorbeeld vracht- en verwerkingskosten bij uw klanten in rekening brengen of de kosten van bepaalde vracht- en verwerkingskosten intern verrekenen. U kunt opgeven of deze bedragen worden geboekt naar kostenrekeningen of toegevoegd aan de kosten van de artikelen.

U kunt toeslagcodes maken voor Klanten en Leveranciers. Wanneer u een toeslagencode configureert, moet u de boeking definiëren. De boeking controleert zowel de debetrekening als de creditrekening. Voor elke toeslagcode die u maakt, kunt u het boekingstype selecteren dat wordt gebruikt. In de volgende tabel ziet u typische voorbeelden van toeslagcodes voor Klanten.

| Boekingstype | Voorbeeld van hoofdrekening | Voorbeeld van hoofdrekeningnaam | Rekeningtype | Debet/Credit? | Vereffeningsrekening | Description |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Bijzondere betalingskosten | 411400 | Omzet – kosten | Omzet | Krediet | Nr. | **Voorbeeld voor ontoereikend saldo:** debet klant/leverancier en credit grootboekrekening |
| Order, vracht | 403500 | Omzet – vrachtkosten | Omzet | Krediet | Nr. | **Voorbeeld voor vrachtkosten die bij een klant in rekening worden gebracht:** debet klant/leverancier en credit grootboekrekening |
| Korting\* | 403200 | Korting | Omzet | Debet | Nr. | **Voorbeeld voor een klantkorting:** debet grootboekrekening en credit klant/leverancier |

\*In het kortingsvoorbeeld wordt de boeking alleen gebruikt wanneer een toeslagencode wordt toegevoegd aan de koptekst of regel van een inkooporder. De geavanceerde kortingsfunctionaliteit die beschikbaar is in Microsoft Dynamics 365 Supply Chain Management, biedt meer controle en geautomatiseerde kortingen. Zie [Klantkortingen](../../supply-chain/sales-marketing/tasks/process-customer-rebates.md) voor meer informatie.

In de voorgaande tabel staan drie voorbeelden van boekingstypen die voor toeslagcodes kunnen worden gebruikt. Gebruik dit als richtlijn en een voorbeeld. Het biedt geen uitgebreide lijst met alle mogelijke combinaties of boekingstypen die kunnen worden gebruikt.

Zie voor meer informatie over redencodes [Toeslagencode maken](../accounts-receivable/create-charges-codes.md).

## <a name="posting-accounts-for-commissions"></a>Boekingsrekeningen voor provisies

U kunt het systeem optioneel configureren om provisies te berekenen voor een verkoopmedewerker of een groep verkoopmedewerkers op een bepaalde verkooporder. Als u deze functionaliteit inschakelt, moet u de boekingsrekening configureren die wordt gebruikt om de provisie te berekenen. Deze configuratie vindt plaats op de pagina **Provisie boeken** in de module **Verkoop en marketing**.

Zie [Regels voor verkoopprovisie instellen](../../supply-chain/sales-marketing/tasks/set-up-sales-commission-rules.md) voor meer informatie.
