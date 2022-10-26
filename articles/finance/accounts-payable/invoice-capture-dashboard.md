---
title: Dashboard van de oplossing Invoice Capture
description: In dit artikel wordt het dashboard van de oplossing Invoice Capture beschreven.
author: sunfzam
ms.date: 10/15/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4c9000039488c1290f4ab992d7fe79b8ccac7b19
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690114"
---
# <a name="invoice-capture-solution-dashboard"></a>Dashboard van de oplossing Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In Invoice Capture bevat het dashboard diagrammen die een overzicht bieden van facturen die zijn geïmporteerd. Met behulp van deze diagrammen kan de manager van de afdeling Leveranciers de prestaties van het proces voor het genereren van facturen analyseren. De manager kan de status van het proces voor het genereren van facturen weergeven en kan door verschillende filters toe te passen ook details weergeven.

## <a name="available-charts"></a>Beschikbare diagrammen

De volgende diagrammen zijn beschikbaar op het dashboard:

- **Alle vastgelegde facturen op status**: in dit diagram worden de volgende statussen voor een vastgelegde factuur weergegeven. Door een status te selecteren, kunnen gebruikers de vastgelegde facturen filteren in de gedetailleerde lijst.

    - Vastgelegd
    - Gereed
    - Wordt gecontroleerd
    - Als verouderd gemarkeerd

- **Totaalvolume aan vastgelegde facturen**: in dit diagram wordt het aantal vastgelegde facturen per periode weergegeven. Gebruikers kunnen de periode wijzigen met de vervolgkeuzelijst.
- **Vastgelegde facturen van de belangrijkste leveranciers**: in dit diagram wordt het totale aantal facturen per leverancier weergegeven. De leveranciers met de meeste facturen staan bovenaan.
- **Dagen tot voltooiing per factuur met uitzonderingen**: in dit diagram wordt het gemiddelde aantal dagen weergegeven dat nodig is om één factuur te kunnen vastleggen. Met behulp van deze informatie kan de manager van de afdeling Leveranciers de tijd analyseren om een factuur te verwerken wanneer handmatige tussenkomst is vereist. Als er een opwaartse trend is, kunnen gebruikers de procesdetails bekijken en instellingen aanpassen om het aantal dagen dat nodig is te verminderen.
- **Onvolledige facturen op 'tijd in behandeling'**: in dit diagram wordt het aantal dagen weergegeven dat een vastgelegde factuur niet is gegenereerd in het ERP-systeem (Enterprise Resource Planning). Hoe groter het aantal dagen in behandeling, hoe langer het proces voor het genereren van facturen duurt. De manager van de afdeling Leveranciers kan inzoomen op de gedetailleerde vastgelegde facturen en facturen genereren in het ERP-systeem.
