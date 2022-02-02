---
title: Boekingen voor Leveranciers
description: In dit onderwerp wordt uitgelegd hoe boekingen worden geconfigureerd in Leveranciers met voorbeelden van boekingsconfiguraties.
author: rachel-profitt
ms.date: 01/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendPosting, VendPaymMode, VendCashDiscount, MarkupTable\_Vend, VendPaymFee
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb3ebad31c9f41e405b9fc31a0f71df05fa1cc60
ms.sourcegitcommit: 10b85a09e8a550155a69aa2a8877a7c88b887242
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/20/2022
ms.locfileid: "8014451"
---
# <a name="accounts-payable-posting"></a>Boeken voor Leveranciers

[!include [banner](../includes/banner.md)]

Het primaire boekingsprofiel voor de module **Leveranciers** is het boekingsprofiel van de leverancier. Dit boekingsprofiel bepaalt welke overzichtsrekening wordt gebruikt wanneer leveranciersaldi naar het grootboek worden geboekt. Een overzichtsrekening is een hoofdrekening. Dit wordt ook wel de handelsrekening voor Leveranciers genoemd.

Zie [Boekingsprofielen van leveranciers](../accounts-payable/vendor-posting-profiles.md) voor meer informatie.

Er zijn verschillende boekingsconfiguraties naast het boekingsprofiel van de leverancier beschikbaar in Leveranciers. De volgende secties bevatten meer informatie over deze andere configuraties.

## <a name="methods-of-payment-posting-accounts"></a>Betalingsmethoden voor boekingsrekeningen

Betalingsmethoden bepalen hoe een betaling naar het grootboek wordt geboekt. Ze bepalen ook het gedrag van de betalingsuitvoer. Gewoonlijk wordt er één betalingsmethode gemaakt voor elk type betaling dat uw organisatie doet (bijvoorbeeld contant, cheque, creditcard, geldorder en creditcard).

De velden in de sectie **Boeking** op het sneltabblad **Algemeen** op de pagina **Betalingsmethoden** (**Leveranciers > Betalingsinstellingen > Betalingsmethoden**) bepalen hoe een betaling naar het grootboek wordt geboekt. U moet eerst een waarde selecteren in het veld **Rekeningtype**. Het rekeningtype dat u selecteert, bepaalt het gedrag van het veld **Betalingsrekening**. Het is raadzaam om **Bank** te selecteren in het veld **Rekeningtype** en vervolgens de bankrekening te selecteren in het veld **Betalingsrekening**. Het voordeel van deze aanpak is dat het systeem de betaling naar de Banksubadministratie boekt, dat afstemming en andere kasgerelateerde processen ondersteunt. In de volgende tabel ziet u een voorbeeld van de boekingsprofielconfiguratie als u de module **Contanten en bankbeheer** gebruikt.

| Boekingstype | Rekeningtype | Voorbeeld van naam van betalingsrekening | Rekeningtype | Debet/Credit? | Vereffeningsrekening | Description |
|--------------|--------------|------------------------------|--------------|---------------|------------------|-------------|
| Bank | Bank | Bank of America | Bankrekening die aan een activum is gekoppeld | Debet | Nee | Voer voor elke betalingsmethode de hoofdrekening in het veld **Betalingsrekening** in. |

Als u niet van plan bent Contanten en bankbeheer te gebruiken, selecteert u **Grootboek** in het veld **Rekeningtype** en vervolgens de hoofdrekening selecteren in het veld **Betalingsrekening**. In de volgende tabel ziet u een voorbeeld van de boekingsprofielconfiguratie als u de module Contanten en bankbeheer **niet** gebruikt.

| Boekingstype | Rekeningtype |Voorbeeld van betalingsrekening | Rekeningtype | Debet/Credit? | Vereffeningsrekening | Description |
|--------------|--------------|------------------------|--------------|---------------|------------------|-------------|
| Ledger | Ledger | 100100: Bank of America | Activum | Debet | Nee | Voer voor elke betalingsmethode de hoofdrekening in het veld **Betalingsrekening** in. |

## <a name="bridging-accounts"></a>Overbruggingsrekeningen

Overbruggingsboeking is een proces met twee stappen dat wordt gebruikt wanneer betalingen worden geboekt. Dit is een optionele functie die bijvoorbeeld kan worden gebruikt bij bankrekeningen met een nulsaldo. Dit bevordert een probleemloos en snel bankafstemmingsproces. In de eerste stap wordt een betaling geboekt naar een tijdelijke rekening (de overbruggingsrekening). In de tweede stap wordt de geboekte post omgekeerd en geboekt naar de bankrekening wanneer de betaling door de bank wordt verwerkt. In de volgende tabel ziet u een voorbeeld van de boekingsprofielconfiguratie voor overbruggingsboekingen.

| Boekingstype | Voorbeeld van hoofdrekening | Voorbeeld van hoofdrekeningnaam | Rekeningtype | Debet/Credit? | Vereffeningsrekening | Description |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Grootboekjournaal | 130725 | Niet-verrekend bedrag | Aansprakelijkheid | Debet | Ja | Voer voor elke betalingsmethode de hoofdrekening in het veld **Overbruggingsrekening** in. |

Zie [Overbruggingsbetalingen instellen en verwerken](../accounts-receivable/set-up-and-process-bridged-payments.md) voor meer informatie.

## <a name="customer-cash-discounts-posting-accounts"></a>Boekingsrekeningen voor contantkortingen van klant

