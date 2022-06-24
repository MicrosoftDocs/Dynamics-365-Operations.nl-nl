---
title: Registratie voor Productieregistratie-uitvoering
description: In dit artikel worden belangrijke concepten en termen beschreven, die u moet kennen om de productieregistratie te configureren en te gebruiken.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgRegistration
audience: Application User
ms.reviewer: kamaybac
ms.custom: 70103
ms.assetid: 52ba1cdd-767f-4edd-896f-61adce8479d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c43a9d847045f2c029f232d6317268d91ee0129a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907198"
---
# <a name="registration-for-manufacturing-execution"></a>Registratie voor Productieregistratie-uitvoering

[!include [banner](../includes/banner.md)]

In dit artikel worden belangrijke concepten en termen beschreven, die u moet kennen om de productieregistratie te configureren en te gebruiken. 

De functie Productie-uitvoering is voornamelijk bedoeld voor gebruik door productiebedrijven. Werknemers kunnen tijd- en artikelverbruik registreren voor productietaken via de pagina **Taakregistratie**. Alle geregistreerde gegevens moeten worden goedgekeurd en later overgebracht naar de relevante modules. Omdat er doorlopend geregistreerde gegevens worden goedgekeurd en overgebracht, kunnen managers gemakkelijk de werkelijke kosten van productieorders bijhouden.

## <a name="manufacturing-execution-and-registration-terminology"></a>Terminologie van productie-uitvoering en -registratie
De volgende tabel bevat termen die betrekking hebben op de productie-uitvoering en bijbehorende registratietaken.

| Voorwaarde                          | Omschrijving                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Productieregistratie       | Een functie die wordt gebruikt om tijd, materiaalverbruik, kosten van productietaken, projecten en indirecte activiteiten te registreren. Registratie wordt uitgevoerd in een client voor productie-uitvoeringsregistratie.                                                                                                                                                                                                                                                                                                                                                                                                   |
| Taaklijst                      | Op de pagina **Taakregistratie** krijgen werknemers de lijst met taken te zien die ze moeten uitvoeren voor een specifieke bron, zoals een machine. Een werknemer kan tijd- en artikelverbruik registreren voor elke klus of taak in de takenlijst.                                                                                                                                                                                                                                                                                                                                                                           |
| Bundeling van taken                  | Als een werknemer meer dan een taak tegelijk start op de pagina **Taakregistratie**, wordt dit ´bundeling van taken´ genoemd. De tijd die aan gebundelde taken wordt besteed, kan op verschillende manieren aan de afzonderlijke taken worden toegewezen met toewijzingssleutels.                                                                                                                                                                                                                                                                                                                                                         |
| Registratie van leider of assistent | Een werknemer kan zich registreren als assistent van een bron en kan een klein team samenstellen waarin meerdere werknemers werken aan dezelfde productietaken. Bronnen waaraan werknemers zijn verbonden als assistenten, worden ´leiders´ genoemd. Alleen de bron die leider is, moet de gegevens registreren. Alle assistenten krijgen automatisch dezelfde geregistreerde gegevens toegewezen. Als bijvoorbeeld een machine functioneert als de leider, kunnen werknemers die zijn geregistreerd als assistenten van die machine, gegevens registreren op de pagina **Taakregistratie**. Zowel de machine als de werknemers die daaraan als assistenten zijn verbonden, ontvangen dezelfde geregistreerde gegevens. |
| Indirecte activiteit             | Een activiteit of taak die geen rechtstreeks verband houdt met een productietaak of project, zoals een afdelingsvergadering, een schoonmaaktaak of een onderhoudstaak in de werkplaats. Werknemers kunnen voor indirecte activiteiten op dezelfde manier gegevens registreren als voor productietaken en projecten.                                                                                                                                                                                                                                                                                                |

## <a name="registrations-in-manufacturing-execution"></a>Gegevens registreren voor de productie-uitvoering
Werknemers kunnen in het kader van de productie-uitvoering verschillende typen gegevens registreren voor werk dat is uitgevoerd tijdens productietaken. Afhankelijk van de instellingen van het systeem kunnen werknemers ook gegevens te registreren voor projectactiviteiten en niet-productieve taken, zoals pauzes, afwezigheid en indirecte activiteiten. De volgende typen gegevens kunnen worden geregistreerd:

-   **Inklokken en uitklokken** (beschikbaar bij tijd en aanwezigheid) - Werknemers klokken in wanneer ze op het werk aankomen en klokken uit wanneer ze naar huis gaan.
-   **Registratie van productietaken** - Werknemers kunnen gegevens registreren met betrekking tot zijn of haar taken, zoals de begintijd van een taak en feedback voor een taak, bij de productietaken die in hun takenlijst worden weergegeven. Werknemers kunnen meerdere taken tegelijkertijd starten. Dit wordt bundeling van taken genoemd.
-   **Registratie van voorraad** - Werknemers kunnen gegevens registreren van materialen die zijn gebruikt in de werkplaats, maar die niet direct te maken hebben met productietaken. Voorbeelden zijn vet, smeermiddelen of andere materialen die worden gebruikt om ervoor te zorgen dat de machines goed blijven werken. De registratie wordt uitgevoerd in een voorraadjournaal.
-   **Registreren op projecten** (beschikbaar bij tijd en aanwezigheid) - Werknemers kunnen registraties, zoals de start en het einde van werk aan projecten of projectactiviteiten, maken die in hun takenlijst worden weergegeven.
-   **Bijzondere projectkosten en projectartikelen registreren** (beschikbaar bij tijd en aanwezigheid) - Werknemers kunnen kosten (onkosten) registreren die gekoppeld zijn aan een project in een projectkostenjournaal, zoals reiskosten en tol. Werknemers kunnen ook artikelverbruik voor projecten registreren. Hiervoor wordt gebruikgemaakt van een projectartikeljournaal.
-   **Zich registreren als assistent van een andere werknemer** - Als twee of meer werknemers willen samenwerken aan een productietaak of project, kan een werknemer zich registreren als assistent van een machine of andere werknemer, die fungeert als de leider. Indien nodig, kan de leider een andere werknemer als leider selecteren.
-   **Verzuim registreren** (beschikbaar bij tijd en aanwezigheid) - Werknemers kunnen tijd registreren voor diverse verzuimcodes die zijn ingesteld. Afwezigheid kan worden aangeduid als een werknemer te laat komt, afwezigheid nodig heeft tijdens de werkdag of eerder weggaat dan verwacht op basis van het standaardwerktijdprofiel.
-   **Pauzes registreren** (beschikbaar bij tijd en aanwezigheid) - Tijdens de werkdag kunnen werknemers registreren dat ze hun werkstation verlaten voor pauze. Er kunnen diverse typen pauze worden ingesteld. Als een werknemer terugkomt en zich opnieuw aanmeldt, registreert het systeem dat de werknemer terug is en wordt de pauzeregistratie gestopt.
-   **Indirecte activiteiten registreren** (beschikbaar bij tijd en aanwezigheid) - Indirecte activiteiten zijn niet-productieve activiteiten die werknemers tijdens een werkdag kunnen uitvoeren, zoals een afdelingsvergadering, teamoverleg of onderhoudstaak die in de werkplaats wordt uitgevoerd. Werknemers kunnen gegevens registreren voor de indirecte activiteiten die zijn ingesteld.
-   **Overwerk registreren** (beschikbaar bij tijd en aanwezigheid) - Werknemers die zijn aangevraagd om overuren te werken kunnen selecteren of de extra uren moeten worden geregistreerd als flexwerk of als overwerk.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]