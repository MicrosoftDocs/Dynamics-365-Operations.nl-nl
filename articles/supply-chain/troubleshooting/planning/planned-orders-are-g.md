---
title: Tijdens de hoofdplanning worden geplande orders voor phantom-producten gegenereerd
description: Geplande orders worden gegenereerd voor phantom-producten nadat de hoofdplanning is uitgevoerd.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: anderso
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f3170bcb723e2d7483258bb0ecf786e62f2aa3d196745074c2ac554bc212ec55
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741999"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a>Tijdens de hoofdplanning worden geplande orders voor phantom-producten gegenereerd

KB-nummer: 4614729

## <a name="symptoms"></a>Symptomen

Geplande orders worden gegenereerd voor phantom-producten nadat de hoofdplanning is uitgevoerd.

## <a name="resolution"></a>Oplossing

De instelling van de optie **Phantom** voor vrijgegeven producten bepaalt het standaardregeltype op de stuklijst. Wanneer de optie **Phantom** is ingesteld op *Ja*, worden er nog steeds geplande orders gemaakt voor het artikel, maar de optie **Rechtstreeks afgeleide behoefte** voor elke geplande order wordt ingesteld op *Ja*. De geplande productieorder kan daarom niet alleen worden gefiatteerd. In plaats daarvan wordt deze altijd automatisch opgenomen wanneer de bovenliggende productieorder wordt gefiatteerd. Daarnaast worden de stuklijstregels van de geplande phantom-order opgenomen in de stuklijst van de bovenliggende productieorder.
