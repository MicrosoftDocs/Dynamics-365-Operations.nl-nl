---
title: Resourcecapaciteit synchroniseren
description: Dit onderwerp bevat informatie over het synchroniseren van de capaciteit van een resource in kalenders en projecten.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27b6fde91a72e37bb2712daba765032322cbd4e9
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760512"
---
# <a name="synchronize-resource-capacity"></a>Resourcecapaciteit synchroniseren

[!include [banner](../includes/banner.md)]

De processen voor resourcesynchronisatie helpen ervoor te zorgen dat informatie voor de kalender en basiskalender doorvloeien naar de planning van projectresources. Als de kalender wordt gewijzigd, voeren de processen de vereiste updates door bij de planning van projectresources. De processen helpen ook de prestaties te verbeteren, omdat de resourcegegevens van de kalender van tevoren worden gesynchroniseerd. Daarom wordt resourceplanningsinformatie sneller bijgewerkt. Het wordt aangeraden om de processen als batch in te plannen in plaats van een voor een. Anders bestaat het risico dat iemand de inclusieve datums vergeet waarop de informatie voor het laatst is gesynchroniseerd. Als de inclusieve datums niet worden gebruikt, kunnen lacunes optreden tijdens de datumsynchronisatie.

![Kalendersynchronisatie](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Vergaarde resourcecapaciteit synchroniseren

Het synchronisatieproces is ontworpen om alle resourcekalenderinformatie te synchroniseren. Deze informatie omvat basiskalenderinformatie over de wijzigingen in de tabel met de resourcekalendercapaciteit van het project. Als nieuwe resources aan het project worden toegevoegd, zorgt synchronisatie ervoor dat de bijgewerkte agendagegevens beschikbaar zijn. Deze synchronisatie kan op elk gewenst moment worden uitgevoerd.

Het wordt aangeraden om een batch te gebruiken. De opties zijn beschikbaar tijdens het synchroniseren van capaciteitsreserveringen.

1. Selecteer **Projectbeheer en boekhouding** &gt; **Periodiek** &gt; **Capaciteitsynchronisatie** &gt; **Vergaarde resourcecapaciteit synchroniseren**.
2. Stel de opties in de volgende tabel in.

    | Optie      | Omschrijving |
    |-------------|-------------|
    | Periodecode | Selecteer eventueel de datumintervalcode voor het grootboek om de begin- en einddatums in te stellen voor het synchronisatieproces voor vergaarde resourcecapaciteit. |
    | Begindatum  | Voer de begindatum in voor het synchronisatieproces voor vergaarde resourcecapaciteit. |
    | Einddatum    | Voer de einddatum in voor het synchronisatieproces voor vergaarde resourcecapaciteit. |

[![Synchronisatieproces](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)
