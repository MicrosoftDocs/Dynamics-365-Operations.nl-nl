---
title: Wijzigingen bijhouden in wervingsgegevens
description: Met de functie voor procescontrole kunt u bijhouden wanneer kandidaten, vacatures of sollicitaties worden gewijzigd voor rapportage- of conformiteitsredenen.
author: tracykeya
manager: AnnBe
ms.date: 04/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: trkeya
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2019 update
ms.openlocfilehash: 448fceccb507bec5b60b686043a303c1997a9ac0
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742663"
---
# <a name="track-changes-in-recruiting-data"></a>Wijzigingen bijhouden in wervingsgegevens

U kunt wijzigingen bijhouden die zijn aangebracht in kandidaten, vacatures of sollicitaties met behulp van controleverwerking. Dit is handig om rapportage- of conformiteitsredenen.

U kunt de bijgehouden gegevens bekijken in Power BI met de OData-connector. Zie [Verbinding maken met OData-feeds in Power BI Desktop](https://docs.microsoft.com/power-bi/desktop-connect-odata) voor meer informatie.

## <a name="track-changes"></a>Wijzigingen bijhouden
Voer de volgende stappen uit om wijzigingen bij te houden in wervingsgegevens:

1. Selecteer de gewenste omgeving in [PowerApps](https://web.powerapps.com).

2. Selecteer **Instellingen** (het tandwielpictogram), kies **Geavanceerde aanpassingen** en selecteer vervolgens **Resources** onder **Resources voor ontwikkelaars**. 

3. Kopieer op de pagina **Resources voor ontwikkelaars** de waarde in het veld **Web API-waarde van exemplaar**. De waarde kan er bijvoorbeeld als volgt uitzien: https://yourorgname.api.crm.dynamics.com/api/data/v9.1/.

4. U kunt vervolgens een query uitvoeren op de gegevens vanuit een van de volgende entiteiten:
  - Vacaturehistorie (msdyn_jobopeninghistories)
  - Sollicitatiehistorie (msdyn_jobapplicationhistories) 
  - Kandidaathistorie (msdyn_candidatehistories)

## <a name="data-reported"></a>Gerapporteerde gegevens

De volgende gegevens zijn beschikbaar bij procescontrole.

| Gerapporteerde gegevens | Beschrijving |
| --- | --- |
| Gewijzigd door (msdyn_ChangedbyId) | Verwijzing naar gebruiker |
| Gemaakt op (createdon) |  Datum en tijdstip in UTC waarop de wijziging is doorgevoerd |
| Wijzigingstype (msdyn_changetype) | Welke wijziging is doorgevoerd |
| Algemene waarden voor kandidaten, vacatures <br></br>en sollicitaties | Gemaakt<br></br>Bijgewerkt |
| Sollicitatiehistorie | Artefact toegevoegd <br></br>Artefact verwijderd |
| Vacaturehistorie | TODO: bericht toegevoegd <br></br>TODO: bericht verwijderd <br></br>TODO: bericht bijgewerkt <br></br>TODO: deelnemer toegevoegd <br></br>TODO: deelnemer verwijderd |
| Kandidaathistorie | Artefact toegevoegd <br></br>Artefact verwijderd <br></br>Werkervaring toegevoegd <br></br>Werkervaring verwijderd <br></br>Opleiding toegevoegd <br></br>Opleiding verwijderd <br></br>Vaardigheid toegevoegd <br></br>Vaardigheid verwijderd <br></br>Label toegevoegd <br></br>Label verwijderd <br></br>Sociaal netwerk toegevoegd <br></br>Sociaal netwerk verwijderd <br></br>Persoonlijke gegevens toegevoegd <br></br>Persoonlijke gegevens bijgewerkt<br></br> |
| Gewijzigde velden (msdyn_changedfields) | In gewijzigde velden in de lijst met JSON-objecten worden mogelijk niet voor alle velden waarden opgeslagen.<br></br><br></br>Voor de wijzigingen "Gemaakt" en "Bijgewerkt" worden de velden in de gemaakte of gewijzigde record weergegeven.<br></br><br></br>Voor wijzigingen van het type "Toegevoegd" worden de velden in de onderliggende record weergegeven.<br></br><br></br>**Voorbeeld:**<br></br><br></br>{<br></br>  "msdyn_applyurl": { "newValue": "" },<br></br>  "msdyn_description": { "valueOmitted": true } <br></br>} |
|Sollicitatiehistorie | Sollicitatie (msdyn_JobapplicatonId)<br></br>Status (msdyn_status) <br></br>Reden van status (msdyn_statusreason) <br></br>Reden voor afwijzing (msdyn_rejectionreason) |
| Vacaturehistorie | Vacature (msdyn_JobopeningId) <br></br>Status (msdyn_jobopeningstatus) <br></br>Reden van status (msdyn_jobopeningstatusreason) |
| Kandidaathistorie | Kandidaat (msdyn_CandidateId) |
