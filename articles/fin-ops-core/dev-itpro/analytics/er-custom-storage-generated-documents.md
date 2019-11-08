---
title: Een aangepaste opslaglocatie voor gegenereerde documenten opgeven
description: In dit onderwerp wordt uitgelegd hoe u de lijst met opslaglocaties uitbreidt voor documenten waarmee indelingen voor elektronische rapportage (ER) worden gegenereerd.
author: NickSelin
manager: AnnBe
ms.date: 02/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10
ms.openlocfilehash: f65118b6a7393ced9d80c30fad7540a7b27da6c7
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569079"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a><span data-ttu-id="1b3a7-103">Een aangepaste opslaglocatie voor gegenereerde documenten opgeven</span><span class="sxs-lookup"><span data-stu-id="1b3a7-103">Specify a custom storage location for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1b3a7-104">Met de API (Application Programming Interface) van het ER-raamwerk kunt u de lijst met opslaglocaties uitbreiden voor documenten waarmee ER-indelingen worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-104">The application programming interface (API) of the Electronic reporting (ER) framework lets you extend the list of storage locations for documents that ER formats generate.</span></span> <span data-ttu-id="1b3a7-105">Dit onderwerp bevat een overzicht van de belangrijkste taken die u moet uitvoeren om een aangepaste opslaglocatie toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-105">This topic includes an overview of the main tasks that you must complete to add a custom storage location.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1b3a7-106">Vereisten</span><span class="sxs-lookup"><span data-stu-id="1b3a7-106">Prerequisites</span></span>

<span data-ttu-id="1b3a7-107">U moet een topologie implementeren die ondersteuning biedt voor continuous build.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-107">You must deploy a topology that supports continuous build.</span></span> <span data-ttu-id="1b3a7-108">(Zie voor meer informatie [Topologieën implementeren die ondersteuning bieden aan continuous build en testautomatisering](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) U moet toegang hebben tot deze topologie voor een van de volgende rollen:</span><span class="sxs-lookup"><span data-stu-id="1b3a7-108">(For more information, see [Deploy topologies that support continuous build and test automation](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) You must have access to this topology for one of the following roles:</span></span>

- <span data-ttu-id="1b3a7-109">Ontwikkelaar elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="1b3a7-109">Electronic reporting developer</span></span>
- <span data-ttu-id="1b3a7-110">Functioneel consultant elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="1b3a7-110">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="1b3a7-111">Systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="1b3a7-111">System administrator</span></span>

<span data-ttu-id="1b3a7-112">U moet ook toegang hebben tot de ontwikkelomgeving voor deze topologie.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-112">You must also have access to the development environment for this topology.</span></span>

## <a name="create-or-import-an-er-format-configuration"></a><span data-ttu-id="1b3a7-113">Een configuratie voor ER-indeling maken of importeren</span><span class="sxs-lookup"><span data-stu-id="1b3a7-113">Create or import an ER format configuration</span></span>

<span data-ttu-id="1b3a7-114">In de huidige topologie [maakt u een nieuwe ER-indeling](tasks/er-format-configuration-2016-11.md) voor het genereren van documenten waarvoor u een aangepaste opslaglocatie wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-114">In the current topology, [create a new ER format](tasks/er-format-configuration-2016-11.md) to generate documents that you plan to add a custom storage location for.</span></span> <span data-ttu-id="1b3a7-115">U kunt ook [een bestaande ER-indeling importeren naar deze topologie](general-electronic-reporting-manage-configuration-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="1b3a7-115">Alternatively, [import an existing ER format into this topology](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![Pagina Indelingsontwerper](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> <span data-ttu-id="1b3a7-117">De ER-indeling die u maakt of importeert, moet ten minste één van de volgende indelingselementen bevatten:</span><span class="sxs-lookup"><span data-stu-id="1b3a7-117">The ER format that you create or import must contain at least one of the following format elements:</span></span>
>
> - <span data-ttu-id="1b3a7-118">Bestand</span><span class="sxs-lookup"><span data-stu-id="1b3a7-118">File</span></span>
> - <span data-ttu-id="1b3a7-119">Map</span><span class="sxs-lookup"><span data-stu-id="1b3a7-119">Folder</span></span>
> - <span data-ttu-id="1b3a7-120">Samenvoeger</span><span class="sxs-lookup"><span data-stu-id="1b3a7-120">Merger</span></span>
> - <span data-ttu-id="1b3a7-121">Bijlage</span><span class="sxs-lookup"><span data-stu-id="1b3a7-121">Attachment</span></span>

