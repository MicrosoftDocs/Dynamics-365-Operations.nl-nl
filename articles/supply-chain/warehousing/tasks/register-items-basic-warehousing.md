--- 
title: Artikelen registreren voor een artikel waarvoor basaal magazijnbeheer mogelijk is met een artikelontvangstjournaal
description: Deze procedure toont hoe u artikelen registreert via het artikelontvangstjournaal wanneer u "basale magazijnen" gebruikt in de module Voorraadbeheer.
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 809a1466b0f4674f503bc654175d8f94b37a6508
ms.openlocfilehash: c7148bd807ef29b0dd89204a0fbe9b8480095aba
ms.contentlocale: nl-nl
ms.lasthandoff: 11/02/2017

---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-arrival-journal"></a>Artikelen registreren voor een artikel waarvoor basaal magazijnbeheer mogelijk is met een artikelontvangstjournaal

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure toont hoe u artikelen registreert via het artikelontvangstjournaal wanneer u "basale magazijnen" gebruikt in de module Voorraadbeheer. Dit wordt gewoonlijk uitgevoerd door een ontvangstadministrateur. U kunt deze procedure uitvoeren in het demobedrijf USMF met de voorbeeldwaarden die worden weergegeven.  Als u geen gebruikmaakt van USMF, hebt u een bevestigde inkooporder nodig met een openstaande inkooporderregel voordat u deze handleiding start. Het artikel op de regel moet in voorraad zijn opgeslagen, er mogen geen productvarianten worden gebruikt en het mag geen traceringsdimensies hebben. En het artikel moet zijn gekoppeld aan een opslagdimensiegroep, waarbij site en magazijn actief zijn.


## <a name="create-item-arrival-journal-header"></a>Koptekst voor artikelontvangstjournaal maken
1. Ga naar Voorraadbeheer > Journaalposten > Artikelontvangst > Artikelontvangst.
2. Klik op Nieuw.
3. Typ een waarde in het veld Naam.
    * Als u USMF gebruikt, kunt u WHS typen. Als u andere gegevens gebruikt, moet het journaal waarvan u de naam kiest de volgende eigenschappen hebben: Orderverzamellocatie controleren moet zijn ingesteld op Nee en Quarantainebeheer moet zijn ingesteld op Nee.  
4. Typ een waarde in het veld Pakbon.
    * Dit is de pakbon-id van de pakbon die door de leverancier is uitgegeven. Voeg een uniek nummer toe.  
5. Selecteer de inkooporder in het veld Nummer.
6. Klik op OK.

## <a name="add-lines-to-item-arrival-journal"></a>Regels toevoegen aan artikelontvangstjournaal
1. Klik op Functies.
2. Klik op Regels maken.
    * De regels kunnen handmatig in dit journaal worden ingevoerd of automatisch worden gemaakt. Hier ziet u hoe deze automatisch kunnen worden gemaakt.  
3. Schakel het selectievakje Hoeveelheid initialiseren in of uit.
    * Hiermee wordt de hoeveelheid op de journaalregels geïnitialiseerd met de hoeveelheid die niet is geregistreerd vanaf de inkooporderregel.  
4. Klik op OK.

## <a name="post-the-journal"></a>Het journaal boeken
1. Klik op Boeken.
2. Klik op OK.

## <a name="generate-the-product-receipt"></a>De productontvangst genereren
1. Klik op Functies.
2. Klik op Productontvangstbon.
3. Klik op OK.


