---
title: Vaste activa opnieuw classificeren
description: In dit artikel wordt het proces van het opnieuw classificeren van activa uitgelegd. Als u een activum opnieuw wilt classificeren, moet u dit overbrengen naar een nieuwe vaste-activagroep of er een nieuw vaste-activanummer aan toewijzen binnen dezelfde groep.
author: moaamer
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4bd901b1709f0b006cecfbbf6d8c170b56f89d19
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284358"
---
# <a name="reclassify-fixed-assets"></a>Vaste activa opnieuw classificeren

[!include [banner](../../includes/banner.md)]

Als u een activum opnieuw wilt classificeren, moet u dit overbrengen naar een nieuwe vaste-activagroep of er een nieuw vaste-activanummer aan toewijzen binnen dezelfde groep. 

Wanneer een vast activum opnieuw wordt ingedeeld:

- Alle boeken voor het bestaande vaste activum worden gemaakt voor het nieuwe vaste activum. Informatie die was ingesteld voor het oorspronkelijke vaste activum is naar het nieuwe vaste activum gekopieerd. De status van de boeken voor het oorspronkelijke vaste activum is Gesloten. 

- De nieuwe boeken voor het nieuwe vaste activum bevatten de datum van het opnieuw classificeren in het veld **Verwervingsdatum**. De datum in het veld **Uitvoeringsdatum afschrijving** is gekopieerd uit de oorspronkelijke activumgegevens. Als de afschrijving al is begonnen, geeft het veld **Datum waarop de afschrijving** het laatst is uitgevoerd de datum van het opnieuw classificeren weer. 

- De bestaande vaste-activatransacties voor het oorspronkelijke vaste activum zijn geannuleerd en opnieuw gegenereerd voor het nieuwe vaste activum.

- Wanneer een activum met een overboekingstransactie opnieuw is geclassificeerd, toont het systeem een bericht in het **Actiecentrum** om aan te geven dat een overboekingstransactie niet werd voltooid tijdens het herclassificatieproces. Een overboekingstransactie moet worden voltooid om de bestaande herclassificatietransacties naar de juiste financiële dimensies te verplaatsen. 

   Tijdens het herclassificatieproces worden de volgende acties uitgevoerd om het activumsaldo van het oorspronkelijke activum naar het nieuwe activum opnieuw te classificeren. 
   
   - Het herclassificatieproces kopieert de gegevens van het oorspronkelijke vaste-activaboek naar het nieuwe vaste-activaboek.

   - De herclassificatietransactie gebruikt gegevens van de oorspronkelijke geboekte verwerving die informatie over financiële dimensies bevat die in de verwervingstransactie zijn opgenomen.  
   
   - Tegelijkertijd draait het herclassificatieproces de verwerving van de oorspronkelijke activum en de activumoverboekingstransactie terug. 

Het volgende diagram en procedure geven een voorbeeld van het herclassificatieproces. 

[![Diagram met het herclassificatieproces.](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)

Voer de volgende stappen uit om een vast activum opnieuw te classificeren:

1. Ga naar **Vaste activa > Periodieke taken > Herclassificatie**.
2. Selecteer in het veld **Vaste-activagroep** de groep die u opnieuw wilt classificeren.
3. Selecteer in het veld **Vaste-activanummer** het activanummer van het activum dat u opnieuw wilt classificeren.
4. Selecteer in het veld **Nieuwe groep vaste activa** een groep waarnaar u het vaste activum wilt overboeken.
    * Als de nieuwe vaste-activagroep aan een nummerreeks is gekoppeld, wordt het veld **Nieuw nummer voor vaste activa** bijgewerkt met het nummer uit de nummerreeks voor de nieuwe vaste-activagroep. Anders wordt het veld **Nieuw nummer voor vaste activa** bijgewerkt met het nummer uit de nummerreeks die is geconfigureerd op de pagina **Vaste-activaparameters**. Als op de pagina **Vaste-activaparameters** geen nummerrreeks is geconfigureerd, typ dan een nummer in het veld **Nieuw nummer voor vaste activa**.  
5. Typ een datum in het veld **Datum herclassificatie**.
6. Typ of selecteer een waarde in het veld **Boekstuknummering**.
7. Selecteer **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
