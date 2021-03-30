---
title: Voettekstmodule
description: In dit onderwerp wordt beschreven wat voettekstmodules zijn en hoe u ze ontwerpt in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 16c9ca145aff97f0af242da4cf662367f1f4ca3d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211443"
---
# <a name="footer-module"></a>Voettekstmodule  

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat voettekstmodules zijn en hoe u ze maakt in Microsoft Dynamics 365 Commerce.

De voettekstmodule is een speciale container die wordt gebruikt voor het hosten van de modules die in de paginavoettekst worden weergegeven. De module kan bijvoorbeeld koppelingen bevatten naar verschillende pagina's in de site, zoals de pagina's **Contact opnemen** en **Winkelbeleid**.

De volgende afbeelding toont een voorbeeld van een voettekstmodule op een sitepagina.

![Voorbeeld van een voettekstmodule](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a>Eigenschappen van voettekstmodule 

Net als de meeste containers ondersteunt een voettekstmodule de eigenschappen voor de kop en de breedte. Ook wordt het toevoegen van meerdere modules ondersteund voor voettekstcategorieën. Elke voettekstcategoriemodule die wordt toegevoegd, wordt weergegeven als een kolom in de voettekstmodule.

## <a name="modules-available-in-a-footer-module"></a>Modules die beschikbaar zijn in een voettekstmodule

**Voettekstitems**: een voettekstitemmodule kan een koptekst, een afbeelding en een koppeling bevatten. De koptekst kan zelfstandig of in combinatie met een afbeelding en een koppeling worden gebruikt. Elke koppeling in de voettekst kan zo worden geconfigureerd dat deze alleen tekst bevat (bijvoorbeeld koppelingen naar 'Contact opnemen' en 'Privacy'), of dat deze zowel tekst als een afbeelding bevat (bijvoorbeeld koppelingen voor sociale media).

**Terug naar boven**: een terug naar boven-module bevat een koppeling voor een snelle navigatie naar de bovenkant van de pagina. Er is een bestemming vereist. De standaard bestemmingswaarde is \#, waarmee de gebruiker naar bovenkant van de pagina gaat.

## <a name="create-a-footer-module"></a>Een voettekstmodule maken

1. Ga naar **Fragmenten** en selecteer **Nieuw** om een nieuw paginafragment te maken.
1. Selecteer in het dialoogvenster **Nieuw fragment** de module **Container**, voer een naam in voor het fragment en selecteer vervolgens **OK**.
1. Selecteer het weglatingsteken (**...**) in het vak **Standaardcontainer** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de **Voettekstcategoriemodule** en selecteer vervolgens **OK**.
1. Selecteer het weglatingsteken (**...**) in het vak **Voettekstcategorie** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de **Voettekstitemmodule** en selecteer vervolgens **OK**.
1. Selecteer het vak **Voettekstitem** en configureer in het eigenschappenvenster aan de rechterkant naar wens de koptekst, koppeling, koppelingstekst en afbeelding.
1. Herhaal stap 5 en 7 als u nog meer voettekstitems wilt toevoegen.
1. Selecteer de knop met het weglatingsteken (**...**) voor het vak **Voettekstcategorie** en selecteer vervolgens **Module toevoegen**, als u een koppeling 'terug naar boven' in uw voettekst wilt toevoegen.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Terug naar boven** en selecteer vervolgens **OK**.
1. Selecteer het vak **Terug naar boven** en configureer in het eigenschappenvenster aan de rechterkant naar wens de tekst en andere eigenschappen.
1. Selecteer **Bewerken voltooien** om het fragment in te checken en selecteer **Publiceren** om te publiceren.

Volg deze stappen op elke paginasjabloon die voor de site wordt gemaakt om te garanderen dat een koptekst op elke pagina wordt weergegeven.

1. Voeg in het vak **Voettekst** van de module **Standaardpagina** in de voettekstmodule het voettekstfragment toe dat u hebt gemaakt.
1. Selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.

Door het fragment aan de paginasjablonen toe te voegen, zorgt u dat de voettekst op elke pagina wordt weergegeven.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Containermodule](add-container-module.md)

[Module met vakje voor kopen](add-buy-box.md)

[Winkelwagenmodule](add-cart-module.md)

[Kassamodule](add-checkout-module.md)

[Orderbevestigingsmodule](order-confirmation-module.md)

[Koptekstmodule](author-header-module.md)

[Voettekstmodule](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]