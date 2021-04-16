---
title: Problemen met verkooporders oplossen
description: In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met verkooporders.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b5389b0d5a8ff68a3c16dedd2d8bb62f6e99af4f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824721"
---
# <a name="troubleshoot-sales-orders"></a>Problemen met verkooporders oplossen

In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met verkooporders.

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a>De belastinggegevens worden niet bijgewerkt als ik de locatie in de kop van een verkooporder wijzig.

### <a name="issue-description"></a>Probleembeschrijving

Als de locatie, het magazijn of het afleveradres wordt gewijzigd in de koptekst van een verkooporder of op het regelniveau, wordt de belastinginformatie voor de aanvraag niet automatisch bijgewerkt voor de regels.

### <a name="issue-resolution"></a>Probleemoplossing

Dit is zo ontworpen. Het probleem doet zich voor omdat het afleveradres, de locatie en het magazijn niet automatisch op regelniveau worden gewijzigd. U moet ze handmatig bijwerken.

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a>Als er twee handelsovereenkomsten zijn voor dezelfde periode of overlappende perioden, wordt altijd dezelfde overeenkomstregel geselecteerd.

### <a name="issue-description"></a>Probleembeschrijving

Als twee handelsovereenkomsten zijn gedefinieerd voor dezelfde periode of overlappende perioden, lijkt telkens dezelfde handelsovereenkomst te worden geselecteerd wanneer u verkooporderregels maakt die die artikelen bevatten.

### <a name="issue-resolution"></a>Probleemoplossing

Als er meer dan één handelsovereenkomst voor een bepaalde datum is, wordt altijd de handelsovereenkomst met de laagste prijs geselecteerd. Download het volgende technische document voor meer informatie: [Handelsovereenkomsten in Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a>Kan ik een inkooporder aan een verkooporder koppelen om aan de vraag te voldoen?

U kunt een inkooporder maken op basis van een verkooporder. Meer informatie vindt u in [Een inkooporder maken op basis van een verkooporder](tasks/create-purchase-order-sales-order.md).

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a>Ik kan een retourorder of een verkooporder niet annuleren of verwijderen.

U kunt alleen verkooporders en retourorders annuleren die de status *Gemaakt* hebben. Zie voor meer informatie [Een retourorder annuleren](../service-management/cancel-return-order.md).

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a>Wanneer ik een verkooporder wil annuleren, krijg ik het bericht "Reserveringen kunnen niet worden verwijderd omdat er werk is gemaakt dat afhankelijk is van de reserveringen".

Foutcode: WAX4661

Als werk aan een verkooporder is gekoppeld, kunt u de verkooporder pas annuleren als het werk is geannuleerd en omgekeerd. Deze vereiste geldt ook als het werk dat aan de verkooporder is gekoppeld, is afgesloten.

Volg deze stappen om dit probleem op te lossen.

1. Annuleer het werk en plaats voorraad terug op de gewenste locatie. Ga naar de desbetreffende belasting van de verkooporder en selecteer **Opgenomen hoeveelheid reduceren** op de ladingsregel of **Werk omkeren** in het actievenster.

    Het werk heeft nu de status *Geannuleerd* en er wordt automatisch werk voor een nieuwe voorraadverplaatsing gemaakt en verwerkt om de voorraad terug te zetten op de locatie die op het moment van de omkering is beschreven.

2. Verwijder de lading. De verzending wordt ook verwijderd.
3. U moet nu naar de verkooporder kunnen gaan en deze kunnen annuleren.

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a>Ik kan een intercompany-inkooporder die aan een verkooporder is gekoppeld, niet annuleren.

### <a name="issue-description"></a>Probleembeschrijving

Als u probeert een intercompany-inkooporder te annuleren die aan een verkooporder is gekoppeld, wordt mogelijk het volgende foutbericht weergegeven: 'Hoeveelheid kan niet worden verminderd omdat de resterende bijwerkhoeveelheid van teken verandert'.

### <a name="issue-resolution"></a>Probleemoplossing

Dit probleem is verholpen in Microsoft Dynamics 365 Supply Chain Management versie 10.0.13. In deze versie en latere versies kunt u nu een intercompany-inkooporder annuleren die aan een verkooporder is gekoppeld.

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a>Kan ik een gefactureerde verkooporder terugzetten als die is verwijderd?

### <a name="issue-description"></a>Probleembeschrijving

Een gefactureerde verkooporder is per ongeluk verwijderd en u wilt deze herstellen of de details weergeven.

### <a name="issue-resolution"></a>Probleemoplossing

Als de verwijderde verkooporder al is gefactureerd, gaat u naar **Klantaccount \> Transacties \> Oorspronkelijke document \> Details weergeven**. Zoek de factuur waarnaar u op zoek bent en selecteer deze om de details weer te geven. Deze gegevens omvatten de verkooporderverwijzing. Op die pagina hebt u ook toegang tot de verkoopordergegevens.

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a>De deadline van een verkooporderkoptekst staat niet in de gegevensentiteit SalesOrderHeaderV2Entity.

Het veld Deadline bestaat niet in de entiteit *SalesOrderHeaderV2Entity*.

## <a name="i-must-delete-orphaned-sales-order-records"></a>Ik moet zwevende verkooporderrecords verwijderen.

Als u zwevende verkooporderrecords wilt opschonen, voert u de periodieke taak *Verkooporders verwijderen* uit door naar een van de volgende locaties te gaan:

- Verkoop en marketing \> Periodieke taken \> Opschonen \> Verkooporders verwijderen
- Detailhandel en commerce \> IT detailhandel en commerce \> Opschonen \> Verkooporders verwijderen

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a>Is er een manier om commissies te berekenen op facturen die al zijn geboekt?

Supply Chain Management biedt momenteel geen ondersteuning voor de berekening van commissies voor geboekte facturen.

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a>Een bundelartikel wordt niet ondersteund in een intercompany-proces.

Het bundelartikel is niet beschikbaar voor de inkooporder, want als u de verkooporderregels voor het bundelartikel bekijkt, ziet u dat de hoeveelheid *0* (nul) is en de status *Geannuleerd*. Dit is zo ontworpen. In de verkooporder worden alleen de onderdelen van het bundelartikel gekocht. In de verkooporder wordt niet het bundelartikel zelf gekocht.

Als u een bundel moet aanschaffen, overweeg dan of u deze als een bundelartikel moet markeren, omdat deze functionaliteit eigenlijk is bedoeld voor opbrengsttoerekeningsscenario's. Meer informatie over bundelartikelen vindt u in [Bundels](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]