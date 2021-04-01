---
title: Problemen met inkooporders oplossen
description: In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met inkooporders.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 5959b098082ac1a0c8ea768795fa63b13950a9c7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242512"
---
# <a name="troubleshoot-purchase-orders"></a>Problemen met inkooporders oplossen

In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met inkooporders.

## <a name="an-action-can-be-completed-only-after-the-line-number-is-fully-distributed"></a>Een actie kan pas worden voltooid nadat het regelnummer volledig is verdeeld.

Dit probleem kan optreden vanwege inconsistenties in inkooporderdistributies.

Als u dit probleem wilt verhelpen en de inkooporder wilt terugzetten op de status *Concept*, gaat u naar **Inkoopbeheer \> Periodieke taken \> Opschonen \> Distributie van inkooporder opnieuw instellen**. Zie het volgende blogbericht voor meer informatie: [Fouten met IO-distributie in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/) oplossen.

## <a name="when-purchase-orders-are-imported-through-data-management-purchase-order-line-numbers-dont-follow-the-increment-that-defined-in-system-parameters"></a>Wanneer inkooporders worden geïmporteerd via gegevensbeheer, volgen de nummers van de inkooporderregels niet de verhoging die is gedefinieerd in de systeemparameters.

### <a name="issue-description"></a>Probleembeschrijving

Automatisch gegenereerde regelnummers voor inkooporderregels die worden geïmporteerd via de gegevensentiteit *Inkooporderregels V2* gebruiken niet de systeemregelnummerverhoging die is opgegeven in systeemparameters. Als u handmatig een inkooporder maakt en regels toevoegt via de gebruikersinterface (UI), worden de regelnummers juist verhoogd. Als u echter het DMF (Data Management Framework) gebruikt, worden ze niet op de juiste wijze verhoogd.

Dit probleem treedt op omdat het systeem bij het importeren van regels via DMF de methode van het DMF gebruikt voor het toewijzen van regels als regelnummers nog niet zijn toegewezen in de geïmporteerde entiteit. Met deze methode worden regelnummers altijd met één verhoogd.

### <a name="issue-workaround"></a>Tijdelijke oplossing voor probleem

Zorg ervoor dat de gewenste regelnummers al zijn opgegeven in de regelnummervelden van de entiteit wanneer u de inkooporderregels importeert. In dit geval worden de regelnummers niet overschreven door DMF.

## <a name="a-default-tax-group-and-a-default-cash-discount-arent-filled-in-from-the-invoice-account"></a>Een standaardbelastinggroep en een standaardcontantkorting worden niet ingevuld op basis van de factuurrekening.

Als u een factuurrekening gebruikt die verschilt van de klantrekening, worden er geen standaardbelastinggroep en standaardcontantkorting ingevuld op basis van de factuurrekening wanneer er een inkooporder wordt gemaakt.

Dit is zo ontworpen. De standaardwaarden voor de belastinggroep, contantkortingen en andere prijsgegevens zijn gebaseerd op de klantrekening, niet op de factuurrekening.

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a>Tijdens een inkooporderbevestiging wordt het foutbericht weergegeven dat de objectverwijzing niet is ingesteld of er wordt een uitzondering gegenereerd door het doel van een aanroep. Tijdens het boeken van leveranciersfacturen treedt er een uitzondering op.

Dit probleem kan optreden vanwege inconsistenties in inkooporderdistributies.

Als u dit probleem wilt verhelpen en de inkooporder wilt terugzetten op de status *Concept*, gaat u naar **Inkoopbeheer \> Periodieke taken \> Opschonen \> Distributie van inkooporder opnieuw instellen**. Zie het volgende blogbericht voor meer informatie: [Fouten met IO-distributie in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/) oplossen.

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a>Een of meer boekhoudingsverdelingen is te veel of te weinig verdeeld.

### <a name="issue-description"></a>Probleembeschrijving

Het volgende foutbericht wordt weergegeven: Een of meer boekhoudingsverdelingen is te veel of te weinig verdeeld.

### <a name="issue-resolution"></a>Probleemoplossing

Dit probleem kan optreden vanwege inconsistenties in inkooporderdistributies.

Als u dit probleem wilt verhelpen en de inkooporder wilt terugzetten op de status *Concept*, gaat u naar **Inkoopbeheer \> Periodieke taken \> Opschonen \> Distributie van inkooporder opnieuw instellen**. Zie het volgende blogbericht voor meer informatie: [Fouten met IO-distributie in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/) oplossen.

## <a name="can-i-show-only-purchase-orders-that-i-created"></a>Kan ik alleen inkooporders weergeven die ik heb gemaakt?

Deze functionaliteit is momenteel niet beschikbaar.

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a>Kan ik voorraad reserveren en transacties maken voor geregistreerde voorraad op een inkooporder?

### <a name="issue-description"></a>Probleembeschrijving

Zelfs wanneer artikelen de status *Geregistreerd* in een inkooporder hebben, kunt u nog steeds de voorraad reserveren. Met andere woorden, u kunt transacties maken voor de geregistreerde voorraad.

### <a name="reproduce-the-issue"></a>Het probleem reproduceren

In de volgende procedure wordt één manier weergegeven om het probleem te reproduceren.

