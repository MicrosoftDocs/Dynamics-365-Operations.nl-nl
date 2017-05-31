---
title: "De datamart voor financiële rapportage opnieuw instellen na het herstellen van een database"
description: "In dit onderwerp wordt beschreven hoe u de datamart voor financiële rapportage opnieuw instelt na het terugzetten van een Microsoft Dynamics 365 for Operations-database."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d227452e48914170404f0ee5163a05e6b875e69f
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>De datamart voor financiële rapportage opnieuw instellen na het herstellen van een database

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt beschreven hoe u de datamart voor financiële rapportage opnieuw instelt na het terugzetten van een Microsoft Dynamics 365 for Operations-database. 

Er zijn verschillende scenario's denkbaar waarin u uw Dynamics 365 for Operations-database wilt herstellen vanaf een back-up of de database vanuit een andere omgeving wilt kopiëren. In een dergelijke situatie moet u ook de juiste stappen uitvoeren zodat de datamart voor financiële rapportage correct gebruikmaakt van de herstelde Dynamics 365 for Operations-database. Als u de datamart voor financiële rapportage opnieuw wilt instellen om andere redenen dan het herstel van een Dynamics 365 for Operations-database en hierover vragen hebt, raadpleegt u het onderwerp [De Management Reporter-datamart opnieuw instellen](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) voor meer informatie. Houd er rekening mee dat de stappen in dit proces worden ondersteund voor de release van mei 2016 van Dynamics 365 for Operations (App-build 7.0.1265.23014 en financiële rapportage-build 7.0.10000.4) en nieuwere versies. Als u een eerdere versie van Dynamics 365 for Operations hebt, neem dan contact op met ons ondersteuningsteam voor hulp.

## <a name="export-report-definitions"></a>Rapportdefinities exporteren
Exporteer eerst de rapportontwerpen die zich in de Report Designer bevinden volgens de onderstaande procedure:

1.  Ga in Report Designer naar **Bedrijf** &gt; **Bouwsteengroepen**.
2.  Selecteer de bouwsteengroep die u wilt exporteren en klik op **Exporteren**. **Opmerking:** Voor Dynamics 365 for Operations wordt slechts één bouwsteengroep ondersteund, namelijk **Standaard**.
3.  Selecteer de rapportdefinities die u wilt exporteren:
    -   Om al uw rapportdefinities en de gekoppelde bouwstenen te exporteren klikt u op **Alles selecteren**.
    -   U kunt specifieke rapporten, rijen, kolommen, structuren of dimensiesets exporteren door op het gewenste tabblad te klikken en vervolgens de te exporteren items selecteren. Druk op Ctrl en houd deze toets ingedrukt om meerdere artikelen in een tabblad te selecteren. Als u te exporteren rapporten selecteert, worden de gekoppelde rijen, kolommen, structuren en dimensiesets geselecteerd.

4.  Klik op **Exporteren**.
5.  Voer een bestandsnaam in en selecteer de beveiligde locatie waar u de geëxporteerde rapportdefinities wilt opslaan.
6.  Klik op **Opslaan**.

