---
title: Beleid voor retouren en restituties voor een afzetkanaal maken en bijwerken
description: In dit artikel wordt uitgelegd hoe u een retour- en restitutiebeleid instelt voor een kanaal.
author: ShalabhjainMSFT
ms.date: 07/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.custom: ''
ms.search.industry: Retail
ms.openlocfilehash: b93852bfb7c6f5a9f2f83f30a1f76da3f9559c7e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286832"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a>Beleid voor retouren en restituties voor een afzetkanaal maken en bijwerken

[!include [banner](includes/banner.md)]

Via het kanaalretourbeleid in Dynamics 365 Commerce kunnen detailhandelaren voorwaarden instellen voor het toestaan van betalingsmethoden voor het verwerken van een retour op een POS-apparaat (Point of Sale).  

In dit artikel worden de stappen beschreven voor het instellen van een retour- en restitutiebeleid voor een kanaal.

De reikwijdte van het beleid is momenteel beperkt tot het instellen van de betalingsmethoden die kunnen worden toegestaan voor een kanaal. De lijst 'toegestaan' is gebaseerd op de betalingsmethoden die zijn gebruikt voor het doen van de aankoop. Bijvoorbeeld:

- Als er een aankoop heeft plaatsgevonden met een geschenkbon, is het winkelbeleid dat alleen restitutie kan plaatsvinden via een nieuwe geschenkbon of dat winkelkrediet wordt verleend. 
- Als een verkoop wordt gedaan met contant geld, zijn de opties voor terugbetaling contant, geschenkbon en klantrekening, maar niet creditcard. 

## <a name="enable-return-policy"></a>Retourbeleid inschakelen

Voer de volgende stappen uit om de functionaliteit voor kanaalretourbeleid in te schakelen in Commerce Headquarters.

1. Ga naar het werkgebied **Functiebeheer** in Dynamics 365 Commerce.
1. Zoek naar de functie **Kanaalretourbeleid inschakelen** in de lijst met functienamen.
1. Selecteer **Nu inschakelen**.
1. Voer op de pagina **Distributieplanning** de taak **1110** (Algemene configuratie) uit om de functiewijziging te verdelen.

## <a name="configure-return-policy"></a>Retourbeleid configureren

Voer de volgende stappen uit om een retourbeleid te configureren voor een detailhandelwinkel of online detailhandelkanaal.

1. Ga naar **Retail en Commerce** \> **Kanaalinstelling** \> **Retouren** \> **Kanaalretourbeleid**.

1. Selecteer **Nieuw** om een nieuwe sjabloon voor retourbeleid te maken. Als u een bestaande sjabloon wilt gebruiken, selecteert u de sjabloon in het linkerdeelvenster. Voor nieuwe sjablonen voegt u een naam en een beschrijving toe aan de hand waarvan u het beleid kunt identificeren wanneer dit op het kanaal wordt toegepast.

   ![Nieuw retourbeleid toevoegen.](media/Return-policy-page1.png)
     
   
1. Definieer in de sectie **Toegestane betalingsmethoden voor restitutie** de optie **Toegestaan** voor betalingsmethoden voor retourbetalingen die specifiek zijn voor elke betalingsmethode.
   ![Toegestane betalingsmethoden per betalingstype instellen.](media/Return-policy-page2.png)
   
    > [!IMPORTANT]
    > - De betalingsmethoden worden afgeleid van de betalingsmethoden die zijn ingesteld voor de organisatie.
    > - Door een toegestane betalingsmethode voor restitutie toe te voegen voor elke vermelde betalingsmethode, zorgt u ervoor dat er restitutie kan plaatsvinden naar de toegestane type retourbetalingsmethode.
    
1. Koppel de sjabloon voor retourbeleid aan de winkels waar deze wordt gebruikt. Selecteer **Toevoegen** op het tabblad **Detailhandelkanalen** en koppel de beschikbare kanalen. 

    - Selecteer in het dialoogvenster **Organisatieknooppunten kiezen** de winkels, regio's en organisaties waaraan de sjabloon moet worden gekoppeld.
    - Er kan slechts één sjabloon voor retourbeleid aan elke winkel worden gekoppeld.
    - Gebruik de pijlknoppen om winkels, regio's of organisaties te selecteren.
    - De ingangsdatum van het beleid is de datum waarop het beleid op de kanalen wordt toegepast en de kanaaltaken worden uitgevoerd. 

    ![Dialoogvenster Organisatieknooppunten kiezen.](media/Return-policy-page3.png)

1. Voer op de pagina **Distributieschema** de taak **1070** uit om het kanaalretourbeleid beschikbaar te maken voor het POS.

## <a name="preview-the-channel-return-policy-in-the-pos"></a>Een voorbeeld van het kanaalretourbeleid bekijken in het POS

Volg de stappen in een van de volgende voorbeelden om de toegestane typen retourbetalingsmethoden in POS weer te geven.

1. Meld u als kassier of manager aan bij het POS.
1. Selecteer onder **Ploeg en lade** de optie **Journaal weergeven**.
1. Selecteer de transactie die deel uitmaakt van de retour. 
1. Selecteer de artikelen die u wilt terugbetalen en kies de betalingsmethode.  
    - Als de geselecteerde betalingsmethode in de lijst met toegestane typen betalingsmethoden voorkomt, kan de kassier de transactie voltooien.
    - Als de geselecteerde betalingsmethode niet is toegestaan, wordt een foutbericht weergegeven.
    - Selecteer **Verschuldigd bedrag** om een lijst weer te geven met alle toegestane typen betalingsmethoden voor retouren.

– of –

1. Meld u als kassier of manager aan bij het POS.
1. Selecteer **Retourtransactie** en voer de ontvangst-id in met behulp van een streepjescodescan of handmatige invoer. 
1. Selecteer de transactie die deel uitmaakt van de retour. 
1. Selecteer de artikelen die u wilt terugbetalen en kies de betalingsmethode.  
    - Als de geselecteerde betalingsmethode in de lijst met toegestane typen betalingsmethoden voorkomt, kan de kassier de transactie voltooien.
    - Als de geselecteerde betalingsmethode niet is toegestaan, wordt een foutbericht weergegeven.
    - Selecteer **Verschuldigd bedrag** om een lijst weer te geven met alle toegestane typen betalingsmethoden voor retouren.

![Type restitutie niet toegestaan.](media/Return-policy-page6.png)



![Typen restitutie toegestaan.](media/Return-policy-page5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
