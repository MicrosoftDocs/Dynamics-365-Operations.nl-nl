---
title: Een nieuw product maken in Commerce
description: In dit onderwerp wordt beschreven hoe u een nieuw product maakt in Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: cb0137468d690649abb18b9d19673ff740d52e5d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207914"
---
# <a name="create-a-new-product-in-commerce"></a>Een nieuw product maken in Commerce


[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een nieuw product maakt in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Een product wordt voornamelijk gedefinieerd door een productnummer, -naam en -beschrijving. Andere gegevens zijn echter ook vereist om een product of service te beschrijven:

## <a name="create-a-new-product"></a>Een nieuw product maken

1. Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Producten en categorieën \> Producten per categorie**.
1. Selecteer **Nieuw** in het actievenster.
1. Selecteer in vervolgkeuzelijst **Producttype** de optie **Artikel** of **Service**.
1. Selecteer in de vervolgkeuzelijst **Productsubtype** de optie **Product** (als het product geen varianten heeft) of **Productmodel** (als het product varianten heeft).
1. Voer in het vak **Productnummer** een productnummer in als dat nog niet is ingevuld.
1. Voer in het vak **Productnaam** een productnaam in.
1. Voer in het vak **Zoeknaam** een zoeknaam in.
1. Selecteer in de vervolgkeuzelijst **Retail-categorie** een geschikte categorie.
1. Als het product een kit is, selecteert u **Ja** bij **Productkit**.
1. Als het productsubtype productmodel is, stelt u de **Productdimensiegroep** zo in dat de ondersteunde varianten worden opgenomen. Opties zijn onder andere **Kleur**, **Grootte**, **Stijl** en **Configuratie**. Mogelijk moet u extra productdimensiegroepen maken.
1. Selecteer in de vervolgkeuzelijst **Configuratietechnologie** een geschikte optie.
1. Selecteer **OK**.

De volgende afbeelding toont een voorbeeldproduct dat wordt toegevoegd.

![Een product maken](media/create-new-product.png)

Wanneer een product wordt toegevoegd, kunt u er extra gegevens voor instellen, zoals **Productbeschrijving**, **Variantgroepen**, **Dimensiegroepen**, **Productkenmerken** en **Gerelateerde producten**.

In de volgende afbeelding ziet u de aanvullende gegevens van een product.

![Productgegevens](media/create-new-product-2.png)

### <a name="create-product-variants"></a>Productvarianten maken

Als het productsubtype **Productmodel** is, moeten er specifieke varianten worden gemaakt. 

Volg deze stappen om productvarianten te maken.

1. Selecteer **Productvarianten** in het actievenster.
1. Als er variantgroepen in het actievenster zijn geselecteerd, selecteert u **Variantsuggesties*.
1. Selecteer de varianten die u voor het product wilt ondersteunen.
1. Selecteer **Maken**.

## <a name="release-a-product"></a>Een product vrijgeven

Om een product te verkopen, moet het eerst aan een rechtspersoon worden vrijgegeven.

1. Selecteer **Producten vrijgeven** op de productpagina.

    ![Product vrijgeven](media/create-new-product-3.png)

1. Selecteer het product dat u wilt vrijgeven en selecteer **Volgende**.

    ![Producten kiezen om vrij te geven](media/create-new-product-4.png)

1. Selecteer de set productvarianten die u wilt vrijgeven en selecteer **Volgende**.

    ![Productvarianten kiezen om vrij te geven](media/create-new-product-5.png)

1. Selecteer de rechtspersoon en selecteer **Volgende**.

    ![Rechtspersoon kiezen](media/create-new-product-6.png)

1. Selecteer **Voltooien**.

    ![Productvrijgave voltooien](media/create-new-product-7.png)

## <a name="configure-a-released-product"></a>Een vrijgegeven product configureren

Nadat een product is vrijgegeven, is er verdere configuratie nodig, zoals het toevoegen van een prijs aan het product.

1. Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Producten en categorieën \> Vrijgegeven producten per categorie**.
1. Selecteer het productcategorieknooppunt voor het product dat is vrijgegeven en selecteer het product in de productenlijst.
1. Selecteer **Bewerken** in het actievenster.
1. Configureer in de sectie **Inkoop** eventuele vereiste eigenschappen, zoals **Eenheid**, **Prijs** en **Hoeveelheid**.
1. Selecteer **Valideren** in het actievenster om ervoor te zorgen dat er geen fouten worden gemeld voor ontbrekende velden.
1. Selecteer **Opslaan** in het actievenster.

In de volgende afbeelding ziet u een voorbeeldconfiguratie voor een vrijgegeven product.

![Een vrijgegeven product configureren](media/create-new-product-8.png)

## <a name="additional-resources"></a>Aanvullende resources

[Rechtspersonen maken](channels-legal-entities.md)

[Een variantgroep maken](create-variant-group.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]