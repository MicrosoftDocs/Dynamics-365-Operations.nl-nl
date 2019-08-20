---
title: Persoonlijke onkosten in een onkostennota
description: In dit onderwerp worden de twee methoden uitgelegd voor het verwerken van de persoonlijke uitgaven van een medewerker in Microsoft Dynamics 365 for Finance and Operations.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b072fa9e78563d3e89b4d60e9ce61473902fee76
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/30/2019
ms.locfileid: "1794978"
---
# <a name="personal-expenses-on-an-expense-report"></a>Persoonlijke onkosten in een onkostennota

[!include [banner](../includes/banner.md)]

Tijdens zakenreizen kan het voorkomen dat werknemers persoonlijke uitgaven afrekenen met een creditcard van het bedrijf. Als u geen proces voor het verwerken van persoonlijke onkosten definieert, kan het goedkeuringsproces voor onkostennota's worden verstoord wanneer de werknemers de gespecificeerde onkostennota's indienen. 

Microsoft Dynamics 365 for Finance and Operations biedt twee methoden voor de verwerking van de persoonlijke onkosten van een werknemer:

- **Door werknemer betaald**: de persoonlijke onkosten op de rekening van de creditcard van het bedrijf worden niet door de organisatie betaald. Er wordt een rapport gemaakt met zowel de persoonlijke onkosten als de bedrijfsonkosten die zijn betaald met de creditcard van het bedrijf.
- **Door bedrijf betaald**: uw bedrijf betaalt de hele rekening van de creditcard van het bedrijf en schrijft de persoonlijke onkosten vervolgens af van de rekening van de werknemer.

Selecteer de methode voor uw organisatie op de pagina **Parameters onkostenbeheer**.
