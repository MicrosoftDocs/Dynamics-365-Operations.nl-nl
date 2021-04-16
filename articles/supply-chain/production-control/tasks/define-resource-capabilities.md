---
title: Bronmogelijkheden definiëren
description: Resourcecapaciteiten beschrijven wat resources voor bedrijfsactiviteiten kunnen doen.
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WrkCtrCapability
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 072991e7b3844ad3583b7d0c575d426299f74e9f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828701"
---
# <a name="define-resource-capabilities"></a>Bronmogelijkheden definiëren

[!include [banner](../../includes/banner.md)]

Resourcecapaciteiten beschrijven wat resources voor bedrijfsactiviteiten kunnen doen. Tijdens het plannen worden de vereisten van elke taak en bewerking vergeleken met de capaciteiten van de beschikbare resources. Deze taakbegeleiding helpt u een resourcecapaciteit te maken en deze toe te wijzen aan een resource. Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF.


## <a name="create-a-resource-capability"></a>Een resourcecapaciteit maken
1. Ga naar Bronmogelijkheden.
2. Klik op Nieuw.
3. Typ in het veld Mogelijkheid de ID van de bronmogelijkheid.
    * Voor een bepaalde bewerking gebruikt u de capaciteits-id om de resources op te geven die deze capaciteit moeten hebben om de bewerking uit te voeren.  
4. Voer in het veld Omschrijving een omschrijving van de mogelijkheid in.

## <a name="assign-capability-to-a-resource"></a>Capaciteit aan een resource toewijzen
1. Klik op Toevoegen.
2. Typ in het veld Bron de ID van de bron.
    * Een resourcecapaciteit kan aan een of meer resources zijn toegewezen.  
3. Voer in het veld Vervaldatum een datum in.
    * U kunt dit veld gebruiken om te specificeren dat een resource de capaciteit voor een beperkte tijd heeft.  
4. Voer een getal in het veld Prioriteit in.
    * Wanneer u taken en bewerkingen plant, kunt u opgeven of u resources op prioriteit wilt selecteren. Als u dit kiest, en er meer dan één resource de taak of de bewerking op de gevraagde datum kan uitvoeren, wordt de resource met de laagste prioriteit met betrekking tot de vereiste capaciteit geselecteerd.  
5. Voer een nummer in het veld Niveau in.
    * Wanneer u opgeeft dat een taak of bewerking een bepaalde capaciteit vereist, kunt u ook het minimum niveau opgeven dat nodig is. Gebruik het capaciteitsniveau om resources te onderscheiden die dezelfde taak kunnen uitvoeren, maar met verschillende snelheden, sterke punten, grootte, enzovoort.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]