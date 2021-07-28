---
title: 'ER Financiële dimensies gebruiken als gegevensbron (deel 4: het rapport uitvoeren)'
description: In dit onderwerp wordt beschreven hoe u een ER-model (Electronic Reporting) configureert om financiële dimensies te gebruiken als gegevensbron voor ER-rapporten. (Deel 4)
author: NickSelin
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11d15a9e932eb02fc1bc8960d9c7ecbf4b57a4e8
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356290"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a>ER Financiële dimensies gebruiken als gegevensbron (deel 4: het rapport uitvoeren)

[!include [banner](../../includes/banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan configureren om financiële dimensies te gebruiken als bron voor ER-rapporten. Deze stappen kunnen in het DEMF-bedrijf worden uitgevoerd.

Als u deze stappen wilt uitvoeren, moet u eerst de stappen uitvoeren in de procedure "ER Financiële dimensies gebruiken als gegevensbron (Deel 3: Het rapport ontwerpen)". U moet ook standaarddocumenttypen op pagina Parameters van elektronische rapportage configureren. De standaarddocumenttypen worden ook ingesteld als u een ER-configuratie downloadt en importeert. 


## <a name="run-report"></a>Rapport uitvoeren
1. Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.
2. Vouw in de structuur 'Voorbeeldmodel Financiële dimensies' uit.
3. Selecteer in de structuur 'Voorbeeldmodel Financiële dimensies\Grootboekjournaalrapport'.
4. Klik op Uitvoeren.
![Pagina ER-configuraties.](../media/er-financial-dimensions-guides-run1.png)
5. Typ of selecteer een waarde in het veld Dimensienaam.
    * Om alle dimensies in het huidige bedrijf te selecteren, typt u het volgende: BusinessUnit;CostCenter;Afdeling; ItemGroup;MainAccount;Project  
![Pagina ER-configuraties.](../media/er-financial-dimensions-guides-run2.png)
6. Breid de sectie Op te nemen records uit.
7. Klik op Filter.
8. Selecteer de rij voor de tabel Grootboekjournaal en het veld Batchnummer journaal.
9. Typ 00057 in het veld Criteria.
10. Klik op OK.
11. Klik op OK.
![Pagina ER-configuraties.](../media/er-financial-dimensions-guides-run3.png)
    * Controleer de gegenereerde uitvoer. Voor elke transactie van de geselecteerde batch worden de financiële dimensies uit de bijbehorende ingestelde dimensies weergegeven. Voer dit rapport uit en selecteer verschillende dimensies om te zien of het rapport niet afhankelijk is van het geselecteerde aantal dimensies of het aantal dimensies dat voor dit exemplaar is geconfigureerd.  
![Pagina ER-configuraties.](../media/er-financial-dimensions-guides-run4.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]