---
title: Module Mediagalerie
description: In dit onderwerp wordt beschreven wat mediagaleriemodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 9df2b91b0a57c73e395242f840c423fa8c7f2c9f
ms.sourcegitcommit: 629988f1a704d62648d98649056931b8c33b9e08
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/14/2020
ms.locfileid: "3811153"
---
# <a name="media-gallery-module"></a>Module Mediagalerie

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat mediagaleriemodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Met mediagaleriemodules worden een of meer afbeeldingen weergegeven in een galerieweergave. Mediagaleriemodules ondersteunen miniatuurafbeeldingen die horizontaal kunnen worden gerangschikt (als een rij onder de afbeelding) of verticaal (als een kolom naast de afbeelding). Mediagaleriemodules bieden ook mogelijkheden waarmee afbeeldingen kunnen worden ingezoomd (vergroot) of weergegeven in de modus volledig scherm. Een afbeelding wordt pas weergegeven in een mediagaleriemodule als deze beschikbaar is in de mediabibliotheek van de Commerce Site Builder. Momenteel worden in mediagaleriemodules alleen afbeeldingen ondersteund.

In de standaardmodus gebruikt een mediagaleriemodule de product-id die beschikbaar is via de paginacontext van een productgegevenspagina (PDP) om de bijbehorende productafbeeldingen te genereren. In Commerce Headquarters moet voor alle producten een pad naar het mediabestand worden gedefinieerd. Afbeeldingen moeten vervolgens worden geüpload naar de mediabibliotheek van sitebuilder op basis van het bestandspad dat is gedefinieerd voor de producten in Commerce Headquarters. Deze afbeeldingen bevatten afbeeldingen voor producten en eventuele productvarianten. Zie [Afbeeldingen uploaden](dam-upload-images.md) voor meer informatie over het uploaden van afbeeldingen naar de mediabibliotheek van Site Builder.

Een mediagaleriemodule kan ook als host fungeren voor een geselecteerde set afbeeldingen op een pagina een met afbeeldingengalerie, waar er geen afhankelijkheden zijn voor de product-id of paginacontext. In dit geval moeten afbeeldingen worden geüpload naar de mediabibliotheek van Site Builder en worden opgegeven in Site Builder.

Hier volgen enkele gebruiksvoorbeelden voor mediagaleriemodules:

- Productafbeeldingen renderen op een PDP
- Productafbeeldingen op een productmarketingpagina renderen
- Een geselecteerde set afbeeldingen tonen op een marketingpagina, zoals een galeriepagina

In het voorbeeld in de volgende afbeelding host een koopvak op een PDP productafbeeldingen met behulp van een mediagaleriemodule.

![Voorbeeld van een koopvak op een pagina met productgegevens waarop productafbeeldingen worden gehost met behulp van een mediagaleriemodule](./media/ecommerce-pdp-buybox.PNG)

## <a name="media-gallery-properties"></a>Eigenschappen van mediagalerie

| Naam van eigenschap. | Waarden | Omschrijving |
|---------------|--------|-------------|
| Bron afbeelding | **Paginacontext** of **Product-id** | De standaardwaarde is **Paginacontext**. Als **Paginacontext** is geselecteerd, verwacht de module dat de pagina de product-id-informatie opgeeft. Als **product-id** is geselecteerd, moet de product-id voor een afbeelding worden opgegeven als de waarde van de eigenschap **Product-id**. Deze mogelijkheid is beschikbaar in Commerce versie 10.0.12. |
| Product-ID | Een product-id | Deze eigenschap is alleen van toepassing als de waarde van de eigenschap **Afbeeldingsbron** **Product-id** is. |
| Inzoomen op afbeelding | **Inline** of **Container** | Met deze eigenschap kan de gebruiker afbeeldingen in de module mediagalerie in- of uitzoomen. Een afbeelding kan inline of in een afzonderlijke container naast de afbeelding worden ingezoomd. Deze mogelijkheid is beschikbaar in 10.0.12 |
| Zoomschaal | Een decimaal getal | Met deze eigenschap geeft u de schaalfactor voor het zoomen van afbeeldingen op. Als de waarde bijvoorbeeld is ingesteld op **2,5** is, worden afbeeldingen 2,5 keer vergroot.|
| Volledig scherm | **True** of **False** | Deze eigenschap geeft aan of afbeeldingen in de modus volledig scherm kunnen worden weergegeven. In de modus volledig scherm kunnen afbeeldingen ook verder worden vergroot als de zoomfunctie is ingeschakeld. Deze mogelijkheid is beschikbaar in Commerce versie 10.0.13. |
| Afbeeldingen | Afbeeldingen die zijn geselecteerd in de mediabibliotheek van Site Builder | Naast het renderen vanuit een product kunnen afbeeldingen worden geselecteerd voor een mediagaleriemodule. Deze afbeeldingen worden toegevoegd aan alle beschikbare productafbeeldingen. Deze mogelijkheid is beschikbaar in Commerce versie 10.0.12. |
| Oriëntatie van miniatuur | **Verticaal** of **Horizontaal** | Met deze eigenschap geeft u aan of miniatuurafbeeldingen moeten worden weergegeven in een verticale of horizontale strook. |

