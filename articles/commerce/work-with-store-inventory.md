---
title: Voorraadbeheer winkel
description: In dit onderwerp worden de typen documenten beschreven waarmee u de voorraad van uw organisatie kunt beheren.
author: rubencdelgado
manager: AnnBe
ms.date: 04/23/2019
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
ms.openlocfilehash: 3f7f228bbf312a2ccdc96d3e95287898bee01de4
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022099"
---
# <a name="store-inventory-management"></a>Voorraadbeheer winkel

[!include [banner](includes/banner.md)]

Bij het werken met voorraad in Dynamics 365 Commerce en met de POS-toepassing, is het belangrijk te weten dat POS beperkte ondersteuning voor voorraaddimensies en bepaalde voorraad artikeltypen biedt.

De POS-oplossing biedt geen ondersteuning voor de volgende artikelconfiguraties:

- Stuklijstartikelen (met uitzondering van de kitproducten die gebruikmaken van sommige onderdelen van de stuklijst)
- Catch weight-artikelen
- Batchvoorraadartikelen

De POS-toepassing ondersteunt momenteel niet de volgende traceringsdimensies in het POS:

- Batchtraceringsdimensie
- Eigenaarsdimensie

De POS-oplossing biedt beperkte ondersteuning voor de volgende dimensies. Beperkte ondersteuning geeft aan dat het POS enkele van deze dimensies standaard invult in voorraadtransacties automatisch gebaseerd op de magazijn/winkel-configuratie. POS ondersteunt de dimensies niet volledig op de manier waarop ze worden ondersteund als een verkooptransactie handmatig in het ERP wordt ingevoerd. 

- **Magazijnlocatie**: gebruikers kunnen de ontvangende magazijnlocatie niet beheren voor artikelen die zijn ontvangen in een winkelmagazijn wanneer de winkel niet is geconfigureerd voor gebruik van het magazijnbeheerproces. Voor deze artikelen wordt een standaardlocatie voor ontvangst gebruikt die is gedefinieerd in het winkelmagazijn. Als het magazijnbeheerproces is ingeschakeld voor de winkel, wordt beperkte ondersteuning geboden waarmee de gebruiker wordt gevraagd een ontvangstlocatie voor de volledige ontvangst te kiezen. Artikelen die vanuit de winkel worden verkocht, worden altijd vanuit de standaardvestiging verkocht zoals deze is gedefinieerd in de winkelmagazijninstellingen. De locatie voor het beheren van retourvoorraad kan worden beheerd via de standaarddefinitie van een retourlocatie in het winkelmagazijn of op basis van redencodes voor retouren die zijn gedefinieerd in het beleid voor retourlocaties.
- **Nummerplaat**: nummerplaten zijn alleen van toepassing wanneer **Magazijnbeheerproces gebruiken** is ingeschakeld voor het artikel en het winkelmagazijn. Wanneer in POS voorraad wordt ontvangen in een winkelmagazijn waarin het magazijnbeheerproces is ingeschakeld en wanneer de locatie die is gekozen om het artikel in te ontvangen aan een locatieprofiel is gekoppeld waarvoor een controle van de nummerplaat is vereist, voegt de POS-toepassing systematisch een nummerplaat toe aan de ontvangstregel. Gebruikers in POS kunnen deze gegevens van de nummerplaat niet wijzigen of beheren. Als volledig beheer van nummerplaten is vereist, wordt voorgesteld de mobiele WMS-toepassing of de ERP-client in de back-office te gebruiken in de winkel om de ontvangst van deze artikelen te beheren.
- **Serienummer** : de POS-toepassing heeft beperkte ondersteuning voor een enkel serienummer dat kan worden geregistreerd op een transactieverkoopregel voor orders die zijn gemaakt in POS met artikelen met serienummer. Dit serienummer wordt niet gevalideerd voor geregistreerde serienummers die zich al in de voorraad bevinden. Als een verkooporder wordt gemaakt in het callcenterkanaal of uitgevoerd via het ERP-systeem en meerdere serienummers zijn geregistreerd voor een enkele verkoopregel tijdens het uitvoeringsproces in het ERP-systeem, kunnen deze serienummers niet worden toegepast of gevalideerd als er een retour wordt verwerkt in POS voor deze orders.
- **Voorraadstatus**: voor artikelen die het magazijnbeheerproces gebruiken en waarvoor een voorraadstatus vereist is, kan dit statusveld niet worden ingesteld of gewijzigd via de POS-toepassing. De standaardvoorraadstatus zoals deze is gedefinieerd in de configuratie van het winkelmagazijn wordt gebruikt wanneer artikelen in de voorraad worden ontvangen.

> [!NOTE]
> Alle organisaties moeten artikelconfiguraties via POS testen in de ontwikkeling of testomgeving voordat u ze implementeert in de productie. Test uw artikelen door het uitvoeren van regelmatige contante verkooptransacties en het maken van klantorders (indien van toepassing) met het POS met uw items. Testen moet het uitvoeren van volledige boekingsprocessen in uw testomgeving omvatten en controleren of er geen problemen zijn.
>
> Het configureren van artikelen op een manier die niet wordt ondersteund door de POS-toepassing, zonder de juiste testen, kan ertoe leiden dat uw proces voor boekingsoverzichten niet werkt in productie zonder een eenvoudige manier om de problemen te corrigeren. Partner- of klantaanpassingen aan de toepassing kunnen desgewenst worden overwogen om te zorgen dat deze boekingsprocessen kunnen worden voltooid. Als aanpassingen niet nodig zijn, moet de organisatie ervoor zorgen dat de productconfiguratie van uw producten is uitgevoerd op een manier die wordt ondersteund door de standaard POS-toepassing/orders maken/boekingsproces voor overzichten.

