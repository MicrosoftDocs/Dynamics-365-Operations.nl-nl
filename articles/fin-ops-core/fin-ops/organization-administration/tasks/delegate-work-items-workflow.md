---
title: Werkitems in een workflow delegeren
description: Als u gedurende niet op kantoor aanwezig zult zijn of als u niet beschikbaar bent om werkitems op te volgen, kunt u uw werkitems aan andere gebruikers delegeren of toewijzen.
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
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
ms.openlocfilehash: aceafbe8dfcdac2ac7b97a4f77a9a30599c60c51
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140577"
---
# <a name="delegate-work-items-in-a-workflow"></a>Werkitems in een workflow delegeren

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a>Een werkitem handmatig delegeren

Als u een afzonderlijk werkitem wilt delegeren, selecteert u de optie **Delegeren** in het menu **Workflow** en voert u vervolgens de gebruiker in die moet worden gedelegeerd samen met een opmerking. Hiermee wordt het werkitem aan die gebruiker opnieuw toegewezen zodat het kan worden voltooid.

## <a name="automatically-delegate-work-items"></a>Werkitems automatisch delegeren

Als u van plan bent om buiten kantoor te zijn of anderszins niet beschikbaar bent om aan werkitems te werken voor een bepaalde periode, kunt u nieuwe werkitems automatisch delegeren aan andere gebruikers met de pagina **Gebruikersopties**.

### <a name="set-up-automatic-delegation"></a>Automatisch delegeren instellen
1. Ga naar **Algemeen > Instellingen > Gebruikersopties**.
2. Klik op het tabblad **Workflow**. Controleer of de sectie Delegatie is uitgevouwen. Om het systeem te configureren om uw werkitems automatisch te delegeren aan andere gebruikers, moet u delegatieregels maken die opgeven wanneer bepaalde typen werkitems worden gedelegeerd. Volg deze stappen om een delegatieregel te maken.  
3. Klik op **Toevoegen**.
4. Selecteer een optie in het veld **Bereik**.
    - Alle – Alle taken of werkitems delegeren die aan u zijn toegewezen.
    - Module: alleen de werkitems delegeren die verband houden met een specifiek workflowtype. Als u deze optie selecteert, moet u het workflowtype selecteren in het veld Naam.
    - Workflow: alleen de werkitems delegeren die verband houden met een specifieke workflow. Als u deze optie selecteert, moet u de workflow selecteren het veld Naam.  
5. Selecteer in het veld **Delegeren** de gebruiker aan wie u werkitems wilt delegeren. Met de velden Begindatum/-tijd en Einddatum/-tijd geeft u op wanneer de werkitems automatisch moeten worden gedelegeerd.  
6. Typ in het veld **Begindatum/-tijd** de datum en een tijd.
7. Typ in het veld **Einddatum** de datum en een tijd.
8. Schakel het selectievakje **Ingeschakeld** in om de machtigingsregel te activeren. Als u onder Bereik de waarde **Module** hebt geselecteerd, moet u de module selecteren in het veld Naam. Als u onder Bereik de waarde **Workflow** hebt geselecteerd, moet u in het veld Naam de workflow selecteren die u wilt delegeren.  
9. Voer in het veld **Opmerking** tekst in waaruit uw reden voor het delegeren van de werkitems blijkt.

