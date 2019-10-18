---
title: Werkorders en vaste activa
description: In dit onderwerp vindt u meer informatie over werkorders en vaste activa in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 95fe394d22f9fe81511c230a2cf7b8ddf00d896f
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250824"
---
# <a name="work-orders-and-fixed-assets"></a>Werkorders en vaste activa


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


In Activabeheer kunnen activa worden gekoppeld aan vaste activa en kunt u werkorders voor deze activa maken. Als u deze functionaliteit gebruikt, kunt u een volledig overzicht krijgen van vaste activa, gerelateerde investeringsprojecten en de kosten die voor de investeringsprojecten zijn geregistreerd in de module **Projectbeheer en boekhouding** en de module **Vaste activa**.

>[!NOTE]
>Het veld **Vaste-activanummer** wordt alleen ingevuld in het project van de werkordertaak als het projecttype 'Investering' is geselecteerd in het project van de werkordertaak.

![Figuur 1](media/24-work-orders.png)

De volgende procedure beschrijft de relatie tussen activa, werkorders, projecten van werkorderprojecttaken, en vaste activa.

1. U maakt een activum dat u wilt relateren aan vaste activa, zoals in de volgende afbeelding wordt weergegeven.

![Figuur 2](media/25-work-orders.png)

2. Wanneer u werkordertypen instelt (**Activabeheer** > **Instellen** > **Werkorders** > **Werkordertypen**), maakt u een werkordertype voor de afhandeling van investeringen. Zie ook [Werkordertypen](../setup-for-work-orders/work-order-types.md).

![Figuur 3](media/26-work-orders.png)

3. Wanneer u werkorderprojectgroepen instelt (koppeling **Activabeheer** > **Instellen** > **Werkorders** > **Projectinstellingen** > **Projectgroep**), maakt u een relatie tussen het werkorder type dat wordt gebruikt voor investeringen en de projectgroep die voor investeringen is gemaakt in de module **Projectbeheer en boekhouding** (**Projectbeheer en boekhouding** > **Instellen** > **Boeking** > **Projectgroepen**).

![Figuur 4](media/27-work-orders.png)

4. Wanneer u een werkorder maakt die betrekking heeft op een vaste-activaobject, selecteert u het werkordertype dat voor de afhandeling van investeringen wordt gebruikt, bijvoorbeeld 'Investering'.

5. Wanneer de werkorder wordt gemaakt, wordt het bijbehorende werkordertype weergegeven in **Alle werkorders**.

![Figuur 5](media/28-work-orders.png)

6. Wanneer de werkorder wordt gemaakt, wordt het project dat aan de werkorder is gerelateerd, gemaakt in **Projectbeheer en boekhouding** > **Alle projecten**. U kunt projectgerelateerde informatie bekijken door in de werkorder op de koppeling **Project-id** te klikken (open in **Activabeheer** de werkorder in de Detailweergave > sneltabblad **Regeldetails** > tabblad **Algemeen** > veld **Project-id**).

![Figuur 6](media/29-work-orders.png)

7. In **Vaste activa** kunt u een overzicht bekijken van de projecten die zijn gekoppeld aan vaste activa (**Vaste activa** > **Vaste activa** > **Vaste activa** > klik op het vaste activum in het veld **Vaste-activanummer** > bekijk de inhoud in het deelvenster **Gerelateerde informatie** >sectie **Gekoppelde projecten**).

