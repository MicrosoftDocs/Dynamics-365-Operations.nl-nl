---
title: niet-gedocumenteerd
description: Een actiebericht is een door het systeem gegenereerde suggestie om een bestaande geplande of gefiatteerde order te wijzigen.
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-07 09 - 21 - 54
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19411
ms.assetid: 52b46d93-7d02-46b5-aad1-9fd08206bf9d
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f2ac69ddf485139b057dafa20e5f1a961fc32067
ms.lasthandoff: 03/29/2017


---

# <a name="undocumented"></a>niet-gedocumenteerd

Een actiebericht is een door het systeem gegenereerde suggestie om een bestaande geplande of gefiatteerde order te wijzigen.

### <a name="introduction"></a>Introductie

Actieberichten worden gegenereerd door de hoofdplanningberekening als reactie op vereisten die zijn gewijzigd. De verzenddatum of de hoeveelheid kan bijvoorbeeld zijn gewijzigd in een verkooporder waarvoor u al een inkooporder hebt gemaakt om aan de vraag te voldoen. In dit geval worden een of meerdere actieberichten gegenereerd door de hoofdplanningberekening om de inkooporder bij te werken. U beslist of u de aanbevolen wijzigingen aanbrengt.

U kunt configureren hoe actieberichten worden berekend voor een behoefteplanningsgroep die u aan een artikel koppelt.

 <a name="selecting-action-messages"></a>Actieberichten selecteren
==========================

Op de pagina **Behoefteplanningsgroepen** kunt u de actieberichten selecteren die het systeem moet genereren, en de behoefteplanningsgroepen of items waar de berichten van toepassing op zijn. U kunt de volgende actieberichten selecteren.

| Bericht             | Beschrijving                                                                                                                                                                                                                                              |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Vervroegen**         | Als u dit bericht selecteert, genereert het systeem wanneer nodig actieberichten om orders naar een eerdere datum te verplaatsen. In het veld **Marge voor vervroegen** kunt u ook het maximumaantal dagen tussen ontvangst en uitgifte zonder vervroegde actie opgeven. |
| **Uitstellen**        | Als u dit bericht selecteert, genereert het systeem wanneer nodig actieberichten om orders naar een latere datum te verplaatsen. In het veld **Marge voor uitstellen** kunt u het maximumaantal dagen tussen ontvangst en uitgifte zonder uitstelactie opgeven.       |
| **Verlagen**        | Als u dit bericht selecteert, moeten productieorders, inkooporders en andere ontvangsttransacties worden verminderd om te hoge voorraadniveaus te voorkomen.                                                                                                   |
| **Verhogen**        | Als u dit bericht selecteert, moeten productieorders, inkooporders en andere ontvangsttransacties worden verhoogd om tekorten in de voorraden te voorkomen.                                                                                                    |
| **Afgeleide acties** | Als u dit bericht selecteert, worden de actieberichten gemaakt voor afgeleide behoeften, bijvoorbeeld acties voor deelorders ter vervulling van de productie.                                                                                                   |




