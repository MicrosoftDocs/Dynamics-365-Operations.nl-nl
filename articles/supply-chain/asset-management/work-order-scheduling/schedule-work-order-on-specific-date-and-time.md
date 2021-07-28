---
title: Werkorder op specifieke datum en tijd plannen
description: In dit onderwerp wordt uitgelegd hoe u een werkorder op een specifieke datum en tijd in Activabeheer kunt plannen.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c28ade5bb6a22b9d15380085ea479e79ba246c1e
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354055"
---
# <a name="schedule-work-order-on-specific-date-and-time"></a>Werkorder op specifieke datum en tijd plannen

[!include [banner](../../includes/banner.md)]

 

Als een werkorder op een bepaalde datum *en* tijd moet worden gepland, kunt u het standaardplanningsproces in Activabeheer negeren en een specifieke planning voor een werkorder maken.

1. Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.

2. Klik in de lijst met werkorders op de werkorder-ID in de kolom **Werkorder**.

3. Klik op **Bewerken**.

4. Voeg op het sneltabblad **Koptekst van werkorder** begin- en einddatums en begin- en eindtijden in de velden voor **verwachte begindatums en -tijden** en **verwachte einddatums en -tijden** in.

    ![Figuur 1.](media/05-work-order-scheduling.png)

5. Klik op het tabblad **Algemeen** op **Plannen** om het standaardplanningsproces te gebruiken of klik op **Verzenden** als u de werkorder wilt toewijzen aan een bepaalde medewerker.

6. Als u bestaande capaciteitsreserveringen wilt negeren om ervoor te zorgen dat de werkorder wordt gepland in de verwachte periode, maakt u de selecties zoals weergegeven in de onderstaande afbeelding in de sectie **Eindige capaciteit** van het dialoogvenster **Werkorder plannen**. Dit houdt in dat bestaande capaciteitsreserveringen door het planningsproces worden genegeerd omdat de werkorder op de verwachte begintijd moet beginnen.

    ![Figuur 2.](media/06-work-order-scheduling.png)

7. Klik op **OK** om het plannen te starten.

8. Als het planningsproces dubbele boekingen oplevert, wordt er een bericht weergegeven op het scherm en kunt u de gerelateerde werkorders aanpassen.

>[!NOTE]
>Als u een onderhoudsmedewerker voor de werkorder wilt plannen, moet deze onderhoudsmedewerker beschikbaar zijn op de verwachte begindatum en -tijd. De beschikbaarheid van medewerkers wordt ingesteld in de [medewerkerskalender](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md). 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]