---
title: Aanvraagtypen en scoringscriteria maken voor offerteaanvragen
description: Deze handleiding laat zien hoe u een verzoektype kunt maken en dit kunt koppelen aan een scoringsmethode.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1a3e0d00d674af913953d7fd01183b0289c20d3d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844093"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a>Aanvraagtypen en scoringscriteria maken voor offerteaanvragen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze handleiding laat zien hoe u een verzoektype kunt maken en dit kunt koppelen aan een scoringsmethode. Er wordt tevens weergegeven hoe u het verzoektype kunt gebruiken in een offerteaanvraag, waarbij vervolgens de standaardscoringsmethode wordt ingesteld. Deze taken worden meestal uitgevoerd door een inkoopmanager. U kunt deze procedure gebruiken met het demogegevensbedrijf USMF of met uw eigen gegevens. U moet over een scoringsmethode beschikken voordat u van start gaat.


## <a name="create-a-solicitation-type"></a>Een nieuw verzoektype maken
1. Ga naar Inkoopbeheer > Instellingen > Offerteaanvraag > Sollicitatietype.
2. Klik op Nieuw.
3. Typ een waarde in het veld Naam.
4. Typ een waarde in het veld Omschrijving.
5. Selecteer in het veld Scoringsmethod de scoringsmethode die u wilt gebruiken voor dit verzoektype.
6. Klik op Opslaan.
7. Sluit de pagina.

## <a name="use-the-solicitation-type"></a>Het verzoektype gebruiken
1. Ga naar Inkoop en sourcing > Offerteaanvragen > Alle offerteaanvragen.
2. Klik op Nieuw.
3. Selecteer in het veld Verzoektype het verzoektype dat u zojuist hebt gemaakt. 
    *   
4. Klik op OK.
5. Klik op Scoringscriteria.
    * De scoringscriteria die worden weergegeven zijn afkomstig van de scoringsmethode die u aan het verzoektype hebt gekoppeld. U kunt ervoor kiezen criteria toe te voegen of te verwijderen op deze pagina. Het is ook mogelijk om nieuwe criteria toe te voegen door deze vanuit andere scoringsmethoden te kopiëren.  
6. Klik op Criteria kopiëren.
7. Typ of selecteer een waarde in het veld Scoringsmethode.
8. Klik op OK.
9. Sluit de pagina.

