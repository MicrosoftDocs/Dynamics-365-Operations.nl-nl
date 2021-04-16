---
title: Een exemplaar kopiëren
description: U kunt Microsoft Dynamics Lifecycle Services (LCS) gebruiken om een Microsoft Dynamics 365 Human Resources-database naar een sandbox-omgeving te kopiëren.
author: andreabichsel
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6cb8050980b9b54480d09a59379430cd229ff141
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801090"
---
# <a name="copy-an-instance"></a>Een exemplaar kopiëren

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

U kunt Microsoft Dynamics Lifecycle Services (LCS) gebruiken om een Microsoft Dynamics 365 Human Resources-database naar een sandbox-omgeving te kopiëren. Als u nog een sandbox-omgeving hebt, kunt u de database ook vanuit die omgeving kopiëren naar een specifieke sandbox-omgeving.

Houd rekening met de volgende tips als u een exemplaar wilt kopiëren:

- Het Human Resources-exemplaar dat u wilt overschrijven, moet een sandbox-omgeving zijn.

- De omgevingen die u kopieert, moeten zich in dezelfde regio bevinden. U kunt niet kopiëren van de ene naar de andere omgeving.

- U moet een beheerder zijn in de doelomgeving, zodat u zich kunt aanmelden nadat u het exemplaar hebt gekopieerd.

