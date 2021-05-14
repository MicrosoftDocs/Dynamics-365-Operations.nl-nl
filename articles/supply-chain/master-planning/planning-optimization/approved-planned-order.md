---
title: Geplande orders weergeven, beheren en goedkeuren
description: Dit onderwerp bevat informatie over het weergeven, beheren en goedkeuren van geplande orders in Planningsoptimalisatie.
author: ChristianRytt
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 3b9b5274481e693f9fa05eb084ec5505ce5bc2eb
ms.sourcegitcommit: 9283caad2d0636f98579c995784abec19fda2e3f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935652"
---
# <a name="view-manage-and-approve-planned-orders"></a>Geplande orders weergeven, beheren en goedkeuren

[!include [banner](../../includes/banner.md)]

Dit onderwerp bevat informatie over het weergeven, beheren en goedkeuren van geplande orders in Planningsoptimalisatie.

## <a name="view-and-manage-planned-orders"></a><a name="view-planned-orders"></a>Geplande orders weergeven en beheren

U kunt geplande orders weergeven en beheren op elke lijstpagina met geplande orders. Ga naar een van de volgende locaties, afhankelijk van het type geplande orders waarmee u wilt werken:

- Hoofdplanning \> Werkgebieden \> Hoofdplanning
- Hoofdplanning \> Hoofdplanning \> Geplande orders
- Productiebeheer \> Productieorders \> Geplande productieorders
- Inkoop en sourcing \> Inkooporders \> Geplande inkooporders
- Voorraadbeheer \> Inkomende orders \> Geplande overboekingen
- Voorraadbeheer \> Uitgaande orders \> Geplande overboekingen

## <a name="view-and-edit-the-status-of-planned-orders"></a>De status van geplande orders weergeven bewerken

Met het veld **Status** van elke geplande order kunt u de voortgang bijhouden of wijzigen hoe een geplande order wordt verwerkt. De volgende **Status**-waarden zijn beschikbaar:

- **Niet-verwerkt**: Wanneer geplande orders door de hoofdplanning worden gegenereerd, hebben zij deze status. Geplande orders met deze status worden verwijderd tijdens de volgende planningsuitvoering.
- **Voltooid**: Deze status geeft aan dat de geplande order is voltooid. Wanneer u besluit een geplande order niet te fiatteren, kunt u handmatig de status wijzigen in *Voltooid*. Merk op dat de statussen *Niet-verwerkt* en *Voltooid* op dezelfde manier worden behandeld in het systeem.
- **Goedgekeurd**: Deze status geeft aan dat de geplande order is goedgekeurd voor fiattering. Als u een geplande order wilt fiatteren, kunt u de status ervan wijzigen in *Goedgekeurd*. Als u de bewerkingen wilt behouden die zijn gemaakt in een geplande order, of als u een geplande order wilt goedkeuren, wijzigt u de status in *Goedgekeurd*. Geplande orders met de status *Goedgekeurd* worden als vaststaand en verwachte levering beschouwd door de hoofdplanning. Ze worden dus niet gewijzigd of verwijderd tijdens een latere hoofdplanningsuitvoering. Om dit gedrag te bereiken, kopieert de planningslogica de geplande orders met de status *Goedgekeurd* van de oude planversie naar de nieuwe planversie tijdens de hoofdplanning. Merk op dat geplande orders met de status *Goedgekeurd* alleen als levering worden beschouwd in het specifieke hoofdplan.

Als u de status van een enkele geplande order wilt wijzigen, [opent u een lijstpagina met geplande orders](#view-planned-orders). Vervolgens opent u de order en volgt u een van deze stappen:

- Wijzig op het sneltabblad **Algemeen** de waarde van het veld **Status**.
- Selecteer vervolgens in het actievenster op het tabblad **Geplande order** in de groep **Verwerken** de optie **Status wijzigen**.
- Selecteer in het actievenster de optie **Goedkeuren** om de order te markeren als goedgekeurd.

Als u de status van meerdere geplande orders tegelijk wilt wijzigen, [opent u een lijstpagina met geplande orders](#view-planned-orders). Vervolgens schakelt u het selectievakje in voor alle orders die u wilt wijzigen en volgt u een van de volgende stappen:

- Selecteer vervolgens in het actievenster op het tabblad **Geplande order** in de groep **Verwerken** de optie **Status wijzigen**.
- Selecteer in het actievenster de optie **Goedkeuren** om de orders te markeren als goedgekeurd.

## <a name="approve-planned-orders"></a>Geplande orders goedkeuren

Goedkeuring van geplande orders is een optionele stap in het proces om een gefiatteerde order te maken op basis van een geplande order.

In de volgende afbeelding ziet u hoe u de **Status**-waarde die aan elke geplande order is toegewezen, kunt gebruiken om een goedkeuringsworkflow te implementeren. Als u een goedkeuringsproces wilt implementeren, past u de **Status**-waarde voor elke geplande order handmatig aan, zoals beschreven in de vorige sectie.

![Stroom geplande orders](media/approved-planned-orders-1.png)

> [!TIP]
> Het wordt aangeraden alle gewijzigde geplande orders goed te keuren. Als u dit niet doet, worden de bewerkingen genegeerd en overschreven bij de volgende planningsbewerking.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Vast geplande orders](planned-order-firming.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
