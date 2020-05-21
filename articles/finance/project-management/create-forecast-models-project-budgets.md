---
title: Prognosemodellen voor projectbudgetten maken
description: In dit onderwerp wordt beschreven hoe u een prognosemodel maakt voor resterende budgetten.
author: RadhikaRS
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 07e540f23a668b40a54906a67d87552fe991825a
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321774"
---
# <a name="create-forecast-models-for-project-budgets"></a>Prognosemodellen voor projectbudgetten maken 

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een prognosemodel maakt voor resterende budgetten. Een project dat onderworpen is aan budgetbeheer gebruikt twee budgettypen: oorspronkelijk en resterend. Wanneer u een projectbudget maakt, moet u de gemaakte oorspronkelijke en de resterende budgetprognosemodellen opgeven in de pagina **Prognosemodellen**. Projectbudgetten die op de opgegeven modellen zijn gebaseerd, worden gemaakt wanneer u het projectbudget toezegt.

> [!NOTE]
> Een prognosemodel dat wordt gebruikt voor budgetbeheer kan geen submodel hebben of kan niet als submodel worden gebruikt.

1. Selecteer **Projectbeheer en boekhouding** > **Instellingen** > **Prognoses**  > **Prognosemodellen**.
2. Selecteer **Nieuw** om een nieuw prognosemodel te maken en voer vervolgens een model-id-nummer en een naam in voor het nieuwe model. 
3. Stel de optie **Gestopt** in op **Ja** om wijzigingen in de prognoseregels voor het prognosemodel te voorkomen. 
4. Als de prognoseregels waaraan het model is gekoppeld cashflowprognoses in het grootboek moeten genereren, stelt u **Opnemen in cashflowprognoses** in op **Ja**. 
5. Als u de projectdatum wilt gebruiken als de factuurdatum, stelt u **Prognose factuurdatum** in op **Ja**. 
6. Selecteer in het veld **Budgettype** een van de volgende modeltypen:

   - **Oorspronkelijk budget**: gebruik de oorspronkelijke budgetbedragen die zijn toegezegd wanneer het eerste budget is gemaakt en goedgekeurd.
   - **Resterend budget**: gebruik de resterende budgetbedragen tijdens de levensduur van het project. De saldi in dit prognosemodel worden verminderd door effectieve transacties en verhoogd of verlaagd door budgetrevisies.
   - **Transporteren**: gebruik de overgeboekte budgetbedragen voor het project. Transporteren is een optioneel proces dat kan worden uitgevoerd om ongebruikte budgetbedragen van het ene fiscaal jaar naar het andere over te boeken.

7. Stel de volgende opties in zoals vereist:

   - Als u de projectdatum wilt gebruiken als de factuurdatum, schakelt u **Prognose factuurdatum** in.
   - Schakel **Prognose met OHW** in voor prognoses op basis van onderhanden werk (OHW) en selecteer vervolgens het type OHW. 
   - U kunt het standaard **Budgettype** **Geen** behouden of een nieuw type invoeren. Het budgettype kan niet worden gewijzigd nadat u een record hebt gewijzigd.     
    > [!NOTE]
    > Als u het standaard budgettype wijzigt, worden alle andere opties niet beschikbaar voor updates en kunt u dit prognosemodel niet opnieuw gebruiken. 
   


 