- Wanneer u de Human Resources-database kopieert, kopieert u niet de elementen (apps of gegevens) die zijn opgenomen in een Microsoft Power Apps-omgeving. Zie [Een omgeving kopiëren](https://docs.microsoft.com/power-platform/admin/copy-environment) voor informatie over het kopiëren van elementen in een Power Apps-omgeving. De Power Apps-omgeving die u wilt overschrijven, moet een sandbox-omgeving zijn. U moet een globale tenantbeheerder zijn om een Power Apps-productieomgeving te wijzigen in een sandbox-omgeving. Zie [Schakelen tussen exemplaren](https://docs.microsoft.com/dynamics365/admin/switch-instance) voor meer informatie over het wijzigen van een Power Apps-omgeving.

- Als u een exemplaar in uw sandbox-omgeving kopieert en u de sandbox-omgeving wilt integreren met Dataverse, moet u aangepaste velden opnieuw toepassen op Dataverse-tabellen. Zie [Aangepaste velden toepassen op Dataverse](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).

## <a name="effects-of-copying-a-human-resources-database"></a>De gevolgen van het kopiëren van een Human Resources-database

De volgende gebeurtenissen treden op wanneer u een Human Resources-database kopieert:

- Tijdens het kopiëren wordt de bestaande database in de doelomgeving gewist. Nadat het kopieerproces is voltooid, kunt u de bestaande database niet herstellen.

- De doelomgeving is pas weer beschikbaar als de kopieerbewerking is voltooid.

- Documenten in de Microsoft Azure Blob-opslag worden niet van de ene omgeving naar de andere gekopieerd. Het resultaat is dat documenten en sjablonen die zijn gekoppeld, niet worden gekopieerd en in de bronomgeving blijven staan.

- Alle gebruikers behalve de gebruiker met beheerdersrechten en andere interne servicegebruikersaccounts worden uitgeschakeld. De gebruiker met beheerdersrechten kan de gegevens verwijderen of onleesbaar maken voordat andere gebruikers weer toegang hebben tot het systeem.

- De gebruiker met beheerdersrechten moet de vereiste configuratiewijzigingen aanbrengen, zoals het opnieuw verbinden van integratie-eindpunten met specifieke services of URL's.

## <a name="copy-the-human-resources-database"></a>De Human Resources-database kopiëren

Als u deze taak wilt voltooien, kopieert u eerst een exemplaar en meldt u zich vervolgens aan bij het Microsoft Power Platform-beheercentrum om uw Power Apps-omgeving te kopiëren.

> [!WARNING]
> Wanneer u een exemplaar kopieert, wordt de database gewist in het doelexemplaar. Het doelexemplaar is niet beschikbaar tijdens dit proces.

1. Meld u aan bij LCS en selecteer het LCS-project met het exemplaar dat u wilt kopiëren.

2. Selecteer in uw LCS-project de tegel **Beheer Human Resources-app**.

3. Selecteer het exemplaar dat u wilt kopiëren en selecteer **Kopiëren**.

4. Selecteer in het taak venster **Een exemplaar kopiëren** het exemplaar dat u wilt overschrijven en selecteer vervolgens **Kopiëren**. Wacht totdat de waarde in het veld **Kopieerstatus** is bijgewerkt naar **Voltooid**.

   ![[Selecteer het exemplaar dat u wilt overschrijven](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. Selecteer **Power Platform** en meld u aan bij het Microsoft Power Platform-beheercentrum.

   ![[Selecteer Power Platform](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. Selecteer de Power Apps-omgeving die u wilt kopiëren en selecteer vervolgens **Kopiëren**.

7. Wanneer het kopieerproces is voltooid, meldt u zich aan bij het doelexemplaar en schakelt u Dataverse-integratie in. Zie voor meer informatie en instructies [Dataverse-integratie configureren](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).

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

Sommige van deze elementen worden niet gekopieerd omdat ze specifiek zijn voor de omgeving. Voorbeelden zijn de **BatchServerConfig**- en **SysCorpNetPrinters**-records. Andere elementen worden niet gekopieerd vanwege het volume van de ondersteuningstickets. Bijvoorbeeld:

- Er kunnen dubbele e-mails worden verzonden omdat SMTP nog steeds is ingeschakeld in de omgeving voor acceptatietests voor gebruikers (sandbox).

- Er worden mogelijk berichten over een ongeldige integratie verzonden omdat batchtaken nog steeds zijn ingeschakeld.

- Gebruikers kunnen zijn ingeschakeld voordat beheerders de opruimacties na vernieuwen kunnen uitvoeren.

Bovendien worden de volgende statuswaarden gewijzigd wanneer u een exemplaar kopieert:

- Alle gebruikers behalve de beheerder worden ingesteld op **Uitgeschakeld**.

- Alle batchtaken, met uitzondering van bepaalde systeemtaken, worden ingesteld op **Inhouden**.

## <a name="environment-admin"></a>Omgevingsbeheerder

Alle gebruikers in de sandbox-doelomgeving, inclusief beheerders, worden vervangen door de gebruikers van de bronomgeving. Voordat u een exemplaar kopieert, moet u controleren of u een beheerder bent in de bronomgeving. Als u nog niet bij de sandbox-doelomgeving bent aangemeld, kunt u dat doen nadat de kopie is voltooid.

Alle gebruikers die geen beheerder zijn in de sandbox-doelomgeving, zijn uitgeschakeld om ongewenste aanmeldingen in de sandbox-omgeving te voorkomen. Beheerders kunnen gebruikers zo nodig opnieuw inschakelen.

## <a name="apply-custom-fields-to-dataverse"></a>Aangepaste velden toepassen op Dataverse

Als u een exemplaar in uw sandbox-omgeving kopieert en u de sandbox-omgeving wilt integreren met Dataverse, moet u aangepaste velden opnieuw toepassen op Dataverse-tabellen.

Voer de volgende stappen uit voor elk aangepast veld dat wordt weergegeven in Dataverse-tabellen:

1. Ga naar het aangepaste veld en selecteer **Bewerken**.

2. Schakel het selectievakje **Ingeschakeld** uit voor elke cdm_*-entiteit waarvoor het aangepaste veld is ingeschakeld.

3. Selecteer **Wijzigingen toepassen**.

4. Selecteer opnieuw **Bewerken**.

5. Schakel het selectievakje **Ingeschakeld** in voor elke cdm_*-entiteit waarvoor het aangepaste veld is uitgeschakeld.

6. Selecteer opnieuw **Wijzigingen toepassen**.

Door het proces van uitschakelen, wijzigingen toepassen, opnieuw inschakelen en wijzigingen weer toepassen, wordt het schema in Dataverse bijgewerkt met de aangepaste velden.

Meer informatie over aangepaste velden vindt u in [Aangepaste velden maken en gebruiken](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields).

## <a name="see-also"></a>Zie ook

[Human resources inrichten](hr-admin-setup-provision.md)</br>
[Een exemplaar verwijderen](hr-admin-setup-remove-instance.md)</br>
[Het updateproces](hr-admin-setup-update-process.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]