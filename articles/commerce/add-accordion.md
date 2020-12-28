---
title: Accordeonmodule
description: In dit onderwerp worden accordeonmodules beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2bb18539f610e5af05f8d9a20a0ba9f34db5c94f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411295"
---
# <a name="accordion-module"></a>Accordeonmodule

[!include [banner](includes/banner.md)]

In dit onderwerp worden accordeonmodules beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Accordeonmodules zijn containerachtige modules die worden gebruikt om de informatie of modules op een pagina te ordenen door een samenvouwbare lade te bieden. Op elke pagina kan een accordeonmodule worden gebruikt.

Aan elke accordeonmodule kunt u een of meer accordeonitemmodules toevoegen. Elke accordeonitemmodule vertegenwoordigt een samenvouwbare lade. Aan elke accordeonitemmodule kunt u een of meer modules toevoegen. Er gelden geen beperkingen voor de typen modules die kunnen worden toegevoegd aan een accordeonitemmodule.

De volgende afbeelding toont een voorbeeld van een accordeonmodule die wordt gebruikt om informatie op de pagina met veelgestelde vragen van een winkel te ordenen.

![Voorbeeld van een accordeonmodule](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a>Eigenschappen van accordeonmodule

| Naam van eigenschap. | Waarden | Omschrijving |
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
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Container** en selecteer vervolgens **OK**.
1. Selecteer het weglatingsteken (**...**) in het vak **Container** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de **Accordeonmodule** en selecteer vervolgens **OK**.
1. Selecteer in het eigenschappen venster van de accordeonmodule de optie **Kop** naast het potloodsymbool.
1. Voer in het dialoogvenster **Kop** onder **Koptekst** **Veelgestelde vragen** in. Selecteer vervolgens **OK**.
1. Schakel in het eigenschappenvenster van de accordeonmodule het selectievakje **Alles uitvouwen weergeven** in en selecteer vervolgens in het veld **Stijl van interactie** de optie **Onafhankelijk**.
1. Selecteer het weglatingsteken (**...**) in het vak **Accordeon** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de **Accordeonitemmodule** en selecteer vervolgens **OK**.
1. Voer in het eigenschappenvenster van de accordeonitemmodule onder **Titel** de titeltekst in (bijvoorbeeld **Hoe werkt retourneren?**).
1. Selecteer het weglatingsteken (**...**) in het vak **Accordeonitem** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Tekstblok** en selecteer vervolgens **OK**.
1. Voer in het eigenschappenvenster van de tekstblokmodule een alinea tekst in (bijvoorbeeld **Retouren worden verwerkt via het callcenter. Neem contact op met 1-800-FABRIKAM voor retouren. Producten hebben een teruggavebeleid van 30 dagen. Retouren moeten worden gestart binnen deze tijdsperiode.**).
1. Voeg in het vak **Accordeon** nog een paar accordeonitemmodules toe. Voeg in elke accordeonitemmodule een tekstblokmodule toe die inhoud bevat.
1. Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken. Op de pagina wordt een accordeonmodule weergegeven die de inhoud bevat die u hebt toegevoegd.
1. Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Containermodule](add-container-module.md)

[Tabbladmodule](add-tab.md)

[Text Block-module](add-content-rich-block.md)
