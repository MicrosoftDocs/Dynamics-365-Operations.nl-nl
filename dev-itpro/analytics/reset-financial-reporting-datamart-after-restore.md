---
title: "De financiële rapportage datamart na het terugzetten van een database terugzetten"
description: "In dit onderwerp wordt beschreven hoe de financiële rapportage datamart na het terugzetten van een Microsoft Dynamics 365 voor bewerkingen database opnieuw."
author: twheeloc
manager: AnnBe
ms.date: 2016-12-08 16 - 20 - 13
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 3967cbb869fbb23d5d7716f619e4c22b4a273921
ms.lasthandoff: 03/29/2017


---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>De financiële rapportage datamart na het terugzetten van een database terugzetten

In dit onderwerp wordt beschreven hoe de financiële rapportage datamart na het terugzetten van een Microsoft Dynamics 365 voor bewerkingen database opnieuw. 

Er zijn verschillende scenario's waarin u mogelijk uw Dynamics 365 voor bewerkingen database terugzetten vanaf een back-up of een kopie van de database vanuit een andere omgeving. Als dit gebeurt, moet u ook de juiste stappen om ervoor te zorgen dat de financiële rapportage datamart correct gebruikmaakt van de teruggezette Dynamics 365 voor bewerkingen-database. Als u vragen hebt over de financiële rapportage datamart om andere redenen buiten een Dynamics 365 voor bewerkingen database terugzetten opnieuw in te stellen, raadpleegt u de [opnieuw instellen van de datamart Management Reporter](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) voor meer informatie. Houd er rekening mee dat de stappen in dit proces worden ondersteund voor Dynamics 365 voor bewerking mei 2016 release (App build 7.0.1265.23014 en financiële rapportage build 7.0.10000.4) en nieuwere versies. Als er een eerdere versie van Dynamics 365 for Operations, neem contact met ons ondersteuningsteam voor meer informatie.

## <a name="export-report-definitions"></a>Rapportdefinities exporteren
Exporteer eerst de rapportontwerpen bevindt zich in de Report Designer als volgt te werk:

1.  In de Report Designer, gaat u naar **bedrijf**&gt;**Bouwsteengroepen**.
2.  Selecteer de groep bouwsteen wilt exporteren en klik op **exporteren**. **opmerking:** voor Dynamics 365 voor bewerkingen, wordt slechts één bouwsteengroep ondersteund, **standaard**.
3.  Selecteer de rapportdefinities die u wilt exporteren:
    -   Om al uw rapportdefinities en de gekoppelde bouwstenen te exporteren klikt u op **Alles selecteren**.
    -   U kunt specifieke rapporten, rijen, kolommen, structuren of dimensiesets exporteren door op het gewenste tabblad te klikken en vervolgens de te exporteren items selecteren. Druk op Ctrl en houd deze toets ingedrukt om meerdere artikelen in een tabblad te selecteren. Wanneer u rapporten wilt exporteren, worden de bijbehorende rijen, kolommen, structuren en dimensiesets worden geselecteerd.

4.  Klik op **exporteren**.
5.  Voer een bestandsnaam en selecteer een beveiligde locatie waar u de geëxporteerde rapportdefinities.
6.  Click **Save**.

