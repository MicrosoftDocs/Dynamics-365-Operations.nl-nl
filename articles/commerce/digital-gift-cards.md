---
title: Digitale geschenkbonnen voor e-commerce
description: In dit onderwerp wordt beschreven hoe digitale geschenkbonnen in de e-commerce-implementatie van Microsoft Dynamics 365 Commerce werken. Het bevat ook een overzicht van belangrijke configuratiestappen.
author: anupamar-ms
manager: annbe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 5a88bef72e13b7b0d948bfd7617cb1dbbcd9ce49
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982661"
---
# <a name="e-commerce-digital-gift-cards"></a>Digitale geschenkbonnen voor e-commerce

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

In dit onderwerp wordt beschreven hoe digitale geschenkbonnen in de e-commerce-implementatie van Microsoft Dynamics 365 Commerce werken. Het bevat ook een overzicht van belangrijke configuratiestappen.

In Dynamics 365 Commerce volgt de aankoop van digitale geschenkbonnen dezelfde stroom als de aankoop van andere producten in het systeem. U hoeft verder geen modules te configureren. Als er meerdere geschenkbonnen aan de winkelwagen worden toegevoegd, worden de geschenkbonartikelen niet samengevoegd op één verkoopregel. Dit gedrag is vereist omdat elke verkoopregel wordt gefactureerd met een apart geschenkbonnummer.

De aankoop van digitale geschenkbonnen wordt ondersteund in Dynamics 365 Commerce versie 10.0.16 en hoger.

De volgende afbeelding toont een voorbeeld van de productdetailpagina (PDP) voor een digitale geschenkbon op de e-commercesite van Fabrikam.

![Voorbeeld van een PDP voor een digitale geschenkbon op de e-commercesite van Fabrikam](./media/GiftcardPDP.PNG)

## <a name="turn-on-the-digital-gift-card-feature-in-commerce-headquarters"></a>De functie voor digitale geschenkbonnen in Commerce Headquarters inschakelen

De aankoopstroom voor digitale geschenkbonnen kan alleen in Dynamics 365 Commerce worden gebruikt als de functie **Geschenkbon aankopen op e-Commerce** in Commerce Headquarters is ingeschakeld. U kunt de functie vinden in de werkruimte **Functiebeheer** in Commerce Headquarters (zie de volgende afbeelding).

![Werkruimte Functiebeheer in Commerce Headquarters](./media/Featureflag.PNG)

## <a name="configure-a-digital-gift-card-in-commerce-headquarters"></a>Een digitale geschenkbon in Commerce Headquarters configureren

Digitale geschenkbonproducten moeten in Commerce Headquarters worden geconfigureerd. Het proces lijkt op dat voor andere producten. De volgende belangrijke stappen zijn echter specifiek voor de configuratie van geschenkbonnen voor aankoop. Zie [Een nieuw product in Commerce maken](create-new-product-commerce.md) voor meer informatie over het maken en configureren van producten.

