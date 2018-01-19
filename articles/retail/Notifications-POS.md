---
title: Ordermeldingen weergeven in POS-client
description: In dit onderwerp wordt beschreven hoe u ordermeldingen inschakelt in de POS-client en het framework voor meldingen, dat kan worden uitgebreid naar andere bewerkingen.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: ShalabhjainMSFT
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: ec6cb212766dd90fa9db7719a2119419ecb935c7
ms.openlocfilehash: aea36591a81f727059e37a958efa62a9ebde9d9d
ms.contentlocale: nl-nl
ms.lasthandoff: 12/20/2017

---

# <a name="display-notifications-in-point-of-sale"></a>Meldingen weergeven in POS-client

In de huidige moderne detailhandelomgeving worden er verschillende taken toegewezen aan winkelmedewerkers, zoals het helpen van klanten, het invoeren van transacties, het uitvoeren van voorraadtellingen en het ontvangen van orders in de winkel. De POS-client (Pont of Sale) stelt de medewerkers in staat deze taken en nog veel meer in één toepassing uit te voeren. Omdat ze gedurende de dag verschillende taken moeten uitvoeren, moeten medewerkers mogelijk op de hoogte worden gesteld wanneer iets hun aandacht vereist. Het framework voor meldingen in de POS-client lost dit probleem op door de detailhandelaren in staat te stellen meldingen op basis van rollen te configureren. Met Dynamics 365 for Retail met toepassingsupdate 5 kunnen deze meldingen alleen worden geconfigureerd voor POS-bewerkingen.

Op dit moment biedt het systeem de mogelijkheid om meldingen weer te geven voor orderafhandelingsbewerking. Het framework is echter ontworpen om te kunnen worden uitgebreid, zodat ontwerpers in de toekomst een meldingshandler kunnen schrijven voor elke bewerking en de meldingen kunnen weergeven in het verkooppunt.  

## <a name="enable-notifications-for-order-fulfillment-operations"></a>Meldingen voor orderafhandelingsbewerkingen inschakelen

Ga als volgt te werk om meldingen voor de orderafhandelingsbewerkingen in te schakelen:

 - Ga naar de pagina **Bewerkingen** (**Detailhandel** > **Afzetkanaalinstellingen** > **POS-instellingen** > **POS** > **Bewerkingen**).
 - Zoek de bewerking Orderafhandeling en schakel het selectievakje **Meldingen inschakelen** in voor deze bewerking. Hiermee geeft u aan het framework voor meldingen aan dat er moet worden geluisterd naar de handler voor de afhandelingsorderbewerking. Als de handler is geïmplementeerd, worden de meldingen weergegeven in het verkooppunt. Is dit niet het geval, dan worden de meldingen niet weergegeven voor deze bewerking.
- Ga naar de POS-machtigingen die zijn gekoppeld aan de werknemers, voeg onder het sneltabblad **Meldingen** de bewerking Orderafhandeling toe en stel Weergavevolgorde in op 1. Wanneer er meer dan één melding is geconfigureerd, wordt de weergavevolgorde gebruikt om de meldingen van boven naar beneden te rangschikken, waarbij 1 de bovenste melding is. Alleen bewerkingen waarvoor het selectievakje **Meldingen inschakelen** is ingeschakeld, kunnen worden toegevoegd. Daarnaast worden de meldingen alleen weergegeven voor de bewerkingen die hier zijn toegevoegd en alleen voor die werknemers voor wie de bewerkingen zijn toegevoegd aan de bijbehorende POS-machtigingen. 

