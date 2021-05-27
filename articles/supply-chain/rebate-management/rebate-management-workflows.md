---
title: Werkstromen voor kortingsbeheerdeals
description: In dit onderwerp wordt uitgelegd hoe u een werkstroom voor kortingsbeheer kunt instellen om deals goed te keuren en te activeren.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: ee342de6d069131e230120c5d65aef58da8e632a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020381"
---
# <a name="rebate-management-deal-workflows"></a>Werkstromen voor kortingsbeheerdeals

[!include [banner](../includes/banner.md)]

Voor het goedkeuren van kortingsaanbiedingen wordt in Kortingsbeheer hetzelfde werkstroomplatform gebruikt als in andere Finance and Operations-toepassingen. Aan elke werkstroom zijn twee taakprocessen gekoppeld:

- Eén element van de werkstroom activeert de deal zodat de gebruiker of het werkstroomproces de transacties kan goedkeuren.
- Eén element van de werkstroom keurt de deal goed.

Voordat u een kortingsdeal kunt gebruiken, moet deze actief zijn in de module **Kortingsbeheer**. Als u een deal wilt activeren, moet u eerst een werkstroom maken en configureren voor *Werkstroom voor kortingsbeheerdeals*.

Nadat een werkstroom is geactiveerd voor kortingsbeheer, kunnen gebruikers niet handmatig deals goedkeuren. De werkstroom moet altijd worden gebruikt.

## <a name="create-and-manage-rebate-management-deal-workflows"></a>Werkstromen voor kortingsbeheerdeals maken en beheren

Als u wilt werken met uw werkstromen voor kortingsbeheerdeals, gaat u naar **Kortingsbeheer \> Instellen \> Werkstromen voor kortingsbeheer**. Hier kunt u werkstromen weergeven, maken en bijwerken. Er kan slechts één werkstroom van dit type tegelijk actief zijn. Zie [Overzicht van werkstroomsysteem](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) en de gerelateerde onderwerpen voor meer informatie over werkstromen, hoe u werkt met de pagina **Werkstromen voor kortingsbeheer** en hoe u werkstromen maakt.

## <a name="use-a-workflow-to-activate-a-deal"></a>Een werkstroom gebruiken om een deal te activeren

Als u een deal wilt activeren via een werkstroom, opent u de deal (bijvoorbeeld op de pagina **Alle kortingsbeheerdeals**). Selecteer vervolgens **Werkstroom \> Indienen** in het actievenster Nadat de nieuwe deal is verwerkt en goedgekeurd via de werkstroom, is deze actief en klaar voor gebruik.

Nadat een deal is geactiveerd, kunt u de instellingen ervan niet wijzigen. Als u een actieve deal moet wijzigen, deactiveert u deze en maakt u vervolgens een nieuwe deal. Als de nieuwe deal op de oude overeenkomst lijkt, kunt u deze maken door de oude deal te kopiëren.
