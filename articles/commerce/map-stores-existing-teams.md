---
title: Winkels en teams toewijzen als er reeds bestaande teams in Microsoft Teams zijn
description: In dit onderwerp wordt beschreven hoe u winkels en bijbehorende teams in Dynamics 365 Commerce Headquarters toewijst als uw organisatie al teams heeft gemaakt in Microsoft Teams vóór de Commerce-integratie.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: aafeaa1da3c3dab5d76a6bfcee06db34a6afba91
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691100"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a>Winkels en teams toewijzen als er reeds bestaande teams in Microsoft Teams zijn

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u winkels en bijbehorende teams in Dynamics 365 Commerce Headquarters toewijst als uw organisatie al teams heeft gemaakt in Microsoft Teams vóór de Commerce-integratie.

Uw organisatie heeft mogelijk teams gemaakt voor sommige of al uw winkels voordat de integratie van Dynamics 365 Commerce en Microsoft Teams plaatsvindt. Als dit het geval is, moet u de toewijzing van winkels en het bijbehorende team in Commerce Headquarters opgeven om taaksynchronisatie tot stand te brengen tussen Commerce POS en Microsoft Teams.

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a>Winkels en bijbehorende teams toewijzen in Commerce Headquarters 

Voer de volgende stappen uit om winkels en bijbehorende teams toe te wijzen in Commerce Headquarters.

1. Ga naar **Systeembeheer \> Werkruimte \> Gegevensbeheer**.
1. Selecteer **Exporteren**. 
1. Selecteer **Nieuw** in het actievenster.
1. Voer onder **Groepsnaam** 'Teams-toewijzing exporteren' in.
1. Selecteer op het sneltabblad **Geselecteerde entiteiten** de optie **Entiteit toevoegen**. Het dialoogvenster **Entiteit toevoegen** wordt weergegeven.  
1. Selecteer **Teams-toewijzing tussen bron en team** in de vervolgkeuzelijst **Entiteitsnaam**.
1. Selecteer **CSV** in de vervolgkeuzelijst **Indeling doelgegevens**.
1. Selecteer **Toevoegen** en vervolgens **Sluiten**.
1. Selecteer de optie **Nu exporteren** linksboven onder het actievenster.
1. Selecteer **Bestand downloaden** onder **Verwerkingsstatus entiteit**.
1. Voer in het geëxporteerde CSV-bestand als volgt de waarden voor **SOURCETYPE**, **SOURCEID** en **TEAMID** in:
    - Voer voor **SOURCETYPE** de waarde 'RetailStore' in. 
    - Voer voor **SOURCEID** het winkelnummer in (bijvoorbeeld '000135' voor de winkel in San Francisco). U kunt winkelnummers vinden bij **Retail en commerce \> Afzetkanalen \> Winkels**.
    - Voer voor **TEAMID** de bijbehorende team-id in vanuit Microsoft Teams (bijvoorbeeld '5f8bc92b-6aa8-451e-85d1-3949c01ddc6c'). U kunt informatie over de team-id vinden op [admin.teams.microsoft.com](https://admin.teams.microsoft.com).
1. Sla het CSV-bestand op uw lokale computer op.
1. Ga naar **Systeembeheern \> Werkruimte \> Gegevensbeheer** en selecteer vervolgens **Importeren**.
1. Selecteer op het sneltabblad **Geselecteerde entiteiten** de optie **Bestand toevoegen**. Het dialoogvenster **Bestand toevoegen** wordt weergegeven.
1. Selecteer **Teams-toewijzing tussen bron en team** in de vervolgkeuzelijst **Entiteitsnaam**.
1. Selecteer **CSV** in de vervolgkeuzelijst **Indeling brongegevens**.
1. Selecteer **Uploaden en toevoegen**, selecteer het CSV-bestand dat u eerder hebt opgeslagen en selecteer vervolgens **Openen**.
1. Selecteer in het dialoogvenster **Bestand toevoegen** de optie **Sluiten**.
1. Selecteer in het actievenster **Opslaan** en vervolgens **Importeren**.

In de volgende voorbeeldafbeelding ziet u de groep **Teams-toewijzing exporteren** in Commerce met de elementen **Entiteit toevoegen** en de geëxporteerde CSV-bestandskoppen gemarkeerd.

![Groep Teams-toewijzing exporteren in Commerce met de elementen Entiteit toevoegen en de geëxporteerde CSV-bestandskoppen gemarkeerd.](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> Nadat u de voorafgaande stappen hebt voltooid, volgt u de stappen in [Taakbeheer synchroniseren tussen Microsoft Teams en POS](synchronize-tasks-teams-pos.md) om taakbeheer te synchroniseren. 

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van integratie van Dynamics 365 Commerce en Microsoft Teams](commerce-teams-integration.md)

[Integratie van Dynamics 365 Commerce en Microsoft Teams inschakelen](enable-teams-integration.md)

[Microsoft Teams inrichten vanuit Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Taakbeheer synchroniseren tussen Microsoft Teams en Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Gebruikersrollen beheren in Microsoft Teams](manage-user-roles-teams.md)

[Veelgestelde vragen over integratie van Dynamics 365 Commerce en Microsoft Teams](teams-integration-faq.md)
