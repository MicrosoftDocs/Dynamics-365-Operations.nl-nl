---
title: Visuele en samenwerkende uitvoering
description: In dit artikel wordt beschreven hoe u uw DDMRP-ontkoppelingspunten (Demand Driven Material Requirements Planning), bufferzones, geplande orders en geschiedenis kunt controleren.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ReqDDMRPWorkspace, ReqDecouplingPointsStatusByNetFlow, ReqDecouplingPointStatusByOnHand, ReqPlannedOrderForm, ReqItemDecoupledLeadTime
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 92e38c6ea19b60ae0a61e55f240ff52698e06933
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689771"
---
# <a name="visual-and-collaborative-execution"></a>Visuele en samenwerkende uitvoering

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

In dit artikel wordt beschreven hoe u uw DDMRP-ontkoppelingspunten (Demand Driven Material Requirements Planning), bufferzones, geplande orders en geschiedenis kunt controleren.

## <a name="visually-track-buffers-and-quantities-for-a-selected-item"></a>Buffers en hoeveelheden voor een geselecteerd artikel visueel bijhouden

In Microsoft Dynamics 365 Supply Chain Management kunt u visueel bijhouden hoe buffers, voorhanden hoeveelheden en nettostroomniveaus in loop van de tijd veranderen voor geselecteerde vrijgegeven producten. Voer de volgende stappen uit om de diagrammen te openen en te controleren.

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Selecteer een vrijgegeven artikel dat als een ontkoppelingspunt is ingesteld. (Zie [Voorraadpositionering](ddmrp-inventory-positioning.md) voor meer informatie.)
1. Selecteer in het actievenster op het tabblad **Plan** **Artikelbehoefteplanning**.
1. Selecteer op de pagina **Artikelbehoefteplanning** een artikelbehoefteplanningsrecord waarmee een ontkoppelingspunt wordt gemaakt. (In deze record wordt de naam van een behoefteplanningsgroep weergegeven die is ingesteld om ontkoppelingspunten te maken.)
1. Selecteer het tabblad **Voorhanden**. Dit tabblad bevat een diagram waarin wordt aangegeven hoe voorhanden hoeveelheden in de loop van de tijd zijn gewijzigd, samen met de waarde van het niveau voorhanden voorraad dat voor een specifieke periode is vastgelegd bij elke uitvoering van de planningsoptimalisatie. Het tabblad bevat ook een tabel die laat zien in welke van de volgende categorieën elk geregistreerde niveau van voorhanden voorraad valt:

    - **Kritiek laag**: minder dan de helft van het minimum voor de periode.
    - **Laag**: tussen de helft van het minimum en het minimum.
    - **Gemiddeld voorhanden**: tussen het minimum en het minimum plus de groene zone.
    - **Hoger dan gemiddeld**: hoger dan gemiddeld.

    ![Historische, voorhanden niveaus op het tabblad Voorhanden.](media/ddmrp-on-hand-graph.png "Historische, voorhanden niveaus op het tabblad Voorhanden")

    > [!NOTE]
    > De kleuren die op het tabblad **Voorhanden** worden gebruikt, vertegenwoordigen andere bereikwaarden dan de vergelijkbare kleuren die worden gebruikt op het tabblad **Bufferwaarden**.

1. Als u wilt weergeven hoe uw bufferwaarden in de loop van de tijd zijn gewijzigd en hoe deze kunnen worden vergeleken met niveaus van voorhanden voorraad en nettostroom, selecteert u het tabblad **Bufferwaarden**.

    ![Historische niveaus van voorhanden voorraad en nettostroom op het tabblad Bufferwaarden.](media/ddmrp-buffer-values-graph.png "Historische niveaus van voorhanden voorraad en nettostroom op het tabblad Bufferwaarden")

## <a name="track-the-status-and-planned-orders-for-all-decoupling-points"></a>De status en geplande orders bijhouden voor alle ontkoppelingspunten

Het werkgebied **Vraaggestuurde MRP** biedt verschillende hulpprogramma's samen met key performance indicators (KPI's) en overzichten van de status van uw ontkoppelingspuntartikelen en gerelateerde geplande orders. Als u het werkgebied wilt openen, gaat u naar **Hoofdplanning \> Werkgebieden \> Vraaggestuurde MRP**.

