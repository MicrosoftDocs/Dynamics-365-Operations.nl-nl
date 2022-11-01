---
title: Toegang tot privéadressen per beveiligingsrol
description: In dit artikel wordt uitgelegd hoe u het probleem oplost waarbij een klant geen toegang tot privéadressen krijgt.
author: twheeloc
ms.date: 09/13/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7c1db052937b03817f22b37c50b9f1b319579cb2
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/20/2022
ms.locfileid: "9702098"
---
# <a name="access-to-private-addresses-by-security-role"></a>Toegang tot privéadressen per beveiligingsrol


[!INCLUDE [PEAP](../includes/peap-2.md)]

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
