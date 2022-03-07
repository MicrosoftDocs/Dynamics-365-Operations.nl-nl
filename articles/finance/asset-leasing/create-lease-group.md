---
title: Een leasegroep maken
description: In dit onderwerp wordt uitgelegd hoe u leasegroepen instelt. Leasegroepen zijn vereist om nieuwe leases te maken.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseGroupTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 88a49e4db868078fd05875df33ca5727363aaa18
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881223"
---
# <a name="create-a-lease-group"></a>Een leasegroep maken

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u leasegroepen instelt. Leasegroepen zijn vereist om nieuwe leases te maken. Aan elke leasegroep zijn leaseboeken gekoppeld. Leaseboeken bepalen de standaardboeken die voor elke lease moeten worden gemaakt. U kunt specifieke rekeningen aan een leasegroep toewijzen op de pagina **Leaseboekingsparameters**.

## <a name="create-a-lease-book-and-add-a-lease-group"></a>Een leaseboek maken en een leasegroep toevoegen

1. Ga naar **Activa leasen \> Instellen \> Leasegroepen**.
2. Selecteer **Nieuw** in het actievenster om een leasegroep toe te voegen. Er wordt een regel aan het raster toegevoegd.
3. Voer op de nieuwe regel in het veld **Leasegroep** een waarde in.
4. Voer een waarde in het veld **Beschrijving** in.

De informatie die u zojuist hebt ingevoerd, wordt toegevoegd aan het veld **Leasegroep** op de pagina **Lease toevoegen**.

## <a name="associate-a-book-with-a-lease-group"></a>Een boek aan een leasegroep koppelen

Nadat u leasegroepen hebt gemaakt, kunt u boeken aan elke groep toewijzen. Wanneer u een lease maakt en deze aan een leasegroep toewijst, maakt het systeem een set schema's voor elk boek dat aan die leasegroep is gekoppeld.

> [!NOTE]
> Boeken moeten worden ingesteld voordat ze aan een leasegroep kunnen worden toegewezen.

1. Ga naar **Activa leasen \> Instellen \> Leasegroep**.
2. Selecteer een leasegroep en selecteer vervolgens **Boeken**.
3. Selecteer **Nieuw** en selecteer vervolgens in het veld **Boektype** het boek dat u wilt toewijzen aan de leasegroep. U kunt meerdere boeken aan een leasegroep toewijzen als een lease op verschillende manieren moet worden verwerkt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
