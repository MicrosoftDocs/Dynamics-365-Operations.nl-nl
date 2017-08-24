--- 
title: Een werksjabloon instellen voor inkooporders
description: Deze procedure is gericht op de instelling van een eenvoudige werksjabloon die u kunt gebruiken wanneer u ontvangen artikelen wegzet.
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bibis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: aa561d558827e78529ef797b6df6dd3c1dcce34d
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-a-work-template-for-purchase-orders"></a>Een werksjabloon instellen voor inkooporders

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure is gericht op de instelling van een eenvoudige werksjabloon die u kunt gebruiken wanneer u ontvangen artikelen wegzet. Werksjablonen bepalen de reeks instructies die op een mobiel apparaat aan de magazijnmedewerker worden voorgesteld wanneer deze artikelen van het ontvangende gebied verplaatst. U kunt deze procedure gebruiken met de opgegeven gegevens van het demogegevensbedrijf USMF. Maak voordat u deze handleiding start een werkgroep-id. In dit voorbeeld wordt een werkgroep-id met de naam Binnenkomend gebruikt. Deze procedure is bedoeld voor de magazijnbeheerder.

1. Ga naar Magazijnbeheer > Instellingen > Werk > Werksjablonen.
2. Selecteer 'Inkooporders' in het veld Werkordertype.

## <a name="create-a-work-template-header"></a>Een koptekst van een werksjabloon maken
1. Klik op Nieuw.
2. Voer een getal in het veld Volgnummer in.
    * Dit is de volgorde waarin de werksjablonen worden beoordeeld. U kunt de volgorde wijzigen, als dat nodig is.  
3. Typ een waarde in het veld Werksjabloon.
    * Dit is de unieke identificatie voor deze sjabloon.  
4. Typ een waarde in het veld Omschrijving van werksjabloon.
    * De optie Geldig wordt niet ingeschakeld voordat u alle informatie die door de sjabloon is vereist hebt ingevuld en vervolgens op Opslaan hebt geklikt.  
    * Een werkorder van het type inkooporder kan niet automatisch worden verwerkt, dus laat de optie Automatisch verwerken ingesteld op Nee.  
5. Typ een waarde in het veld Werkgroep-id.
    * Met werkgroep-id's kunt u werk in groepen organiseren. De waarde die u hier instelt, wordt de standaardwaarde voor elk werk dat met deze sjabloon wordt gemaakt.  
6. Typ '1' in het veld Werkprioriteit.
    * Dit geeft het belang van het werk aan. De waarde die u hier instelt, wordt de standaardwaarde voor elk werk dat met deze sjabloon wordt gemaakt.  
7. Klik op Opslaan.
    * U moet de koptekst van het werksjabloon opslaan voordat de knop bewerken-query beschikbaar wordt.  

## <a name="set-up-the-query-for-the-work-template"></a>De query voor de werksjabloon instellen
1. Klik op Query bewerken.
    * We zullen een beperking instellen zodat de sjabloon alleen in een specifiek magazijn kan worden gebruikt.  
2. Klik op Toevoegen.
3. Markeer in de lijst de geselecteerde rij.
4. Typ 'magazijn' in het veld Veld.
5. Typ een waarde in het veld Criteria.
6. Klik op OK.
7. Klik op Ja.

## <a name="set-work-template-details"></a>Werksjabloongegevens instellen
1. Klik op Nieuw.
2. Selecteer 'Verzamelen' in het veld Werktype.
3. Typ 'inkoop' in het veld Werkklasse-id.
    * De werkklasse die u hier instelt, wordt de standaardwaarde op alle werkregels van type orderverzameling die met deze sjabloon worden gemaakt. De werkklasse kan niet worden overschreven via de werkorderregels. Werkklassen worden gebruikt om het type werkorderregels te bepalen en/of beperken dat een magazijnmedewerker op een mobiel apparaat kan verwerken.  
4. Klik op Nieuw.
5. Selecteer 'Wegzetten' in het veld Werktype.
6. Typ een waarde in het veld Werkklasse-id.
    * De instructies voor verzamelen en neerzetten zijn ingesteld. Elk verzamel-/wegzetpaar moeten dezelfde werkklasse hebben. Gebruik dezelfde werkklasse die u voor de instructie voor verzamelen hebt geleverd.  
7. Klik op Opslaan.
    * Het selectievakje Geldig is nu ingeschakeld.  


