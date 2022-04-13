---
title: Een teamkalender aanmaken
description: Geef teamkalenders weer en maak deze in Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 963df35247285ad764a814daa4b51eff35207d97
ms.sourcegitcommit: 67c4ed957e43d4d60bb609d93921a0be9619e675
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2022
ms.locfileid: "8509355"
---
# <a name="view-team-and-company-calendars"></a>Team- en bedrijfsagenda's weergeven

>[!Important]
>De functionaliteit die in dit onderwerp wordt vermeld, is momenteel beschikbaar voor klanten van de zelfstandige versie van Dynamics 365 Human Resources. Sommige of alle functionaliteit is beschikbaar als onderdeel van een toekomstige versie van de Finance-infrastructuur na versie 10.0.26 van Finance.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

U kunt team- en bedrijfskalenders weergeven in Dynamics 365 Human Resources. In teamkalenerds worden alleen directe rapporten weergegeven, zoals gedefinieerd in de regelhiërarchie.

## <a name="view-your-team-calendar-as-an-employee"></a>Uw teamkalender als werknemer weergeven

- Selecteer in het werkgebied **Selfservice werknemer** de optie **Teamverzuimkalender** onder **Overzicht**.

## <a name="view-your-team-calendar-as-a-manager"></a>Uw teamkalender als manager weergeven

1. Selecteer in het werkgebied **Selfservice werknemer** de optie **Mijn team**.

2. Selecteer **Verlof en verzuim** en selecteer vervolgens **Verzuimkalender manager weergeven**.

Managers kunnen ook toegang krijgen tot de teamkalender via **Uitstaande verlofaanvragen voor mijn team**, **Goedgekeurd verlof** en **Verlofaanvragen**. 

## <a name="view-your-absence-manager-calendar-as-the-absence-manager"></a>De verzuimmanagerkalender weergeven als verzuimmanager

> [!NOTE]
> Als u de verzuimmanagerkalender wilt weergeven, moet u eerst de functie **(Preview) Verlof laten beheren door een verzuimmanager** in Functiebeheer inschakelen. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het inschakelen van preview-functies.

Gebruikers met de rol van verzuimmanager kunnen verlofaanvragen op hun kalender bekijken. Voer deze stappen uit om toegang tot de verlofkalender te krijgen.

1. Selecteer in de werkruimte **Selfservice werknemer** **Verlofbeheer** en vervolgens **Kalender verzuimmanager**.

2. Voer in het veld **Datum** de gewenste datum in.

3. Werk waar nodig de weergaveopties bij.

De kalender van de verzuimmanager bevat alle records voor de werknemers die rapporteren aan de verzuimmanager in de verlofhiërarchie.

## <a name="view-a-company-calendar"></a>Een bedrijfskalender weergeven

Mensen in Human Resources-rollen kunnen bedrijfskalenders weergeven. In bedrijfs kalenders worden alle werknemers weergegeven. Standaard wordt in de kalender de datum van vandaag plus 28 dagen weergegeven, maar u kunt het datumbereik wijzigen. U kunt de kalender ook filteren op **naam**, **personeelsnummer** en **verloftype**.

1. Selecteer in het werkgebied **Verlof en verzuim** de optie **Koppelingen**.

2. Selecteer **Verlof- en verzuimkalender**.

Rollen van Human Resources kunnen ook toegang krijgen tot de bedrijfskalender via **Aanvragen voor verlof en verzuim**, **Goedgekeurd verlof** en **Verlofaanvragen**. 

Kalenders bevatten nu extra filters en opties. Alle kalenders bevatten weergaveopties voor:

- Goedgekeurde aanvragen
- Aanvragen in behandeling
- Werknemers met verlofaanvragen
- Werknemers zonder verlofaanvragen
- Verjaardagen van werknemers
- Verlofaanvragen 
- Verlofaanvragen

Kalenderconfiguratie in de pagina **Verlof- en verzuimparameters** bepaalt de beschikbare weergaveopties.

U kunt kalenders ook filteren op manager of afdeling. De primaire positietoewijzing bepaalt welke werknemers worden weergegeven wanneer deze filters zijn ingesteld. 

> [!IMPORTANT]
> U kunt de functie **Verlofweergave voor het hele bedrijf** inschakelen in Functiebeheer. U moet vervolgens de functie op de pagina **Gedeelde Human Resources-parameters** inschakelen om de rechtspersoonfilter in kalenders weer te geven. Zie [Verlof- en verzuimparameters configureren](hr-leave-and-absence-parameters.md) voor meer informatie.
> 
> U kunt de kalender filteren op rechtspersoon. Als u alle werknemers wilt weergeven, ongeacht de rechtspersoon, wist u het filterveld en selecteert u vervolgens **Invoeren**. 

Zie [Kalenderparameters configureren](hr-leave-and-absence-parameters.md?configure-calendar-parameters) voor meer informatie over kalenderinstellingen.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
