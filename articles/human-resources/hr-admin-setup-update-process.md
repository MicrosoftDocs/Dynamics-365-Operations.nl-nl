---
title: Het updateproces
description: Microsoft Dynamics 365 Human Resources is echt software in de vorm van een service (SaaS) die voortdurende 'touchless' updates verzorgt met wijzigingen in toepassingen en platforms.
author: twheeloc
ms.date: 12/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 197b3c5717494ab3c80a57cda337a9021293bf73
ms.sourcegitcommit: 68efa7b89273d04484566cbe14d3533a8fd4ee53
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/02/2022
ms.locfileid: "9819291"
---
# <a name="update-process"></a>Het updateproces

_**Is van toepassing op:** Human resources in de zelfstandige infrastructuur_ 

> [!NOTE]
> Vanaf juli 2022 kunnen er geen nieuwe Human Resources-omgevingen worden ingericht in de zelfstandige Human Resources-infrastructuur en er kunnen geen nieuwe Microsoft Dynamics LCS-projecten (Lifecycle Services) in worden gemaakt. Klanten kunnen Human Resources-omgevingen implementeren in de infrastructuur voor financiën en bedrijfsactiviteiten. Zie voor meer informatie [Human Resources in de infrastructuur voor financiën en bedrijfsactiviteiten inrichten](hr-admin-setup-provision-fo.md).

> [!IMPORTANT]
> Het update- en hotfix-proces in de infrastructuur van de app voor financiën en bedrijfsactiviteiten verschilt van het update- en hotfix-proces voor Human resources (zelfstandig). Zie [Proces voor overschakeling naar de nieuwste update van de app voor financiën en bedrijfsactiviteiten](../fin-ops-core/dev-itpro/migration-upgrade/upgrade-latest-update.md) voor meer informatie over het updateproces. Zie voor meer informatie over hotfixes [Updates downloaden vanuit Lifecycle Services (LCS)](/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs.md). 

Microsoft Dynamics 365 Human Resources is echt software in de vorm van een service (SaaS) die voortdurende 'touchless' updates verzorgt. Deze updates bevatten zowel toepassings-als platformwijzigingen die vaak belangrijke verbeteringen voor de service bieden, waaronder wettelijke updates.

## <a name="update-policy"></a>Updatebeleid

Er worden regelmatig updates uitgebracht voor alle omgevingen. Human Resources wordt ondersteund volgens het [Microsoft Support Lifecycle-beleid](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), dat consistente en voorspelbare richtlijnen bevat voor de beschikbaarheid van ondersteuning.

## <a name="release-cadence"></a>Releasetempo 

Human Resources-updates worden automatisch op alle omgevingen toegepast. Human Resources biedt twee typen releases:

- **Service-updates**: service-updates bevatten ook toepasselijke platformupdates wanneer ze worden uitgebracht. Naast updates op basis van uitzonderingen vinden regelmatige service-updates plaats via de GA (General Availability) van Dynamics 365 Finance-platformupdates. Zie [Nieuwe of gewijzigde functies in Platformupdates](../fin-ops-core/dev-itpro/get-started/whats-new-home-page.md) voor meer informatie over platformreleases. Updates bieden een gefaseerde globale implementatie tussen regio's. Zie [Nieuwe of gewijzigde functies in Dynamics 365 Human Resources](hr-admin-whats-new.md) voor meer informatie over updates.

- **Dataverse-oplossingsupdates**: deze updates worden ongeveer om de zes weken uitgevoerd, indien nodig. Deze bevatten nieuwe entiteiten en wijzigingen in bestaande entiteiten in Dataverse. Deze updates worden in dezelfde regio's uitgebracht als de tweewekelijkse updates en het duurt ongeveer zes weken voordat ze door alle datacentra zijn gerepliceerd. Oplossingsupdates kunnen al dan niet samenvallen met tweewekelijkse service-updates.

