---
title: Navigatiemenumodule
description: In dit artikel worden navigatiemenumodules beschreven en wordt aangegeven hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: d2ac2bcf4324f2386c97fbf264c076062e6f304c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852740"
---
# <a name="navigation-menu-module"></a>Navigatiemenumodule

[!include [banner](includes/banner.md)]

In dit artikel worden navigatiemenumodules beschreven en wordt aangegeven hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

Het belangrijkste doel van navigatiemenumodules is om sitegebruikers in staat te stellen te bladeren naar producten en sitepagina's op basis van de kanaalnavigatiehiërarchie die is gedefinieerd in Dynamics 365 Commerce Headquarters. Items die in een navigatiemenumodule zijn geconfigureerd, worden weergegeven als navigatie in de koptekst van de site. Navigatiemenumodules bieden ook ondersteuning voor statische menuonderwerpen die zijn gekoppeld aan andere pagina's op een e-Commerce-site.

De navigatiemenumodule kan worden toegevoegd aan de koptekstmodule van een pagina. In het Fabrikam-thema worden standaard twee niveaus weergegeven in het navigatiemenu. In het Starter-thema worden standaard drie niveaus weergegeven in het navigatiemenu. Als u het aantal niveaus wilt wijzigen, is een weergave-extensie vereist voor het thema.

In de volgende afbeelding ziet u een voorbeeld van een navigatiemenu voor de Fabrikam-site met twee niveaus voor de categoriehiërarchie en enkele statische menuopdrachten.
![Voorbeeld van een navigatiemenumodule.](./media/ecommerce-header.png)

## <a name="navigation-menu-module-properties"></a>Eigenschappen van navigatiemenumodule

| Naam van eigenschap.             | Waarde                 | Beschrijving |
|---------------------------|-----------------------|-------------|
| Bron                  | **Detailhandel**, **Handmatig ontwerp**, **Detailhandel en handmatig ontwerp** | Met de waarde **Detailhandel** kan de kanaalnavigatiehiërarchie uit Commerce Headquarters worden weergegeven in het navigatiemenu. Met **Handmatig ontwerp** kunnen statische menuopdrachten worden opgesteld. Bij **Detailhandel en handmatig ontwerp** is een combinatie van beide mogelijk. |
| Categorieafbeeldingen weergeven | **True** of **False**    | Als deze eigenschap is ingeschakeld, worden in het navigatiemenu categorieafbeeldingen weergegeven die voor elke categorie zijn gedefinieerd in Commerce Headquarters. Toegevoegd in Commerce-release 10.0.14. |
| Reclameafbeeldingen weergeven | **True** of **False** | Wanneer deze eigenschap is ingeschakeld, kunnen promoties worden geconfigureerd met afbeeldingen, koppelingen en tekst. Deze eigenschap is toegevoegd in de Commerce-versie 10.0.17. |
|Categorie voor promotie-inhoud toevoegen | Tekst, afbeelding of koppeling | Wanneer de eigenschap **Reclameafbeeldingen weergeven** is ingeschakeld, kunt u tekst, een afbeelding of een koppeling als promotie-inhoud toevoegen aan het navigatiemenu. |
| Navigatiemenu met meerdere niveaus inschakelen | **True** of **False** | Wanneer deze eigenschap is ingeschakeld, kunnen in het navigatiemenu meerdere niveaus van de navigatiehiërarchie worden weergegeven. Deze functie is beschikbaar in de Commerce-versie 10.0.15. |
| Aantal niveaus | geheel getal | Met deze eigenschap wordt het aantal niveaus bepaald dat moet worden weergegeven als de eigenschap **Navigatiemenu met meerdere niveaus inschakelen** is ingesteld op **Waar**. |
| Statische menuopdracht| Matrix met waarden| Statische menuonderwerpen die de naam van een menuopdracht koppelen aan een statische sitepagina. U kunt menuonderwerpen maken onder andere menuopdrachten. Statische menu's worden standaard weergegeven op het hoofdniveau en worden toegevoegd aan de kanaalnavigatiehiërarchie als deze bestaat. |
| Hoofdmenu weergeven | **True** of **False** | Wanneer deze eigenschap is ingeschakeld, kan het navigatiemenu onder een aangepast hoofdniveau worden gedefinieerd (bijvoorbeeld **Nu winkelen**). Deze functie is beschikbaar in Dynamics 365 Commerce versie 10.0.15. |
| Hoofdmenu | tekenreeks | Deze eigenschap kan worden gebruikt om tekst voor een aangepast hoofdniveau te definiëren als de eigenschap **Hoofdmenu weergeven** is ingesteld op **Waar**. |

In de volgende afbeelding ziet u een voorbeeld van een categorieafbeelding die wordt weergegeven in het navigatiemenu voor de site van Fabrikam.
![Voorbeeld van een navigatiemenumodule met categorieafbeeldingen.](./media/ecommerce-categoryimages.PNG)

## <a name="add-a-navigation-menu-module-to-a-header-module"></a>Een navigatiemenumodule aan een koptekstmodule toevoegen

Zie [Koptekstmodule](author-header-module.md) voor meer informatie over het toevoegen van een navigatiemenumodule aan een koptekstmodule.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Breadcrumb-module](add-breadcrumb.md)

[Siteselectiemodule](site-selector.md)

[Module met vakje voor kopen](add-buy-box.md)

[Conformiteit van cookie](cookie-compliance.md)

[Koptekstmodule](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
