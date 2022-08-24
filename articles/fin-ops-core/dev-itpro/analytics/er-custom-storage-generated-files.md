---
title: Aangepaste opslaglocaties opgeven voor gegenereerde documenten
description: In dit artikel wordt uitgelegd hoe u de lijst met opslaglocaties uitbreidt voor documenten die zijn gegenereerd door indelingen voor elektronische rapportage (ER).
author: kfend
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: f938762d722493360614fd53e81bc5a4eba99928
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268171"
---
# <a name="specify-custom-storage-locations-for-generated-documents"></a>Aangepaste opslaglocaties opgeven voor gegenereerde documenten

[!include[banner](../includes/banner.md)]

Met de API (Application Programming Interface) van het ER-raamwerk kunt u de lijst met opslaglocaties uitbreiden voor documenten waarmee ER-indelingen worden gegenereerd. In dit artikel wordt uitgelegd hoe u een aangepaste opslaglocatie voor gegenereerde documenten kunt toevoegen door de taak voor het maken van ER-bestemmingen te delegeren aan de standaard bestemmingsfabriek en vervolgens een aangepaste klasse te implementeren die een eigen bestemmingslogica heeft.

## <a name="prerequisites"></a>Vereisten

Implementeer een topologie die ondersteuning biedt voor continuous build. Zie [Topologieën implementeren die ondersteuning bieden voor continue bouw- en testautomatisering](/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation) voor meer informatie. U moet ook toegang hebben tot deze topologie voor een van de volgende rollen:

- Ontwikkelaar elektronische rapportage
- Functioneel consultant elektronische rapportage
- Systeembeheerder

U moet ook toegang hebben tot de ontwikkelomgeving voor deze topologie.

Alle taken in dit artikel kunnen in het bedrijf **USMF** worden uitgevoerd.

## <a name="import-the-fixed-asset-roll-forward-er-format"></a>De ER-indeling voor Voortschrijdende prognose voor vaste activa importeren

Als u de documenten wilt genereren waarvoor u een aangepaste opslaglocatie wilt toevoegen, [importeert](er-download-configurations-global-repo.md) u de configuratie van de ER-indeling **Voortschrijdende prognose voor vaste activa** in de huidige topologie.

![Configuratie archiefpagina.](./media/er-custom-storage-generated-files-import-format.png)

## <a name="run-the-fixed-asset-roll-forward-report"></a>Het rapport voor voortschrijdende prognose voor vaste activa uitvoeren

1. Ga naar **Vaste activa** \> **Query's en rapporten** \> **Transactierapporten** \> **Voortschrijdende prognose voor vaste activa**.
2. Voer in het veld **Begindatum** de waarde **1/1/2017** (1 januari 2017) in.
3. Voer in het veld **Einddatum** de waarde **1/31/2017** (31 januari 2017) in.
4. Selecteer in het veld **Valuta** de optie **Boekhoudvaluta**.
5. Selecteer in het veld **Indelingstoewijzing** de optie **Voortschrijdende prognose voor vaste activa**.
6. Selecteer **OK**.

![Het runtime-dialoogvenster voor het rapport Voortschrijdende prognose voor vaste activa.](./media/er-custom-storage-generated-files-runtime-dialog.png)

