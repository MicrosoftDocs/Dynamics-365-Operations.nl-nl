---
title: Problemen met productontvangstbonnen en -facturering oplossen
description: In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden terwijl u werkt met productontvangstbonnen en -facturering.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 3522a024261ff6dfffb53f2101139460be7669e4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832005"
---
# <a name="troubleshoot-product-receipts-and-invoicing"></a>Problemen met productontvangstbonnen en -facturering oplossen

In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden terwijl u werkt met productontvangstbonnen en -facturering.

## <a name="i-cant-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a>Ik kan niet meer dan één factuur boeken voor een inkooporderregel die op categorieën gebaseerde artikelen bevat.

Een hoeveelheid is verplicht als u facturen wilt boeken. Als de volledige hoeveelheid van een regel slechts voor een gedeeltelijk bedrag is gefactureerd, kunt u het resterende bedrag niet op een andere factuur factureren.

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a>Tijdens een inkooporderbevestiging wordt het foutbericht weergegeven dat de objectverwijzing niet is ingesteld of er wordt een uitzondering gegenereerd door het doel van een aanroep. Tijdens het boeken van leveranciersfacturen treedt er een uitzondering op.

Dit probleem kan optreden vanwege inconsistenties in inkooporderdistributies.

Als u dit probleem wilt verhelpen en de inkooporder wilt terugzetten op de status *Concept*, gaat u naar **Inkoopbeheer \> Periodieke taken \> Opschonen \> Distributie van inkooporder opnieuw instellen**. Zie het volgende blogbericht voor meer informatie: [Fouten met IO-distributie in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/) oplossen.

## <a name="i-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a>Ik kan niet meerdere productontvangstbonnen in één inkooporder consolideren.

U kunt niet meerdere productontvangstbonnen consolideren in één inkooporder als de verschillende productontvangstbonregels verschillende boekingsdatums hebben.

In eerdere versies van Microsoft Dynamics 365 Supply Chain Management was consolidatie in deze situatie toegestaan. Dit bleek is echter foutgevoelig te zijn. De boekhoudingsdatum op de gemaakte inkooporderregels mag niet verschillen van de boekhoudingsdatum op de productontvangstbonregels waarop deze inkooporderregels zijn gemaakt. (De boekhoudingsdatum op de inkooporderregels komt overeen met de boekhoudingsdatum in de koptekst van de inkooporder.) De consolidatie van meerdere productontvangstbonnen in één inkooporder is daarom niet meer toegestaan.

De boekhoudingsdatum wordt bijvoorbeeld gebruikt voor budgetreserveringen en vordering. Daarom moet deze tijdens de overgang van productontvangstbon naar de inkooporder worden bewaard.

## <a name="when-product-receipts-are-canceled-transactions-can-be-posted-to-a-suspended-ledger-account"></a>Wanneer productontvangstbonnen worden geannuleerd, kunnen transacties naar een uitgestelde grootboekrekening worden geboekt.

### <a name="issue-description"></a>Probleembeschrijving

Als een productontvangstbon wordt geannuleerd, kunnen transacties naar uitgestelde grootboekrekeningen worden geboekt, zelfs als de hoofdrekeningen zijn opgeschort.

### <a name="reproduce-the-issue"></a>Het probleem reproduceren

In de volgende procedure wordt één manier weergegeven om het probleem te reproduceren.

1. Controleer op de pagina **Parameters van module Leveranciers** op het tabblad **Algemeen** of de optie **Productontvangstbon in grootboek boeken** is ingesteld op *Ja*.
1. Maak een inkooporder en voeg een orderregel toe met een hoeveelheid van *1000* voor een product.
1. Bevestig de inkooporder.
1. Boek de productontvangstbon en controleer de boekstukken.
1. Schort de relevante hoofdrekeningen, *200140* en *140200*, op.
1. Annuleer de geboekte productontvangstbon.
1. U ziet dat transacties naar de uitgestelde grootboekrekeningen kunnen worden geboekt.

