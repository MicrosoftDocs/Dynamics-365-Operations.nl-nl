---
title: Onkostennota's en meerdere goedkeurders
description: "In dit onderwerp vindt u informatie over onkostennota's die moeten worden goedgekeurd door meer dan één persoon."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 0f7592c580a21040c8b630885939ceaab3855c2c
ms.contentlocale: nl-nl
ms.lasthandoff: 03/13/2018

---

# <a name="expense-reports-and-multiple-approvers"></a>Onkostennota's en meerdere goedkeurders

[!INCLUDE [banner](../includes/banner.md)]

Afhankelijk van het goedkeuringsbeleid voor onkosten van uw organisatie moet mogelijk meer dan één persoon een onkostendeclaratie goedkeuren die door een werknemer wordt ingediend. Wanneer u de werkstroom voor goedkeuring van het onkostenrapport instelt, kunt u werkstroomelementen toevoegen die taken of stappen voor één of meerdere goedkeurders van onkostenrapporten bevatten. U kan bijvoorbeeld vereisen dat alle onkostendeclaraties eerst worden goedgekeurd door de manager van de werknemer die het rapport ingediend heeft en vervolgens door de coördinator Crediteuren.

Indien u meerdere goedkeurders van onkostendeclaraties vereist, kunt u de workflowelementen op een van de volgende manieren toevoegen:

- Voeg één goedkeuringselement toe dat één stap omvat. In deze stap kan bijvoorbeeld vereist worden dat een onkostendeclaratie wordt toegewezen aan een gebruikersgroep en dat deze door 50% van de leden van de gebruikersgroep goedgekeurd moet worden.
- Voeg één goedkeuringselement toe dat meerdere stappen omvat. De stappen in het goedkeuringselement zijn bijvoorbeeld als volgt:

    1. De manager van de werknemer die de onkostendeclaratie heeft ingediend keurt deze goed.
    2. De medewerker Crediteuren controleert de items van de onkostendeclaratie.
    3. De budgeteigenaar keurt de onkostendeclaratie goed.

- Voeg meerdere goedkeuringselementen toe die allemaal één stap bevatten. U kunt bijvoorbeeld een afzonderlijk goedkeuringselement toevoegen voor elk van de volgende stappen:

    1. De manager van de werknemer keurt de onkostendeclaratie goed.
    2. De budgeteigenaar keurt de onkostendeclaratie goed.

