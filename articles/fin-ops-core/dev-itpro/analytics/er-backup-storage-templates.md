---
title: Back-upopslag van ER-sjablonen
description: In dit onderwerp wordt uitgelegd hoe u de back-upopslag voor elektronische rapportage (ER) gebruikt voor het herstellen van sjablonen.
author: NickSelin
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-08-13
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 305576b79fdb11f29de9207662de0fe4b4dd6eb5
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6351837"
---
# <a name="backup-storage-of-er-templates"></a>Back-upopslag van ER-sjablonen

[!include [banner](../includes/banner.md)]

Zakelijke gebruikers gebruiken het [overzicht van elektronische rapportage (ER)](general-electronic-reporting.md) om indelingen voor uitgaande documenten te configureren in overeenstemming met de wettelijke voorschriften van verschillende landen/regio's. Er kunnen voor geconfigureerde ER-indelingen vooraf gedefinieerde sjablonen worden gebruikt voor het genereren van uitgaande documenten in verschillende indelingen, zoals Microsoft Excel-werkmappen, Microsoft Word-documenten of PDF-documenten. De sjablonen zijn gevuld met gegevens die voor de geconfigureerde gegevensstroom voor gegenereerde documenten nodig zijn.

Elke geconfigureerde indeling kan als onderdeel van een ER-oplossing worden gepubliceerd. Elke ER-oplossing kan vanuit één exemplaar van Finance and Operations worden geëxporteerd en in een ander exemplaar worden geïmporteerd.

Het ER-raamwerk gebruikt [Documentbeheer configureren](../../fin-ops/organization-administration/configure-document-management.md) om de vereiste sjablonen te bewaren voor het huidige exemplaar van Finance and Operations. Afhankelijk van de instellingen van het ER-raamwerk kan Microsoft Azure-blobopslag of een Microsoft SharePoint-map worden geselecteerd als de fysieke primaire opslaglocatie voor sjablonen. (Zie [Raamwerk elektronische rapportage (ER) configureren](electronic-reporting-er-configure-parameters.md) voor meer informatie.) De tabel DocuValue bevat een afzonderlijke record voor elke sjabloon. In elke record bevat het veld **AccessInformation** het pad van een sjabloonbestand dat zich in de geconfigureerde opslaglocatie bevindt.

Wanneer u Finance and Operations-exemplaren beheert, kunt u besluiten uw het huidige exemplaar naar een andere locatie te migreren. U kunt bijvoorbeeld uw productie-exemplaar migreren naar een nieuwe sandbox-omgeving. Als u het ER-raamwerk voor het opslaan van sjablonen in de blobopslag hebt geconfigureerd, verwijst de tabel DocuValue in de nieuwe sandbox-omgeving naar het blobopslag-exemplaar in de productieomgeving. Dit exemplaar kan echter niet worden geopend vanuit de sandbox-omgeving omdat het migratieproces de migratie van artefacten in de blobopslag niet ondersteunt. Daarom wordt er een uitzondering gemaakt wanneer u een ER-indeling probeert uit te voeren die een sjabloon gebruikt om bedrijfsdocumenten te genereren, en ziet u een waarschuwing over de ontbrekende sjabloon. U kunt ook het ER-hulpprogramma voor opschonen gebruiken om de ER-indelingsconfiguratie met de sjabloon te verwijderen en vervolgens opnieuw te importeren. Omdat u mogelijk verschillende ER-indelingsconfiguraties hebt, kan dit proces veel tijd in beslag nemen.

Met de functie Back-upopslag van ER-sjablonen kunt u sjablonen maken zodat deze altijd beschikbaar zijn voor het genereren van bedrijfsdocumenten.

> [!NOTE]
> Deze functie kan alleen worden gebruikt wanneer blobopslag is geselecteerd als de fysieke opslaglocatie voor de ER-sjablonen.

## <a name="automated-recovery-and-notification"></a>Automatisch herstel en kennisgeving

Voor deze functie wordt elke sjabloon van een nieuwe ER-indelingsconfiguratie in de huidige omgeving automatisch opgeslagen op de back-upopslaglocatie voor sjablonen (de ERDocuDatabaseStorage-databasetabel) wanneer de volgende gebeurtenissen optreden:

- U importeert een nieuwe ER-indelingsconfiguratie die een sjabloon bevat.
- U voltooit de conceptversie van een ER-indelingsconfiguratie die een sjabloon bevat.

Back-upkopieën van sjablonen worden gemigreerd naar een nieuw exemplaar van Finance and Operations als onderdeel van de toepassingsdatabase.

Als er een sjabloon met een ER-indeling nodig is voor het genereren van uitgaande documenten, voor het verwerken van leveranciersbetalingen, waaronder het genereren van betalingsadvies en controlerapporten, maar de vereiste sjabloon niet is gevonden op de primaire opslaglocatie, vinden de volgende gebeurtenissen plaats:

