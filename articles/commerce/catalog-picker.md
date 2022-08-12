---
title: Module Cataloguskiezer
description: In dit artikel worden modules voor cataloguskiezer behandeld en wordt beschreven hoe u deze aan B2B (business-to-business) E-commercesites van Microsoft Dynamics 365 Commerce toevoegt.
author: ashishmsft
ms.date: 07/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-04-21
ms.openlocfilehash: 642319eea7e40415fd32898f6ec07bfc86f3b1b1
ms.sourcegitcommit: d1491362421bf2fcf72a81dc2dc2d13d3b98122b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/11/2022
ms.locfileid: "9136940"
---
# <a name="catalog-picker-module"></a>Module Cataloguskiezer

[!include [banner](includes/banner.md)]

In dit artikel worden modules voor cataloguskiezer behandeld en wordt beschreven hoe u deze aan B2B (business-to-business) E-commercesites van Microsoft Dynamics 365 Commerce toevoegt.

Een module voor cataloguskiezer is een speciale container die wordt gebruikt om alle productcatalogi weer te geven die beschikbaar zijn voor gebruikers van de B2B-site om te winkelen. Meerdere catalogi worden momenteel alleen ondersteund voor B2B-sites.

In de volgende afbeelding ziet u een voorbeeld van een cataloguskiezermodule.

![Voorbeeld van een cataloguskiezermodule met drie productcatalogi.](./media/Catalog-picker-sample.png)

## <a name="add-a-catalog-picker-module-to-your-site"></a>Een cataloguskiezermodule toevoegen aan uw site

Voer de volgende stappen uit om een module voor cataloguskiezer toe te voegen aan uw site in Commerce Site Builder.

### <a name="create-a-catalog-picker-page"></a>Een pagina voor cataloguskiezer maken

Maak eerst een pagina voor cataloguskiezer.

1. Ga naar **Pagina's** en selecteer **Nieuw** om een nieuwe pagina te maken.
1. Voer in het dialoogvenster **Een nieuwe pagina maken** onder **Paginanaam** **Cataloguskiezer** in.
1. Voer onder **Pagina-URL** een URL voor de pagina en selecteer vervolgens **Volgende**.

    ![Het dialoogvenster Een nieuwe pagina maken.](./media/Create-catalog-picker-page.png)

1. Selecteer onder **Een sjabloon kiezen** **Algemene inhoud** en selecteer vervolgens **Volgende**.
1. Selecteer onder **Een indeling kiezen** **Flexibele indeling** en selecteer vervolgens **Volgende**.
1. Controleer de paginaconfiguratie onder **Controle en voltooien**. Selecteer **Terug** als u de pagina-informatie moet bewerken. Als de paginagegevens juist zijn, selecteert u **Pagina maken**.
1. Selecteer onder **Cataloguskiezer** **Hoofdvak**, selecteer het weglatingsteken (**...**) en vervolgens **Module toevoegen**.

    ![Een module toevoegen aan het hoofdvak onder Cataloguskiezer.](./media/Author-web-page-catalog-picker-1.png)

1. Selecteer in het dialoogvenster **Modules selecteren** de module **Container** en selecteer vervolgens **OK**.
1. Selecteer het vak **Container**, selecteer het weglatingsteken (**...**) en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Cataloguskiezer** en selecteer vervolgens **OK**.
1. Selecteer in het eigenschappenvenster **Cataloguskiezer** onder **Kop** **Catalogi** en voer vervolgens een kop in voor de cataloguskiezerpagina.
1. Selecteer onder **Kopniveau** een kopniveau en selecteer vervolgens **OK**.
1. Voer onder **Tekst met opmaak** tekst in die boven aan de cataloguskiezerpagina wordt weergegeven.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

### <a name="add-a-link-on-your-account-page"></a>Een koppeling aan uw rekeningpagina toevoegen

Voeg vervolgens een verwijzing toe aan uw cataloguskiezerpagina op uw pagina **Mijn rekening**.

1. Ga naar **Pagina's**, zoek en selecteer de pagina **Mijn rekening** van uw site en selecteer vervolgens **Bewerken**.
1. Selecteer onder het vak **Hoofd** van de pagina het vak **Algemene tegel voor rekening**. 
1. Selecteer in het eigenschappenvenster **Algemene tegel voor rekening** onder **Koppelingen** **Actiekoppeling toevoegen** en selecteer vervolgens **Actiekoppeling**.
1. Voer in het dialoogvenster **Actiekoppeling** onder **Koppelingstekst** de koppelingstekst in voor de koppeling naar de pagina van de cataloguskiezer.
1. Selecteer onder **Koppelingsdoel** de optie **Een koppeling toevoegen**.
1. Selecteer in het dialoogvenster **Een koppeling toevoegen** de optie **Aangepaste pagina** en selecteer vervolgens **Volgende**.
1. Selecteer onder **Naam** de cataloguskiezerpagina, selecteer **Toepassen** en selecteer vervolgens **OK**.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

De onderstaande afbeelding toont een voorbeeld van een rekeningpagina met een verwijzing naar de cataloguspagina.

![Pagina Mijn rekening met koppeling naar catalogus.](./media/my-accounts.png)

### <a name="add-a-link-from-the-header"></a>Een koppeling vanuit de koptekst toevoegen

Voeg ten slotte een koppeling vanuit de koptekst van uw site toe aan uw catalogi.

1. Ga naar **Fragmenten**, zoek en selecteer het koptekstfragment van uw site en selecteer vervolgens **Bewerken**.
1. Selecteer het vak **Kop**. 
1. Selecteer in het eigenschappenvenster **Koptekst** onder **Mijn rekening-koppelingen** **Actiekoppeling toevoegen** en selecteer vervolgens **Actiekoppeling**.
1. Voer in het dialoogvenster **Actiekoppeling** onder **Koppelingstekst** de koppelingstekst in voor de koppeling naar de pagina van de cataloguskiezer.
1. Selecteer onder **Koppelingsdoel** de optie **Een koppeling toevoegen**.
1. Selecteer in het dialoogvenster **Een koppeling toevoegen** de optie **Aangepaste pagina** en selecteer vervolgens **Volgende**.
1. Selecteer onder **Naam** de cataloguskiezerpagina, selecteer **Toepassen** en selecteer vervolgens **OK**.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om het koptekstfragment te controleren en selecteer **Publiceren** om het te publiceren.

De onderstaande afbeelding toont een voorbeeld van een koptekst van een e-commercewebsite met een koppeling naar de B2B-catalogus.

![Koptekst van e-commercewebsite met vervolgkeuzekoppeling naar catalogus.](./media/catalog-in-header.png)


## <a name="additional-resources"></a>Aanvullende bronnen 

[Commercecatalogi maken voor B2B-sites](catalogs-b2b-sites.md)

[Impact van uitbreidbaarheid van Commerce-catalogi voor B2B-aanpassingen](catalogs-b2b-sites-dev.md)

[Veelgestelde vragen over Commercecatalogi voor B2B-sites](catalogs-b2b-sites-FAQ.md)

[Accountbeheerpagina's en -modules](account-management.md)

[Koptekstmodule](author-header-module.md)
