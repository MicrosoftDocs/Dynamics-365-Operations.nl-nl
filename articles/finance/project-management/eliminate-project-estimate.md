---
title: Een projectraming elimineren
description: Dit onderwerp bevat informatie over het verwijderen van een projectraming nadat deze is voltooid.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: eb323bdeb2a4701cdc9383b8da29e05a4cab107c
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410206"
---
# <a name="eliminate-a-project-estimate"></a>Een projectraming elimineren

[!include [banner](../includes/banner.md)]

Projectramingen bieden de financiële weergave voor werk dat is geraamd en gepland voor een project. Indien u voor een project met ramingen wilt werken, moet u het project aan een ramingsproject koppelen. Een ramingsproject is altijd gebaseerd op een bestaand project, maar meerdere projecten kunnen verwijzen naar één ramingsproject. Alleen projecten met een vaste prijs en investeringsprojecten kunnen aan ramingsprojecten worden gekoppeld, en deze projecten moeten bij dezelfde projectgroep als het ramingsproject horen.

Als u een ramingsproject wilt schrappen, moet het voltooid zijn. In de volgende stappen wordt uitgelegd hoe u een raming kunt verwijderen.

1. Ga naar **Projectbeheer en boekhouding** > **Alle projecten** en open het project. 
2. Selecteer op het tabblad **Beheren** de optie **Ramingen** en selecteer op de pagina **Raming** de optie **Schrappen**.
3. Stel op de pagina **Raming schrappen** op het tabblad **Algemeen** de volgende opties in:

   - **Periodecode**: de periodecode selecteren om de juiste ramingsprojecten te kiezen. 
   - **Ramingsdatum**: de juiste ramingsdatum voor schrapping selecteren.
   - **Elimineren met OHW-waarschuwingen**: schakel deze optie in als u een melding wilt weergeven wanneer een raming wordt geschrapt die is gekoppeld aan onderhanden werk (OHW). Wanneer deze optie niet is ingeschakeld, kan de raming niet worden geschrapt wanneer er niet-geraamde transacties bestaan. 
   > [!NOTE]
   > Deze optie is alleen beschikbaar als schrapping wordt toegepast op een ramingsproject. Dit veld is niet beschikbaar als u periodieke boekingen gebruikt. Deze instelling werkt met de instellingen op het tabblad **Raming** op de pagina **Projectparameters** en in de veldengroep **Schrapping toestaan als niet-geraamde transacties bestaan**.
   - **Fase instellen op Gereed**: schakel deze optie in om de fase van het ramingsproject in te stellen op **Gereed** nadat u de schrapping hebt uitgevoerd.
   - **Ramingslijst afdrukken**: de gegevens selecteren die u wilt opnemen wanneer de ramingslijst wordt afgedrukt.
   - **Infologboek weergeven**: schakel deze optie in om het infologboek weer te geven.
   - **Boekingsdatum**: kies de grootboekboekingsdatum van de raming.

4.  Selecteer **OK**.
5. Nadat het schrappingsproces is voltooid, wordt het geschrapte ramingsproject weergegeven met een negatieve waarde. 

Als u niet van plan bent om een raming te schrappen, kunt u de geschrapte raming selecteren en **Schrapping omkeren**.   
