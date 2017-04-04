---
title: Importeren of handmatig postcodes maken
description: In dit artikel wordt uitgelegd hoe importeren en handmatig postcodes maken in de juiste indeling. In dit onderwerp bevat informatie over de functie die is toegevoegd voor Microsoft Dynamics 365 voor bewerkingen.
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LogisticsAddressSetup
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 29901
ms.assetid: 0c9cbc5f-88ae-4ed2-8331-13ecea029f79
ms.search.region: Belgium, Netherlands, Sweden
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: 700a4aec4d89fc9e99e9570c409a7a9b3a6be2c5
ms.lasthandoff: 03/31/2017


---

# <a name="import-or-manually-create-postal-codes"></a>Importeren of handmatig postcodes maken

In dit artikel wordt uitgelegd hoe importeren en handmatig postcodes maken in de juiste indeling. In dit onderwerp bevat informatie over de functie die is toegevoegd voor Microsoft Dynamics 365 voor bewerkingen. 

Het importproces kunt u de postcodes voor een specifiek land/regio bijwerken. U kunt postcodes ook handmatig maken.

## <a name="import-zippostal-codes"></a>Postcodes importeren
U kunt de **importeren postcodes** pagina nieuwe postcodes importeren in Microsoft Dynamics 365 voor bewerkingen. Wanneer u de codes importeert, wordt de bestaande postcodes worden vervangen door de nieuwe indeling en eventuele nieuwe codes toegevoegd.

Voor sommige landen, moet u de Data management framework gebruiken om codes te importeren, terwijl voor andere landen alleen een uploadbestand vereist is. België, Nederland en Zweden moeten een bestand te uploaden.

> [!NOTE]
> -   Voor België geeft de officiële webpagina vanuit de Belgische bericht een officiële lijst van de postcodes en de bijbehorende plaatsnamen. HTML-bestandsindeling biedt ondersteuning voor het importeren.
> -   Voor Nederland kunt een derde partij-indeling u het bestand met postcodes. Nadat het importeren is voltooid, worden alle postcodes in de notatie (NNNN AA).
> -   Voor Zweden Postnummerservice.se biedt twee typen bestanden: Zweedse postcodes en Zweedse adressen. De import ondersteunt de bestandsindeling voor beide typen.


## <a name="create-zippostal-codes-manually"></a>Handmatig postcodes maken
In plaats van de codes importeert, kunt u de **adresinstelling** pagina handmatig toevoegen van nieuwe postcodes.

