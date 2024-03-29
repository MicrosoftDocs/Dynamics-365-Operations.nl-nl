---
title: Een productpagina verrijken
description: In dit artikel wordt beschreven hoe u een productpagina verrijkt in Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: f01dcc2518fe861339b4984522582ed3de7aa6ad
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282129"
---
# <a name="enrich-a-product-page"></a>Een productpagina verrijken

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u een productpagina verrijkt in Microsoft Dynamics 365 Commerce.

Standaard gebruikt uw site een algemene pagina om productgegevens weer te geven. Deze pagina bevat de basisgegevens over het product en de besturingselementen die nodig zijn om het product te verkopen. U kunt echter de informatie van de Commerce Scale Unit aanvullen met extra afbeeldingen of tekst voor een specifiek product. Dit proces wordt het verrijken van de productpagina genoemd.

In veel gevallen zult u specifieke aanvullende inhoud voor uw producten willen gebruiken. Wanneer u naar **Retail en Commerce** gaat in het ontwerpprogramma, ziet u een lijst met producten uit het afzetkanaal dat aan de site is toegewezen. In deze lijst geeft de kolom **Verrijkt** aan of de productpagina voor een product is verrijkt. Als er een vinkje in de kolom staat, bestaat er een verrijkte product pagina voor het product. Als er geen vinkje wordt weergegeven, worden de standaard productpagina en -inhoud voor het product gebruikt. U kunt zowel verrijkte als niet-verrijkte productpagina's voorvertonen door een productnaam in de lijst te selecteren.

## <a name="enrich-a-product-page"></a>Een productpagina verrijken

Volg deze stappen om een productpagina te verrijken.

1. Selecteer onder **Sites** de naam **Fabrikam** (of de naam van uw site).
1. Selecteer **Producten** in het navigatievenster aan de linkerkant.
1. Selecteer een product dat geen verrijkte productpagina heeft.
1. Selecteer **Een productpagina verrijken** in het actievenster.
1. Selecteer **PDP-sjabloon** en vervolgens **OK**.
1. Vouw in de overzichtsstructuur aan de linkerkant het vak **Hoofd** uit.
1. Selecteer de knop met het weglatingsteken (**...**) voor het vak **Hoofd** en selecteer **Module toevoegen**.
1. Selecteer **Container 2** en vervolgens **OK**.
1. Selecteer de knop met het weglatingsteken voor **Container 2** en selecteer **Module toevoegen**.
1. Selecteer **Functie** en vervolgens **OK**.
1. Voer in het deelvenster Eigenschappen rechts in het veld **Rich Text** de bijgewerkte omschrijving van het product in.
1. Voer in het veld **Koptekst** een koptekst in en selecteer vervolgens **OK**.
1. Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.
1. Voer in het veld **Opmerkingen** **Een product verrijkt** in en selecteer vervolgens **OK**.
1. Als u een verrijkte pagina wilt weergeven, selecteert u **Voorbeeld**. Wanneer u klaar bent, sluit u het tabblad Voorbeeld om terug te keren naar het ontwerpgereedschap.
1. Selecteer **Publiceren**.

## <a name="additional-resources"></a>Aanvullende resources

[Een bestaande sitepagina wijzigen](modify-existing-page.md)

[Een nieuwe sitepagina toevoegen](add-new-page.md)

[Pagina-indelingen selecteren](select-page-layouts.md)

[Metagegevens SEO beheren](manage-seo-metadata.md)

[Een pagina opslaan, voorvertonen en publiceren](save-preview-publish-page.md)

[Een landingspagina voor een categorie verrijken](enrich-category-page.md)

[Toegankelijkheid van pagina-inhoud controleren](verify-accessibility.md)

[Dynamische e-commercepagina's maken op basis van URL-parameters](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
