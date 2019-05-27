---
title: Gedeeltelijke verzending van een transportlading
description: In dit onderwerp wordt uitgelegd hoe u gedeeltelijk een lading verzendt en de planning van capaciteit voor de lading uitstelt.
author: Mirzaab
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTransportLoad
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 8c172f1b66e56f60e89f56ea98910f8d0e4f3e36
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545262"
---
# <a name="partial-shipment-of-a-transport-load"></a>Gedeeltelijke verzending van een transportlading

[!include[banner](../includes/banner.md)]

Door gedeeltelijke verzending van ladingen in te stellen kunt u ladingen verwerken waarvoor de capaciteit niet kan worden bepaald totdat alle verkoopregels zijn toegevoegd. Het proces kan vervolgens worden voltooid als het exacte palletaantal bekend is. U hoeft daarom niet te bepalen welke pallets worden toegewezen aan welk transport tot op het moment waarop een transport fysiek wordt geladen uit de gefaseerde voorraad.

Deze functie is een alternatief voor het afdwingen van een meer starre structuur, waarbij u moet bepalen welke pallets worden toegewezen aan welk transport vóór het verzamel- of ladingswerk kan worden gemaakt. In plaats daarvan kunnen gebruikers afzonderlijke ladingen configureren voor de bevestiging van een gedeeltelijke verzending. De transportlaadprocessen voor deze ladingen kunnen dan plaatsvinden. Zo kan de transportplanningsdienst ladingen plannen zonder rekening te houden met de capaciteit van afzonderlijke transporten.

Op het moment van laden kunnen werknemers een nieuwe transportlading definiëren waarvoor een pallet kan worden geladen. Ze kunnen ook een bestaande transportlading aangeven. Deze gegevens kan worden geregistreerd via een mobiel apparaat. Daarom kunnen verschillende magazijnmedewerkers voorraad laden uit dezelfde of verschillende ladingen op de dezelfde vrachtwagen. De ladingen kunnen vervolgens volledig of gedeeltelijk worden verzonden.

> [!NOTE] 
> Om voorraad te laden vanuit een lading voor een bepaalde transportlading en en het gedeeltelijk verzenden van de lading , moet werk worden gegenereerd met behulp van een ladingsklasse in een werksjabloon. Gewone verzamelactiviteiten van het type **Verzamelen** kunnen niet worden geladen voor een transportlading zoals een vrachtwagen.

## <a name="set-up-transport-loads-for-partial-shipment"></a>Transportladingen voor gedeeltelijke verzending instellen

De instelling voor gedeeltelijke verzending van ladingen bestaat uit de volgende twee procedures.

### <a name="set-the-loading-strategy"></a>Ladingstrategie instellen

U moet gedeeltelijk laden inschakelen door het instellen van de ladingstrategie. Nadat u een lading hebt gemaakt, kunt u de ladingstrategie instellen.

1. Selecteer **Magazijnbeheer** \> **Ladingen** \> **Alle ladingen**.
2. Selecteer een lading en klik op **Koptekst**.
3. Selecteer in het veld **Ladingstrategie** **Verzending van gedeeltelijke lading toegestaan**.

### <a name="create-a-menu-item-for-loading-of-transport-loads"></a>Een menu-item maken voor het laden van transportladingen

U moet een nieuw menu-item maken waarmee transportladingen kunnen worden geladen. Met een transportlading kunt u werkregels groeperen van één of meer ladingen. Alles dat wordt toegevoegd aan de transportlading, kan vervolgens worden verzonden via een mobiele scanner.

1. Selecteer **Magazijnbeheer** \> **Instellen** \> **Mobiel apparaat** \> **Menuopties voor mobiel apparaat**.
2. Selecteer **Nieuw** en selecteer in het veld **Modus** de waarde **werk**.
3. Stel de optie **Bestaand werk gebruiken** in op **Ja**.
4. Selecteer op het tabblad **Algemeen** in het veld **Bestuurd door** de optie **Transportlading**.
5. Als u de bevestiging van de zending op een mobiele scanner wilt inschakelen, selecteert u in het veld **Toegestaan bevestigingstype verzending** de optie **Transportlading**.

## <a name="confirm-shipment-of-a-transport-load-from-the-client"></a>Verzending van een transportlading van de client bevestigen

Met deze instelling kunt u een transportlading bevestigen die een volledige of een gedeeltelijk lading omvat die moet worden verzonden.

1. Selecteer **Magazijnbeheer** \> **Ladingen** \> **Transportladingen**.
2. Selecteer in het actievenster op het tabblad **Verzenden en ontvangen** in de groep **Bevestigen** de optie **Transport**.
