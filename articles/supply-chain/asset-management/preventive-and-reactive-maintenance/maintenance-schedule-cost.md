---
title: Kosten onderhoudsschema
description: In dit onderwerp worden de kosten van onderhoudsplannen in Activabeheer uitgelegd.
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 267452bf5ec8cafebb5927045e8708a41603ec16f48626b7fd351d13fdb2fab7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746251"
---
# <a name="maintenance-schedule-cost"></a>Kosten onderhoudsschema

[!include [banner](../../includes/banner.md)]

 

In Activabeheer kunt u budgetkosten berekenen op regels voor onderhoudsplanning. Dit is handig als u een overzicht wilt weergeven van verwachte kosten, bijvoorbeeld kosten met betrekking tot geplande onderhoudstaken voor het volgende jaar. De berekeningen zijn gebaseerd op bestaande regels voor onderhoudsplanning van het type "Onderhoudsplannen" en "Onderhoudsrondes" en "Onderhoudsaanvragen".

1. Klik **Onderhoudsbeheer** > **Aanvragen** > **Activa** > **Kosten onderhoudsplanning**.

2. In het dialoogvenster **Kosten onderhoudsplanning** kunt u een **Financiële dimensieset** selecteren als u kosten gegroepeerd in financiële dimensies wilt weergeven.

>[!NOTE]
>U kunt financiële dimensie sets instellen in **Grootboek** > **Rekeningschema** > **Dimensies** > **Financiële dimensiesets**.

3. U kunt het veld **Niveau** gebruiken om aan te geven hoe gedetailleerd de regels voor onderhoudsplanning zijn met betrekking tot functionele locaties. Als u bijvoorbeeld het getal "1" invoegt in het veld en u een structuur met meerdere niveaus voor functionele locaties hebt, worden alle regels voor onderhoudsplanning voor een functionele locatie weergegeven op het hoogste niveau. Daarom kunnen de uren op een regel worden opgeteld op basis van functionele locaties die zich op een lager niveau bevinden. Als u het getal "0" in het veld **Niveau** invoegt, wordt er een gedetailleerd resultaat met alle regels voor onderhoudsplanning weergegeven op alle niveaus voor functionele locaties waarop deze betrekking hebben.

4. Als u een berekening wilt maken voor specifieke activa, klikt u op **Filteren** in het Sneltabblad **Records die moeten worden opgenomen** en selecteert u de relevante activa. Indien nodig kunt u ook een **Verwachte begindatum** voor de kostenberekening opgeven of een andere **Status** voor de kostenberekening selecteren.

5. Klik op **OK** om de kostenberekening te starten.

6. Klik op het tabblad **Kosten van onderhoudsplanning** > in de actievenstergroepen op **Groeperen op...**, klik op de relevante knoppen om het vereiste detailniveau van de kostenberekening weer te geven. De geselecteerde knoppen voor actievenstergroepen zijn gemarkeerd. U kunt knoppen activeren of deactiveren door erop te klikken.

7. Klik op de knop **kosten berekenen** als u een nieuwe kostenberekening wilt maken.

In de onderstaande afbeelding ziet u de resultaten van de kostenberekening van een onderhoudsschema.

![Figuur 1.](media/17-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]