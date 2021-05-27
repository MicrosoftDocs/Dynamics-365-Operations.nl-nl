---
title: Voorraadbeheer winkel
description: In dit onderwerp worden de typen documenten beschreven waarmee u de voorraad van uw organisatie kunt beheren.
author: rubencdelgado
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 64106cb1aeea01f1f227247d32b8b1dfdea98362
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020190"
---
# <a name="commerce-inventory-management"></a>Commerce-voorraadbeheer

[!include [banner](includes/banner.md)]

Wanneer u werkt met voorraad in Microsoft Dynamics 365 Commerce en u een van de Commerce-toepassingen gebruikt die zijn gekoppeld aan een CSU (Commerce Scale Unit), is het belangrijk te weten dat de orderverwerkingslogica in CSU beperkte ondersteuning biedt voor sommige voorraaddimensies en voorraadartikeltypen. Commerce-toepassingen bieden geen ondersteuning voor de volledige reeks mogelijkheden voor artikelconfiguratie die beschikbaar zijn via de opties voor artikelconfiguratie in Dynamics 365 Supply Chain Management.

De Commerce-toepassingen op CSU bieden geen ondersteuning voor de volgende productdimensies en artikelconfiguraties:

- Productdimensie- en stuklijstartikelen voor de configuratie (met uitzondering van producten in detailhandelkits, die bepaalde onderdelen van de stuklijst gebruiken)
- Catch weight-artikelen
- Artikelen met door productdimensies beheerde versie

De Commerce-toepassingen op CSU ondersteunen niet de volgende traceringsdimensies:
- Eigenaarsdimensie

- De POS-toepassing kan beperkte ondersteuning bieden voor de volgende dimensies. Het POS voert mogelijk automatisch enkele van de dimensies in voorraadtransacties in op basis van de configuratie van het magazijn of de winkel. Het POS ondersteunt de dimensies niet volledig op de manier waarop ze worden ondersteund als een verkooptransactie handmatig in Commerce Headquarters wordt ingevoerd. 

- **Magazijnlocatie**: wanneer deze de nieuwe POS-bewerkingen [inkomende bewerking](./pos-inbound-inventory-operation.md) en [uitgaande bewerking](./pos-outbound-inventory-operation.md) gebruiken, kunnen gebruikers een magazijnvoorraadlocatie selecteren voor het ontvangen van artikelen of het verzenden van uitgaande overboekingsorderartikelen. Als ze de verouderde bewerking **Verzamelen en ontvangen** gebruiken, is er beperkte ondersteuning voor locatiebeheer beschikbaar voor ontvangst en verzending van uitgaande overdrachten. Deze ondersteuning is alleen beschikbaar als de optie **Magazijnbeheerproces gebruiken** is ingeschakeld voor het artikel en het winkelmagazijn. Een voorraadlocatie kan momenteel niet worden gebruikt met de bewerking **Voorraadtelling** of de bewerking **Zoeken in voorraad**.

- **Nummerplaat**: nummerplaten zijn alleen van toepassing wanneer de optie **Magazijnbeheerproces gebruiken** is ingeschakeld voor het artikel en het winkelmagazijn. Als in het POS voorraad wordt ontvangen in een winkelmagazijn via de bewerking **Inkomende bewerking** of de bewerking **Verzameling en ontvangen** waarbij het magazijnbeheerproces is ingeschakeld, en als de locatie die is geselecteerd om het artikel in te ontvangen, aan een locatieprofiel is gekoppeld waarvoor een controle van de nummerplaat is vereist, past de POS-toepassing systematisch een nummerplaat toe op de ontvangstregel. POS-gebruikers kunnen deze nummerplaatgegevens niet wijzigen of beheren. Als volledig beheer van nummerplaten is vereist, adviseren we de winkel gebruik te maken van de [app voor magazijnbeheer](../supply-chain/warehousing/install-configure-warehousing-app.md) of de client in de back-office om de ontvangst van deze artikelen te beheren.

- **Serienummer**: de POS-toepassing biedt beperkte ondersteuning voor registratie van een enkel serienummer op een transactieverkoopregel voor orders die worden gemaakt in het POS en die artikelen met serienummer bevatten. Dit serienummer wordt niet gevalideerd voor geregistreerde serienummers die zich al in de voorraad bevinden. Als een verkooporder wordt gemaakt in het callcenterkanaal of uitgevoerd via het ERP-systeem (Enterprise Resource Planning) en meerdere serienummers zijn geregistreerd op een enkele verkoopregel tijdens het uitvoeringsproces in het ERP-systeem, kunnen deze serienummers niet worden toegepast of gevalideerd als er een retour wordt verwerkt voor de order in het POS. Wanneer voorraad wordt ontvangen via de bewerking **Inkomende bewerking**, kunnen gebruikers [de ontvangen serienummers registreren of bevestigen](./pos-serialized-items.md).

- **Batch-id:** de POS-toepassing biedt beperkte ondersteuning tijdens het boeken van overzichten als een batchartikel wordt verkocht, maar POS-gebruikers kunnen de batch-id niet definiëren die is verkocht of opgehaald met de POS-toepassing.

