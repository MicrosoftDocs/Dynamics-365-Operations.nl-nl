---
title: Toegang tot privéadressen per beveiligingsrol
description: In dit artikel wordt uitgelegd hoe u het probleem oplost waarbij een klant geen toegang tot privéadressen krijgt.
author: andreabichsel
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 21919e0bf75a5a47fc64b87410ccd75ff34259fb1c8c2bc1aa82318dcd0572b9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719111"
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