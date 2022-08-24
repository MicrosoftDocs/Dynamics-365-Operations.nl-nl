---
title: Een variantgroep maken
description: In dit artikel wordt beschreven hoe u een maat-, stijl- of kleurvariantgroep kunt maken voor een product in Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
ms.openlocfilehash: 507076259c2d9dfe97a0e24d253b5ac0a8325fe2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270095"
---
# <a name="create-a-variant-group"></a>Een variantgroep maken


[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u een maat-, stijl- of kleurvariantgroep kunt maken voor een product in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Dynamics 365 Commerce ondersteunt meerdere varianten voor producten. Het is ideaal om variantgroepen voor verschillende productcategorieën in te stellen. U kunt bijvoorbeeld een maatgroep maken voor t-shirts met de maten extra small, small, medium, large en extra large, of een kleurgroep maken om alle beschikbare kleuren van een product op te nemen. U moet variantgroepen toevoegen voordat u producten toevoegt.

In dit artikel wordt een maatgroep gemaakt en geconfigureerd. Vergelijkbare procedures kunnen worden gebruikt voor het toevoegen en configureren van stijlgroepen en kleurgroepen.

## <a name="create-a-size-group"></a>Een maatgroep maken

Volg deze stappen om een maatgroep te maken.
 
1. Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Producten en categorieën \> Variantgroepen \> Maatgroepen**.
1. Selecteer **Nieuw** in het actievenster.
1. Voer in het vak **Maatgroep** een unieke naam voor de maatgroep in.
1. Voer in het vak **Omschrijving** een passende beschrijving in.
1. Selecteer **Opslaan** in het actievenster.

## <a name="add-attributes-to-the-size-group"></a>Kenmerken toevoegen aan de maatgroep

Volg deze stappen om kenmerken aan een maatgroep toe te voegen.

1. Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Producten en categorieën \> Variantgroepen \> Maatgroepen**
1. Selecteer een maatgroep in het navigatievenster.
1. Selecteer **Toevoegen** onder **Maatgroepregels**.
1. Voer in het vak **Maat** een tekenreeks die staat voor de maat (bijvoorbeeld 'XL').
1. Voer in het vak **Maatnaam** een naam in voor de maat (bijvoorbeeld 'Extra Large').
1. Voer in het vak **Aanvullingsgewicht** een getal in dat staat voor het aanvullingsgewicht.
1. Voer in het vak **Getal in streepjescode** een getal in dat staat voor de streepjescode.
1. Voer in het vak **Weergavevolgorde** een getal voor de weergavevolgorde in.
1. Selecteer **Opslaan** in het actievenster wanneer u klaar bent met het toevoegen van maten.

De volgende afbeelding toont een voorbeeld van een maatgroep voor 'hemdmaten'.

![Een maatgroep maken.](media/Size-Groups.png)

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van Productgegevens](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[Detailhandelproducten instellen](set-up-retail-products.md)

[Productdimensies](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
