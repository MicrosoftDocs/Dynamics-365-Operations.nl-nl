---
title: Werkorders maken
description: In dit onderwerp wordt uitgelegd hoe u werkorders maakt in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f94f8bc20753e38ce1cb6eccdfbc85c2e491ffad
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206122"
---
# <a name="creating-work-orders"></a>Werkorders maken

[!include [banner](../../includes/banner.md)]

 

Wanneer u preventieve onderhoudstaken hebt gepland, is de volgende stap het maken van werkorders voor de taken. Dit kunt u doen in een van de onderhoudsschema's. De geplande taken in een onderhoudsschema kunnen verschillende verwijzingstypen hebben:

| Verwijzingstype | Beschrijving                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| Onderhoudsplannen     | Taken voor preventief onderhoud op basis van de typen onderhoudsplan Tijd of Teller.                       |
| Onderhoudsrondes    | Taken voor preventief onderhoud met verschillende activa waarvoor een vergelijkbaar type onderhoud is vereist.           |
| Onderhoudsverzoek   | Handmatig gemaakt verzoek om onderhoud of reparatie van een activum, dat kan worden omgezet in een werkorder. |


1. Klik op **Activabeheer** > **Algemeen** > **Hele onderhoudsschema** of **Openstaande onderhoudsschemaregels** of **Openstaande onderhoudsschemagroepen**.

2. Selecteer de geplande onderhoudstaken waarvoor u een werkorder wilt maken en klik op **Werkorder**. In het dialoogvenster **Werkorders maken** wordt het totaal aantal geraamde uren voor de geselecteerde regels weergegeven in het veld **Prognose voor onderhoudsuren**.

3. Selecteer in de sectie **Parameters** hoeveel werkorders er gemaakt moeten. U kunt één werkorder per onderhoudsschemaregel maken of een aantal werkorders op basis van uw selecties in de sectie **Eén werkorder per**.

4. Selecteer een **Werkordertype** dat wordt gebruikt voor alle werkorders die u maakt. In de onderstaande afbeelding ziet u een voorbeeld van het dialoogvenster **Werkorders maken**.

![Figuur 1](media/18-preventive-maintenance.png)

5. Klik op **OK**. Er worden een of meer werkorders gemaakt.

