---
title: Navigatiemenumodule
description: In dit onderwerp worden navigatiemenumodules beschreven en wordt aangegeven hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 91239bd1db3f5819b7ad8d45ccfd8ab0d88b1b41
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817869"
---
# <a name="navigation-menu-module"></a>Navigatiemenumodule

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

In dit onderwerp worden navigatiemenumodules beschreven en wordt aangegeven hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Het belangrijkste doel van navigatiemenumodules is om sitegebruikers in staat te stellen te bladeren naar producten en sitepagina's op basis van de kanaalnavigatiehiërarchie die is gedefinieerd in Dynamics 365 Commerce Headquarters. Items die in een navigatiemenumodule zijn geconfigureerd, worden weergegeven als navigatie in de koptekst van de site. Navigatiemenumodules bieden ook ondersteuning voor statische menuonderwerpen die zijn gekoppeld aan andere pagina's op een e-Commerce-site.

De navigatiemenumodule kan worden toegevoegd aan de koptekstmodule van een pagina. In het Fabrikam-thema worden standaard twee niveaus weergegeven in het navigatiemenu. In het Starter-thema worden standaard drie niveaus weergegeven in het navigatiemenu. Als u het aantal niveaus wilt wijzigen, is een weergave-extensie vereist voor het thema.

In de volgende afbeelding ziet u een voorbeeld van een navigatiemenu voor de Fabrikam-site met twee niveaus voor de categoriehiërarchie en enkele statische menuopdrachten.
![Voorbeeld van een navigatiemenumodule](./media/ecommerce-header.png)

## <a name="navigation-menu-module-properties"></a>Eigenschappen van navigatiemenumodule

| Naam van eigenschap.             | Waarde                 | Beschrijving |
|---------------------------|-----------------------|-------------|
| Bron                  | **Detailhandel**, **Handmatig ontwerp**, **Detailhandel en handmatig ontwerp** | Met de waarde **Detailhandel** kan de kanaalnavigatiehiërarchie uit Commerce Headquarters worden weergegeven in het navigatiemenu. Met **Handmatig ontwerp** kunnen statische menuopdrachten worden opgesteld. Bij **Detailhandel en handmatig ontwerp** is een combinatie van beide mogelijk. |
| Categorieafbeeldingen weergeven | **True** of **False**    | Als deze eigenschap is ingeschakeld, worden in het navigatiemenu categorieafbeeldingen weergegeven die voor elke categorie zijn gedefinieerd in Commerce Headquarters. Toegevoegd in Commerce-release 10.0.14. |
| Statische menuopdracht| Matrix met waarden| Statische menuonderwerpen die de naam van een menuopdracht koppelen aan een statische sitepagina. U kunt menuonderwerpen maken onder andere menuopdrachten. Statische menu's worden standaard weergegeven op het hoofdniveau en worden toegevoegd aan de kanaalnavigatiehiërarchie als deze bestaat. |

In de volgende afbeelding ziet u een voorbeeld van een categorieafbeelding die wordt weergegeven in het navigatiemenu voor de site van Fabrikam.
![Voorbeeld van een navigatiemenumodule met categorieafbeeldingen](./media/ecommerce-categoryimages.PNG)

## <a name="add-a-navigation-menu-module-to-a-header-module"></a>Een navigatiemenumodule aan een koptekstmodule toevoegen

Zie [Koptekstmodule](author-header-module.md) voor meer informatie over het toevoegen van een navigatiemenumodule aan een koptekstmodule.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Module met vakje voor kopen](add-buy-box.md)

[Conformiteit van cookie](cookie-compliance.md)

[Koptekstmodule](author-header-module.md)
