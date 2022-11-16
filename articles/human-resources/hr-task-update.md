---
title: Taken instellen in Taakbeheer
description: In dit artikel wordt uitgelegd hoe u taken instelt in Taakbeheer in Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2022-06-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6a38cc2e36c24ddbfe0d8b2886301c108599ab25
ms.sourcegitcommit: 55e440e30490b2d36d86b22aa1263d5da97633aa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/04/2022
ms.locfileid: "9745384"
---
# <a name="set-up-tasks-in-task-management"></a>Taken instellen in Taakbeheer

[!INCLUDE [PEAP](../includes/peap-1.md)]

In versies van Microsoft Dynamics 365 Human Resources vóór versie 10.0.30 moesten gebruikers die een taak wilden bewerken die taak in elke afzonderlijke controlelijst bewerken. Vanaf Human Resources-versie 10.0.30 kunnen gebruikers echter selecteren hoe bewerkte taken worden verwerkt. Als een taak die wordt bewerkt in een controlelijst is opgenomen, moet de optie **Upgrade voor taakbeheer inschakelen** worden geselecteerd op het tabblad **Taakbeheer** van de pagina **Gedeelde Human resources-parameters** om in te stellen dat de controlelijst de bewerkte taak kan gebruiken.

[![De optie Upgrade voor taakbeheer inschakelen op de pagina Gedeelde Human resources-parameters.](./media/task-update.png)](./media/task-update.png)

Als bewerkingen van taken moeten worden toegepast voor alle gekoppelde controlelijsttaken, moet er al een relatie bestaan tussen de taak in de taakbibliotheek en de taak in de controlelijst. Er is een optie toegevoegd om de relatie tussen de bibliotheektaak en de controlelijsttaak te maken.

U kunt taken afzonderlijk maken en deze vervolgens opnieuw gebruiken in meerdere controlelijsten. Als u een taak wilt maken, selecteert u op de pagina **Instellingen voor aannemen** op het tabblad **Taken** de optie **Nieuw**.

## <a name="set-up-tasks"></a>Taken instellen

U kunt een gemaakte taak aan meerdere controlelijsten toewijzen door de taak te selecteren en vervolgens **Toepassen op controlelijsten** in het menu te selecteren.

U kunt ook taken rechtstreeks aan een controlelijst toevoegen. Als u een taak wilt toevoegen aan een controlelijst, maakt u op de pagina **Instellingen voor onboarding** op het tabblad **Controlelijst** een nieuwe controlelijst waaraan u de taak toevoegt of voegt u de taak aan een bestaande controlelijst toe.

Als u een bibliotheektaak wilt bewerken, selecteert u **Bewerken** in het menu Taakbibliotheek. Als de taak is gekoppeld aan controlelijsten, worden deze controlelijsten weergegeven op de pagina **Taak bewerken**. Als u wilt dat de taken in controlelijsten worden bijgewerkt met de bewerkingen, selecteert u die controlelijsten in de sectie **Controlelijsten toepassen**.

Als u taken uit de taakbibliotheek wilt verwijderen, selecteert u de optie **Verwijderen**. Als de taak is gekoppeld aan een controlelijst, wordt met deze actie de taak niet uit de controlelijst verwijderd. Een afzonderlijke actie is nodig om een taak uit een controlelijst te verwijderen.

### <a name="set-up-checklists"></a>Controlelijsten instellen

Een controlelijst is een groep taken. U kunt zoveel controlelijsten maken als u nodig hebt en u kunt dezelfde taken aan meerdere controlelijsten toewijzen. Wanneer u een controlelijst maakt, geeft u een eigenaar en een kalender op.

Als u een nieuwe taak in een controlelijst wilt maken, selecteert u **Nieuw** op de menubalk Taken. Wanneer u een nieuwe taak maakt, kunt u ervoor kiezen deze toe te voegen aan de taakbibliotheek, zodat deze kan worden gedeeld met meerdere controlelijsten. Als u de taak aan de bibliotheek wilt toevoegen, moet u de optie **Taak toepassen op bibliotheek** instellen op **Ja**. Als u de taak aan de taakbibliotheek toevoegt, kunt u de taak tegelijk ook aan andere controlelijsten toevoegen door die controlelijsten te selecteren in de sectie **Controlelijsten toepassen**. Als u de taak niet toevoegt aan de taakbibliotheek, staat deze alleen in de controlelijst waarin u deze maakt.

Als u een taak in een controlelijst wilt bewerken, selecteert u **Bewerken** in het taakmenu. Als de taak is gekoppeld aan controlelijsten, worden deze controlelijsten weergegeven op de pagina **Taak bewerken**. Als u wilt dat de taken in andere controlelijsten worden bijgewerkt met de bewerkingen, selecteert u die controlelijsten in de sectie **Controlelijsten toepassen**.

Als u taken uit een controlelijst wilt verwijderen, selecteert u **Verwijderen**. Met deze actie worden de taken uit de controlelijst verwijderd. Ze worden niet uit de taakbibliotheek verwijderd. Als u taken uit de taakbibliotheek wilt verwijderen, gaat u naar de pagina **Taakbibliotheek** en selecteert u **Verwijderen**.
