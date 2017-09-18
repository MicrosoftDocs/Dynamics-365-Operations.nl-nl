--- 
title: Een inkoopbeleid maken
description: Deze procedure laat zien hoe u aanschafbeleid kunt maken voor afstemming met uw bedrijfsprocessen voor inkoop.
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 51486712d732bba064fd6c9b64dbccb730603877
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="create-purchasing-policies"></a>Een inkoopbeleid maken

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u aanschafbeleid kunt maken voor afstemming met uw bedrijfsprocessen voor inkoop. Voordat u een inkoopbeleid kunt maken, moet u de parameters van het aanschafbeleid instellen. Het is mogelijk om een aanschafbeleid te maken, te wijzigen en in te trekken, maar u kunt een aanschafbeleid niet verwijderen. Deze procedure wordt meestal uitgevoerd door een inkoopmanager. U kunt deze procedure gebruiken met het demogegevensbedrijf USMF of met uw eigen gegevens.


## <a name="set-up-policy-parameters"></a>Beleidsparameters instellen
1. Ga naar Inkoopbeleid.
2. Klik op Parameters.
    * Beleidsprioriteitsregels gelden op verschillende niveaus in uw organisatie. De organisatie-eenheden die worden weergegeven, zijn afhankelijk van uw organisatiehiërarchie en van de niveaus in de hiërarchie waaraan het doel van Interne inkoopcontrole is toegewezen. Zo kan uw organisatie bijvoorbeeld rechtspersonen, kostenplaatsen, regio's en afdelingen bevatten, terwijl slechts enkele daarvan het hiërarchiedoel Interne inkoopcontrole hebben. Standaard is de organisatie van het type Bedrijf beschikbaar.  
3. Klik op het tabblad Beleidsregeltypeparameters.
4. Selecteer 'Beheerregel Inkoopbeleid\Opdracht tot Inkoop' in de structuur.
    * U definieert de voorrangsvolgorde voor beleidsoplossing op beleidsniveau. Voor sommige beleidstypen kunt u echter de voorrangsvolgorde voor individuele beleidsregeltypen overschrijven. Zo kunt u bijvoorbeeld de volgorde van prioriteit voor inkoopbeleid definiëren als: kostenplaats, afdeling, bedrijf. Voor de catalogusbeleidsregel wilt u mogelijk de volgende volgorde van prioriteit: afdeling, kostenplaats, bedrijf. U kunt de volgorde van prioriteit alleen wijzigen voor de catalogusbeleidsregel. Wanneer een medewerker een bestelopdracht maakt, wordt de weergegeven catalogus bepaald door het beleid dat is gekoppeld aan de afdeling van de medewerker en vervolgens aan de kostenplaats en het bedrijf van de medewerker.  
    * Als er meer dan één organisatorisch niveau is aangegeven, kunt u de pijlen omhoog/omlaag gebruiken om de prioriteitsvolgorde in te stellen voor de beheerregel voor opdracht tot inkoop.  
5. Sluit de pagina.

## <a name="create-a-new-policy"></a>Een nieuw beleid maken
1. Klik op Nieuw.
2. Typ een waarde in het veld Naam.
3. Typ een waarde in het veld Omschrijving.
    * Een enkel aanschafbeleid kan uitsluitend op één organisatiehiërarchie betrekking hebben. Zo kunt u bijvoorbeeld,één hiërarchie hebben genaamd "Geografisch" en een andere genaamd "Afdeling", die beide een ander aanschafbeleid hebben.  
    * Selecteer een organisatie waarop het beleid van toepassing moet zijn.  
4. Klik op de pijl om de geselecteerde organisatie toe te voegen.
    * U kunt dit proces herhalen om meer organisaties toe te voegen.  

## <a name="add-a-policy-rule"></a>Een beleidsregel toevoegen
1. Selecteer in de lijst Beleidsregeltype de optie Regel voor bestelopdrachtdoelen.
    * U kunt een regel maken waarmee het doel van de standaardbestelopdracht wordt ingesteld op het type Verbruik, maar waarbij in plaats daarvan ook het aanvullingstype kan worden geselecteerd.  
2. Klik op Beleidsregel maken.
3. Selecteer Ja in het veld Handmatig overschrijven toestaan.
4. Klik op Sluiten.
    * Nu kunt u beleidsregels instellen voor het aanschafbeleid.   Merk op dat een type beleidsregel geen overlappende regels kan hebben die tegelijkertijd actief zijn binnen een enkel inkoopbeleid.  
5. Sluit de pagina.
6. Sluit de pagina.

