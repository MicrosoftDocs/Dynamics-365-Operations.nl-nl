---
title: Vaste activa koppelen met leases
description: In dit onderwerp wordt uitgelegd hoe u een bestaand vast activum aan een nieuwe lease koppelt.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d627633e43c2e6f5cad90dfe4100ff95a71541f7
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442168"
---
# <a name="associate-fixed-assets-with-leases"></a>Vaste activa koppelen met leases

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u een bestaand vast activum aan een nieuwe lease koppelt. Wanneer u een vast activum koppelt aan een lease, wordt de waarde van het activum met gebruiksrecht (RoU) bij de eerste toerekening gebruikt als de verwervingskosten van het vaste activum.

Voordat u een vast activum aan een lease kunt koppelen, moet u een record voor het vaste activum maken in Vaste activa. Vervolgens maakt u op de pagina **Leaseoverzicht** een lease en koppelt u het activum aan die lease.

1. Voeg een lease toe door de stappen te volgen in [Leases toevoegen of kopiëren](add-lease.md). Selecteer op de pagina **Lease toevoegen** in het veld **Vaste-activanummer** het activum dat nog niet is aangeschaft.
2. Selecteer **Boeken** en bevestig het betalingsschema.
3. Selecteer **Initiële toerekening**.
4. Selecteer **Activaleasejournaal**.

    Met de journaalpost voor eerste toerekening van de lease wordt het vaste activum gedebiteerd voor het bedrag dat meestal wordt gedebiteerd van de rekening voor het RoU-activum.

    U kunt nu het transactietype en boek voor het vaste activum weergeven.

5. Selecteer **Journaaldetails**.
6. Selecteer **Regels** om de afzonderlijke regels voor de journaalboeking weer te geven.
7. Selecteer de journaalregel die de activa bevat en selecteer vervolgens het tabblad **Vaste activa**.

    Op het tabblad **Vaste activa** ziet u het transactietype en het boek. Standaard wordt het veld **Transactietype** ingesteld op **Verwerving** en het veld **Boek** op het huidige boek voor het vaste activum.

Nadat u de journaalboeking voor de eerste toerekening hebt uitgevoerd, wordt de transactie weergegeven als een verwervingstransactie voor het vaste activum. Als u de transactietabel wilt weergeven, gaat u naar **Vaste activa \> Vaste activa \> Vaste activa**, selecteert u het betreffende activum en vervolgens **Waarderingen**. U kunt zien dat met de journaalboeking voor de eerste toerekening een verwervingstransactie is gemaakt voor het opgegeven vaste activum.

De vaste activa kunnen nu worden afgeschreven met de standaard afschrijvingsfunctionaliteit in Vaste activa. Zie voor meer informatie [Afschrijvingsmethoden en conventies](../fixed-assets/depreciation-methods-conventions.md).

> [!NOTE]
> Als u een vast activum aan een lease koppelt, worden de knoppen **Afschrijving van activa** en **Leasewaardevermindering** uitgeschakeld in Activa leasen. U kunt transacties voor afschrijvingen van activa en waardevermindering voor leases weergeven in Vaste activa. De knop **Activatransacties**, waarmee een queryformulier wordt geopend, wordt ook uitgeschakeld. U kunt het queryformulier **Activatransacties** ook openen in Vaste activa.  
