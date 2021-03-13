---
title: Configuratieregels
description: Dit artikel geeft algemene informatie over configuratieregels. Configuratieregels definiëren relaties tussen artikelen in een stuklijst (BOM) voor producten die op dimensies gebaseerde configuratietechnologie gebruiken.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b8b3de89235c6dac52f059af9665ea70f80d83a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007786"
---
# <a name="configuration-rules"></a>Configuratieregels

[!include [banner](../includes/banner.md)]

Dit artikel geeft algemene informatie over configuratieregels. Configuratieregels definiëren relaties tussen artikelen in een stuklijst (BOM) voor producten die op dimensies gebaseerde configuratietechnologie gebruiken.

Configuratieregels zijn beschikbaar wanneer u op dimensies gebaseerde configuratiemodellen definieert. Configuratieregels worden gebruikt om specifieke artikelcombinaties in een stuklijst af te dwingen of te verbieden. Nadat een stuklijst is gemaakt en de relevante artikelen aan hun respectievelijke configuratiegroepen zijn toegewezen, kunnen een of meer configuratieregels worden gedefinieerd. Als twee artikelen bij elkaar horen, wordt de operator **Selecteren** gebruikt om opname te garanderen. Als twee artikelen elkaar wederzijds uitsluiten, wordt de operator **Selectie opheffen** gebruikt om uitsluiting te garanderen.  

**Opmerking:** Deze informatie is alleen van toepassing op productmodellen die gebruikmaken van de technologie van op dimensies gebaseerde configuratie.  

Het wijzigen van configuratieregels heeft geen invloed op bestaande configuraties. Het is echter wel belangrijk de regels in te stellen voordat u een nieuwe configuratie gaat definiëren en om die regels te controleren als u er niet zeker van bent of deze wel of niet zijn gewijzigd.  

**Opmerking:** Bij de methode **Selecteren** worden de afgeleide configuratiegroep, het artikelnummer en de configuratie automatisch geselecteerd. Bij de methode **Selectie opheffen** kunnen de afgeleide configuratiegroep, het artikelnummer en de configuratie niet worden geselecteerd.

<a name="additional-resources"></a>Aanvullende resources
--------

[Overzicht van Op dimensies gebaseerde productconfiguraties](dimension-based-product-configuration.md)