## <a name="create-a-new-document-type"></a><span data-ttu-id="1b3a7-122">Een nieuw documenttype maken</span><span class="sxs-lookup"><span data-stu-id="1b3a7-122">Create a new document type</span></span>

<span data-ttu-id="1b3a7-123">Als u wilt opgeven hoe documenten worden doorgestuurd waarmee een ER-indeling wordt gegenereerd, moet u [ER-bestemmingen](electronic-reporting-destinations.md) configureren.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-123">To specify how documents that an ER format generates are routed, you must configure [ER destinations](electronic-reporting-destinations.md).</span></span> <span data-ttu-id="1b3a7-124">In elke ER-bestemming die is geconfigureerd voor het opslaan van gegenereerde documenten zoals bestanden, moet u een documenttype van het raamwerk voor documentbeheer opgeven.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-124">In each ER destination that is configured to store generated documents as files, you must specify a document type of the Document management framework.</span></span> <span data-ttu-id="1b3a7-125">Verschillende documenttypen kunnen worden gebruikt om documenten door te sturen waarmee verschillende ER-indelingen worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-125">Different document types can be used to route documents that different ER formats generate.</span></span>

1. <span data-ttu-id="1b3a7-126">Voeg een nieuw [documenttype](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management) toe voor de ER-indeling die u eerder hebt gemaakt of geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-126">Add a new [document type](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management) for the ER format that you created or imported earlier.</span></span> <span data-ttu-id="1b3a7-127">In de volgende afbeelding is het documenttype **FileX**.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-127">In the illustration that follows, the document type is **FileX**.</span></span>
2. <span data-ttu-id="1b3a7-128">Als u dit documenttype wilt onderscheiden van andere documenttypen, neemt u een specifiek trefwoord in de naam op.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-128">To differentiate this document type from other document types, include a specific keyword in its name.</span></span> <span data-ttu-id="1b3a7-129">In de volgende afbeelding is de naam bijvoorbeeld **(LOCAL) map**.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-129">For example, in the illustration that follows, the name is **(LOCAL) folder**.</span></span>
3. <span data-ttu-id="1b3a7-130">Geef in het veld **Klasse** **Bestand bijvoegen** op.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-130">In the **Class** field, specify **Attach file**.</span></span>
4. <span data-ttu-id="1b3a7-131">Geef in het veld **Groep** **Bestand** op.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-131">In the **Group** field, specify **File**.</span></span>