Als uw organisatie contantkortingen ontvangt van leveranciers in ruil voor snelle betaling, moet u contantkortingscodes configureren en opgeven hoe de kortingen naar het grootboek moeten worden geboekt. Er zijn verschillende opties beschikbaar voor het opgeven van de hoofdrekening die wordt gebruikt om een contantkorting voor klanten te boeken.

Zie [Contantkortingen](../cash-bank-management/cash-discounts.md) voor meer informatie.

## <a name="payment-fee-posting-accounts"></a>Boekingsrekeningen voor betalingskosten

Met betalingskosten kunt u automatisch kosten toevoegen aan een leveranciersbetaling wanneer een set voorwaarden van toepassing is. Betalingskosten kunnen worden betaald aan de leverancier of als onkosten naar uw bankrekening worden geboekt. Hieronder volgen een aantal voorbeelden:

- Een leverancier berekent een toeslag van 3 procent van het betalingstotaal als u betaalt met een creditcard.
- Uw bank brengt $1,00 in rekening voor elke overboeking die u verwerkt, en de kosten worden als onkosten betaald.

Wanneer u leverancierbetalingskosten configureert en het veld **Toeslagen** instelt op **Leverancier**, is het veld **Hoofdrekening** niet beschikbaar en wordt het boekingsprofiel van de leverancier gebruikt om de kosten te boeken. Als u het veld **Toeslag** instelt op **Grootboek**, moet u het veld **Hoofdrekening** instellen op de hoofdrekening waar de betalingskosten worden geboekt. Deze hoofdrekening is doorgaans een onkostenrekening. In de volgende tabel ziet u een voorbeeld van de boekingsprofielconfiguratie voor boekingen van betalingskosten.

| Boekingstype | Voorbeeld van hoofdrekening | Voorbeeld van hoofdrekeningnaam | Rekeningtype | Debet/Credit? | Vereffeningsrekening | Description |
|--------------|----------------------|---------------------------|--------------|----------------|------------------|-------------|
| Grootboekjournaal | 618190 | Bankkosten | Onkosten | Debet | Nee | Als **Grootboek** is geselecteerd in het veld **Toeslag**, selecteert u deze rekening in het veld **Hoofdrekening** op de pagina **Betalingskosten**. |

Zie [Bijzondere kosten voor leveranciersbetalingen definiëren](../accounts-payable/tasks/define-vendor-payment-fees.md) voor meer informatie.

## <a name="charges-code-posting-accounts"></a>Toeslagencode voor boekingsrekeningen

Als u inkoopbedragen wilt bijhouden naast regelartikelen, kunt u toeslagcodes gebruiken. Uw leverancier kan bijvoorbeeld vracht- en verwerkingskosten bij u in rekening brengen of de kosten van bepaalde vracht- en verwerkingskosten intern verrekenen. U kunt opgeven of deze bedragen worden geboekt naar kostenrekeningen of toegevoegd aan de kosten van de artikelen.

U kunt toeslagcodes maken voor Klanten en Leveranciers. Wanneer u een toeslagencode configureert, moet u de boeking definiëren. De boeking controleert zowel de debetrekening als de creditrekening. Wanneer u toeslagcodes maakt, kunt u het boekingstype selecteren dat wordt gebruikt voor elke toeslagcode. In de volgende tabel ziet u voorbeelden van gebruikelijke toeslagcodes voor Leveranciers op de pagina **Toeslagencodes**.

| Boekingstype | Voorbeeld van hoofdrekening | Voorbeeld van hoofdrekeningnaam | Rekeningtype | Debet/Credit? | Vereffeningsrekening | Description |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Bijzondere kosten voor inkoop | Laat het veld leeg. | Niet van toepassing | Artikel | Debet | Nee | **Voorbeeld van inkoopkosten voor een artikel:** </p><ul><li>Veld **Debettype** = **Artikel**</li><li>  Veld **Credittype** = **Klant/leverancier**.</li><li> Bij het boeken van het artikel wordt de hoofdrekening van het voorraadboekingsprofiel gebruikt. |
| Order, vracht | 600120 | Vracht in | Omzet | Debet | Nee | **Voorbeeld voor vrachtkosten die aan een leverancier worden betaald:** </p><ul><li>Veld **Debettype** = **Grootboekrekening**</li><li> Veld **Credittype** = **Klant/leverancier** |
| Korting\* | 503160 | Leverancierskortingen (Contra COGS)| Onkosten | Krediet | Nee | **Voorbeeld voor een leverancierskorting:**</p><ul><li>Veld **Debettype** = **Klant/leverancier**</li><li>Veld **Credittype** = **Grootboekrekening** |

\*In het kortingsvoorbeeld wordt de boeking alleen gebruikt wanneer een toeslagencode wordt toegevoegd aan de koptekst of regel van een inkooporder. De geavanceerde kortingsfunctionaliteit die beschikbaar is in Microsoft Dynamics 365 Supply Chain Management, biedt meer controle en geautomatiseerde kortingen. Zie [Leverancierkortingen](../../supply-chain//procurement/vendor-rebates.md) voor meer informatie.

In de voorgaande tabel staan drie voorbeelden van boekingstypen die voor toeslagcodes kunnen worden gebruikt. Gebruik dit als richtlijn en een selectie van voorbeelden. Het biedt geen uitgebreide lijst met alle mogelijke combinaties of boekingstypen die kunnen worden gebruikt.

Zie voor meer informatie over redencodes [Toeslagencode maken](../accounts-receivable/create-charges-codes.md).
