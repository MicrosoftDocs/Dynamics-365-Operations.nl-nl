---
title: Een landingspagina voor een categorie verrijken
description: In dit artikel wordt de verrijking van categoriepagina's in Dynamics 365 Commerce beschreven.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: e3397ffee9b32f3d3efedea38255f88daee5233c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282156"
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