- Wanneer u digitale geschenkbonproducten configureert in het dialoogvenster **Nieuw product**, stelt u het veld **Producttype** in op **Service**. (Als u het dialoogvenster wilt openen, gaat u naar **Retail and Commerce \> Producten en categorieën \> Producten per categorie** en selecteer **Nieuw**.) Voor producten van het type **Service** wordt niet gecontroleerd of er voorraad beschikbaar is voordat een order wordt geplaatst. Zie [Een nieuw product maken](create-new-product-commerce.md#create-a-new-product) voor meer informatie.
- Op de pagina **Commerce-parameters** moet op het tabblad **Boeking** het veld **Geschenkbonproduct** worden ingesteld op **Digitale geschenkbon** (zie de volgende illustratie). Zie [Ondersteuning voor externe geschenkbonnen](./dev-itpro/gift-card.md) als het product een externe geschenkbon is voor meer informatie.

    ![Veld Geschenkbonproduct in Commerce Headquarters](./media/PostGiftcard.png)

- Als een geschenkbon meerdere vooraf gedefinieerde bedragen moet ondersteunen (bijvoorbeeld $ 25, $ 50 en $ 100), moet de dimensie **Grootte** worden gebruikt om deze vooraf gedefinieerde bedragen in te stellen. Elk vooraf gedefinieerd bedrag wordt een variant. Zie [Productdimensies](https://docs.microsoft.com/dynamics365/supply-chain/pim/product-dimensions?toc=/dynamics365/retail/toc.json) voor meer informatie.
- Als klanten een aangepast bedrag voor een geschenkbon moeten kunnen opgeven, stelt u eerst een variant in die een aangepast bedrag toestaat. Open vervolgens het product vanuit de pagina **Vrijgegeven producten in categorie** en stel vervolgens op het sneltabblad **Commerce** het veld **Prijs intoetsen** in op **Moet geen prijs intoetsen** (zie de volgende illustratie). Met deze instelling wordt gegarandeerd dat klanten een prijs kunnen invoeren wanneer ze in een PDP door het product bladeren.

    ![Veld Prijs intoetsen Commerce Headquarters](./media/KeyInPrice.png)

- De leveringsmodus voor een digitale geschenkbon moet worden ingesteld op **Elektronisch**. Selecteer op de pagina **Leveringsmethoden** (**Retail and commerce \> Kanaal instellen \> Leveringsmethode**) de modus **Elektronisch** in het lijstdeelvenster en voeg het digitale geschenkbonproduct aan het raster op het sneltabblad **Producten** toe (zie de volgende illustratie). Zie [Leveringsmethoden instellen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery) voor meer informatie.

    ![Digitale geschenkbonproducten op de pagina Leveringsmethode in Commerce Headquarters](./media/ElectronicMode.PNG)

- Zorg ervoor dat er een online functionaliteitsprofiel is gemaakt en gekoppeld aan uw online winkel in Commerce Headquarters. Stel in het functionaliteitsprofiel de optie **Producten samenvoegen** in op **Ja**. Met deze instelling worden alle artikelen, behalve geschenkbonnen, samengevoegd. Zie [Een online functionaliteitsprofiel maken](online-functionality-profile.md) voor meer informatie.
- Om er zeker van te zijn dat klanten een e-mailbericht ontvangen nadat een geschenkbon is gefactureerd, maakt u een nieuw type e-mailmelding op de pagina **E-mailmeldingsprofielen** en stelt u het veld **Meldingstype voor e-mail** in op **Geschenkbon uitgeven**. Zie [Een e-mailmeldingsprofiel instellen](email-notification-profiles.md) voor meer informatie.

## <a name="add-product-images-to-the-commerce-site-builder-media-library"></a>Productafbeeldingen toevoegen aan de Mediabibliotheek van Commerce Site Builder

U moet productafbeeldingen voor digitale geschenkbonproducten toevoegen aan de Mediabibliotheek van Commerce Site Builder. Zorg ervoor dat de bestandsnamen van de afbeeldingsbestanden voor geschenkbonnen de naamgevingsconventies van de site voor productafbeeldingen volgen. Zie [Afbeeldingen uploaden](dam-upload-images.md) voor meer informatie.

## <a name="configure-a-custom-amount-for-a-digital-gift-card-in-commerce-site-builder"></a>Een aangepast bedrag configureren voor een digitale geschenkbon in Commerce Site Builder

Als een digitale geschenkbon geconfigureerd is voor een aangepast bedrag, moet dit gedrag ook worden ingeschakeld in de [module Aankoopvak](add-buy-box.md) die wordt gebruikt op de PDP's van uw site. De module Aankoopvak ondersteunt moduleconfiguratie om aangepaste bedragen mogelijk te maken. U kunt ook de minimum- en maximumbedragen definiëren die toegestaan zijn voor aangepaste bedragen.

Voer de volgende stappen uit om een aangepast bedrag te configureren voor een digitale geschenkbon in Commerce Site Builder.

1. Ga naar de module Aankoopvak die wordt gebruikt op de PDP's van uw site. Deze module kan in een fragment, in een sjabloon of op een pagina worden geïmplementeerd.
1. Selecteer **Bewerken**.
1. Schakel in het deelvenster Eigenschappen aan de rechterkant het selectievakje **Aangepaste prijs toestaan** in.
1. Optioneel: als u minimum- en maximumbedragen wilt definiëren voor aangepaste bedragen, voert u bedragen in onder **Minimumprijs** en **Maximumprijs**.
1. Selecteer **Bewerken voltooien** en vervolgens **Publiceren**.

## <a name="additional-resources"></a>Aanvullende bronnen

[Module met vakje voor kopen](add-buy-box.md)

[Kassamodule](add-checkout-module.md)

[Winkelwagenmodule](add-cart-module.md)

[Een nieuw product maken in Commerce](create-new-product-commerce.md)

[Leveringsmethoden instellen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Productdimensies](https://docs.microsoft.com/dynamics365/supply-chain/pim/product-dimensions?toc=/dynamics365/retail/toc.json)

[Een profiel voor e-mailmeldingen instellen](email-notification-profiles.md)

[Een online functionaliteitsprofiel maken](online-functionality-profile.md)

[Ondersteuning voor externe geschenkbonnen](./dev-itpro/gift-card.md)
