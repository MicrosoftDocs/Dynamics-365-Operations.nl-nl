---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources 8 maart 2021
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 8 maart 2021.
author: marcelbf
manager: tfehr
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c3cd69c86e8590951dd96da75d99bfee2855ac93
ms.sourcegitcommit: 75b432ce9019c81253eb6bd865db905701e28a26
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/11/2021
ms.locfileid: "5579398"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-08-2021"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources 08 maart 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn of die binnenkort worden vrijgegeven in Dynamics 365 Human Resources.

Zie [Updateproces](hr-admin-setup-update-process.md) voor meer informatie over het updateproces en de planning.

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 1](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) voor meer informatie over nieuwe functies en de verwachte algemene beschikbaarheidsdatums ervan.

## <a name="in-this-release"></a>In deze versie

Deze versie bevat de volgende nieuwe functies en correcties. Wijzigingen die van toepassing zijn op buildnummer 8.1.4017.

### <a name="new-features"></a>Nieuwe functies

De volgende functie zijn algemeen beschikbaar in deze release.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Bedrijfsweergave van verlof voor managers | [Bedrijfsweergave van werknemersverlof voor managers](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Parameters voor verlof en verzuim configureren](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-parameters) |

### <a name="bug-fixes"></a>Correcties

Deze versie bevat de volgende correcties.

> [!NOTE]
> Ons doel is om deze informatie zo snel mogelijk bij u te krijgen. Mogelijk wordt dit onderwerp gewijzigd om correcties op te nemen die in de build zijn gemaakt nadat dit onderwerp oorspronkelijk werd gepubliceerd.

| Probleemnummer | Uitgeven |  Beschrijving |
| --- | --- | --- |
| 486611 | Verlof wordt weergegeven op verlofkalender wanneer **Verlof voor alle kalenders uitschakelen** is ingeschakeld | Als **Verlof voor alle kalenders uitschakelen** is ingeschakeld, wordt er geen verlofinformatie meer weergegeven wanneer de functie voor het verbeteren van verlof- en verzuimkalenders is ingeschakeld.|
| 508972 | Validatie van inschrijving ontbreekt bij verlof en verzuim van banktransactie-entiteit | Wanneer u de banktransactie-entiteit voor verlof en verzuim gebruikt, kunnen werknemers die niet zijn ingeschreven voor een plan niet meer worden geïmporteerd. |
| 554854 | Kalender bijwerken in de entiteit Dienstverband geeft fouten als de standaard rechtspersoon bij gebruikersopties anders is | Als de entiteit Dienstverband wordt gebruikt om de kalender voor een werknemer bij te werken, levert dat geen fout meer op als de standaard rechtspersoon in gebruikersopties anders is. |
| 558347 | Bij het laden van de startpagina wordt 'Geen record in formulierconfiguraties (FormRunConfiguration)' weergegeven. | Personalisaties veroorzaken het foutbericht 'Geen record in formulierconfiguraties (FormRunConfiguration)' wanneer de startpagina wordt geladen. |
| 557327 | Werkruimte voor vergoedingenbeheer: boven het raster wordt een hiaat weergegeven. | Probleem opgelost met gebruikerservaring met een onbedoeld hiaat dat wordt weergegeven op de randen van het tabelraster in de werkruimte Vergoedingen. |
| 557334 | Werkruimte Vergoedingenbeheer: vervolgkeuzevak voor selectie van **Periode** moet alleen worden weergegeven op het tabblad **Overzicht** | Vergoedingen vervolgkeuzevak voor de selectie van **Periode** verschijnt nu alleen als het tabblad **Overzicht** actief is in de werkruimte Vergoedingen en niet in de sectie **Procesresultaten** en **Koppelingen**. |
| 557336 | Werkruimte voor vergoedingenbeheer: de tekst **Openstaande inschrijving met uitgecheckte plannen** wordt ingekort in de tegelweergave | Tekst in de tegelweergave gewijzigd in **Uitgecheckte plannen... openstaande inschrijving** om afkapping van noodzakelijke context te vermijden. |

## <a name="in-preview"></a>Preview

Van de volgende nieuwe functies kan een voorbeeld worden bekeken. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het in- en uitschakelen van functies.

| Functie | Vrijgaveplan | Documentatie |
| --- | --- | --- |
| Werkgebied voor vergoedingenbeheer | [Werkruimte Vergoedingenbeheer (preview)](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Werkgebied voor vergoedingenbeheer](hr-benefits-management-workspace.md) |
| Voorkomen dat werknemers zakelijke contactgegevens bewerken | [Voorkomen dat werknemers zakelijke contactgegevens bewerken](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Bewerken van persoonlijke gegevens beperken](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>Binnenkort beschikbaar

| Functie | Gegevens |
| --- | --- |
| Vaardigheden die een manager voor diens werknemers invoert, kunnen automatisch worden goedgekeurd door een workflow | Binnenkort beschikbaar. |

Zie [Overzicht van Dynamics 365 Human Resources 2021 release wave 1](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) voor een volledige lijst met geplande functies en de bijbehorende geplande versies.

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van Dynamics 365 Human Resources 2021 release wave 1](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
