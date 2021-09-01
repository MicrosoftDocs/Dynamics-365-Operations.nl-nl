---
title: Sjablonen laden
description: In dit onderwerp wordt beschreven hoe u laadsjablonen instelt en hoe u een laadsjabloon koppelt aan een nieuwe lading.
author: Henrikan
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 35e858970114224fe6c4dabf05675d1204b8fd49c3147dab5b8758ab3de47f5a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745425"
---
# <a name="load-templates"></a>Sjablonen laden

Wanneer u een nieuwe lading maakt, kunt u een laadsjabloon toewijzen. De laadsjabloon bevat informatie over apparatuur en over maateenheden zoals de hoogte, breedte, diepte en het volume van de lading.

In dit onderwerp wordt beschreven hoe u laadsjablonen instelt en hoe u een laadsjabloon koppelt aan een nieuwe lading.

## <a name="set-up-a-load-template"></a>Een laadsjabloon instellen

1. Ga naar **Transportbeheer \> Instellen \> Lading opbouwen \> Laadsjabloon**.
1. Selecteer in het actievenster **Nieuw** om een nieuwe sjabloon toe te voegen of **Bewerken** om een bestaande sjabloon te bewerken.
1. Stel in de rij voor de nieuwe of bestaande sjabloon de volgende velden in:

    - **Ladingssjabloon-id**: voer een unieke id in voor de laadsjabloon.
    - **Apparatuur**: selecteer de apparatuur die moet worden gebruikt om de lading te verzenden.
    - **Laadhoogte**, **Laadbreedte** en **Laaddiepte**: voer de afmetingen van de lading in.
    - **Maximaal toegestane ladingvolume** en **Maximaal toegestane ladinggewicht**: voer het maximaal toegestane volume en gewicht van de lading in.
    - **Maximaal toegestaan brutogewicht**: voer het maximaal toegestane brutogewicht van de lading in. Het brutogewicht omvat zowel tarragewicht als laadgewicht.
    - **Maximumaantal vrachtstukken**: voer het maximumaantal vrachtstukken in dat de lading kan bevatten.
    - **Stapellading op vloer**: schakel dit selectievakje in als u laden op vloer wilt gebruiken. Bij een vloerlading worden dozen binnen de container van vloer tot plafond en van wand tot wand gestapeld om de capaciteit te maximaliseren.

1. Selecteer **Opslaan** in het actievenster.

## <a name="associate-a-load-template-with-a-new-load"></a>Een laadsjabloon aan een nieuwe lading koppelen

1. Ga naar **Transportbeheer \> Planning \> Workbench ladingplanning**.
1. Selecteer in het bovenste gedeelte van de pagina een van de volgende tabbladen, afhankelijk van het type brondocument waarvoor u een lading maakt: **Verzendingen**, **Verkoopregels**, **Transferregels** of **Inkooporderregels**. 
1. Selecteer het specifieke document waarvoor u de lading wilt plannen.
1. Selecteer in het actievenster op het tabblad **Vraag en aanbod** in de groep **Toevoegen** de optie **Aan nieuwe lading**.
1. Selecteer in het dialoogvenster **Laadsjabloon** in het veld **Laadsjabloon-ID** de toe te passen sjabloon.
1. Selecteer **OK** om de sjabloon toe te passen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]