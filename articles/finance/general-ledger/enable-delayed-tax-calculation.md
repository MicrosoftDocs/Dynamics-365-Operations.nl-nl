---
title: Vertraagde belastingberekening inschakelen in journalen
description: In dit onderwerp wordt uitgelegd hoe u de functie Vertraagde belastingberekening inschakelt om de belastingberekening te helpen verbeteren als het aantal journaalregels zeer groot is.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: e336be5468106007e1f5adf26bf272c88b8b413b
ms.sourcegitcommit: bc9b65b73bf6443581c2869a9ecfd0675f0be566
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/15/2019
ms.locfileid: "2623516"
---
# <a name="enable-delayed-tax-calculation-on-journals"></a>Vertraagde belastingberekening inschakelen in journalen
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit onderwerp wordt uitgelegd hoe u btw-berekening in journalen kunt vertragen. Deze mogelijkheid helpt de prestaties van belastingberekeningen te verbeteren wanneer er veel journaalregels zijn.

Standaard worden btw-bedragen op journaalregels berekend telkens wanneer btw-gerelateerde velden worden bijgewerkt. Deze velden bevatten de velden voor btw-groepen en btw-groepen voor artikelen. Eventuele wijzigingen in een journaalregel leiden ertoe dat belastingbedragen opnieuw worden berekend voor alle journaalregels. Hoewel gebruikers hiermee belastingbedragen kunnen zien die in realtime zijn berekend, kan dit ook invloed hebben op de prestaties als het aantal journaalregels erg groot is.

Met de functie Vertraagde belastingberekening kunt u de btw-berekening in journalen vertragen en zodoende prestatieproblemen oplossen. Als deze functie is ingeschakeld, worden btw-bedragen alleen berekend wanneer een gebruiker **Btw** selecteert of het journaal boekt.

U kunt de berekening van de btw op drie niveaus vertragen:

- Rechtspersoon
- Journaalnaam
- Journaalkoptekst

Het systeem geeft prioriteit aan de instelling voor de journaalkoptekst. Standaard wordt deze instelling overgenomen van de journaalnaam. De instelling voor de journaalnaam wordt standaard overgenomen van de instelling op de pagina **Grootboekparameters** wanneer de journaalnaam wordt gemaakt. In de volgende secties wordt uitgelegd hoe u vertraagde belastingberekening inschakelt voor rechtspersonen, journaalnamen en journaalkopteksten.

## <a name="turn-on-delayed-tax-calculation-at-the-legal-entity-level"></a>Vertraagde btw-berekening inschakelen op het niveau van de rechtspersoon

1. Ga naar **Grootboek \> Grootboek instellen \> Grootboekparameters**.
2. Stel op het tabblad **Btw** op het sneltabblad **Algemeen** de optie **Vertraagde belastingberekening** in op **Ja**.

![Afbeelding van grootboekparameters](media/delayed-tax-calculation-gl.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-name-level"></a>Vertraagde btw-berekening inschakelen op het niveau van de journaalnaam

1. Ga naar **Grootboek \> Journaalinstellingen \> Journaalnamen**.
2. Stel in de sectie **Btw** op het sneltabblad **Algemeen** de optie **Vertraagde belastingberekening** in op **Ja**.

![Afbeelding van journaalnamen](media/delayed-tax-calculation-journal-name.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-header-level"></a>Vertraagde btw-berekening inschakelen op het niveau van de journaalkoptekst

1. Ga naar **Grootboek \> Journaalboekingen \> Algemene journalen**.
2. Selecteer **Nieuw**.
3. Selecteer een journaalnaam.
4. Stel op het tabblad **Instellingen** de optie **Vertraagde belastingberekening** in op **Ja**.

![Afbeelding van grootboekpagina](media/delayed-tax-calculation-journal-header.png)
