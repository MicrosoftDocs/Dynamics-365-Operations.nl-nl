---
title: Een werksjabloon instellen voor inkooporders
description: In dit onderwerp wordt beschreven hoe u een eenvoudige werksjabloon instelt die u kunt gebruiken wanneer u ontvangen artikelen wegzet.
author: ShylaThompson
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9acf6db9138a009527c6662f1cbb7e5fedc8778
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976858"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a>Een werksjabloon instellen voor inkooporders

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een eenvoudige werksjabloon instelt die u kunt gebruiken wanneer u ontvangen artikelen wegzet. Werksjablonen bepalen de reeks instructies die op een mobiel apparaat aan de magazijnmedewerker worden voorgesteld wanneer deze artikelen van het ontvangende gebied verplaatst. U kunt deze procedure gebruiken met de opgegeven gegevens van het demogegevensbedrijf USMF. Maak voordat u deze guide start een werkgroep-id. In dit voorbeeld wordt een werkgroep-id met de naam Binnenkomend gebruikt. Deze procedure is bedoeld voor de magazijnbeheerder.

1. Ga in het navigatievenster naar **Modules > Magazijnbeheer > Instellingen > Werk >Werksjablonen**.
2. Selecteer **Inkooporders** in het veld **Werkordertype**.

## <a name="create-a-work-template-header"></a>Een koptekst van een werksjabloon maken
1. Selecteer **Nieuw**.
2. Typ een getal in het veld **Volgnummer**. Dit is de volgorde waarin de werksjablonen worden beoordeeld. U kunt de volgorde wijzigen, als dat nodig is.  
3. Typ een waarde in het veld **Werksjabloon**. Dit is de unieke identificatie voor deze sjabloon.  
4. Typ een waarde in het veld **Omschrijving van werksjabloon**.
    - De optie **Geldig** wordt niet ingeschakeld voordat u alle informatie die voor de sjabloon vereist is, hebt ingevuld en vervolgens op **Opslaan** hebt geklikt.  
    - Een werkorder van het type **Inkooporder** kan niet automatisch worden verwerkt, dus laat de optie **Automatisch verwerken** ingesteld op **Nee**.  
5. Typ een waarde in het veld **Werkgroep-id**. Met werkgroep-id's kunt u werk in groepen organiseren. De waarde die u hier instelt, wordt de standaardwaarde voor elk werk dat met deze sjabloon wordt gemaakt.  
6. Typ `1` in het veld **Werkprioriteit**. Dit geeft het belang van het werk aan. De waarde die u hier instelt, wordt de standaardwaarde voor elk werk dat met deze sjabloon wordt gemaakt.  
7. Selecteer **Opslaan**. U moet de koptekst van de werksjabloon opslaan voordat de knop **Query bewerken** beschikbaar wordt.  

## <a name="set-up-the-query-for-the-work-template"></a>De query voor de werksjabloon instellen
1. Selecteer **Query bewerken**. We zullen een beperking instellen zodat de sjabloon alleen in een specifiek magazijn kan worden gebruikt.  
2. Selecteer **Toevoegen**.
3. Typ `warehouse` in het veld **Veld**.
4. Typ een waarde in het veld **Criteria**.
5. Selecteer **OK**.
6. Selecteer **Ja**.

## <a name="set-work-template-details"></a>Werksjabloongegevens instellen
1. Selecteer **Nieuw**.
2. Selecteer **Verzamelen** in het veld **Werktype**.
3. Typ `purchase` in het veld **Werkklasse-id**. De werkklasse die u hier instelt, wordt de standaardwaarde op alle werkregels van type orderverzameling die met deze sjabloon worden gemaakt. De werkklasse kan niet worden overschreven via de werkorderregels. Werkklassen worden gebruikt om het type werkorderregels te bepalen en/of beperken dat een magazijnmedewerker op een mobiel apparaat kan verwerken.  
4. Selecteer **Nieuw**.
5. Selecteer **Wegzetten** in het veld **Werktype**.
6. Typ een waarde in het veld **Werkklasse-id**. De instructies voor verzamelen en neerzetten zijn ingesteld. Elk verzamel-/wegzetpaar moeten dezelfde werkklasse hebben. Gebruik dezelfde werkklasse die u voor de instructie voor verzamelen hebt geleverd.  
7. Selecteer **Opslaan**. Het selectievakje **Geldig** is nu ingeschakeld.  

