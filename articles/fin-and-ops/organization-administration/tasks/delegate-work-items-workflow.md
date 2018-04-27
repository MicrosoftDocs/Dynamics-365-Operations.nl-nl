--- 
title: Werkitems in een workflow delegeren
description: Als u gedurende niet op kantoor aanwezig zult zijn of als u niet beschikbaar bent om werkitems op te volgen, kunt u uw werkitems aan andere gebruikers delegeren of toewijzen.
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 4765fec0cdce0e2f8859c979ff97d20aa6b20bfa
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="delegate-work-items-in-a-workflow"></a>Werkitems in een workflow delegeren

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Als u gedurende niet op kantoor aanwezig zult zijn of als u niet beschikbaar bent om werkitems op te volgen, kunt u uw werkitems aan andere gebruikers delegeren of toewijzen. Door middel van deze procedure kunt u het systeem zo configureren dat uw werkitems automatisch aan een andere gebruiker worden gedelegeerd.



Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.


## <a name="set-up-automatic-delegation"></a>Automatisch delegeren instellen
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


