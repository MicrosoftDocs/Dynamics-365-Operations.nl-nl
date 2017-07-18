---
title: Quarantaineorders
description: In dit artikel wordt beschreven hoe quarantaineorders worden gebruikt om voorraad te blokkeren.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: ec3d54e8e08850cd81891e7058b2b787e08b0fb9
ms.contentlocale: nl-nl
ms.lasthandoff: 06/13/2017

---

# <a name="quarantine-orders"></a>Quarantaineorders

[!include[banner](../includes/banner.md)]


In dit artikel wordt beschreven hoe quarantaineorders worden gebruikt om voorraad te blokkeren. 

Quarantaineorders kunnen worden gebruikt om voorraad te blokkeren. U wilt bijvoorbeeld artikelen om redenen van kwaliteitscontrole in quarantaine plaatsen. Voorraad die in quarantaine is geplaatst, wordt verplaatst naar een quarantainemagazijn. **Opmerking:** als u gebruikmaakt van geavanceerde magazijnbeheerprocessen (in Magazijnbeheer), wordt quarantaineorderverwerking alleen gebruikt voor retourverkooporders.

## <a name="quarantine-onhand-inventory-items"></a>Voorhanden voorraadartikelen in quarantaine plaatsen
Wanneer u artikelen in quarantaine plaatst, kunt u de quarantaineorders handmatig maken of het systeem zo instellen dat de quarantaineorders automatisch worden gemaakt tijdens inkomende verwerking. Als u quarantaineorders automatisch wilt maken, selecteert u de optie **Quarantainebeheer** op het tabblad **Voorraadbeleid** op de pagina **Artikelmodelgroepen**. U moet ook een standaardquarantainemagazijn opgeven in het veld **Quarantainemagazijn** voor de magazijnen van ontvangst. Wanneer de fysiek voorhanden voorraad wordt geregistreerd in een inkooporder of productieorder, worden in quarantaine geplaatste artikelen automatisch verplaatst naar een quarantainemagazijn in Microsoft Dynamics 365 for Finance and Operations. Deze verplaatsing vindt plaats omdat de status van de quarantaineorder is gewijzigd in **Gestart**. Wanneer u quarantaineorders handmatig maakt, hoeft het artikel niet te worden ingesteld voor quarantainebeheer in de gekoppelde artikelmodelgroep. Voor dit proces moet u de voorhanden voorraad opgeven die in quarantaine moet worden geplaatst, en het quarantainemagazijn dat moet worden gebruikt. U kunt de quarantaineorderstatussen gebruiken om het proces plannen.

## <a name="quarantine-order-statuses"></a>Statussen van quarantaineorder
Quarantaineorders kunnen de volgende status hebben:

-   Gemaakt
-   Gestart
-   Gereedgemeld
-   Beëindigd

### <a name="created"></a>Gemaakt

Wanneer een quarantaineorder handmatig is gemaakt, maar het artikel nog niet in het quarantainemagazijn is geplaatst, krijgt de quarantaineorder de status **Gemaakt**. Er worden twee voorraadtransacties gegenereerd. Eén transactie is een uitgiftetransactie die de status **In bestelling**, **Fysiek gereserveerd** of **Verzameld** kan hebben. De andere transactie is een ontvangsttransactie die de status **Besteld** of **Geregistreerd** in het quarantainemagazijn kan hebben. U kunt updates in de voorraad met de normale processen reserveren, kiezen en registreren.

### <a name="started"></a>Gestart

Wanneer een quarantaineorder de status **Gestart** heeft, wordt de voorraad verplaatst van het normale magazijn naar het quarantainemagazijn en worden twee voorraadtransacties gegenereerd. Een transactie heeft de status **Ingehouden** en de andere transactie heeft de status **Ontvangen**. Tegelijkertijd worden twee voorraadtransacties gemaakt voor het verwerken van de retouroverdracht. Deze transacties hebben geen datum. Een transactie heeft de status **Fysiek gereserveerd** en de andere transactie heeft de status **Besteld**.

### <a name="reported-as-finished"></a>Gereedgemeld

Als u op **Rapporteren als gereed** klikt, kunt u een gestarte quarantaineorder gereedmelden. Het artikel wordt vrijgegeven uit quarantaine, maar wordt nog niet naar het normale magazijn teruggeplaatst. Dit kan worden verwerkt via een artikelontvangstjournaal dat tijdens het proces voor gereedmelding kan worden geïnitialiseerd.

### <a name="ended"></a>Beëindigd

Wanneer een quarantaineorder wordt beëindigd, wordt het artikel vanuit het quarantainemagazijn teruggeplaatst naar het normale magazijn. De status van de artikeltransactie wordt ingesteld op **Verkocht** in het quarantainemagazijn en op **Ingekocht** in het normale magazijn.

## <a name="quarantine-order-scrap"></a>Quarantaineorderuitval
Als onderdeel van het quarantaineorderproces kunt u voorraad laten uitvallen. Wanneer u uitval verwerkt, wordt de status van de voorraad ingesteld op **Verkocht** door een uitgiftetransactie vanuit het quarantainemagazijn.

<a name="see-also"></a>Zie ook
--------

[Voorraadblokkering](inventory-blocking.md)




