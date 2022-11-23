---
title: Aan de slag met hoofdplanning
description: In dit artikel wordt uitgelegd hoe u aan de slag gaat met de functionaliteit voor hoofdplanningen in Dynamics 365 Supply Chain Management.
author: t-benebo
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 4b986461e90b356580da8a136c1da95e7dc64696
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780407"
---
# <a name="get-started-with-master-planning"></a>Aan de slag met hoofdplanning

[!include [banner](../../includes/banner.md)]

De hoofdplanning in Supply Chain Management wordt geleverd door een externe service, de invoegservice Planningsoptimalisatie voor Dynamics 365 Supply Chain Management. In dit onderwerp wordt uitgelegd hoe u aan die service komt en de service instelt.

## <a name="availability"></a>Beschikbaarheid

Planningsoptimalisatie is momenteel beschikbaar in de volgende Azure-regio's: Verenigde Staten, Canada, Brazilië, Europa, Frankrijk, Verenigd Koninkrijk, Noorwegen, Zwitserland, Australië, Azië/Pacific, Japan en India. Als u de invoegtoepassing vanuit een andere geografische regio probeert te installeren, wordt in LCS een bericht weergegeven dat deze niet wordt ondersteund. Zie [Azure-regio's](https://azure.microsoft.com/global-infrastructure/geographies/#geographies) voor meer informatie over Azure-regio's en de verwante regio's.

Planningsoptimalisatie wordt niet ondersteund voor on-premises implementaties van Dynamics 365 Supply Chain Management.

## <a name="licensing"></a>Licenties

Als u de hoofdplanning kunt uitvoeren met uw huidige licentie, hoeft u geen extra licentie aan te schaffen om Planningsoptimalisatie te kunnen gebruiken.

## <a name="install-and-enable-planning-optimization"></a>Planningsoptimalisatie installeren en inschakelen

Als u Planningsoptimalisatie wilt gebruiken, moet u ervoor zorgen dat het systeem aan alle vereisten voldoet. Vervolgens moet u de licentiesleutel inschakelen en de invoegtoepassing Planningsoptimalisatie voor Dynamics 365 Supply Chain Management installeren.

### <a name="prerequisites"></a>Vereisten

Voordat u de invoegtoepassing Planningsoptimalisatie installeert, moet aan de volgende vereisten zijn voldaan:

- U moet Supply Chain Management uitvoeren in een omgeving met grote beschikbaarheid voor LCS, tier 2 of hoger (geen OneBox-omgeving), met Dynamics 365 Supply Chain Management versie 10.0.7 of hoger. Als u de invoegtoepassing in een OneBox-omgeving probeert te installeren, wordt de installatie niet voltooid en moet u de installatie annuleren.

- Uw systeem moet zijn ingesteld voor Power Platform-integratie. Zie [Microsoft Power Platform-integratie met apps voor financiën en bedrijfsactiviteiten](../../../fin-ops-core/dev-itpro/power-platform/overview.md) voor meer informatie.

### <a name="enable-the-planning-optimization-license"></a>De Planningsoptimalisatie-licentie inschakelen

Als u Planningsoptimalisatie wilt gebruiken, moet u de configuratiesleutel ervan activeren. U doet dit als volgt:

1. Plaats uw systeem in de onderhoudsmodus, zoals wordt beschreven in [Onderhoudsmodus](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Ga naar **Systeembeheer \> Instellingen \> Licentieconfiguratie**.
1. Schakel op het tabblad **Configuratiesleutels** het selectievakje in voor **Planningsoptimalisatie**.
1. Schakel de onderhoudsmodus uit, zoals wordt beschreven in [Onderhoudsmodus](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

### <a name="install-the-planning-optimization-add-in"></a>De invoegtoepassing Planningsoptimalisatie installeren

U moet de invoegtoepassing installeren vanuit uw LCS-project en vervolgens de functie Planningsoptimalisatie inschakelen via de gebruikersinterface van Supply Chain Management.

De invoegtoepassing Planningsoptimalisatie installeren:

1. Meld u aan bij LCS en open de gewenste omgeving.
1. Ga naar **Volledige details**.
1. Schuif omlaag naar het sneltabblad **Invoegtoepassingen voor omgeving**.
1. Selecteer **Een nieuwe invoegtoepassing installeren**.
1. Selecteer **Planningsoptimalisatie**.
1. Volg de installatiehandleiding en ga akkoord met de voorwaarden en bepalingen.
1. Selecteer **Installeren**.
1. Op het sneltabblad **Invoegtoepassingen voor omgeving** ziet u dat Planningsoptimalisatie wordt geïnstalleerd.
1. Na een paar minuten moet **Installeren** veranderen in **Geïnstalleerd** (u moet de pagina mogelijk vernieuwen). Wanneer Planningsoptimalisering is geïnstalleerd, kunt u het activeren in Dynamics 365 Supply Chain Management.

Het hoofddoel van het installeren van de invoegtoepassing Planningsoptimalisatie is het verbinden van de service en de omgeving. Daarom moet u de invoegtoepassing afzonderlijk installeren in elke omgeving waarin u Planningsoptimalisatie wilt gebruiken, ongeacht eventuele code die tussen de omgevingen wordt verplaatst.

## <a name="integrate-planning-optimization-with-your-system"></a>Planningsoptimalisatie integreren met uw systeem

Als u wilt configureren of de invoegtoepassing Planningsoptimalisatie moet worden gebruikt voor hoofdplanning, gaat u naar **Hoofdplanning** \> **Instellen** \> **Integratie van Planningsoptimalisatie**.

### <a name="connection-status"></a>Verbindingsstatus

De verbindingsstatus geeft de huidige status aan van de verbinding tussen Supply Chain Management en de service Planningsoptimalisatie. De volgende tabel bevat de mogelijke waarden.

| Verbindingsstatus | Beschrijving | Kan Planningsoptimalisatie worden gebruikt? |
|---|---|---|
| Verbonden | Er is een verbinding tot stand gebracht tussen de service Planningsoptimalisatie en Supply Chain Management. | Ja |
| Verbinding wordt ingeschakeld | Een aanvraag om de verbinding met de service Planningsoptimalisatie in te schakelen, wordt momenteel uitgevoerd. | Nee |
| Niet verbonden | Er is geen verbinding met de service Planningsoptimalisatie. De verbinding kan worden ingeschakeld vanuit LCS, zoals eerder in dit artikel is beschreven. | Nr. |
| Verbinding wordt uitgeschakeld | Een aanvraag om de verbinding met de service Planningsoptimalisatie uit te schakelen, wordt momenteel uitgevoerd. | Nee |
| Status ophalen | Het systeem wacht op statusinformatie van de service Planningsoptimalisatie. | Nee |

### <a name="the-use-planning-optimization-option"></a>De optie Planningsoptimalisatie gebruiken

De instelling van de optie **Planningsoptimalisatie gebruiken** bepaalt welke planningsengine wordt gebruikt voor de hoofdplanning:

- **Ja**: Planningsoptimalisatie wordt gebruikt voor de hoofdplanning.
- **Nee**: de afgeschafte hoofdplanningsengine wordt gebruikt voor de hoofdplanning.

Deze instelling is van toepassing op alle rechtspersonen (bedrijven). Het is niet mogelijk om Planningsoptimalisatie te gebruiken in bepaalde rechtspersonen en de afgeschafte hoofdplanningsengine in andere rechtspersonen.

> [!NOTE]
> Als bestaande planningsbatchtaken die zijn gemaakt voor de afgeschafte hoofdplanningsengine worden geactiveerd terwijl de optie **Planningsoptimalisatie gebruiken** is ingesteld op **Ja**, mislukken deze taken.

### <a name="integration-with-the-setup"></a>Integratie met de setup

Als Planningsoptimalisatie is ingeschakeld, wordt de hoofdplanning uitgevoerd met behulp van de invoegtoepassing Planningsoptimalisatie. In dit geval worden de resultaten en functies van de hoofdplanning beïnvloed.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
