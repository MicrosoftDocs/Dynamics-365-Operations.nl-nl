---
title: Veelgestelde vragen over integratie van Attract met LinkedIn
description: In dit onderwerp worden vragen beantwoord die u mogelijk hebt over de integratie tussen LinkedIn en Microsoft Dynamics 365 Talent - Attract.
author: hasrivas
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: hasrivas
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: d66ebc01597f8038a38b46a9f1b70feaa5dc505e
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008634"
---
# <a name="linkedin-integration-faq"></a>Veelgestelde vragen over LinkedIn-integratie

[!include [banner](includes/banner.md)]

LinkedIn is het grootste onlinenetwerk voor professionals ter wereld. Microsoft Dynamics Talent: Attract kan met LinkedIn worden geïntegreerd om u toegang te bieden tot te beste talenten ter wereld. Met Attract kunt u vacatures rechtstreeks op LinkedIn plaatsen, maar kunt u ook kandidaatgegevens van LinkedIn in Attract opnemen.

## <a name="for-recruiters-and-hiring-managers"></a>Voor wervers en aanstellende managers

Hier vindt u antwoorden op veelgestelde vragen over hoe u Attract en LinkedIn samen kunt gebruiken.

### <a name="what-linkedin-features-do-i-get-with-attract"></a>Welke LinkedIn-functies krijg ik met Attract?

Dankzij de integratie met LinkedIn kunt u de volgende taken uitvoeren:

