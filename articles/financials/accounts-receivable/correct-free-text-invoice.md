---
title: Een vrije-tekstfactuur corrigeren
description: In dit artikel wordt beschreven hoe u een geboekte vrije-tekstfactuur corrigeert en opnieuw uitgeeft als gecorrigeerde factuur.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a353db68c2223d62cd8e5048f0e953ed134c0803
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="correct-a-free-text-invoice"></a>Een vrije-tekstfactuur corrigeren

[!include[banner](../includes/banner.md)]


In dit artikel wordt beschreven hoe u een geboekte vrije-tekstfactuur corrigeert en opnieuw uitgeeft als gecorrigeerde factuur.

Als u een vrije-tekstfactuur wilt corrigeren die al is geboekt, opent u de geboekte vrije-tekstfactuur. Selecteer op de pagina **Factuur** **Annuleren** en selecteer vervolgens **Factuur corrigeren**. Selecteer een redencode, voeg opmerkingen toe en selecteer de datum voor de nieuwe, gecorrigeerde factuur. U kunt de gecorrigeerde factuur wijzigen en boeken. 

Wanneer u de gecorrigeerde factuur boekt, wordt er een annuleringsfactuur gemaakt voor een creditbedrag dat gelijk is aan het oorspronkelijke factuurbedrag. Hierdoor is het gecombineerde saldo van de oorspronkelijke en de annuleringsfactuur gelijk aan 0 (nul). De annuleringsfactuur wordt vereffend met de oorspronkelijke factuur. 

Als u de gecorrigeerde factuur boekt, hebt u drie facturen:

-   **Oorspronkelijke factuur** – De factuur die de informatie bevat die u corrigeert.
-   **Annuleringsfactuur** – De creditnota die door het systeem is gegenereerd om de factuur te annuleren die zonet is gecorrigeerd.
-   **Gecorrigeerde factuur** – De factuur die de gecorrigeerde factuurgegevens bevat.

U kunt annulerings- en correctiefacturen op twee manieren identificeren:

-   De pagina **Alle vrije-tekstfacturen** bevat een kolom **Correctie** waarin u kunt zien welke facturen annuleringsfacturen en gecorrigeerde facturen zijn.
-   In de koptekst van de vrije-tekstfactuur wordt de status **Annuleringsfactuur** \[factuurnummer]\] of **Gecorrigeerde factuur '\[factuurnummer\]'** weergegeven.

> [!NOTE]
> Deze functie is alleen beschikbaar als de configuratiesleutel **Correctie van vrije-tekstfactuur** is geselecteerd.