> [!NOTE]
> Oplossingsupdates zijn beschikbaar in alle datacentra zodra deze zijn uitgebracht. Als u niet wilt wachten totdat de updates automatisch worden gerepliceerd, kunt u deze updates handmatig toepassen op elke willekeurige omgeving in elk datacentrum.

Indien nodig biedt Human Resources ook de volgende typen oplossingen:

- **Revisie (hotfix)**: foutcorrecties die kunnen optreden samen met, of los van, een tweewekelijkse service-updaterelease

- **Noodoplossing**: proactieve en reactieve hotfixes die zelfstandig zijn, kunnen alleen configuratiewijzigingen of ook codewijzigingen bevatten om problemen met live-sites op te lossen en kunnen los van een tweewekelijkse service-updaterelease optreden

Releases worden beoordeeld, getest en gevalideerd in een interne omgeving. Nadat de builds zijn afgemeld, worden ze geïmplementeerd voor productie.

## <a name="communications"></a>Communicatie

Op de volgende locaties kunt u nagaan wat er is gepland voor Human Resources en wat we hebben uitgebracht:

- [Dynamics 365 Human Resources-roadmap](https://dynamics.microsoft.com/roadmap/human-resources/)

- [Dynamics 365-releaseplannen](/dynamics365/release-plans/)

- [Nieuwe of gewijzigde functies in Dynamics 365 Human Resources](hr-admin-whats-new.md)

- [Problemen zoeken in Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs.md) (alleen voor fouten die betrekking hebben op platforms)

- [Human resources-blog](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [Human Resources Yammer-community](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a>Preview-functies in een sandbox-omgeving

U kunt preview-functies in een sandbox-omgeving valideren voordat u deze in uw productie-omgeving inschakelt. Zie [Overzicht van functiebeheer](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) voor meer informatie over het inschakelen van nieuwe functies.

Alle nieuwe functies behouden gedurende minimaal 30 dagen en doorgaans 30-60 dagen de previewstatus. De belangrijkste functies zijn over het algemeen beschikbaar in oktober en april van elk jaar na de previewperiode. Zodra u nieuwe functies in het werkgebied **Functiebeheer** ziet, kunt u deze inschakelen. Sommige functies zijn mogelijk standaard ingeschakeld.

Soms is een integrale functie standaard ingeschakeld en kan deze niet worden uitgeschakeld (bijvoorbeeld het werkgebied Functiebeheer).

Als een functie algemeen beschikbaar is, kan deze worden in- of uitgeschakeld in productieomgevingen. Het werkgebied **Functiebeheer** geeft aan wanneer een preview-functie verplicht wordt. Deze datum is gewoonlijk 1 oktober of 1 april, in overeenstemming met de halfjaarlijkse releaseplannen. U kunt verplichte functies niet uitschakelen. Tot de functie verplicht wordt, kunt u deze in alle omgevingen in- of uitschakelen.

Het is raadzaam om de functies vooraf in een sandbox- of testomgeving te bekijken. U kunt het beste een kopie van uw huidige productie-omgeving of database maken in een sandbox-omgeving, zodat u beschikt over de volledige ervaring van de nieuwe functies met uw gegevens.

Zie [Een Human Resources-project inrichten](hr-admin-setup-provision.md) voor meer informatie over het inrichten van een sandbox-omgeving. Zie [Een exemplaar verwijderen](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment) als u een testomgeving wilt verwijderen. 

## <a name="report-bugs"></a>Fouten rapporteren

Tijdens het testen van preview-functies of het uitproberen van nieuwe mogelijkheden, is het mogelijk dat u items vindt die niet werken zoals u verwacht. Meld eventuele fouten via [Microsoft Dynamics 365-ondersteuning](https://dynamics.microsoft.com/support/).

## <a name="see-also"></a>Zie ook

[Releaseplannen voor Dynamics 365 en Power Platform](/dynamics365/release-plans)</br>
[Nieuwe of gewijzigde functies in Dynamics 365 Human Resource](hr-admin-whats-new.md)</br>
[Lifecycle-beleid voor software](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
