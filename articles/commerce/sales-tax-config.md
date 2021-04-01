---
title: Btw voor online orders configureren
description: Dit onderwerp biedt een overzicht van de selectie van btw-groepen voor verschillende typen online orders in Dynamics 365 Commerce.
author: gvrmohanreddy
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: 36dd3e8a3d47f02eed5b9c8bb79d773d98069376
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254836"
---
# <a name="configure-sales-tax-for-online-orders"></a>Btw voor online orders configureren

[!include [banner](includes/banner.md)]

Dit onderwerp biedt een overzicht van de selectie van btw-groepen voor verschillende typen online orders. 

Uw e-commercekanaal kan opties, zoals levering of ophalen, ondersteunen voor online bestellingen. De btw-toepasselijkheid is gebaseerd op de optie die door uw online gebruikers is geselecteerd. Wanneer een klant ervoor kiest een artikel online te kopen en het naar een adres wordt verzonden, wordt de btw bepaald op basis van de btw-groep voor de klant. Wanneer een klant een ingekocht artikel ophaalt in een winkel, wordt de btw bepaald op basis van de instelling van de btw-groep voor het ophalen in de winkel. 

## <a name="orders-shipped-to-a-customer-address"></a>Orders die naar een klantadres zijn verzonden 

In het algemeen wordt de btw voor online orders die naar klantadressen worden verzonden, gedefinieerd door de bestemming. Elke btw-groep bevat een btw-configuratie op basis van de detailhandel waaronder uw bedrijf bestemmingsgegevens kan definiëren, zoals land/regio, staat, regio en plaats in een hiërarchische vorm. Wanneer een online order wordt geplaatst, gebruikt de commerce-belastingservice het afleveradres van alle regelartikelen in de order en zoekt naar btw-groepen met dezelfde btw-criteria op basis van de bestemming. Voor een online order met het afleveradres voor het artikel naar San Francisco, Californië, wordt de btw-groep en btw-code voor Californië automatisch berekend en wordt de btw voor elk artikel dienovereenkomstig berekend.  

## <a name="customer-based-tax-groups"></a>Op klanten gebaseerde btw-groepen

In Commerce Headquarters zijn twee locaties waar btw-groepen voor klanten worden geconfigureerd:

- **Klantprofiel**
- **Het verzendadres van de klant**

### <a name="if-a-customers-profile-has-a-tax-group-configured"></a>Als het klantprofiel een btw-groep heeft geconfigureerd

Voor het profielrecord van een klant in Headquarters is het mogelijk een btw-groep te configureren, maar voor online orders wordt de btw-groep die in het profiel van een klant is geconfigureerd, niet gebruikt voor de belastingservice. 

### <a name="if-a-customers-shipping-address-has-a-tax-group-configured"></a>Als het verzendadres van de klant een btw-groep heeft geconfigureerd

Als voor de verzendadres van een klant een btw-groep is geconfigureerd en daar een online order (of artikel) naartoe wordt verzonden, wordt de btw-groep die is geconfigureerd in het adresrecord van de klant gebruikt door de belastingservice voor belastingberekeningen.

#### <a name="configure-a-tax-group-for-a-customers-shipping-address-record"></a>Een btw-groep configureren voor het verzendadres van een klant

Voer de volgende stappen uit om een btw-groep te configureren voor het verzendadres van een klant in Commerce Headquarters.

1. Ga naar **Alle klanten** en selecteer de gewenste klant. 
1. Selecteer op het sneltabblad **Adressen** het gewenste adres en selecteer vervolgens **Meer opties \> Geavanceerd**. 
1. Stel onder het tabblad **Algemeen** op de pagina **Adressen beheren** de btw-waarde naar wens in.

> [!NOTE]
> De btw-groep wordt gedefinieerd met behulp van het afleveradres van de orderregel en de op bestemming gebaseerde btw wordt geconfigureerd in de btw-groep zelf. Zie [Belastingen voor online winkels instellen op basis van de bestemming](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination) voor meer informatie.

## <a name="order-pickup-in-store"></a>Order ophalen in de winkel

Voor orderregels met ophalen in winkel of bij een afhaallocatie, wordt de btw-groep van de geselecteerde ophaalwinkel toegepast. Zie [Andere btw-opties voor winkels instellen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores) voor meer informatie over het configureren van de btw-groep voor een bepaalde winkel.

> [!NOTE]
> Wanneer een orderregel wordt opgenomen in een winkel, worden de btw-instellingen voor het adres van de klant (indien ingesteld) genegeerd door de belastingservice en wordt de btw-configuratie van de ophaalwinkel toegepast. 

## <a name="additional-resources"></a>Aanvullende bronnen

[Btw-overzicht](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[Btw-berekeningsmethoden in het veld Oorsprong](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[Btw-overeenkomst en -overschrijvingen](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[Berekeningsopties Volledige bedrag en interval voor btw-codes](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[Berekening van btw-vrijstelling](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]