---
title: Experimenten in Dynamics 365 Commerce
description: Met experimenten kunt u ook behandelingen van pagina-indelingen en inhoud in Site Builder maken, bewerken en beheren. Complete ondersteuning van experimenten is ingeschakeld voor e-Commerce-pagina's en -entiteiten binnen een pagina.
author: sushma-rao
ms.date: 06/07/2022
ms.topic: overview
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 1ef877072ba7ffe1b0326cf8d526b512b5ab30b8
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946199"
---
# <a name="experimentation-in-dynamics-365-commerce"></a>Experimenten in Dynamics 365 Commerce
Gebruik experimenten in Dynamics 365 Commerce om hypotheses te valideren met betrekking tot de effectiviteit van uw e-Commerce-pagina's en om beslissingen te nemen over de op gegevens gebaseerde betrouwbaarheid. Commerce ondersteunt A/B-tests op pagina's, modules en fragmenten en stelt u in staat om de invloed van voorgestelde wijzigingen op uw website te meten.

U kunt pagina- en inhoudsbehandelingen, die **variaties** worden genoemd, in Commerce Site Builder maken, bewerken en beheren. Commerce wordt geïntegreerd met services van derden waarmee u experimenten en behandelingstoewijzingen kunt maken. Realtime gebeurtenisstromen die in Commerce zijn vastgelegd, maken de analyse mogelijk waarmee de resultaten van het experiment in de service van derden worden gedefinieerd. U kunt deze analyse vervolgens gebruiken om uw hypotheses te ondersteunen of te bestrijden.

## <a name="set-up-prerequisites"></a>Instellingsvereisten

1. **De juiste versie van Commerce ophalen**: voer een upgrade op uw modulebibliotheek, SDK (Software Development Kit) voor uitbreidbaarheid van online afzetkanalen en Commerce Scale Unit uit naar Commerce versie 10.0.13 of hoger.
1. **Een experimentconnector instellen**: met een experimentconnector kan Commerce verbinding maken met services van derden om de lijst met experimenten op te halen en te bepalen wanneer een experiment aan een gebruiker moet worden weergegeven. U kunt een connector van een externe leverancier aanschaffen bij [AppSource](https://appsource.microsoft.com). Volg de installatie-instructies van de uitgever. U kunt ook de voorbeeldtestconnector van Commerce gebruiken om de experimentwerkstroom te testen zonder dat u een externe service hoeft te configureren. Zie [Connectors configureren en inschakelen](e-commerce-extensibility/connectors.md) voor meer informatie. 
1. **Vlag voor de experimentfunctie inschakelen in Commerce**: u kunt experimenten op tenantniveau inschakelen door naar **Tenantinstellingen \> Functies** te gaan of op siteniveau door naar **Site-instellingen \> Functies** te gaan. Schakel de vlag **Experimenten** in om te beginnen met het maken van modulevarianten. Als u deze vlag uitschakelt, wordt geen enkel experiment meer weergegeven voor gebruikers en worden alle bewerkingsfuncties in Site Builder verwijderd.
    
## <a name="experimentation-lifecycle"></a>Levenscyclus van experiment

Het instellen van een experiment, het maken van variaties en het uitvoeren van een experiment vormen een iteratief proces. In het onderstaande diagram ziet u de levenscyclus van experimenten in Commerce en de service van derden. 

[ ![Levenscyclus van experiment.](./media/experimentation_lifecycle.svg) ](./media/experimentation_lifecycle.svg#lightbox)

Zie de volgende artikelen voor meer informatie over elke stap in het proces van het experiment.
- [Een hypothese opstellen en metrische gegevens bepalen voor een experiment](experimentation-identify.md)
- [Een experiment opzetten](experimentation-setup.md)
- [Een experiment verbinden en bewerken](experimentation-connect-edit.md)
- [Een preview van experimentvarianten weergeven en een experiment publiceren](experimentation-preview-publish.md)
- [Een experiment uitvoeren en controleren](experimentation-run-monitor.md)
- [Een variant promoveren en een experiment voltooien](experimentation-review-complete.md)

> [!NOTE]
> Selecteer **Experimenten** in het linkernavigatievenster van Site Builder als u wilt weten waar een experiment zich in de levenscyclus bevindt. Er wordt een lijst met experimenten weergegeven met de status van elk experiment in zowel Commerce als de service van derden. Zie [De status van een experiment controleren](experimentation-status.md) voor meer informatie.

## <a name="next-step"></a>Volgende stap
[Een hypothese opstellen en metrische gegevens voor succes bepalen voor een experiment](experimentation-identify.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
