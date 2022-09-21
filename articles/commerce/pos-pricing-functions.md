---
title: Prijsfuncties in POS
description: In dit artikel worden verschillende prijs- en kortingsfuncties in de POS-toepassing (Point of Sale, verkooppunt) van Microsoft Dynamics 365 Commerce beschreven.
author: boycez
ms.date: 08/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2022-07-14
ms.openlocfilehash: 210798ac192ee251594ec8ff9d23dab31ec2043e
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473682"
---
# <a name="pricing-functions-in-pos"></a>Prijsfuncties in POS

[!include [banner](includes/banner.md)]

In dit artikel worden verschillende prijs- en kortingsfuncties in de POS-toepassing (Point of Sale, verkooppunt) van Microsoft Dynamics 365 Commerce beschreven.

De POS-toepassing van Dynamics 365 Commerce biedt uitgebreide mogelijkheden waarmee eerstelijnsmedewerkers Store Commerce-bewerkingen kunnen uitvoeren. In de volgende tabel ziet u de prijs- en kortingsfuncties die momenteel beschikbaar zijn in de toepassing.

| Functie                       | POS-bewerkingen |
|--------------------------------|----------------|
| Prijzen weergeven                    | [Prijscontrole](#price-check) |
| Kortingen weergeven                 | [Alle kortingen weergeven](#view-all-discounts)<br>[Beschikbare kortingen weergeven](#view-available-discounts) |
| Prijzen overschrijven                | [Prijsoverschrijving](#price-override) |
| Kortingen toepassen of verwijderen      | [Kortingsbedrag voor regelitem](#line-discount-amount)<br>[Regelkortingspercentage](#line-discount-percent)<br>[Totaal kortingsbedrag](#total-discount-amount)<br>[Totaal kortingspercentage](#total-discount-percent)<br>[Systeemkortingen verwijderen uit transactie](#remove-system-discounts-from-transaction)<br>[Systeemkortingen opnieuw toepassen](#reapply-system-discounts) |
| Coupons toepassen of verwijderen        | [Couponcode toevoegen](#add-coupon-code)<br>[Couponcode verwijderen](#remove-coupon-code) |
| Prijzen en kortingen berekenen | [Opnieuw berekenen](#recalculate) |

Zie [Online- en offline POSs-bewerkingen](pos-operations.md) voor informatie over de manier waarop de voorgaande bewerkingen kunnen worden geconfigureerd in de POS-toepassing en of deze de offlinemodus ondersteunen.

## <a name="price-check"></a>Prijscontrole

Met de bewerking **Prijscontrole** kunnen POS-gebruikers vooraf geconfigureerde prijzen zoeken voor een specifiek product.

## <a name="view-all-discounts"></a>Alle kortingen weergeven

Met de bewerking **Alle kortingen weergeven** kunnen POS-gebruikers alle effectieve promoties zoeken die momenteel actief zijn in het winkelkanaal. Deze bewerking vermeldt met name alle kortingen die voldoen aan een van de volgende voorwaarden:

- De prijsgroep van de korting komt overeen met de prijsgroep van de winkel.
- De prijsgroep van de korting wordt toegewezen aan een aansluiting of een loyaliteitsprogramma.
- De prijsgroep van de korting wordt toegewezen aan een catalogus die aan de winkel is gekoppeld.

Met de bewerking **Alle kortingen weergeven** worden alleen kortingen weergegeven die niet concurreren met al vereffende kortingen. Dit zorgt ervoor dat, als een verkoopmedewerker een klant op de hoogte stelt over een korting, en de klant de vereiste actie kiest (de klant koopt bijvoorbeeld één artikel meer om 10 procent te krijgen), wordt de korting toegepast op de transactie. Op coupon gebaseerde kortingen worden alleen weergegeven als de parameter **Toepassen zonder couponcode** is ingeschakeld.

In de bewerking **Alle kortingen weergeven** kunnen POS-gebruikers zoeken naar kortingen op naam en omschrijving en kunnen ze kortingen filteren op basis van of deze een coupon vereisen.

## <a name="view-available-discounts"></a>Beschikbare kortingen weergeven

Met de bewerking **Beschikbare kortingen weergeven** kunnen POS-gebruikers alle kortingen weergeven die van toepassing zijn op een geselecteerde regel in een transactie of op de gehele transactie. De kortingen die van toepassing zijn op een geselecteerde regel betreft kortingen die al zijn toegepast en kortingen die nog niet zijn toegepast, maar kunnen worden toegepast (bijvoorbeeld combinatiekortingen waarvoor extra artikelen nodig zijn). Als een toepasselijke korting wordt gekoppeld aan een coupon waarbij de parameter **Toepassen zonder couponcode** is ingeschakeld, kan de POS-gebruiker ook de functie **Coupon toepassen** in deze bewerking gebruiken om de coupon rechtstreeks in te wisselen zonder een couponcode of streepjescode van een coupon te moeten invoeren of scannen.

## <a name="price-override"></a>Prijsoverschrijving

Met de bewerking **Prijs overschrijven** kunnen POS-gebruikers de verkoopprijs van een product in een transactie overschrijven. Deze bewerking werkt alleen voor producten die zijn geconfigureerd om prijsoverschrijvingen toe te staan.

## <a name="line-discount-amount"></a>Kortingsbedrag voor regelitem

Met de bewerking **Regelkortingsbedrag** kunnen POS-gebruikers een kortingsbedrag invoeren voor een regelartikel in een transactie. Deze bewerking is alleen van toepassing op kortingsartikelen en heeft betrekking op de waarde van het **maximale regelkortingsbedrag** dat is opgegeven in de POS-machtigingsgroep voor de gebruiker.

## <a name="line-discount-percent"></a>Regelkortingspercentage

Met de bewerking **Regelkortingspercentage** kunnen POS-gebruikers een kortingspercentage invoeren voor een regelartikel in een transactie. Deze bewerking is alleen van toepassing op kortingsartikelen en heeft betrekking op de waarde van het **maximale regelkortingspercentage** dat is opgegeven in de POS-machtigingsgroep voor de gebruiker.

## <a name="total-discount-amount"></a>Totaal kortingsbedrag

Met de bewerking **Totaal kortingsbedrag** kunnen POS-gebruikers een kortingsbedrag invoeren voor een transactie. Deze bewerking is alleen van toepassing op kortingsartikelen en heeft betrekking op de waarde van het **maximale totale kortingsbedrag** dat is opgegeven in de POS-machtigingsgroep voor de gebruiker. Als het ingevoerde kortingsbedrag hoger is dan het maximale totale kortingsbedrag, wordt de bewerking geblokkeerd en wordt er geen machtiging overschrijvende stroom geactiveerd. Op dit moment kan een totaal kortingsbedrag niet worden toegepast op een winkelwagen met een combinatie van verkoopartikelen en retourartikelen.

## <a name="total-discount-percent"></a>Totaal kortingspercentage

Met de bewerking **Totaal kortingspercentage** kunnen POS-gebruikers een kortingspercentage invoeren voor een transactie. Deze bewerking is alleen van toepassing op kortingsartikelen en heeft betrekking op de waarde van het **maximale totale kortingspercentage** dat is opgegeven in de POS-machtigingsgroep voor de gebruiker. Als het ingevoerde kortingspercentage hoger is dan het maximale totale kortingspercentage, wordt de bewerking geblokkeerd en wordt er geen machtiging overschrijvende stroom geactiveerd. Op dit moment kan een totaal kortingspercentage niet worden toegepast op een winkelwagen met een combinatie van verkoopartikelen en retourartikelen.

## <a name="remove-system-discounts-from-transaction"></a>Systeemkortingen verwijderen uit transactie

Met de bewerking **Systeemkortingen verwijderen uit transactie** kunnen POS-gebruikers alle toegepaste systeemkortingen (inclusief kortingen op basis van coupons) verwijderen uit een transactie. Nadat deze bewerking is uitgevoerd, sluit de prijsengine systeemkortingen uit van het kortingberekeningsbereik. Met de bewerking **Systeemkortingen verwijderen uit transactie** worden geen handmatige kortingen verwijderd.

## <a name="reapply-system-discounts"></a>Systeemkortingen opnieuw toepassen

Met de bewerking **Systeemkortingen opnieuw toepassen** kunnen POS-gebruikers berekende kortingen opnieuw gebruiken voor een transactie als de kortingen zijn verwijderd met de bewerking **Systeemkortingen verwijderen uit transactie**. Nadat deze bewerking is uitgevoerd, neemt de prijsengine systeemkortingen op in het kortingberekeningsbereik.

## <a name="add-coupon-code"></a>Couponcode toevoegen

Met de bewerking **Couponcode toevoegen** kunnen POS-gebruikers een coupon toevoegen aan een transactie door een couponcode in te voeren. Gebruikers kunnen ook de streepjescode van een coupon scannen of deze invoeren met behulp van het numerieke toetsenbord in het scherm **Transacties**.

## <a name="remove-coupon-code"></a>Couponcode verwijderen

Met de bewerking **Couponcode verwijderen** kunnen POS-gebruikers een of meer coupons selecteren en verwijderen die momenteel worden toegepast op een transactie.

## <a name="recalculate"></a>Opnieuw berekenen

Met de bewerking **Opnieuw berekenen** kunnen POS-gebruikers een prijsberekening op aanvraag activeren. Deze bewerking is vereist wanneer de prijsvergrendeling en/of uitgestelde prijsberekening is ingeschakeld en de POS-gebruiker de prijzen en kortingen opnieuw wil berekenen nadat de winkelwagen of order is gewijzigd. Met de bewerking **Opnieuw berekenen** wordt de gehele order altijd opnieuw berekend. De bewerking kan niet worden gebruikt om geselecteerde verkoopregels opnieuw te berekenen. Als u handmatige kortingen wilt toepassen op een vergrendelde verkoopregel in POS, moeten POS-gebruikers eerst de bewerking **Opnieuw berekenen** gebruiken om alle verkoopregels te ontgrendelen.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
