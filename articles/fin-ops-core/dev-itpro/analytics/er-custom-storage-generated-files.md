---
title: Aangepaste opslaglocaties opgeven voor gegenereerde documenten
description: In dit onderwerp wordt uitgelegd hoe u de lijst met opslaglocaties uitbreidt voor documenten die zijn gegenereerd door indelingen voor elektronische rapportage (ER).
author: NickSelin
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 25719de3d86785442e00f7375de525b95bdb094d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753691"
---
# <a name="specify-custom-storage-locations-for-generated-documents"></a><span data-ttu-id="051be-103">Aangepaste opslaglocaties opgeven voor gegenereerde documenten</span><span class="sxs-lookup"><span data-stu-id="051be-103">Specify custom storage locations for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="051be-104">Met de API (Application Programming Interface) van het ER-raamwerk kunt u de lijst met opslaglocaties uitbreiden voor documenten waarmee ER-indelingen worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="051be-104">The application programming interface (API) of the Electronic reporting (ER) framework lets you extend the list of storage locations for documents that ER formats generate.</span></span> <span data-ttu-id="051be-105">In dit onderwerp wordt uitgelegd hoe u een aangepaste opslaglocatie voor gegenereerde documenten kunt toevoegen door de taak voor het maken van ER-bestemmingen te delegeren aan de standaard bestemmingsfabriek en vervolgens een aangepaste klasse te implementeren die een eigen bestemmingslogica heeft.</span><span class="sxs-lookup"><span data-stu-id="051be-105">This topic explains how to add a custom storage location for generated documents by delegating the task of creating ER destinations to the default destination factory and then implementing a custom class that has its own destination logic.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="051be-106">Vereisten</span><span class="sxs-lookup"><span data-stu-id="051be-106">Prerequisites</span></span>

