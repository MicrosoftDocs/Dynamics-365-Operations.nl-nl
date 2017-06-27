---
title: Een vrachtbrief maken
description: In dit onderwerp wordt uitgelegd hoe u een vrachtbrief maakt wanneer u gebruik maakt van de processen voor magazijnbeheer.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: f3010daa41f54cf026d46b1b7648a277651173da
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="create-a-bill-of-lading"></a>Een vrachtbrief maken

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt uitgelegd hoe u een vrachtbrief maakt wanneer u gebruik maakt van de processen voor magazijnbeheer.  

Een vrachtbrief is een juridisch document tussen het bedrijf dat de artikelen verzendt en de vervoerder. Het document begeleidt de verzonden artikelen en dient als ontvangstbewijs wanneer artikelen op de plaats van bestemming worden afgeleverd. Als u magazijnbeheer gebruikt, zijn er twee manieren om een vrachtbrief te genereren:

  -   Het rapport handmatig aanmaken, op de pagina **Vrachtbrief**.
  -   Het rapport genereren in de **Workbench ladingplanning**.

Als u de vrachtbrief genereert in de **Workbench ladingplanning** moet de ladingsstatus **Verzonden** zijn. Als de lading meer dan één zending bevat, kunt u een vrachtbrief maken voor elke zending. Nadat een vrachtbrief is gemaakt, kunt u er wijzigingen in aanbrengen op de pagina **Vrachtbrief**.

## <a name="master-bill-of-lading"></a>Hoofdvrachtbrief
Als de lading meer dan een zending bevat, kunt u een hoofdvrachtbrief maken. Deze heeft dezelfde indeling en informatie als een vrachtbrief, maar bevat de samengevatte inhoud voor alle zendingen. Als op de pagina **Transportbeheerparameters** de optie **Een hoofdvrachtbrief maken wanneer een lading uit meer dan een zending bestaat** is ingesteld op **Ja**, wordt een hoofdvrachtbrief automatisch gegenereerd wanneer u een vrachtbrief maakt in de **Workbench ladingplanning** en er meerdere zendingen zijn. U kunt ook een lijst met de vrachtbrieven verkrijgen door te klikken op **Gerelateerde informatie** &gt; **Vrachtbrief**. Als u vrachtbrieven handmatig aanmaakt, kunt u een hoofdvrachtbrief maken op de pagina **Vrachtbrief**.




