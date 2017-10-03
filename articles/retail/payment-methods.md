---
title: Betalingsmethoden
description: Elk betalingstype dat een detailhandelaar accepteert, moet worden geconfigureerd wanneer het systeem wordt ingesteld. In dit artikel wordt beschreven welke betalingstypen u kunt instellen en wordt het proces beschreven voor het instellen hiervan.
author: MargoC
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: b9570efe8b90dc6402fef67cf7838e5d8546cf02
ms.contentlocale: nl-nl
ms.lasthandoff: 06/20/2017

---

# <a name="payment-methods"></a>Betalingsmethoden

[!include[banner](includes/banner.md)]


Elk betalingstype dat een detailhandelaar accepteert, moet worden geconfigureerd wanneer het systeem wordt ingesteld. In dit artikel wordt beschreven welke betalingstypen u kunt instellen en wordt het proces beschreven voor het instellen hiervan.

Detailhandelaren kunnen verschillende typen betaling accepteren voor de producten en diensten die ze verkopen. Hoewel contantbetalingen de meestvoorkomende vorm van betalingen zijn, kunnen detailhandelaren ook betalingen ontvangen in de vorm van cheques, kaarten, tegoedbonnen, enzovoort. Elk betalingstype dat de detailhandelaar accepteert, moet worden geconfigureerd in Dynamics 365 for Retail wanneer het systeem wordt ingesteld. De volgende lijst bevat omschrijvingen van elk betalingstype dat kan worden ingesteld in Dynamics 365 for Retail:

-   **Contant**: geld in de fysieke vorm van valuta, zoals bankbiljetten en muntstukken. Deze valuta kan de bedrijfsvaluta zijn of de lokale valuta van de winkel.
-   **Cheque**: een verhandelbaar middel voor betaling van een bepaald bedrag in een bepaalde valuta door een bepaalde bank. Een cheque is meestal geldig voor onbepaalde tijd of gedurende zes maanden na uitgifte, tenzij een andere geldigheidsperiode is opgegeven. De periode varieert, afhankelijk van de bank waar de cheque wordt geïnd. Er zijn verschillende soorten cheques, zoals cheques aan order, cheques aan balie, cheques aan toonder en cheques op naam. U kunt cheques instellen als een betalingsmethode voor elke winkel. Cheques kunnen worden geaccepteerd in de valuta die op het niveau van het bedrijf of de winkel is opgegeven. U moet cheques instellen als een betalingsmethode voordat u een cheque kunt accepteren als betaling in een winkel.
-   **Valuta**: de hoofdvorm van betaling anders dan de standaardvaluta van het bedrijf. Munten en bankbiljetten zijn beide vormen van valuta. Deze betalingsmethode vertegenwoordigt alle valuta's die worden gebruikt. Voordat u deze betalingsmethode kunt gebruiken, moet u valuta's instellen en detailhandelwisselgegevens voor de valuta's opgeven.
-   **Kaart**: Alle typen kaarten die worden gebruikt, zoals betaalpassen en creditcards. Het is een goed idee om op organisatieniveau maar één kaartbetalingsmethode in te stellen die alle typen kaarten vertegenwoordigt. Op het niveau van de winkel kan vervolgens een betalingsmethode worden ingesteld voor elke kaart of reeks kaarten die met dezelfde instellingen moet worden verwerkt. U moet instellen om welke kaarten het gaat, met andere woorden betaalpassen en creditcards, voordat u de kaarten in een winkel als betaling kunt accepteren.
-   **Creditnota** - Creditnota's die worden uitgegeven of ingewisseld bij het verkooppunt. De creditnota kan een creditnota of retourcreditnota zijn die is uitgegeven tegen een retourverkoop. Als creditnota's slechts gedeeltelijk worden ingewisseld, geeft het programma een nieuwe creditnota uit voor het nieuwe saldo. De nieuwe creditnota heeft een nieuw nummer. Een creditnota kan maar één keer worden gebruikt en alle gebruikte nummers worden in het systeem geregistreerd. De record kan op de pagina **Creditnotatabel** worden weergegeven. Een klant kan geen groter bedrag inwisselen dan de waarde van de creditnota.
-   **Geschenkbon**: geschenkbonnen die worden uitgegeven of ingewisseld bij het verkooppunt. Overbetaling op geschenkbonnen is niet toegestaan.
-   **Klantrekening**: betalingen die op het moment van de verkoop kunnen worden afgeschreven van de klantrekening. U kunt deze betalingsmethode ook gebruiken om verkoopinformatie of klantspecifieke kortingen te verzamelen wanneer de klant op een andere manier een betaling doet. In dat geval moet u klantspecifieke informatie hebben ingesteld.
-   **Loyaliteitspunten** : Het aantal punten dat klanten door middel van loyaliteitsprogramma's verzamelt. Als u loyaliteitsprogramma's maakt, kunnen klanten punten behalen en deze vervolgens op verschillende manieren terugkopen. In sommige loyaliteitsprogramma's kunnen klanten bijvoorbeeld loyaliteitspunten terugkopen in de vorm van een korting of deze zelfs gebruiken als vorm van betaling.

Voor het instellen van betalingsmethoden moet u de volgende taken voltooien.

1.  Betalingsmethoden instellen voor een organisatie. De betalingsmethoden maken die in de gehele organisatie worden geaccepteerd.
2.  Kaarttypen en kaartnummers voor de hele organisatie maken. Als creditcards of betaalpassen worden geaccepteerd, moet u één betalingsmethode maken voor kaarten en vervolgens de typen kaarten en kaartnummers voor de organisatie maken.
3.  Betalingsmethoden voor winkels instellen. Koppel betalingsmethoden aan elke winkel en voer vervolgens de winkelspecifieke instellingen in voor elke betalingsmethode.
4.  Betalingsmethoden via kaart instellen voor winkels. Voltooi de kaartinstellingen voor alle kaartbetalingsmethoden die door de winkel worden geaccepteerd.




