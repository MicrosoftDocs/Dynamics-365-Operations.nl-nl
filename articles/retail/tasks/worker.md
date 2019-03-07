---
title: " Een medewerker configureren"
description: Deze procedure laat zien hoe u een medewerker detailhandel als een vertegenwoordiger kunt configureren die voor provisie op verkopen in POS aanmerking komt.
author: jblucher
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 797640b487884fc487582addea274007e4ba7a7d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "362528"
---
# <a name="configure-a-worker"></a> Een medewerker configureren

[!include[task guide banner](../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u een medewerker detailhandel als een vertegenwoordiger kunt configureren die voor provisie op verkopen in POS aanmerking komt. Deze procedure gebruikt het demobedrijf USRT.


## <a name="create-a-commission-sales-group-for-the-worker"></a>Een provisieverkoopgroep voor de medewerker maken
1. Ga naar Verkoop en marketing > Provisies > Verkoopgroepen.
    * Werknemers kunnen aan een of meerdere verkoopgroepen worden toegewezen. In POS kunt u een willekeurige verkoopgroep kiezen die werknemers bevat uit het adresboek van de opslag.  
2. Klik op Nieuw.
3. Typ een waarde in het veld Groep.
4. Typ een waarde in het veld Naam.
5. Klik op Opslaan.
6. Klik in het actievenster op Algemeen.
7. Klik op Vertegenwoordiger.
    * Een verkoopgroep kan meer dan een werknemer bevatten. Provisies kunnen tussen werknemers worden gesplitst op basis van hoe u het provisieaandeel definieert.  
8. Typ of selecteer een waarde in het veld Naam.
9. Typ een getal in het veld Provisieaandeel.
10. Klik op Opslaan.
11. Sluit de pagina.
12. Sluit de pagina.

## <a name="assign-the-workers-default-sales-group"></a>De standaardverkoopgroep toewijzen aan medewerkers
1. Ga naar Detailhandel en commerce > Werknemers > Werknemers.
2. Zoek en selecteer de gewenste record in de lijst.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Klik op het tabblad Detailhandel.
    * Een werknemer kan aan een standaardverkoopgroep worden toegewezen. De standaardverkoopgroep wordt automatisch toegevoegd aan verkoopregels in POS als de optie in het functionaliteitprofiel voor de opslag is ingeschakeld.  
5. Klik op Bewerken.
6. Typ of selecteer een waarde in het veld Standaardgroep.
7. Klik op Opslaan.

