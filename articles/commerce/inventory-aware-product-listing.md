---
title: Productlijst met voorraadinzicht
description: Dit artikel beschrijft hoe organisaties productlijstpagina's op hun Microsoft Dynamics 365 Commerce e-commercewebsite kunnen configureren zodat ze op de hoogte zijn van de voorraad.
author: boycez
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2022-08-23
ms.openlocfilehash: 2a65dedf2da62fcd92169077d75a0f3b7832a86d
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473728"
---
# <a name="inventory-aware-product-listing"></a>Productlijst met voorraadinzicht

[!include [banner](../includes/banner.md)]

Dit artikel beschrijft hoe organisaties productlijstpagina's op hun Microsoft Dynamics 365 Commerce e-commercewebsite kunnen configureren zodat ze op de hoogte zijn van de voorraad. Productlijstpagina's bevatten categorielandingspagina's en zoekresultaten.

Klanten verwachten doorgaans dat bij het zoeken op een e-commercesite de getoonde producten rekening houden met de voorraad, zodat ze kunnen beslissen wat ze moeten doen als een product niet op voorraad is. De modules voor de categorie [Commerce-modulebibliotheek](starter-kit-overview.md) en zoekresultaten kunnen worden geconfigureerd om voorraadgegevens op te nemen. Zo kunnen de modules de volgende mogelijkheden bieden:

- Labels met voorraadniveau naast de producten weergeven.
- Producten die niet op voorraad zijn, niet tonen in de productlijst.
- Producten die niet op voorraad zijn, onderaan de productlijstpagina's weergeven.
- Productfilters op basis van voorraad ondersteunen.

Als u deze ervaring wilt inschakelen, moet u eerst de functie **Uitgebreide productdetectie in e-Commerce voor inzicht in voorraad** inschakelen in Commerce headquarters.

> [!NOTE]
> In Commerce versie 10.0.29 en later is de functie **Uitgebreide productdetectie in e-Commerce voor inzicht in voorraad** standaard ingeschakeld.

## <a name="set-up-product-attribute-for-inventory-availability"></a>Productkenmerk instellen voor voorraadbeschikbaarheid

Productlijst met inzicht in de voorraad maakt gebruik van het raamwerk met productkenmerken. U moet voor een specifiek productkenmerk maken om de voorraadbeschikbaarheidsgegevens vast te leggen.

Als u het productkenmerk voor voorraadbeschikbaarheid wilt configureren in Commerce Headquarters, neemt u de volgende stappen.

1. Ga naar **Detailhandel en commerce \> IT detailhandel en commerce \> Producten en voorraad \> Productkenmerken invullen met voorraadniveau**.
1. Voer in het dialoogvenster **Productkenmerken invullen met voorraadniveau** in het veld **Productkenmerk en typenaam** een aangepaste naam in voor het specifieke productkenmerk dat wordt gemaakt om voorraadgegevens vast te leggen.
1. Selecteer in het veld **Voorraadbeschikbaarheid gebaseerd op** het hoeveelheidstype waarop de berekening van het voorraadniveau moet worden gebaseerd: **Fysiek beschikbaar** of **Totaal beschikbaar**.
1. Stel de optie **Batchverwerking** in op **Ja**.
1. Selecteer **OK**.

> [!NOTE]
> Voor een consistente berekening van het voorraadniveau in de pagina's van uw e-commercesite moet u ervoor zorgen dat u hetzelfde hoeveelheidstype selecteert voor zowel het veld **Voorraadbeschikbaarheid gebaseerd op** voor de taak **Productkenmerken invullen met voorraadniveau** als de instelling **Voorraadniveau gebaseerd op** in Commerce Site Builder.

Nadat het specifieke productkenmerk is gemaakt, is de volgende stap het configureren van het kenmerk voor het online kanaal.

Als u het kenmerk voor het online kanaal wilt configureren in Commerce Headquarters, neemt u de volgende stappen.

1. Ga naar **Retail en Commerce \> Kanaalinstellingen \> Kanaalcategorieën en productkenmerken**.
1. Selecteer het online kanaal waarvoor u de productlijst met voorraadinzicht wilt inschakelen.
1. Selecteer en open een gekoppelde kenmerkgroep en voeg vervolgens het nieuwe productkenmerk hieraan toe.
1. Ga naar **Retail en commerce \> Retail en commerce IT \> Distributieplanning** en voer taak **1150** (**Catalogus**) uit. We raden u aan om deze taak te plannen als een batchproces en deze met dezelfde frequentie uit te voeren als de taak **Productkenmerken invullen met voorraadniveau**.

> [!NOTE]
> In Commerce versie 10.0.26 en eerder moet u, nadat u het productkenmerk voor de voorraadbeschikbaarheid hebt toegevoegd aan een kenmerkgroep, ook **Kenmerkmetagegevens instellen** selecteren en vervolgens de opties **Kenmerk in kanaal weergeven**, **Ophaalbaar**, **Kan worden verfijnd** en **Kan worden opgezocht** inschakelen voor het nieuwe productkenmerk.

## <a name="configure-the-display-behavior-for-out-of-stock-products-on-product-listing-pages"></a>Het weergavegedrag van producten die niet op voorraad zijn configureren op pagina's met productlijsten

Nadat alle voorgaande configuratiestappen zijn voltooid, hebben de verfijningen op de categorie- en zoekresultatenpagina's een voorraadfilteroptie. Er wordt een voorraadniveaulabel weergegeven voor elk productkenmerk dat op de pagina wordt weergegeven.

De pagina met de categorie en zoekresultaten geeft producten weer op het hoofdniveau, niet op productvariantniveau. Het voorraadniveau dat wordt weergegeven naast elk product is een samengevoegd voorraadniveau dat wordt bepaald door het voorraadniveau van alle varianten van een product. Het voorraadniveau van een variant wordt berekend op basis van de beschikbare voorraad van die variant in het standaardmagazijn van het online kanaal in Commerce Headquarters. Het voorraadniveau van een hoofdproduct heeft twee mogelijke waarden die de status op voorraad en niet op voorraad vertegenwoordigen. Een hoofdproduct wordt als niet voorradig beschouwd als alle varianten niet op voorraad zijn. Anders wordt het product beschouwd als op voorraad. Het label voor de waarde wordt opgehaald uit de definitie van het [voorraadniveau](inventory-buffers-levels.md). Als er geen voorraadniveau is gedefinieerd, zijn de standaardlabels (in het Engels) Beschikbaar **Available** en **Out of stock**.

U kunt vervolgens de instelling **Voorraadinstellingen voor productlijstpagina's** configureren in Commerce Site Builder om te bepalen hoe op de pagina met categorie en zoekresultaten niet-voorradige producten worden weergegeven. Zie [Voorraadinstellingen toepassen](inventory-settings.md) voor meer informatie.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
