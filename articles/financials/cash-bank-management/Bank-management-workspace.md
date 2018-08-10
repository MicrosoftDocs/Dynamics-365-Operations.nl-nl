---
title: Werkgebied voor bankbeheer
description: Dit onderwerp bevat informatie over het werkgebied Bankbeheer. Dit werkgebied bevat informatie die is gerelateerd aan bedrijfsbankrekeningen en bevat een overzichtsweergave en een analysepagina. De overzichtsweergave bevat overzichtstegels, bankrekeninggegevens, een saldodiagram en gerelateerde informatie. De pagina Analyses gebruikt de mogelijkheden van Microsoft Power BI om visuele elementen te tonen die betrekking hebben op bankrekeningsaldi.
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 92a52646063c145d733b9d2960253004e8eab80a
ms.openlocfilehash: 3c38807e9ed3b2ced37ada35b72e388c125bd654
ms.contentlocale: nl-nl
ms.lasthandoff: 03/05/2018

---
# <a name="bank-management-workspace"></a>Werkgebied voor bankbeheer

[!include [banner](../includes/banner.md)]

Het werkgebied **Bankbeheer** bevat informatie die is gerelateerd aan bedrijfsbankrekeningen. Dit werkgebied bevat een **Overzicht** sweergave en de pagina **Analyses**. De **Overzicht** sweergave bevat overzichtstegels, bankrekeninggegevens, een saldodiagram en gerelateerde informatie. De pagina **Analyses** gebruikt de mogelijkheden van Microsoft Power BI om visuele elementen te tonen die betrekking hebben op bankrekeningsaldi.

## <a name="summary-view"></a>Overzichtsweergave

### <a name="summary"></a>Overzicht

De tegels in de sectie **Overzicht** bieden een overzicht van uw bankrekeningen en snelle toegang tot de pagina's die u het vaakst moet gebruiken. De bankafstemmingsgegevens gelden specifiek voor de functie voor geavanceerde bankafstemming. Informatie wordt alleen opgenomen voor de bankrekeningen waarvoor de optie **Geavanceerde bankafstemming** is ingesteld op **Ja** op de pagina **Bankrekening**. In de sectie **Overzicht** kunt u elektronische bankbestanden voor bankrekeningen importeren voor alle rechtspersonen.

### <a name="bank-accounts"></a>Bankrekeningen

Elke bankrekening in de rechtspersoon wordt vertegenwoordigd door een kaart in de sectie **Bankrekeningen**. Het huidige saldo wordt weergegeven en u kunt inzoomen op de transacties waaruit het overzichtssaldobedrag bestaat. Met het bedrag aan **Overbruggingstransacties** kunt u ook inzoomen op de transacties waaruit dit overzichtsbedrag bestaat. Overbruggingstransacties zijn alle transacties in behandeling die zijn geboekt met behulp van de overbruggingsfunctionaliteit, maar die nog niet zijn verrekend. Het bedrag van **Saldo in behandeling** is het huidige saldo minus de overbruggingstransacties of transacties in behandeling.

De kaart wordt ook weergegeven wanneer de bankrekening voor het laatst is afgestemd. Deze informatie wordt alleen weergegeven als Geavanceerde bankafstemming is ingeschakeld voor de bankrekening.

### <a name="balance"></a>Balans

Het diagram **Saldo** toont historische saldogegevens voor de bankrekening die is geselecteerd in de sectie **Bankrekeningen** of een overzicht van historische saldogegevens voor alle bankrekeningen in de rechtspersoon. Deze informatie is beschikbaar voor verschillende perioden: de huidige week, de huidige maand, het huidige jaar, de laatste vijf jaar en alle perioden (de volledige historie van de bankrekening). 

Als u het diagram **Saldo** bekijkt voor één bankrekening, worden de historische saldi weergegeven in de bankrekeningvaluta. Als u het diagram bekijkt voor alle bankrekeningen in de rechtspersoon, worden de historische saldi weergegeven in de valuta voor boekhouding.

Informatie over wanneer de gegevens voor het laatst zijn bijgewerkt, vindt u boven aan het diagram. U kunt de gegevens desgewenst bijwerken.

### <a name="related-information"></a>Verwante informatie

In de sectie **Verwante informatie** kunt u de pagina **Algemeen journaal** openen om bankoverschrijvingen te voltooien. U kunt ook de pagina´s **Banktransacties** en **Overbruggingstransacties** snel openen.

## <a name="analytics-view"></a>Analyseweergave

De pagina **Analyses** bevat belangrijke metrische gegevens over de bankrekeningen in het huidige bedrijf. De volgende visualisaties zijn beschikbaar op de pagina:

-   Totaal banksaldo in systeemvaluta
-   Saldo per rechtspersoon
-   Werkelijk versus voorspeld saldo van vandaag in valuta van de bankrekening
-   Saldo per bankrekening
-   Saldo per valuta

U kunt bankanalyses bekijken voor alle bedrijven in het werkgebied **Overzicht van contant geld - alle bedrijven**.

