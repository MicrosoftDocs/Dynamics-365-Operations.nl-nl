---
title: Voettekstmodule
description: In dit onderwerp wordt beschreven wat voettekstmodules zijn en hoe u ze ontwerpt in Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f8e0290b5af9d0c1fc9ad0279b0d7f81c9feb2fc
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001133"
---
# <a name="footer-module"></a>Voettekstmodule  


[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat voettekstmodules zijn en hoe u ze maakt in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

De voettekstmodule is een speciale container die wordt gebruikt voor het hosten van de modules die in de paginavoettekst worden weergegeven. De module kan bijvoorbeeld koppelingen bevatten naar verschillende pagina's in de site, zoals de pagina's **Contact opnemen** en **Winkelbeleid**.

## <a name="footer-module-properties"></a>Eigenschappen van voettekstmodule 

Net als de meeste containers ondersteunt een voettekstmodule de eigenschappen voor de kop en de breedte. Ook wordt het toevoegen van meerdere modules ondersteund voor voettekstcategorieën. Elke voettekstcategoriemodule die wordt toegevoegd, wordt weergegeven als een kolom in de voettekstmodule.

## <a name="modules-available-in-a-footer-module"></a>Modules die beschikbaar zijn in een voettekstmodule

**Voettekstitems**: een voettekstitemmodule kan een koptekst, een afbeelding en een koppeling bevatten. De koptekst kan zelfstandig of in combinatie met een afbeelding en een koppeling worden gebruikt. Elke koppeling in de voettekst kan zo worden geconfigureerd dat deze alleen tekst bevat (bijvoorbeeld koppelingen naar 'Contact opnemen' en 'Privacy'), of dat deze zowel tekst als een afbeelding bevat (bijvoorbeeld koppelingen voor sociale media).

**Terug naar boven**: een terug naar boven-module bevat een koppeling voor een snelle navigatie naar de bovenkant van de pagina. Er is een bestemming vereist. De standaard bestemmingswaarde is #, waarmee de gebruiker naar bovenkant van de pagina gaat.

## <a name="author-a-footer-module"></a>Een voettekstmodule ontwerpen

1. Selecteer **Fragmenten** in het navigatievenster en selecteer **Nieuw paginafragment**.
1. Selecteer in het dialoogvenster **Nieuw paginafragment** de voettekstmodule, voer een naam in voor het paginafragment en selecteer vervolgens **OK**.
1. Selecteer in de overzichtsstructuur links de knop met het weglatingsteken (**...**) voor de voettekstmodule en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de voettekstcategoriemodule en selecteer vervolgens **OK**.
1. Selecteer in de overzichtsstructuur links de knop met het weglatingsteken (...) voor de voettekstcategoriemodule en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de voettekstitemmodule en selecteer vervolgens **OK**.
1. Selecteer in de overzichtsstructuur de module van het voettekstitem. Configureer vervolgens in het eigenschappenvenster aan de rechterkant naar wens de koptekst, koppeling, koppelingstekst en afbeelding.
1. Herhaal stap 5 en 7 als u nog meer voettekstitems wilt toevoegen.
1. Selecteer de knop met het weglatingsteken voor de voettekstcategoriemodule en selecteer vervolgens **Module toevoegen**, als u een koppeling 'terug naar boven' in uw voettekst wilt toevoegen.
1. Selecteer in het dialoogvenster **Module toevoegen** de terug naar boven-module en selecteer vervolgens **OK**.
1. Selecteer in de overzichtsstructuur de terug naar boven-module. Vervolgens configureert u in het venster Eigenschappen rechts de terug naar boven-module.
1. Sla het paginafragment op, check het in en publiceer de sjabloon.

Voer de volgende stappen uit op elke paginasjabloon die voor de site is gemaakt.

1. Voeg in het vak **Hoofd** van de standaardpagina in de voettekstmodule het voettekstfragment toe dat u hebt gemaakt.
1. Sla de sjabloon op, check in en publiceer de sjabloon.

Door het paginafragment aan de paginasjablonen toe te voegen zorgt u dat de voettekst op elke pagina wordt weergegeven.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht starterskit](starter-kit-overview.md)

[Module Container](add-container-module.md)

[Koopvakmodule](add-buy-box.md)

[Winkelwagenmodule](add-cart-module.md)

[Betalingsmodule](add-checkout-module.md)

[Orderbevestigingsmodule](order-confirmation-module.md)

[Koptekstmodule](author-header-module.md)

[Voettekstmodule](author-footer-module.md)
