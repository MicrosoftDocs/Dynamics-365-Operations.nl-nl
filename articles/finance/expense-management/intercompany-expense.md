---
title: Intercompany-onkosten
description: Een werknemer die werkzaam is bij één rechtspersoon in een organisatie, voert mogelijk werk uit voor een andere rechtspersoon in dezelfde organisatie. In deze situatie kunt u de functie IC-kosten gebruiken om de onkosten van voor de werknemer toe te wijzen aan de rechtspersoon voor wie het werk is uitgevoerd.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 07e425707eb20730f10246a27799f4deeef93f97
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/21/2020
ms.locfileid: "3390879"
---
# <a name="intercompany-expenses"></a>Intercompany-onkosten

[!include [banner](../includes/banner.md)]

Een werknemer die werkzaam is bij één rechtspersoon in een organisatie, voert mogelijk werk uit voor een andere rechtspersoon in dezelfde organisatie. In deze situatie kunt u de functie IC-kosten gebruiken om de onkosten van voor de werknemer toe te wijzen aan de rechtspersoon voor wie het werk is uitgevoerd. De rechtspersoon waarbij de werknemer in dienst is, wordt de uitlenende rechtspersoon genoemd. De juridische entiteit waarvan de werknemer onkosten maakt, heet de ontlenende rechtspersoon. 

Voordat een werknemer onkosten kan maken en indienen voor werk dat is uitgevoerd voor een andere rechtspersoon, selecteert u voor de uitlenende rechtspersoon op de pagina **Parameters onkostenbeheer** de optie **Intercompany-onkostenregels toestaan**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Boeking van btw voor intercompany-onkosten

[!include [banner](../includes/banner.md)]

Als u btw-groepen wilt gebruiken die zijn gekoppeld aan de uitlenende rechtspersoon (bron) in plaats van de lenende rechtspersoon (bestemming) in uw onkostendeclaratie, moet u deze configureren in de btw-instellingen voor het grootboek. Wanneer de grootboekparameter **Rechtspersoon voor intercompany-btw-boekingen** is ingesteld op **Bron** en **Belastingregels btw toepassen** is ingesteld op **Nee**, wordt de btw-combinatie voor de uitlenende rechtspersoon gebruikt. Wanneer dezelfde parameter wordt ingesteld op **Bestemming**, wordt de btw-combinatie voor de lenende rechtspersoon gebruikt. Voor rechtspersonen in de Verenigde Staten geldt dat als de parameter is ingesteld op **Bron**, het veld **Te ontvangen btw** ook worden geconfigureerd op de nieuwe pagina **Grootboekboekingsgroepen**. De boekhoudingsengine gebruikt de informatie uit dit veld voor belastinggerelateerde journaalregels.   
Het gedrag is consistent voor onkostenregels die zijn geboekt met of zonder een project.  
