---
title: Configuratieregels
description: "Dit artikel geeft algemene informatie over configuratieregels. Configuratieregels definiëren relaties tussen artikelen in een stuklijst (BOM) voor producten die op dimensies gebaseerde configuratietechnologie gebruiken."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: 271a780eec291455b433c0767246d79cb965ce02
ms.lasthandoff: 03/31/2017


---

# <a name="configuration-rules"></a>Configuratieregels

[!include[banner](../includes/banner.md)]


Dit artikel geeft algemene informatie over configuratieregels. Configuratieregels definiëren relaties tussen artikelen in een stuklijst (BOM) voor producten die op dimensies gebaseerde configuratietechnologie gebruiken.

Configuratieregels zijn beschikbaar wanneer u op dimensies gebaseerde configuratiemodellen definieert. Configuratieregels worden gebruikt om specifieke artikelcombinaties in een stuklijst af te dwingen of te verbieden. Nadat een stuklijst is gemaakt en de relevante artikelen aan hun respectievelijke configuratiegroepen zijn toegewezen, kunnen een of meer configuratieregels worden gedefinieerd. Als twee artikelen bij elkaar horen, wordt de operator **Selecteren** gebruikt om opname te garanderen. Als twee artikelen elkaar wederzijds uitsluiten, wordt de operator **Selectie opheffen** gebruikt om uitsluiting te garanderen.  

**Opmerking:** Deze informatie is alleen van toepassing op productmodellen die gebruikmaken van de technologie van op dimensies gebaseerde configuratie.  

Het wijzigen van configuratieregels heeft geen invloed op bestaande configuraties. Het is echter wel belangrijk de regels in te stellen voordat u een nieuwe configuratie gaat definiëren en om die regels te controleren als u er niet zeker van bent of deze wel of niet zijn gewijzigd.  

**Opmerking:** Bij de methode **Selecteren** worden de afgeleide configuratiegroep, het artikelnummer en de configuratie automatisch geselecteerd. Bij de methode **Selectie opheffen** kunnen de afgeleide configuratiegroep, het artikelnummer en de configuratie niet worden geselecteerd.

<a name="see-also"></a>Zie ook
--------

[Op dimensie gebaseerde productconfiguratie](dimension-based-product-configuration.md)