## <a name="purchase-orders"></a>Inkooporders

Inkooporders worden gemaakt op het hoofdkantoor. Als een magazijn in de koptekst van de inkooporder is opgenomen, kan de order in de winkel worden ontvangen via Modern POS (MPOS) of Cloud POS met de bewerking **Orderverzameling/ontvangst**. Nadat de hoeveelheden die in de winkel zijn ontvangen, zijn ingevoerd in het veld **Nu ontvangen** in POS voor het inkooporderdocument, kunnen ze lokaal worden opgeslagen of worden vastgelegd. Het lokaal opslaan van deze gegevens heeft geen invloed op de voorhanden voorraad. Opslaan moet alleen plaatsvinden als de gebruiker niet gereed is om de ontvangst naar HQ te boeken en u hebt alleen een manier nodig om eerder ingevoerde gegevens voor **Nu ontvangen** tijdelijk op te slaan. Hiermee worden de gegevens voor nu ontvangen lokaal opgeslagen in de kanaaldatabase van de gebruiker. Nadat het document is verwerkt met de optie **Vastleggen**, worden de gegevens voor **Nu ontvangen** naar HQ verzonden en wordt de ontvangst van de inkooporder geboekt. 

## <a name="transfer-orders"></a>Transferorders

Met een transferorder kan worden opgegeven dat een bepaalde winkel de locatie is waaruit artikelen kunnen worden verzonden of de locatie waarin de voorraad wordt ontvangen. Als de POS-gebruiker het verzendmagazijn voor een transferorder is, kunnen hoeveelheden voor **Nu verzenden** vanuit POS worden ingevoerd. De gegevens die door de verzendende winkel worden ingevoerd, kunnen lokaal worden opgeslagen of worden vastgelegd. Wanneer lokaal wordt opgeslagen, worden er geen wijzigingen aangebracht in het document voor de transferorder in HQ. Opslaan moet alleen plaatsvinden als de gebruiker niet gereed is om de zending naar HQ te boeken en u hebt een manier nodig om eerder ingevoerde gegevens voor **Nu verzenden** tijdelijk op te slaan. Nadat de winkel de zending heeft bevestigd, moet de optie **Vastleggen** worden geselecteerd. Hiermee wordt de verzending van de transferorder in HQ geboekt, zodat het ontvangende magazijn deze nu kan ontvangen. 

Als de POS-gebruiker het ontvangend magazijn voor een transferorder is, kunnen de hoeveelheden voor **Nu ontvangen** vanuit POS worden ingevoerd. De gegevens die door de ontvangende winkel worden ingevoerd, kunnen lokaal worden opgeslagen of worden vastgelegd. Opslaan moet alleen plaatsvinden als de gebruiker niet gereed is om de ontvangst naar HQ te boeken en u hebt een manier nodig om eerder ingevoerde gegevens voor **Nu ontvangen** tijdelijk op te slaan. Hiermee worden de gegevens voor nu ontvangen lokaal opgeslagen in de kanaaldatabase van de gebruiker. Nadat het document is verwerkt met de optie **Vastleggen**, worden de gegevens voor **Nu ontvangen** naar HQ verzonden en wordt de ontvangst van de transferorder geboekt. Het is belangrijk te weten dat de ontvangende winkel wordt beperkt tot het ontvangen van hoeveelheden die gelijk zijn aan of kleiner zijn dan de verzonden hoeveelheden. Een poging om hoeveelheden te ontvangen voor een transferorder die nog niet eerder is verzonden resulteert in fouten en de ontvangst wordt niet bevestigd in HQ.

## <a name="stock-counts"></a>Voorraadtellingen

Voorraadtellingen kunnen gepland of ongepland worden uitgevoerd. Geplande voorraadtellingen worden in gang gezet op het hoofdkantoor, dat bepaalt welke artikelen moeten worden geteld. Het hoofdkantoor maakt een voorraadtellingsdocument dat in de winkel kan worden ontvangen waarop de hoeveelheden die daadwerkelijk in voorraad zijn, worden ingevoerd in MPOS of Cloud POS. Ongeplande voorraadtellingen worden gestart in de winkel en de hoeveelheden van de werkelijke voorhanden voorraad worden bijgewerkt in MPOS of Cloud POS. In tegenstelling tot de geplande voorraadtellingen werken ongeplande voorraadtellingen niet met een vooraf gedefinieerde lijst met artikelen. Wanneer een voorraadtelling van beide typen is voltooid, wordt deze toegezegd en verzonden naar het hoofdkantoor. De telling wordt op het hoofdkantoor gevalideerd en geboekt als aparte stap.

## <a name="inventory-lookup"></a>Zoeken in voorraad

De huidige voorhanden producthoeveelheid voor meerdere winkels en magazijnen kan worden weergegeven op de pagina **Zoeken in voorraad**. Naast de huidige voorhanden hoeveelheid kunnen de toekomstige ATP-hoeveelheden (Available To Promise) worden weergegeven voor elke afzonderlijke winkel. Als u dit wilt doen, selecteert u de winkel waarvoor u de ATP wilt weergeven en klikt u vervolgens op **Beschikbaarheid van winkel weergeven**.
