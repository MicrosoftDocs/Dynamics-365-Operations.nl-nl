---
title: Tabbladmodule
description: In dit artikel wordt beschreven wat tabbladmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
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
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 91c79ca1b70a776352ef99d854397ada34c548e3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276968"
---
# <a name="tab-module"></a>Tabbladmodule

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven wat tabbladmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

Tabbladmodules zijn containerachtige modules die worden gebruikt om de informatie op een sitepagina in tabbladen te ordenen. Ze kunnen worden gebruikt op elke pagina waar informatie moet worden weergegeven op tabbladen.

Aan elke tabbladmodule kunt u een of meer modules toevoegen. Elke tabbladitemmodule vertegenwoordigt één tabblad. In elke tabbladitemmodule kunnen een of meer modules worden toegevoegd. Er gelden geen beperkingen voor de typen modules die kunnen worden toegevoegd aan een tabbladitemmodule.

De volgende afbeelding toont een voorbeeld van een tabbladmodule op een sitepagina. In dit voorbeeld is het tabblad **Verzending** geselecteerd.

![Voorbeeld van een tabbladmodule.](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a>Eigenschappen van tabbladmodule

| Naam van eigenschap. | Waarden | Beschrijving |
|---------------|--------|-------------|
| Koptekst | Tekst | Deze eigenschap geeft een optionele koptekst aan voor de tabbladmodule. |
| Actieve tabbladindex | Nummer | Met deze eigenschap wordt het tabblad aangegeven dat standaard actief moet zijn wanneer een pagina wordt geladen. Als er geen waarde wordt opgegeven, is het eerste tabbladitem standaard actief. |

## <a name="tab-item-module-properties"></a>Eigenschappen van tabbladitemmodule

| Naam van eigenschap. | Waarden | Omschrijving |
|---------------|--------|-------------|
| Titel | Tekst | Deze eigenschap geeft de titeltekst aan voor de tabbladitemmodule. |

## <a name="add-a-tab-module-to-a-page"></a>Een tabbladmodule toevoegen aan een pagina

Voer de volgende stappen uit om een tabbladmodule aan een nieuwe pagina toe te voegen en de eigenschappen in te stellen.

1. Gebruik de sjabloon Fabrikam-marketing (of een sjabloon zonder beperkingen) om een nieuwe pagina te maken met de naam **Pagina met winkelbeleid**.
1. Selecteer in het vak **Hoofd** van de **Standaardpagina** het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Container** en selecteer vervolgens **OK**.
1. Selecteer het weglatingsteken (**...**) in het vak **Container** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Tabblad** en selecteer vervolgens **OK**.
1. Selecteer in het eigenschappen venster van de tabbladmodule de optie **Kop** naast het potloodsymbool.
1. Voer in het dialoogvenster **Kop** onder **Koptekst** een koptekst in (bijvoorbeeld een **Beleid**). Selecteer vervolgens **OK**.
1. Selecteer het weglatingsteken (**...**) in het vak **Tabblad** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Tabbladitem** en selecteer vervolgens **OK**.
1. Voer in het eigenschappenvenster van de tabbladitemmodule onder **Titel** de titeltekst in (bijvoorbeeld **Levering**).
1. Selecteer het weglatingsteken (**...**) in het vak **Tabbladitem** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Tekstblok** en selecteer vervolgens **OK**.
1. Voeg in het eigenschappenvenster van de tekstblokmodule een alinea tekst toe onder het veld **RTF**.
1. Voeg in het vak **Tabblad** nog een paar modules met titels toe. Voeg in elke tabbladmodule een tekstblokmodule toe die inhoud bevat.
1. Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken. Op de pagina wordt een tabbladmodule weergegeven die modules met tabbladitems bevat met de inhoud die u hebt toegevoegd.
1. Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Containermodule](add-container-module.md)

[Accordeonmodule](add-accordion.md)

[Text Block-module](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
