---
title: Voorraadbeheer winkel
description: In dit onderwerp worden de typen documenten beschreven waarmee u de voorraad van uw organisatie kunt beheren.
author: rubencdelgado
manager: AnnBe
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 02f8afbe3bb6f94c66a8b5aa02531c219adc3963
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "339229"
---
# <a name="store-inventory-management"></a>Voorraadbeheer winkel

[!include [banner](includes/banner.md)]

In dit onderwerp worden de typen documenten beschreven waarmee u de voorraad van uw organisatie kunt beheren.

Met de volgende typen documenten kunt u de voorraad van uw organisatie beheren.

Bij het werken met voorraad in Dynamics 365 for Retail en met de POS-toepassing, is het belangrijk te weten dat POS beperkte ondersteuning voor voorraaddimensies en bepaalde voorraad artikeltypen biedt.  

De POS-oplossing biedt geen ondersteuning voor de volgende artikelconfiguraties:
- Stuklijstartikelen (met uitzondering van de kitproducten die gebruikmaken van sommige onderdelen van de stuklijst)
- Catch weight-artikelen
- Batchvoorraadartikelen

De POS-toepassing ondersteunt momenteel niet de volgende traceringsdimensies in het POS:
- Batchtraceringsdimensie
- Eigenaarsdimensie

De POS-oplossing biedt beperkte ondersteuning voor de volgende dimensies. Beperkte ondersteuning geeft aan dat het POS enkele van deze dimensies standaard invult in voorraadtransacties automatisch gebaseerd op de magazijn/winkel-configuratie. POS ondersteunt de dimensies niet volledig op de manier waarop ze worden ondersteund als een verkooptransactie handmatig in het ERP wordt ingevoerd. 

- Locatie
- Nummerplaat (alleen van toepassing wanneer **Magazijnbeheerproces gebruiken** is ingeschakeld voor het artikel en het winkelmagazijn)
- Serienummer
- Voorraadstatus

> [!NOTE]
> Alle organisaties moeten artikelconfiguraties via POS testen in de ontwikkeling of testomgeving voordat u ze implementeert in de productie. Test uw artikelen door het uitvoeren van regelmatige contante verkooptransacties en het maken van klantorders (indien van toepassing) met het POS met uw items. Testen moet het uitvoeren van volledige boekingsprocessen in uw testomgeving omvatten en controleren of er geen problemen zijn.
> Het configureren van artikelen op een manier die niet wordt ondersteund door de POS-toepassing, zonder de juiste testen, kan ertoe leiden dat uw proces voor boekingsoverzichten niet werkt in productie zonder een eenvoudige manier om de problemen te corrigeren. Partner- of klantaanpassingen aan de toepassing kunnen desgewenst worden overwogen om te zorgen dat deze boekingsprocessen kunnen worden voltooid. Als aanpassingen niet nodig zijn, moet de organisatie ervoor zorgen dat de productconfiguratie van uw producten is uitgevoerd op een manier die wordt ondersteund door de standaard POS-toepassing/orders maken/boekingsproces voor overzichten.

## <a name="purchase-orders"></a>Inkooporders

Inkooporders worden gemaakt op het hoofdkantoor. Als een detailhandelsmagazijn in de koptekst van de inkooporder wordt opgenomen, kan de order worden ontvangen in de winkel door middel van Modern POS (MPOS) of Cloud POS in Microsoft Dynamics 365 for Retail. Nadat de hoeveelheden die in de winkel zijn ontvangen, worden ingevoerd, kunnen zij lokaal worden opgeslagen voor verdere wijzigingen. Ook kan de hoeveelheden kunnen worden vastgelegd en verzonden naar het hoofdkantoor. Op het hoofdkantoor worden de hoeveelheden die zijn ontvangen in de winkel, weergegeven in Dynamics 365 for Retail, in het veld **Nu ontvangen** op de inkooporder.

## <a name="transfer-orders"></a>Transferorders

Een transferorder kan opgeven dat een bepaalde winkel een locatie is waaruit artikelen kunnen worden verzonden. In dit geval wordt de transferorder weergegeven in de winkel als een aanvraag voor picken in MPOS of Cloud POS. Nadat het picken van de aangevraagde hoeveelheden, worden ze toegezegd en verzonden naar het hoofdkantoor. Op het hoofdkantoor worden de hoeveelheden die in de winkel zijn opgenomen, weergegeven in Dynamics 365 for Retail, in het veld **Nu verzenden** op de transferorder. Een transferorder kan opgeven dat een bepaalde winkel een locatie is waarnaar artikelen kunnen worden verzonden. In dit geval wordt de transferorder weergegeven in de winkel als een aanvraag voor ontvangen in MPOS of Cloud POS. Nadat de hoeveelheden die in de winkel zijn ontvangen, worden ingevoerd, kunnen zij lokaal worden opgeslagen voor verdere wijzigingen. Ook kan de hoeveelheden kunnen worden vastgelegd en verzonden naar het hoofdkantoor. Op het hoofdkantoor worden de hoeveelheden die zijn ontvangen in de winkel, weergegeven in Dynamics 365 for Retail, in het veld **Nu ontvangen** op de transferorder.

## <a name="stock-counts"></a>Voorraadtellingen

Voorraadtellingen kunnen gepland of ongepland worden uitgevoerd. Geplande voorraadtellingen worden in gang gezet op het hoofdkantoor, dat bepaalt welke artikelen moeten worden geteld. Het hoofdkantoor maakt een voorraadtellingsdocument dat in de winkel kan worden ontvangen waarop de hoeveelheden die daadwerkelijk in voorraad zijn, worden ingevoerd in MPOS of Cloud POS. Ongeplande voorraadtellingen worden gestart in de winkel en de hoeveelheden van de werkelijke voorhanden voorraad worden bijgewerkt in MPOS of Cloud POS. In tegenstelling tot de geplande voorraadtellingen werken ongeplande voorraadtellingen niet met een vooraf gedefinieerde lijst met artikelen. Wanneer een voorraadtelling van beide typen is voltooid, wordt deze toegezegd en verzonden naar het hoofdkantoor. De telling wordt op het hoofdkantoor gevalideerd en geboekt.

## <a name="inventory-lookup"></a>Zoeken in voorraad

De huidige voorhanden producthoeveelheid voor meerdere winkels en magazijnen kan worden weergegeven op de pagina Zoeken in voorraad. Naast de huidige voorhanden hoeveelheid kunnen de toekomstige ATP-hoeveelheden (Available To Promise) worden weergegeven voor elke afzonderlijke winkel. Als u dit wilt doen, selecteert u de winkel waarvoor u de ATP wilt weergeven en klikt u vervolgens op **Beschikbaarheid van winkel weergeven**.
