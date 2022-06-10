---
title: Voettekstmodule
description: In dit onderwerp wordt beschreven wat voettekstmodules zijn en hoe u ze ontwerpt in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 542796ffce08694954d03878cd7782b01c2c6b27
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780254"
---
# <a name="footer-module"></a>Voettekstmodule  

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat voettekstmodules zijn en hoe u ze maakt in Microsoft Dynamics 365 Commerce.

De voettekstmodule is een speciale container die wordt gebruikt voor het hosten van de modules die in de paginavoettekst worden weergegeven. De module kan bijvoorbeeld koppelingen bevatten naar verschillende pagina's in de site, zoals de pagina's **Contact opnemen** en **Winkelbeleid**.

De volgende afbeelding toont een voorbeeld van een voettekstmodule op een sitepagina.

![Voorbeeld van een voettekstmodule.](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a>Eigenschappen van voettekstmodule 

Net als de meeste containers ondersteunt een voettekstmodule de eigenschappen voor de kop en de breedte. Ook wordt het toevoegen van meerdere modules ondersteund voor voettekstcategorieën. Elke voettekstcategoriemodule die wordt toegevoegd, wordt weergegeven als een kolom in de voettekstmodule.

## <a name="modules-available-in-a-footer-module"></a>Modules die beschikbaar zijn in een voettekstmodule

**Voettekstitem**: een voettekstitemmodule kan een koptekst of een koppeling bevatten. De koptekst wordt meestal gebruikt als titel voor een voettekstsectie.  Elke koppeling in de voettekst kan zo worden geconfigureerd dat deze alleen tekst bevat (bijvoorbeeld koppelingen naar 'Contact opnemen' en 'Privacy'), of dat deze zowel tekst als een afbeelding bevat (bijvoorbeeld koppelingen voor sociale media). Als zowel een koptekst als een koppeling is opgegeven, heeft de kopteksteigenschap voorrang op de koppeling. 

**Terug naar boven**: een terug naar boven-module bevat een koppeling voor een snelle navigatie naar de bovenkant van de pagina. Er is een bestemming vereist. De standaard bestemmingswaarde is \#, waarmee de gebruiker naar bovenkant van de pagina gaat.

## <a name="create-a-footer-module"></a>Een voettekstmodule maken

1. Ga naar **Fragmenten** en selecteer **Nieuw** om een nieuw paginafragment te maken.
1. Selecteer in het dialoogvenster **Een fragment selecteren** de module **Container**, voer een naam in voor het fragment en selecteer vervolgens **OK**.
1. Selecteer het weglatingsteken (**...**) in het vak **Standaardcontainer** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Voettekstcategorie** en selecteer vervolgens **OK**.
1. Selecteer het weglatingsteken (**...**) in het vak **Voettekstcategorie** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Voettekstitem** en selecteer vervolgens **OK**.
1. Selecteer het vak **Voettekstitem** en configureer in het eigenschappenvenster aan de rechterkant naar wens de koptekst, koppeling, koppelingstekst en afbeelding.
1. Herhaal stap 5 en 7 als u nog meer voettekstitems wilt toevoegen.
1. Selecteer de knop met het weglatingsteken (**...**) voor het vak **Voettekstcategorie** en selecteer vervolgens **Module toevoegen** als u een koppeling 'terug naar boven' in uw voettekst wilt toevoegen.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Terug naar boven** en selecteer vervolgens **OK**.
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