<span data-ttu-id="051be-107">Implementeer een topologie die ondersteuning biedt voor continuous build.</span><span class="sxs-lookup"><span data-stu-id="051be-107">Deploy a topology that supports continuous build.</span></span> <span data-ttu-id="051be-108">Zie [Topologieën implementeren die ondersteuning bieden voor continue bouw- en testautomatisering](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="051be-108">For more information, see [Deploy topologies that support continuous build and test automation](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).</span></span> <span data-ttu-id="051be-109">U moet ook toegang hebben tot deze topologie voor een van de volgende rollen:</span><span class="sxs-lookup"><span data-stu-id="051be-109">You must have access to this topology for one of the following roles:</span></span>

- <span data-ttu-id="051be-110">Ontwikkelaar elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="051be-110">Electronic reporting developer</span></span>
- <span data-ttu-id="051be-111">Functioneel consultant elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="051be-111">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="051be-112">Systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="051be-112">System administrator</span></span>

<span data-ttu-id="051be-113">U moet ook toegang hebben tot de ontwikkelomgeving voor deze topologie.</span><span class="sxs-lookup"><span data-stu-id="051be-113">You must also have access to the development environment for this topology.</span></span>

<span data-ttu-id="051be-114">Alle taken in dit onderwerp kunnen in het bedrijf **USMF** worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="051be-114">All the tasks in this topic can be completed in the **USMF** company.</span></span>

## <a name="import-the-fixed-asset-roll-forward-er-format"></a><span data-ttu-id="051be-115">De ER-indeling voor Voortschrijdende prognose voor vaste activa importeren</span><span class="sxs-lookup"><span data-stu-id="051be-115">Import the Fixed asset roll forward ER format</span></span>

<span data-ttu-id="051be-116">Als u de documenten wilt genereren waarvoor u een aangepaste opslaglocatie wilt toevoegen, [importeert](er-download-configurations-global-repo.md) u de configuratie van de ER-indeling **Voortschrijdende prognose voor vaste activa** in de huidige topologie.</span><span class="sxs-lookup"><span data-stu-id="051be-116">To generate the documents that you plan to add a custom storage location for, [import](er-download-configurations-global-repo.md) the **Fixed asset roll forward** ER format configuration into the current topology.</span></span>

![Configuratie archiefpagina](./media/er-custom-storage-generated-files-import-format.png)

## <a name="run-the-fixed-asset-roll-forward-report"></a><span data-ttu-id="051be-118">Het rapport voor voortschrijdende prognose voor vaste activa uitvoeren</span><span class="sxs-lookup"><span data-stu-id="051be-118">Run the Fixed asset roll forward report</span></span>

1. <span data-ttu-id="051be-119">Ga naar **Vaste activa** \> **Query's en rapporten** \> **Transactierapporten** \> **Voortschrijdende prognose voor vaste activa**.</span><span class="sxs-lookup"><span data-stu-id="051be-119">Go to **Fixed assets** \> **Inquiries and reports** \> **Transaction reports** \> **Fixed asset roll forward**.</span></span>
2. <span data-ttu-id="051be-120">Voer in het veld **Begindatum** de waarde **1/1/2017** (1 januari 2017) in.</span><span class="sxs-lookup"><span data-stu-id="051be-120">In the **From date** field, enter **1/1/2017** (January 1, 2017).</span></span>
3. <span data-ttu-id="051be-121">Voer in het veld **Einddatum** de waarde **1/31/2017** (31 januari 2017) in.</span><span class="sxs-lookup"><span data-stu-id="051be-121">In the **To date** field, enter **1/31/2017** (January 31, 2017).</span></span>
4. <span data-ttu-id="051be-122">Selecteer in het veld **Valuta** de optie **Boekhoudvaluta**.</span><span class="sxs-lookup"><span data-stu-id="051be-122">In the **Currency field**, select **Accounting currency**.</span></span>
5. <span data-ttu-id="051be-123">Selecteer in het veld **Indelingstoewijzing** de optie **Voortschrijdende prognose voor vaste activa**.</span><span class="sxs-lookup"><span data-stu-id="051be-123">In the **Format mapping** field, select **Fixed asset roll forward**.</span></span>
6. <span data-ttu-id="051be-124">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="051be-124">Select **OK**.</span></span>

![Het runtime-dialoogvenster voor het rapport Voortschrijdende prognose voor vaste activa](./media/er-custom-storage-generated-files-runtime-dialog.png)

<span data-ttu-id="051be-126">Controleer in Microsoft Excel het uitgaande document dat is gegenereerd en beschikbaar is voor downloaden.</span><span class="sxs-lookup"><span data-stu-id="051be-126">In Microsoft Excel, review the outbound document that is generated and available for download.</span></span> <span data-ttu-id="051be-127">Dit gedrag is het [standaardgedrag](electronic-reporting-destinations.md#default-behavior) voor een ER-indeling waarvoor geen [bestemmingen](electronic-reporting-destinations.md) zijn geconfigureerd en die in de interactieve modus wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="051be-127">This behavior is the [default behavior](electronic-reporting-destinations.md#default-behavior) for an ER format that no [destinations](electronic-reporting-destinations.md) are configured for, and that is running in interactive mode.</span></span>

## <a name="review-the-source-code"></a><span data-ttu-id="051be-128">De broncode controleren</span><span class="sxs-lookup"><span data-stu-id="051be-128">Review the source code</span></span>

<span data-ttu-id="051be-129">Controleer de code van de methode `generateReportByGER()` van de klasse `AssetRollForwardService`.</span><span class="sxs-lookup"><span data-stu-id="051be-129">Review the code of the `generateReportByGER()` method of the `AssetRollForwardService` class.</span></span> <span data-ttu-id="051be-130">U ziet dat de methode `Run()` wordt gebruikt om het ER-raamwerk aan te roepen en het rapport **Voortschrijdende prognose voor vaste activa** te genereren.</span><span class="sxs-lookup"><span data-stu-id="051be-130">Notice that the `Run()` method is used to call the ER framework and generate the **Fixed asset roll forward** report.</span></span>

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

## <a name="modify-the-source-code"></a><span data-ttu-id="051be-131">De broncode wijzigen</span><span class="sxs-lookup"><span data-stu-id="051be-131">Modify the source code</span></span>

1. <span data-ttu-id="051be-132">Voeg in het Visual Studio-project een nieuwe klasse toe (`AssetRollForwardDestination` in dit voorbeeld) en schrijf code om uw aangepaste doel te implementeren voor rapporten **Voortschrijdende prognose voor vaste activa** die worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="051be-132">In your Visual Studio project, add a new class (`AssetRollForwardDestination` in this example), and write code to implement your custom destination for **Fixed asset roll forward** reports that are generated.</span></span>

    - <span data-ttu-id="051be-133">De methode `new()` is bedoeld om het oorspronkelijke ER-bestemmingsobject en de via toepassingslogica gestuurde parameter op te halen die de aangepaste locatie aangeeft waar gegenereerde rapporten moeten worden opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="051be-133">The `new()` method is designed to get the original ER destination object and the application logic–driven parameter that specifies the custom location where generated reports should be stored.</span></span> <span data-ttu-id="051be-134">In dit voorbeeld is de aangepaste locatie de naam van een map van het lokale bestandssysteem van de server waarop de AOS-service (Application Object Server) wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="051be-134">In this example, the custom location is the name of a folder of the local file system of the server that runs the Application Object Server (AOS) service.</span></span>
    - <span data-ttu-id="051be-135">De methode `saveFile()` is ontworpen om een gegenereerd document op te slaan in een map van het lokale bestandssysteem van de server waarop de AOS-service wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="051be-135">The `saveFile()` method is designed to save a generated document to a folder of the local file system of the server that runs the AOS service.</span></span>

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

2. <span data-ttu-id="051be-136">Voeg in uw Visual Studio-project een nieuwe klasse toe (`AssetRollForwardDestinationFactory` in dit voorbeeld) en schrijf code om een aangepaste bestemmingsfabriek in te stellen waarmee het maken van een bestemming wordt gedelegeerd naar de standaardfabriek en om een bestandsbestemming van uw eigen bestemming te voorzien.</span><span class="sxs-lookup"><span data-stu-id="051be-136">In your Visual Studio project, add a new class (`AssetRollForwardDestinationFactory` in this example), and write code to set up a custom destination factory that delegates the creation of a destination to the default destination factory, and to wrap a file destination with your own destination.</span></span>

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

3. <span data-ttu-id="051be-137">Wijzig de bestaande klasse `AssetRollForwardService` en schrijf code om een aangepaste bestemmingsfabriek in te stellen voor de rapportuitvoeringsfunctie.</span><span class="sxs-lookup"><span data-stu-id="051be-137">Modify the existing `AssetRollForwardService` class, and write code to set up a custom destination factory for the report runner.</span></span> <span data-ttu-id="051be-138">Wanneer een aangepaste bestemmingsfabriek is opgebouwd, wordt de toepassingsgestuurde parameter die een bestemmingsmap opgeeft doorgegeven.</span><span class="sxs-lookup"><span data-stu-id="051be-138">Notice that when a custom destination factory is constructed, the application-driven parameter that specifies a target folder is passed.</span></span> <span data-ttu-id="051be-139">Op deze manier wordt de bestemmingsmap gebruikt om gegenereerde bestanden op te slaan.</span><span class="sxs-lookup"><span data-stu-id="051be-139">In this way, that target folder is used to store generated files.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="051be-140">Controleer of de opgegeven map (**c:\\0** in dit voorbeeld) aanwezig is in het lokale bestandssysteem van de server waarop de AOS-service wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="051be-140">Make sure that the specified folder (**c:\\0** in this example) is present in the local file system of the server that runs the AOS service.</span></span> <span data-ttu-id="051be-141">Anders wordt een uitzondering [DirectoryNotFoundException](https://docs.microsoft.com/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1) gegenereerd tijdens runtime.</span><span class="sxs-lookup"><span data-stu-id="051be-141">Otherwise, a [DirectoryNotFoundException](https://docs.microsoft.com/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1) exception will be thrown at runtime.</span></span>

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

4. <span data-ttu-id="051be-142">Maak uw project opnieuw.</span><span class="sxs-lookup"><span data-stu-id="051be-142">Rebuild your project.</span></span>

## <a name="re-run-the-fixed-asset-roll-forward-report"></a><span data-ttu-id="051be-143">Het rapport voor voortschrijdende prognose voor vaste activa opnieuw uitvoeren</span><span class="sxs-lookup"><span data-stu-id="051be-143">Re-run the Fixed asset roll forward report</span></span>

1. <span data-ttu-id="051be-144">Ga naar **Vaste activa** \> **Query's en rapporten** \> **Transactierapporten** \> **Voortschrijdende prognose voor vaste activa**.</span><span class="sxs-lookup"><span data-stu-id="051be-144">Go to **Fixed assets** \> **Inquiries and reports** \> **Transaction reports** \> **Fixed asset roll forward**.</span></span>
2. <span data-ttu-id="051be-145">Voer in het veld **Begindatum** de waarde **1/1/2017** in.</span><span class="sxs-lookup"><span data-stu-id="051be-145">In the **From date** field, enter **1/1/2017**.</span></span>
3. <span data-ttu-id="051be-146">Voer in het veld **Einddatum** de waarde **1/31/2017** in.</span><span class="sxs-lookup"><span data-stu-id="051be-146">In the **To date** field, enter **1/31/2017**.</span></span>
4. <span data-ttu-id="051be-147">Selecteer in het veld **Valuta** de optie **Boekhoudvaluta**.</span><span class="sxs-lookup"><span data-stu-id="051be-147">In the **Currency field**, select **Accounting currency**.</span></span>
5. <span data-ttu-id="051be-148">Selecteer in het veld **Indelingstoewijzing** de optie **Voortschrijdende prognose voor vaste activa**.</span><span class="sxs-lookup"><span data-stu-id="051be-148">In the **Format mapping** field, select **Fixed asset roll forward**.</span></span>
6. <span data-ttu-id="051be-149">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="051be-149">Select **OK**.</span></span>
7. <span data-ttu-id="051be-150">Blader door de lokale map **C:\\0** om het gegenereerde bestand te zoeken.</span><span class="sxs-lookup"><span data-stu-id="051be-150">Browse the local **C:\\0** folder to find the generated file.</span></span>

> [!NOTE]
> <span data-ttu-id="051be-151">Omdat het object `originDestination` in dit voorbeeld niet wordt gebruikt in het object `AssetRollForwardDestination`, worden de configuraties voor de [bestemmingen](electronic-reporting-destinations.md) van de ER-indeling genegeerd tijdens runtime.</span><span class="sxs-lookup"><span data-stu-id="051be-151">Because the `originDestination` object isn't used in the `AssetRollForwardDestination` object in this example, the configurations for the ER format [destinations](electronic-reporting-destinations.md) will be ignored at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="051be-152">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="051be-152">Additional resources</span></span>

- [<span data-ttu-id="051be-153">Bestemmingen van elektronische rapportage (ER)</span><span class="sxs-lookup"><span data-stu-id="051be-153">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="051be-154">Startpagina voor Uitbreidbaarheid</span><span class="sxs-lookup"><span data-stu-id="051be-154">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]