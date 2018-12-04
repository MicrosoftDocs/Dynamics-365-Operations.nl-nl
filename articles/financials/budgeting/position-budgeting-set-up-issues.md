---
title: Probleemoplossing voor positiebudgettering
description: Dit artikel bevat beantwoorden op vragen die u kunt hebben wanneer u positiebudgettering configureert. Het behandelt vaak gestelde vragen over hoe u budgetkostenelementen, compensatiegroepen en compensatierasters maakt.
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmBudgetPurposeType, HcmPositionForecast
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 88253
ms.assetid: c44df01b-8700-4022-b4c6-c4b1cb84d31d
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f2ef04008a5e6339a2193f9fcc77f2e0e6643557
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="position-budgeting-troubleshooting"></a>Probleemoplossing voor positiebudgettering

[!include [banner](../includes/banner.md)]

Dit artikel bevat beantwoorden op vragen die u kunt hebben wanneer u positiebudgettering configureert. Het behandelt vaak gestelde vragen over hoe u budgetkostenelementen, compensatiegroepen en compensatierasters maakt. 

<a name="why-cant-i-find-the-forecast-position-page-in-human-resources"></a>Waarom kan ik de prognosepositiepagina in Human resources niet vinden?
---------------------------------------------------------------

Prognoseposities zijn verplaatst naar Budgettering.

## <a name="why-cant-i-delete-a-budget-cost-element"></a>Waarom kan ik geen budgetkostenelement verwijderen?
U kunt geen budgetkostenelement verwijderen dat aan een prognosepositie is toegewezen. Voordat u een budgetkostenelement kunt verwijderen, moet u het uit alle prognoseposities verwijderen. **Tip:** als u alle posities wilt zoeken waaraan een budgetkostenelement is toegewezen, selecteert u het kostenelement op de pagina **Budgetkostenelementen** en klikt u vervolgens op **Posities bijwerken** De posities die het kostenelement gebruiken, worden in het bovenste raster weergegeven.

## <a name="how-can-i-remove-a-cost-element-from-multiple-forecast-positions-without-opening-each-one"></a>Hoe kan ik een kostenelement verwijderen uit meerdere prognoseposities zonder elke positie te openen?
U kunt een kostenelement niet verwijderen. U kunt echter wel de begin- en einddatum wijzigen, zodat deze vallen buiten de datums van de budgetplanningscyclus. Het kostenelement wordt dan niet meer toegewezen aan prognoseposities in die budgetplanningscyclus. Als u deze wijziging wilt aanbrengen, opent u het budgetkostenelement, klikt u op het sneltabblad **Kostenberekening** op **Datums wijzigen** en wijzigt u de ingangsdatum of de vervaldatum. Klik op **OK** om automatisch alle prognoseposities bij te werken waaraan het kostenelement is toegewezen. **Tip:** als u deze methode gebruikt, moet u er rekening mee houden dat het budgetkostenelement uit **alle** prognoseposities wordt verwijderd waarin de begin- en de einddatum niet meer binnen het juiste bereik liggen. Als dit niet is wat u wilt, moet u elke prognosepositie openen waaruit u het budgetkostenelement wilt verwijderen en de wijziging handmatig aanbrengen.

## <a name="why-cant-i-enter-an-annual-amount-on-the-cost-calculation-fasttab-for-the-budget-cost-element"></a>Waarom kan ik geen jaarlijks bedrag invoeren op het sneltabblad Kostenberekening voor het budgetkostenelement?
U kunt geen jaarlijks bedrag invoeren als er budgetkostenelementen op het sneltabblad **Berekeningsbasis** staan, omdat het systeem een percentage vereist om de waarde te berekenen. Als u de waarde wilt wijzigen, verwijdert u alle budgetkostenelementen uit het sneltabblad **Berekeningsbasis**.

## <a name="why-cant-i-change-the-budget-cost-type-from-earning-to-another-budget-cost-type"></a>Waarom kan ik het budgetkostentype niet wijzigen van inkomsten in een ander budgetkostentype?
Sommige budgetkostenelementen gebruiken het kostenelement inkomsten als berekeningsbasis. Als u het veld **Budgetkostentype** wilt wijzigen, verwijdert u het kostenelement inkomsten uit het sneltabblad **Berekeningsbasis** van alle budgetkostenelementen.

## <a name="why-cant-i-change-the-date-on-budget-cost-element-lines-for-a-budget-cost-element"></a>Waarom kan ik de datum op de regels van budgetkostenelementen niet wijzigen voor een budgetkostenelement?
U kunt de datum in het budgetkostenelement niet wijzigen wanneer een budgetkostenelement door een prognosepositie wordt gebruikt. Deze beperking helpt ervoor zorgen dat de prognoseposities altijd binnen de richtlijnen van het budgetkostenelement zijn. Als u de datum wilt wijzigen, klikt u op sneltabblad **Kostenberekening**, klikt u op **Datums wijzigen** en voert u de nieuwe datums in. Klik vervolgens op **OK** om automatisch de posities bij te werken waaraan het kostenelement is toegewezen.

## <a name="why-cant-i-change-the-costs-for-a-budget-cost-element-on-the-compensation-group-page"></a>Waarom kan ik de kosten voor een budgetkostenelement niet wijzigen op de pagina Compensatiegroep?
U kunt budgetkostenelementen alleen wijzigen op de pagina **Budgetkostenelementen**.

## <a name="why-do-i-receive-an-error-message-when-i-change-the-dates-for-a-cost-element-on-a-forecast-position"></a>Waarom krijg ik een foutmelding wanneer ik de datums voor een kostenelement wijzig in een prognosepositie?
De datums op de prognosepositiekostenelementregel moeten binnen de volgende bereiken vallen:

-   De activerings- en deactiveringsdata van de positie.
-   De activerings- en de vervaldata van het budgetkostenelement.
-   De begin- en einddatums van de budgetcyclus die aan het budgetplanningsproces van de prognosepositie is gekoppeld.





