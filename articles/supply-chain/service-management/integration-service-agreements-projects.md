---
title: Integratie voor serviceovereenkomsten en projecten
description: Als u werkt met serviceovereenkomsten en serviceovereenkomstregels, maakt u gebruik van gegevens die in de gebieden in Projectbeheer en boekhouding zijn ingesteld.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6bd2fb1f54a3decb77f019db6b2016cebdcaddb9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571043"
---
# <a name="integration-for-service-agreements-and-projects"></a>Integratie voor serviceovereenkomsten en projecten 

[!include [banner](../includes/banner.md)]


Als u werkt met serviceovereenkomsten en serviceovereenkomstregels, maakt u gebruik van gegevens die in de volgende gebieden in **Projectbeheer en boekhouding** zijn ingesteld.

## <a name="project-prices"></a>Projectprijzen

De kostprijs en verkoopprijs voor een serviceovereenkomsttransactie worden afgeleid uit de ingestelde kostprijzen die gelden voor het project dat aan de serviceovereenkomst is gekoppeld. Kost- en verkoopprijzen kunnen per project, werknemer en categorie worden ingesteld. 

## <a name="project-validation"></a>Projectvalidatie

Op basis van de validatie-instellingen in **Projectbeheer en boekhouding** wordt bepaald welke projecten, werknemers en categorieën in een serviceovereenkomstregel beschikbaar zijn voor selectie. Met de validatie-instellingen kunt u werknemers, projecten en categorieën combineren om de toegang te controleren. 

## <a name="project-line-properties"></a>Projectregeleigenschappen

Voor een serviceovereenkomstregel wordt automatisch een regeleigenschap ingevoerd.

Regeleigenschappen worden gemaakt in het formulier **Regeleigenschappen** in **Projectbeheer en boekhouding**. De regeleigenschap die in een serviceovereenkomst wordt ingevoerd, is gekoppeld aan het project dat voor de serviceovereenkomst is geselecteerd, en wordt vervolgens overgenomen door de serviceovereenkomstregel. 

## <a name="default-offset-accounts"></a>Standaardtegenrekeningen

Voor een onkostentransactie die u invoert, wordt automatisch een standaardonkostentegenrekening geselecteerd. De standaardonkostenrekening is ingesteld voor het project dat aan de huidige serviceovereenkomst is gekoppeld.

## <a name="project-categories"></a>Projectcategorieën

Welke categorieën voor serviceovereenkomstregels beschikbaar zijn, wordt ingesteld in het formulier **Projectcategorieën** in **Projectbeheer en boekhouding**. 

> [!NOTE]
> <P>Categorieën waarvoor het selectievakje <STRONG>Actief in journalen</STRONG> op het tabblad <STRONG>Project</STRONG> in het formulier <STRONG>Projectcategorieën</STRONG> is ingeschakeld, zijn beschikbaar voor selectie. Als echter het selectievakje <STRONG>Inactieve categorieën</STRONG> op het tabblad <STRONG>Journalen</STRONG> in het formulier <STRONG>Projectbeheer- en boekhoudingsparameters</STRONG> is ingeschakeld, zijn alle categorieën beschikbaar voor selectie.</P>

## <a name="project-parameters"></a>Projectparameters

Als het veld **Ontslagen werknemers** op het tabblad **Journalen** in het formulier **Projectbeheer- en boekhoudingsparameters** is geselecteerd, kunt u inactieve werknemers en actieve werknemers in de formulieren **Serviceovereenkomsten** en **Serviceorders** selecteren.

Verder kunt u de velden **Begintijd** en **Eindtijd** op het tabblad **Project** in het formulier **Serviceorders** inschakelen om begin- en eindtijden op serviceorderregels in te voeren.

## <a name="enable-the-starting-and-ending-time-feature-for-service-orders"></a>De functie voor begin- en eindtijd voor serviceorders inschakelen

1.  Klik op **Projectbeheer en boekhouding** \> **Instellen** \> **Projectbeheer- en boekhoudingsparameters**.

2.  Klik op het tabblad **Journalen** en schakel het selectievakje **Begin-/eindtijden weergeven** in.

3.  Klik op **Projectbeheer en boekhouding** \> **Instellen** \> **Journalen** \> **Journaalnamen**.

4.  Selecteer de journaalnaam die aan de serviceorder is gekoppeld.

5.  Klik op het tabblad **Algemeen** en schakel het selectievakje **Begin-/eindtijden weergeven** in.


> [!NOTE]
> <P>Selecteer de journaalnaam voor de serviceorder in het veld <STRONG>Uur</STRONG> op het tabblad <STRONG>Journalen</STRONG> in het formulier <STRONG>Parameters voor servicebeheer</STRONG>.</P>





