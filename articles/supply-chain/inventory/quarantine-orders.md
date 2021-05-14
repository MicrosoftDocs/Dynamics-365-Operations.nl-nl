---
title: Quarantaineorders
description: In dit onderwerp wordt beschreven hoe quarantaineorders kunnen worden gebruikt om voorraad te blokkeren.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e1eed14b7d38cf569af7192dec9580e771f06df
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956177"
---
# <a name="quarantine-orders"></a>Quarantaineorders

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe quarantaineorders kunnen worden gebruikt om voorraad te blokkeren.

Met quarantaineorders kunt u voorraad blokkeren. U wilt bijvoorbeeld artikelen om redenen van kwaliteitscontrole in quarantaine plaatsen. Voorraad die in quarantaine is geplaatst, wordt verplaatst naar een quarantainemagazijn.

> [!NOTE]
> Als u gebruikmaakt van geavanceerde magazijnbeheerprocessen (in Magazijnbeheer), wordt quarantaineorderverwerking alleen gebruikt voor retourverkooporders.

## <a name="quarantine-on-hand-inventory-items"></a>Voorhanden voorraadartikelen in quarantaine plaatsen

Wanneer u artikelen in quarantaine plaatst, kunt u de quarantaineorders handmatig maken of het systeem zo instellen dat er automatisch quarantaineorders worden gemaakt tijdens de verwerking van inkomende artikelen.

Volg deze stappen om het systeem zo in te stellen dat het automatisch quarantaineorders genereert.

1. Ga naar **Voorraadbeheer \> Instellen \> Voorraad \> Artikelmodelgroepen**.
1. Selecteer een relevante modelgroep in het lijstvenster of maak een nieuwe modelgroep.
1. Schakel op het sneltabblad **Voorraadbeleid** het selectievakje **Quarantainebeheer** in.
1. Sluit de pagina.
1. Geef in het veld **Quarantainemagazijn** voor de ontvangende magazijnen een standaardquarantainemagazijn op.

Wanneer een artikel dat in het magazijn is geregistreerd als ontvangen, behoort tot een modelgroep waarvoor het selectievakje **Quarantainebeheer** is ingeschakeld, wordt er door het systeem een quarantaineorder voor dat artikel gegenereerd. De quarantaineorder geeft werknemers de opdracht om het artikel naar het quarantainemagazijn te verplaatsen.

Wanneer u quarantaineorders handmatig maakt op de pagina **Quarantaineorders**, hoeft het artikel niet te worden ingesteld voor quarantainebeheer in de gekoppelde artikelmodelgroep. Voor dit proces moet u de voorhanden voorraad opgeven die in quarantaine moet worden geplaatst, en het quarantainemagazijn dat moet worden gebruikt. U kunt de quarantaineorderstatussen gebruiken om het proces plannen.

## <a name="quarantine-order-statuses"></a>Statussen van quarantaineorder

Quarantaineorders kunnen de volgende status hebben:

- Gemaakt
- Gestart
- Gereedgemeld
- Beëindigd

### <a name="created"></a>Gemaakt

Wanneer een quarantaineorder handmatig is gemaakt, maar het artikel nog niet in het quarantainemagazijn is geplaatst, krijgt de quarantaineorder de status **Gemaakt**. Er worden twee voorraadtransacties gegenereerd. Eén transactie is een uitgiftetransactie die de status **In bestelling**, **Fysiek gereserveerd** of **Verzameld** kan hebben. De andere transactie is een ontvangsttransactie die de status **Besteld** of **Geregistreerd** in het quarantainemagazijn kan hebben. U kunt updates in de voorraad met de normale processen reserveren, kiezen en registreren.

### <a name="started"></a>Gestart

Wanneer een quarantaineorder de status **Gestart** heeft, wordt de voorraad verplaatst van het normale magazijn naar het quarantainemagazijn en worden twee voorraadtransacties gegenereerd. Een transactie heeft de status **Ingehouden** en de andere transactie heeft de status **Ontvangen**. Tegelijkertijd worden twee voorraadtransacties gemaakt voor het verwerken van de retouroverdracht. Deze transacties hebben geen datum. Een transactie heeft de status **Fysiek gereserveerd** en de andere transactie heeft de status **Besteld**.

### <a name="reported-as-finished"></a>Gereedgemeld

Als u een gestarte quarantaineorder gereed wilt melden, opent u de order en selecteert u **Rapporteren als gereed** in het actievenster. Het artikel wordt vrijgegeven uit quarantaine, maar wordt nog niet teruggeplaatst in het normale magazijn. De terugplaatsing in het normale magazijn kan worden verwerkt via een artikelontvangstjournaal, dat kan worden geïnitialiseerd tijdens het gereedmeldingsproces.

### <a name="ended"></a>Beëindigd

Wanneer een quarantaineorder wordt beëindigd, wordt het artikel vanuit het quarantainemagazijn teruggeplaatst naar het normale magazijn. De status van de artikeltransactie wordt ingesteld op *Verkocht* in het quarantainemagazijn en op *Ingekocht* in het normale magazijn.

## <a name="quarantine-order-scrap"></a>Quarantaineorderuitval

Als onderdeel van het quarantaineorderproces kunt u voorraad laten uitvallen. Wanneer u uitval verwerkt, wordt de status van de voorraad ingesteld op *Verkocht* door een uitgiftetransactie vanuit het quarantainemagazijn.

## <a name="additional-resources"></a>Aanvullende resources

- [Voorraadblokkering](inventory-blocking.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