- [Vacatures plaatsen op LinkedIn](./attract-post-jobs-to-linkedin.md) (als gratis Limited Listings).
- [Kandidaatgegevens vanuit LinkedIn exporteren naar Attract](./attract-linkedin-recruiter.md#export-linkedin-candidates-to-attract-with-one-click).
- [Sollicitanten toestaan om op functies te solliciteren met LinkedIn](./attract-admin-linkedin.md#set-up-apply-with-linkedin-in-attract).

### <a name="what-do-i-need-before-i-can-post-jobs-to-linkedin"></a>Wat heb ik nodig voordat ik vacatures kan plaatsen op LinkedIn?

Uw beheerder moet [LinkedIn-integratie configureren in Attract](./attract-admin-linkedin.md#configure-job-posting-to-linkedin). Vervolgens kunt u aan de slag.

### <a name="how-do-i-post-jobs-to-linkedin-from-attract"></a>Hoe plaats ik vacatures op LinkedIn vanuit Attract?

Nadat u een taak hebt gemaakt in Attract, hoeft u alleen de knop **Nu plaatsen** te selecteren die correspondeert met LinkedIn. Zie [Vacatures plaatsen op LinkedIn vanuit Attract](./attract-post-jobs-to-linkedin.md#post-jobs-to-linkedin) voor meer informatie.

### <a name="can-i-get-candidate-information-from-linkedin-into-attract"></a>Kan ik kandidaatgegevens vanuit LinkedIn in Attract krijgen?

Ja. Als u een goede kandidaat ziet op LinkedIn, kunt u de gegevens van die kandidaat eenvoudig exporteren in Attract. Zie voor meer informatie [Kandidaten zoeken met LinkedIn Recruiter](attract-linkedin-recruiter.md).

### <a name="how-can-i-get-help-accessing-linkedin-from-attract"></a>Hoe kan ik hulp krijgen bij het openen van LinkedIn vanuit Attract?

Zie [Problemen met integratie met LinkedIn oplossen](./attract-troubleshoot-linkedin.md) als u problemen hebt met het aanmelden bij of plaatsen van vacatures in LinkedIn vanuit Attract.

Zie [Ondersteuning voor Talent](./talent-support.md) voor andere problemen met Attract. Zie de [ondersteuningspagina van LinkedIn](https://www.linkedin.com/help) voor hulp met LinkedIn.

## <a name="for-admins-and-developers"></a>Voor beheerders en ontwikkelaars

Hier vindt u antwoorden op veelgestelde vragen over hoe u de integratie tussen Attract en LinkedIn kunt configureren.

### <a name="how-do-i-configure-attract-so-that-recruiters-and-hiring-managers-can-post-jobs-to-linkedin"></a>Hoe configureer ik Attract zo dat wervers en aanstellende managers vacatures kunnen plaatsen naar LinkedIn?

U kunt de beschikbare opties configureren op het tabblad **LinkedIn-integratie** in het beheercentrum. Zie [integratie met LinkedIn instellen](./attract-admin-linkedin.md) voor meer informatie.

### <a name="can-i-export-candidate-information-from-linkedin"></a>Kan ik kandidaatgegevens vanuit LinkedIn exporteren?

Ja, maar u moet eerst de integratie met LinkedIn Recruiter configureren. Zie [integratie met LinkedIn instellen](./attract-admin-linkedin.md) voor meer informatie.

### <a name="how-can-i-post-jobs-to-premium-job-slots-on-linkedin"></a>Hoe kan ik vacatures plaatsen in Premium Job Slots op LinkedIn?

Hoewel Attract een krachtige oplossing biedt voor het plaatsen van vacatures op LinkedIn, hebt u mogelijk extra flexibiliteit nodig. Het is bijvoorbeeld mogelijk dat u Premium Job Slots wilt plaatsen naast de gratis Limited Listings of misschien wilt u dat LinkedIn uw batchpersoneelsadvertenties meerdere keren per dag verwerkt.

#### <a name="types-of-linkedin-job-posts"></a>Typen LinkedIn-personeelsadvertenties

LinkedIn biedt de volgende typen personeelsadvertenties:

- **Limited Listing**: gratis personeelsadvertenties die in zoekresultaten worden weergegeven wanneer kandidaten naar functies zoeken op LinkedIn en op de LinkedIn-pagina van een bedrijf. Limited Listings zijn gericht op actieve werkzoekenden. Dit type vermelding is het type dat Attract biedt aan LinkedIn. U kunt geen Limited Listing-vacatures promoten op LinkedIn. Als u Limited Listings wilt promoten, moet u met LinkedIn werken om Job Wrapping in te schakelen. Raadpleeg voor meer informatie over Job Wrapping de onderwerpen [Beperkte aanbiedingen VS Premium job slots voor Job Wrapping](https://www.linkedin.com/help/recruiter/answer/79049/limited-listings-vs-premium-job-slots-for-job-wrapping) en [Job Wrapping Plus - Veelgestelde vragen](https://www.linkedin.com/help/recruiter/answer/79050/job-wrapping-frequently-asked-questions).
- **Premium Job Slot** – Gekochte vacatures die op verschillende plaatsen in LinkedIn, zoals de LinkedIn-feed, e-mails en het gebied **Vacatures die u misschien interesseren**, worden weergegeven. Premium Job Slots zijn gericht op passieve kandidaten, maar ze worden ook weergegeven in zoekopdrachten naar vacatures.

Vanuit Attract worden vacatures op LinkedIn als gratis Limited Listings geplaatst. Als u Premium Job Slots wilt gebruiken, moet u Job Wrapping via LinkedIn Recruiter gebruiken. Voor Job Wrapping hebt u een contract voor job wrapping met LinkedIn nodig. Zie [Job Wrapping via LinkedIn Recruiter - Overzicht](https://www.linkedin.com/help/recruiter/answer/79037) voor meer informatie.

#### <a name="frequency-of-batch-processing-on-linkedin"></a>Frequentie van batchverwerking op LinkedIn

Op LinkedIn worden vacatures één keer per dag in een batch via Attract verwerkt. Daarom kan het maximaal 48 uur duren voordat vacatures op LinkedIn worden weergegeven nadat ze zijn geplaatst via Attract. Als u wilt dat vacatures sneller worden weer gegeven op LinkedIn of als u extra flexibiliteit nodig hebt, kunt u de API (Application Programming Interface) Recruiting System Connected van LinkedIn gebruiken. Zie [Recruiter System Connect](https://docs.microsoft.com/linkedin/talent/recruiter-system-connect) voor meer informatie.

#### <a name="table-of-options-for-job-posting-to-linkedin"></a>Tabel met opties voor het plaatsen van vacatures op LinkedIn

In de volgende tabel worden de verschillende opties voor het plaatsen van vacatures naar LinkedIn beschreven. De tabel bevat de voordelen van elke optie en aanvullende informatie.

|  | Attract | Job Wrapping via LinkedIn Recruiter | Recruiter System Connect-API |
|---|---|---|---|
| **Beschrijving** | Vanuit Attract worden vacatures als XML-feed op LinkedIn geplaatst. | Het bedrijf sluit een contract met LinkedIn af en biedt een XML-feed voor het plaatsen van vacatures. | De klant gebruikt de API voor het synchroniseren van gegevens tussen Attract en LinkedIn Recruiter. |
| **Wat voor soort vacature kan ik plaatsen?** | Limited Listing | Premium Job Slot of Limited Listing | Limited Listing |
| **Kan ik de vacature promoten op LinkedIn?** | Nee | Premium Job Slots: ja<br>Limited Listings: nee | Nee |
| **Hoe vaak worden vacatures geplaatst op LinkedIn?** | Eenmaal per dag | Eenmaal per dag | Meerdere keren per dag, zoals gedefinieerd door de API |
| **Aanbevolen door LinkedIn?** | Nee | Ja | Nee |
| **Wat heb ik nodig?** | De aanschaf van Attract | Een contract voor job wrapping met LinkedIn en de aanschaf van Premium Job Slots | Een API-overeenkomst met LinkedIn | 
| **Waar kan ik meer informatie vinden?** | [Integratie met LinkedIn instellen](./attract-admin-linkedin.md) | [Job Wrapping via LinkedIn Recruiter - Overzicht](https://www.linkedin.com/help/recruiter/answer/79037) | [Recruiter System Connect](https://docs.microsoft.com/linkedin/talent/recruiter-system-connect) |

> [!NOTE]
> U hebt geen LinkedIn Recruiter System Connect-licentie nodig om vacatures op LinkedIn te plaatsen met Attract.

## <a name="see-also"></a>Zie ook

[Integratie met LinkedIn instellen](./attract-admin-linkedin.md)

[Vacatures plaatsen op LinkedIn vanuit Attract](./attract-post-jobs-to-linkedin.md)

[Kandidaten zoeken met LinkedIn Recruiter](./attract-linkedin-recruiter.md)

[Problemen met integratie met LinkedIn oplossen](./attract-troubleshoot-linkedin.md)
