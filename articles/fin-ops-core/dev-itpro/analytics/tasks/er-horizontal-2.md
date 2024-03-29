---
title: 'ER Horizontaal uitvouwbare bereiken gebruiken om kolommen in Excel-rapporten dynamisch toe te voegen (deel 2: Indeling uitvoeren)'
description: In dit artikel wordt beschreven hoe u een ER-indeling (Electronic Reporting) configureert om rapporten te genereren als OPENXML-werkbladbestanden (Excel). (Deel 2)
author: kfend
ms.date: 08/29/2018
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
ms.openlocfilehash: 08755eafa2a18993ba669f0deccd75477bfae410
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290389"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a>ER Horizontaal uitvouwbare bereiken gebruiken om kolommen in Excel-rapporten dynamisch toe te voegen (deel 2: Indeling uitvoeren)

[!include [banner](../../includes/banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker die aan de rol van systeembeheerder of ontwikkelaar elektronische rapportage is toegewezen, een elektronische rapportindeling (ER) kan configureren om rapporten als OPENXML-werkbladen (Excel-bestanden) te genereren waarin de vereiste kolommen dynamisch kunnen worden gemaakt als horizontaal uitvouwbare bereiken. Deze stappen kunnen in het DEMF-bedrijf worden uitgevoerd.

Als u deze stappen wilt uitvoeren, voert u eerst de stappen uit in de procedure "ER Gebruik horizontaal uitvouwbare bereiken om kolommen in Excel-rapporten dynamisch toe te voegen (Deel 1: Ontwerpindeling)".

Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.


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
    * Controleer de gegenereerde uitvoer. Houd er rekening mee dat het nieuwe Excel-bestand hetzelfde aantal kolommen bevat als voor financiële dimensies zijn ingeschakeld. De rapportkoptekst in deze kolommen geeft de namen van de financiële dimensies weer. De transactieregels in deze kolommen geven de financiële dimensies weer. Voer dit rapport uit en selecteer verschillende dimensies om te zien of het rapport niet afhankelijk is van het geselecteerde aantal dimensies of het aantal dimensies dat voor dit exemplaar is geconfigureerd.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
