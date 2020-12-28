---
title: Gebruiker heeft toegang tot Human Resources, maar niet tot de app Onboard of Attract
description: In dit onderwerp wordt uitgelegd hoe u het probleem oplost waarbij een gebruiker toegang tot Microsoft Dynamics 365 Talent - Human Resources krijgt, maar geen toegang heeft tot Attract of Onboard.
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
ms.openlocfilehash: 6c384d9a7100982eabd201d910e1bea14355dc1f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460788"
---
# <a name="user-can-access-human-resources-but-not-onboard-or-attract"></a>Gebruiker heeft toegang tot Human Resources, maar niet tot de app Onboard of Attract

[!include [banner](includes/banner.md)]

**Omgevingsdetails**

- De implementatie van Microsoft Dynamics Lifecycle Services (LCS) is uitgevoerd door gebruiker A.
- Gebruiker A heeft gebruiker B als gebruiker toegevoegd aan Microsoft Dynamics 365 Human Resources.

**Uitgifte**

Gebruiker B heeft toegang tot Human Resources, maar kan de app Talent: Attract of Talent: Onboard niet openen. Wanneer de gebruiker naar **Apps ervaren** probeert te gaan, komt hij of zij in plaats daarvan terecht in een proefomgeving.

**Oplossing**

Aan gebruiker B moeten de rechten worden toegewezen die nodig zijn om de Microsoft Power Apps-omgeving weer te geven die gebruiker A heeft gemaakt tijdens het inrichtingsproces.

Zie voor meer informatie de sectie Toegang verlenen tot de omgeving in [Talent inrichten](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

**Langetermijnoplossing**

Microsoft overweegt automatisch de juiste rechten voor Onboard en Attract toe te wijzen wanneer een gebruiker wordt toegevoegd aan Human Resources.
