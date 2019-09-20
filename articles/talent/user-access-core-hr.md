---
title: Gebruiker heeft toegang tot Core HR, maar niet tot de app Onboard of Attract
description: In dit onderwerp wordt uitgelegd hoe u het probleem oplost waarbij een gebruiker toegang tot Microsoft Dynamics 365 for Talent Core HR krijgt, maar geen toegang heeft tot de app Attract of Onboard.
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
ms.openlocfilehash: 6fc27a4c137fef2f8d204d90366c316389da08e6
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741707"
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

Zie voor meer informatie de sectie Toegang verlenen tot de omgeving in [Talent inrichten](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

**Langetermijnoplossing**

Microsoft overweegt automatisch de juiste rechten voor Onboard en Attract toe te wijzen wanneer een gebruiker wordt toegevoegd aan Core HR.
