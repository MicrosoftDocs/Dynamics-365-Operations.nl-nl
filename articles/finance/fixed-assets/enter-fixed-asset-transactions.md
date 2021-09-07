---
title: Transactieopties voor vaste activa
description: In dit onderwerp worden de beschikbare methoden voor het maken van vaste-activatransacties beschreven.
author: moaamer
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: roschlom
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9e2d7f21d8c88185383e252f8f6324208493c81
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344685"
---
# <a name="fixed-asset-transaction-options"></a>Transactieopties voor vaste activa

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit onderwerp worden de beschikbare methoden voor het maken van vaste-activatransacties beschreven.

U kunt vaste activa instellen voor integratie met crediteuren, debiteuren, inkoop en sourcing en grootboek. Ook kunt u artikelen in voorraadbeheer overbrengen naar vaste activa als u deze items intern gebruikt.

## <a name="accounts-payable"></a>Leveranciers    
U kunt transacties voor vaste activa invoeren op de pagina Journaalboekstuk. Deze pagina kan worden geopend vanuit de pagina Factuurjournaal. U kunt de pagina Journaalboekstuk ook openen via de pagina Factuurgoedkeuringsjournaal. Selecteer Vaste activa in het veld Tegenrekeningtype. Selecteer vervolgens een nummer voor vaste activa in het veld Tegenrekening. Voer op het tabblad Vaste activa waarden in het veld Transactietype en Boek in.

## <a name="accounts-receivable"></a>Klanten  
U kunt transacties voor vaste activa invoeren op de pagina Vrije-tekstfactuur.  Selecteer een regelartikel op de pagina Vrije-tekstfactuur in het raster met factuurregels. Klik op het sneltabblad Regeldetails. Geef het VA-nummer en boek op voor de afboekingstransactie. Voor facturen met vrije tekst is het vaste-activatransactietype altijd Verkoop/afstoting.

## <a name="procurement-and-sourcing"></a>Inkoopbeheer
U kunt transacties voor vaste activa invoeren op de pagina Inkooporder. Voer de vereiste informatie in om een inkooporder te maken en klik op OK. Klik op de pagina Inkooporder op het sneltabblad Regeldetails. Geef vervolgens op het tabblad Vaste activa informatie op over het vaste activum. 

Om een verwervingstransactie voor een bestaand vast activum te boeken, geeft u het VA-nummer, het boek en het transactietype op. Het vaste activum kan niet worden geboekt als deze informatie ontbreekt. U boekt een verwervingstransactie voor een nieuw vast activum door het selectievakje Nieuw vast activum? in te schakelen en de vaste-activagroep te selecteren waaraan het nieuwe activum moet worden toegewezen. Geen van de vaste-activavelden voor een regel zijn echter beschikbaar als het artikel zich in een voorraadmodelgroep bevindt die een standaardkostenvoorraadmodel gebruikt. Bovendien bepalen de opties die zijn gedefinieerd op de pagina Parameters vaste activa of u verwervingstransacties kunt boeken vanuit de inkoopmodules. 

Wanneer een inkooporder of het Voorraad naar vaste-activajournaal wordt gebruikt voor de verwerking van vaste activa, heeft dit gevolgen voor de voorraadwaarde.

## <a name="general-ledger"></a>Grootboek
Elk type vaste-activatransactie kan worden geboekt op de Algemeen journaal. Ook kunt u dagboeken gebruiken in vaste activa om VA-transacties te boeken.

### <a name="options-for-entering-fixed-asset-transaction-types"></a>Opties voor het invoeren van vaste-activatransactietypen


| Transactietype                    | Module                   | Opties                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| Verwerving, Correctie van verwerving | Vaste activa             | Vaste activa, Voorraad naar vaste activa   |
|                                     | Grootboek           | Algemeen journaal                           |
|                                     | Leveranciers             | Factuurjournaal, Factuurgoedkeuringsjournaal |
|                                     | Inkoopbeheer | Inkooporder                            |
| Afschrijving                        | Vaste activa             | Vaste activa                              |
|                                     | Grootboek           | Algemeen journaal                           |
| Afstoting                            | Vaste activa             | Vaste activa                              |
|                                     | Grootboek           | Algemeen journaal                           |
|                                     | Debiteuren      | Vrije-tekstfactuur                         |

De resterende waarde van de afschrijvingsperioden van het vaste activum wordt niet bijgewerkt wanneer een regel van een journaal van het type afschrijvingstransactie handmatig wordt gemaakt of wordt geïmporteerd door middel van een gegevensentiteit. De resterende waarde wordt bijgewerkt wanneer het afschrijvingsvoorstelproces wordt gebruikt om de journaalregel te maken.

Zie [Integratie vaste activa](fixed-asset-integration.md) voor meer informatie.

Het systeem voorkomt dat afschrijvingen twee keer naar dezelfde periode worden geboekt. Als twee gebruikers bijvoorbeeld afzonderlijk van elkaar afschrijvingsvoorstellen aanmaken voor januari, wordt de afschrijving van de eerste gebruiker in het eerste journaal geboekt. Wanneer de tweede gebruiker een afschrijving boekt in het tweede journaal, controleert het systeem de datum waarop de afschrijving de laatste keer is uitgevoerd en wordt de afschrijving geen tweede keer voor dezelfde periode geboekt.

### <a name="transactions-that-require-a-different-voucher-number"></a>Transacties waarvoor een ander boekstuknummer vereist is

Voor de volgende vaste-activatransacties worden verschillende boekstuknummers gebruikt:

- Er worden extra aanschafkosten voor een activum gemaakt en 'achterstallige' afschrijving wordt berekend.
- Een activum wordt opgesplitst.
- Een parameter voor het berekenen van afschrijving bij buitengebruikstelling wordt ingeschakeld en vervolgens wordt het activum afgestoten.
- De servicedatum van ene activum valt vóór de verwervingsdatum. Daarom wordt een afschrijvingscorrectie geboekt.

> [!NOTE]
> Wanneer u transacties invoert, moet u ervoor zorgen dat alle transacties van toepassing zijn op hetzelfde vaste activum. Een boekstuk wordt niet geboekt als het meer dan één vast activum bevat, zelfs niet als het veld **Nieuw boekstuk** is ingesteld op **Maximaal één boekstuknummer** op de pagina **Journaalnamen** in Grootboek. Als u meer dan één vast activum in het boekstuk opneemt, ontvangt u het bericht 'Er kan niet meer dan één vaste-activatransactie per boekstuk zijn weergegeven' en kunt u het boekstuk niet boeken.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
