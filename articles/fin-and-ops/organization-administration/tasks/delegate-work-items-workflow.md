---
title: Werkitems in een workflow delegeren
description: Als u gedurende niet op kantoor aanwezig zult zijn of als u niet beschikbaar bent om werkitems op te volgen, kunt u uw werkitems aan andere gebruikers delegeren of toewijzen.
author: jasongre
manager: AnnBe
ms.date: 04/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: feace647d7acef6abf86b13fcb8019c622c55ff6
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509447"
---
# <a name="delegate-work-items-in-a-workflow"></a>Werkitems in een workflow delegeren

[!include [task guide banner](../../includes/task-guide-banner.md)]

## <a name="manually-delegate-a-work-item"></a>Een werkitem handmatig delegeren

Als u een afzonderlijk werkitem wilt delegeren, selecteert u de optie **Delegeren** in het menu **Workflow** en voert u vervolgens de gebruiker in die moet worden gedelegeerd samen met een opmerking. Hiermee wordt het werkitem aan die gebruiker opnieuw toegewezen zodat het kan worden voltooid.

## <a name="automatically-delegate-work-items"></a>Werkitems automatisch delegeren

Als u van plan bent om buiten kantoor te zijn of anderszins niet beschikbaar bent om aan werkitems te werken voor een bepaalde periode, kunt u nieuwe werkitems automatisch delegeren aan andere gebruikers met de pagina **Gebruikersopties**.

### <a name="set-up-automatic-delegation"></a>Automatisch delegeren instellen
1. Ga naar de Algemeen > Instellingen > Gebruikersopties.
2. Klik op het tabblad Workflow.
    * Controleer of de sectie Delegatie is uitgevouwen.    Om het systeem te configureren om uw werkitems automatisch te delegeren aan andere gebruikers, moet u delegatieregels maken die opgeven wanneer bepaalde typen werkitems worden gedelegeerd. Volg deze stappen om een delegatieregel te maken.  
3. Klik op Toevoegen.
4. Selecteer een optie in het veld Bereik.
    * Alle – Alle taken of werkitems delegeren die aan u zijn toegewezen.    Module: alleen de werkitems delegeren die verband houden met een specifiek workflowtype. Als u deze optie selecteert, moet u het workflowtype selecteren in het veld Naam.    Workflow: alleen de werkitems delegeren die verband houden met een specifieke workflow. Als u deze optie selecteert, moet u de workflow selecteren het veld Naam.  
5. Selecteer in het veld Delegeren de gebruiker aan wie u werkitems wilt delegeren.
    * Met de velden Begindatum/-tijd en Einddatum/-tijd geeft u op wanneer de werkitems automatisch moeten worden gedelegeerd.  
6. Typ in het veld Begindatum/-tijd de datum en een tijd.
7. Typ in het veld Einddatum de datum en een tijd.
8. Schakel het selectievakje Ingeschakeld in om de machtigingsregel te activeren.
    * Als u onder Bereik de waarde Module hebt geselecteerd, moet u de module selecteren in het veld Naam.    Als u onder Bereik de waarde Workflow hebt geselecteerd, moet u de in het veld Naam de workflow selecteren die u wilt delegeren.  
9. Voer in het veld Opmerking tekst in waaruit uw reden voor het delegeren van de werkitems blijkt.

