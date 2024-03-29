---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources 26 september 2020
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 26 september 2020.
author: jcart1106
ms.date: 09/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2f78201585101e2848eded69e03d5eb4c22d7e9a
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066757"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-26-2020"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources 26 september 2020

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



In dit artikel worden de functies beschreven die in Dynamics 365 Human Resources nieuw, gewijzigd of binnenkort beschikbaar zijn. Zie [Updateproces](hr-admin-setup-update-process.md) voor meer informatie over het updateproces en de planning.

Zie [Overzicht van Dynamics 365 Human Resources 2020 release wave 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/) voor meer informatie over nieuwe functies en de verwachte algemene beschikbaarheidsdatums ervan.

## <a name="in-this-release"></a>In deze versie

Deze versie bevat de volgende nieuwe functies en correcties. Wijzigingen die van toepassing zijn op buildnummer 8.1.3589-hf.3.

### <a name="new-features"></a>Nieuwe functies

De volgende functie is algemeen beschikbaar in deze release:

- **Platformupdate 10.0.13 is nu beschikbaar**: zie [Platformupdates voor versie 10.0.13 van apps voor financiën en bedrijfsactiviteiten (oktober 2020)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-13.md) voor meer informatie over de update.

### <a name="bug-fixes"></a>Correcties

Deze versie bevat de volgende correcties.

> [!NOTE]
> Ons doel is om deze informatie zo snel mogelijk bij u te krijgen. Mogelijk wordt dit artikel gewijzigd om correcties op te nemen die in de build zijn gemaakt nadat dit artikel oorspronkelijk werd gepubliceerd.

| Probleemnummer | Probleem | Description |
| --- | --- | --- |
| 469495 | Update van standaardraster en -dialoogvenster voor financiële dimensies | Het raster en dialoogvenster voor financiële dimensies zijn overal in Human Resources bijgewerkt. |
| 474887 | Met werkitems voor verlofaanvragen wordt de verkeerde koppeling in een handmatige beslissing geopend | Wanneer een werkstroomconfiguratie een handmatige beslissing bevat en u vanuit **Aan mij toegewezen werkitems** naar de verlofaanvraag gaat, wordt de verkeerde koppeling geopend, waarbij een leeg formulier wordt weergegeven of een verlofaanvraag die is gemaakt door de huidige gebruiker in plaats van de gebruiker die eraan is toegewezen voor de handmatige beslissing. |
| 474962 | Entiteiten van parameters voor verlof en verzuim bevatten velden met dubbelzinnige labels | Entiteitslabels van parameters voor verlof en verzuim zijn bijgewerkt zodat ze duidelijker zijn. |
| 481401 | De toerekeningsverwerking loopt vast wanneer de toerekeningsdatumbasis valt na de begindatum van de toerekening en aan het einde van de maand | Toerekeningsverwerking is bijgewerkt zodat er geen vertraging optreedt wanneer de toerekeningsdatumbasis valt na de begindatum van de toerekening en aan het einde van de maand. |
| 447167 | De lijsten met verlopende records bevatten inactieve werknemers | Het tabblad **Verlopende records** in **Personeelsbeheer** bevatte inactieve werknemers. Nu bevatten de lijsten alleen actieve werknemers. |
| 486840 | Er wordt een verkeerde verlof- of verzuimaanvraag geopend via **Aan mij toegewezen werkitems** | Als een verlof- of verzuimaanvraag wordt geselecteerd via **Aan mij toegewezen werkitems** wordt niet meer de meest recente verlof- of verzuimaanvraag geopend die aan de huidige gebruiker is toegewezen. |
| 506868 | Het veld **Titel** van Dataverse niet ingesteld voor de entiteit **Functiepositie** | Het veld **Titel** in de entiteiten **Functie** en **Functiepositie** wordt weergegeven als niet opgegeven. Het veld **Titel** wordt nu weergegeven. |
| 430359 | Geen toegang tot taken van de offboarding-controlelijst waaraan manager- en werknemersrollen zijn toegewezen | Werknemers met een toekomstige ontslagdatum konden geen toegang krijgen tot hun controlelijsttaken als ze alleen een werknemersrol of managerrol hadden. Nu kunnen gebruikers die alleen een werknemers- of managerrol hebben, toegang krijgen tot offboarding-taken met een toekomstige ontslagdatum. |
| 458102 | Nieuwe werknemers worden niet weergegeven in de entiteit **Gegevens werknemerssalaris** wanneer ze worden gemaakt | Nieuwe werknemers worden opgenomen in de entiteit voor gegevens van werknemerssalaris zonder dat de salarisgegevens voor de werknemer hoeven te worden geopend voordat de entiteit wordt geëxporteerd. |

## <a name="in-preview"></a>Preview

Van de volgende nieuwe functies kan een voorbeeld worden bekeken. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het in- en uitschakelen van functies.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Human Resources-app in Microsoft Teams | [Verlof en verzuim van werknemers in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Human Resources-app in Teams](./hr-admin-teams-leave-app.md)<br>[Verlofaanvragen beheren in Teams](hr-teams-leave-app.md) |
| Uitgebreide aanvragen en goedkeuringen voor werkstromen | [Verbeteringen in de ervaring van werkstromen voor organisatie en personeelsbeheer](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Configuratieoptie om de lijst Aan mij toegewezen werkitems te positioneren](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |

## <a name="coming-soon"></a>Binnenkort beschikbaar

De volgende nieuwe functie is gepland voor een toekomstige versie:

- [Aangepaste koppelingen in Selfservice manager](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service)

Zie [Overzicht van Dynamics 365 Human Resources 2019 release wave 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/) voor een volledige lijst met geplande functies en de bijbehorende geplande versies.

## <a name="additional-resources"></a>Aanvullende bronnen

[Wat is nieuw of gewijzigd in Human Resources](hr-admin-whats-new.md)
[Overzicht van Dynamics 365 Human Resources 2020 release wave 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)
[Updateproces](hr-admin-setup-update-process.md)
[Functies beheren](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
