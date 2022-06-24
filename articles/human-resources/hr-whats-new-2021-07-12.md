---
title: Nieuwe of gewijzigde functies in Dynamics 365 Human Resources 12 juli 2021
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 12 juli 2021.
author: marcelbf
ms.date: 07/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-12
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 259004773c4e5a7d8865d563da9bcfea3a116632
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870953"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-12-2021"></a>Nieuwe of gewijzigde functies in Dynamics 365 Human Resources 12 juli 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit artikel worden de functies beschreven die in Dynamics 365 Human Resources nieuw, gewijzigd of binnenkort beschikbaar zijn.

Zie [Updateproces](hr-admin-setup-update-process.md) voor meer informatie over het updateproces en de planning.

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) voor meer informatie over nieuwe functies en de verwachte algemene beschikbaarheidsdatums ervan.

## <a name="in-this-release"></a>In deze versie

Deze versie bevat de volgende nieuwe functies en correcties. Wijzigingen die van toepassing zijn op buildnummer 8.1.4353.

### <a name="new-features"></a>Nieuwe functies

De volgende functie zijn algemeen beschikbaar in deze release.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
|  Dienstjarenweergave in-/uitschakelen | |Met deze functie kunt u verschillende datums gebruiken om de dienstjaren te berekenen die worden weergegeven op de pagina **Gestroomlijnde invoer werknemer** en op de pagina **Personen**.  Dit is beschikbaar in [Parameters van Human Resources](/dynamics365/human-resources/hr-setup-parameters). |


### <a name="bug-fixes"></a>Correcties

Deze versie bevat de volgende correcties.

> [!NOTE]
> Ons doel is om deze informatie zo snel mogelijk bij u te krijgen. Mogelijk wordt dit artikel gewijzigd om correcties op te nemen die in de build zijn gemaakt nadat dit artikel oorspronkelijk werd gepubliceerd.

| Probleemnummer | Probleem |  Description |
| --- | --- | --- |
| 595871 | Infodeelvenster Human Resources heeft onjuiste Dataverse-terminologie | Bij het hernoemen van Common Data Service naar Dataverse, is de terminologie is bijgewerkt in het Microsoft Dynamics 365 Human Resources-informatievenster (**Help en ondersteuning > Info**). |
| 598676 | De taak Gestroomlijnde invoer werknemer overschrijven kan tot een foutmelding leiden bij gebruik van Opgeslagen weergave| Als de functie 'Gestroomlijnde werknemerinvoer' op de pagina **Werknemer** is ingeschakeld, kan de toepassing mislukken als **Altijd openen voor bewerking** is ingesteld in de opgeslagen weergave. |
| 592344 |De sectie Vergoedingen voor werknemers op positie moet alleen worden gelezen als vergoedingenbeheer is ingeschakeld | Vergoedingsgegevens voor werknemers worden gemaakt met verouderde vergoedingenfunctionaliteit.  Wanneer vergoedingenbeheer is ingeschakeld, zijn de velden alleen-lezen. Wanneer vergoedingsbeheer is ingeschakeld en **Verouderde vergoedingsformulieren verbergen** worden ingesteld op **Ja** in gedeelde HR-parameters, wordt het tabblad **Werknemerscompensatie** verborgen. |
| 598617 | Tabblad voor activering van formulier **HcmDiscussion** veroorzaakt een oneindige lus bij toepassing van personalisaties | Wanneer in de weergave van zowel het raster als de detailweergave **Altijd openen voor bewerking** is ingeschakeld, veroorzaakt de code die het tabblad activeert in de overschreven taakmethode een conflict met personalisatie over welk besturingselement de focus moet hebben en wordt een oneindige lus gemaakt. |
| 593553 | Het veld Journaaldatum in het prestatiejournaal wordt weergegeven in UTC | Het veld **Journaaldatum** voor prestatiejournaal wordt weergegeven in de UTC-tijdzone in plaats van de tijdzone die is gedefinieerd in de systeemdatuminstellingen, waardoor de datum voor sommige tijdzones niet correct is. |
| 586930 | Bij het openen van activiteiten voor prestatiedoelstellingen wordt een geheel andere record geopend | Wanneer de functie 'Uitgebreide rapportenweergave prestatiejournalen' is ingeschakeld in Functiebeheer, opent het selecteren van de prestatiedoelstellingen voor uitgebreide rapporten op het tabblad **Mijn team** in **Selfservice werknemer** de doelstellingen voor een werknemer in plaats van de geselecteerde werknemer. |
| 569959 |  Entiteit HcmPositionWorkerAssignmentV2 wijst geen werknemer aan een positie toe | Gebruikers ontvangen een fout bij het toevoegen van een positietoewijzingsrecord via de entiteit en publicatie mislukt. |
| 582259 | Het rapport VETS 4212 gebruikt het formulier uit 2017 in plaats van het formulier uit 2020 | Bijgewerkt naar 2020-indeling.  Als u de nieuwe indeling wilt laden, gaat u naar **Rapportconfiguraties** en verwijdert u het VETS-4212-rapport in de linkerkolom. Ga naar **Elektronische rapportage - Opslagplaatsen - HR-resources** en selecteer **Open**.  Selecteer **VETS-4212 PDF-afdrukken** en selecteer vervolgens **Importeren**.|


## <a name="in-preview"></a>Preview

Van de volgende nieuwe functies kan een voorbeeld worden bekeken. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het in- en uitschakelen van functies.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Werkgebied voor vergoedingenbeheer | [Werkruimte Vergoedingenbeheer (preview)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Werkgebied voor vergoedingenbeheer](hr-benefits-management-workspace.md) |
| Vereenvoudigde integratie van de salarisadministratie inschakelen (API's voor integratie van de salarisadministratie) | [Vereenvoudigde integratie met externe salarisadministrateurs inschakelen](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [API voor integratie van salarisadministratie](hr-admin-integration-payroll-api-introduction.md)|
|  Verlof laten beheren door een verzuimmanager | [Verlof laten beheren door een verzuimmanager](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | [De rol van verzuimmanager configureren](https://go.microsoft.com/fwlink/?linkid=2168107)|
|  Bijlagenvereiste per verloftype configureren | [Bijlagenvereiste per verloftype configureren](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Verlof- en verzuimtypen configureren](https://go.microsoft.com/fwlink/?linkid=2168108)|
|  Verlofeenheden per verloftype configureren | [Verlofeenheden per verloftype configureren](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Verlof- en verzuimtypen configureren](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Toestaan dat werknemers kunnen worden gemarkeerd als gereed voor betalen | [Toestaan dat werknemers kunnen worden gemarkeerd als gereed voor betalen](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Gereed voor betaling](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Binnenkort beschikbaar

| Functie | Gegevens |
| --- | --- |
| Platformupdate 10.0.20 (44) | Platformupdate 10.0.20 is gepland voor de uitrol met de volgende servicerelease op 26 juli 2021. Zie voor meer informatie [Platformupdates voor versie 10.0.20 van apps voor financiële en bedrijfsactiviteiten (augustus 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20). |

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) voor een volledige lijst met geplande functies en de bijbehorende geplande versies.

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van Dynamics 365 Human Resources 2021 release wave 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
