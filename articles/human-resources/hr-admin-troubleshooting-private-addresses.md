---
title: Toegang tot privéadressen per beveiligingsrol
description: In dit onderwerp wordt uitgelegd hoe u het probleem oplost waarbij een klant geen toegang tot privéadressen krijgt.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0b96733946e4ef79de244730d0c442b9900426c1
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413334"
---
# <a name="access-to-private-addresses-by-security-role"></a>Toegang tot privéadressen per beveiligingsrol

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Probleem**

Als een klant een beveiligingsrol dupliceert en zich aanmeldt als die nieuwe rol, zijn de als privé gemarkeerde adressen niet zichtbaar voor de klant.

**Resolutie**

Om het probleem op te lossen, moet de klant deze stappen uitvoeren voor de gedupliceerde beveiligingsrol.

1. Ga naar **Organisatiebeheer \> Globaal adresboek \> Parameters van globaal adresboek**.
2. Verplaats de nieuwe beveiligingsrol op het tabblad **Beveiliging privé-locatie** van de lijst **Beschikbare rollen** naar de lijst **Geselecteerde rollen**.
3. Selecteer **Opslaan**.

![De pagina Parameters van globaal adresboek.](media/GAD-parameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
