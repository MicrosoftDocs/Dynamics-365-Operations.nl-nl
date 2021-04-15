---
title: Dynamics 365 Supply Chain Management (Asset Management) integreren met Dynamics 365 Guides
description: In dit onderwerp wordt uitgelegd hoe u de module Asset Management in Microsoft Dynamics 365 Supply Chain Management kunt integreren met Dynamics 365 Guides om de mixed-reality guides toe te passen in uw dagelijkse service- en onderhoudswerkstromen.
author: kamaybac
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 4af14a66c839ccee02008057ad1de8ef5b9d291b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813912"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a>Dynamics 365 Supply Chain Management (Asset Management) integreren met Dynamics 365 Guides

U kunt de module **Asset Management** in Microsoft Dynamics 365 Supply Chain Management integreren met Dynamics 365 Guides om de mixed-reality guides toe te passen in uw dagelijkse service- en onderhoudswerkstromen. Als er een guide is gekoppeld aan een Asset Management-werkorder, ziet een werknemer die de onderhoudscontrolelijst van de werkorder opent in de mobiele app Supply Chain Management (Dynamics 365) dat er een guide beschikbaar is. De werknemer kan vervolgens de guide zoeken en openen in de Dynamics 365 Guides HoloLens-app.

## <a name="prerequisites"></a>Vereisten

Voordat u guides kunt koppelen aan werkorders voor Asset Management, moet u de volgende vereisten voltooien:

- [Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) versie 10.0.9 of later installeren.
- [Twee keer wegschrijven inschakelen voor Supply Chain Management-apps](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).
- [Flight inschakelen](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) voor de functie **MRGuidesFeature**. (Voor productieomgevingen moet u eerst een ondersteuningsticket indienen om uw tenant aan de flightinggroep toe te voegen.)
- [Schakel de volgende configuratiesleutels](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) in op de pagina **Licentieconfiguratie**:

    - Asset Management \> Asset Management mixed reality
    - Mixed reality \> Mixed reality-guide

- [Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) versie 200.0.0.96 of later installeren.

## <a name="use-dynamics-365-guides-with-asset-management"></a>Dynamics 365 Guides gebruiken met Asset Management

Als u een guide wilt koppelen, gebruikt u een regel in de onderhoudscontrolelijst in Asset Management. U kunt de koppeling maken via een sjabloon voor de onderhoudscontrolelijst, een onderhoudstaaktype of een werkorder, omdat deze drie regels voor onderhoudscontrolelijsten bevatten. U kunt tijd besparen met een sjabloon, omdat een sjabloon kan worden gekoppeld aan alle onderhoudstaaktypen die hiervan gebruikmaken. Een guide die is gekoppeld aan een onderhoudstaaktype, wordt bijvoorbeeld automatisch gekoppeld aan alle werkorders waarmee het taaktype wordt opgegeven. Anderzijds bestaat een guide die alleen voor die werkorder direct aan een werkorder wordt gekoppeld.

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a>Een guide aan een sjabloon voor onderhoudscontrolelijsten koppelen

Voer de volgende stappen uit om een guide aan een sjabloon voor onderhoudscontrolelijsten te koppelen.

