---
title: Werkitems in een workflow delegeren
description: Als u gedurende niet op kantoor aanwezig zult zijn of als u niet beschikbaar bent om werkitems op te volgen, kunt u uw werkitems aan andere gebruikers delegeren of toewijzen.
author: ChrisGarty
ms.date: 07/07/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed21f6d32cdcf74eb153daba32c20b7cef94d4e4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747364"
---
# <a name="delegate-work-items-in-a-workflow"></a>Werkitems in een workflow delegeren

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a>Een werkitem handmatig delegeren

Als u een afzonderlijk werkitem wilt delegeren, selecteert u de optie **Delegeren** in het menu **Workflow** en voert u vervolgens de gebruiker in die moet worden gedelegeerd samen met een opmerking. Hiermee wordt het werkitem aan die gebruiker opnieuw toegewezen zodat het kan worden voltooid.

## <a name="manually-delegate-multiple-work-items"></a>Meerdere werkitems handmatig delegeren

U kunt meerdere werkitems delegeren via de pagina **Aan mij toegewezen werkitems**. De volgende werkstroomtypen komen in aanmerking voor bulkdelegering: Goedkeuringswerkstroom inkoopovereenkomst, Inkooporderwerkstroom, Controle inkoopbestelopdracht en Leveranciersfactuurwerkstroom. De functie **Meerdere werkitems delegeren** is standaard uitgeschakeld en kan worden ingeschakeld in **Werkruimten > Functiebeheer**. Neem contact op met uw systeembeheerder voor hulp bij het inschakelen van deze functie.
1.  Naar **Algemeen > Algemeen > Werkitems > Aan mij toegewezen werkitems**.
2.  Selecteer de werkitems die u wilt delegeren.
3.  Klik op het menu **Werkitems delegeren**.
4.  Selecteer in het veld **Gebruiker** de gebruiker aan wie u werkitems wilt delegeren.
5.  Voer in het veld **Opmerking** tekst in met uw reden voor het delegeren van de werkitems.
6.  Klik op de knop **Werkitems delegeren** om het delegeren van het werkitem te voltooien.

## <a name="automatically-delegate-work-items"></a>Werkitems automatisch delegeren

Als u van plan bent om buiten kantoor te zijn of anderszins niet beschikbaar bent om aan werkitems te werken voor een bepaalde periode, kunt u nieuwe werkitems automatisch delegeren aan andere gebruikers met de pagina **Gebruikersopties**.

### <a name="set-up-automatic-delegation"></a>Automatisch delegeren instellen
1. Ga naar **Algemeen > Instellingen > Gebruikersopties**.
2. Klik op het tabblad **Workflow**. Controleer of de sectie Delegatie is uitgevouwen. Om het systeem te configureren om uw werkitems automatisch te delegeren aan andere gebruikers, moet u delegatieregels maken die opgeven wanneer bepaalde typen werkitems worden gedelegeerd. Volg deze stappen om een delegatieregel te maken.  
3. Klik op **Toevoegen**.
4. Selecteer een optie in het veld **Bereik**:
    - Alle – Alle taken of werkitems delegeren die aan u zijn toegewezen.
    - Module: alleen de werkitems delegeren die verband houden met een specifiek workflowtype. Als u deze optie selecteert, moet u het workflowtype selecteren in het veld **Naam**.
    - Workflow: alleen de werkitems delegeren die verband houden met een specifieke workflow. Als u deze optie selecteert, moet u de workflow selecteren het veld **Naam**.  
5. Vul het veld **Naam** in:
    - Selecteer de doelmodule voor het **Module** bereik.
    - Selecteer de doelwerkstroom voor het **Werkstroom** bereik.
6. Selecteer in het veld **Delegeren** de gebruiker aan wie u werkitems wilt delegeren. Met de velden **Begindatum/-tijd** en **Einddatum/-tijd** geeft u op wanneer de werkitems automatisch moeten worden gedelegeerd.  
7. Typ in het veld **Begindatum/-tijd** de datum en een tijd.
8. Typ in het veld **Einddatum** de datum en een tijd.
9. Schakel het selectievakje **Ingeschakeld** in om de machtigingsregel te activeren. 
10. Voer in het veld **Opmerking** tekst in met uw reden voor het delegeren van de werkitems.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]