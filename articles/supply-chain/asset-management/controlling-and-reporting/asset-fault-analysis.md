---
title: Foutanalyse activum
description: In dit onderwerp worden foutanalyses voor activa in Activabeheer uitgelegd.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectFaultCalculate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 913e5cf8d39dfe36efea0526d84808e7d736b030
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6361143"
---
# <a name="asset-fault-analysis"></a>Foutanalyse activum

[!include [banner](../../includes/banner.md)]

 

In Activabeheer kunt u foutregistraties voor activa analyseren om een overzicht weer te geven van het totale aantal fouten dat tijdens een bepaalde periode is geregistreerd. Foutregistraties kunnen vanuit verschillende perspectieven worden geanalyseerd, bijvoorbeeld met de focus op activa, activatypen, functionele locaties, foutsymptomen of fouttypen.

1. Klik op **Activabeheer** > **Query's** > **Activafout** > **Foutanalyse activum**.

2. In het dialoogvenster **Berekening van foutanalyse voor activa** kunt u het veld **Niveau** gebruiken om aan te geven hoe gedetailleerd de activafoutregels met betrekking tot functionele locaties moeten zijn. 

    Als u bijvoorbeeld het getal 1 invoegt in het veld en u een structuur met meerdere niveaus voor functionele locaties hebt, worden alle activafoutregels voor een functionele locatie weergegeven op het hoogste niveau. Daarom kunnen de uren op een regel zijn opgeteld op basis van functionele locaties die zich op een lager niveau bevinden. 
        
    Als u het getal 0 in het veld **Niveau** invoegt, wordt er een gedetailleerd resultaat met alle activafoutregels weergegeven op alle niveaus voor functionele locaties waarop deze betrekking hebben.

3. Als u de zoekopdracht wilt beperken, kunt u specifieke activa, foutdatums, foutoorzaken en probleemoplossingen selecteren op het sneltabblad **Op te nemen records**.

4. Klik op **OK** om de berekening te starten.

5. Klik op het tabblad **Foutanalyse activum** op een of meer knoppen **Groeperen op** om het gewenste detailniveau weer te geven. Geactiveerde knoppen zijn gemarkeerd. U kunt knoppen activeren of deactiveren door erop te klikken.

6. Klik op **Berekeningen bijwerken** om uw selecties op het scherm weer te geven. 

>[!NOTE]
>Telkens wanneer u een knop **Groeperen op** activeert of deactiveert, moet u niet vergeten op de knop **Berekeningen bijwerken** te klikken. Dit is vereist omdat een grote hoeveelheid gegevens wordt verwerkt terwijl u de foutwaarschijnlijkheid opnieuw berekent.

## <a name="examples"></a>Voorbeelden

Er zijn veel manieren om foutregistraties te analyseren. Deze sectie bevat vijf voorbeelden van hoe verschillende gegevensselecties meer inzicht en details kunnen bieden bij het analyseren van foutregistraties voor activa.

### <a name="group-by-symptoms"></a>Groeperen op symptomen

In de onderstaande schermafbeelding is alleen de knop **Symptoom** geselecteerd.

- Er zijn foutregistraties uitgevoerd voor drie foutsymptomen: Luchtlek, Gesprongen zekering en Vastgelopen apparatuur.  
- In de kolom **Waarschijnlijkheidspercentage** zijn alle percentages bij elkaar 100%. De waarschijnlijkheid is gebaseerd op alle **symptoomregistraties** in deze foutanalyse.

![Figuur 1.](media/06-controlling-and-reporting.png)

### <a name="group-by-symptoms-and-time-period"></a>Groeperen op symptomen en tijdsperiode

In de onderstaande schermafbeelding worden **Jaar** en **Maand** toegevoegd om aan te geven hoe u tijdens een geselecteerde periode foutregistraties kunt weergeven.