Controleer in Microsoft Excel het uitgaande document dat is gegenereerd en beschikbaar is voor downloaden. Dit gedrag is het [standaardgedrag](electronic-reporting-destinations.md#default-behavior) voor een ER-indeling waarvoor geen [bestemmingen](electronic-reporting-destinations.md) zijn geconfigureerd en die in de interactieve modus wordt uitgevoerd.

## <a name="review-the-source-code"></a>De broncode controleren

Controleer de code van de methode `generateReportByGER()` van de klasse `AssetRollForwardService`. U ziet dat de methode `Run()` wordt gebruikt om het ER-raamwerk aan te roepen en het rapport **Voortschrijdende prognose voor vaste activa** te genereren.

```xpp
class AssetRollForwardService extends SysOperationServiceBase
{
    public const str ERFormatModelName = 'Fixed assets';
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'AssetRollForward';

    /// <summary>
    /// Generates report by general electronic reporting
    /// </summary>
    /// <param name = "_contract">The Asset Period Statement contract</param>
    public void generateReportByGER(AssetRollForwardContract _contract)
    {
        ERFormatMappingId   formatMappingId;
        AssetRollForwardDP  dataProvider;
        AssetRollForwardTmp assetRollForwardTmp;
        Query               query;

        query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
        dataProvider = AssetRollForwardDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

        if (assetRollForwardTmp)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                // Call ER to generate the report.
                ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName)
                    .withParameter(parameters)
                    .withFileDestination(_contract.getFileDestination())
                    .run();
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

## <a name="modify-the-source-code"></a>De broncode wijzigen

1. Voeg in het Visual Studio-project een nieuwe klasse toe (`AssetRollForwardDestination` in dit voorbeeld) en schrijf code om uw aangepaste doel te implementeren voor rapporten **Voortschrijdende prognose voor vaste activa** die worden gegenereerd.

    - De methode `new()` is bedoeld om het oorspronkelijke ER-bestemmingsobject en de via toepassingslogica gestuurde parameter op te halen die de aangepaste locatie aangeeft waar gegenereerde rapporten moeten worden opgeslagen. In dit voorbeeld is de aangepaste locatie de naam van een map van het lokale bestandssysteem van de server waarop de AOS-service (Application Object Server) wordt uitgevoerd.
    - De methode `saveFile()` is ontworpen om een gegenereerd document op te slaan in een map van het lokale bestandssysteem van de server waarop de AOS-service wordt uitgevoerd.

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;

    /// <summary>
    /// Destination class for <c>AssetRollForwardDestinationFactory</c> that stores a generated report.
    /// </summary>
    public class AssetRollForwardDestination implements ERIFileDestination
    {
        private ERIFileDestination originDestination;
        private str TargetFolder;

        /// <summary>
        /// Creates a stream for new file.
        /// </summary>
        /// <param name = "_fileName">Name of a new file.</param>
        /// <returns>Stream for new file.</returns>
        public System.IO.Stream newFileStream(System.String _fileName)
        {
            return originDestination.newFileStream(_fileName);
        }

        /// <summary>
        /// Saves file in destination.
        /// </summary>
        /// <param name = "_stream">A stream to save.</param>
        /// <param name = "_fileName">A file name.</param>
        /// <returns>Saved stream.</returns>
        public System.IO.Stream saveFile(System.IO.Stream _stream, System.String _fileName)
        {
            _stream.Seek(0, System.IO.SeekOrigin::Begin);
            using (var localStream = System.IO.File::OpenWrite(TargetFolder + _fileName))
            {
                _stream.CopyTo(localStream);
            }
            return _stream;
        }

        /// <summary>
        /// Constructs destination for fixed asset roll forward report.
        /// </summary>
        /// <param name = "_originDestination">The original destination.</param>
        /// <param name = "_TargetFoder">The folder to store a report that's being created.</param>
        /// <returns>The fixed asset roll forward destination.</returns>
        public static AssetRollForwardDestination construct(ERIFileDestination _originDestination, str _TargetFoder)
        {
            return new AssetRollForwardDestination(_originDestination, _TargetFoder);
        }

        protected void new(ERIFileDestination _originDestination, str _TargetFoder)
        {
            originDestination = _originDestination;
            TargetFolder = _TargetFoder;
        }
    }
    ```

2. Voeg in uw Visual Studio-project een nieuwe klasse toe (`AssetRollForwardDestinationFactory` in dit voorbeeld) en schrijf code om een aangepaste bestemmingsfabriek in te stellen waarmee het maken van een bestemming wordt gedelegeerd naar de standaardfabriek en om een bestandsbestemming van uw eigen bestemming te voorzien.

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    using Microsoft.Dynamics365.LocalizationFramework.Format.FileGeneration;

    /// <summary>
    /// Destination factory for using <c>AssetRollForwardDestinationFactory</c>.
    /// </summary>
    public class AssetRollForwardDestinationFactory implements ERIFileDestinationFactory, ERIFileDestinationFactoryPostProcessor
    {
        private ERIFileDestinationFactory originDestinationFactory;
        private str TargetFolder;

        /// <summary>
        /// Creates file destination for print management.
        /// </summary>
        /// <param name = "_fileDestination">A default file destination.</param>
        /// <param name = "_identification">An identification strategy.</param>
        /// <param name = "_rootContext">A root context.</param>
        /// <param name = "_root">A root element.</param>
        /// <returns>A file destination.</returns>
        public ERIDataDrivenFileDestination createPrintMgmtDestination(
            ERIFileDestination _fileDestination,
            ERIObjectIdentificationStrategy _identification,
            ERTextFormatDataContext _rootContext,
            ERTextFormatIFileComponent _root)
        {
            ERIDataDrivenFileDestination dataDrivenDestination = originDestinationFactory.createPrintMgmtDestination(
                _fileDestination,
                _identification,
                _rootContext,
                _root);

            IFileDestinationHost fileDestinationHost = dataDrivenDestination as IFileDestinationHost;
            if (fileDestinationHost)
            {
                fileDestinationHost.FileDestination = AssetRollForwardDestination::construct(
                    fileDestinationHost.get_FileDestination(),
                    TargetFolder);
            }

            return dataDrivenDestination;
        }

        /// <summary>
        /// Constructs the fixed asset roll forward destination factory.
        /// </summary>
        /// <param name = "_originDestinationFactory">The original destination.</param>
        /// <param name = "_TargetFolder">The string containing a folder name that corresponds to the report, that's being created.</param>
        /// <returns>The destination factory for the fixed asset roll forward report.</returns>
        public static AssetRollForwardDestinationFactory construct(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            AssetRollForwardDestinationFactory destinationFactory = new AssetRollForwardDestinationFactory(_originDestinationFactory, _TargetFolder);

            ERIFileDestinationFactoryPostProcessorsHost factoryPostProcessing = ERCast::asObject(destinationFactory.originDestinationFactory) as ERIFileDestinationFactoryPostProcessorsHost;

            if (factoryPostProcessing)
            {
                factoryPostProcessing.addDestinationPostProcessor(destinationFactory);
            }
            return destinationFactory;
        }

        public ERIFileDestination processDestinationAfterCreation(ERIFileDestination _sourceDestination)
        {
            return AssetRollForwardDestination::construct(_sourceDestination, TargetFolder);
        }

        protected void new(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            originDestinationFactory = _originDestinationFactory;
            TargetFolder = _TargetFolder;
        }
    }
    ```

3. Wijzig de bestaande klasse `AssetRollForwardService` en schrijf code om een aangepaste bestemmingsfabriek in te stellen voor de rapportuitvoeringsfunctie. Wanneer een aangepaste bestemmingsfabriek is opgebouwd, wordt de toepassingsgestuurde parameter die een bestemmingsmap opgeeft doorgegeven. Op deze manier wordt de bestemmingsmap gebruikt om gegenereerde bestanden op te slaan.

    > [!NOTE] 
    > Controleer of de opgegeven map (**c:\\0** in dit voorbeeld) aanwezig is in het lokale bestandssysteem van de server waarop de AOS-service wordt uitgevoerd. Anders wordt een uitzondering [DirectoryNotFoundException](/dotnet/api/system.io.directorynotfoundexception) gegenereerd tijdens runtime.

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    /// <summary>
    /// The electronic reporting service class for fixed asset roll forward report
    /// </summary>
    class AssetRollForwardService extends SysOperationServiceBase
    {
        public const str ERFormatModelName = 'Fixed assets';
        public const str ERModelDataSourceName = 'model';
        public const str DefaultExportedFileName = 'AssetRollForward';

        /// <summary>
        /// Generates report by general electronic reporting
        /// </summary>
        /// <param name = "_contract">The Asset Period Statement contract</param>
        public void generateReportByGER(AssetRollForwardContract _contract)
        {
            ERFormatMappingId   formatMappingId;
            AssetRollForwardDP  dataProvider;
            AssetRollForwardTmp assetRollForwardTmp;
            Query               query;

            query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
            dataProvider = AssetRollForwardDP::construct();
            formatMappingId = _contract.parmFormatMapping();
            assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

            if (assetRollForwardTmp)
            {
                try
                {
                    ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                        .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                        .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                    // Call ER to generate the report.
                    ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());

                    ERIFileDestinationFactoryHost factoryHost = ERCast::asObject(formatMappingRun) as ERIFileDestinationFactoryHost;
                    if (factoryHost)
                    {
                        ERIFileDestinationFactory fileDestinationFactory = factoryHost.getFileDestinationFactory();
                        factoryHost.setFileDestinationFactory(AssetRollForwardDestinationFactory::construct(fileDestinationFactory, @'c:\0\'));
                        formatMappingRun.run();
                    }
                }
                catch
                {
                    // An error occurred while exporting data.
                    error("@SYP4861341");
                }
            }
            else
            {
                // There is no data available.
                info("@SYS300117");
            }
        }
    }
    ```

4. Maak uw project opnieuw.

## <a name="re-run-the-fixed-asset-roll-forward-report"></a>Het rapport voor voortschrijdende prognose voor vaste activa opnieuw uitvoeren

1. Ga naar **Vaste activa** \> **Query's en rapporten** \> **Transactierapporten** \> **Voortschrijdende prognose voor vaste activa**.
2. Voer in het veld **Begindatum** de waarde **1/1/2017** in.
3. Voer in het veld **Einddatum** de waarde **1/31/2017** in.
4. Selecteer in het veld **Valuta** de optie **Boekhoudvaluta**.
5. Selecteer in het veld **Indelingstoewijzing** de optie **Voortschrijdende prognose voor vaste activa**.
6. Selecteer **OK**.
7. Blader door de lokale map **C:\\0** om het gegenereerde bestand te zoeken.

> [!NOTE]
> Omdat het object `originDestination` in dit voorbeeld niet wordt gebruikt in het object `AssetRollForwardDestination`, worden de configuraties voor de [bestemmingen](electronic-reporting-destinations.md) van de ER-indeling genegeerd tijdens runtime.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Bestemmingen van elektronische rapportage (ER)](electronic-reporting-destinations.md)
- [Startpagina voor Uitbreidbaarheid](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
