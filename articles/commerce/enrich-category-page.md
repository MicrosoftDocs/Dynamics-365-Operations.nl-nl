---
title: Een landingspagina voor een categorie verrijken
description: In dit artikel wordt de verrijking van categoriepagina's in Dynamics 365 Commerce beschreven.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bfee3b09768fa19ab95c880d7f7cbf330a8c58d7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856959"
---
# <a name="enrich-a-category-landing-page"></a>Een landingspagina voor een categorie verrijken

[!include [banner](includes/banner.md)]

In dit artikel wordt de verrijking van categoriepagina's in Dynamics 365 Commerce beschreven.

Commerce biedt een standaard landingspagina voor categorieën die wordt gebruikt wanneer categoriegegevens worden weergegeven. Een standaard categoriepagina bevat vereiste elementen, zoals verfijners, gecategoriseerde productplaatsing, sorteeropties, een keuzeoverzicht en pagineringsknoppen. 

In plaats van de standaardcategoriepagina te gebruiken kunt u echter een "verrijkte" categorielandingspagina gebruiken die meer inhoud en meer specifieke elementen bevat. Bij een speciale verrijking moet u bijvoorbeeld categoriespecifieke marketinginhoud toevoegen aan de categoriepagina. Deze inhoud kan betrekking hebben op plaatsing van producten in meerdere categorieën voor cross-sell doeleinden, redactionele lijsten, afbeeldingen, video's en andere tekst. U kunt de standaardcategoriepagina wijzigen of een andere categoriepagina definiëren voor een specifieke categorie.

![Verrijkte landingspagina voor categorie.](./media/CategoryLandingPages.png)

In Commerce Site Builder bevat de pagina **Producten** een lijst met categorieën uit het afzetkanaal die aan de site zijn toegewezen. Als de **verrijkte** status voor een categoriepagina is geselecteerd, is deze categoriepagina verrijkt. Anders worden de standaard categoriepagina en de inhoud van de categorie gebruikt. U kunt zowel verrijkte als niet-verrijkte categoriepagina's voor een categorie voorvertonen door een categorienaam te selecteren.

Ga als volgt te werk om een categoriepagina te verrijken.

1. Selecteer op de pagina **Producten** de naam van de categorie waarvoor u de categoriepagina wilt verrijken. De standaard categoriepagina voor de geselecteerde categorie wordt geopend in de pagina-editor.
2. Selecteer **Categoriepagina verrijken**.
3. Selecteer een sjabloon voor de verrijkte categoriepagina. Als u alleen kleine wijzigingen aanbrengt, kunt u de standaard categoriepagina selecteren. Anders kunt u een specifieke sjabloon voor een categoriepagina selecteren. Wanneer u de sjabloon selecteert, wordt de pagina-editor geopend en wordt de geselecteerde sjabloon gebruikt om een nieuwe categoriepagina te maken voor de geselecteerde categorie. De pagina wordt uitgecheckt naar u en u kunt wijzigingen aanbrengen.

> [!NOTE]
> In modules die gebruikmaken van de categoriespecificatiegegevens, worden de gegevens uit de geselecteerde categorie gebruikt. De instellingen van de sjabloon die u selecteert, bepalen welke wijzigingen u kunt aanbrengen.

## <a name="additional-resources"></a>Aanvullende resources

[Een bestaande sitepagina wijzigen](modify-existing-page.md)

[Een nieuwe sitepagina toevoegen](add-new-page.md)

[Pagina-indelingen selecteren](select-page-layouts.md)

[Metagegevens SEO beheren](manage-seo-metadata.md)

[Een pagina opslaan, voorvertonen en publiceren](save-preview-publish-page.md)

[Een productpagina verrijken](enrich-product-page.md)

[Toegankelijkheid van pagina-inhoud controleren](verify-accessibility.md)

[Dynamische e-commercepagina's maken op basis van URL-parameters](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
