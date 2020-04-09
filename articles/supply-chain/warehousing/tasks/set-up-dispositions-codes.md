---
title: Beschikkingscodes instellen
description: Deze procedure is gericht op de instelling van een beschikkingscode die op een mobiel apparaat kan worden gebruikt voor het ontvangstproces van retourorders.
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec353ecffdc457e1502cfad24e7a50ae31048647
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146049"
---
# <a name="set-up-dispositions-codes"></a>Beschikkingscodes instellen

[!include [banner](../../includes/banner.md)]

Deze procedure is gericht op de instelling van een beschikkingscode die op een mobiel apparaat kan worden gebruikt voor het ontvangstproces van retourorders. Beschikkingscodes zijn een verzameling regels die kunnen worden gebruikt wanneer artikelen worden ontvangen. Bijvoorbeeld, wanneer een werkgebruiker een mobiel apparaat gebruikt om artikelen te ontvangen die beschadigd zijn, moet de gebruiker een beschikkingscode voor de beschadigde artikelen scannen. De voorraadstatus van de ontvangen goederen, de werksjabloon en de locatierichtlijn kan worden bepaald aan de hand van de gescande beschikkingscode. Voor het inkooporderontvangstproces en het productieordergereedmeldproces is het gebruik van een beschikkingscode optioneel. Voor het ontvangstproces van verkooporderretouren is het gebruik van een beschikkingscode, als de artikelen met een mobiel apparaat worden geregistreerd, verplicht.  Deze taakbegeleiding is gemaakt met het demogegevensbedrijf USMF. Deze procedure is bedoeld voor de magazijnbeheerder. 

1. Ga naar Magazijnbeheer > Instellingen > Mobiel apparaat > Beschikkingscodes.
2. Klik op Nieuw.
    * Maak een nieuwe beschikkingscode om te gebruiken voor klantretouren.  
3. Typ een waarde in het veld Beschikkingscode.
4. Selecteer in het veld Voorraadstatus een voorraadstatus waar er voorraadblokkering is.
    * Als u USMF workflow gebruikt, selecteert u 'Blokkeren'. U kunt een voorraadstatus aan de beschikkingscode toevoegen om de standaardstatus op de orderregels te overschrijven.  
5. Typ een waarde in het veld Werksjabloon.
    * Optioneel: selecteer een werksjablooncode die aan een retourorder is gekoppeld. Als geen waarde is opgegeven, wordt de werksjabloon opgelost met de standaardregels die in uw systeem zijn geconfigureerd. Een werksjabloon selecteren beperkt de processen waarmee deze beschikkingscode kan worden gebruikt. Als een beschikkingscode bijvoorbeeld een werksjabloon met een werkorder van het type inkooporder heeft, kan deze niet worden gebruikt om artikelen te registreren die door klanten worden geretourneerd.  
6. Typ een waarde in het veld Beschikkingscode retourneren.
    * De retourbeschikkingscode definieert de rest van het retourorderproces voor de geregistreerde artikelen. In dit voorbeeld moet de klant een creditnota ontvangen. Voeg een retourbeschikkingscode toe die een actiecredit bevat.  

