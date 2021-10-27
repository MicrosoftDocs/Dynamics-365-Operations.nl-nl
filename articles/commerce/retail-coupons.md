---
title: Coupons voor detailhandelverkoop instellen
description: In dit onderwerp vindt u een overzicht van coupons en uitleg over hoe u deze instelt in Dynamics 365 Commerce.
author: josaw1
ms.date: 10/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailCoupon, RetailParameters, RetailSharedParameters
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 6a2ee38139f20b883bdfa5f0776951246f763f5f
ms.sourcegitcommit: f699dbc21a06dbfb3fb299b789b428ea8d643868
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/05/2021
ms.locfileid: "7603118"
---
# <a name="set-up-coupons-for-retail-sales"></a>Coupons voor detailhandelverkoop instellen

[!include [banner](includes/banner.md)]

## <a name="overview-of-coupons"></a>Overzicht van coupons

Coupons zijn codes en streepjescodes die worden gebruikt om kortingen aan transacties toe te voegen. Elke coupon kan meerdere codes bevatten en elke code kan eigen geldigheidsdatums hebben.

Elke coupon is gekoppeld aan één korting. De prijsgroepen die aan de korting zijn gekoppeld, definiëren de klanten die gebruik kunnen maken van een coupon of de afzetkanalen waarvoor een coupon geldig is.

In wezen zijn coupons extra validatie naast de kortingen. De coupon levert de couponcodes en de streepjescodes die vereist zijn, samen met de datumbereiken voor deze codes. De coupon biedt ook optioneel beperkingen voor gebruik en vereiste klanteigenschappen. De korting omvat de set van producten waarvoor de coupon geldig is. De prijsgroepen voor de korting omvatten de set van klanten, afzetkanalen of catalogi waarvoor de coupon geldig is.

Om een coupon te maken, maakt u de korting en de coupon afzonderlijk. U koppelt ze vervolgens door de korting op de couponpagina te selecteren in Commerce.

> [!NOTE]
> Nadat een coupon is gekoppeld aan een korting, worden verschillende velden op de kortingspagina in Commerce alleen-lezen, omdat deze worden beheerd door de instellingen van de coupon. Deze velden zijn de velden voor de status en de standaarddatumbereiken.
> 
> Wanneer u de coupon in het callcenterkanaal gebruikt, moet u de knop **Opnieuw berekenen** selecteren **(tabblad Verkopen > Berekenen > Herberekenen)** om de korting die aan het coupon is gekoppeld, toe te staan. Deze extra stap wordt in een toekomstige versie verwijderd.

Als u een coupon wilt toepassen op een verkooptransactie in POS, kunt u **Couponcode** of **Streepjescode van coupon** gebruiken. Als u de **couponcode** wilt gebruiken, moet de bewerking **Couponcode toevoegen** worden geconfigureerd in de [schermindeling](pos-screen-layouts.md) **Transactie** van POS. Selecteer **Couponcode toevoegen** en voer de couponcode in. Als u **Streepjescode van coupon** wilt gebruiken, scant u de streepjescode of voert u de streepjescode in met het numerieke toetsenbord in het scherm **Transactie**.

### <a name="limited-use-coupons"></a>Coupons met gebruiksbeperkingen

Coupons kunnen worden geconfigureerd als coupons met gebruiksbeperkingen. Deze beperkingen kunnen worden gedefinieerd per klant of kanaal of als een algehele beperking. De beperking wordt toegepast wanneer de code of de streepjescode wordt ingevoerd of gescand in POS of tijdens het boeken van een verkooporder.

De beperking wordt afgedwongen per couponcode op een coupon. Een coupon voor eenmalig gebruik met twee couponcodes kan bijvoorbeeld twee maal worden gebruikt: voor elke couponcode één keer. Elke code op een coupon kan afzonderlijk worden ingesteld om actief te zijn.

De coupons kunnen voor elk verkoopkanaal worden gebruikt, maar voor callcenterorders kunnen de coupons met gebruiksbeperkingen alleen worden gebruikt voor callcentersorders waarvoor de instelling **Ordervoltooiing** voor het callcenter is ingeschakeld. Als dit niet is ingeschakeld, kunnen alleen coupons zonder gebruiksbeperkingen worden gebruikt in callcenterorders.

> [!NOTE]
> Zodra een couponcode de gebruikslimiet heeft bereikt, wordt de status van de couponcode *niet* automatisch gewijzigd in Gebruikt. De gebruikslimiet van de couponcode is echter bereikt en kan niet worden gebruikt. Als de status van een couponcode handmatig is ingesteld op iets anders dan **Actief**, kan deze couponcode niet worden gebruikt in een kanaal.  

