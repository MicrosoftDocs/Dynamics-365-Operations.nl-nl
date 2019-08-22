---
title: Bronmogelijkheden definiëren
description: Resourcecapaciteiten beschrijven wat resources voor bedrijfsactiviteiten kunnen doen.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrCapability
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1ee6bfd06d7a38418812c2663695ab31701ef1ab
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843668"
---
# <a name="define-resource-capabilities"></a>Bronmogelijkheden definiëren

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

