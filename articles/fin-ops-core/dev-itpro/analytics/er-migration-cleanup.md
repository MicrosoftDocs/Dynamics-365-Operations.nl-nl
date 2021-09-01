---
title: ER-migratie opschonen
description: In dit onderwerp wordt uitgelegd hoe u de opschoonfunctie voor de ER-migratie kunt gebruiken om problemen met ER-sjablonen op te lossen.
author: NickSelin
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, ERParameters, ERMigrationCleanup
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: d437bed9b9873f82bcd047e85245bd2a8c66fb3572c06660f29fc19f66aebae1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723136"
---
# <a name="er-migration-cleanup"></a>ER-migratie opschonen 

[!include[banner](../includes/banner.md)]

Wanneer u Finance-exemplaren beheert, kunt u besluiten uw het huidige exemplaar naar een andere locatie te migreren. U kunt bijvoorbeeld uw productie-exemplaar migreren naar een nieuwe sandbox-omgeving. Als u het ER-raamwerk (Electronic Reporting) voor het opslaan van sjablonen in de Microsoft Azure-blobopslag hebt geconfigureerd, verwijst de tabel **DocuValue** in de nieuwe sandbox-omgeving naar het blobopslag-exemplaar in de productieomgeving. Dit exemplaar kan echter niet worden geopend vanuit de sandbox-omgeving omdat het migratieproces de migratie van artefacten in de blobopslag niet ondersteunt. In de nieuwe sandbox-omgeving wordt echter wel verwezen naar de het blobopslagexemplaar in de sandbox-omgeving die nog niet beschikt over de ER-sjablonen.

Er wordt een uitzondering gemaakt wanneer u een ER-indeling probeert uit te voeren die een sjabloon gebruikt om bedrijfsdocumenten te genereren, en ziet u een waarschuwing over de ontbrekende sjabloon. U kunt ook de opschoonoptie voor ER-migratie gebruiken om de ER-indelingsconfiguratie met de sjabloon te verwijderen en vervolgens opnieuw te importeren.

[![Een ER-indeling uitvoeren.](./media/er-migration-cleanup-run.png)](./media/er-migration-cleanup-run.png)

U ontvangt een vergelijkbare fout als u navigeert naar de pagina **Configuraties** (**Organisatiebeheer** \> **Elektronische rapport** \> **Configuraties**) en in de configuratiestructuur een ER-indelingsconfiguratie probeert te verwijderen die gebruikmaakt van een sjabloon.

[![Een ER-indeling verwijderen.](./media/er-migration-cleanup-delete.png)](./media/er-migration-cleanup-delete.png)

Voer de volgende stappen uit om problemen op te lossen met ER-sjablonen waartoe u geen toegang hebt.

1.  Ga naar de pagina **Organisatiebeheer** \> **Periodiek** \> **Migratie opschonen**.
2.  Selecteer een ER-indelingsconfiguratie die niet kan worden uitgevoerd of verwijderd.
3.  Selecteer **Verwijderen**.
4.  Bevestig het verwijderen van de geselecteerde ER-indelingsconfiguratie.
5.  [Importeer](download-electronic-reporting-configuration-lcs.md) de verwijderde ER-indelingsconfiguratie in het huidige Finance-exemplaar.

## <a name="applicability"></a>Toepasbaarheid

> [Belangrijk] De optie **Migratie opschonen** is alleen bedoeld voor ER-indelingsconfiguraties die niet-toegankelijke ER-sjablonen bevatten. Wanneer u een ER-indelingsconfiguratie verwijdert met de optie **Migratie opschonen**, worden de sjablonen verwijderd die betrekking hebben op de configuratie-artefacten in de enige toepassingsdatabase. De aanwezigheid van de relevante fysieke bestanden in de blobopslag wordt niet gevalideerd. Hierbij wordt ervan uitgegaan dat er geen is. Gebruik daarom niet de optie **Migratie opschonen** als alternatief voor de verwijderoptie van ER-configuraties op de pagina **Configuraties**. Gebruik de optie **Migratie opschonen** alleen als de verwijderoptie van ER-configuraties op de pagina **Configuraties** mislukt.
>
> Als u de de optie **Migratie opschonen** gebruikt om een ER-indelingsconfiguratie te verwijderen wanneer de desbetreffende sjabloon aanwezig is in de blobopslag, verwijdert u alleen de configuratie-artefacten in de toepassingsdatabase. Het fysieke bestand van de sjabloon in de blobopslag blijft aanwezig. Het overschrijven van bestanden in de blobopslag is niet langer toegestaan. Zie [KB4557217](https://fix.lcs.dynamics.com/Issue/Details?kb=4557217) voor meer informatie. Bovendien kunt u de configuraties die zijn verwijderd via Migratie opschonen in deze omgeving, niet meer opnieuw importeren. U kunt dit probleem oplossen door het bijbehorende bestand te zoeken in de blobopslag en het handmatig te verwijderen.

[![Een ER-indeling importeren.](./media/er-migration-cleanup-import.png)](./media/er-migration-cleanup-import.png)

Een vergelijkbaar probleem kan optreden als u uw toepassingsexemplaar migreert naar een andere locatie die meerdere keren als migratiedoel is gebruikt en waarvoor de blobopslag al ER-sjabloonbestanden bevat.

Omdat u mogelijk verschillende ER-indelingsconfiguraties hebt, kan dit proces veel tijd in beslag nemen. Daarom verdient het gebruik van de functie [Back-up van ER-sjablonen](er-backup-storage-templates.md) voor het automatisch herstellen van sjablonen met verbroken verwijzingen de voorkeur.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]