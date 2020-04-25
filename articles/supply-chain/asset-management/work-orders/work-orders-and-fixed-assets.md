---
title: Werkorders en vaste activa
description: In dit onderwerp vindt u meer informatie over werkorders en vaste activa in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ca7a5d88de4308d7be9c1bc749b9dbf1da027c2c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208818"
---
# <a name="work-orders-and-fixed-assets"></a>Werkorders en vaste activa

[!include [banner](../../includes/banner.md)]


In Activabeheer kunnen activa worden gekoppeld aan vaste activa en kunt u werkorders voor deze activa maken. Als u deze functionaliteit gebruikt, kunt u een volledig overzicht krijgen van vaste activa, gerelateerde investeringsprojecten en de kosten die voor de investeringsprojecten zijn geregistreerd in de modules **Projectbeheer en boekhouding** en **Vaste activa** in Microsoft Dynamics 365 for Finance and Operations.

>[!NOTE]
>Het veld **Vaste-activanummer** in het project van de werkordertaak wordt alleen ingesteld als het projecttype **Investering** is geselecteerd in het project van de werkordertaak.

In de onderstaande afbeelding ziet u de relatie tussen een investeringsproject in de module **Projectbeheer en boekhouding** en het project van een werkorder.

![Figuur 1](media/24-work-orders.png)

De volgende procedure beschrijft de relatie tussen activa, werkorders, projecten van werkorderprojecttaken, en vaste activa.

1. U maakt een activum dat u aan een vast activum relateert.

![Figuur 2](media/25-work-orders.png)

2. Wanneer u werkordertypen op de pagina **Werkordertypen** instelt (**Activabeheer** > **Instellen** > **Werkorders** > **Werkordertypen**), maakt u een werkordertype voor de afhandeling van investeringen. Zie ook [Werkordertypen](../setup-for-work-orders/work-order-types.md).

![Figuur 3](media/26-work-orders.png)

3. Wanneer u werkorderprojectgroepen op het tabblad **Projectgroep** van de pagina **Projectinstellingen werkorder** instelt (**Activabeheer** > **Instellen** > **Werkorders** > **Projectinstellingen**Projectgroep), maakt u een relatie tussen het werkordertype dat wordt gebruikt voor investeringen en de projectgroep die voor investeringen is gemaakt op de pagina **Projectgroepen** van de module **Projectbeheer en boekhouding** (**Projectbeheer en boekhouding** > **Instellen** > **Boeking** > **Projectgroepen**).

![Figuur 4](media/27-work-orders.png)

4. Wanneer u een werkorder maakt die betrekking heeft op een vast activum, selecteert u het werkordertype dat wordt gebruikt voor de afhandeling van investeringen, bijvoorbeeld **Investering**.

5. Wanneer de werkorder is gemaakt, wordt het bijbehorende werkordertype weergegeven op de pagina **Alle werkorders**.

![Figuur 5](media/28-work-orders.png)

6. Wanneer de werkorder is gemaakt, wordt het project dat aan de werkorder is gekoppeld, gemaakt op de pagina **Alle projecten** van de module **Projectbeheer en boekhouding** (**Projectbeheer en boekhouding** > **Projecten** > **Alle projecten**). Als u projectgerelateerde informatie wilt bekijken, selecteert u de koppeling in het veld **Project-id** op het tabblad **Algemeen** van het sneltabblad **Regeldetails** in de detailweergave van de pagina **Alle werkorders** van de module **Activabeheer** (**Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders**).

![Figuur 6](media/29-work-orders.png)

7. Als u een overzicht wilt weergeven van de projecten die aan een vast activum zijn gekoppeld, selecteert u **Vaste activa** > **Vaste activa** > **Vaste activa** en selecteert u vervolgens in het veld **Vaste-activanummer** de koppeling naar het vaste activum om de detailweergave te openen. Vouw het deelvenster **Gerelateerde informatie**, rechts van de pagina, uit en selecteer het sneltabblad **Gekoppelde projecten**.

