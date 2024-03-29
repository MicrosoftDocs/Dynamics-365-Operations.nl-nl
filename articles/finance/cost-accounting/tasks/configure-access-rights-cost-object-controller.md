---
title: Toegangsrechten configureren voor een controller voor kostenobjecten
description: Gebruik deze procedure om toegangsrechten te configureren voor een controller voor kostenobjecten.
author: kfend
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 17615ff70c15789ac30223464b20ccd61a1bad55
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710625"
---
# <a name="configure-access-rights-for-a-cost-object-controller"></a>Toegangsrechten configureren voor een controller voor kostenobjecten

[!include [banner](../../includes/banner.md)]

Gebruik deze procedure om toegangsrechten te configureren voor een controller voor kostenobjecten. Deze registratie gebruikt het USP2-demogegevensbedrijf.


## <a name="assign-the-cost-object-controller-role"></a>De rol van controller voor kostenobjecten toewijzen
1. Ga naar Systeembeheer > Gebruikers > Gebruikers.
2. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het veld Gebruikers met een waarde van 'alicia'.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Klik op Rollen toewijzen.
5. Zoek en selecteer de gewenste record in de lijst.
6. Klik op OK.

## <a name="enable-access-list-security"></a>Toegangslijstbeveiliging inschakelen
1. Ga naar Kostprijsboekhouding > Dimensies > Dimensiehiërarchieën.
2. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer Organisatie.  
3. Klik op Bewerken.
4. Selecteer Ja in het veld Hiërarchie van toegangslijsten.
5. Klik op Hiërarchie weergeven.

## <a name="assign-access-rights-to-user"></a>Toegangsrechten toewijzen aan gebruiker
1. Klik op Nieuw.
2. Markeer in de lijst de geselecteerde rij.
3. Typ of selecteer een waarde in het veld Gebruikers-id.
    * Selecteer Beheer.  
4. Selecteer in de structuur 'Organisatie\CEO\CFO\FIM'.
5. Klik op Nieuw.
6. Markeer in de lijst de geselecteerde rij.
7. Typ of selecteer een waarde in het veld Gebruikers-id.
    * Selecteer Alicia.  
8. Klik op Opslaan.

## <a name="enable-access-rights-in-cost-accounting"></a>Toegangsrechten inschakelen in kostprijsboekhouding
1. Ga naar Kostprijsboekhouding > Instellen > Parameters.
2. Klik op het tabblad Algemeen.
3. Selecteer Ja in het veld Weergavetoegang voor dimensieleden voor kostenobject inschakelen.
4. Klik op Opslaan.
5. Sluit de pagina.
6. Ga naar Kostprijsboekhouding > Instellen > Configuratie van werkgebied voor kostenbeheer.
7. Klik op Bewerken.
8. Selecteer Ja in het veld Gepubliceerd.
    * Als u Ja selecteert, kan een gebruiker die aan een van de volgende vier rollen is toegewezen, de rapporten zien in het werkgebied voor kostenbeheer: accounting manager, kostenaccountant, assistent kostenaccountant en controller voor kostenobjecten. Als u Nee selecteert, kan alleen een gebruiker die aan een van de volgende rollen is toegewezen, de rapporten zien: manager van kostprijsboekhouding, kostenaccountant en assistent kostenaccountant.    
9. Klik op Opslaan.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
