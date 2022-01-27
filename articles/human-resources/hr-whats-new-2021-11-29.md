---
title: Nieuwe of gewijzigde functies in Dynamics 365 Human Resources (19 november 2021)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 19 november 2021.
author: marcelbf
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3a86c1c24fbc758f4e3d0fd8b052e02078bee41e
ms.sourcegitcommit: 88f8a0369ce66b82314db9639491b695e18a7e5c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902599"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-november-19-2021"></a>Nieuwe of gewijzigde functies in Dynamics 365 Human Resources (19 november 2021)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn of die binnenkort worden vrijgegeven in Microsoft Dynamics 365 Human Resources.

Zie [Updateproces](hr-admin-setup-update-process.md) voor meer informatie over het updateproces en de planning.

Zie [Dynamics 365 Human Resources 2021 release wave 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/) voor meer informatie over nieuwe functies en de verwachte algemene beschikbaarheidsdatums ervan.

## <a name="in-this-release"></a>In deze versie

Deze versie omvat de volgende correcties. Wijzigingen die van toepassing zijn op buildnummer 8.1.4591.

### <a name="bug-fixes"></a>Correcties

Deze versie bevat de volgende correcties.

> [!NOTE]
> Ons doel is om deze informatie zo snel mogelijk bij u te krijgen. Mogelijk wordt dit onderwerp gewijzigd om correcties op te nemen die in de build zijn gemaakt nadat dit onderwerp oorspronkelijk werd gepubliceerd.

| Probleemnummer | Probleem | Description |
|---|---|---|
| 626178 | Navigatie ontbreekt op de medewerkerstegels in **Selfservice manager** | Dit probleem is nu opgelost. De navigatie is beschikbaar voor het bekijken van de rapportdetails in **Selfservice manager**. |
| 632573 | Er is geen validatiefout bij het opslaan van een **cursus** | Dit probleem is nu opgelost. Bij het maken van een cursus waarvoor **Minimum aantal deelnemers** was ingesteld op een waarde hoger dan 0 kon de cursus ook worden opgeslagen als **Maximum aantal deelnemers** 0 was. |
| 615955 | Het foutbericht Het veld **Doel** moet worden ingevuld wordt weergegeven bij maken van een nieuwe locatie voor wervingsverzoeken. | Wanneer u een adres voor een nieuwe locatie voor wervingsverzoeken maakt, wordt het foutbericht Het veld Doel moet worden ingevuld weergegeven. Het veld **Doel** is echter niet beschikbaar op de pagina. |
| 620797 | De fout voor het lege veld **Geslacht** is misleidend | Wanneer geen geslacht niet voor een persoonlijke contactpersoon wordt ingevoerd, wordt in het rapport 'Klik hier of tik hier om tekst in te voeren' weergegeven. Dat is misleidend omdat er niets in het veld kan worden ingevoerd. |
| 620800 | De koppeling Vergoedingenoverzicht is verborgen | Het vergoedingenoverzicht is niet standaard weer te geven in **Selfservice werknemer**.  Er is een koppeling toegevoegd aan de rechterkant van **Selfservice werknemer** onder de sectie **Koppelingen** |
| 629778 | Prestatieprobleem met CDS-integratie. | Een prestatieprobleem werd veroorzaakt door een autorisatiegerelateerde aanvraag. |

## <a name="in-preview"></a>Preview

Van de volgende nieuwe functies kan een voorbeeld worden bekeken. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het in- en uitschakelen van functies.

| Functie | Vrijgaveplan | Documentatie |
|---|---|---|
| Werkgebied voor vergoedingenbeheer | [Werkruimte Vergoedingenbeheer (preview)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Werkgebied voor vergoedingenbeheer](hr-benefits-management-workspace.md) |


## <a name="coming-soon"></a>Binnenkort beschikbaar
Zie [Dynamics 365- en bedrijfsclouds: releasewave 2-plan van 2021](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/) voor een volledige lijst met geplande functies en de bijbehorende geplande versies.

[!INCLUDE[footer-include](../includes/footer-banner.md)]