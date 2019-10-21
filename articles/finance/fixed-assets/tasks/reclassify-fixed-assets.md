---
title: Vaste activa opnieuw classificeren
description: Als u een activum opnieuw wilt classificeren, moet u dit overbrengen naar een nieuwe vaste-activagroep of er een nieuw vaste-activanummer aan toewijzen binnen dezelfde groep.
author: saraschi2
manager: AnnBe
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 47d8cf2ff1e275df0466a7fe327a3180c0399e49
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186918"
---
# <a name="reclassify-fixed-assets"></a>Vaste activa opnieuw classificeren

[!include [task guide banner](../../includes/task-guide-banner.md)]

Als u een activum opnieuw wilt classificeren, moet u dit overbrengen naar een nieuwe vaste-activagroep of er een nieuw vaste-activanummer aan toewijzen binnen dezelfde groep. 

Wanneer een vast activum opnieuw wordt ingedeeld:

• Alle boeken voor het bestaande vaste activum worden gemaakt voor het nieuwe vaste activum. Informatie die was ingesteld voor het oorspronkelijke vaste activum is naar het nieuwe vaste activum gekopieerd. De status van de boeken voor het oorspronkelijke vaste activum is Gesloten. 

• De nieuwe boeken van het nieuwe vaste activum bevatten de datum van het opnieuw classificeren in het veld **Verwervingsdatum**. De datum in het veld **Uitvoeringsdatum afschrijving** is gekopieerd uit de oorspronkelijke activumgegevens. Als de afschrijving al is begonnen, geeft het veld **Datum waarop de afschrijving** het laatst is uitgevoerd de datum van het opnieuw classificeren weer. 

• De bestaande vaste-activatransacties voor het oorspronkelijke vaste activum zijn geannuleerd en opnieuw gegenereerd voor het nieuwe vaste activum.

Voer de volgende stappen uit om een vast activum opnieuw te classificeren:

1. Ga naar **Vaste activa > Periodieke taken > Herclassificatie**.
2. Selecteer in het veld **Vaste-activagroep** de groep die u opnieuw wilt classificeren.
3. Selecteer in het veld **Vaste-activanummer** het activanummer van het activum dat u opnieuw wilt classificeren.
4. Selecteer in het veld **Nieuwe groep vaste activa** een groep waarnaar u het vaste activum wilt overboeken.
    * Als de nieuwe vaste-activagroep aan een nummerreeks is gekoppeld, wordt het veld **Nieuw nummer voor vaste activa** bijgewerkt met het nummer uit de nummerreeks voor de nieuwe vaste-activagroep. Anders wordt het veld **Nieuw nummer voor vaste activa** bijgewerkt met het nummer uit de nummerreeks die is geconfigureerd op de pagina **Vaste-activaparameters**. Als op de pagina **Vaste-activaparameters** geen nummerrreeks is geconfigureerd, typ dan een nummer in het veld **Nieuw nummer voor vaste activa**.  
5. Typ een datum in het veld **Datum herclassificatie**.
6. Typ of selecteer een waarde in het veld **Boekstuknummering**.
7. Klik op **OK**.