U kunt het bestand kopiëren of uploaden naar een beveiligde locatie, zodat u het later kunt importeren in een andere omgeving. Informatie over het gebruik van een Microsoft Azure-opslagaccount vindt u in het onderwerp [Gegevensoverdracht met het opdrachtregelprogramma AzCopy](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy). 
> [!NOTE]
> Microsoft biedt bij uw abonnement voor Dynamics 365 for Operations geen opslagaccount aan. U moet een opslagaccount aanschaffen of een opslagaccount uit een separaat Azure-abonnement gebruiken. 
> [!WARNING]
> Houd rekening met het gedrag van het station D in virtuele Azure-machines. Bewaar uw geëxporteerde bouwsteengroepen hier niet permanent. Zie voor meer informatie over tijdelijke schijven het onderwerp [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

## <a name="stop-services"></a>Services afstoppen
Maak via Extern bureaublad verbinding met alle computers in de omgeving en stop de volgende Windows-services af door middel van services.msc:

-   World Wide Web Publishing-service (op alle AOS-computers)
-   Microsoft Dynamics 365 for Operations Batch Management-service (alleen op niet-privé AOS-computers)
-   Management Reporter 2012 Process Service (alleen op BI-computers)

Deze services hebben openstaande verbindingen met de Dynamics 365 for Operations-database.

## <a name="reset"></a>Opnieuw instellen
#### <a name="locate-the-latest-dataupgradezip-package"></a>Het meest recente pakket DataUpgrade.zip zoeken

Zoek het meest recente pakket DataUpgrade.zip met de aanwijzingen in het onderwerp [Het script DataUpgrade.zip downloaden](..\migration-upgrade\upgrade-data-to-latest-update.md). De instructies geven aan hoe u de juiste versie van het gegevensupgradepakket voor uw omgeving vindt.

#### <a name="execute-scripts-against-dynamics-365-for-operations-database"></a>Scripts uitvoeren op de Dynamics 365 for Operations-database

Voer de volgende scripts uit op de Dynamics 365 for Operations-database (niet op de database voor financiële rapportage).

-   DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Deze scripts zorgen ervoor dat de gebruikers, rollen en instellingen voor het bijhouden van wijzigingen juist zijn.

#### <a name="execute-powershell-command-to-reset-database"></a>PowerShell-opdracht uitvoeren om de database opnieuw in te stellen

Voer de volgende opdracht direct op de AOS-computer uit, om de integratie tussen Dynamics 365 for Operations en de financiële rapportage opnieuw in te stellen:

1.  Open Windows PowerShell als beheerder.
2.  Voer uit: F:
3.  Voer uit: cd F:\\MRApplicationService\\MRInstallDirectory
4.  Voer uit: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1
5.  Voer uit: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;mijn_reden_voor_opnieuw_instellen&gt;”
    -   U wordt gevraagd om 'Y' in te voeren om te bevestigen.

Uitleg van parameters:

-   De geldige waarden voor -Reason zijn: SERVICING, BADDATA, OTHER.
-   Bij de parameter -ReasonDetail kunt u vrije tekst invoeren.
-   De waarden voor Reason en ReasonDetail worden vastgelegd in telemetrie/omgevingsbewaking.

## <a name="start-services"></a>Services opstarten
Start de services die u eerder hebt afgestopt opnieuw op door middel van services.msc:

-   World Wide Web Publishing-service (op alle AOS-computers)
-   Microsoft Dynamics 365 for Operations Batch Management-service (alleen op niet-privé AOS-computers)
-   Management Reporter 2012 Process Service (alleen op BI-computers)

## <a name="import-report-definitions"></a>Rapportdefinities importeren
Importeert uw rapportontwerpen vanuit de Report Designer, met behulp van het bestand dat bij het exporteren werd aangemaakt:

1.  Ga in Report Designer naar **Bedrijf** &gt; **Bouwsteengroepen**.
2.  Selecteer de bouwsteengroep die u wilt exporteren en klik op **Exporteren**. 
    > [!NOTE]
    > Voor Dynamics 365 for Operations wordt slechts één bouwsteengroep ondersteund, namelijk **Standaard**.
3.  Selecteer de bouwsteen **Standaard** en klik op **Importeren**.
4.  Selecteer het bestand met de geëxporteerde rapportdefinities en klik op **Openen**.
5.  Selecteer in het dialoogvenster Importeren de te importeren rapportdefinities:
    -   Als u alle rapportdefinities en de ondersteunende bouwstenen wilt importeren, klikt u op **Alles selecteren**.
    -   Om specifieke rapporten, rijen, kolommen, structuren of dimensiesets te importeren, selecteert u de te importeren rapporten, rijen, kolommen, structuren of dimensiesets.

6.  Klik op **Importeren**.





