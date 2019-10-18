---
title: Vertraagde belastingberekening inschakelen in journaal
description: In dit onderwerp wordt uitgelegd hoe u de functie **Vertraagde belastingberekening inschakelen in journaal** gebruikt om de belastingberekening te verbeteren bij een groot volume van journaalregels.
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
ms.openlocfilehash: 5a8ae30a007d3e2b8b7a9bc9eb7786f6e58246d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177123"
---
# <a name="enable-delayed-tax-calculation-on-journal"></a>Vertraagde belastingberekening inschakelen in journaal
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit onderwerp wordt uitgelegd hoe u de functie **Vertraagde belastingberekening inschakelen in journaal** gebruikt om de belastingberekening te verbeteren bij een groot volume van journaalregels.

Het huidige gedrag van btw-berekening in journaal wordt tijdens real-time geactiveerd wanneer de gebruiker btw-gerelateerde velden bijwerkt, bijvoorbeeld btw-groep/btw-groep van artikel. Bij een update op journaalregelniveau wordt het btw-bedrag op alle journaalregels opnieuw berekend. Het helpt de gebruiker om het real-time berekende belastingbedrag te zien, maar dit kan ook tot prestatieproblemen leiden bij een groot aantal journaalregels.

Deze functie biedt een optie om de belastingberekening te vertragen om de prestatieproblemen op te lossen. Als deze functie is ingeschakeld, wordt het btw-bedrag alleen berekend wanneer de gebruiker op de opdracht "Btw" klikt of het journaal boekt.

Gebruiker kan de parameter op drie niveaus in- of uitschakelen:
- Per rechtspersoon
- Per journaalnaam
- Per journaalkoptekst

Het systeem zal de parameterwaarde in de journaalkoptekst opnemen als definitief. De parameterwaarde op de journaalkoptekst wordt standaard opgehaald uit de journaalnaam. De parameterwaarde in de journaalnaam wordt standaard opgehaald uit de grootboekparameter wanneer de journaalnaam wordt gemaakt.

De velden "Werkelijk btw-bedrag" en "Berekend btw-bedrag" in het journaal worden verborgen als deze parameter wordt ingeschakeld. Dit is om de gebruiker niet in verwarring te brengen, omdat de waarde van deze twee velden altijd 0 aangeeft voordat de belastingberekening door de gebruiker wordt geactiveerd.

## <a name="enable-delayed-tax-calculation-by-legal-entity"></a>Berekening van vertraagde btw per rechtspersoon inschakelen

1. Ga naar **Grootboek > Grootboek instellen > Grootboekparameters**
2. Klik op het tabblad **Btw**
3. Zoek op het sneltabblad **Algemeen** de parameter **Vertraagde belastingberekening** en schakel deze in/uit

![](media/delayed-tax-calculation-gl.png)



## <a name="enable-delayed-tax-calculation-by-journal-name"></a>Vertraagde belastingberekening inschakelen per journaalnaam

1. Ga naar **Grootboek > Journaalinstellingen > Journaalnamen**
2. Zoek op het sneltabblad **Algemeen** de parameter **Vertraagde belastingberekening** en schakel deze in/uit

![](media/delayed-tax-calculation-journal-name.png)

## <a name="enable-delayed-tax-calculation-by-journal"></a>Vertraagde belastingberekening inschakelen per journaal

1. Ga naar **Grootboek > Journaalboekingen > Algemene journalen**
2. Klik op **Nieuw**
3. Selecteer een journaalnaam
4. Klik op **Instellen**
5. Zoek de parameter **Vertraagde belastingberekening** en schakel deze in/uit

![](media/delayed-tax-calculation-journal-header.png)
