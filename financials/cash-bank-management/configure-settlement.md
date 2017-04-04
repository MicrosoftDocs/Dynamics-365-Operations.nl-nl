---
title: Vereffening configureren
description: "Hoe en wanneer de transacties worden vereffend, kunnen complexe onderwerpen zijn. Daarom is het belangrijk dat u parameters begrijpt en de parameters kunt definiëren om aan uw bedrijfsbehoeften te voldoen. In dit artikel worden de parameters beschreven die voor Leveranciers en Klanten worden gebruikt voor vereffening."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, CustParameters, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14601
ms.assetid: 6b61e08c-aa8b-40c0-b904-9bca4e8096e7
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 6927ed98c82f174a18d3d8821fbdb302801835c4
ms.lasthandoff: 03/31/2017


---

# <a name="configure-settlement"></a>Vereffening configureren

Hoe en wanneer de transacties worden vereffend, kunnen complexe onderwerpen zijn. Daarom is het belangrijk dat u parameters begrijpt en de parameters kunt definiëren om aan uw bedrijfsbehoeften te voldoen. In dit artikel worden de parameters beschreven die voor Leveranciers en Klanten worden gebruikt voor vereffening. 

De volgende parameters invloed op hoe vereffeningen worden verwerkt in Microsoft Dynamics 365 voor bewerkingen. Vereffening is het proces van het vereffenen van een factuur met een betaling of creditnota. Deze parameters bevinden zich in het gebied **Vereffening** van de pagina´s **Parameters van module Klanten** en **Parameters van module Leveranciers** .

-   **Automatische vereffening**: stel deze optie in op **Ja** als een transactie automatisch met andere openstaande transacties moet worden vereffend wanneer deze wordt geboekt. Als deze optie is ingesteld op **Nee**, kunnen gebruikers transacties handmatig vereffenen wanneer ze betalingen invoeren, of later met behulp van de pagina **Transacties vereffenen**.
-   **Administratie voor contantkorting** : opgeven hoe een [korting voor contante betaling wordt uitgevoerd wanneer een factuur te veel is betaald](cash-discount-handling-overpayments.md). Voor een overbetaling, wordt de korting voor contante betaling kan worden verminderd, deze kan worden beschouwd als een verschil of op rekening voor de leverancier of klant kunnen blijven staan.
    -   **Flexibel**: het bedrag van de contantkorting wordt verminderd met het bedrag van de overbetaling. Dit gedrag wordt altijd gebruikt, ongeacht of het overbetalingsbedrag meer of minder is dan het bedrag dat is in gevoerd in het veld **Max. te veel/te weinig betaald bedrag**.
    -   **Specifiek**: het overbetalingsbedrag wordt geboekt naar een grootboekrekening voor contantkortingsverschillen of het blijft een saldo op de rekening van de klant of de leverancier. Het specifieke gedrag is afhankelijk van de vraag of het overbetalingsbedrag tussen 0,00 en het bedrag dat in het veld **Max. te veel/te weinig betaald bedrag** is, of dat het overbetalingsbedrag meer is dan het bedrag van **Max. te veel/te weinig betaald bedrag**.
-   **Maximale afronding**: voer de maximaal toegestane afronding voor de vereffende transacties in. Als het verschil gelijk is aan of kleiner is dan het afrondingsverschil dat in dit veld is opgegeven, wordt het verschil geboekt naar de grootboekrekening voor afrondingsverschillen, die is opgegeven op de pagina **Rekeningen voor automatische transacties**.
-   **Max. te veel/te weinig betaald bedrag**: voer het bedrag in dat is geaccepteerd voor over- en onderbetaling. Als u de btw voor te veel of te weinig betaalde bedragen wilt berekenen, moet u klikken op **Btw** op de pagina **Grootboekparameters** en vervolgens de optie **Btw op te veel/te weinig betaald bedrag** selecteren.
    -   Als er door een te veel of een te weinig betaald bedrag een afronding ontstaat die kleiner is dan het verschil dat in het veld **Maximale afronding** is opgegeven, wordt het afrondingsbedrag naar de afrondingsrekening geboekt.
    -   Als er door een te veel of een te weinig betaald bedrag een afronding ontstaat die groter is dan het verschil dat in het veld **Maximale afronding** is opgegeven, wordt het afrondingsbedrag geboekt naar de verschilrekening die is geselecteerd voor het boekingstype **Contantkorting van klant** of **Contantkorting van leverancier** op de pagina **Rekeningen voor automatische transacties**.