![Werkgebied Vraaggestuurde MRP](media/ddmrp-workspace.png "Werkgebied Vraaggestuurde MRP")

## <a name="get-overviews-of-decoupling-points-and-planned-orders"></a>Overzichten van ontkoppelingspunten en geplande orders verkrijgen

Naast het werkgebied **Vraaggestuurde MRP** biedt Supply Chain Management verschillende pagina's waar u informatie kunt bekijken over uw DDMRP-instellingen, ontkoppelingspunten en geplande orders. Sommige pagina's bieden ook handige knoppen in het actievenster waarmee u buffers kunt beheren, hoofdplanning kunt uitvoeren en andere verwante weergaven kunt openen.

- Als u de status van ontkoppelingspunten per nettostroomniveau wilt weergeven, gaat u naar **Hoofdplanning \> Hoofdplanning \> DDMRP \> Status ontkoppelingspunten op basis van nettostroom**.
- Als u de status van ontkoppelingspunten per niveau voorhanden voorraad wilt weergeven, gaat u naar **Hoofdplanning \> Hoofdplanning \> DDMRP \> Status ontkoppelingspunten op basis van voorhanden voorraad**.
- Als u geplande orders voor ontkoppelingspunten wilt weergeven, gaat u naar **Hoofdplanning \> Hoofdplanning \> DDMRP \> Geplande orders voor ontkoppelingspunten**.
- Ga naar **Hoofdplanning \> Hoofdplanning \> DDMRP \> Ontkoppelde doorlooptijd** als u ontkoppelde doorlooptijden wilt weergeven.

## <a name="clean-up-decoupling-point-buffer-values"></a>Bufferwaarden van ontkoppelingspunten opschonen

In de loop van de tijd wordt een grote hoeveelheid historische gegevens opgebouwd die zijn gerelateerd aan lopende bufferberekeningen. Deze historische gegevens zorgen voor toename van uw gegevensvolume en kunnen uiteindelijk invloed hebben op de prestaties van uw systeem. Daarom is het raadzaam dat u af en toe de oude bufferwaarden van ontkoppelingspunten opschoont.

> [!WARNING]
> Met de opschoningstaak worden instellingen voor historische bufferwaarde en historische gegevens over voorhanden voorraad/nettostroom verwijderd. Dit kan niet ongedaan worden gemaakt.

Voer de volgende stappen uit om uw bufferwaarden voor ontkoppelingspunten op te schonen.

1. Ga naar **Hoofdplanning \> Hoofdplanning \> DDMRP \> Bufferwaarden van ontkoppelingspunt opschonen**.
1. Stel in het dialoogvenster **Bufferwaarden van ontkoppelingspunt opschonen** de volgende velden in:

    - **Records verwijderen die ouder zijn dan (dagen)**: geef in dagen de ouderdom op van de jongste records die u wilt behouden. Alle records met bufferwaarden van ontkoppelingspunten die ouder zijn dan deze waarde worden verwijderd.
    - **Hoofdplan**: selecteer een hoofdplan met artikelen die door deze opschoning moeten worden beïnvloed. De opschoning is van toepassing op alle artikelen in het plan nadat de **Filter**-instellingen die u in dit dialoogvenster opgeeft, zijn toegepast.

1. Als u de set met records wilt beperken waarop de batchtaak moet worden uitgevoerd, selecteert u op het sneltabblad **Op te nemen records** **Filter** om het dialoogvenster **Query** te openen. Dit dialoogvenster werkt op dezelfde manier als bij andere typen [achtergrondtaken](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) in Supply Chain Management.
1. Geef op het sneltabblad **Uitvoeren op de achtergrond** op hoe, wanneer en hoe vaak de opschoning moet worden uitgevoerd. De velden werken op dezelfde manier als bij andere typen [achtergrondtaken](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) in Supply Chain Management.
1. Selecteer **OK** om de nieuwe taak aan de batchwachtrij voor uitvoering toe te voegen.