In de volgende afbeelding ziet u een voorbeeld van een module mediagalerie waarin de opties voor volledig scherm en zoomen beschikbaar zijn.

![Voorbeeld van een module mediagalerie waarin de opties voor volledig scherm en zoomen beschikbaar zijn](./media/ecommerce-media-zoom.png)

In de volgende afbeelding ziet u een voorbeeld van een mediagaleriemodule met geselecteerde afbeeldingen (dat wil zeggen dat de opgegeven afbeeldingen niet afhankelijk zijn van de product-id of pagina context).

![Voorbeeld van een mediagaleriemodule met geselecteerde afbeeldingen](./media/ecommerce-media-curated.PNG)

## <a name="commerce-scale-unit-interaction"></a>Interactie met Commerce Scale Unit

Wanneer de afbeeldingsbron is afgeleid van de paginacontext, wordt de product-id van de PDP gebruikt om de afbeeldingen op te halen. De mediagaleriemodule haalt het afbeeldingsbestandspad voor producten op met behulp van Commerce Scale Unit-API's (Application Programming Interfaces). De afbeeldingen worden vervolgens opgehaald uit de mediabibliotheek, zodat ze kunnen worden weergegeven in de module.

## <a name="add-a-media-gallery-module-to-a-page"></a>Een mediagaleriemodule toevoegen aan een pagina

Voer deze stappen uit om een mediagaleriemodule aan een marketingpagina toe te voegen.

1. Ga naar **Sjablonen** en selecteer **Nieuw** om een nieuwe sjabloon te maken.
1. Voer in het dialoogvenster **Nieuwe sjabloon** onder **Sjabloonnaam** **Marketingsjabloon** in en selecteer vervolgens **OK**.
1. Selecteer het weglatingsteken (**...**) in het vak **Hoofdtekst** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Standaardpagina** en selecteer vervolgens **OK**.
1. Selecteer in het vak **Hoofdonderdeel** van de standaardpagina het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Container** en selecteer vervolgens **OK**.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.
1. Ga naar **Pagina's** en selecteer **Nieuw** om een nieuwe pagina te maken.
1. Selecteer in het dialoogvenster **Een sjabloon kiezen** de sjabloon **Marketingsjabloon**. Voer onder **Paginanaam** **Mediagaleriepagina** in en selecteer vervolgens **OK**.
1. Selecteer in het vak **Hoofd** van de nieuwe pagina het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Container** en selecteer vervolgens **OK**.
1. Selecteer het weglatingsteken (**...**) in het vak **Container** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de **Mediagalerie** en selecteer vervolgens **OK**.
1. Selecteer **product-id** in het eigenschappenvenster voor de module mediagalerie onder **Afbeeldingsbron**. Voer in het veld **Product-id** een product-id in.
1. Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken. U zou de afbeeldingen voor het product in een galerieweergave moeten kunnen zien.
1. Als u alleen geselecteerde afbeeldingen wilt gebruiken, selecteert u in het eigenschappenvenster onder **Afbeeldingsbron** de optie **Product-id**. Selecteer vervolgens onder **Afbeeldingen** **Een afbeelding toevoegen** zo vaak als nodig is om afbeeldingen uit de mediabibliotheek toe te voegen.
1. Stel eventuele extra eigenschappen in die u wilt instellen, zoals **Afbeelding zoomen**, **Zoomfactor** en **Oriëntatie van miniatuur**.
1. Wanneer u klaar bent, selecteert u **Opslaan**, selecteert u **Bewerken voltooien** om de pagina in te checken en selecteer u vervolgens **Publiceren** om de pagina te publiceren.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht starterskit](starter-kit-overview.md)

[Module met vakje voor kopen](add-buy-box.md)

[Containermodule](add-container-module.md)

[Afbeeldingen uploaden](dam-upload-images.md)
