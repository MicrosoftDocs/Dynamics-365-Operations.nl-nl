---
title: Rapportageopties in Talent
description: In dit onderwerp wordt uitgelegd hoe u het probleem oplost waarbij een klant Dynamics 365 Talent-rapporten wil aanpassen of nieuwe rapporten wil maken.
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
ms.openlocfilehash: 05d4a2c4314b40042ae45b4f653554bad09be4fa
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897943"
---
# <a name="reporting-options-in-talent"></a>Rapportageopties in Talent

**Omgevingsdetails**

Dit probleem geldt voor alle omgevingen.

**Symptoom**

De klant wil Dynamics 365 Talent-rapporten aanpassen of nieuwe rapporten maken.

**Probleem**

De gebruiker kan de ingesloten Microsoft Power BI-rapporten niet aanpassen.

**Oplossing**

- De Core HR-gegevens die naar Common Data Service stromen, kunnen via de Power Apps Common Data Service-connector aan Power BI Desktop worden gerapporteerd. Common Data Service bevat een subset van Core HR-gegevens. Raadpleeg voor meer informatie over Power BI en dashboards [Power BI-rapporten en dashboards maken met Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).
- Elektronische rapportage (ER) is beschikbaar voor sommige rapporten in Talent. Door de klant gestuurde aanpassingen kunnen worden uitgevoerd via de ER-configuratieopties.
- Gegevens kunnen worden geëxporteerd naar Microsoft Excel of Microsoft Word met behulp van de verschillende gegevensentiteiten die Talent biedt dankzij de integratie met Microsoft Office.

**Langetermijnoplossing**

Er worden meer Power BI-opties beschikbaar en meer gegevens en entiteiten worden opgenomen in Common Data Service.
