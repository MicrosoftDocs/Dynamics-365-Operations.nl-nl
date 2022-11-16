---
title: Planhistorie en planningslogboeken weergeven
description: In dit artikel wordt uitgelegd hoe u de historie van planningstaken bekijkt.
author: t-benebo
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MPSPlanRegenerationJobList, MPSPlanRegenerationJobLogs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ab469686a009364bf53cb963506fd2107075a283
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740926"
---
# <a name="view-plan-history-and-planning-logs"></a>Planhistorie en planningslogboeken weergeven

[!include [banner](../../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u de historie van planningstaken in Microsoft Dynamics 365 Supply Chain Management bekijkt.

Als u de historie voor een plan wilt weergeven, opent u het plan door naar **Hoofdplanning** \> **Instellingen** \> **Plannen** \> **Hoofdplannen** te gaan en **Historie** te selecteren. In de historie worden alle taken voor het geselecteerde plan weergegeven. De lijst bevat voltooide en actieve taken.

Per hoofdplan behoudt het systeem maximaal 60 geschiedenisrecords en worden records verwijderd die ouder zijn dan 30 dagen. Telkens wanneer u een nieuwe hoofdplanningsberekening maakt, voegt het systeem een nieuwe geschiedenisrecord toe en schoont het de oudste records waar nodig op.

Naast de begintijd en status van taken kunt u het logboek voor een bepaalde taak weergeven. Het logboek bevat aanvullende informatie en waarschuwingen. Niet alle taken hebben een logboek. Selecteer **Logboek** als u het logboek voor een taak wilt weergeven. Logboekvermeldingen worden slechts 30 dagen opgeslagen na de datum waarop de taak is voltooid. Daarna worden ze automatisch verwijderd.

Als de optie **Batchverwerking** op het sneltabblad **Uitvoeren op de achtergrond** is ingeschakeld tijdens het instellen van de hoofdplanning, bevat het batchtaaklogboek meer informatie over eventuele waarschuwingen en fouten die tijdens de hoofdplanning zijn gegenereerd. Automatische fiatteringsfouten worden bijvoorbeeld alleen vastgelegd in het batchtaaklogboek. Deze worden niet weergegeven in logboeken op de pagina **Historie**.

Voer deze stappen uit om automatische fiatteringsfouten en andere waarschuwingen of fouten weer te geven die tijdens een hoofdplanningsrun zijn opgetreden.

1. Ga naar **Systeembeheer \> Query's \> Batchtaken**.
1. Zoek en selecteer de record voor de hoofdplanningsrun waarin u bent geïnteresseerd. (De waarde van het veld **Taakomschrijving** kan bijvoorbeeld beginnen met *Hoofdplanning*.)
1. Voer een van de volgende stappen uit, afhankelijk van het *verbeterde formulier* of het *verouderde formulier (niet-gewijzigd)* voor de pagina **Batchtaken**:

    - Als u het verbeterde formulier gebruikt, selecteert u **Batchtaakhistorie** in het actievenster. Selecteer vervolgens **Logboek** op de pagina **Batchtaakhistorie** in het actievenster.
    - Als u het verouderde formulier gebruikt, selecteert u **Logboek** op het tabblad **Batchtaak** in het actievenster.

1. Selecteer **Berichtdetails** om het deelvenster **Berichtdetails** te openen, waar u alle waarschuwingen en fouten kunt bekijken die tijdens de verwerking zijn vastgelegd.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
