--- 
title: Het veiligheidsvoorraadjournaal gebruiken om de minimumbehoefteplanning bij te werken
description: Deze procedure laat zien hoe u voorstellen voor minimumbehoefteplanning kunt berekenen op basis van historische transacties en vervolgens de artikelbehoefteplanning kunt bijwerken met de voorstellen.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d278b20724006ec3b3aa557738e8b130ca2bba15
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a>Het veiligheidsvoorraadjournaal gebruiken om de minimumbehoefteplanning bij te werken

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u voorstellen voor minimumbehoefteplanning kunt berekenen op basis van historische transacties en vervolgens de artikelbehoefteplanning kunt bijwerken met de voorstellen. Dit wordt gedaan via het veiligheidsvoorraadjournaal. Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF. Deze taak is bedoeld voor de productieplanner om te helpen de minimumbehoefteplanning te onderhouden.


## <a name="create-a-new-safety-stock-journal-name"></a>Een nieuw veiligheidsvoorraadjournaal maken
1. Ga naar Journaalnamen veiligheidsvoorraad.
2. Klik op Nieuw.
3. Typ 'Materiaal' in het veld Naam.
4. Typ 'Materiaal' in het veld Omschrijving.
5. Sluit de pagina.

## <a name="create-a-safety-stock-journal"></a>Een veiligheidsvoorraadjournaal maken
1. Ga naar Berekening van veiligheidsvoorraad.
2. Klik op Nieuw.
3. Typ of selecteer een waarde in het veld Naam.
    * Selecteer de naam van het veiligheidsvoorraadjournaal dat u hebt gemaakt, bijvoorbeeld Materiaal.  
4. Klik op Regels maken.
5. Voer een datum in het veld Begindatum in.
    * Stel de datum in op '2015-01-02'.  
6. Voer een datum in het veld Einddatum in.
    * Stel de datum in op '2015-12-30'.  
7. Klik op OK.
    * Hiermee worden regels gemaakt voor de dimensies die voorraadtransacties hebben.  

## <a name="calculate-proposal"></a>Voorstel berekenen
1. Klik op Voorstel berekenen.
2. Selecteer de optie Gemiddelde uitgifte tijdens doorlooptijd gebruiken.
3. Stel de vermenigvuldigingsfactor in op '10'.
    * De vermenigvuldigingsfactor wordt gebruikt om het voorstel te corrigeren. Omdat demogegevens slechts enkele transacties bevatten, moet u de factor instellen om een realistisch voorstel te krijgen.  
4. Klik op OK.
    * Blader omlaag om M0002 en M0003 te zoeken. Bekijk de kolom Berekende minimumhoeveelheid.   

## <a name="update-minimum-quantity"></a>Minimumhoeveelheid bijwerken
1. Voer een getal in het veld Nieuwe minimumhoeveelheid in.
    * Werk de nieuwe minimumhoeveelheid bij op basis van de waarde in Berekende minimumhoeveelheid. Als het berekende minimum nul is, kunt u de gewenste toekomstige waarde invoeren. Zo kunt u bijvoorbeeld de berekende minimumhoeveelheid in dit veld invoeren voor M0002 in magazijn 12.  
2. Zoek en selecteer de gewenste record in de lijst.
    * U kunt bijvoorbeeld M0002 selecteren in magazijn 12.  
3. Voer een getal in het veld Nieuwe minimumhoeveelheid in.
    * Werk de nieuwe minimumhoeveelheid bij op basis van de waarde in Berekende minimumhoeveelheid. Als het berekende minimum nul is, kunt u de gewenste toekomstige waarde invoeren.  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a>De nieuwe minimumhoeveelheid boeken en het resultaat valideren
1. Klik op Boeken.
2. Klik op OK.
3. Klik om de koppeling in het veld Artikelnummer te volgen.
4. Klik om de koppeling in het veld Artikelnummer te volgen.
5. Klik in het actievenster op Plannen.
6. Klik op Artikelbehoefteplanning.
    * Merk op dat de minimumhoeveelheid is bijgewerkt met de nieuwe minimumhoeveelheid uit het veiligheidsvoorraadjournaal.  