- De foutsymptomen worden nu weergegeven als registraties per jaar/maand.  
- Als u in de kolom **Waarschijnlijkheidspercentage** alle percentages voor elke maand optelt, komt u uit op 100%. De waarschijnlijkheid is gebaseerd op de **symptoomregistraties** in deze foutanalyse. Als u een groot aantal regels voor een activum hebt, maar een groot percentage op een regel staat, is dit een indicatie van een foutsymptoom om nader te onderzoeken of het aantal registraties voor dit foutsymptoom kan worden beperkt.

![Figuur 2.](media/07-controlling-and-reporting.png)

### <a name="group-by-multiple-symptoms-and-assets"></a>Groeperen op meerdere symptomen en activa

De combinatie van activa en een activumtype wordt gebruikt als basis voor de berekeningen die worden weergegeven in de drie onderstaande schermafbeeldingen, die steeds gedetailleerder worden.  

Over het algemeen geldt dat de knoppen in de actievenstergroepen **Groeperen op datum**, **Groeperen op activum**, **Groeperen op functionele locatie** en de knop **Fout** (fout-id) periodes of activarelaties bevatten. De knoppen **Symptoom**, **Gebied**, **Type**, **Oorzaak** en **Oplossing** zijn categorisaties die in foutbeheer worden gebruikt om foutregistraties te analyseren en probleemgebieden te identificeren.  

**Groeperen op symptoom, activum en activatype**

In de onderstaande schermafbeelding zijn **Activum** en **Activumtype** toegevoegd om meer details te bieden over foutregistraties.

- De foutsymptomen zijn nu opgesplitst in combinaties van **Activum** / **Activumtype** / **Symptoom**.  
- Als u in de kolom **Waarschijnlijkheidspercentage** alle percentages voor de combinatie van **Activum** / **Activumtype** / **Symptoom** optelt, komt u uit op 100%. De waarschijnlijkheid is gebaseerd op **symptoomregistraties** in deze foutanalyse. Als u een groot aantal regels voor een activum hebt, maar een groot percentage op een regel staat, is dit een indicatie van een foutsymptoom om nader te onderzoeken of het aantal registraties voor dit foutsymptoom kan worden beperkt.

![Figuur 3.](media/08-controlling-and-reporting.png)

**Groeperen op twee symptomen, activum en activatype**

In de onderstaande schermafbeelding is **Gebied** toegevoegd aan **Symptoom**, **Activum** en **Activumtype** om meer details te bieden over foutregistraties.

- Als u in de kolom **Waarschijnlijkheidspercentage** alle percentages voor de combinatie van **Activum** / **Activumtype** / **Symptoom** voor een activum optelt, komt u uit op 100%. De waarschijnlijkheid is gebaseerd op de combinatie van **Symptoom** en **Gebied** in deze foutanalyse. Als u een groot aantal regels voor een activum hebt, maar een groot percentage op een regel staat, is dit een indicatie van een foutgebied om nader te onderzoeken of het aantal registraties voor dit foutgebied kan worden beperkt.  

![Figuur 4.](media/09-controlling-and-reporting.png)

**Groeperen op drie symptomen, activum en activatype**

In de onderstaande schermafbeelding is **Type** toegevoegd en de meest gedetailleerde berekening wordt in dit voorbeeld weergegeven.
 
- Als u in de kolom **Waarschijnlijkheidspercentage** alle percentages voor de combinatie van **Activum** / **Activumtype** / **Symptoom** voor een activum optelt, komt u uit op 100%. De waarschijnlijkheid is gebaseerd op de combinatie van **Symptoom**, **Gebied** en **Type** in deze foutanalyse. Als u een groot aantal regels voor een activum hebt, maar een groot percentage op een regel staat, is dit een indicatie van een fouttype om nader te onderzoeken of het aantal registraties voor dit fouttype kan worden beperkt.

![Figuur 5.](media/10-controlling-and-reporting.png)


>[!NOTE]
>Voor een overzicht van alle gemaakte foutregistraties voor werkorders en onderhoudsverzoeken klikt u op **Activabeheer** > **Query's** > **Activafout** > **Activafouten**. Selecteer op de pagina **Activafouten** een activumfoutregistratie en vouw het deelvenster **Verwante informatie** uit om informatie over de bijbehorende werkorder of het bijbehorende onderhoudsverzoek weer te geven.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]