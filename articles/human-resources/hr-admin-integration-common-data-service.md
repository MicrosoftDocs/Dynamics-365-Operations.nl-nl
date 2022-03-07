---
title: Dataverse-integratie configureren
description: U kunt de integratie tussen Microsoft Dataverse en Dynamics 365 Human Resources in- of uitschakelen. U kunt ook synchronisatiegegevens weergeven, traceringsgegevens wissen en een tabel opnieuw synchroniseren als hulp bij het oplossen van problemen tussen de twee omgevingen.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1a1ee5345e2d6b3736d45e233a59ac4009a9f1c8
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344683"
---
# <a name="configure-dataverse-integration"></a>Dataverse-integratie configureren

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

U kunt de integratie tussen Microsoft Dataverse en Dynamics 365 Human Resources in- of uitschakelen. U kunt ook de synchronisatiegegevens weergeven, traceringsgegevens wissen en een tabel opnieuw synchroniseren als hulp bij het oplossen van problemen tussen de twee omgevingen.

> [!NOTE]
> Voor meer informatie over Dataverse (voorheen Common Data Service) en bijgewerkte terminologie, zie [Wat is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

Wanneer u integratie uitschakelt, kunnen gebruikers wijzigingen aanbrengen in Human Resources of Dataverse, maar deze wijzigingen worden niet gesynchroniseerd tussen de twee omgevingen.

Integratie tussen Human Resources en Dataverse is standaard uitgeschakeld.

Mogelijk wilt u integratie in de volgende situaties uitschakelen:

- U vult gegevens in via het Data Management Framework en u moet de gegevens meerdere keren importeren om de juiste status te krijgen.

- Er zijn problemen met gegevens in Human Resources of Dataverse. Als u integratie uitschakelt, kunt u een record in de ene omgeving verwijderen zonder deze in de andere omgeving te verwijderen. Wanneer u de integratie weer inschakelt, wordt de record in de omgeving waarin deze niet is verwijderd, gesynchroniseerd naar de omgeving waarin deze was verwijderd. De synchronisatie begint de volgende keer dat de batchtaak **Gemiste aanvragen Dataverse-integratie synchroniseren** wordt uitgevoerd.

> [!WARNING]
> Wanneer u gegevensintegratie uitschakelt, moet u niet dezelfde record in beide omgevingen bewerken. Wanneer u de integratie weer inschakelt, wordt de record die u als laatste hebt bewerkt, gesynchroniseerd. Als u in beide omgevingen niet dezelfde wijzigingen in de record hebt aangebracht, kan er gegevensverlies optreden.

## <a name="access-the-dataverse-integration-page"></a>Toegang tot de pagina Dataverse-integratie

1. Selecteer in het Human Resources-exemplaar waarin u de instellingen voor de integratie met Dataverse wilt weergeven of configureren, de tegel **Systeembeheer**.

    [![Tegel Systeembeheer.](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. Selecteer het tabblad **Koppelingen**.

    [![Tabblad Koppelingen.](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. Selecteer onder **Integraties** de optie **Dataverse-configuratie**.

    [![Koppeling Dataverse-configuratie.](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a>Gegevensintegratie tussen Human Resources en Dataverse in- of uitschakelen

- Als u de integratie wilt inschakelen, stelt u de optie **Dataverse-integratie inschakelen** in op **Ja** op de pagina **Microsoft Dataverse-integratie**.

    > [!NOTE]
    > Wanneer u de integratie inschakelt, worden de gegevens gesynchroniseerd wanneer de batchtaak **Gemiste aanvragen Dataverse-integratie synchroniseren** de volgende keer wordt uitgevoerd. Alle gegevens zijn als het goed is beschikbaar nadat de batchtaak is voltooid.

- Als u de integratie wilt uitschakelen, stelt u de optie in op **Nee**.

[![De Dataverse-integratie in- of uitschakelen.](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)

> [!WARNING]
> Het wordt nadrukkelijk aanbevolen om Dataverse-integratie uit te schakelen tijdens het uitvoeren van gegevensmigratietaken. Grote gegevensuploads kunnen de prestaties aanzienlijk beïnvloeden. Het uploaden van 2000 werknemers kan bijvoorbeeld enkele uren duren wanneer integratie is ingeschakeld, en minder dan een uur wanneer het is uitgeschakeld. De getallen die in dit voorbeeld worden gegeven, zijn alleen voor demonstratiedoeleinden. De exacte hoeveelheid tijd die nodig is voor het importeren van records kan sterk variëren op basis van een groot aantal factoren.

## <a name="view-data-integration-details"></a>Details van de gegevensintegratie weergeven

Op het sneltabblad **Beheer** van de pagina **Microsoft Dataverse-integratie** kunt u zien hoe de rijen in Human Resources en Dataverse aan elkaar zijn gekoppeld.

- Als u de rijen voor een tabel wilt weergeven, selecteert u de tabel in het veld **Dataverse-tabel**. In het raster worden alle rijen weergegeven die zijn gekoppeld aan de geselecteerde tabel.

> [!NOTE]
> Niet alle Dataverse-tabellen worden op dit moment weergegeven. Alleen tabellen die het gebruik van aangepaste velden ondersteunen, worden weergegeven in het raster. Nieuwe tabellen worden beschikbaar via doorlopende releases van Human Resources.

Het raster bevat de volgende velden:

- **Dataverse-tabel**: de naam van de tabel in Dataverse.
- **Dataverse-tabelverwijzing**: de id die in Dataverse wordt gebruikt om een record aan te duiden. Deze waarde is gelijk aan de **RecId**-waarde van Human Resources. U kunt de id vinden wanneer u de Dataverse-tabel opent in Microsoft Excel.
- **Human Resources-entiteitsnaam**: de Human Resources-entiteit die als laatste gegevens heeft gesynchroniseerd naar Dataverse. De entiteit kan het voorvoegsel Dataverse of een ander voorvoegsel hebben.
- **Human Resources-verwijzing** – De **RecId**-waarde die is gekoppeld aan de record in Human Resources.
- **Verwijderd uit Dataverse**: een waarde die aangeeft of de rij is verwijderd uit Dataverse.

> [!NOTE]
> Records in Human Resources komen overeen met rijen in Dataverse.

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a>De koppeling van een record in Human Resources verwijderen uit een Dataverse-rij

Als u problemen ondervindt tijdens de gegevenssynchronisatie tussen Human Resources en Dataverse, kunt u deze mogelijk oplossen door de traceringsgegevens te wissen en de traceringstabel opnieuw te synchroniseren. Als u de koppeling verwijdert en vervolgens een rij wijzigt of verwijdert in Dataverse, worden de wijzigingen niet gesynchroniseerd naar Human Resources. Als u wijzigingen aanbrengt in Human Resources, wordt er een nieuwe traceringsrecord gemaakt en wordt de rij bijgewerkt in Dataverse.

- Als u de koppeling van een Human Resources-record en een Dataverse-rij wilt verwijderen, selecteert u de tabel in het veld **Dataverse-tabel** en selecteert u de optie **Traceringsgegevens wissen**.

[![Traceringsgegevens wissen.](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)

Zie de volgende procedure als u een volledige synchronisatie wilt uitvoeren op de tabel nadat u de traceringsgegevens hebt gewist.

## <a name="sync-a-table-between-human-resources-and-dataverse"></a>Een tabel synchroniseren tussen Human Resources en Dataverse

Gebruik deze procedure als:

- De wijzigingen van Dataverse te lang duren om te worden weergegeven in Human Resources.

- U moet de traceringstabel vernieuwen nadat u de tracering hebt gewist.

Een volledige synchronisatie uitvoeren voor een tabel tussen Human Resources en Dataverse:

1. Selecteer de tabel in het veld **Dataverse-tabel**.

2. Selecteer **Nu synchroniseren**.

[![Een volledige synchronisatie uitvoeren.](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)

## <a name="see-also"></a>Zie ook

[Dataverse-tabellen](hr-developer-entities.md)<br>
[Virtuele Dataverse-entiteiten configureren](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Veelgestelde vragen over virtuele tabellen in Human Resources](hr-admin-virtual-entity-faq.md)<br>
[Wat is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Terminologiewijzigingen](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]