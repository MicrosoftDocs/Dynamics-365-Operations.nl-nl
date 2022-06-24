---
title: Abonnementsmodule
description: In dit artikel worden abonnementsmodules beschreven en wordt aangegeven hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 23b74f5853ffb7f191ea7ee3da0d3238db339d34
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852688"
---
# <a name="subscribe-module"></a>Abonnementsmodule

[!include [banner](includes/banner.md)]

In dit artikel worden abonnementsmodules beschreven en wordt aangegeven hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

Abonnementsmodules kunnen worden gebruikt op sitepagina's om klantgegevens vast te leggen voor nieuwsbrieven of promoties.

In de volgende afbeelding ziet u een voorbeeld van een abonnementsmodule in de voettekst van een sitepagina van Adventure Works.

![Voorbeeld van een abonnementsmodule in de voettekst van een sitepagina van Adventure Works](./media/Subscribe.PNG)

> [!IMPORTANT]
> - De abonnementsmodule is beschikbaar in de modulebibliotheek van Commerce vanaf Dynamics 365 Commerce versie 10.0.20.
> - Een voorbeeld van de abonnementsmodule is opgenomen in het Adventure Works-thema.
> - Voor de abonnementsmodule is een extensie voor de gegevensactie nodig om met enkele marketing-e-mailproviders te werken, zodat de nieuwsbrieven of promotie-e-mails kunnen worden verzonden nadat klantgegevens zijn vastgelegd.

## <a name="subscribe-module-properties"></a>Eigenschappen van abonnementsmodule

| Naam van eigenschap. | Waarden | Beschrijving |
|---------------|--------|-------------|
| Koptekst       | Koptekst en tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**) | Een koptekst voor de abonnementsmodule, zoals **Abonneren op de nieuwsbrief** of **Aanmelden voor 10% korting**. |
| Alinea     | Alineatekst | De abonnementsmodule ondersteunt tekst in RTF-indeling om extra informatie te bieden voor de actieoproep in de koptekst. |

## <a name="add-a-subscribe-module-to-a-new-page"></a>Een abonnementsmodule toevoegen aan een nieuwe pagina

Voer de volgende stappen uit om een abonnementsmodule toe te voegen aan een nieuwe pagina en de vereiste eigenschappen in te stellen in Commerce Site Builder.

1. Ga naar **Sjablonen** en open de marketingsjabloon voor de startpagina van uw site (of maak een nieuwe marketingsjabloon).
1. Selecteer in het vak **Hoofdonderdeel** van de standaardpagina het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Abonneren** en selecteer vervolgens **OK**.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.
1. Ga naar **Pagina's** en open de startpagina van de site (of maak een nieuwe startpagina met de marketingsjabloon).
1. Selecteer in het vak **Hoofd** van de standaardpagina de knop met het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Abonneren** en selecteer vervolgens **OK**.
1. Voeg een kopkets, bijvoorbeeld **Abonneren**, toe in het eigenschapvenster van de abonnementsmodule.
1. Voeg tekst voor de alinea toe, zoals **Meest actuele trends, stijlen en promoties. Staat u op de lijst? Abonneer u en ontvang de allernieuwste hot deals!**
1. Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.
1. Selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Adventure Works-thema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
