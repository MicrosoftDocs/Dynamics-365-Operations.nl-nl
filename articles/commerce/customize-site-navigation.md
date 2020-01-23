---
title: Sitenavigatie aanpassen
description: In dit onderwerp wordt beschreven hoe u een aangepaste online navigatiehiërarchie kunt maken om uw producten te ordenen op uw Microsoft Dynamics 365 Commerce-site.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 642cb5c145dec68631eb9ab27d926ba8ab75c59b
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914905"
---
# <a name="customize-site-navigation"></a>Sitenavigatie aanpassen

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een aangepaste online navigatiehiërarchie kunt maken om uw producten te ordenen op uw Microsoft Dynamics 365 Commerce-site.

## <a name="overview"></a>Overzicht

Met online winkels kunnen klanten producten bekijken en bladeren door middel van productcategorieën. Deze functie wordt meestal geboden door tabbladen boven aan de pagina of door een navigatiebalk aan de linkerkant. In Dynamics 365 Commerce maakt en beheert u de hiërarchiestructuur van uw categorienavigatie en de producten die in de verschillende categorieën zijn opgenomen.

## <a name="create-a-retail-channel-navigation-hierarchy"></a>Een navigatiehïerarchie voor uw detailhandelafzetkanaal maken

Voer de volgende stappen uit om een navigatiehiërarchie voor uw detailhandelafzetkanaal te maken.

1. Ga naar **Detailhandel \> Producten en categorieën \> Categorie- en productbeheer**.
1. Selecteer **Categoriehiërarchieën**en vervolgens **Nieuw**.
1. Geef de hiërarchie een naam.

    > [!NOTE]
    > De bovenste categorie die u maakt, is het hoofdknooppunt voor de categorie. Deze wordt niet weergegeven op de site. Als u een categoriehiërarchie wilt maken waarin één knooppunt op het hoogste niveau wordt weergegeven op uw site, maakt u de categorie en geeft u deze een naam als een onderliggend element van de hoofdcategorie.

1. Selecteer **Nieuw categorieknooppunt** en geef de categorie een naam.
1. Ga verder met het maken van categorieën op hetzelfde en het onderliggende niveau als nodig is.

U kunt nu producten toewijzen aan elke categorie die u hebt gemaakt onder de categorie op het hoogste niveau.

## <a name="customize-the-order-of-categories"></a>De volgorde van categorieën aanpassen

De categorieën die u definieert, worden standaard in alfabetische volgorde op de site weergegeven. U kunt echter ook de weergavevolgorde van categorieën aanpassen.

## <a name="assign-a-category-hierarchy-type"></a>Wijs een categoriehiërarchietype toe

1. Ga naar **Detailhandel \> Producten en categorieën \> Categorie- en productbeheer**.
1. Selecteer **Categoriehiërarchieën**.
1. Selecteer in het Actievenster op het tabblad **Categoriehiërarchie** in de groep **Instellen** de optie **Gekoppeld hiërarchietype**.
1. Selecteer **Nieuw**.
1. Selecteer **Navigatiehiërarchie voor detailhandelafzetkanaal** in het veld **Categoriehiërarchietype**.
1. Selecteer in het veld **Categoriehiërarchie** de afzetkanaalnavigatiehiërarchie die u eerder hebt gemaakt.

## <a name="publish-new-or-updated-navigation-hierarchies"></a>Nieuwe of bijgewerkte navigatiehiërarchieën publiceren

Voer de volgende stappen uit om de navigatiehiërarchie beschikbaar te maken voor uw online winkel.

1. Ga naar **Detailhandel \> Kanaalinstellingen \> Kanaalcategorieën en productkenmerken**.
1. Selecteer uw online winkel in de structuur aan de linkerkant.
1. Selecteer **Afzetkanaalupdates publiceren**.
1. Klik op **Detailhandel \> IT detailhandel \> Distributieplanning**.
1. Zoek en selecteer in de lijst **Taak 1040**.
1. Selecteer **Nu uitvoeren**.
1. Herhaal stap 5 en 6 voor de projecten 1070 en 1150.

## <a name="show-categories-on-your-site"></a>Categorieën op uw site weergeven

Als u de categoriehiërarchie wilt weergeven in uw online winkel, moet u de navigatiemenumodule toevoegen aan de desbetreffende locatie in een sjabloon of fragment. Vervolgens wordt de navigatiehiërarchie in de navigatiemenumodule weergegeven, als u uw navigatiehiërarchie voor de detailhandel hebt gepubliceerd in het afzetkanaal waaraan uw site is gekoppeld.

> [!NOTE]
> Met de navigatiemenumodule die is opgenomen in het startpakket voor winkels kunnen gebruikers alleen navigeren naar categorieën zonder subcategorieën. Als u wilt dat uw klanten kunnen navigeren naar categorieën met subcategorieën, moet u de navigatiemenumodule aanpassen.

## <a name="add-custom-navigation-options"></a>Aangepaste navigatieopties toevoegen

In het navigatiemenu kunt u navigatieopties toevoegen die geen deel uitmaken van de productcategoriehiërarchie. Aan het einde van de lijst met productcategorieën kunt u bijvoorbeeld een item **Contact opnemen** toevoegen dat verwijst naar een contactpagina die u voor uw site hebt gemaakt.

Voer de volgende stappen uit om aangepaste navigatieopties aan het navigatiemenu toe te voegen.

1. Selecteer in de sjabloon of het fragment dat u wilt aanpassen de navigatiemenumodule.
1. Ga naar het tabblad **Gegevens** in het eigenschappenvenster en selecteer **Item toevoegen** om een nieuw CMS-navigatie-item (Content Management System) te maken.
1. Geef de koppelingstekst en een URL op.
1. Herhaal stap 2 en 3 om meer aangepaste navigatieopties toe te voegen.
1. Wanneer u klaar bent, slaat u de sjabloon of het fragment op en checkt u het in.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht sjablonen en indelingen](templates-layouts-overview.md)

[Werken met sjablonen](work-with-templates.md)

[Werken met vooraf ingestelde indelingen](work-with-layouts.md)

[Werken met fragmenten](work-with-fragments.md)

[Werken met modules](work-with-modules.md)

[Een pagina-URL maken](create-page-url.md)

[Werken met publicatiegroepen](publish-groups.md)
