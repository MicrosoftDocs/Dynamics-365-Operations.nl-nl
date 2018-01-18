---
title: "De datamart voor financiële rapportage opnieuw instellen"
description: "In dit onderwerp wordt beschreven hoe u de datamart voor financiële rapportage opnieuw instelt."
author: aolson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 5b956dcc5a4a93033396ae0ffcf8b7aeba2cf3f2
ms.openlocfilehash: a07e8b5bae2c4f71e9212cd2f8080d2481769818
ms.contentlocale: nl-nl
ms.lasthandoff: 12/14/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a>De datamart voor financiële rapportage opnieuw instellen

[!include[banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u de datamart voor financiële rapportage opnieuw instelt voor de volgende versies:

- Microsoft Dynamics 365 for Finance and Operations Financial Reporting 7.2.6.0 en hoger
- Microsoft Dynamics 365 for Finance and Operations Financial Reporting 7.0.10000.4 en hoger
- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises)

Voor Finance and Operations Financial Reporting 7.2.6.0 kunt u KB 4052514 downloaden via <https://fix.lcs.dynamics.com/Issue/Resolved?kb=4052514>.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a>De datamart voor financiële rapportage opnieuw instellen voor Finance and Operations Financial Reporting 7.2.6.0 en hoger

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a>De datamart voor financiële rapportage opnieuw instellen vanuit Rapportontwerper

> [!NOTE]
> De stappen in dit proces worden ondersteund voor Finance and Operations Financial Reporting 7.2.6.0 en hoger. Als u een oudere versie hebt, neemt u voor ondersteuning contact op met het ondersteuningsteam.

In bepaalde gevallen moet u de datamart voor financiële rapportage mogelijk opnieuw instellen. U kunt deze taak voltooien in de client Rapportontwerper. Hier volgen enkele scenario's waarin u de datamart wellicht opnieuw moet instellen:

- De Finance and Operations-database is opnieuw ingesteld, maar de database van de datamart niet.
- Gedurende een periode worden er onjuiste gegevens weergegeven.
- Van de ondersteuning krijgt u instructies voor het opnieuw instellen van de datamart als onderdeel van een stap voor probleemoplossing.

De datamart moet alleen opnieuw worden ingesteld op tijden dat de database relatief licht wordt belast. Financiële rapportage is niet beschikbaar tijdens het proces van opnieuw instellen.

#### <a name="reset-the-data-mart"></a>De datamart opnieuw instellen

Als u de datamart opnieuw wilt instellen, selecteert u in Rapportontwerper in het menu **Extra** de optie **Datamart opnieuw instellen**. Het dialoogvenster dat verschijnt, bevat twee secties: **Statistieken** en **Opnieuw instellen**.

[![Dialoogvenster Datamart opnieuw instellen](./media/Reset-72.jpg)](./media/Reset-72.jpg)

##### <a name="integration-attempts"></a>Integratiepogingen

In het raster **Integratiepogingen** ziet u hoe vaak het systeem heeft geprobeerd transacties te integreren. Als de eerste paar pogingen mislukken, blijft het systeem het enkele dagen proberen. U weet dat de datamart opnieuw moet worden ingesteld als het aantal pogingen 8 of meer is en er veel dimensiecombinatie- of transactierecords zijn. In deze situatie worden de gegevens niet gerapporteerd.

##### <a name="data-status"></a>Status gegevens

Het raster **Status gegevens** biedt een momentopname van de transacties, wisselkoersen en dimensiewaarden in de datamart. Een groot aantal verouderde records duidt erop dat een groot aantal updates van de records is uitgevoerd. Deze situatie kan ertoe leiden dat rapporten langzamer worden gegenereerd.

##### <a name="misaligned-main-account-categories"></a>Onjuist uitgelijnde hoofdrekeningcategorieën

Als u een oudere versie dan Microsoft Dynamics 365 for Finance and Operations Financial Reporting 7.2.1 gebruikt, moet u de datamart wellicht opnieuw instellen als u namen van rekeningen wijzigt en rekeningen tussen rekeningcategorieën verplaatst. Deze acties kunnen ertoe leiden dat hoofdrekeningcategorieën onjuist worden uitgelijnd. In het veld **Onjuist uitgelijnde hoofdrekeningcategorieën** wordt aangegeven of dit probleem zich voordoet.

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a>De datamart opnieuw instellen in Finance and Operations Financial Reporting 7.2.6.0

Als u de datamart opnieuw wilt instellen in Finance and Operations Financial Reporting 7.2.6.0 of eerdere versies, schakelt u in het dialoogvenster **Datamart opnieuw instellen** het selectievakje **Datamart opnieuw instellen** in en selecteert u **OK**. Stel de datamart alleen opnieuw in tijdens een geplande uitvaltijd.

[![Selectievakje Datamart opnieuw instellen](./media/Reset-72.jpg)](./media/Reset-72.jpg)

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a>De datamart opnieuw instellen en een reden selecteren in Microsoft Dynamics 365 for Finance and Operations Financial Reporting 7.3.0

Als u vaststelt dat een datamart opnieuw moet worden ingesteld, schakelt u het selectievakje **Datamart opnieuw instellen** in en selecteert u een reden in het veld **Reden**. De volgende opties zijn beschikbaar:

- **Ontbrekende of onjuiste gegevens**: op basis van de statistieken hebt u vastgesteld dat er mogelijk gegevens ontbreken. Voordat u doorgaat, wordt u aangeraden contact op te nemen met de ondersteuning om de hoofdoorzaak te achterhalen.
- **Database herstellen**: de Finance and Operations-database is hersteld, maar de database van de datamart voor financiële rapportage niet.
- **Overige**: u herstelt de datamart om een andere reden. Als u vermoedt dat er een probleem is, moet u contact opnemen met de ondersteuning.

[![Datamart opnieuw instellen](./media/Integration.png)](./media/Integration.png)

> [!NOTE]
> Controleer voordat u met een reset begint of met alle taken voor het opnieuw instellen van datamarts een initiële laadbewerking is uitgevoerd. U kunt dit controleren door te zoeken naar een waarde in de kolom Laatste uitvoering. Selecteer hiervoor **Extra** &gt; **Integratiestatus**.

#### <a name="clear-users-and-companies"></a>Gebruikers en bedrijven wissen

Schakel het selectievakje **Gebruikers en bedrijven wissen** in als u uw database opnieuw hebt ingesteld, maar vervolgens wijzigingen hebt doorgevoerd in gebruikers of bedrijven. U hoeft dit selectievakje zelden in te schakelen.

Wanneer u klaar bent om het proces voor opnieuw instellen te starten, selecteert u **OK**. U wordt gevraagd te bevestigen dat u het proces wilt starten. Houd er rekening mee dat financiële rapportage niet beschikbaar is tijdens het opnieuw instellen en de initiële gegevensintegratie daarna.

Als u de status van de integratie wilt bekijken, selecteert u **Extra** &gt; **Integratiestatus** om na te gaan wanneer de integratie het laatst is uitgevoerd en de status te bekijken.

[![De status van de integratie weergeven](./media/New-integration.PNG)](./media/New-integration.PNG)

> [!NOTE]
> Het opnieuw instellen is voltooid wanneer voor alle toewijzingen de status RanToCompletion wordt weergegeven en in het venster Integratiestatus het bericht Integratie voltooid in de linkerbenedenhoek wordt weergegeven.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a>De datamart voor financiële rapportage opnieuw instellen voor Finance and Operations Financial Reporting 7.0.10000.4 en hoger

Als u uw Finance and Operations-database opnieuw moet instellen vanaf een back-up of de database uit een andere omgeving kopieert, moet u de stappen in dit gedeelte volgen om te zorgen dat de datamart voor financiële rapportage correct gebruikmaakt van de opnieuw ingestelde Finance and Operations-database.

> [!NOTE]
> De stappen in dit proces worden ondersteund voor Microsoft Dynamics AX 7.0.1 (mei 2016) (toepassingsbuild 7.0.1265.23014 en Financial Reporting-build 7.0.10000.4) en hoger. Als u een eerdere versie van Finance and Operations hebt, neemt u voor hulp contact op met de ondersteuning.

### <a name="export-report-definitions"></a>Rapportdefinities exporteren

Volg eerst deze stappen als u de rapportontwerpen wilt exporteren vanuit Rapportontwerper.

1. Selecteer in Rapportontwerper de optie **Bedrijf** &gt; **Bouwsteengroepen**.
2. Selecteer de bouwsteengroep die u wilt exporteren en selecteer **Exporteren**.

    > [!NOTE]
    > Voor Finance and Operations wordt slechts één bouwsteengroep ondersteund, namelijk **Standaard**.

3. Selecteer de rapportdefinities die u wilt exporteren:

    - Als u alle rapportdefinities en de bijbehorende bouwstenen wilt exporteren, selecteert u **Alles selecteren**.
    - U kunt specifieke rapporten, rijen, kolommen, structuren of dimensiesets exporteren door het gewenste tabblad te selecteren en vervolgens de te exporteren items te selecteren. Druk op Ctrl en houd deze toets ingedrukt om meerdere artikelen op een tabblad te selecteren. Wanneer u rapporten selecteert om te exporteren, worden de bijbehorende rijen, kolommen, structuren en dimensiegroepen ook geselecteerd.

4. Selecteer **Exporteren**.
5. Voer een bestandsnaam in en selecteer de beveiligde locatie waar u de geëxporteerde rapportdefinities wilt opslaan.
6. Selecteer **Opslaan**.

U kunt het bestand naar een veilige locatie kopiëren of uploaden. Op deze manier kan het bestand later in een andere omgeving worden geïmporteerd. Informatie over het gebruik van een Microsoft Azure-opslagaccount vindt u in het onderwerp [Gegevensoverdracht met het opdrachtregelprogramma AzCopy](/azure/storage/storage-use-azcopy).

> [!NOTE]
> Microsoft biedt geen opslagaccount aan als onderdeel van uw Finance and Operations-abonnement. U moet een opslagaccount aanschaffen of een opslagaccount uit een separaat Azure-abonnement gebruiken.

> [!WARNING]
> Houd rekening met het gedrag van het station D op virtuele Azure-machines (VM's). Sla uw geëxporteerde bouwsteengroepen niet permanent op station D op. Zie [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/) voor meer informatie over tijdelijke stations.

### <a name="stop-services"></a>Services afstoppen

De volgende Microsoft Windows-services hebben openstaande verbindingen met de Finance and Operations-database. Maak via Microsoft Extern bureaublad verbinding met alle computers in de omgeving en stop deze services met services.msc.

- World Wide Web Publishing-service (op alle AOS-computers)
- Microsoft Dynamics 365 for Finance and Operations Batch Management-service (alleen op niet-privé AOS-computers)
- Management Reporter 2012 Process Service (alleen op BI-computers)

### <a name="reset"></a>Opnieuw instellen

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a>Het meest recente pakket met MinorVersionDataUpgrade.zip downloaden

Download het meest recente pakket met MinorVersionDataUpgrade.zip. Zie voor meer informatie over het zoeken en downloaden van de juiste versie van het gegevensupgradepakket [Downloaden van het meest recente bruikbare pakket met gegevensupgrade](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package). 

Een upgrade is niet vereist voor het downloaden van het pakket MinorVersionDataUpgrade.zip. U hoeft alleen maar de stappen in het gedeelte Downloaden van het meest recente bruikbare pakket met gegevensupgrade van dat onderwerp te volgen. U kunt de overige stappen in het onderwerp overslaan.

#### <a name="run-scripts-against-the-finance-and-operations-database"></a>Scripts uitvoeren op de Finance and Operations-database

Voer de volgende scripts uit op de Finance and Operations-database (niet op de database voor financiële rapportage):

- DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
- DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Deze scripts zorgen ervoor dat de gebruikers, rollen en instellingen voor het bijhouden van wijzigingen juist zijn.

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a>Een Windows PowerShell-opdracht uitvoeren om de database opnieuw in te stellen

Start Microsoft Windows PowerShell als beheerder op de AOS-computer en voer de volgende opdrachten uit om de integratie tussen Finance and Operations en Financial Reporting opnieuw in te stellen.

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

Hier volgt een uitleg van de parameters in de opdracht **Reset-DatamartIntegration**:

- De geldige waarden voor **-Reason** zijn **SERVICING**, **BADDATA** en **OTHER**.
- Bij de parameter **-ReasonDetail** kunt u vrije tekst invoeren.
- De reden en redengegevens worden vastgelegd in telemetrie/omgevingsbewaking.

> [!NOTE]
> Nadat u de opdrachten hebt uitgevoerd, wordt u gevraagd om **Y** in te voeren om te bevestigen dat u de database opnieuw wilt instellen.

#### <a name="restart-services"></a>Services opnieuw starten

Start de services die u eerder hebt afgestopt opnieuw op door middel van services.msc:

- World Wide Web Publishing-service (op alle AOS-computers)
- Microsoft Dynamics 365 for Finance and Operations Batch Management-service (alleen op niet-privé AOS-computers)
- Management Reporter 2012 Process Service (alleen op BI-computers)

#### <a name="import-report-definitions"></a>Rapportdefinities importeren

Importeert uw rapportontwerpen vanuit Rapportontwerper met behulp van het bestand dat tijdens het exporteren is gemaakt.

1. Selecteer in Rapportontwerper de optie **Bedrijf** &gt; **Bouwsteengroepen**.
2. Selecteer de bouwsteengroep die u wilt exporteren en selecteer **Exporteren**.

    > [!NOTE]
    > Voor Finance and Operations wordt slechts één bouwsteengroep ondersteund, namelijk **Standaard**.

3. Selecteer de bouwsteen **Standaard** en selecteer **Importeren**.
4. Selecteer het bestand met de geëxporteerde rapportdefinities en selecteer **Openen**.
5. Selecteer in het dialoogvenster **Importeren** de rapportdefinities die u wilt importeren:

    - Als u alle rapportdefinities en de bijbehorende bouwstenen wilt importeren, selecteert u **Alles selecteren**.
    - Als u specifieke rapporten, rijen, kolommen, structuren of dimensiegroepen wilt importeren, selecteert u de rapporten, rijen, kolommen, structuren of dimensiegroepen die u wilt importeren.

6. Selecteer **Importeren**.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a>De datamart voor financiële rapportage opnieuw instellen voor Finance and Operations (on-premises)

1. Instrueer alle gebruikers om Rapportontwerper en het gedeelte Financiële rapportage van Finance and Operations af te sluiten.
2. Voer het volgende script uit op de database voor financiële rapportage (MRDB).

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ```

3. U moet alle records uit de tabel FINANCIALREPORTS in de Finance and Operations-database (AXDB) afkappen of verwijderen.
4. Als deze tabel aanwezig is, moet u alle records uit de tabel FINANCIALREPORTVERSION in de Finance and Operations-database (AXDB) afkappen of verwijderen. Als de tabel niet bestaat in de Finance and Operations-database, slaat u deze stap over.
5. Voer het script **ResetDatamart.sql** uit op de database voor financiële rapportage. Met dit script wordt de datamartintegratie uitgeschakeld, worden alle datamartgegevens verwijderd en wordt de datamartintegratie opnieuw ingeschakeld.

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
        FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
            EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
            INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
            WHERE o.[type] = 'V' 
            AND referenced_schema_name = @schemaname
            AND referenced_entity_name = @tablename))
            BEGIN
            PRINT 'deleting from ' + @tablename
            EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
            PRINT 'truncating from ' + @tablename
            EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    ------------------------------------------
    ------------------------------------------
    PRINT 'Reset the map tokens'
    UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Reset the tasks'
    UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
    PRINT 'Enable integration tasks, RunImmediately'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
    WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Enable the Maintenance Task'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
    (SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
    ------------------------------------------
    ------------------------------------------
    ```

6. Na het opnieuw instellen kunt u handmatig controleren of de gegevens opnieuw zijn geladen door de volgende query uit te voeren op de database voor financiële rapportage.

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    Controleer of alle rijen een waarde voor **LastRunTime** bevatten en of **StateType** is ingesteld op **5**. Wanneer voor **StateType** de waarde **5** wordt weergegeven, zijn de gegevens opnieuw geladen. Een waarde van **7** geeft een foutstatus aan. Soms heeft de toewijzing Organisatiehiërarchie deze status wanneer deze voor het eerst wordt uitgevoerd. Als het goed is, wordt de foutstatus automatisch opgelost.

