---
title: Common Data Service-integratie configureren
description: U kunt de integratie tussen Common Data Service en Dynamics 365 Human Resources in- of uitschakelen. U kunt ook synchronisatiegegevens weergeven, traceringsgegevens wissen en een entiteit opnieuw synchroniseren als hulp bij het oplossen van problemen tussen de twee omgevingen.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7aad8217d48917d6855046a6810fe994f5564d94
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431309"
---
# <a name="configure-common-data-service-integration"></a>Common Data Service-integratie configureren

U kunt de integratie tussen Common Data Service en Dynamics 365 Human Resources in- of uitschakelen. U kunt ook de synchronisatiegegevens weergeven, traceringsgegevens wissen en een entiteit opnieuw synchroniseren als hulp bij het oplossen van problemen tussen de twee omgevingen.

Wanneer u integratie uitschakelt, kunnen gebruikers wijzigingen aanbrengen in Human Resources of Common Data Service, maar deze wijzigingen worden niet gesynchroniseerd tussen de twee omgevingen.

Integratie tussen Human Resources en Common Data Service is standaard uitgeschakeld.

Mogelijk wilt u integratie in de volgende situaties uitschakelen:

- U vult gegevens in via het Data Management Framework en u moet de gegevens meerdere keren importeren om de juiste status te krijgen.

- Er zijn problemen met gegevens in Human Resources of Common Data Service. Als u integratie uitschakelt, kunt u een record in de ene omgeving verwijderen zonder deze in de andere omgeving te verwijderen. Wanneer u de integratie weer inschakelt, wordt de record in de omgeving waarin deze niet is verwijderd, gesynchroniseerd naar de omgeving waarin deze was verwijderd. De synchronisatie begint de volgende keer dat de batchtaak **Gemiste aanvragen Common Data Service-integratie synchroniseren** wordt uitgevoerd.

> [!WARNING]
> Wanneer u gegevensintegratie uitschakelt, moet u niet dezelfde record in beide omgevingen bewerken. Wanneer u de integratie weer inschakelt, wordt de record die u als laatste hebt bewerkt, gesynchroniseerd. Als u in beide omgevingen niet dezelfde wijzigingen in de record hebt aangebracht, kan er gegevensverlies optreden.

## <a name="access-the-common-data-service-integration-page"></a>Toegang tot de pagina Common Data Service-integratie

1. Selecteer in het Human Resources-exemplaar waarin u de instellingen voor de integratie met Common Data Service wilt weergeven of configureren, de tegel **Systeembeheer**.

    [![Tegel Systeembeheer](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. Selecteer het tabblad **Koppelingen**.

    [![Tabblad Koppelingen](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. Selecteer onder **Integraties** de optie **Common Data Service-configuratie**.

    [![Koppeling Common Data Service-configuratie](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a>Gegevensintegratie tussen Human Resources en Common Data Service in- of uitschakelen

- Als u de integratie wilt inschakelen, stelt u de optie **De integratie met Common Data Service inschakelen** in op **Ja**.

    > [!NOTE]
    > Wanneer u de integratie inschakelt, worden de gegevens gesynchroniseerd wanneer de batchtaak **Gemiste aanvragen Common Data Service-integratie synchroniseren** de volgende keer wordt uitgevoerd. Alle gegevens zijn als het goed is beschikbaar nadat de batchtaak is voltooid.

- Als u de integratie wilt uitschakelen, stelt u de optie in op **Nee**.

[![De Common Data Service-integratie in- of uitschakelen](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)

## <a name="view-data-integration-details"></a>Details van de gegevensintegratie weergeven

Op het sneltabblad **Beheer** van de pagina **Common Data Service-integratie** kunt u zien hoe de records in Human Resources en Common Data Service aan elkaar zijn gekoppeld.

- Als u de records voor een entiteit wilt weergeven, selecteert u de entiteit in het veld**CDS-entiteitsnaam**. In het raster worden alle records weergegeven die zijn gekoppeld aan de geselecteerde entiteit.

[![De records voor een entiteit weergeven](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)

> [!NOTE]
> Niet alle Common Data Service-entiteiten worden op dit moment in het raster weergegeven. Alleen entiteiten die het gebruik van aangepaste velden ondersteunen, worden weergegeven in het raster. Nieuwe entiteiten worden beschikbaar via doorlopende releases van Human Resources.

Het raster bevat de volgende velden:

- **CDS-entiteitsnaam** – De naam van de entiteit in Common Data Service.
- **CDS-entiteitsverwijzing** – De id die in Common Data Service wordt gebruikt om een record aan te duiden. Deze waarde is gelijk aan de **RecId**-waarde van Human Resources. U kunt de id vinden wanneer u de Common Data Service-entiteit opent in Microsoft Excel.
- **Human Resources-entiteitsnaam** – De entiteit die als laatste gegevens heeft gesynchroniseerd naar Common Data Service. De entiteit kan het voorvoegsel Common Data Service of een ander voorvoegsel hebben.
- **Human Resources-verwijzing** – De **RecId**-waarde die is gekoppeld aan de record in Human Resources.
- **Is verwijderd uit CDS** – Een waarde die aangeeft of de record is verwijderd uit Common Data Service.

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a>De koppeling van een record in Human Resources verwijderen uit Common Data Service

Als u problemen ondervindt tijdens de gegevenssynchronisatie tussen Human Resources en Common Data Service, kunt u deze mogelijk oplossen door de traceringsgegevens te wissen en de traceringstabel opnieuw te synchroniseren. Als u de koppeling verwijdert en vervolgens een record wijzigt of verwijdert in Common Data Service, worden de wijzigingen niet gesynchroniseerd naar Human Resources. Als u wijzigingen aanbrengt in Human Resources, wordt er een nieuwe traceringsrecord gemaakt en wordt de record bijgewerkt in Common Data Service.

- Als u de koppeling van een record tussen Human Resources en Common Data Service wilt verwijderen, selecteert u de entiteit in het veld **CDS-entiteitsnaam** en selecteert u vervolgens de optie **Traceringsgegevens wissen**.

[![Traceringsgegevens wissen](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)

Zie de volgende procedure als u een volledige synchronisatie wilt uitvoeren op de entiteit nadat u de traceringsgegevens hebt gewist.

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a>Een entiteit synchroniseren tussen Human Resources en Common Data Service

Gebruik deze procedure als:

- De wijzigingen van Common Data Service te lang duren om te worden weergegeven in Human Resources.

- U moet de traceringstabel vernieuwen nadat u de tracering hebt gewist.

Een volledige synchronisatie uitvoeren voor een entiteit tussen Human Resources en Common Data Service:

1. Selecteer de entiteit in het veld **CDS-entiteitsnaam**.

2. Selecteer **Nu synchroniseren**.

[![Een volledige synchronisatie uitvoeren](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)


