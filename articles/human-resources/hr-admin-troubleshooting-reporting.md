---
title: Rapportageopties
description: In dit artikel wordt uitgelegd hoe u het probleem oplost dat ontstaat als een klant Microsoft Dynamics 365 Human Resources-rapporten wil aanpassen of nieuwe rapporten wil maken.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
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
ms.openlocfilehash: 9ee6dba5e37877f1c0b3b9df8306b3194ea2f3e4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008691"
---
# <a name="reporting-options"></a>Rapportageopties

**Omgevingsdetails**

Dit probleem geldt voor alle omgevingen.

**Symptoom**

De klant wil Dynamics 365 Human Resources-rapporten aanpassen of nieuwe rapporten maken.

**Probleem**

De gebruiker kan de ingesloten Microsoft Power BI-rapporten niet aanpassen.

**Oplossing**

- De Human Resources-gegevens die naar Common Data Service stromen, kunnen worden gebruikt in rapporten via de Power Apps Common Data Service-connector naar Power BI Desktop. Houd er rekening mee dat Common Data Service een subset van Human Resources-gegevens bevat. Raadpleeg voor meer informatie over Power BI en dashboards [Power BI-rapporten en dashboards maken met Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).
- Elektronische rapportage (ER) is beschikbaar voor sommige rapporten in Human Resources. Door de klant gestuurde aanpassingen kunnen worden uitgevoerd via de ER-configuratieopties.
- Gegevens kunnen worden geëxporteerd naar Microsoft Excel of Microsoft Word met behulp van de verschillende gegevensentiteiten die Human Resources biedt dankzij de integratie met Microsoft Office.

**Langetermijnoplossing**

Er worden meer Power BI-opties beschikbaar en meer gegevens en entiteiten worden opgenomen in Common Data Service.