1. Inkooporder maken.
2. Registreer de inkooporderregel.
3. U ziet dat u reserveringen of transacties voor de geregistreerde voorraad kunt genereren.

### <a name="issue-resolution"></a>Probleemoplossing

Dit is zo ontworpen. De verwachting is dat de geregistreerde artikelen fysiek zijn aangekomen in het magazijn of voorraad en dat ze daarom beschikbaar zijn voor reservering.

## <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a>Inkooporders reflecteren niet de taalinstellingen van de rechtspersoon.

### <a name="issue-description"></a>Probleembeschrijving

De productnaam op een inkooporder wordt weergegeven in de systeemtaal in plaats van de taal die is ingesteld voor de rechtspersoon waarvoor de inkooporder is gemaakt.

### <a name="reproduce-the-issue"></a>Het probleem reproduceren

In de volgende procedure wordt één manier weergegeven om het probleem te reproduceren.

1. Stel de systeemtaal in op *en-US* (Amerikaans-Engels).
1. Zorg ervoor dat er een product is waarin de talen *en_US* en *de* (Duits) worden onderhouden voor vertalingen van de productnaam.
1. De taal van een rechtspersoon wijzigen in *de*.
1. Maak in de rechtspersoon waarvoor de taal *de* is ingesteld een inkooporder die het product bevat.
1. U ziet dat de productnaam nog steeds wordt weergegeven in Amerikaans Engels (de systeemtaal).

### <a name="issue-resolution"></a>Probleemoplossing

Dit is zo ontworpen. Op inkooporders wordt het product altijd weergegeven in de systeemtaal. De taal van de inkooporder wordt gebruikt bij het maken van een bevestigingsjournaal.

## <a name="the-approved-vendor-list-by-product-entity-doesnt-allow-the-effective-date-to-be-changed"></a>De ingangsdatum kan niet per productentiteit worden gewijzigd in de lijst met goedgekeurde leveranciers.

### <a name="issue-description"></a>Probleembeschrijving

Een product heeft een goedgekeurde leverancier die bijvoorbeeld een ingangsdatum heeft van 11 januari 2018 (*01/11/2018*) en de vervaldatum *Nooit*. Als u de ingangsdatum probeert te wijzigen in 10 januari 2018 (*01/10/2018*) of 12 januari 2018 (*01/12/2018*), wordt het volgende foutbericht weergegeven:

> Kan geen record maken in lijst met goedgekeurde leveranciers (PdsApproveVendorList). De waarde voor Vervaldatum moet groter zijn dan of gelijk zijn aan die van de Ingangsdatum.

### <a name="issue-resolution"></a>Probleemoplossing

U kunt alleen de periode verlengen waarvoor de leverancier is goedgekeurd. De volgende regels zijn van toepassing:

- Als u de ingangsdatum zo wilt wijzigen dat deze eerder is dan een van de bestaande records (perioden) voor de leverancier van het artikel, moet de vervaldatum van de nieuwe periode eerder zijn dan de vervaldatums in de bestaande records.
- Als u de vervaldatum zo wilt wijzigen dat deze later is dan een van de bestaande perioden, moet de ingangsdatum na de laatste vervaldatum in een bestaande record vallen.
- Als u de totale periode waarvoor de leverancier is goedgekeurd, wilt verkorten, moet u bestaande records verwijderen of wijzigen. U kunt ook de schakeloptie **Afkappen** gebruiken tijdens het importeren. Met deze schakeloptie verwijdert u alle bestaande records in de tabel voor goedgekeurde leveranciers per artikel.

Voor het voorbeeldscenario dat in de beschrijving van het probleem wordt beschreven, waarbij een record de ingangsdatum *01/11/2018* en de vervaldatum van *Nooit* heeft, kunt u een nieuwe record importeren met de ingangsdatum *01/10/2018* en de vervaldatum *Nooit*. Het is echter niet mogelijk om via gegevensbeheer de periode zo te verkleinen dat de ingangsdatum wordt bijgewerkt naar *01/12/2018*. U moet deze wijziging aanbrengen in de gebruikersinterface.

## <a name="after-i-change-the-delivery-address-on-a-purchase-order-header-the-delivery-name-isnt-synced"></a>Nadat ik het afleveradres in een inkooporderkop heb gewijzigd, wordt de leveringsnaam niet gesynchroniseerd.

### <a name="issue-description"></a>Probleembeschrijving

Het adres in de koptekst van een inkooporder wordt bijgewerkt naar een adres dat geen afleveradres is. Hoewel het adres op de inkooporder wordt bijgewerkt, wordt de leveringsnaam niet bijgewerkt op basis van het bijgewerkte adres.

### <a name="issue-resolution"></a>Probleemoplossing

Dit is zo ontworpen. Het geselecteerde adres moet worden geclassificeerd als afleveradres. Anders wordt de leveringsnaam niet bijgewerkt op basis van het geselecteerde adres.

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a>Kan ik de gebruiker vinden die een inkooporder heeft geannuleerd?

Deze informatie wordt alleen bijgehouden als de inkooporder onder wijzigingsbeheer valt. Als u wijzigingsbeheer gebruikt, kunt u zien wie de wijziging heeft ingediend (de annulering) en wie deze heeft goedgekeurd.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]