---
title: Fiscale kalenders, boekjaren en boekperioden
description: In dit artikel worden fiscale kalenders, boekjaren en perioden beschreven en wordt aangegeven hoe ze voor rechtspersonen, vaste activa en budgettering moeten worden gebruikt.
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FiscalCalendars
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 25851
ms.assetid: a968a5e5-585e-4389-aa4e-c885a7e23413
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 22a08b1b9e819f5c683d278f37bf3404e757d200
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="fiscal-calendars-fiscal-years-and-periods"></a>Fiscale kalenders, boekjaren en boekperioden

[!include[banner](../includes/banner.md)]


In dit artikel worden fiscale kalenders, boekjaren en perioden beschreven en wordt aangegeven hoe ze voor rechtspersonen, vaste activa en budgettering moeten worden gebruikt.

Fiscale kalenders vormen een raamwerk voor de financiële activiteiten van een organisatie. Elke fiscale kalender bevat een of meer boekjaren, en elk boekjaar bevat meerdere perioden. Fiscale kalenders kunnen zijn gebaseerd op een kalenderjaar van 1 januari tot 31 december op elke andere datum die u selecteert. Sommige organisaties kiezen bijvoorbeeld een fiscale kalender die op 1 juli van het ene jaar begint en op 30 juni van het volgende jaar eindigt. 

Er is geen limiet voor het aantal fiscale kalenders dat u kunt maken, en geen limiet voor het aantal boekjaren dat voor een fiscale kalender kan worden gemaakt. Elke fiscale kalender is onafhankelijk van uw organisatie en kan door meerdere rechtspersonen in de organisatie worden gebruikt. Stel, een organisatie heeft acht afdelingen en elke afdeling heeft een eigen rechtspersoon. Vijf daarvan hanteren dezelfde fiscale kalender en drie gebruiken andere fiscale kalenders. U kunt één fiscale kalender maken voor de vijf rechtspersonen die dezelfde fiscale kalender delen, en vervolgens afzonderlijke fiscale kalenders maken voor de andere rechtspersonen.

## <a name="create-fiscal-calendars-fiscal-years-and-periods"></a>Fiscale kalenders, boekjaren en boekperioden maken
Op de pagina Fiscale kalenders kunt u fiscale kalenders, boekjaren en boekperioden maken en verwijderen. U kunt bestaande perioden ook opsplitsen en afsluitingsperioden maken die kunnen worden gebruikt om een boekjaar af te sluiten. 

Een afsluitperiode wordt gebruikt voor grootboektransacties die worden gegenereerd bij het afsluiten van een boekjaar. Als de afsluittransacties zijn opgenomen in één boekperiode, is het eenvoudiger om financiële overzichten te maken, zowel met als zonder verschillende soorten afsluitboekingen. Als een boekjaar is verdeeld in twaalf boekperioden, is de afsluitperiode meestal de dertiende periode. Het is echter mogelijk om een afsluitperiode te maken van elke periode met de status Open. 

Als u een afsluitperiode maakt, selecteert u een periode met de status Open die de gewenste datums bevat. De begin- en einddatum van de afsluitperiode worden uit de huidige periode gekopieerd. De oorspronkelijke periode blijft bestaan. Stel dat u Periode 12 selecteert, de laatste periode in het boekjaar, die de datums van 1 augustus tot en met 31 augustus bevat. U geeft een naam voor de afsluitperiode op, bijvoorbeeld Afsluiting. Nadat u de nieuwe afsluitperiode hebt gemaakt, beschikt u over de oorspronkelijke periode en de afsluitperiode. Beide perioden beginnen op 1 augustus en eindigen op 31 augustus.

## <a name="select-fiscal-calendars-for-ledgers-fixed-assets-and-budget-cycles"></a>Fiscale kalenders selecteren voor grootboeken, vaste activa en budgetcycli
Fiscale kalenders worden gebruikt voor afschrijving van vaste activa, financiële transacties en budgetcycli. Wanneer u een fiscale kalender maakt, kunt u deze voor meerdere doeleinden gebruiken. U kunt een fiscale kalender voor een waardemodel of afschrijvingsboek selecteren om er een kalender voor vaste activa van te maken. U kunt een fiscale kalender voor een grootboek selecteren om er een grootboekkalender van te maken. En u kunt een fiscale kalender voor een budgetcyclus selecteren om er een budgetkalender van te maken. U kunt hiervoor dezelfde fiscale kalender gebruiken.

### <a name="select-a-fiscal-calendar-for-your-legal-entity"></a>Een fiscale kalender voor uw rechtspersoon selecteren

Selecteer in het formulier Grootboek de fiscale kalender die u wilt gebruiken voor het grootboek voor uw rechtspersoon. Voor elke rechtspersoon moet een fiscale kalender worden geselecteerd op de pagina Grootboek. Nadat u een fiscale kalender hebt geselecteerd, kunt u op de pagina Grootboekkalender de statuswaarden en machtigingen instellen voor de perioden die deel uitmaken van een boekjaar.

### <a name="select-a-fiscal-calendar-for-fixed-assets"></a>Een fiscale kalender voor vaste activa selecteren

U kunt een fiscale kalender voor een waardemodel of afschrijvingsboek selecteren. Die fiscale kalender wordt gebruikt door de vaste activa die het geselecteerde waardemodel of afschrijvingsboek gebruiken. U kunt een selectie maken uit alle fiscale kalenders die op de pagina Fiscale kalenders zijn gedefinieerd.

### <a name="define-budget-cycle-time-spans"></a>Budgetcyclusduren definiëren

Budgetcycli geven aan hoelang een budget wordt gebruikt. Budgetcycli kunnen een deel van een boekjaar of meerdere boekjaren bevatten, zoals een tweejarige of driejarige budgetcyclus. De budgetcyclusduur geeft aan uit hoeveel perioden de budgetcyclus bestaat. Gebruik de pagina Budgetcyclusduren om de budgetcyclusduur op te geven.

## <a name="maintain-periods-for-your-organization"></a>Perioden voor uw organisatie onderhouden
Met de pagina Grootboekkalender kunt u de details bekijken van de fiscale kalender, boekjaren en boekperioden die door uw organisatie worden gebruikt. U kunt ook de status van de perioden wijzigen en selecteren welke gebruikers boekhoudtransacties naar perioden kunnen boeken. Aan het begin van een nieuwe periode wilt u misschien dat een groep gebruikers het boeken van financiële transacties in de voorgaande periode kan afmaken, terwijl andere groepen alleen in de nieuwe periode kunnen werken.






