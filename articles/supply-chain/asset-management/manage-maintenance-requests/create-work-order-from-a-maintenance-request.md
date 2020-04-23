---
title: Werkorders maken van onderhoudsverzoeken
description: In dit onderwerp wordt uitgelegd hoe u een werkorder van een onderhoudsverzoek maakt in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b6bd98796140ab7aa3e7813ff1526413504554c5
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205202"
---
# <a name="create-work-orders-from-maintenance-requests"></a>Werkorders maken van onderhoudsverzoeken

[!include [banner](../../includes/banner.md)]

 


Wanneer u onderhoudsverzoeken hebt gemaakt, kunt u deze eenvoudig omzetten in werkorders. In dit onderwerp wordt beschreven hoe u het snelst kunt werken met onderhoudsverzoeken, verschillende onderhoudsverzoeken tegelijk kunt bijwerken en vervolgens een werkorder kunt maken voor meerdere onderhoudsverzoeken tegelijk. Op de pagina **Actieve onderhoudsaanvragen** of **De onderhoudsverzoeken van mijn functionele locatie** kunt u ook met één onderhoudsverzoek tegelijk werken en één onderhoudsverzoek in een werkorder omzetten.

> [!NOTE]
> Elk onderhoudsverzoek kan aan slechts één werkorder worden gekoppeld. Meerdere onderhoudsverzoeken kunnen echter wel in één werkorder worden opgenomen, zelfs als de onderhoudsverzoeken verschillende activa hebben.

1. Selecteer **Activabeheer** \> **Algemeen** \> **Onderhoudsaanvragen** \> **Alle onderhoudsverzoeken**.
2. Voordat u een werkorder van onderhoudsverzoeken kunt maken, moet u minimaal één type onderhoudstaak selecteren voor de onderhoudsverzoeken, en ook een type onderhoudstaak variant en vakgebied, als deze informatie relevant is. In de rasterweergave kunt u eenvoudig informatie voor een onderhoudsverzoek bijwerken.
3. Wanneer u klaar bent om een werkorder te maken, selecteert u de onderhoudsverzoeken die u wilt opnemen.

    - Als u meerdere onderhoudsverzoeken selecteert om in een werkorder om te zetten, moeten zowel het veld **Activum** als het veld **Type onderhoudstaak** zijn ingesteld voordat u de werkorder maakt.
    - Als u één onderhoudsverzoek selecteert om in een werkorder om te zetten, moet alleen het veld **Activum** worden ingesteld voordat u de werkorder maakt. Wanneer u echter de werkorder maakt, kunt u een onderhoudstaaktype (en een gerelateerd onderhoudstaaktype variant en vakgebied, als deze informatie relevant is) in het dialoogvenster **Werkorder** selecteren.

4. Selecteer **Werkorder**.
5. Stel in het dialoogvenster **Werkorder maken** de velden in en selecteer **OK**.

    Op een berichtenbalk kan een bericht verschijnen dat een nieuwe werkorder is gemaakt.

    Wanneer u een werkorder maakt die is gebaseerd op een onderhoudsverzoek en als het activum dat aan het onderhoudsverzoek is gekoppeld, wordt opgenomen in een garantieovereenkomst, verschijnt er op een berichtenbalk een bericht over de garantieovereenkomst.

6. Selecteer **Activabeheer** \> **Algemeen** \> **Werkorders** \> **Alle werkorders** en open de nieuwe werkorder.

    ![Nieuwe werkorder openen](media/05-manage-maintenance-requests.png)

