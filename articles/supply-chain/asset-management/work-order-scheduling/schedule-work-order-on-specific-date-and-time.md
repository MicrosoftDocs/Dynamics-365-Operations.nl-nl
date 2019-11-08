---
title: Werkorder op specifieke datum en tijd plannen
description: In dit onderwerp wordt uitgelegd hoe u een werkorder op een specifieke datum en tijd in Activabeheer kunt plannen.
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
ms.openlocfilehash: 634bbb4326d560848d36f579a1179187d8369087
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652029"
---
# <a name="schedule-work-order-on-specific-date-and-time"></a>Werkorder op specifieke datum en tijd plannen

[!include [banner](../../includes/banner.md)]

 

Als een werkorder op een bepaalde datum *en* tijd moet worden gepland, kunt u het standaardplanningsproces in Activabeheer negeren en een specifieke planning voor een werkorder maken.

1. Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.

2. Klik in de lijst met werkorders op de werkorder-ID in de kolom **Werkorder**.

3. Klik op **Bewerken**.

4. Voeg op het sneltabblad **Koptekst van werkorder** begin- en einddatums en begin- en eindtijden in de velden voor **verwachte begindatums en -tijden** en **verwachte einddatums en -tijden** in.

    ![Figuur 1](media/05-work-order-scheduling.png)

5. Klik op het tabblad **Algemeen** op **Plannen** om het standaardplanningsproces te gebruiken of klik op **Verzenden** als u de werkorder wilt toewijzen aan een bepaalde medewerker.

6. Als u bestaande capaciteitsreserveringen wilt negeren om ervoor te zorgen dat de werkorder wordt gepland in de verwachte periode, maakt u de selecties zoals weergegeven in de onderstaande afbeelding in de sectie **Eindige capaciteit** van het dialoogvenster **Werkorder plannen**. Dit houdt in dat bestaande capaciteitsreserveringen door het planningsproces worden genegeerd omdat de werkorder op de verwachte begintijd moet beginnen.

    ![Figuur 2](media/06-work-order-scheduling.png)

7. Klik op **OK** om het plannen te starten.

8. Als het planningsproces dubbele boekingen oplevert, wordt er een bericht weergegeven op het scherm en kunt u de gerelateerde werkorders aanpassen.

>[!NOTE]
>Als u een onderhoudsmedewerker voor de werkorder wilt plannen, moet deze onderhoudsmedewerker beschikbaar zijn op de verwachte begindatum en -tijd. De beschikbaarheid van medewerkers wordt ingesteld in de [medewerkerskalender](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md). 

