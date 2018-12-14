---
title: Gebruiker heeft toegang tot Core HR, maar niet tot de app Onboard of Attract
description: In dit onderwerp wordt uitgelegd hoe u het probleem oplost waarbij een gebruiker toegang tot Microsoft Dynamics 365 for Talent Core HR krijgt, maar geen toegang heeft tot de app Attract of Onboard.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 2e5d0b1bf993aec89c7d2c6d4916732f5824310d
ms.contentlocale: nl-nl
ms.lasthandoff: 12/04/2018

---

# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a>Gebruiker heeft toegang tot Core HR, maar niet tot de app Onboard of Attract

[!include [banner](includes/banner.md)]

**Omgevingsdetails**

- De implementatie van Microsoft Dynamics Lifecycle Services (LCS) is uitgevoerd door gebruiker A.
- Gebruiker A heeft gebruiker B als gebruiker toegevoegd aan Microsoft Dynamics 365 for Talent Core HR.

**Probleem**

Gebruiker B heeft toegang tot Core HR, maar kan de app Talent: Attract of Talent: Onboard niet openen. Wanneer de gebruiker naar **Apps ervaren** probeert te gaan, komt hij of zij in plaats daarvan terecht in een proefomgeving.

**Oplossing**

Aan gebruiker B moeten de rechten worden toegewezen die nodig zijn om de Microsoft PowerApps-omgeving weer te geven die gebruiker A heeft gemaakt tijdens het inrichtingsproces.

Zie voor meer informatie de sectie Toegang verlenen tot de omgeving in [Talent inrichten](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).

**Langetermijnoplossing**

Microsoft overweegt automatisch de juiste rechten voor Onboard en Attract toe te wijzen wanneer een gebruiker wordt toegevoegd aan Core HR.