- Als de sjabloon beschikbaar is op de back-upopslaglocatie, wordt deze automatisch overgenomen van de back-upopslaglocatie, teruggezet naar de primaire opslaglocatie en gebruikt voor de huidige uitvoering.
- Elke gebruiker die aan de rol **Ontwikkelaar elektronische rapportage** of **Systeembeheerder** is toegewezen, wordt op de hoogte gesteld van de ontbrekende sjabloon via het actiecentrum. Welk bericht wordt weergegeven, is afhankelijk van de waarde van de parameter **Automatisch de procedure uitvoeren voor het in batch herstellen van de gebroken sjablonen**:

    - Als deze parameter is ingesteld **UIT**, kunt u het batchproces starten om automatisch vergelijkbare problemen op te lossen voor andere sjablonen met een ER-indelingsconfiguratie. Het bericht bevat een koppeling die u kunt gebruiken om het batchproces te starten.
    - Als deze parameter is ingesteld op **Aan**, verschijnt het bericht dat er een probleem met ontbrekende sjablonen is ontdekt en dat het nieuwe batchproces **Verbroken sjablonen terugzetten uit interne databaseback-up** automatisch is geprogrammeerd. Met dit batchproces worden vergelijkbare problemen met andere sjablonen automatisch opgelost.

Als u de parameter **Automatisch de procedure uitvoeren voor het in batch herstellen van de gebroken sjablonen** wilt instellen, voert u de volgende stappen uit:

1. Open in Finance and Operations de pagina **Organisatiebeheer \> Elektronische rapportage \> Configuraties**.
2. Selecteer op de pagina **Configuraties** in het actievenster op het tabblad **Configuraties** in de groep **Geavanceerde instellingen** de optie **Gebruikersparameters**.
3. Stel in het dialoogvenster **Gebruikersparameters** de vereiste waarde in voor de parameter **Automatisch de procedure uitvoeren voor het in batch herstellen van de gebroken sjablonen**.

> [!NOTE]
> Deze parameter is gedefinieerd voor de toepassingsgebruiker en geldt specifiek voor het aangemelde bedrijf.

![Pagina ER-configuraties.](./media/GER-BackupTemplates-1.png)

In de volgende afbeelding toont een voorbeeld van het bericht dat wordt weergegeven wanneer de parameter **Automatisch de procedure uitvoeren voor het in batch herstellen van de gebroken sjablonen** is ingesteld op **Aan**.

![Pagina Journaal met betalingen van leverancier.](./media/GER-BackupTemplates-2.png)

In de volgende afbeelding ziet u het batchproces **Verbroken sjablonen terugzetten uit interne databaseback-up** op de pagina **Batchtaak**.

![Pagina Batchtaak.](./media/GER-BackupTemplates-3.png)

Het uitvoeringslogboek van het voltooide batchproces **Verbroken sjablonen terugzetten uit interne databaseback-up** bevat informatie over de sjablonen die zijn hersteld uit de back-upopslaglocatie naar de primaire opslaglocatie.

![Pagina Batchtaakhistorie.](./media/GER-BackupTemplates-4.png)

Het proces van het automatisch maken van back-ups van sjablonen in de ER-indelingsconfiguraties is standaard ingeschakeld. Als u wilt stoppen met het maken van back-ups van sjablonen, stelt u de optie **Stoppen met het maken van back-upkopieën van sjablonen** in op **Ja** op het tabblad **Bijlagen** van de pagina **Parameters van elektronische rapportage**. U kunt deze pagina openen via het werkgebied **Elektronische rapportage**.

Als u de optie **Stoppen met het maken van back-upkopieën van sjablonen** hebt ingesteld op **Ja** en u de back-ups die eerder van de sjablonen zijn gemaakt niet wilt bewaren, selecteert u **Back-upopslag opschonen** op de pagina **Parameters van elektronische rapportage**.

Als u uw omgeving hebt opgewaardeerd naar Finance and Operations, versie 10.0.5 (oktober 2019) en u wilt migreren naar een nieuwe omgeving waarin de ER-indelingsconfiguraties zijn opgenomen die kunnen worden uitgevoerd, selecteert u **Back-upopslag invullen** op de pagina **Parameters van elektronische rapportage** voordat de migratie plaatsvindt. Met deze knop start u het proces van het maken van back-ups van alle beschikbare sjablonen, zodat deze kunnen worden opgeslagen op de ER-opslaglocatie voor back-ups van sjablonen.

![Pagina Parameters van elektronische rapportage.](./media/GER-BackupTemplates-5.png)

## <a name="manual-recovery"></a>Handmatig herstel

Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Beschadigde sjablonen herstellen** om handmatig het herstelproces van ER-sjablonen te starten vanuit de opslaglocatie voor back-ups naar de primaire opslaglocatie. Voordat u dit proces start, kunt u op de pagina **Beschadigde sjablonen herstellen** opgeven of dit interactief moet worden uitgevoerd of dat het batchproces hiervoor wordt gepland.

## <a name="supported-deployments"></a>Ondersteunde implementaties

In Finance and Operations versie 10.0.5 is de functie Back-upopslag van ER-sjablonen alleen beschikbaar in cloudimplementaties.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van elektronische rapportage (ER)](general-electronic-reporting.md)

[Raamwerk elektronische rapportage (ER) configureren](electronic-reporting-er-configure-parameters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]