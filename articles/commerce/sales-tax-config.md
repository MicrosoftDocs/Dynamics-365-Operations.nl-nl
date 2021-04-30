---
title: Btw voor online orders configureren
description: Dit onderwerp biedt een overzicht van de selectie van btw-groepen voor verschillende typen online orders in Dynamics 365 Commerce.
author: gvrmohanreddy
manager: AnnBe
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8df939c1a566fb63bc53e455cc6c2aa85956ac79
ms.sourcegitcommit: 583801af75c50915ea5ffc60e831fb617d045533
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2021
ms.locfileid: "5853806"
---
# <a name="configure-sales-tax-for-online-orders"></a>Btw voor online orders configureren

[!include [banner](includes/banner.md)]

Dit onderwerp bevat een overzicht van de selectie van btw-groepen voor verschillende online ordertypen met belastinginstellingen op basis van bestemming of klantrekening. 

Mogelijk moet uw e-commercekanaal opties, zoals levering of ophalen, ondersteunen voor online bestellingen. De btw-toepasselijkheid is gebaseerd op de optie die door uw online klanten is geselecteerd. 

## <a name="destination-based-taxes-for-online-orders"></a>Op bestemming gebaseerde btw voor online orders

In het algemeen wordt de btw voor online orders die naar klantadressen worden verzonden, gedefinieerd door de bestemming. Elke btw-groep bevat een btw-configuratie op basis van de detailhandel waaronder uw bedrijf bestemmingsgegevens kan definiëren, zoals land of regio, staat, regio en plaats in een hiërarchische vorm.

### <a name="orders-delivered-to-customer-address"></a>Orders die aan een klantadres zijn geleverd

Wanneer een online order wordt geplaatst, gebruikt de commerce-belastingservice het afleveradres van alle regelartikelen in de order en zoekt naar btw-groepen met dezelfde btw-criteria op basis van de bestemming. Voor een online order met het afleveradres voor het artikel naar San Francisco, Californië, wordt de btw-groep en btw-code voor Californië automatisch berekend en wordt de btw voor elk artikel dienovereenkomstig berekend.

### <a name="order-pick-up-in-store"></a>Order ophalen in de winkel

Voor orderregels met ophalen in winkel of bij een afhaallocatie, wordt de btw-groep van de geselecteerde ophaalwinkel toegepast. Zie [Andere btw-opties voor winkels instellen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores) voor meer informatie over het configureren van de btw voor een bepaalde winkel.

## <a name="customer-account-based-taxes-for-online-orders"></a>Op klantrekening gebaseerde btw voor online orders

Er kan een bedrijfsscenario zijn waarin u een btw-groep wilt configureren voor een specifieke klantrekening in Commerce Headquarters. Er zijn twee locaties in Headquarters waar u btw op een klantrekening kunt configureren. Als u deze wilt openen, moet u eerst naar een detailpagina voor klanten gaan via **Retail en Commerce \> Klanten \> Alle klanten** en vervolgens een klant selecteren.

Er zijn twee locaties waar u btw op een klantrekening kunt configureren:

- **Btw-groep** op het sneltabblad **Factuur en levering** van de pagina met klantdetails. 
- **Btw**  op het sneltabblad **Algemeen** van de pagina **Adressen beheren**. Als u hier wilt komen vanaf de klantdetailpagina, selecteert u een specifiek adres onder het sneltabblad **Adressen** en selecteert u vervolgens **Geavanceerd**.

> [!TIP]
> Als u bij online klantorders alleen de op bestemming gebaseerde belastingen wilt toepassen en belastingen op klantrekeningen wilt vermijden, moet u ervoor zorgen dat het veld **Btw-groep** leeg is op het sneltabblad **Factuur en levering** van de pagina met klantdetails. Om er zeker van te zijn dat nieuwe klanten die zich via het online kanaal aanmelden, de btw-groepsinstellingen niet overnemen van de standaardinstellingen voor de klant of klantengroep, moet het veld **Btw-groep** ook leeg zijn voor de standaard klantinstellingen en klantengroepinstellingen van het online kanaal (**Retail en Commerce \> Klanten \> Klantengroepen**).

## <a name="determine-destination-based-tax-or-customer-account-based-tax-applicability"></a>Toepasbaarheid van btw op basis van bestemming of klantrekening bepalen 

In de volgende tabel wordt uitgelegd of op bestemming of op klantrekeningbelasting gebaseerde belastingen worden toegepast op online orders. 

| Klanttype | Verzendadres                   | Klant > Factuur en levering > Btw-groep? | Adres van klantrekening in Headquarters? | Klantadres > Geavanceerd > Algemeen > Btw-groep?                                              | Btw-groep toegepast      |
|---------------|------------------------------------|-----------------------------------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------|------------------------------|
| Gast         | Manhattan, NY                      | Nee (leeg)                                                | Nee (leeg)                              | Nee (leeg)                                                                                                   | NY (op bestemming gebaseerde btw) |
| Aangemeld     | Austin, TX                          | Nee (leeg)                                             | Ja                               | None<br/><br/>Nieuw adres dat via online kanaal is toegevoegd.                                                            | TX (op bestemming gebaseerde btw) |
| Aangemeld     | San Francisco, CA (Ophalen bij winkel) | Ja (NY)                                            | Niet van toepassing                              | Niet van toepassing                                                                                                    | CA (op bestemming gebaseerde btw) |
| Aangemeld     | Houston, TX                         | Ja (NY)                                            | Ja                               | Ja (NY)<br/><br/>Nieuw adres dat via een online kanaal en btw-groep wordt overgenomen van de klantrekening. | NY (btw op basis van klantrekening)  |
| Aangemeld     | Austin, TX                          | Ja (NY)                                            | Ja                               | Ja (NY)<br/><br/>Nieuw adres dat via een online kanaal en btw-groep wordt overgenomen van de klantrekening. | NY (btw op basis van klantrekening)  |
| Aangemeld     | Sarasota, FL                       | Ja (NY)                                            | Ja                               | Ja (WA)<br/><br/>Handmatig ingesteld op WA.                                                                          | WA (btw op basis van klantrekening)  |
| Aangemeld     | Sarasota, FL                       | Nee (leeg)                                                | Ja                               | Ja (WA)<br/><br/>Handmatig ingesteld op WA.                                                                          | WA (btw op basis van klantrekening)  |

## <a name="additional-resources"></a>Aanvullende bronnen

[Belastingen voor online winkels instellen op basis van de bestemming](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination)

[Btw-overzicht](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[Btw-berekeningsmethoden in het veld Oorsprong](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[Btw-overeenkomst en -overschrijvingen](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[Berekeningsopties Volledige bedrag en interval voor btw-codes](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[Berekening van btw-vrijstelling](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