> [!NOTE]
> U kunt meldingen op gebruikersniveau overschrijven door naar de record van een werknemer te gaan, **POS-machtigingen** te selecteren en vervolgens het meldingsabonnement van die gebruiker te bewerken.

 - Ga naar de pagina **Functionaliteitsprofiel** (**Detailhandel** > **Afzetkanaalinstellingen** > **POS-instellingen** > **POS-profielen** > **Functionaliteitsprofielen**). Werk de eigenschap **Meldingsinterval** bij om in minuten in te stellen met welk interval de meldingen moeten worden opgehaald. U wordt aangeraden deze waarde in te stellen op 10 minuten om onnodige communicatie met het hoofdkantoor te voorkomen. Wanneer u dit interval op 0 instelt, worden er geen meldingen weergegeven.  

 - Ga naar **Detailhandel** > **IT detailhandel** > **Distributieplanning**. Selecteer de planning 1060-Personeel om instellingen voor meldingsabonnementen te synchroniseren en klik op **Nu uitvoeren**. Synchroniseer vervolgens het machtigingsinterval door de configuratie 1070-Kanaal te selecteren en op **Nu uitvoeren** te klikken. 

## <a name="view-notifications-in-pos"></a>Meldingen weergeven in POS-client

Als u de bovenstaande stappen hebt voltooid, kunnen de werknemers voor wie u de meldingen hebt ingesteld de meldingen weergeven in de POS-client. Als u de meldingen wilt weergegeven, klikt u op het meldingspictogram in de titelbalk van de POS-client. Vervolgens wordt het meldingencentrum met de meldingen voor de orderafhandelingsbewerking weergegeven. Als het goed is, worden de volgende groepen weergegeven: 

- **Orders in behandeling**: voor deze groep wordt het aantal orders met de status in behandeling weergegeven, zoals orders die moeten worden geaccepteerd door een POS-medewerker met de vereiste machtigingen voor afhandeling in de winkel. Wanneer u op het weergegeven getal op de groep klikt, wordt de pagina **Orderafhandeling** weergegeven, gefilterd om alleen de orders in behandeling weer te geven die aan de winkel zijn toegewezen voor afhandeling. Als de orders automatisch worden geaccepteerd voor de winkel, is het aantal voor deze groep nul.

- **Ophalen in de winkel**: voor deze groep wordt het aantal orders weergegeven waarvoor de leveringsmethode **Afhalen** is ingesteld en de huidige winkel is ingesteld als afhaallocatie. Wanneer u op het weergegeven getal op de groep klikt, wordt de pagina **Orderafhandeling** weergegeven, gefilterd om de actieve orders weer te geven die zijn ingesteld om te worden verzameld vanuit de huidige winkel.

- **Verzenden uit winkel**: voor deze groep wordt het aantal orders weergegeven waarvoor de leveringsmethode **Verzenden** is ingesteld en de huidige winkel is ingesteld als verzendlocatie. Wanneer u op het weergegeven getal op de groep klikt, wordt de pagina **Orderafhandeling** weergegeven, gefilterd om de actieve orders weer te geven die zijn ingesteld om te worden verzonden vanuit de huidige winkel.

Wanneer er nieuwe orders aan de winkel worden toegewezen voor afhandeling, verandert het meldingspictogram om aan te geven dat er nieuwe meldingen zijn en het aantal bijbehorende groepen wordt bijgewerkt. De gebruiker kan ook klikken op het pictogram voor vernieuwen, naast de naam van de bewerking, om de telling van de groepen onmiddellijk bij te werken. De telling wordt ook bijgewerkt op basis van het vooraf gedefinieerde interval. Voor elke groep met een nieuw artikel, dat niet is gezien door de huidige werknemer, wordt een pictogram weergegeven om aan te geven dat deze groep een nieuw artikel heeft. Door te klikken op de tegels in meldingen opent u de specifieke bewerking waarvoor deze melding is geconfigureerd. In de bovenstaande scenario's wordt de pagina **Orderafhandeling** geopend en worden de juiste parameters doorgegeven: orders in behandeling, ophalen in de winkel en verzenden uit winkel. 

> [!NOTE]
> Meldingen voor orders in behandeling worden in een toekomstige update van Dynamics 365 for Retail ingeschakeld. 


