---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources 5 oktober 2021
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 5 oktober 2021.
author: marcelbf
ms.date: 10/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ba24afd16a471abb36a6f7bc9a8610acec374190
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067966"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-5-2021"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources 5 oktober 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit artikel worden de functies beschreven die nieuw, gewijzigd of binnenkort beschikbaar zijn in Microsoft Dynamics 365 Human Resources.

Zie [Updateproces](hr-admin-setup-update-process.md) voor meer informatie over het updateproces en de planning.

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/) voor meer informatie over nieuwe functies en de verwachte algemene beschikbaarheidsdatums ervan.

## <a name="in-this-release"></a>In deze versie

Deze versie bevat de volgende nieuwe functies en correcties. Wijzigingen die van toepassing zijn op buildnummer 8.1.4485.

### <a name="new-features"></a>Nieuwe functies

De volgende functie zijn algemeen beschikbaar in deze release.

| Functie | Vrijgaveplan | Documentatie |
|---|---|---|
| Platformupdate 10.0.21 (45) | -- | [Platformupdates voor versie 10.0.21 van apps voor financiën en bedrijfsactiviteiten (oktober 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21) |


### <a name="bug-fixes"></a>Correcties

Deze versie bevat de volgende correcties.

> [!NOTE]
> Ons doel is om deze informatie zo snel mogelijk bij u te krijgen. Mogelijk wordt dit artikel gewijzigd om correcties op te nemen die in de build zijn gemaakt nadat dit artikel oorspronkelijk werd gepubliceerd.

| Probleemnummer | Probleem | Description |
|---|---|---|
| 598896 | Het werknemersbedrag wordt pas weergegeven als de werknemer de inschrijving heeft voltooid | Op de pagina **Werknemerselfservice** wordt het werknemersbedrag voor de vergoeding niet weergegeven. Op de pagina **Selfservice voor vergoedingen** wordt nu het werknemersbedrag weergegeven.  |
| 613440 | Kan geen gegevens uit **Gegevensbeheer** exporteren | Bij het exporteren van gegevens voor een project in **Gegevensbeheer** mislukt de export onverwacht. |
| 618327 | Afgesloten en toekomstige perioden worden weergegeven op de pagina **Rapportenparameters** voor het vergoedingenoverzicht | Wanneer u naar het **Vergoedingenoverzicht** in **Werknemerselfservice** gaat, worden op de pagina **Rapportparameters** de opties **Op te nemen records** en **Op de achtergrond uitvoeren** weergegeven. Deze secties zijn verwijderd.|
| 618326 | De pagina **Rapportparameters** in **Werknemerselfservice** voor het vergoedingenoverzicht is onjuist| Wanneer de gebruiker naar de doelpagina **Rapport vergoedingenoverzicht** gaat, kan de gebruiker perioden voor vergoedingsplannen selecteren die zijn afgesloten of in de toekomst liggen, wat resulteert in een lege pagina. Alleen de huidige periode voor het vergoedingsplan wordt in de lijst weergegeven. |

## <a name="in-preview"></a>Preview

Van de volgende nieuwe functies kan een voorbeeld worden bekeken. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het in- en uitschakelen van functies.

| Functie | Vrijgaveplan | Documentatie |
|---|---|---|
| Werkgebied voor vergoedingenbeheer | [Werkruimte Vergoedingenbeheer (preview)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Werkgebied voor vergoedingenbeheer](hr-benefits-management-workspace.md) |
| Aangepaste velden in Geschiktheid |[Ondersteuning voor aangepaste velden in verwerking van geschiktheid](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management) | [Aangepaste velden in verwerking van geschiktheid gebruiken](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules#using-custom-fields-in-eligibility-rules) |
| Vergoedingenverklaring |[Vergoedingenoverzicht](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/benefits-summary-statement) | [Vergoedingeninstructie](hr-benefits-statement.md) |

### <a name="benefits-statement-known-issues"></a>Bekende problemen in Vergoedingenoverzicht

| Probleem | Omschrijving |
|---|---|
|Fout bij het verzenden via e-mail van een rapport met de **Duitse rapportbestemming** | Het vergoedingenoverzicht kan worden ingesteld om de e-mailparameters te gebruiken op de pagina **Bestemmingen Duits rapport**. Wanneer u het instellen en afdrukken van het rapport voltooit, krijgt de gebruiker een opmaakfout en wordt het vergoedingenoverzicht niet verzonden.|

## <a name="feature-management-changes"></a>Wijzigingen in functiebeheer

| Functie | Omschrijving |
|---|---|
|Weergave van uitgebreide rapporten voor prestatiejournalen | Deze functie wordt standaard ingeschakeld in deze versie. |

## <a name="coming-soon"></a>Binnenkort beschikbaar

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/) voor een volledige lijst met geplande functies en de bijbehorende geplande versies.

| Functie | Gegevens |
|---|---|
| Platformupdate 10.0.22 (46) | Implementatie van platformupdate 10.0.22 is gepland voor de volgende servicerelease op 1 november 2021. Zie voor meer informatie [Platformupdates voor versie 10.0.22 van apps voor financiën en bedrijfsactiviteiten (november 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22). |



## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van Dynamics 365 Human Resources 2021 release wave 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

