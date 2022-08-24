---
title: Accordeonmodule
description: In dit artikel worden accordeonmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: ec895476770f297825d6c88d0b0a5fef43a5c6ef
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279151"
---
# <a name="accordion-module"></a>Accordeonmodule

[!include [banner](includes/banner.md)]

In dit artikel worden accordeonmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

Accordeonmodules zijn containerachtige modules die worden gebruikt om de informatie of modules op een pagina te ordenen door een samenvouwbare lade te bieden. Op elke pagina kan een accordeonmodule worden gebruikt.

Aan elke accordeonmodule kunt u een of meer accordeonitemmodules toevoegen. Elke accordeonitemmodule vertegenwoordigt een samenvouwbare lade. Aan elke accordeonitemmodule kunt u een of meer modules toevoegen. Er gelden geen beperkingen voor de typen modules die kunnen worden toegevoegd aan een accordeonitemmodule.

De volgende afbeelding toont een voorbeeld van een accordeonmodule die wordt gebruikt om informatie op de pagina met veelgestelde vragen van een winkel te ordenen.

![Voorbeeld van een accordeonmodule.](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a>Eigenschappen van accordeonmodule

| Naam van eigenschap. | Waarden | Beschrijving |
|---------------|--------|-------------|
| Kop | Tekst | Deze eigenschap geeft een optionele koptekst aan voor de accordeonmodule. |
| Alles uitvouwen | **True** of **False** | Als de waarde is ingesteld op **Waar**, wordt de functie voor het uit- en samenvouwen ingeschakeld zodat alle items in de accordeonmodule kunnen worden uitgevouwen en samengevouwen. |
| Stijl van interactie | **Onafhankelijk** of **Alleen één item uitvouwen** | Deze eigenschap bepaalt de stijl van de interactie voor accordeonitems. Als de waarde op **Onafhankelijk** wordt ingesteld, kan elk accordeonitem onafhankelijk worden uitgevouwen of samengevouwen. Als de waarde wordt ingesteld op **Alleen één item uitvouwen**, kan slechts één item tegelijk worden uitgevouwen. Wanneer items worden uitgevouwen, worden eerder uitgevouwen items samengevouwen. |

## <a name="accordion-item-module-properties"></a>Eigenschappen van accordeonitemmodule

| Naam van eigenschap. | Waarden | Omschrijving |
|----------------|--------|-------------|
| Titel | Tekst | Deze eigenschap geeft de titeltekst aan voor de accordeonitemmodule. Als u de titelregio selecteert, kunnen gebruikers de sectie uitvouwen of samenvouwen. |
| Standaard uitvouwen | **True** of **False** | Als de waarde is ingesteld op **Waar**, wordt het accordeonitem standaard uitgevouwen wanneer de pagina wordt geladen. |

## <a name="add-an-accordion-module-to-a-faq-page"></a>Een accordeonmodule toevoegen aan een pagina met veelgestelde vragen

Voer de volgende stappen uit om een accordeonmodule aan een pagina met veelgestelde vragen toe te voegen en de eigenschappen in te stellen in Site builder.

1. Ga naar **Pagina's** en gebruik de sjabloon Fabrikam-marketing (of een sjabloon zonder beperkingen) om een nieuwe pagina te maken met de naam **Veelgestelde vragen over winkel**.
1. Selecteer in het vak **Hoofd** van de **Standaardpagina** het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Container** en selecteer vervolgens **OK**.
1. Selecteer het weglatingsteken (**...**) in het vak **Container** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Accordeon** en selecteer vervolgens **OK**.
1. Selecteer in het eigenschappen venster van de accordeonmodule de optie **Kop** naast het potloodsymbool.
1. Voer in het dialoogvenster **Kop** onder **Koptekst** **Veelgestelde vragen** in. Selecteer vervolgens **OK**.
1. Schakel in het eigenschappenvenster van de accordeonmodule het selectievakje **Alles uitvouwen weergeven** in en selecteer vervolgens in het veld **Stijl van interactie** de optie **Onafhankelijk**.
1. Selecteer het weglatingsteken (**...**) in het vak **Accordeon** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Accordeonitem** en selecteer vervolgens **OK**.
1. Voer in het eigenschappenvenster van de accordeonitemmodule onder **Titel** de titeltekst in (bijvoorbeeld **Hoe werkt retourneren?**).
1. Selecteer het weglatingsteken (**...**) in het vak **Accordeonitem** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Tekstblok** en selecteer vervolgens **OK**.
1. Voer in het eigenschappenvenster van de tekstblokmodule een alinea tekst in (bijvoorbeeld **Retouren worden verwerkt via het callcenter. Neem contact op met 1-800-FABRIKAM voor retouren. Producten hebben een teruggavebeleid van 30 dagen. Retouren moeten worden gestart binnen deze tijdsperiode.**).
1. Voeg in het vak **Accordeon** nog een paar accordeonitemmodules toe. Voeg in elke accordeonitemmodule een tekstblokmodule toe die inhoud bevat.
1. Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken. Op de pagina wordt een accordeonmodule weergegeven die de inhoud bevat die u hebt toegevoegd.
1. Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Containermodule](add-container-module.md)

[Tabbladmodule](add-tab.md)

[Text Block-module](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
