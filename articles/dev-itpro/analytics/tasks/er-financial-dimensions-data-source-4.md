--- 
title: "Een rapport uitvoeren dat gebruikmaakt van financiële dimensies als gegevensbron voor elektronische aangifte (ER)"
description: "In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan configureren om financiële dimensies te gebruiken als bron voor ER-rapporten."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: ee951d7f3f04e641f7bed767a2eebd1c180eb9f3
ms.contentlocale: nl-nl
ms.lasthandoff: 03/26/2018

---
# <a name="run-a-report-that-uses-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a>Een rapport uitvoeren dat gebruikmaakt van financiële dimensies als gegevensbron voor elektronische aangifte (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan configureren om financiële dimensies te gebruiken als bron voor ER-rapporten. Deze stappen kunnen in het DEMF-bedrijf worden uitgevoerd.

Als u deze stappen wilt uitvoeren, moet u eerst de stappen uitvoeren in de procedure “ER Financiële dimensies gebruiken als gegevensbron (Deel 3: Het rapport ontwerpen)”. U moet ook standaarddocumenttypen op pagina Parameters van elektronische rapportage configureren. De standaarddocumenttypen worden ook ingesteld als u een ER-configuratie downloadt en importeert. 


## <a name="run-report"></a>Rapport uitvoeren
1. Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.
2. Vouw in de structuur 'Voorbeeldmodel Financiële dimensies' uit.
3. Selecteer in de structuur 'Voorbeeldmodel Financiële dimensies\Grootboekjournaalrapport'.
4. Klik op Uitvoeren.
5. Typ of selecteer een waarde in het veld Dimensienaam.
    * Om alle dimensies in het huidige bedrijf te selecteren, typt u het volgende:
BusinessUnit;CostCenter;Afdeling; ItemGroup;MainAccount;Project  
6. Breid de sectie Op te nemen records uit.
7. Klik op Filter.
8. Selecteer de rij voor de tabel Grootboekjournaal en het veld Batchnummer journaal.
9. Typ 00057 in het veld Criteria.
10. Klik op OK.
11. Klik op OK.
    * Controleer de gegenereerde uitvoer. Merk op dat voor elke transactie van de geselecteerde batch, de financiële dimensies uit de bijbehorende ingestelde dimensies worden weergegeven. Voer dit rapport uit en selecteer verschillende dimensies om te zien of het rapport niet afhankelijk is van het geselecteerde aantal dimensies of het aantal dimensies dat voor dit exemplaar van Dynamics 365 for Finance and Operations, is geconfigureerd.  


