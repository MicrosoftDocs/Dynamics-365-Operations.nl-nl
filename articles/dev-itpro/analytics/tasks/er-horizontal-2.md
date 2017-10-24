--- 
title: Een indeling uitvoeren die gebruikmaakt van horizontaal uitvouwbare bereiken voor het dynamisch toevoegen van kolommen in Excel-rapporten voor elektronische aangifte (ER)
description: In de volgende stappen wordt uitgelegd hoe een gebruiker die aan de rol van systeembeheerder of ontwikkelaar elektronische rapportage is toegewezen, een elektronische rapportindeling (ER) kan configureren om rapporten als OPENXML-werkbladen (Excel-bestanden) te genereren waarin de vereiste kolommen dynamisch kunnen worden gemaakt als horizontaal uitvouwbare bereiken.
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 8e5c53905b903bc5242625283f3b093144243cf9
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="run-a-format-that-uses-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-for-electronic-reporting-er"></a>Een indeling uitvoeren die gebruikmaakt van horizontaal uitvouwbare bereiken voor het dynamisch toevoegen van kolommen in Excel-rapporten voor elektronische aangifte (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker die aan de rol van systeembeheerder of ontwikkelaar elektronische rapportage is toegewezen, een elektronische rapportindeling (ER) kan configureren om rapporten als OPENXML-werkbladen (Excel-bestanden) te genereren waarin de vereiste kolommen dynamisch kunnen worden gemaakt als horizontaal uitvouwbare bereiken. Deze stappen kunnen in het DEMF-bedrijf worden uitgevoerd.

Als u deze stappen wilt uitvoeren, voert u eerst de stappen uit in de procedure "ER Gebruik horizontaal uitvouwbare bereiken om kolommen in Excel-rapporten dynamisch toe te voegen (Deel 1: Ontwerpindeling)".

Deze procedure is voor een functie die in versie 1611 van Dynamics 365 for Operations is toegevoegd.


## <a name="find-created-format"></a>Gemaakte indeling zoeken
1. Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.
2. Vouw in de structuur 'Voorbeeldmodel Financiële dimensies' uit.
3. In de structuur selecteert u 'Voorbeeldmodel Financiële dimensies\Voorbeeldrapport met horizontaal uitvouwbare bereiken'.

## <a name="execute-format-to-create-excel-output"></a>Indeling uitvoeren om Excel-uitvoer te maken
1. Klik op Uitvoeren.
2. Typ in het veld Dimensienaam 'BusinessUnit;CostCenter;Department'.
    * Typ of selecteer een waarde in het veld Dimensienaam.  Om alle dimensies voor het huidige bedrijf te selecteren, voert u het volgende in: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
3. Breid de sectie Op te nemen records uit.
4. Klik op Filter.
5. Selecteer de rij voor de tabel Grootboekjournaal en het veld Batchnummer journaal.
6. Typ in het veld Criteria '00057..00058'.
    * 00057..00058  
7. Klik op OK.
8. Klik op OK.
    * Controleer de gegenereerde uitvoer. Houd er rekening mee dat het nieuwe Excel-bestand hetzelfde aantal kolommen bevat als voor financiële dimensies zijn ingeschakeld. De rapportkoptekst in deze kolommen geeft de namen van de financiële dimensies weer. De transactieregels in deze kolommen geven de financiële dimensies weer. Voer dit rapport uit en selecteer verschillende dimensies om te zien of het rapport niet afhankelijk is van het geselecteerde aantal dimensies of het aantal dimensies dat voor dit exemplaar van Dynamics 365 for Finance and Operations, Enterprise edition, is geconfigureerd.  