![Pagina Documenttypen](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> <span data-ttu-id="1b3a7-133">Documenttypen zijn bedrijfsspecifiek.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-133">Document types are company-specific.</span></span> <span data-ttu-id="1b3a7-134">Als u een ER-indeling met een geconfigureerde bestemming in meerdere bedrijven wilt gebruiken, moet u een afzonderlijk documenttype in elk bedrijf configureren.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-134">To use an ER format with a configured destination in multiple companies, you must configure a separate document type in each company.</span></span>

## <a name="review-source-code"></a><span data-ttu-id="1b3a7-135">Broncode controleren</span><span class="sxs-lookup"><span data-stu-id="1b3a7-135">Review source code</span></span>

<span data-ttu-id="1b3a7-136">Controleer de code van de methode **insertFile()** van de klasse **ERDocuManagement**.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-136">Review the code of the **insertFile()** method of the **ERDocuManagement** class.</span></span> <span data-ttu-id="1b3a7-137">Merk op dat de gebeurtenis **AttachingFile()** wordt geactiveerd terwijl het gegenereerde bestand aan een record wordt gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-137">Notice that the **AttachingFile()** event is raised while the generated file is attached to a record.</span></span>

```
/// <summary>
/// Inserts file as attachment in Document Management.
/// </summary>
/// <param name = "_owner">A record as the attachment owner.</param>
/// <param name = "_stream">The file stream.</param>
/// <param name = "_filePath">The file path with name.</param>
/// <param name = "_attachmentName">The name of file attachment.</param>
/// <returns>The reference to inserted file.</returns>
[Hookable(false)]
public DocuRef insertFile(
    Common _owner, 
    System.IO.Stream _stream, 
    str _filePath, 
    str _attachmentName, 
    DocuTypeId _docuTypeId)
{
    DocuRef docuRef;
    if (_stream)
    {
        DocuType::createDefaults();
        if (!this.isDocuTypeValid(_docuTypeId))
        {
            throw error(strFmt("@ElectronicReporting:DocuTypeIsNotValid", _docuTypeId));
        }
        var args = ERDocuManagementAttachingFileEventArgs::construct(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        ERDocuManagementEvents::onAttachingFile(args);
        if (args.isHandled())
        {
            docuRef = args.getDocuRef();
        }
        else
        {
            docuRef = this.attachFile(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        }
    }
    return docuRef;
}
```

<span data-ttu-id="1b3a7-138">De gebeurtenis **AttachingFile()** wordt geactiveerd wanneer de volgende ER-bestemmingen worden verwerkt:</span><span class="sxs-lookup"><span data-stu-id="1b3a7-138">The **AttachingFile()** event is raised when the following ER destinations are processed:</span></span>

- <span data-ttu-id="1b3a7-139">**Archief** : wanneer deze bestemming wordt gebruikt, wordt een nieuwe record voor de ER-indeling die wordt uitgevoerd, gemaakt in de tabel ERFormatMappingRunJobTable.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-139">**Archive** – When this destination is used, a new record for the ER format that is run is created in the ERFormatMappingRunJobTable table.</span></span> <span data-ttu-id="1b3a7-140">Het veld **Gearchiveerd** in deze record wordt ingesteld op **False**.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-140">The **Archived** field in this record is set to **False**.</span></span> <span data-ttu-id="1b3a7-141">Als de ER-indeling met succes wordt uitgevoerd, wordt het gegenereerde document gekoppeld aan deze record en wordt de gebeurtenis **AttachingFile()** geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-141">If the ER format is successfully run, the generated document is attached to this record, and the **AttachingFile()** event is raised.</span></span> <span data-ttu-id="1b3a7-142">Met het documenttype dat wordt geselecteerd in deze ER-bestemming, wordt de opslaglocatie voor het gekoppelde bestand (Microsoft Azure-opslag of een Microsoft SharePoint-map) bepaald.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-142">The document type that is selected in this ER destination determines the storage location for the attached file (Microsoft Azure Storage or a Microsoft SharePoint folder).</span></span>
- <span data-ttu-id="1b3a7-143">**Taakarchief** : wanneer deze bestemming wordt gebruikt, wordt een nieuwe record voor de ER-indeling die wordt uitgevoerd, gemaakt in de tabel ERFormatMappingRunJobTable.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-143">**Job archive** – When this destination is used, a new record for the ER form that is run is created in the ERFormatMappingRunJobTable table.</span></span> <span data-ttu-id="1b3a7-144">Het veld **Gearchiveerd** in deze record wordt ingesteld op **True**.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-144">The **Archived** field in this record is set to **True**.</span></span> <span data-ttu-id="1b3a7-145">Als de ER-indeling met succes wordt uitgevoerd, wordt het gegenereerde document gekoppeld aan deze record en wordt de gebeurtenis **AttachingFile()** geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-145">If the ER format is successfully run, the generated document is attached to this record, and the **AttachingFile()** event is raised.</span></span> <span data-ttu-id="1b3a7-146">Met het documenttype dat wordt geconfigureerd in de ER-parameters, wordt de opslaglocatie voor het gekoppelde bestand (Azure-opslag of een SharePoint-map) bepaald.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-146">The document type that is configured in the ER parameters determines the storage location for the attached file (Azure Storage or a SharePoint folder).</span></span>

![Pagina Parameters van elektronische rapportage](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a><span data-ttu-id="1b3a7-148">Een ER-bestemming configureren</span><span class="sxs-lookup"><span data-stu-id="1b3a7-148">Configure an ER destination</span></span>

1. <span data-ttu-id="1b3a7-149">Configureer de gearchiveerde bestemming voor een van de eerder genoemde elementen (bestand, map, samenvoeger of bijlage) van de ER-indeling die u hebt gemaakt of geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-149">Configure the archived destination for one of the previously mentioned elements (file, folder, merger, or attachment) of the ER format that you created or imported.</span></span> <span data-ttu-id="1b3a7-150">Raadpleeg voor richtlijnen [ER-bestemmingen configureren](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).</span><span class="sxs-lookup"><span data-stu-id="1b3a7-150">For guidance, see [ER Configure destinations](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).</span></span>
2. <span data-ttu-id="1b3a7-151">Gebruik het documenttype dat u eerder hebt toegevoegd voor de geconfigureerde bestemming.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-151">Use the document type that you added earlier for the configured destination.</span></span> <span data-ttu-id="1b3a7-152">(Voor het voorbeeld in dit onderwerp is het documenttype **FileX**.)</span><span class="sxs-lookup"><span data-stu-id="1b3a7-152">(For the example in this topic, the document type is **FileX**.)</span></span>

![Dialoogvenster Bestemmingsinstellingen](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a><span data-ttu-id="1b3a7-154">Broncode wijzigen</span><span class="sxs-lookup"><span data-stu-id="1b3a7-154">Modify source code</span></span>

1. <span data-ttu-id="1b3a7-155">Voeg een nieuwe klasse aan uw Microsoft Visual Studio-project toe en schrijf code om u te abonneren op de eerder vermelde gebeurtenis **AttachingFile()**.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-155">Add a new class to your Microsoft Visual Studio project, and write code to subscribe to the **AttachingFile()** event that was mentioned earlier.</span></span> <span data-ttu-id="1b3a7-156">(Zie voor meer informatie over het uitbreidbaarheidspatroon dat wordt gebruikt [Reageren met behulp van EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) Schrijf bijvoorbeeld in de nieuwe klasse code waarmee de volgende acties worden uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="1b3a7-156">(For more information about the extensibility pattern that is used, see [Respond by using EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) For example, in the new class, write code that performs the following actions:</span></span>

    1. <span data-ttu-id="1b3a7-157">Sla gegenereerde bestanden op in een map van het lokale bestandssysteem van de server waarop de service Application Object Server (AOS) wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-157">Store generated files in a folder of the local file system of the server that runs the Application Object Server (AOS) service.</span></span>
    2. <span data-ttu-id="1b3a7-158">Sla deze gegenereerde bestanden alleen op als het nieuwe documenttype (bijvoorbeeld het type **FileX** met het trefwoord '(LOCAL)' in de naam) wordt gebruikt terwijl een bestand wordt gekoppeld aan de record in het logboek van de ER-uitvoeringstaak.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-158">Store these generated files only when the new document type (for example, the **FileX** type that has the "(LOCAL)" keyword in its name) is used while a file is attached to the record in the ER execution job log.</span></span>

    ```
    class ERDocuSubscriptionSample
    {
        void new()
        {
        }
        [SubscribesTo(classStr(ERDocuManagementEvents), 
        staticDelegateStr(ERDocuManagementEvents, 
        attachingFile))]
        public static void ERDocuManagementEvents_attachingFile(ERDocuManagementAttachingFileEventArgs _args)
        {
            if (!_args.isHandled())
            {
                DocuType docuType = DocuType::find(_args.getDocuTypeId());
                if (strContains(docuType.Name, '(LOCAL)'))
                {
                    _args.markAsHandled();
                    var stream = _args.getStream();
                    if (stream.CanSeek)
                    {
                        stream.Seek(0, System.IO.SeekOrigin::Begin);
                    }
                    using (var localStream = System.IO.File::OpenWrite(@'c:\0\' + _args.getAttachmentName()))
                    {
                        stream.CopyTo(localStream);
                    }
                }
            }
        }
    }
    ```

2. <span data-ttu-id="1b3a7-159">Maak uw project opnieuw.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-159">Rebuild your project.</span></span>

## <a name="run-the-er-format-that-you-created-or-imported"></a><span data-ttu-id="1b3a7-160">De ER-indeling uitvoeren die u hebt gemaakt of geïmporteerd</span><span class="sxs-lookup"><span data-stu-id="1b3a7-160">Run the ER format that you created or imported</span></span>

1. <span data-ttu-id="1b3a7-161">Voer de ER-indeling uit die u hebt gemaakt of geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-161">Execute the ER format that you created or imported.</span></span>
2. <span data-ttu-id="1b3a7-162">Ga naar **Organisatiebeheer \> Elektronische rapportage \> Elektronische rapportagetaken**.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-162">Go to **Organization administration \> Electronic reporting \> Electronic reporting jobs**.</span></span> <span data-ttu-id="1b3a7-163">Zoek de record die is gemaakt voor deze uitvoeringstaak en waaraan het gegenereerde bestand is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-163">Find the record that was created for this execution job, and that has the generated file attached to it.</span></span>
3. <span data-ttu-id="1b3a7-164">Verken de lokale map **C:\\0** om hetzelfde gegenereerde bestand te zoeken.</span><span class="sxs-lookup"><span data-stu-id="1b3a7-164">Explore the local **C:\\0** folder to find same generated file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1b3a7-165">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="1b3a7-165">Additional resources</span></span>

- [<span data-ttu-id="1b3a7-166">Bestemmingen van elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="1b3a7-166">Electronic reporting destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="1b3a7-167">Startpagina voor uitbreidbaarheid</span><span class="sxs-lookup"><span data-stu-id="1b3a7-167">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)