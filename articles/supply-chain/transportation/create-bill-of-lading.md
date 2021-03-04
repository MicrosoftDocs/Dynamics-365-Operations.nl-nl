---
title: Een vrachtbrief maken
description: In dit onderwerp wordt uitgelegd hoe u een vrachtbrief maakt wanneer u gebruik maakt van de processen voor magazijnbeheer.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench, WHSBillOfLadingCarrier, WHSBillOfLadingOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd014f5804681936920b47e999709f153def11bc
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4425862"
---
# <a name="create-a-bill-of-lading"></a>Een vrachtbrief maken

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u een vrachtbrief maakt wanneer u gebruik maakt van de processen voor magazijnbeheer.  

Een vrachtbrief is een juridisch document tussen het bedrijf dat de artikelen verzendt en de vervoerder. Het document begeleidt de verzonden artikelen en dient als ontvangstbewijs wanneer artikelen op de plaats van bestemming worden afgeleverd. Als u magazijnbeheer gebruikt, zijn er twee manieren om een vrachtbrief te genereren:

  -   Het rapport handmatig aanmaken, op de pagina **Vrachtbrief**.
  -   Het rapport genereren in de **Workbench ladingplanning**.

Als u de vrachtbrief genereert in de **Workbench ladingplanning** moet de ladingsstatus **Verzonden** zijn. Als de lading meer dan één zending bevat, kunt u een vrachtbrief maken voor elke zending. Nadat een vrachtbrief is gemaakt, kunt u er wijzigingen in aanbrengen op de pagina **Vrachtbrief**.

## <a name="master-bill-of-lading"></a>Hoofdvrachtbrief
Als de lading meer dan een zending bevat, kunt u een hoofdvrachtbrief maken. Deze heeft dezelfde indeling en informatie als een vrachtbrief, maar bevat de samengevatte inhoud voor alle zendingen. Als op de pagina **Transportbeheerparameters** de optie **Een hoofdvrachtbrief maken wanneer een lading uit meer dan een zending bestaat** is ingesteld op **Ja**, wordt een hoofdvrachtbrief automatisch gegenereerd wanneer u een vrachtbrief maakt in de **Workbench ladingplanning** en er meerdere zendingen zijn. U kunt ook een lijst met de vrachtbrieven verkrijgen door te klikken op **Gerelateerde informatie** &gt; **Vrachtbrief**. Als u vrachtbrieven handmatig aanmaakt, kunt u een hoofdvrachtbrief maken op de pagina **Vrachtbrief**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]