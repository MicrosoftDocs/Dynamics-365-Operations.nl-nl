---
title: Werkorder verzenden
description: In dit onderwerp wordt uitgelegd hoe u werkorders verzendt in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3b1621cf0f1e47d7bd5fe2fa0b41fbcd61f14def
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887200"
---
# <a name="dispatch-work-order"></a>Werkorder verzenden

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

U kunt één werkorder of werkordertaken voor één medewerker plannen met behulp van de functionaliteit **Verzenden**.

1. Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.

2. Selecteer de werkorder in de lijst.

3. Klik op het tabblad **Algemeen** op **Verzenden**.

4. Selecteer in het dialoogvenster **Werkorders plannen** de medewerker in het veld **Medewerker**.

5. In het veld **Uren plannen** kunt u verwachte werkuren invoegen voor het geval verwachte werkuren afwijken van prognose-uren.

6. In het veld **Gepland begin** kunt u zo nodig de begindatum en -tijd bewerken.

7. Als in het planningsproces capaciteitsbeperkingen in acht moeten worden genomen voor resources die al zijn gepland voor andere taken, moet u ervoor zorgen dat de wisselknoppen **Activum**, **Hulpmiddel** en **Medewerker** zijn ingesteld op Ja. Als u gedetailleerde informatie over het planningsproces wilt weergeven, stelt u de wisselknop in op **Uitgebreid**. Dit betekent dat er gedetailleerde informatie over de berekende scores voor de werkorder wordt weergegeven in het infologboek.

8. Selecteer Ja voor de wisselknop **Schema negeren** om gesloten dagen in de kalender te negeren (van toepassing op activum, medewerker en hulpprogramma's). Selecteer Ja voor de wisselknop **Geplande uitvoering negeren** om beperkingen te negeren die mogelijk zijn geselecteerd voor de werkorder met betrekking tot de planning. Zie de sectie [Geplande uitvoering](../setup-for-work-orders/scheduled-execution.md) voor informatie over het instellen van de geplande uitvoering.

9. Klik op **OK**. De levenscyclusstatus van de werkorder wordt automatisch bijgewerkt naar de geplande levenscyclusstatus opgegeven via **Activabeheer** > **Instellingen** > **Werkorders** > **Levenscyclusmodellen**.

In de volgende afbeelding ziet u een voorbeeld van selecties voor verzending in het dialoogvenster **Werkorder plannen**.

![Figuur 1](media/04-work-order-scheduling.png)

>[!NOTE]
>Als u de planning voor een werkorder wilt verwijderen, selecteert u de werkorder in **Alle werkorders** en klikt u op **Planning verwijderen** op het tabblad **Algemeen**. Werk de levenscyclusstatus voor de werkorder handmatig bij als u de planning verwijdert.