### <a name="issue-resolution"></a>Probleemoplossing

Transacties kunnen worden geboekt naar de opgeschorte grootboekrekeningen wanneer productontvangstbonnen worden geannuleerd, omdat met dit gedrag correcte boekingen mogelijk zijn.

## <a name="a-product-receipt-voucher-number-is-consumed-even-if-no-financial-voucher-is-generated-during-product-receipt"></a>Er wordt een boekstuknummer voor de productontvangstbon verbruikt, zelfs als er tijdens de productontvangst geen financieel boekstuk is gegenereerd.

Als de optie **Toerekening van aansprakelijkheid bij productontvangstbon** is ingesteld op *Nee* voor de artikelmodelgroep, worden er geen boekingen naar het grootboek uitgevoerd. Er wordt echter een fysieke gebeurtenis voor de boekhouding in een subadministratie geregistreerd en voor die gebeurtenis is een boekstuknummer vereist. Dit boekstuknummer is het boekstuknummer waarnaar in de voorraadtransacties wordt verwezen.

Het is raadzaam om de optie **Toerekening van aansprakelijkheid bij productontvangstbon** in te stellen op *Ja*, zoals wordt beschreven in het volgende blogbericht: [Diverse toeslagen boeken op het moment van ontvangst van het product](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).

## <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a>De instelling Boeken op toeslagrekening in grootboek is niet ingeschakeld.

### <a name="issue-description"></a>Probleembeschrijving

Dit probleem doet zich voor wanneer een inkooporder wordt gefactureerd, als de optie **Boeken op toeslagrekening in grootboek** is ingesteld *Ja* op het tabblad **Factuur** van de pagina **Parameters van module Leveranciers**.

### <a name="reproduce-the-issue"></a>Het probleem reproduceren

In de volgende procedure wordt één manier weergegeven om het probleem te reproduceren.

1. Ga naar **Leveranciers \> Instellen \> Parameters van Leveranciers**.
1. Stel op het tabblad **Factuur** de optie **Boeken op toeslagrekening in grootboek** in op *Ja*.
1. Ga naar **Voorraadbeheer \> Instellen \> Boeken \> Boeken**.
1. Controleer op het tabblad **Inkooporder** of u alle regels in de inkoopuitgave voor het product hebt verwijderd.
1. Ga naar **Leveranciers \> Inkooporders \> Alle inkooporders**.
1. Inkooporder maken. Selecteer in het veld **Leveranciersrekening** de optie *1001 Acme Office Supplies*.
1. Voeg een inkooporderregel met de volgende instellingen toe:

    - **Artikelnummer:** *D0011 Laser Projector*
    - **Locatie:** *1*
    - **Magazijn:** *11*
    - **Hoeveelheid:** *4*

1. Selecteer in het actievenster op het tabblad **Inkoop** in de groep **Actie** de optie **Bevestigen**.
1. Selecteer in het Actievenster op het tabblad **Ontvangen** in de groep **Genereren** de optie **Productontvangstbon**.
1. Voer in het dialoogvenster **Productontvangstbon boeken** in het veld **Productontvangstbon** een willekeurig getal in en selecteer vervolgens **OK**.
1. Selecteer in het actievenster op het tabblad **Factuur** in de groep **Genereren** de optie **Factuur**.
1. Voer in het veld **Getal** een willekeurig getal in als het factuurnummer.
1. Werk de vereffeningsstatus bij en boek.
1. U ontvangt nu de volgende fout wanneer u een factuur genereert vanuit een inkooporder: 'Rekeningnummer voor inkoopuitgave van het transactietype bestaat niet'.

### <a name="issue-resolution"></a>Probleemoplossing

Dit is afhankelijk van de parameterinstellingen voor facturen en factuurgroepen. Zie het volgende blogbericht voor meer informatie: [Boekhouding voor inkooptoeslag en voorraadwijziging](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]