## <a name="managing-coupons"></a>Coupons beheren

U moet de korting en de coupon afzonderlijk aanmaken. U koppelt ze vervolgens door de korting op de couponpagina te selecteren. Nadat u een coupon koppelt aan een korting, worden verschillende velden voor de korting alleen-lezen, omdat deze worden beheerd door de instellingen van de coupon. Deze velden zijn de velden voor de status en de standaarddatumbereiken.

In wezen zijn coupons nu extra validatie naast de kortingen. De coupon levert de couponcodes en de streepjescodes die vereist zijn, samen met de datumbereiken, de gebruiksbeperkingen en de vereiste klanteigenschappen. De korting omvat de set van producten waarvoor de coupon geldig is. De prijsgroepen van de korting omvatten de set van klanten, afzetkanalen of catalogi waarvoor de coupon geldig is.

## <a name="system-setup-for-coupons"></a>Systeeminstellingen voor coupons

Voordat u een coupon kunt instellen, moet u de streepjescode en twee nummerreeksen voor de coupon instellen.

1. Maak op de pagina **Maskertekens** een nieuw maskerteken voor de couponcode aan. U kunt elk niet-gebruikt teken kiezen.
2. Op de pagina **Instellingen streepjescodemasker** maakt u een nieuw streepjescodemasker. Stel het veld **Type** in op **Coupon**.
3. Op de pagina **Streepjescode-instellingen** maakt u een nieuwe streepjescode die gebruik maakt van het streepjescodemasker dat u zojuist hebt gemaakt.
4. Op de pagina **Nummerreeksen** kunt u twee nieuwe nummerreeksen maken. Eén reeks is voor de couponcode-id en de andere reeks is voor het couponnummer. De couponcode-ID is de unieke id voor elke couponcode voor een coupon. Het couponnummer is de unieke identificatie voor een coupon. Elke coupon kan meerdere codes en streepjescodes bevatten, die de coupon triggeren.

    > [!NOTE]
    > U moet voor beide nummerreeksen het veld **Bereik** instellen op **Bedrijf**. In de meeste gevallen moet u beide volgnummers automatisch genereren.

5. Selecteer op de pagina **Commerce-parameters** op het tabblad **Streepjescodes** de streepjescode die u eerder hebt gemaakt.
6. Selecteer op de pagina **Gedeelde Commerce-parameters** op het tabblad **Nummerreeksen** de nummerreeksen die u hebt gemaakt voor het couponnummer en de couponcode-id.
7. U kunt nu de pagina **Coupons** openen en nieuwe coupons maken.

## <a name="the-effect-of-partial-updates-on-coupons"></a>Het effect van gedeeltelijke updates op coupons

De couponfunctionaliteit omvat meerdere afzonderlijke functies. Commerce Headquarters (HQ) en het afzetkanaal kunnen gedeeltelijk worden bijgewerkt voor meerdere componenten. Het is daarom belangrijk dat u begrijpt hoe gedeeltelijke updates de couponfunctionaliteit als geheel beïnvloeden.

- **HQ wordt gedeeltelijk bijgewerkt, maar Commerce Scale Unit en POS worden niet bijgewerkt.** In een HQ-update worden de pagina's Coupon en Korting bijgewerkt en de Commerce-prijsengine wordt ook bijgewerkt. Als slechts een van deze twee onderdelen wordt bijgewerkt, komen sommige pagina's in Commerce niet overeen met de gegevens voor prijsberekening. Daardoor kunnen onverwachte kortingsberekeningen of -fouten optreden tijdens het berekenen van kortingen.
- **HQ wordt bijgewerkt, maar Commerce Scale Unit en POS worden niet bijgewerkt (N-1).** Omdat niet alle winkels tegelijkertijd kunnen worden bijgewerkt, wordt aangeraden om HQ bij te werken voordat u de winkels bijwerkt. In het scenario N-1 is nieuwe functionaliteit die is gerelateerd aan coupons niet beschikbaar in winkels die nog niet zijn bijgewerkt. De couponfunctionaliteit kan bijvoorbeeld uitsluitingsregels introduceren. Als u uitsluitingsregels gebruikt bij een korting, worden deze niet toegepast in een winkel die een oudere versie uitvoert.
- **HQ wordt niet bijgewerkt, maar Commerce Scale Unit en POS worden wel bijgewerkt (N+1).** Omdat de bijgewerkte prijsengine in Commerce Scale Unit oudere kortingscodes kan verwerken tijdens prijsberekeningen, zou de update geen functionele invloed moeten hebben in dit scenario.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
