---
title: Een budget maken op basis van transactierekeningen en totaalrekeningen.
description: Dit artikel biedt een overzicht van het proces voor het maken van budgetten op basis van totaalrekeningen. Daarnaast wordt beschreven hoe u budgetbeheer voor totaalrekeningen inschakelt, als budgetbeheer vereist is.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6129a5431cba22ea656e4d6f473a4e93a81131ea
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "331708"
---
# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a>Een budget maken op basis van transactierekeningen en totaalrekeningen.

[!include [banner](../includes/banner.md)]

Dit artikel biedt een overzicht van het proces voor het maken van budgetten op basis van totaalrekeningen. Daarnaast wordt beschreven hoe u budgetbeheer voor totaalrekeningen inschakelt, als budgetbeheer vereist is.

Zowel met budgetplan- als budgetregisterinvoerdocumenten is budgettering voor hoofdrekeningen mogelijk die het hoofdrekeningtype **Totaal** hebben. Werkelijke kosten kunnen alleen naar transactiehoofdrekeningen worden geboekt. 

Voor het periodieke proces **Budgetplan genereren op basis van grootboek** op het tabblad **Bron** kunt u het hoofdrekeningtype **Totaal** als criterium opgeven. In dit geval wordt elke totale hoofdrekening opgenomen in het doelbudgetplan en is het bedrag gelijk aan het totaalbedrag van het bereik van geselecteerde hoofdrekeningen. 

U kunt budgetbeheer voor hoofdrekeningen van het type **Totaal** activeren. Deze functionaliteit wordt ondersteund via het gebruik van budgetgroepen. Voor elke totale hoofdrekening moet het budget dat moet worden beheerd voor een budgetgroep, worden gemaakt op de pagina **Budgetbeheerconfiguratie**. De criteria die u opgeeft, moeten de totale hoofdrekening en het bereik van rekeningen bevatten. Om het proces voor het maken van budgetgroepen te versnellen, kunt u profiteren van de gegevensentiteit van budgetbeheergroepen. 

Wanneer een budget wordt gebruikt bij rapportage, zoals in een financieel overzicht, bestaat de som van het budget voor de totaalrekening uit de volgende bedragen:

-   De budgetten die op elke transactiegrootboekrekening binnen het interval van de totaalrekening zijn gemaakt.
-   Het budgetbedrag dat direct op de totaalrekening is ingevoerd.

Zo kunt u afzonderlijke budgetten voor de belangrijkste transactierekeningen binnen het interval van de totaalrekening maken en het beschikbare budgetbedrag vervolgens toevoegen aan de totaalrekening.



