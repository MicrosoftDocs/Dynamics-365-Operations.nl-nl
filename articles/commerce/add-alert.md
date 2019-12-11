---
title: Waarschuwingsmodule
description: In dit onderwerp wordt beschreven wat waarschuwingsmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 82138dd7f0934f732215f67a3726638eb87075d4
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785347"
---
# <a name="alert-module"></a>Waarschuwingsmodule

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat waarschuwingsmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Een waarschuwingsmodule wordt gebruikt om inline informatieve berichten op een pagina weer te geven. Waarschuwingsmodules ondersteunen een tekstbericht en een koppeling. Ze kunnen worden gebruikt om promoties op alle pagina's van een e-commerce-site weer te geven. 

Waarschuwingsmodules worden aangestuurd door gegevens van het Content Management System (CMS) en kunnen op elke willekeurige pagina worden geplaatst.

## <a name="examples-of-alert-modules-in-e-commerce"></a>Voorbeelden van waarschuwingsmodules in e-commerce

U kunt waarschuwingsmodules in de koptekst van de site gebruiken om promoties of berichten voor de hele site aan te geven. Hieronder vindt u enkele voorbeelden:

"Jaarlijkse uitverkoop eindigt over 10 dagen"

"Grote besparingen bij terug naar school. Winkel nu."

## <a name="alert-module-properties"></a>Eigenschappen van waarschuwingsmodule

| Naam van eigenschap.  | Waarde                              | Beschrijving |
|----------------|------------------------------------|-------------|
| Tekst           | Tekst                               | Het tekstbericht dat wordt weergegeven in de waarschuwingsmodule. |
| Tekstuitlijning | **Rechts**, **Links** of **Midden** | Een waarde waarmee wordt gedefinieerd hoe tekst in de waarschuwingsmodule wordt uitgelijnd. |
| Waarschuwing negeren  | **True** of **False**              | Als de waarde is ingesteld op **True**, kan de klant de waarschuwing sluiten. |
| Koppeling           | URL                                | Een URL voor een optionele koppeling. |

## <a name="add-an-alert-module-to-a-page"></a>Een waarschuwingsmodule toevoegen aan een pagina 

Voer de volgende stappen uit om een waarschuwingsmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.

1. Maak een paginasjabloon met de naam **waarschuwingsjabloon**.
1. Voeg in het **hoofdvak** van de standaardpagina een waarschuwingsmodule toe.
1. Check de sjabloon in en publiceer deze. 
1. Gebruik de waarschuwingsjabloon die u zojuist hebt gemaakt om een pagina met de naam **waarschuwingspagina** te maken. 
1. Voeg in het **hoofdvak** van de nieuwe pagina een waarschuwingsmodule toe.
1. Voer in de instellingen voor de waarschuwingmodule de waarschuwingstekst in. U kunt de andere eigenschappen bewerken als u de waarschuwingsmodule verder wilt aanpassen.
1. Sla de pagina op en bekijk een voorbeeld. Boven aan de pagina wordt een waarschuwing weergegeven met de tekst die u hebt toegevoegd.
1. Check de pagina in en publiceer deze. 

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht starterskit](starter-kit-overview.md)

[Carrouselmodule](add-carousel.md)

[Inhoudsrijke-blokmodule](add-content-rich-block.md)

[Module voor het plaatsen van inhoud](add-content-placement-modules.md)

[Functiemodule](add-feature-module.md)

[Heldmodule](add-hero-module.md)

[Videospelermodule](add-video-player.md)
