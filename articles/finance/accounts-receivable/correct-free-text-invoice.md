---
title: Een vrije-tekstfactuur corrigeren
description: In dit artikel wordt beschreven hoe u een geboekte vrije-tekstfactuur corrigeert en opnieuw uitgeeft als gecorrigeerde factuur.
author: abruer
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c83ac47bc5e7f7ed223c772591cf8a7c1e63a40
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715492"
---
# <a name="correct-a-free-text-invoice"></a>Een vrije-tekstfactuur corrigeren

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u een geboekte vrije-tekstfactuur corrigeert en opnieuw uitgeeft als gecorrigeerde factuur.

Als u een vrije-tekstfactuur wilt corrigeren die al is geboekt, opent u de geboekte vrije-tekstfactuur. Selecteer op de pagina **Factuur** **Annuleren** en selecteer vervolgens **Factuur corrigeren**. Selecteer een redencode, voeg opmerkingen toe en selecteer de datum voor de nieuwe, gecorrigeerde factuur. U kunt de gecorrigeerde factuur wijzigen en boeken. 

Wanneer u de gecorrigeerde factuur boekt, wordt er een annuleringsfactuur gemaakt voor een creditbedrag dat gelijk is aan het oorspronkelijke factuurbedrag. Hierdoor is het gecombineerde saldo van de oorspronkelijke en de annuleringsfactuur gelijk aan 0 (nul). De annuleringsfactuur wordt vereffend met de oorspronkelijke factuur. 

Als u de gecorrigeerde factuur boekt, hebt u drie facturen:

-   **Oorspronkelijke factuur** – De factuur die de informatie bevat die u corrigeert.
-   **Annuleringsfactuur** – De creditnota die door het systeem is gegenereerd om de factuur te annuleren die zonet is gecorrigeerd.
-   **Gecorrigeerde factuur** – De factuur die de gecorrigeerde factuurgegevens bevat.

U kunt annulerings- en correctiefacturen op twee manieren identificeren:

-   De pagina **Alle vrije-tekstfacturen** bevat een kolom **Correctie** waarin u kunt zien welke facturen annuleringsfacturen en gecorrigeerde facturen zijn.
-   In de koptekst van de vrije-tekstfactuur wordt de status **Annuleringsfactuur** \[factuurnummer\] of **Gecorrigeerde factuur '\[factuurnummer\]'** weergegeven.

> [!NOTE]
> Deze functie is alleen beschikbaar als de configuratiesleutel **Correctie van vrije-tekstfactuur** is geselecteerd. Voor meer informatie over het inschakelen van configuratiesleutels zie de sectie Configuratiesleutels inschakelen (of uitschakelen) in het artikel [onderhoudsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md). 





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
