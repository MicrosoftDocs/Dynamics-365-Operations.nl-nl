---
title: Magazijnwerk voor afhandeling van uitzonderingen annuleren
description: In dit artikel wordt de functie Werk annuleren beschreven waarmee magazijnsupervisors geblokkeerd werk kunnen verwerken.
author: Mirzaab
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9a5c0cc988141b102cf3659ab4599e025f8f4640
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907169"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a>Magazijnwerk voor afhandeling van uitzonderingen annuleren

[!include [banner](../includes/banner.md)]

Met de functie Werk annuleren in Microsoft Dynamics 365 Supply Chain Management kan de beheerdergebruiker specifieke magazijnwerkzaamheden annuleren die momenteel worden uitgevoerd, maar die worden geblokkeerd door het systeem of niet kunnen worden voltooid vanwege uitzonderlijke omstandigheden. Deze functionaliteit is een aantrekkelijk en veilig alternatief voor SQL-herstelscripts waarmee inconsistente gegevens worden gecorrigeerd. Terwijl deze scripts echter meestal worden aangevraagd bij IT-professionals, kan de functie Werk annuleren worden gebruikt door gebruikers in het bedrijf die beheerdersrechten hebben.

U kunt toegang krijgen tot de functie Werk annuleren via **Magazijnbeheer** \> **Periodieke taken** \> **Opschonen \> Werk annuleren**. Geef in het dialoogvenster **Werk annuleren** de werk-id op van de werkzaamheden die u wilt annuleren en selecteer vervolgens **OK**.

## <a name="warehouse-work-that-can-be-canceled"></a>Magazijnwerk dat kan worden geannuleerd

Tijdens orderverzameling in magazijnen kan een werknemer situaties tegenkomen waarbij hoeveelheden die afkomstig zijn van een opslaglocatie zijn geregistreerd naar hun gebruikerlocatie, maar de wegzetbewerking niet kan worden geregistreerd. Inconsistente magazijngegevens zijn vaak, maar niet altijd, de reden waarom werk wordt geblokkeerd.

In tegenstelling tot de normale annuleringsfunctionaliteit die toegankelijk is via de knop **Annuleren** in de werkkoptekst, hoeft bij de functie Werk annuleren de als laatste voltooide werkregel geen werkregel van het type **wegzetten** te zijn. Met andere woorden, bij de functie Werk annuleren kan de annuleringslogica ook worden uitgevoerd als de artikelhoeveelheid op een werkregel zich op een gebruikerslocatie bevindt.

> [!NOTE]
> Voor werk dat om operationele redenen moet worden geannuleerd, moeten magazijngebruikers de normale annuleringsfunctionaliteit op de werkpagina blijven gebruiken.

Alleen werk van het type **Verkoop**, **Overboekingsuitgifte**, **Orderverzameling van grondstoffen** of **Aanvulling** kan worden geannuleerd met de functie Werk annuleren. De annuleringslogica wordt niet uitgevoerd voor orderverzameling van bevroren grondstoffen of werk dat kan worden geannuleerd met behulp van de normale functie Annuleren (zie de voorgaande opmerking).

Om het werk te deblokkeren, worden eventuele resterende werkregels door het systeem geannuleerd en worden de magazijngegevens hersteld die aan de werk-id zijn gekoppeld die de gebruiker heeft opgegeven. Normale magazijnverwerkingsactiviteiten voor de desbetreffende artikelhoeveelheid kunnen vervolgens worden hervat.

Als u het desbetreffende artikel op een specifieke locatie wilt neerzetten nadat het werk is geannuleerd, moet de gebruiker een voorraadmutatie of hoeveelheidcorrectie gebruiken op een mobiel apparaat.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]