1. Maak een guide met de apps Dynamics 365 Guides voor pc en HoloLens. De volgende onderwerpen bevatten informatie over het maken van guides:

    - [De pc-app gebruiken om een guide te maken](https://docs.microsoft.com/dynamics365/mixed-reality/guides/pc-app-overview)
    - [De HoloLens-app gebruiken om uw hologrammen te plaatsen](https://docs.microsoft.com/dynamics365/mixed-reality/guides/hololens-app-overview)

1. Maak in Supply Chain Management [een sjabloon voor onderhoudscontrolelijsten](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).
1. Koppel de guide die u hebt gemaakt aan een regel voor de onderhoudscontrolelijst in de nieuwe sjabloon voor onderhoudscontrolelijsten:

    1. Selecteer op het sneltabblad **Regels onderhoudscontrolelijsten** de regel waaraan u de guide wilt koppelen.
    1. Selecteer op het sneltabblad **Gekoppelde guides** de optie **Guide toevoegen**.

        ![Een guide aan een regel van een onderhoudscontrolelijst koppelen](media/am-guides-integration-add-guide.png "Een guide aan een regel van een onderhoudscontrolelijst koppelen")

    1. Selecteer in het veld **Naam** een guide en selecteer vervolgens **Opslaan**.

        ![Een guide selecteren in het veld Naam](media/am-guides-integration-select-guide.png "Een guide selecteren in het veld Naam")

1. De sjabloon voor onderhoudscontrolelijsten koppelen aan een taaktype:

    1. [Maak een onderhoudstaaktype](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type) of selecteer een bestaand type onderhoudstaak.
    1. Selecteer in het actievenster **Standaardwaarden voor het onderhoudstaaktype**.

        ![Knop voor standaardinstellingen voor onderhoudstaaktypen](media/am-guides-integration-job-defaults.png "Knop voor standaardinstellingen voor onderhoudstaaktypen")

    1. Maak een regel en selecteer vervolgens **Opslaan**.

        ![Een regel maken](media/am-guides-integration-add-line.png "Een regel maken")

    1. Selecteer in het actievenster de optie **Onderhoudscontrolelijst**.

        ![Knop Onderhoudscontrolelijst](media/am-guides-integration-maintenance-checklist.png "Knop Onderhoudscontrolelijst")

    1. Voeg op het sneltabblad **Regels onderhoudscontrolelijsten** een regel toe en wijzig vervolgens de waarde van het veld **Type** in **Sjabloon**.

        ![De waarde voor Type wijzigen](media/am-guides-integration-checklist-lines.png "De waarde voor Type wijzigen")

    1. Selecteer op het sneltabblad **Regeldetails** in het veld **Sjabloon** de sjabloon waaraan u de guide hebt gekoppeld en selecteer vervolgens **Opslaan**.

        ![De sjabloon selecteren](media/am-guides-integration-checklist-line-details.png "De sjabloon selecteren")

1. [Maak een werkorder](work-orders/manually-created-workorders.md#create-work-order) en selecteer het type onderhoudstaak dat gebruikmaakt van de sjabloon voor onderhoudscontrolelijsten waaraan u de guide hebt gekoppeld. De guide wordt automatisch gekoppeld aan de werkorder.

    ![Een type onderhoudstaak selecteren](media/am-guides-integration-create-work-order.png "Een type onderhoudstaak selecteren")

1. Bekijk de guide die aan de werkorder en werknemers is gekoppeld:

    1. Open de [mobiele werkruimte Asset Management](asset-management-mobile-workspace.md) om de werkorder te openen.
    1. [Open de onderhoudscontrolelijst](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) voor de werkorder.
    1. Selecteer een controlelijstregel om de bijbehorende guide weer te geven.

        ![Guide gekoppeld met een controlelijstregel](media/am-guides-integration-show-guide.png "Guide gekoppeld met een controlelijstregel")

    1. Open de guide op HoloLens.

        ![De guide on HoloLens openen](media/am-guides-integration-hololens-select.png "De guide op HoloLens openen")

> [!NOTE]
> U kunt een guide ook rechtstreeks aan de controlelijst voor onderhoud van een werkorder of taaktype koppelen.

> [!IMPORTANT]
> Er is een bekend probleem dat optreedt wanneer u een sjabloon voor onderhoudscontrolelijsten aan een standaard onderhoudstaaktype koppelt. De guide die aan de sjabloon is gekoppeld, wordt dan niet weergegeven op het sneltabblad **Gekoppelde guides** van de pagina **Standaardinstellingen onderhoudstaaktype**. De guide wordt echter weergegeven nadat het taaktype is toegepast op een werkorder op het sneltabblad **Gekoppelde guides**.

## <a name="see-also"></a>Zie ook

- [Overzicht van twee keer wegschrijven](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [Overzicht van activabeheer](index.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]