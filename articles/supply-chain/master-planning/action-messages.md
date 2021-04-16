---
title: Actieberichten
description: Een actiebericht is een door het systeem gegenereerde suggestie om een bestaande geplande of gefiatteerde order te wijzigen.
author: ChristianRytt
ms.date: 10/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, MCRSalesOrderMessages, MCRSalesTableDetailedStatus, TAMItemVendRebateGroup, TAMVendRebate, TAMVendRebateAgreementLineInfoPart, TAMVendRebateGroup, TAMVendRebateTable, TAMVendRebateTrans, ReqTransActionListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19411
ms.assetid: 52b46d93-7d02-46b5-aad1-9fd08206bf9d
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ea565a8935151235e4c3b103dd86b7131711a4a2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816575"
---
# <a name="action-messages"></a>Actieberichten

[!include [banner](../includes/banner.md)]

Een actiebericht is een door het systeem gegenereerde suggestie om een bestaande geplande of gefiatteerde order te wijzigen.

## <a name="introduction"></a>Introductie

Actieberichten worden gegenereerd door de hoofdplanningberekening als reactie op vereisten die zijn gewijzigd. De verzenddatum of de hoeveelheid kan bijvoorbeeld zijn gewijzigd in een verkooporder waarvoor u al een inkooporder hebt gemaakt om aan de vraag te voldoen. In dit geval worden een of meerdere actieberichten gegenereerd door de hoofdplanningberekening om de inkooporder bij te werken. U beslist of u de aanbevolen wijzigingen aanbrengt.

U kunt configureren hoe actieberichten worden berekend voor een behoefteplanningsgroep die u aan een artikel koppelt.

## <a name="select-action-messages"></a>Actieberichten selecteren

Op de pagina **Behoefteplanningsgroepen** kunt u de actieberichten selecteren die het systeem moet genereren, en de behoefteplanningsgroepen of items waar de berichten van toepassing op zijn. U kunt de volgende actieberichten selecteren.

| Bericht             | Beschrijving                                                                                                                                                                                                                                              |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Vervroegen**         | Als u dit bericht selecteert, genereert het systeem wanneer nodig actieberichten om orders naar een eerdere datum te verplaatsen. In het veld **Marge voor vervroegen** kunt u ook het maximumaantal dagen tussen ontvangst en uitgifte zonder vervroegde actie opgeven. |
| **Uitstellen**        | Als u dit bericht selecteert, genereert het systeem wanneer nodig actieberichten om orders naar een latere datum te verplaatsen. In het veld **Marge voor uitstellen** kunt u het maximumaantal dagen tussen ontvangst en uitgifte zonder uitstelactie opgeven.       |
| **Verlagen**        | Als u dit bericht selecteert, moeten productieorders, inkooporders en andere ontvangsttransacties worden verminderd om te hoge voorraadniveaus te voorkomen.                                                                                                   |
| **Verhogen**        | Als u dit bericht selecteert, moeten productieorders, inkooporders en andere ontvangsttransacties worden verhoogd om tekorten in de voorraden te voorkomen.                                                                                                    |
| **Afgeleide acties** | Als u dit bericht selecteert, worden de actieberichten gemaakt voor afgeleide behoeften, bijvoorbeeld acties voor deelorders ter vervulling van de productie.                                                                                                   |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]