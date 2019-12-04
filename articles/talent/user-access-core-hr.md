---
title: Gebruiker heeft toegang tot Core HR, maar niet tot Onboard of Attract
description: In dit onderwerp wordt uitgelegd hoe u het probleem oplost waarbij een gebruiker toegang tot Microsoft Dynamics 365 Talent - Core HR krijgt, maar geen toegang heeft tot Attract of Onboard.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1a86936d756d8375761ce50c9d9bf33dc638dfad
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772914"
---
# <a name="user-can-access-core-hr-but-not-onboard-or-attract"></a>Gebruiker heeft toegang tot Core HR, maar niet tot Onboard of Attract

[!include [banner](includes/banner.md)]

**Omgevingsdetails**

- De implementatie van Microsoft Dynamics Lifecycle Services (LCS) is uitgevoerd door gebruiker A.
- Gebruiker A heeft gebruiker B als gebruiker toegevoegd aan Microsoft Dynamics 365 Talent: Core HR.

**Uitgifte**

Gebruiker B heeft toegang tot Core HR, maar kan de app Talent: Attract of Talent: Onboard niet openen. Wanneer de gebruiker naar **Apps ervaren** probeert te gaan, komt hij of zij in plaats daarvan terecht in een proefomgeving.

**Oplossing**

Aan gebruiker B moeten de rechten worden toegewezen die nodig zijn om de Microsoft Power Apps-omgeving weer te geven die gebruiker A heeft gemaakt tijdens het inrichtingsproces.

Zie voor meer informatie de sectie Toegang verlenen tot de omgeving in [Talent inrichten](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

**Langetermijnoplossing**

Microsoft overweegt automatisch de juiste rechten voor Onboard en Attract toe te wijzen wanneer een gebruiker wordt toegevoegd aan Core HR.