-   **Contantkortingen berekenen voor gedeeltelijke betalingen**: stel deze optie in op **Ja** zodat contantkortingen automatisch kunnen worden berekend voor gedeeltelijke betalingen.
    -   Dit effect van deze optie is afhankelijk van de waarde van het veld **Contantkorting gebruiken** op de pagina **Transacties vereffenen**. Als deze optie is ingesteld op **Ja**, wordt de korting genomen als het veld **Contantkorting gebruiken** is ingesteld op **Normaal**. Wanneer het veld **Contantkorting gebruiken** is ingesteld op **Altijd**, wordt de contantkorting altijd toegepast, ongeacht de instelling van dit veld. Wanneer het veld **Contantkorting gebruiken** is ingesteld op **Nooit**, wordt de contantkorting nooit toegepast, ongeacht de instelling van dit veld.
    -   Als deze optie is ingesteld op **Ja** en een gebruiker wijzigt de waarde in het veld **Te vereffenen bedrag** op de pagina **Transacties vereffenen**, wordt de korting automatisch berekend en weergegeven als de standaardinvoer in het veld **Contantkortingsbedrag dat moet worden toegepast**.
    -   Als deze optie is ingesteld op **Nee** en een gebruiker wijzigt de waarde in het veld **Te vereffenen bedrag** op de pagina **Transacties vereffenen**, is de standaardinvoer in het veld **Contantkortingsbedrag dat moet worden toegepast** **0** (nul).
-   **Contantkortingen berekenen voor creditnota's**: stel deze optie in op **Ja** om automatisch een contantkorting voor creditnota's te berekenen. In Klanten is een creditnotatransactie een negatieve transactie met een waarde in het veld **Factuur** op de pagina **Vrije-tekstfactuur** of een retour op de pagina **Verkooporder**.
    -   Het effect van deze optie is afhankelijk van de waarde van het veld **Contantkorting gebruiken** op de pagina **Transacties vereffenen**. Als deze optie is ingesteld op **Ja**, wordt de korting berekend wanneer de *** gebruik contantkorting *** veld is ingesteld op **normaal**. Wanneer de *** gebruik contantkorting *** veld is ingesteld op **altijd**, de contantkorting altijd genomen, ongeacht de instelling van dit veld. Wanneer de *** gebruik contantkorting *** veld is ingesteld op **nooit**, de contantkorting nooit genomen, ongeacht de instelling van dit veld.
    -   Als deze optie is in gesteld op **Ja** en een creditnota wordt gemarkeerd op de pagina **Transacties vereffenen**, wordt de korting automatisch berekend en weergegeven als de standaardinvoer in het veld **Contantkortingsbedrag dat moet worden toegepast**.
    -   Als deze optie is ingesteld op **Nee** en een creditnota is gemarkeerd op de pagina **Transacties vereffenen**, is de standaardinvoer in het veld **Contantkortingsbedrag dat moet worden toegepast** **0** (nul).
-   **Kortingstegenrekeningen (alleen leveranciers)**: definieer de grootboekrekening van de standaardcontantkorting die voor de boeking voor contantkortingen moet worden gebruikt.
    -   ** Hoofdrekening voor leverancierskortingen gebruiken**: de contantkorting wordt geboekt naar de hoofdrekening die op de pagina **Contantkortingsinstelling** wordt gedefinieerd.
    -   **Rekeningen op de factuurregels**: de contantkorting wordt geboekt naar de grootboekrekeningen op de oorspronkelijke factuur.
-   **Regels op facturen met vrije tekst en rentenota's markeren (alleen klanten)**: stel deze optie in op **Ja** om de knop **Factuurregels markeren** op de pagina´s **Klantbetalingen invoeren** **Betalingsjournaalboekstuk** en **Transacties vereffenen** in te schakelen. Met deze knop kunnen gebruikers afzonderlijke regels voor vereffening markeren.
-   **Prioriteit van vereffening (alleen klanten)**: stel deze optie in op **Ja** om de knop **Markeren op prioriteit** in te schakelen op de pagina **Klantbetalingen invoeren** en **Transacties vereffenen**. Deze knop kan gebruikers de vooraf vastgestelde vereffeningsorder toewijzen aan transacties.  Nadat de volgorde van vereffening is toegepast op een transactie, kunnen de order en de betalingstoewijzing worden gewijzigd voordat u deze boekt.
-   **Ken de prioriteit voor automatische vereffeningen** : deze optie instelt op **Ja** gebruik van de gedefinieerde prioriteitsvolgorde wanneer transacties automatisch worden vereffend. Dit veld is beschikbaar als de **prioriteit van vereffening** en **automatische vereffening** opties zijn ingesteld op **Ja**.



