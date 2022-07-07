---
title: Impact van uitbreidbaarheid van Commerce-catalogi voor B2B-aanpassingen
description: In dit artikelwordt de impact beschreven van de uitbreidbaarheid van Commerce-catalogi voor de B2B-functie in Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 04/28/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: a9abdb5ea702917a745c3156f774aade757c159e
ms.sourcegitcommit: 6616b969afd6beb11a79d8e740560bf00016ea7f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/17/2022
ms.locfileid: "9027249"
---
# <a name="extensibility-impact-of-commerce-catalogs-for-b2b-customizations"></a>Impact van uitbreidbaarheid van Commerce-catalogi voor B2B-aanpassingen

[!include [banner](includes/banner.md)]

In dit artikel wordt de impact beschreven van de uitbreidbaarheid van **Commerce-catalogi voor B2B** in Microsoft Dynamics 365 Commerce.

Als u de cataloguscontext wilt uitbreiden naar aangepaste scenario's, moeten uw aanpassingen mogelijk worden bijgewerkt. Deze update volgt het standaardproces dat klanten moeten volgen, omdat de aanpassingen mogelijk niet automatisch de laatste functies ondersteunen nadat de upgrades zijn uitgevoerd. Als uw aanpassingen nieuwe functies of bugfixes bevatten, raden we u aan om de aanpassingscode dienovereenkomstig bij te werken. Deze update lijkt op de wijzigingen die Microsoft mogelijk heeft aangebracht voor de basiscode.

Controleer de aanpassingen die volgen om te bepalen of uw aanpassingen moeten worden bijgewerkt.

> [!NOTE]
> - Alle merchandising-API's (application programming interfaces) moeten werken met de catalogus. Daarom is het van cruciaal belang dat u de parameter **CatalogID** opgeeft.
> - De standaardcatalogus (**CatalogID**=**0**) is geen geldige catalogus voor aangemelde B2B-gebruikers. Daarom mislukken alle API-aanroepen die '0' doorgeven of een standaardwaarde gebruiken, omdat sitegebruikers geen toegang hebben tot catalogus 0. Voor de juiste ervaring moeten de API-aanroepen van klanten worden bijgewerkt zodat ze de catalogus-id doorgeven die in de cataloguskiezer is geselecteerd. Als u een standaardwaarde gebruikt en de gebruiker van catalogus wisselt, moet de website de gegevens voor de geselecteerde catalogus leveren. Daarom moeten aangepaste API's de geselecteerde catalogus doorgeven voor de API's die worden uitgevoerd via de basiscode van Commerce.

Voor de volgende aanpassingen zijn ontwikkelingsupdates vereist:

- **Case 1:** een klant introduceert zijn eigen [gegevensactie](e-commerce-extensibility/data-actions.md) die een productgerelateerde API of gegevensactie aanroept. De volgende updatestappen zijn vereist:

    1. Als de gegevensactie een directe API-aanroep gebruikt, werkt u de gegevensactie bij zodat deze de catalogus-id krijgt, zoals in het onderstaande voorbeeld wordt weergegeven.

        ![Bijgewerkte gegevensactie die de catalogus-id aangeeft.](./media/customization1_a.png)

    1. Als de gegevensactie een andere productgerelateerde gegevensactie in de aanpassing aanroept, moet de code worden bijgewerkt zodat deze nieuwe parameters, zoals **requestContext**, doorgeeft. De parameter **requestContext** wordt gebruikt om de huidige catalogus-id op te halen, zoals in het onderstaande voorbeeld wordt weergegeven.

        ![Bijgewerkte gegevensactie die de nieuwe parameter doorgeeft.](./media/customization1_b.png)

- **Case 2:** een klant heeft een [overschreven gegevensactie](e-commerce-extensibility/data-action-overrides.md). De volgende updatestap is vereist:

    - Werk de gegevensactie bij zoals voor case 1.

- **Case 3:** een klant heeft een weergave-extensie, scriptinjectormodule of [gekloonde module](e-commerce-extensibility/modules-overview.md#clone-a-module-library-module) met aanroepen naar API's of gegevensacties. De volgende updatestap is vereist:

    - Werk de code bij zoals voor case 1, zoals in het onderstaande voorbeeld wordt weergegeven.

       ![Bijgewerkte code die de nieuwe parameter doorgeeft.](./media/customization3.png)

- **Case 4:** een klant gebruikt een **getById** API-aanroep. De volgende updatestap is vereist:

    - Schakel in plaats daarvan over naar de API-aanroep **getByIds**, omdat de API-aanroep **getById** een aantal beperkingen heeft en de catalogi niet ondersteunt.

- **Case 5:** een klant heeft een gegevensactie die informatie ophaalt voor meerdere producten die mogelijk uit verschillende catalogi afkomstig zijn. De volgende updatestap is vereist:

    - Splits de API-aanroepen op catalogus-id. Zo kan de winkelwagen producten uit verschillende catalogi bevatten voor winkelwagen-API's. De productregels moeten op catalogus-id worden gegroepeerd en ze moeten de API voor elke catalogus afzonderlijk aanroepen, zoals in het onderstaande voorbeeld is weergegeven.

        ![Bijgewerkte gegevensactie die productregels groeperen op catalogus-id.](./media/customization5.png)

## <a name="additional-resources"></a>Aanvullende bronnen

[Commercecatalogi maken voor B2B-sites](catalogs-b2b-sites.md)

[Veelgestelde vragen over Commercecatalogi voor B2B-sites](catalogs-b2b-sites-FAQ.md)
