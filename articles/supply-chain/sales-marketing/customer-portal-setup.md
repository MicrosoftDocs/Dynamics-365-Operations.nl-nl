---
title: De klantportal installeren, instellen en bijwerken
description: In dit onderwerp vindt u instructies voor licenties en instelling voor de klantportal.
author: dasani-madipalli
manager: tfehr
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 2153bbca2be7c72e48b9dc51b1f7fdbe2ab89903
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977733"
---
# <a name="install-set-up-and-update-the-customer-portal"></a>De klantportal installeren, instellen en bijwerken

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="licensing-requirements"></a>Licentievereisten

Voor het implementeren van de klantportal hebt u de volgende licenties nodig:

- **Power Apps-portals**: deze licentie is vereist om de klantportal te hosten. Portals worden op basis van gebruik in licentie gegeven. Zie [Licentievereisten voor Power Apps-portals](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals) voor meer informatie.
- **Twee keer wegschrijven**: u moet over de vereiste licenties beschikken om twee keer wegschrijven in te schakelen voor Supply Chain Management-tabellen. Zie [Systeemvereisten voor twee keer wegschrijven](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md) voor meer informatie.

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a>Afhankelijkheden voor twee keer wegschrijven en Power Apps-portals

De klantportal is afhankelijk van Power Apps-portals en bewerkingen voor twee keer wegschrijven, zoals wordt weer gegeven in de volgende afbeelding.

![Afhankelijkheden van klantportal](media/customer-portal-elements.png "Afhankelijkheden van klantportal")

In tegenstelling tot andere functies van Supply Chain Management, bevindt de klantportalsjabloon zich in Power Apps-portals. Daarom wordt de klantportal beperkt door de functionaliteit en capaciteiten die door Power Apps-portals en de tabellen in twee keer wegschrijven worden geleverd.

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a>Vereiste instellingen om de klantportal in te schakelen

Nadat u hebt vastgesteld dat u over de vereiste licenties beschikt, kunt u Twee keer wegschrijven instellen zoals beschreven in de [Initiële synchronisatie-instructies voor Twee keer wegschrijven](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).

Zorg ervoor dat u de volgende tabeltoewijzingen in twee keer wegschrijven inschakelt:

- Koptekst van verkooporder
- Details verkooporder
- Rekeningen
- Contactpersonen
- Producten

Nadat deze instellingen zijn voltooid, kunt u de sjabloon voor de klantportal inrichten.

## <a name="provision-the-customer-portal"></a>De klantportal inrichten

Controleer voordat u begint of u de [vereiste instellingen](#required-setup) al hebt uitgevoerd. Voer vervolgens de volgende stappen uit om de klantportal in te richten.

1. Ga naar [make.powerapps.com](https://make.powerapps.com/).
2. Controleer of u de omgeving gebruikt waarin u twee keer wegschrijven hebt ingeschakeld.
3. Ga naar het tabblad **Maken**, blader naar de sectie **Beginnen bij sjabloon** en selecteer de sjabloon met de naam **Klantportal**.
4. Volg de instructies op het scherm.

Nadat de inrichting is voltooid, kunt u de klantportal openen via de sectie **Uw apps** op de **Startpagina**.

> [!NOTE]
> Als de oplossing voor dubbel schrijven niet is geïnstalleerd in de omgeving waarin u werkt, wordt er een foutbericht weergegeven en wordt de klantportal niet ingericht.

## <a name="update-the-customer-portal"></a>De klantportal bijwerken

Later wordt mogelijk meer functionaliteit aan de klantportal toegevoegd. Eventuele wijzigingen die Microsoft in de onderliggende oplossingsonderdelen aanbrengt, worden automatisch weergegeven in uw omgeving. Op de website die in uw omgeving wordt ingericht, worden echter niet automatisch wijzigingen weergegeven die in de configuratiegegevens zijn aangebracht. U moet deze wijzigingen handmatig toepassen door de code op te halen uit de nieuwe sjabloon en deze samen te voegen met de ingerichte website.

## <a name="additional-resources"></a>Aanvullende bronnen

Als u wilt weten hoe u de klantportal kunt instellen en aanpassen, moet u eerst de volgende documentatie voor de onderliggende technologieën controleren:

- [Documentatie over Power Apps-portals](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [Documentatie over twee keer wegschrijven](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

Om uw portals effectief te beheren, moet u inzicht hebben in de Power Apps-portals en Microsoft Dataverse-levenscyclus. Voor meer informatie raadpleegt u de volgende bronnen:

- [Informatie over Portallevenscyclus](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [Een portal bijwerken](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [Portalconfiguratie migreren](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [Solution Lifecycle Management: Dynamics 365 voor Customer Engagement-apps](https://www.microsoft.com/download/details.aspx?id=57777)
