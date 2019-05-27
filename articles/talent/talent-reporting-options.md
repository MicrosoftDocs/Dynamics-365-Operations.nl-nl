---
title: Rapportageopties in Talent
description: In dit onderwerp wordt uitgelegd hoe u het probleem oplost waarbij een klant Dynamics 365 for Talent-rapporten wil aanpassen of nieuwe rapporten wil maken.
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
ms.openlocfilehash: 7e00a6e4fc01f72e1ef2347e08754997135215ed
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517728"
---
# <a name="reporting-options-in-talent"></a>Rapportageopties in Talent

[!include [banner](includes/banner.md)]

**Omgevingsdetails**

Dit probleem geldt voor alle omgevingen.

**Symptoom**

De klant wil Dynamics 365 for Talent-rapporten aanpassen of nieuwe rapporten maken.

**Probleem**

De gebruiker kan de ingesloten Microsoft Power BI-rapporten niet aanpassen.

**Oplossing**

- De Core HR-gegevens die naar Common Data Service stromen, kunnen via de PowerApps Common Data Service-connector aan Power BI Desktop worden gerapporteerd. Common Data Service bevat een subset van Core HR-gegevens. Raadpleeg voor meer informatie over Power BI en dashboards [Power BI-rapporten en -dashboards maken met PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).
- Elektronische rapportage (ER) is beschikbaar voor sommige rapporten in Talent. Door de klant gestuurde aanpassingen kunnen worden uitgevoerd via de ER-configuratieopties.
- Gegevens kunnen worden geëxporteerd naar Microsoft Excel of Microsoft Word met behulp van de verschillende gegevensentiteiten die Talent biedt dankzij de integratie met Microsoft Office.

**Langetermijnoplossing**

Er worden meer Power BI-opties beschikbaar en meer gegevens en entiteiten worden opgenomen in Common Data Service.
