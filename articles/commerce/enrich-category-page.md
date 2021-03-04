---
title: Een landingspagina voor een categorie verrijken
description: In dit onderwerp wordt de verrijking van categoriepagina's in Dynamics 365 Commerce beschreven.
author: v-chgri
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ca31ec7d2eee7d2b0c863506338341a870ff07ee
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411377"
---
# <a name="enrich-a-category-landing-page"></a>Een landingspagina voor een categorie verrijken


[!include [banner](includes/banner.md)]

In dit onderwerp wordt de verrijking van categoriepagina's in Dynamics 365 Commerce beschreven.

## <a name="overview"></a>Overzicht

Commerce biedt een standaard landingspagina voor categorieën die wordt gebruikt wanneer categoriegegevens worden weergegeven. Een standaard categoriepagina bevat vereiste elementen, zoals verfijners, gecategoriseerde productplaatsing, sorteeropties, een keuzeoverzicht en pagineringsknoppen. 

In plaats van de standaardcategoriepagina te gebruiken kunt u echter een "verrijkte" categorielandingspagina gebruiken die meer inhoud en meer specifieke elementen bevat. Bij een speciale verrijking moet u bijvoorbeeld categoriespecifieke marketinginhoud toevoegen aan de categoriepagina. Deze inhoud kan betrekking hebben op plaatsing van producten in meerdere categorieën voor cross-sell doeleinden, redactionele lijsten, afbeeldingen, video's en andere tekst. U kunt de standaardcategoriepagina wijzigen of een andere categoriepagina definiëren voor een specifieke categorie.

![Verrijkte landingspagina voor categorie](./media/CategoryLandingPages.png)

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]