---
title: 'ER Financiële dimensies gebruiken als gegevensbron (deel 4: het rapport uitvoeren)'
description: In dit artikel wordt beschreven hoe u een ER-model (Electronic Reporting) configureert om financiële dimensies te gebruiken als gegevensbron voor ER-rapporten. (Deel 4)
author: kfend
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERSolutionTable, SysQueryForm
ms.openlocfilehash: d0fca8b1a6139b71782af05531d9494c968ef9f5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290749"
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
![Uitschuifvenster Parameters elektronisch rapport, vervolgkeuzelijst Dimensienaam.](../media/er-financial-dimensions-guides-run2.png)
6. Breid de sectie Op te nemen records uit.
7. Klik op Filter.
8. Selecteer de rij voor de tabel Grootboekjournaal en het veld Batchnummer journaal.
9. Typ 00057 in het veld Criteria.
10. Klik op OK.
11. Klik op OK.
![Uitschuifvenster Parameters elektronisch rapport, sectie met op te nemen rapporten.](../media/er-financial-dimensions-guides-run3.png)
    * Controleer de gegenereerde uitvoer. Voor elke transactie van de geselecteerde batch worden de financiële dimensies uit de bijbehorende ingestelde dimensies weergegeven. Voer dit rapport uit en selecteer verschillende dimensies om te zien of het rapport niet afhankelijk is van het geselecteerde aantal dimensies of het aantal dimensies dat voor dit exemplaar is geconfigureerd.  
![Gegenereerde uitvoer van ER-configuraties.](../media/er-financial-dimensions-guides-run4.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
