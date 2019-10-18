---
title: 'ER Financiële dimensies gebruiken als gegevensbron (deel 4: het rapport uitvoeren)'
description: In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan configureren om financiële dimensies te gebruiken als bron voor ER-rapporten.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aa5b726a7c400da09381944f3303f7ac4bb796aa
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182411"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4-run-the-report"></a>ER Financiële dimensies gebruiken als gegevensbron (Deel 4: het rapport uitvoeren)

[!include [task guide banner](../../includes/task-guide-banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan configureren om financiële dimensies te gebruiken als bron voor ER-rapporten. Deze stappen kunnen in het DEMF-bedrijf worden uitgevoerd.

Als u deze stappen wilt uitvoeren, moet u eerst de stappen uitvoeren in de procedure “ER Financiële dimensies gebruiken als gegevensbron (Deel 3: Het rapport ontwerpen)”. U moet ook standaarddocumenttypen op pagina Parameters van elektronische rapportage configureren. De standaarddocumenttypen worden ook ingesteld als u een ER-configuratie downloadt en importeert. 


## <a name="run-report"></a>Rapport uitvoeren
1. Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.
2. Vouw in de structuur 'Voorbeeldmodel Financiële dimensies' uit.
3. Selecteer in de structuur 'Voorbeeldmodel Financiële dimensies\Grootboekjournaalrapport'.
4. Klik op Uitvoeren.
5. Typ of selecteer een waarde in het veld Dimensienaam.
    * Om alle dimensies in het huidige bedrijf te selecteren, typt u het volgende: BusinessUnit;CostCenter;Afdeling; ItemGroup;MainAccount;Project  
6. Breid de sectie Op te nemen records uit.
7. Klik op Filter.
8. Selecteer de rij voor de tabel Grootboekjournaal en het veld Batchnummer journaal.
9. Typ 00057 in het veld Criteria.
10. Klik op OK.
11. Klik op OK.
    * Controleer de gegenereerde uitvoer. Merk op dat voor elke transactie van de geselecteerde batch, de financiële dimensies uit de bijbehorende ingestelde dimensies worden weergegeven. Voer dit rapport uit en selecteer verschillende dimensies om te zien of het rapport niet afhankelijk is van het geselecteerde aantal dimensies of het aantal dimensies dat voor dit exemplaar is geconfigureerd.  

