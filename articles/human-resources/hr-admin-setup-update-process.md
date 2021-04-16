---
title: Het updateproces
description: Microsoft Dynamics 365 Human Resources is echt software in de vorm van een service (SaaS) die voortdurende 'touchless' updates verzorgt met wijzigingen in toepassingen en platforms.
author: andreabichsel
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4069e369b1a9f15372d1e29e3809198b90b12c7e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791528"
---
# <a name="update-process"></a>Het updateproces

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Human Resources is echt software in de vorm van een service (SaaS) die voortdurende 'touchless' updates verzorgt. Deze updates bevatten zowel toepassings-als platformwijzigingen die vaak belangrijke verbeteringen voor de service bieden, waaronder wettelijke updates.

## <a name="update-policy"></a>Updatebeleid

Er worden regelmatig updates uitgebracht voor alle omgevingen. Human Resources wordt ondersteund volgens het [Microsoft Support Lifecycle-beleid](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), dat consistente en voorspelbare richtlijnen bevat voor de beschikbaarheid van ondersteuning.

## <a name="release-cadence"></a>Releasetempo 

Human Resources-updates worden automatisch op alle omgevingen toegepast. Human Resources biedt twee typen releases:

- **Service-updates**: tweewekelijkse updates die correcties en nieuwe functies bevatten. Service-updates bevatten ook toepasselijke platformupdates wanneer ze worden uitgebracht. Zie [Tabel 3: platform-releases](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases) om na te gaan wanneer platform-updates gewoonlijk worden uitgebracht. Tweewekelijkse updates bieden een gefaseerde globale implementatie tussen regio's. Zie [Nieuwe of gewijzigde functies in Dynamics 365 Human Resources](hr-admin-whats-new.md) voor meer informatie over tweewekelijkse updates.

    Alle ondersteunde gegevenscentra worden tweewekelijks bijgewerkt, tenzij anders aangegeven. In de volgende regio's worden tweewekelijkse updates uitgebracht: Verenigde Staten, Australië, Europa, Groot-Brittannië, Azië en Canada. 

- **Dataverse-oplossingsupdates**: deze updates worden ongeveer om de zes weken uitgevoerd, indien nodig. Deze bevatten nieuwe entiteiten en wijzigingen in bestaande entiteiten in Dataverse. Deze updates worden in dezelfde regio's uitgebracht als de tweewekelijkse updates en het duurt ongeveer zes weken voordat ze door alle datacentra zijn gerepliceerd. Oplossingsupdates kunnen al dan niet samenvallen met tweewekelijkse service-updates.

> [!NOTE]
> Oplossingsupdates zijn beschikbaar in alle datacentra zodra deze zijn uitgebracht. Als u niet wilt wachten totdat de updates automatisch worden gerepliceerd, kunt u deze updates handmatig toepassen op elke willekeurige omgeving in elk datacentrum.

Indien nodig biedt Human Resources ook de volgende typen oplossingen:

- **Revisie (hotfix)**: foutcorrecties die kunnen optreden samen met, of los van, een tweewekelijkse service-updaterelease

- **Noodoplossing**: proactieve en reactieve hotfixes die zelfstandig zijn, kunnen alleen configuratiewijzigingen of ook codewijzigingen bevatten om problemen met live-sites op te lossen en kunnen los van een tweewekelijkse service-updaterelease optreden

Releases worden beoordeeld, getest en gevalideerd in een interne omgeving. Nadat de builds zijn afgemeld, worden ze geïmplementeerd voor productie.

## <a name="release-cadence-exceptions-in-2021"></a>Uitzonderingen in releasetempo in 2021

Om rekening te houden met feestdagen, is de releaseplanning voor november en december 2021 als volgt:

- Release van november: 1 november - 14 november
- Release van december: 29 november - 12 december
 
Her releasetempo van een keer per twee weken wordt op de gebruikelijke manier hervat op 10 januari 2022.

## <a name="communications"></a>Berichtgeving

Op de volgende locaties kunt u nagaan wat er is gepland voor Human Resources en wat we hebben uitgebracht:

- [Dynamics 365 Human Resources-roadmap](https://dynamics.microsoft.com/roadmap/human-resources/)

- [Dynamics 365-releaseplannen](https://docs.microsoft.com/dynamics365/release-plans/)

- [Nieuwe of gewijzigde functies in Dynamics 365 Human Resources](hr-admin-whats-new.md)

- [Problemen zoeken in Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (alleen voor fouten die betrekking hebben op platforms)

- [Human resources-blog](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [Human Resources Yammer-community](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a>Preview-functies in een sandbox-omgeving

U kunt preview-functies in een sandbox-omgeving valideren voordat u deze in uw productie-omgeving inschakelt. Zie [Overzicht van functiebeheer](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) voor meer informatie over het inschakelen van nieuwe functies.

Alle nieuwe functies behouden gedurende minimaal 30 dagen en doorgaans 30-60 dagen de previewstatus. De belangrijkste functies zijn over het algemeen beschikbaar in oktober en april van elk jaar na de previewperiode. Zodra u nieuwe functies in het werkgebied Functiebeheer ziet, kunt u deze inschakelen. Sommige functies zijn mogelijk standaard ingeschakeld.

Soms is een integrale functie standaard ingeschakeld en kan deze niet worden uitgeschakeld (bijvoorbeeld het werkgebied Functiebeheer).

Als een functie algemeen beschikbaar is, kan deze worden in- of uitgeschakeld in productieomgevingen. Het werkgebied Functiebeheer geeft aan wanneer een previewfunctie verplicht wordt. Deze datum is gewoonlijk 1 oktober of 1 april, in overeenstemming met de halfjaarlijkse releaseplannen. U kunt verplichte functies niet uitschakelen. Tot de functie verplicht wordt, kunt u deze in alle omgevingen in- of uitschakelen.

Het is raadzaam om de functies vooraf in een sandbox- of testomgeving te bekijken. U kunt het beste een kopie van uw huidige productie-omgeving of database maken in een sandbox-omgeving, zodat u beschikt over de volledige ervaring van de nieuwe functies met uw gegevens.

Zie [Een Human Resources-project inrichten](hr-admin-setup-provision.md) voor meer informatie over het inrichten van een sandbox-omgeving. Zie [Een exemplaar verwijderen](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment) als u een testomgeving wilt verwijderen. 

## <a name="report-bugs"></a>Fouten rapporteren

Tijdens het testen van preview-functies of het uitproberen van nieuwe mogelijkheden, is het mogelijk dat u items vindt die niet werken zoals u verwacht. Meld eventuele fouten via [Microsoft Dynamics 365-ondersteuning](https://dynamics.microsoft.com/support/).

## <a name="see-also"></a>Zie ook

[Releaseplannen voor Dynamics 365 en Power Platform](https://docs.microsoft.com/dynamics365/release-plans)</br>
[Nieuwe of gewijzigde functies in Dynamics 365 Human Resource](hr-admin-whats-new.md)</br>
[Lifecycle-beleid voor software](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
