---
title: Een exemplaar kopiëren
description: U kunt Microsoft Dynamics Lifecycle Services (LCS) gebruiken om een Microsoft Dynamics 365 Human Resources-database naar een sandbox-omgeving te kopiëren.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bb363369994d99f358be0c23cdaf1dbc80b644e5
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092287"
---
# <a name="copy-an-instance"></a>Een exemplaar kopiëren

U kunt Microsoft Dynamics Lifecycle Services (LCS) gebruiken om een Microsoft Dynamics 365 Human Resources-database naar een sandbox-omgeving te kopiëren. Als u nog een sandbox-omgeving hebt, kunt u de database ook vanuit die omgeving kopiëren naar een specifieke sandbox-omgeving.

Voor het kopiëren van een exemplaar moet u het volgende controleren:

- Het Human Resources-exemplaar dat u wilt overschrijven, moet een sandbox-omgeving zijn.

- De omgevingen die u kopieert, moeten zich in dezelfde regio bevinden. U kunt niet kopiëren van de ene naar de andere omgeving.

- U moet een beheerder zijn in de doelomgeving, zodat u zich kunt aanmelden nadat u het exemplaar hebt gekopieerd.

- Wanneer u de Human Resources-database kopieert, kopieert u niet de elementen (apps of gegevens) die zijn opgenomen in een Microsoft PowerApps-omgeving. Zie [Een omgeving kopiëren](https://docs.microsoft.com/power-platform/admin/copy-environment) voor informatie over het kopiëren van elementen in een PowerApps-omgeving. De PowerApps-omgeving die u wilt overschrijven, moet een sandbox-omgeving zijn. U moet een globale tenantbeheerder zijn om een PowerApps-productieomgeving te wijzigen in een sandbox-omgeving. Zie [Schakelen tussen exemplaren](https://docs.microsoft.com/dynamics365/admin/switch-instance) voor meer informatie over het wijzigen van een PowerApps-omgeving.

## <a name="effects-of-copying-a-human-resources-database"></a>De gevolgen van het kopiëren van een Human Resources-database

De volgende gebeurtenissen treden op wanneer u een Human Resources-database kopieert:

- Tijdens het kopiëren wordt de bestaande database in de doelomgeving gewist. Nadat het kopieerproces is voltooid, kunt u de bestaande database niet herstellen.

- De doelomgeving is pas weer beschikbaar als de kopieerbewerking is voltooid.

- Documenten in de Microsoft Azure Blob-opslag worden niet van de ene omgeving naar de andere gekopieerd. Daarom worden documenten en sjablonen die zijn gekoppeld, niet gekopieerd en blijven deze in de bronomgeving.

- Alle gebruikers behalve de gebruiker met beheerdersrechten en andere interne servicegebruikersaccounts worden uitgeschakeld. De gebruiker met beheerdersrechten kan de gegevens dus verwijderen of onleesbaar maken voordat andere gebruikers weer toegang hebben tot het systeem.

- De gebruiker met beheerdersrechten moet de vereiste configuratiewijzigingen aanbrengen, zoals het opnieuw verbinden van integratie-eindpunten met specifieke services of URL's.

## <a name="copy-the-human-resources-database"></a>De Human Resources-database kopiëren

Als u deze taak wilt voltooien, kopieert u eerst een exemplaar en meldt u zich vervolgens aan bij het Microsoft Power Platform-beheercentrum om uw PowerApps-omgeving te kopiëren.

> [!WARNING]
> Wanneer u een exemplaar kopieert, wordt de database gewist in het doelexemplaar. Het doelexemplaar is niet beschikbaar tijdens dit proces.

1. Meld u aan bij LCS en selecteer het LCS-project met het exemplaar dat u wilt kopiëren.

2. Selecteer in uw LCS-project de tegel **Beheer Human Resources-app**.

3. Selecteer het exemplaar dat u wilt kopiëren en selecteer **Kopiëren**.

4. Selecteer in het taak venster **Een exemplaar kopiëren** het exemplaar dat u wilt overschrijven en selecteer vervolgens **Kopiëren**. Wacht totdat de waarde in het veld **Kopieerstatus** is bijgewerkt naar **Voltooid**.

   ![[Selecteer de instantie die u wilt overschrijven](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. Selecteer **Power Platform** en meld u aan bij het Microsoft Power Platform-beheercentrum.

   ![[Selecteer Power Platform](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. Selecteer de PowerApps-omgeving die u wilt kopiëren en selecteer vervolgens **Kopiëren**.

7. Wanneer het kopieerproces is voltooid, meldt u zich aan bij het doelexemplaar en schakelt u Common Data Service-integratie in. Zie voor meer informatie en instructies [Common Data Service-integratie configureren](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).

## <a name="data-elements-and-statuses"></a>Gegevenselementen en statussen

De volgende gegevenselementen worden niet gekopieerd wanneer u een Human Resources-exemplaar kopieert:

- E-mailadressen in de tabel **LogisticsElectronicAddress**

- De batchtaakhistorie in de tabellen **BatchJobHistory**, **BatchHistory** en **BatchConstraintHistory**

- Het SMTP-wachtwoord (Simple Mail Transfer Protocol) in de tabel **SysEmailSMTPPassword**

- De SMTP-relayserver in de tabel **SysEmailParameters**

- Afdrukbeheerinstellingen in de tabellen **PrintMgmtSettings** en **PrintMgmtDocInstance**

- Omgevingsspecifieke records in de tabellen **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** en **BatchServerGroup**

- Documentbijlagen in de tabel DocuValue. Deze bijlagen bevatten Microsoft Office-sjablonen die in de bronomgeving zijn overschreven.

- De verbindingsreeks in de tabel **PersonnelIntegrationConfiguration**

Sommige van deze elementen worden niet gekopieerd omdat ze omgevingsspecifiek zijn. Voorbeelden zijn de **BatchServerConfig**- en **SysCorpNetPrinters**-records. Andere elementen worden niet gekopieerd vanwege het volume van de ondersteuningstickets. Er kunnen bijvoorbeeld dubbele e-mailberichten worden verzonden omdat SMTP nog steeds is ingeschakeld in de omgeving voor acceptatietests voor gebruikers (sandbox-omgeving), er kunnen ongeldige integratieberichten worden verzonden omdat batchtaken nog steeds zijn ingeschakeld en er kunnen gebruikers worden ingeschakeld voordat beheerders opruimacties na vernieuwing kunnen uitvoeren.

Bovendien worden de volgende statuswaarden gewijzigd wanneer u een exemplaar kopieert:

- Alle gebruikers behalve de beheerder worden ingesteld op **Uitgeschakeld**.

- Alle batchtaken, met uitzondering van bepaalde systeemtaken, worden ingesteld op **Inhouden**.

## <a name="environment-admin"></a>Omgevingsbeheerder

Alle gebruikers in de sandbox-doelomgeving, inclusief beheerders, worden vervangen door de gebruikers van de bronomgeving. Voordat u een exemplaar kopieert, moet u controleren of u een beheerder bent in de doelomgeving. Als u dat niet bent, kunt u zich niet aanmelden bij de sandbox-doelomgeving nadat de kopie is voltooid.

Alle gebruikers die geen beheerder zijn in de sandbox-doelomgeving, zijn uitgeschakeld om ongewenste aanmeldingen in de sandbox-omgeving te voorkomen. Beheerders kunnen gebruikers zo nodig opnieuw inschakelen.
