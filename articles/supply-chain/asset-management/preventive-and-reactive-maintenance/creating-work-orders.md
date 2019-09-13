---
title: Werkorders maken
description: In dit onderwerp wordt uitgelegd hoe u werkorders maakt in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b23ed3251b2f6cf4f34b423ce2f85301d6ab31a1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875583"
---
# <a name="creating-work-orders"></a>Werkorders maken


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Wanneer u preventieve onderhoudstaken hebt gepland, is de volgende stap het maken van werkorders voor de taken. Dit kunt u doen in een van de onderhoudsschema's. De geplande taken in een onderhoudsschema kunnen verschillende verwijzingstypen hebben:

| Verwijzingstype | Beschrijving                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| Onderhoudsplannen     | Taken voor preventief onderhoud op basis van de typen onderhoudsplan Tijd of Teller.                       |
| Onderhoudsrondes    | Taken voor preventief onderhoud met verschillende activa waarvoor een vergelijkbaar type onderhoud is vereist.           |
| Onderhoudsverzoek   | Handmatig gemaakt verzoek om onderhoud of reparatie van een activum, dat kan worden omgezet in een werkorder. |


1. Klik op **Activabeheer** > **Algemeen** > **Hele onderhoudsschema** of **Openstaande onderhoudsschemaregels** of **Openstaande onderhoudsschemagroepen**.

2. Selecteer de geplande onderhoudstaken waarvoor u een werkorder wilt maken en klik op **Werkorder**. Het totaal aantal geraamde uren voor de geselecteerde regels wordt weergegeven in het veld **Prognose voor onderhoudsuren**.

3. Selecteer in de sectie **Parameters** hoeveel werkorders er gemaakt moeten. U kunt één werkorder per onderhoudsschemaregel maken of een aantal werkorders op basis van uw selecties in de sectie **Eén werkorder per**.

4. Selecteer een **Werkordertype** dat wordt gebruikt voor alle werkorders die u maakt.

5. Klik op **OK**. Er worden een of meer werkorders gemaakt.

![Figuur 1](media/18-preventive-maintenance.png)

