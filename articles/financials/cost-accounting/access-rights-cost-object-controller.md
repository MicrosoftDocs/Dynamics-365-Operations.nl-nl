---
title: "Toegangsrechten definiëren voor controllers voor kostenobjecten"
description: Dit onderwerp bevat informatie over toegangsrechten voor controllers voor kostenobjecten.
author: AndersGirke
manager: AnnBe
ms.date: 06/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: yuyus
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: YuyuScheller
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 44ef687dcc5c7f515494894b3784bf5eceb99eed
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="access-rights-of-a-cost-object-controller"></a>Toegangsrechten voor een controller voor kostenobjecten

[!include[banner](../includes/banner.md)]

Het werkgebied **Kostenbeheer** is een centraal punt waar managers de prestaties van hun kostenobjecten kunnen bekijken. In dit werkgebied kunnen managers gebruikmaken van gegevens over Kostprijsboekhouding, zelfs als ze geen kostenaccountants zijn. Uit veiligheidsoverwegingen dienen managers alleen de gegevens over Kostprijsboekhouding te mogen zien die betrekking hebben op de specifieke kostenobjecten waarvoor ze verantwoordelijk zijn.

Er zijn vier unieke rollen in Kostprijsboekhouding.

| Rolnaam               | Licentie      |
|-------------------------|--------------|
| Manager van kostprijsboekhouding | Activiteit     |
| Kostenaccountant         | Operations   |
| Assistent kostenaccountant   | Operations   |
| Controller voor kostenobjecten  | Teamleden |

In dit onderwerp wordt uitgelegd hoe de rol **Controller voor kostenobjecten** aan een manager kan worden toegewezen.

Wanneer de **Controller voor kostenobjecten** wordt toegewezen aan een manager, kan de manager de volgende taken uitvoeren:

- Toegang verkrijgen tot het werkgebied **Kostenbeheer** (in de client).

    - Gedetailleerd bekijken van en weergaverechten verkrijgen voor de pagina's die ondersteuning bieden aan de detailanalyse-ervaring.

- Toegang verkrijgen tot het werkgebied **Kostenbeheer** (in de mobiele toepassing).

> [!NOTE]
> De rol **Controller voor kostenobjecten** bepaalt niet de kostenobjecten tot welke de gebruiker toegang kan krijgen en waarvoor gegevens kunnen worden weergegeven. Beveiliging op rijniveau wordt geleverd via dimensiehiërarchieën en de hiërarchie van toegangslijsten.

## <a name="grant-access-rights"></a>Toegangsrechten toekennen
In het volgende voorbeeld ziet u hoe een dimensiehiërarchie eruit kan zien.

**Gegevens van dimensiehiërarchie**

| Naam van dimensiehiërarchie | Dimensie    | Naam van type dimensiehiërarchie      | Hiërarchie van toegangslijsten |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organisatie             | Kostenplaatsen | Hiërarchie dimensieclassificatie | **Ja**               |

U kunt het sneltabblad **Gebruikers** in de hiërarchieontwerper gebruiken om een of meer gebruikers-id's op elk knooppunt in te voegen.

|                                   | Gebruikers            | Bereiken van dimensieleden   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| **Knooppunten**                         | **Gebruikers-id**      | **Van dimensielid** | **Tot dimensielid** |
| Organisatie                      | Benjamin, Claire |                           |                         |
| &nbsp;&nbsp;Beheer                 | april            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Financiën   | Alicia           | CC002                     | CC003                   |
|                                   |                  | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;HR        | Arnie            | CC001                     | CC001                   |
| &nbsp;&nbsp;Productie            | David            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Verpakking | Ellen            | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Assembleren  | Chris            | CC006                     | CC006                   |

> [!NOTE]
> Kostenaccountants moeten worden toegewezen op het hoogste niveau van de hiërarchie, zodat ze alle vermeldingen in Kostprijsboekhouding kunnen zien.

Voordat de hiërarchie van toegangslijsten en de beveiligingsinstellingen kunnen worden toegepast, moet de optie **Weergavetoegang voor dimensieleden voor kostenobject inschakelen** op **Ja** worden ingesteld op het tabblad **Algemeen** van de pagina **Parameters voor kostprijsboekhouding** (**Kostprijsboekhouding** > **Instellen** > **Parameters**).

De instellingen voor de hiërarchie van toegangslijsten worden gebruikt voor het bepalen van de gegevens die in de volgende gebieden worden weergegeven:

- Werkgebied **Kostenbeheer** (in de client):

    - Gegevens op de pagina's die worden gebruikt voor detailanalyse

- Werkgebied **Kostenbeheer** (in de mobiele toepassing):

    - Saldi in kaarten

- Microsoft Power BI:

    - Gegevens die worden weergegeven in Power BI-visualisaties
    - Gegevens van Power BI-visualisaties die worden ingesloten in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, client

> [!IMPORTANT]
> - Voordat de hiërarchie van toegangslijsten van invloed kan zijn op gegevens in Power BI, moeten de hiërarchie van toegangslijsten en beveiliging op rijniveau in Power BI worden gekoppeld. Zie [Beveiliging instellen voor het inhoudpakket Kostprijsboekhouding](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md) voor meer informatie.
> - Dit onderwerp bevat de vereisten waaraan moet worden voldaan voordat u het werkgebied **Kostenbeheer** kunt gebruiken.

Zie ook

- [Werkgebied voor kostenbeheer](cost-control-workspace.md)
- [Dimensiehiërarchie](dimension-hierarchy.md)
- [Beveiliging instellen voor het inhoudpakket Kostprijsboekhouding](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)