- **Voorraadstatus**: voor artikelen die het magazijnbeheerproces gebruiken en waarvoor een voorraadstatus vereist is, kan dit statusveld niet worden ingesteld of gewijzigd via de POS-toepassing. De standaardvoorraadstatus die is gedefinieerd in de configuratie van het winkelmagazijn wordt gebruikt wanneer artikelen in de voorraad worden ontvangen.

> [!NOTE]
> Alle organisaties moeten artikelconfiguraties via Commerce-apps testen in ontwikkel- of testomgevingen voordat zij deze artikelconfiguraties implementeren in productieomgevingen. Test uw artikelen door deze te gebruiken voor het uitvoeren van regelmatige contante verkooptransacties en het maken van klantorders (indien van toepassing) via het POS, callcenter of e-commerce om te valideren dat deze volledig kunnen worden ondersteund. U moet ook de processen voor afhandeling en voorraadbeheer van het POS testen (zoals bewerkingen voor het ontvangen van voorraad en het afhandelen van orders) voordat u nieuwe artikelconfiguraties gaat implementeren, om ervoor te zorgen dat de POS-toepassing deze kan ondersteunen. Bij het testen moet een volledig overzicht/orderboekingsproces in uw testomgeving worden uitgevoerd en moet worden gecontroleerd of er geen boekingsproblemen optreden wanneer orders voor deze artikelen worden gemaakt en geboekt in Commerce Headquarters.
>
> Als artikelen zo worden geconfigureerd dat deze niet worden ondersteund door de Commerce-toepassingen en de juiste tests niet worden uitgevoerd, kunnen er gegevensproblemen optreden die niet eenvoudig of helemaal niet kunnen worden gecorrigeerd.

## <a name="purchase-orders"></a>Inkooporders

Inkooporders worden gemaakt in Commerce Headquarters. Als een winkelmagazijn in de koptekst van de inkooporder of op inkooporderregels is opgenomen, kunnen de regels in de winkel worden ontvangen via de bewerking [Inkomende bewerking](./pos-inbound-inventory-operation.md) in het POS. 

## <a name="transfer-orders"></a>overboekingsorders

overboekingsorders kunnen worden gemaakt in Commerce Headquarters of via de bewerking [Inkomende bewerking](./pos-inbound-inventory-operation.md) of [Uitgaande bewerking](./pos-outbound-inventory-operation.md) in het POS. Gebruik de POS-bewerking **Inkomende bewerking** om een aanvraag voor een overboekingsorder te maken zodat de voorraad naar de winkel wordt verzonden vanuit een ander magazijn of een andere winkellocatie. Gebruik de POS-bewerking **Uitgaande bewerking** om een aanvraag voor een overboekingsorder te maken voor verzending van voorraad vanuit de winkel naar een ander magazijn of een andere winkellocatie. Nadat een overboekingsorder voor een winkel is gemaakt, kan die winkel de voorraadontvangst voor de overboekingsorder beheren via de bewerking **Inkomende bewerking** in het POS. Als de winkelvoorraad naar een andere locatie wordt verzonden, wordt de bewerking **Uitgaande bewerking** in het POS gebruikt om het uitgaande verzendproces van die winkel te beheren.

## <a name="stock-counts"></a>Voorraadtellingen

Voorraadtellingen kunnen gepland of ongepland worden uitgevoerd. Geplande voorraadtellingen worden gemaakt via Commerce Headquarters door een journaaldocument voor tellingen te maken dat is gekoppeld aan het magazijn van de winkel. In dit journaal worden de artikelen opgegeven die moeten worden geteld. De winkel kan vervolgens toegang krijgen tot deze vooraf gedefinieerde tellingsjournalen en er acties op uitvoeren met behulp van de bewerking **Voorraadtelling** in het POS. Winkelgebruikers starten een niet-geplande voorraadtelling, omdat deze nodig is wanneer ze de bewerking **Voorraadtelling** in het POS gebruiken. In tegenstelling tot de geplande voorraadtellingen werken ongeplande voorraadtellingen niet met een vooraf gedefinieerde lijst met artikelen. Wanneer een voorraadtelling van beide typen is voltooid in het POS, wordt deze toegezegd en verzonden naar het hoofdkantoor. In het hoofdkantoor moet de telling vervolgens als een afzonderlijke stap in Commerce Headquarters worden gevalideerd en geboekt.

## <a name="inventory-lookup"></a>Zoeken in voorraad

De producthoeveelheid die momenteel voorhanden is voor meerdere winkels en magazijnen kan worden weergegeven op de pagina **Zoeken in voorraad**. Naast de huidige voorhanden hoeveelheid kunnen de toekomstige ATP-hoeveelheden (Available To Promise) worden weergegeven voor elke winkel. Selecteer de winkel waarvoor u de ATP-hoeveelheden wilt weergeven en selecteer vervolgens **Beschikbaarheid van de winkel weergeven**. Zie [Voorraadbeschikbaarheid voor detailhandelkanalen berekenen](./calculated-inventory-retail-channels.md) voor informatie over de beschikbare configuratieopties.


[!INCLUDE[footer-include](../includes/footer-banner.md)]