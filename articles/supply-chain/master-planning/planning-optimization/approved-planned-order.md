---
title: Geplande orders goedkeuren
description: Dit onderwerp beschrijft de goedkeuring van geplande orders die worden ondersteund in Planningsoptimalisatie.
author: ChristianRytt
manager: tfehr
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: b7975088be898ccecceb1f7be009cecff107f6e6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425416"
---
# <a name="approve-planned-orders"></a>Geplande orders goedkeuren

[!include [banner](../../includes/banner.md)]

Dit onderwerp bevat informatie over het bijwerken van de status van geplande orders in Planningsoptimalisatie.

De goedkeuring van geplande orders is een optionele stap in de procedure om een gefiatteerde order te maken op basis van een geplande order. Het wordt aanbevolen om gewijzigde geplande orders goed te keuren om te voorkomen dat de bewerkingen worden genegeerd en overschreven door de volgende planning.

![Stroom geplande orders](media/approved-planned-orders-1.png)

Via het veld **Status** kunt u uw voortgang in de gaten houden aan de hand van de volgende waarden:

- **Niet-verwerkt:** wanneer geplande orders door de hoofdplanning worden gegenereerd, hebben de geplande orders de status *Niet-verwerkt*. Geplande orders met deze status worden verwijderd tijdens de volgende planningsuitvoering.
- **Voltooid:** als u besluit een geplande order niet te fiatteren, kunt u de status wijzigen in *Voltooid* om aan te geven dat u de evaluatie van deze geplande order hebt voltooid. De statussen *Niet-verwerkt* en *Voltooid* worden op dezelfde manier behandeld in het systeem.
- **Goedgekeurd:** als u wijzigingen wilt behouden of van plan bent om een geplande order te fiatteren, wijzigt u de status in *Goedgekeurd*. Geplande orders met de status *Goedgekeurd* worden als vaststaand en verwachte levering beschouwd door de hoofdplanning. Ze worden dus niet gewijzigd of verwijderd tijdens een latere hoofdplanningsuitvoering. Om dit te bereiken, kopieert de planningslogica de *goedgekeurde* geplande orders van de oude planversie naar de nieuwe planversie tijdens de hoofdplanning. *Goedgekeurde* geplande orders worden alleen als levering beschouwd in het specifieke hoofdplan.

U kunt geplande orders vanuit de werkruimte **Hoofdplanning**, de lijst **Geplande order** of de lijsten **Geplande productieorders**, **Geplande inkooporders** en **Geplande overboeking** beheren.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]