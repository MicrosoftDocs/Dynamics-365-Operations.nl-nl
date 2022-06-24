---
title: Vaste activa koppelen met leases
description: In dit artikel wordt uitgelegd hoe u een bestaand vast activum aan een nieuwe lease koppelt.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseDetail
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 5cc341008d25da544ec35d5660b5ff0b38f2287b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895104"
---
# <a name="associate-fixed-assets-with-leases"></a>Vaste activa koppelen met leases

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit artikel wordt uitgelegd hoe u een bestaand vast activum aan een nieuwe lease koppelt. Wanneer u een vast activum koppelt aan een lease, wordt de waarde van het activum met gebruiksrecht (RoU) bij de eerste toerekening gebruikt als de verwervingskosten van het vaste activum.

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

Wanneer een lease is gekoppeld aan een vast activum, wordt het veld **Levensduur** in het vaste-activaboek bijgewerkt met de kleinste waarde uit de volgende criteria: 

 - De economische levensduur van het activum
 - De leasetermijn uit het gekoppelde leaseboek

Als het veld **Eigendomsoverdracht** is ingesteld op **Ja** voor het leaseboek, is de waarde in het veld **Levensduur** altijd de economische levensduur van het activum. 
 
De levensduur wordt elke keer bijgewerkt wanneer de lease wordt aangepast om ervoor te zorgen dat het activum met gebruiksrecht wordt afgeschreven gedurende de termijnlease, alsof het wordt afgeschreven in Activum leasen.

> [!NOTE]
> Als u een vast activum aan een lease koppelt, worden de knoppen **Afschrijving van activa** en **Leasewaardevermindering** uitgeschakeld in Activa leasen. U kunt transacties voor afschrijvingen van activa en waardevermindering voor leases weergeven in Vaste activa. De knop **Activatransacties**, waarmee een queryformulier wordt geopend, wordt ook uitgeschakeld. U kunt het queryformulier **Activatransacties** ook openen in Vaste activa.  

Op de pagina's **Vaste activa** en **Vaste-activaboek** wordt de lease-id weergegeven die aan een vast activum is gekoppeld. Als een vast activum aan een lease is gekoppeld, worden de lease-id en de leaseomschrijving weergegeven op het sneltabblad **Lease-informatie** op de pagina **Vaste activa**. Voor vaste-activaboeken die aan leaseboeken zijn gekoppeld, worden via de velden **Lease-id**, **Leaseomschrijving** en **Boektype** gegevens weergegeven over het geselecteerde vaste-activaboek op het sneltabblad **Leasegegevens** om aan te geven dat deze zijn gekoppeld aan een leaseboek.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