Het bestand kan worden gekopieerd en worden geüpload naar een beveiligde locatie, zodat het later opnieuw worden geïmporteerd in een andere omgeving. Informatie over het gebruik van een Microsoft Azure opslag rekening kunt vinden in [gegevensoverdracht met het hulpprogramma AzCopy-opdrachtregelprogramma](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy). **opmerking:** Microsoft niet voorzien in een rekening voor de opslag als onderdeel van uw Dynamics 365 bewerkingen overeenkomst. Kopen van een rekening voor de opslag of gebruik een account van de opslag van een afzonderlijk abonnement dat Azure. **Belangrijk:** rekening houden met de werking van het station D op Azure virtuele Machines. De geëxporteerde bouwsteen-groepen niet permanent wilt behouden. Zie voor meer informatie over tijdelijke schijven [inzicht in de tijdelijke schijf in Windows Azure virtuele Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

## <a name="stop-services"></a>Services stoppen
Extern bureaublad verbinding maken met alle computers in het milieu en de volgende Windows-services stoppen met behulp van services.msc gebruiken:

-   World wide web publishing-service (op alle AOS-computers)
-   Microsoft Dynamics 365 voor bewerkingen Batch Management-Service (privé-AOS alleen op computers)
-   Management Reporter 2012 Processervice (op BI computers)

Deze services heeft open verbinding naar de Dynamics 365 voor bewerkingen-database.

## <a name="reset"></a>Opnieuw instellen
#### <a name="locate-the-latest-dataupgradezip-package"></a>Zoek de meest recente DataUpgrade.zip-pakket

Zoek de meest recente DataUpgrade.zip-pakket met behulp van de aanwijzingen gevonden in [downloaden van het script DataUpgrade.zip](..\migration-upgrade\upgrade-data-to-latest-update.md). De aanwijzingen uitgelegd hoe u de juiste versie van het gegevens-upgrade-pakket voor uw omgeving.

#### <a name="execute-scripts-against-dynamics-365-for-operations-database"></a>Scripts met Dynamics 365 voor bewerkingen database uitvoeren

Voer de volgende scripts ten opzichte van de Dynamics 365 for Operations-database (niet ten opzichte van de financiële rapportage-database).

-   DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Deze scripts zorgen ervoor dat de gebruikers, rollen en instellingen voor het bijhouden van wijzigingen juist zijn.

#### <a name="execute-powershell-command-to-reset-database"></a>PowerShell-opdracht naar de database opnieuw uitvoeren

De volgende opdracht uitvoeren direct op de AOS-computer, opnieuw instellen van de integratie tussen Dynamics 365 for Operations en financiële rapportage:

1.  Open Windows PowerShell als beheerder.
2.  Uitvoeren: F:
3.  Uitvoeren: cd F:\\MRApplicationService\\MRInstallDirectory
4.  Uitvoeren: Import-Module. \\Server\\MRDeploy\\MRDeploy.psd1
5.  Worden uitgevoerd: Reset-DatamartIntegration-andere reden - ReasonDetail '&lt;Mijn reden opnieuw in te stellen&gt;'
    -   U wordt gevraagd om in te voeren 'Y' om te bevestigen.

Uitleg van parameters:

-   De geldige waarden voor - reden zijn: onderhoud, BADDATA, overige.
-   De parameter - ReasonDetail is vrije-tekstfacturen.
-   De reden en reasonDetail worden vastgelegd in telemetrie/omgeving controleren.

## <a name="start-services"></a>Services starten
Gebruik services.msc services die u eerder hebt gestopt opnieuw starten:

-   World wide web publishing-service (op alle AOS-computers)
-   Microsoft Dynamics 365 voor bewerkingen Batch Management-Service (privé-AOS alleen op computers)
-   Management Reporter 2012 Processervice (op BI computers)

## <a name="import-report-definitions"></a>Rapportdefinities importeren
Uw rapportontwerpen importeren vanuit de Report Designer, met behulp van het bestand gemaakt tijdens het exporteren:

1.  In de Report Designer, gaat u naar **bedrijf**&gt;**Bouwsteengroepen**.
2.  Selecteer de groep bouwsteen wilt exporteren en klik op **exporteren**. **opmerking:** voor Dynamics 365 voor bewerkingen, wordt slechts één bouwsteengroep ondersteund, **standaard**.
3.  Selecteer de **standaard** bouwen blokkeren en klik op **importeren**.
4.  Selecteer het bestand met de geëxporteerde rapportdefinities en klik op **openen**.
5.  Selecteer in het dialoogvenster Importeren de te importeren rapportdefinities:
    -   Als u alle rapportdefinities en de ondersteunende bouwstenen wilt importeren, klikt u op **Alles selecteren**.
    -   Om specifieke rapporten, rijen, kolommen, structuren of dimensiesets te importeren, selecteert u de te importeren rapporten, rijen, kolommen, structuren of dimensiesets.

6.  Click **Import**.



