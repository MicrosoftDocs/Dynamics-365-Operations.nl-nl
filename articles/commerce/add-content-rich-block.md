---
title: Inhoudsrijke-blokmodule
description: In dit onderwerp wordt beschreven wat inhoudsrijke-blokmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 27dabb425b3c9a3015ffc54ff3c0e50b7ee11749
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785416"
---
# <a name="content-rich-block-module"></a>Inhoudsrijke-blokmodule

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat inhoudsrijke-blokmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Een inhoudsrijke-blokmodule is een speciale container waarin een of meer inhoudsrijke-blokitems kunnen worden geplaatst. Inhoudsrijke-blokmodules worden gebruikt voor tekstinhoud op een pagina. Deze inhoud kan informatief of promotioneel zijn.

Inhoudsrijke-blokmodules worden aangestuurd door gegevens van het Content Management System (CMS) en kunnen op elke willekeurige pagina worden geplaatst. Ze zijn zelfstandige modules die niet afhankelijk is van andere paginacontext of andere modules.

## <a name="examples-of-content-rich-block-modules-in-e-commerce"></a>Voorbeelden van inhoudsrijke-blokmodules in e-commerce

Inhoudsrijke-blokmodules kunnen op de volgende manieren worden gebruikt:

* Voor het presenteren van productfuncties op een pagina met productgegevens.
* Voor informatieve doeleinden op elke willekeurige pagina. Ze kunnen bijvoorbeeld de voordelen van loyaliteitsprogramma's toelichten, verzend- en retourbeleid beschrijven, veelgestelde vragen beantwoorden of informatie over het bedrijf invullen.
* Aangepaste berichten toevoegen aan een pagina met productgegevens. (bijvoorbeeld "gratis verzending voor bestellingen boven $50").
* Voor disclaimers en contactgegevens op pagina's met productdetails, winkelwagens, kassa en andere pagina's (bijvoorbeeld "verzending en retouren vallen onder het winkelbeleid").

## <a name="content-rich-block-module-properties"></a>Eigenschappen van inhoudsrijke-blokmodules

| Naam van eigenschap.     | Waarde                                 | Eigenschap |
|-------------------|---------------------------------------|----------|
| Aantal kolommen | Een getal tussen **1** en **4**     | Het aantal kolommen in het Inhoudsrijke blok. Er kunnen maximaal vier kolommen zijn. |
| Breedte             | **Passen in container** of **Scherm vullen** | Als de waarde wordt ingesteld op **Passen in container**, zijn de items in de container beperkt tot de breedte van de container. Als de waarde is ingesteld op **Scherm vullen**, zijn de items niet beperkt tot de breedte van de container voor de plaatsing van inhoud, maar gebruiken ze de modus Volledig scherm. U kunt de waarde wijzigen om de gewenste indeling te bereiken. |

## <a name="content-rich-block-item-module-properties"></a>Eigenschappen van modules met inhoudsrijke blokitems

| Naam van eigenschap. | Waarde          | Beschrijving |
|---------------|----------------|-------------|
| Alinea     | Alineatekst | De tekst die bij elk item in het inhoudsrijke blok wordt getoond. Sommige basisfuncties voor tekstopmaak worden ondersteund, zoals vetgedrukte, onderstreepte en cursieve tekst. |

## <a name="add-a-content-rich-block-module-to-a-page"></a>Een inhoudsrijke-blokmodule toevoegen aan een pagina

Voer de volgende stappen uit om een inhoudsrijke-blokmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.

1. Maak een paginasjabloon met de naam **Inhoudsjabloon**.
1. Voeg in het **hoofdvak** van de standaardpagina een inhoudsrijke-blokmodule toe.
1. Check de sjabloon in en publiceer deze.
1. Gebruik de inhoudsjabloon die u zojuist hebt gemaakt om een pagina met de naam **Inhoudpagina** te maken.
1. Voeg in het **hoofdvak** van de nieuwe pagina een inhoudsrijke-blokmodule toe.
1. Stel in de eigenschappen van de inhoudsrijke-blokmodule het aantal kolommen in op **2**.
1. Selecteer in de inhoudsrijke-blokmodule de optie **Een module toevoegen** en voeg een inhoudsrijk blokitem (bijvoorbeeld **Item1**) toe.
1. Voeg in het nieuwe inhoudsrijke blokitem een alineatekst toe.
1. Selecteer in de inhoudsrijke-blokmodule de optie **Een module toevoegen** en voeg een inhoudsrijk blokitem (bijvoorbeeld **Item2**) toe.
1. Voeg in het nieuwe inhoudsrijke blokitem een alineatekst toe.
1. Sla de pagina op en bekijk de wijzigingen. In een weergave met twee kolommen ziet u twee inhoudsrijke blokken.
1. Check de pagina in en publiceer deze.

> [!NOTE]
> Als u een derde inhoudsrijk blokitem toevoegt, wordt deze onder de twee items geplaatst die u eerder hebt toegevoegd. Door het aantal kolommen en items in de container te wijzigen, kunt u verschillende indelingen voor tekstinhoud bereiken.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht starterskit](starter-kit-overview.md)

[Waarschuwingsmodule](add-alert.md)

[Carrouselmodule](add-carousel.md)

[Module voor het plaatsen van inhoud](add-content-placement-modules.md)

[Functiemodule](add-feature-module.md)

[Heldmodule](add-hero-module.md)

[Videospelermodule](add-video-player.md)

