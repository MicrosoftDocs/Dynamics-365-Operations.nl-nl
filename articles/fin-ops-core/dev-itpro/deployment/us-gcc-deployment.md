---
title: Dynamics 365 Finance, Supply Chain Management en Commerce in de Amerikaanse Government Community Cloud (GCC)
description: Dit artikel bevat informatie over Microsoft Dynamics 365 US Government-producten die beschikbaar zijn voor gekwalificeerde overheidsinstellingen en privé-entiteiten.
author: hasaid
ms.date: 11/12/2021
ms.topic: article
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2021-11-09
ms.openlocfilehash: 90e64fec512307af209ace128d5897475de7aee5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867268"
---
# <a name="dynamics-365-finance-supply-chain-management-and-commerce-in-us-government-community-cloud-gcc"></a>Dynamics 365 Finance, Supply Chain Management en Commerce in de Amerikaanse Government Community Cloud (GCC)

[!include [banner](../includes/banner.md)]



Bepaalde Microsoft Dynamics 365-producten voor de Amerikaanse (VS) overheid zijn beschikbaar voor gekwalificeerde overheidsinstellingen en privé-entiteiten. Deze entiteiten zijn beperkt tot de volgende typen:

- Entiteiten van de Amerikaanse federale, staats-, lokale en territoriale overheid
- Privé-entiteiten die Dynamics 365 US Government gebruiken om oplossingen te leveren aan overheidsinstellingen of aan gekwalificeerde leden van de cloudcommunity
- Privé-entiteiten met klantgegevens die onder overheidsregels vallen, en Dynamics 365 US Government is de juiste service om aan de wettelijke vereisten te voldoen

Zie [Dynamics 365 US Government](/power-platform/admin/microsoft-dynamics-365-government) voor meer informatie.

## <a name="onboarding"></a>Onboarding

Als u de initiële onboarding voor een implementatieproject wilt voltooien in Microsoft Dynamics Lifecycle Services (LCS), volgt u de instructies in [Een implementatieproject onboarden](../../../fin-ops-core/fin-ops/imp-lifecycle/onboard.md). Gebruik echter niet de koppeling naar openbare LCS die in deze instructies is opgegeven. Gebruik in plaats daarvan de volgende URL om LCS voor Amerikaanse Government Community Cloud (GCC) te openen: <https://gov.lcs.microsoftdynamics.us>.

Nadat de initiële onboarding is voltooid, volgt u de instructies in [Onboarding voor project](../lifecycle-services/project-onboarding.md). Gebruik opnieuw [LCS voor GCC](https://gov.lcs.microsoftdynamics.us) in plaats van openbare LCS.

## <a name="environment-deployment"></a>Implementatie van omgeving

Nadat u de onboarding voor een project hebt voltooid, kunt u de aanvullende mogelijkheden van LCS controleren die zijn beschreven in [Lifecycle Services (LCS) voor klanten met apps voor financiële en bedrijfsactiviteiten](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md). Ga vervolgens verder met de implementatie van de omgeving.

- Als u door Microsoft beheerde omgevingen wilt implementeren via LCS, volgt u de instructies in [Lifecycle Services (LCS) voor klanten met apps voor financiële en bedrijfsactiviteiten](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md#new-deployment-experience).
- Zie [Ontwikkelomgevingen implementeren en openen](../../../fin-ops-core/dev-itpro/dev-tools/access-instances.md) voor in de cloud gehoste omgevingen. U moet ook het onboardingsproces voor Resource Manager voltooien voor uw connectors, zoals beschreven in [Het proces voor onboarding van Azure Resource Manager voltooien voor Lifecycle Services-projecten van de Amerikaanse overheid](arm-onbarding-us-goverment.md).

> [!NOTE]
> Voor LCS-projecten van de Amerikaanse overheid worden alleen Azure-overheidsabonnementen ondersteund.

## <a name="features-that-arent-available"></a>Functies die niet beschikbaar zijn

Sommige functies zijn niet beschikbaar voor implementatie in GCC of zijn niet beschikbaar voor gebruik met Dynamics 365 in GCC. Zo zijn bijvoorbeeld Azure DevOps-services niet beschikbaar in GCC. Er kunnen echter wel on-premises Azure DevOps of openbare Azure DevOps-services worden gebruikt. Zie [Beschikbaarheid van functies in zakelijke toepassingen voor de Amerikaanse overheid](https://aka.ms/BAPFunctionalParity) voor gedetailleerde informatie over de beschikbaarheid van functies.

## <a name="frequently-asked-questions"></a>Veelgestelde vragen

### <a name="are-dynamics-365-finance-and-dynamics-365-supply-chain-management-supported-in-gcc-high"></a>Worden Dynamics 365 Finance en Dynamics 365 Supply Chain Management ondersteund in GCC High?

Nummer Dynamics 365 Finance en Dynamics 365 Supply Chain Management worden alleen ondersteund in GCC.

### <a name="can-i-use-public-azure-devops-with-finance-and-supply-chain-management-in-gcc"></a>Kan ik openbare Azure DevOps gebruiken met Finance en Supply Chain Management in GCC?

Ja, u kunt openbare Azure DevOps-services gebruiken als u geen vereisten hebt voor een oplossing die is gecertificeerd door het Federal Risk and Authorization Management Program (FEDRAMP). U kunt ook Azure DevOps Server gebruiken.

### <a name="can-i-deploy-a-cloud-hosted-environment-tier-1-development-environment-on-an-azure-commercial-subscription"></a>Kan ik een in de cloud gehoste ontwikkelomgeving van niveau 1 implementeren in een commercieel Azure-abonnement?

Nee. In [LCS voor GCC](https://gov.lcs.microsoftdynamics.us) moet u een Azure Government-abonnement gebruiken om een in de cloud gehoste omgeving te kunnen implementeren.

### <a name="what-can-i-do-if-i-need-a-package-from-the-shared-asset-library-but-it-isnt-available-in-lcs-for-gcc"></a>Wat kan ik doen als ik een pakket uit de bibliotheek met gedeelde activa nodig heb, dat echter niet beschikbaar is in LCS voor GCC?

U kunt hetzelfde pakket downloaden vanuit de bibliotheek voor gedeelde activa in [openbare LCS](https://lcs.dynamics.com). Uw partner kan u ook helpen met het downloaden van het pakket.

### <a name="is-the-code-upgrade-tool-available-in-gcc"></a>Is het hulpprogramma voor het bijwerken van codes beschikbaar in GCC?

Nee, het hulpprogramma voor het bijwerken van codes is momenteel niet beschikbaar in GCC. U kunt echter een prospectproject maken in [openbare LCS](https://lcs.dynamics.com) en gebruikmaken van het hulpprogramma voor het bijwerken van code. Het is niet mogelijk om omgevingen in prospectprojecten te implementeren.

### <a name="can-my-partner-open-a-support-ticket-on-my-behalf"></a>Kan mijn partner namens mij een ondersteuningsticket openen?

Ja. Als uw partner echter een niet-GCC-identiteit gebruikt, wordt het ondersteuningsticket doorgestuurd naar de wachtrij voor openbare ondersteuning. Het wordt aangeraden om klant-GCC-rechten in LCS te gebruiken om ondersteuningstickets te openen.

## <a name="see-also"></a>Zie ook

- [Dynamics 365 US Government](/power-platform/admin/microsoft-dynamics-365-government)
- [Beschikbaarheid van functies in zakelijke toepassingen voor de Amerikaanse overheid](https://aka.ms/BAPFunctionalParity).
- [Gebruikershandleiding Lifecycle Services (LCS)](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [Overzicht van Cloudimplementatie](../../../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
