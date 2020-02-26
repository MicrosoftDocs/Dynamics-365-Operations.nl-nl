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
ms.openlocfilehash: 45a2335d7a661ddc1d8907c56ae8193387f44e26
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/07/2020
ms.locfileid: "3030861"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a>Een aangepaste opslaglocatie voor gegenereerde documenten opgeven

[!include[banner](../includes/banner.md)]

Met de API (Application Programming Interface) van het ER-raamwerk kunt u de lijst met opslaglocaties uitbreiden voor documenten waarmee ER-indelingen worden gegenereerd. Dit onderwerp bevat een overzicht van de belangrijkste taken die u moet uitvoeren om een aangepaste opslaglocatie toe te voegen.

## <a name="prerequisites"></a>Vereisten

U moet een topologie implementeren die ondersteuning biedt voor continuous build. (Zie voor meer informatie [Topologieën implementeren die ondersteuning bieden aan continuous build en testautomatisering](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) U moet toegang hebben tot deze topologie voor een van de volgende rollen:

- Ontwikkelaar elektronische rapportage
- Functioneel consultant elektronische rapportage
- Systeembeheerder

U moet ook toegang hebben tot de ontwikkelomgeving voor deze topologie.

## <a name="create-or-import-an-er-format-configuration"></a>Een configuratie voor ER-indeling maken of importeren

In de huidige topologie [maakt u een nieuwe ER-indeling](tasks/er-format-configuration-2016-11.md) voor het genereren van documenten waarvoor u een aangepaste opslaglocatie wilt toevoegen. U kunt ook [een bestaande ER-indeling importeren naar deze topologie](general-electronic-reporting-manage-configuration-lifecycle.md).

![Pagina Indelingsontwerper](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> De ER-indeling die u maakt of importeert, moet ten minste één van de volgende indelingselementen bevatten:
>
> - Bestand
> - Map
> - Samenvoeger
> - Bijlage

## <a name="create-a-new-document-type"></a>Een nieuw documenttype maken

Als u wilt opgeven hoe documenten worden doorgestuurd waarmee een ER-indeling wordt gegenereerd, moet u [Bestemmingen van elektronische rapportage (ER)](electronic-reporting-destinations.md) configureren. In elke ER-bestemming die is geconfigureerd voor het opslaan van gegenereerde documenten zoals bestanden, moet u een documenttype van het raamwerk voor documentbeheer opgeven. Verschillende documenttypen kunnen worden gebruikt om documenten door te sturen waarmee verschillende ER-indelingen worden gegenereerd.

1. Voeg een nieuw [documenttype](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management) toe voor de ER-indeling die u eerder hebt gemaakt of geïmporteerd. In de volgende afbeelding is het documenttype **FileX**.
2. Als u dit documenttype wilt onderscheiden van andere documenttypen, neemt u een specifiek trefwoord in de naam op. In de volgende afbeelding is de naam bijvoorbeeld **(LOCAL) map**.
3. Geef in het veld **Klasse** **Bestand bijvoegen** op.
4. Geef in het veld **Groep** **Bestand** op.

![Pagina Documenttypen](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> Documenttypen zijn bedrijfsspecifiek. Als u een ER-indeling met een geconfigureerde bestemming in meerdere bedrijven wilt gebruiken, moet u een afzonderlijk documenttype in elk bedrijf configureren.

## <a name="review-source-code"></a>Broncode controleren

Controleer de code van de methode **insertFile()** van de klasse **ERDocuManagement**. Merk op dat de gebeurtenis **AttachingFile()** wordt geactiveerd terwijl het gegenereerde bestand aan een record wordt gekoppeld.

```xpp
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

De gebeurtenis **AttachingFile()** wordt geactiveerd wanneer de volgende ER-bestemmingen worden verwerkt:

- **Archief** : wanneer deze bestemming wordt gebruikt, wordt een nieuwe record voor de ER-indeling die wordt uitgevoerd, gemaakt in de tabel ERFormatMappingRunJobTable. Het veld **Gearchiveerd** in deze record wordt ingesteld op **False**. Als de ER-indeling met succes wordt uitgevoerd, wordt het gegenereerde document gekoppeld aan deze record en wordt de gebeurtenis **AttachingFile()** geactiveerd. Met het documenttype dat wordt geselecteerd in deze ER-bestemming, wordt de opslaglocatie voor het gekoppelde bestand (Microsoft Azure-opslag of een Microsoft SharePoint-map) bepaald.
- **Taakarchief** : wanneer deze bestemming wordt gebruikt, wordt een nieuwe record voor de ER-indeling die wordt uitgevoerd, gemaakt in de tabel ERFormatMappingRunJobTable. Het veld **Gearchiveerd** in deze record wordt ingesteld op **True**. Als de ER-indeling met succes wordt uitgevoerd, wordt het gegenereerde document gekoppeld aan deze record en wordt de gebeurtenis **AttachingFile()** geactiveerd. Met het documenttype dat wordt geconfigureerd in de ER-parameters, wordt de opslaglocatie voor het gekoppelde bestand (Azure-opslag of een SharePoint-map) bepaald.

![Pagina Parameters van elektronische rapportage](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a>Een ER-bestemming configureren

1. Configureer de gearchiveerde bestemming voor een van de eerder genoemde elementen (bestand, map, samenvoeger of bijlage) van de ER-indeling die u hebt gemaakt of geïmporteerd. Raadpleeg voor richtlijnen [ER-bestemmingen configureren](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).
2. Gebruik het documenttype dat u eerder hebt toegevoegd voor de geconfigureerde bestemming. (Voor het voorbeeld in dit onderwerp is het documenttype **FileX**.)

![Dialoogvenster Bestemmingsinstellingen](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a>Broncode wijzigen

1. Voeg een nieuwe klasse aan uw Microsoft Visual Studio-project toe en schrijf code om u te abonneren op de eerder vermelde gebeurtenis **AttachingFile()**. (Zie voor meer informatie over het uitbreidbaarheidspatroon dat wordt gebruikt [Reageren met behulp van EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) Schrijf bijvoorbeeld in de nieuwe klasse code waarmee de volgende acties worden uitgevoerd:

    1. Sla gegenereerde bestanden op in een map van het lokale bestandssysteem van de server waarop de service Application Object Server (AOS) wordt uitgevoerd.
    2. Sla deze gegenereerde bestanden alleen op als het nieuwe documenttype (bijvoorbeeld het type **FileX** met het trefwoord '(LOCAL)' in de naam) wordt gebruikt terwijl een bestand wordt gekoppeld aan de record in het logboek van de ER-uitvoeringstaak.

    ```xpp
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

2. Maak uw project opnieuw.

## <a name="run-the-er-format-that-you-created-or-imported"></a>De ER-indeling uitvoeren die u hebt gemaakt of geïmporteerd

1. Voer de ER-indeling uit die u hebt gemaakt of geïmporteerd.
2. Ga naar **Organisatiebeheer \> Elektronische rapportage \> Elektronische rapportagetaken**. Zoek de record die is gemaakt voor deze uitvoeringstaak en waaraan het gegenereerde bestand is gekoppeld.
3. Verken de lokale map **C:\\0** om hetzelfde gegenereerde bestand te zoeken.

## <a name="additional-resources"></a>Aanvullende resources

- [Bestemmingen van elektronische rapportage (ER)](electronic-reporting-destinations.md)
- [Startpagina voor Uitbreidbaarheid](../extensibility/extensibility-home-page.md)
