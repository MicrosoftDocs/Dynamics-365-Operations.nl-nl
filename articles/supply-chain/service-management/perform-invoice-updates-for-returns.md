---
title: Facturen bijwerken voor retouren
description: Deze functionaliteit ondersteunt de bedrijfsprocessen van organisaties die ervoor kiezen retourorders en verkooporders tegelijkertijd en door dezelfde persoon te laten factureren.
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 53ae1c3bda06d07a0ca633981ddd46092eae507e
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---


# <a name="perform-invoice-updates-for-returns"></a>Facturen bijwerken voor retouren 

[!include [banner](../includes/banner.md)]


Een retourorder is een type verkooporder dat is gemarkeerd als een retourorder. De lijstpagina **Alle verkooporders** wordt daarom gebruikt voor het genereren van facturen voor retourorders in plaats van het formulier **Retourorders**. Deze functionaliteit ondersteunt de bedrijfsprocessen van organisaties die ervoor kiezen retourorders en verkooporders tegelijkertijd en door dezelfde persoon te laten factureren.

Omdat de factuur voor een geretourneerd artikel voor een negatief bedrag is, wordt deze een creditnota genoemd.

Wanneer u het bijwerken van de factuur instelt op batchverwerking, moet de verkooporder van het type **Geretourneerde order** de retourregelstatus **Ontvangen** hebben. Dit duidt erop dat de pakbon van de order is bijgewerkt.

## <a name="post-an-invoice-for-a-return-order"></a>Boek een factuur voor de retourorder.

1.  Klik op **Klanten** \> **Algemeen** \> **Verkooporders** \> **Alle verkooporders**.

2.  Selecteer een verkooporder waarvoor **Geretourneerde order** wordt weergegeven in het veld **Ordertype**.

3.  Klik in het actievenster op het tabblad **Factuur** in de groep **Genereren** op **Factuur**.

4.  Schakel op het tabblad **Parameters** het selectievakje **Boeking** in.

5.  Bekijk de informatie in het formulier en breng de wijzigingen aan die nodig zijn.

6.  Klik tot slot op **OK**. De creditnota wordt geboekt.

## <a name="see-also"></a>Zie ook

[Pakbonnen bijwerken voor retouren](packing-slip-updates-returns.md)

  



