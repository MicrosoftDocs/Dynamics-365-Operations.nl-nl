---
title: Rapportageopties
description: In dit artikel wordt uitgelegd hoe u het probleem oplost dat ontstaat als een klant Microsoft Dynamics 365 Human Resources-rapporten wil aanpassen of nieuwe rapporten wil maken.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2d0fc6b2d4af6ad021943717645bfff7a27797a8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803892"
---
# <a name="reporting-options"></a>Rapportageopties

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**Omgevingsdetails**

Dit probleem geldt voor alle omgevingen.

**Symptoom**

De klant wil Dynamics 365 Human Resources-rapporten aanpassen of nieuwe rapporten maken.

**Uitgeven**

De gebruiker kan de ingesloten Microsoft Power BI-rapporten niet aanpassen.

**Oplossing**

- De Human Resources-gegevens die naar Dataverse stromen, kunnen worden gebruikt in rapporten via de Power Apps Dataverse-connector naar Power BI Desktop. Houd er rekening mee dat Dataverse een subset van Human Resources-gegevens bevat. Raadpleeg voor meer informatie over Power BI en dashboards [Power BI-rapporten en dashboards maken met Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).
- Elektronische rapportage (ER) is beschikbaar voor sommige rapporten in Human Resources. Door de klant gestuurde aanpassingen kunnen worden uitgevoerd via de ER-configuratieopties.
- Gegevens kunnen worden geëxporteerd naar Microsoft Excel of Microsoft Word met behulp van de verschillende gegevensentiteiten die Human Resources biedt dankzij de integratie met Microsoft Office.

**Langetermijnoplossing**

Er worden meer Power BI-opties beschikbaar en meer gegevens en entiteiten worden opgenomen in Dataverse.


[!INCLUDE[footer-include](../includes/footer-banner.md)]