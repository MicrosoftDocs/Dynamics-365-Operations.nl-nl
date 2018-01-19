---
title: Coupons voor detailhandelverkoop maken
description: In dit onderwerp vindt u een overzicht van detailhandelcoupons en uitleg over hoe u deze instelt.
author: scott-tucker
manager: AnnBe
ms.date: 05/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailCoupon, RetailParameters, RetailSharedParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.search.region: Global
ms.search.industry: retail
ms.author: scotttuc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7e05361bf865e44ba6073198fba94d7102b1ed19
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="create-coupons-for-retail-sales"></a>Coupons voor detailhandelverkoop maken

[!include[banner](includes/banner.md)]


## <a name="overview-of-coupons"></a>Overzicht van coupons

Coupons zijn codes en streepjescodes die worden gebruikt om detailhandelkortingen aan transacties toe te voegen. Elke coupon kan meerdere codes bevatten en elke code kan eigen geldigheidsdatums hebben. 

Elke coupon is gekoppeld aan één detailhandelkorting. De prijsgroepen die aan de korting zijn gekoppeld, definiëren de klanten die gebruik kunnen maken van een coupon of de afzetkanalen waarvoor een coupon geldig is. 

In wezen zijn coupons extra validatie naast de detailhandelkortingen. De coupon levert de couponcodes en de streepjescodes die vereist zijn, samen met de datumbereiken voor deze codes. De coupon biedt ook optioneel beperkingen voor gebruik en vereiste klanteigenschappen. De korting omvat de set van producten waarvoor de coupon geldig is. De prijsgroepen voor de korting omvatten de set van klanten, afzetkanalen of catalogi waarvoor de coupon geldig is.

Om een coupon te maken, maakt u de korting en de coupon afzonderlijk. U koppelt ze vervolgens door de korting te selecteren op de couponpagina in Microsoft Dynamics 365 for Retail. 

> [!NOTE]
> Nadat een coupon is gekoppeld aan een korting, worden verschillende velden op de kortingspagina in Microsoft Dynamics 365 for Retail alleen-lezen, omdat deze worden beheerd door de instellingen van de coupon. Deze velden zijn de velden voor de status en de standaarddatumbereiken.

### <a name="limited-use-coupons"></a>Coupons met gebruiksbeperkingen

Coupons kunnen worden geconfigureerd als coupons met gebruiksbeperkingen. Deze beperkingen kunnen worden gedefinieerd per klant of kanaal of als een algehele beperking. De beperking wordt toegepast wanneer de code of de streepjescode wordt ingevoerd of gescand in POS of tijdens het boeken van een verkooporder. Een coupon wordt vastgelegd als gebruikt wanneer een order is voltooid waaraan de coupon is gekoppeld.

De beperking wordt afgedwongen per couponcode op een coupon. Een coupon voor eenmalig gebruik met twee couponcodes kan bijvoorbeeld twee maal worden gebruikt: voor elke couponcode één keer. Elke code op een coupon kan afzonderlijk worden ingesteld om actief te zijn.

## <a name="managing-coupons"></a>Coupons beheren

U moet de korting en de coupon afzonderlijk aanmaken. U koppelt ze vervolgens door de korting op de couponpagina te selecteren. Nadat u een coupon koppelt aan een korting, worden verschillende velden voor de korting alleen-lezen, omdat deze worden beheerd door de instellingen van de coupon. Deze velden zijn de velden voor de status en de standaarddatumbereiken.  

In wezen zijn coupons nu extra validatie naast de detailhandelkortingen. De coupon levert de couponcodes en de streepjescodes die vereist zijn, samen met de datumbereiken, de gebruiksbeperkingen en de vereiste klanteigenschappen. De korting omvat de set van producten waarvoor de coupon geldig is. De prijsgroepen van de korting omvatten de set van klanten, afzetkanalen of catalogi waarvoor de coupon geldig is.

## <a name="system-setup-for-coupons"></a>Systeeminstellingen voor coupons 

Voordat u een coupon kunt instellen, moet u de streepjescode en twee nummerreeksen voor de coupon instellen. 

1.  Maak op de pagina **Maskertekens** een nieuw maskerteken voor de couponcode aan. U kunt elk niet-gebruikt teken kiezen.
2.  Op de pagina **Instellingen streepjescodemasker** maakt u een nieuw streepjescodemasker. Stel het veld **Type** in op **Coupon**.
3.  Op de pagina **Streepjescode-instellingen** maakt u een nieuwe streepjescode die gebruik maakt van het streepjescodemasker dat u zojuist hebt gemaakt.
4.  Op de pagina **Nummerreeksen** kunt u twee nieuwe nummerreeksen maken. Eén reeks is voor de couponcode-id en de andere reeks is voor het couponnummer. De couponcode-ID is de unieke id voor elke couponcode voor een coupon. Het couponnummer is de unieke identificatie voor een coupon. Elke coupon kan meerdere codes en streepjescodes bevatten, die de coupon triggeren.

    > [!NOTE]
    > U moet voor beide nummerreeksen het veld **Bereik** instellen op **Bedrijf**. In de meeste gevallen moet u beide volgnummers automatisch genereren.

5.  Selecteer op de pagina **Gedeelde parameters detailhandel** op het tabblad **Streepjescodes** de streepjescode die u eerder hebt gemaakt.
6.  Selecteer op de pagina **Detailhandelparameters** op het tabblad **Nummerreeksen** de nummerreeksen die u hebt gemaakt voor het couponnummer en de couponcode-id.
7.  U kunt nu de pagina **Coupons** openen en nieuwe coupons maken.

## <a name="the-effect-of-partial-updates-on-coupons"></a>Het effect van gedeeltelijke updates op coupons

De couponfunctionaliteit omvat meerdere afzonderlijke functies in Dynamics 365 for Retail. Microsoft Dynamics 365 for Retail headquarters (HQ) en het afzetkanaal kunnen gedeeltelijk worden bijgewerkt voor meerdere componenten. Het is daarom belangrijk dat u begrijpt hoe gedeeltelijke updates de couponfunctionaliteit als geheel beïnvloeden.

- **HQ wordt gedeeltelijk bijgewerkt, maar detailhandelserver en POS worden niet bijgewerkt.** In een HQ-update worden de pagina's Coupon en Korting bijgewerkt en de detailhandelprijsengine wordt ook bijgewerkt. Als slechts een van deze twee onderdelen wordt bijgewerkt, komen sommige pagina's in Retail niet overeen met de gegevens voor prijsberekening. Daardoor kunnen onverwachte kortingsberekeningen of -fouten optreden tijdens het berekenen van kortingen.
- **HQ wordt bijgewerkt, maar detailhandelserver en POS worden niet bijgewerkt (N-1).** Omdat niet alle winkels tegelijkertijd kunnen worden bijgewerkt, wordt aangeraden om HQ bij te werken voordat u de winkels bijwerkt. In het scenario N-1 is nieuwe functionaliteit die is gerelateerd aan coupons niet beschikbaar in winkels die nog niet zijn bijgewerkt. De couponfunctionaliteit kan bijvoorbeeld ' uitsluitings'-regels introduceren. Als u uitsluitingsregels gebruikt bij een korting, worden deze niet toegepast in een winkel die een oudere versie uitvoert.
- **HQ wordt niet bijgewerkt, maar detailhandelserver en POS worden wel bijgewerkt (N+1).** Omdat de bijgewerkte prijsengine in detailhandelserver oudere kortingscodes kan verwerken tijdens prijsberekeningen, zou de update geen functionele invloed moeten hebben in dit scenario.

