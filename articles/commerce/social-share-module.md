---
title: Module voor sociaal delen
description: In dit artikel worden modules voor sociaal delen beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 88bc5469e3072b625836cc942efbd2206f6dd6ba
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284679"
---
# <a name="social-share-module"></a>Module voor sociaal delen

[!include [banner](includes/banner.md)]

In dit artikel worden modules voor sociaal delen beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

Met modules voor sociaal delen kunnen gebruikers pagina-URL's van e-commerce-sites delen op sociale media, zoals Facebook, Twitter, Pinterest en LinkedIn. URL's van sitepagina's kunnen ook via e-mail worden gedeeld. Modules voor sociaal delen worden vaak gebruikt op pagina's met productgegevens om gebruikers te helpen productgegevens te delen.

Elke module voor sociaal delen is een container voor modules voor items voor sociaal delen. Elke module voor items voor sociaal delen kan zo worden geconfigureerd dat deze naar een specifieke site voor sociale media verwijst. Integratie met Facebook, Twitter, Pinterest, LinkedIn en e-mail wordt standaard ondersteund. Wanneer een sitegebruiker een symbool voor sociale media selecteert, wordt een HTML-iframe voor de betreffende site voor sociale media gestart. Binnen het iframe kan de gebruiker zich aanmelden en de weergegeven pagina-inhoud publiceren.

Op elk platform voor sociale media kunnen cookies worden bijgehouden, dus voor deze module moeten sitegebruikers het cookietoestemmingsbericht accepteren. Wanneer geen toestemming wordt gegeven voor cookies, wordt de module verborgen op de pagina. Zie [Conformiteit van cookie](cookie-compliance.md) voor meer informatie.

In de volgende afbeelding wordt een voorbeeld van een module voor sociaal delen op een pagina met productgegevens weergegeven.

![Voorbeeld van een module voor sociaal delen.](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a>Eigenschappen van module voor sociaal delen

| Naam van eigenschap.             | Waarde                 | Beschrijving |
|---------------------------|-----------------------|-------------|
| Ondertitel                  | Tekst | Met deze eigenschap geeft u een bijschrift op voor de module. |
| Afdrukstand | **Horizontaal** of **Verticaal**  | Met deze eigenschap wordt de afdrukstand van de indeling voor de sociale media-items bepaald. |

## <a name="social-share-item-module-properties"></a>Eigenschappen van module voor items voor sociaal delen
| Naam van eigenschap.             | Waarde                 | Beschrijving |
|---------------------------|-----------------------|-------------|
| Sociale media              | **Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail** | Een vervolgkeuzemenu met een lijst met sociale-mediaplatforms. |
| Pictogram |Afbeelding    | Dit is de afbeelding die voor de respectieve sociale media wordt weergegeven. Voor elk platform kunt u het beste de SDK van het platform voor sociale media raadplegen voor de aanbevolen afbeelding voor elk platform. |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a>Een module voor sociaal delen toevoegen aan een koopvakmodule

Ga als volgt te werk om een module voor sociaal delen toe te voegen aan een koopvakmodule.

1. Selecteer op de Fabrikam-site de optie **Pagina's** en selecteer vervolgens de pagina **DefaultPDP** om de pagina met productgegevens te openen. 
1. Selecteer in het vak **Koopvak** (vereist) het beletselteken (**...**) en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Delen op sociale media** en selecteer vervolgens **OK**.
1. Selecteer in het vak **Delen op sociale media** het beletselteken (**...**) en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **SocialShare** en selecteer vervolgens **OK**.
1. Selecteer **Horizontaal** in het deelvenster Eigenschappen van de module **SocialShare** onder **Afdrukstand**. Voeg zo nodig een bijschrift toe.
1. Selecteer in het vak **SocialShare** het beletselteken (**...**) en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **SocialShareItem** en selecteer vervolgens **OK**.
1. Selecteer **Facebook** in het deelvenster Eigenschappen van de module **SocialShareItem** onder **Sociale media**.
1. Selecteer **+ Een afbeelding toevoegen** in het deelvenster Eigenschappen van de module **SocialShareItem** onder **Pictogram**.
1. Selecteer in het dialoogvenster **Mediakiezer** de afbeelding van het Facebook-logo en selecteer vervolgens **OK**. Als er geen Facebook-logo aanwezig is, selecteert **Nieuw media-item uploaden** om een item te uploaden.
1. Voeg zo nodig extra **SocialShareItem**-modules toe en configureer deze.
1. Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken. Op de pagina wordt de module voor sociaal delen weergegeven.
1. Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Module met vakje voor kopen](add-buy-box.md)

[Conformiteit van cookie](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
