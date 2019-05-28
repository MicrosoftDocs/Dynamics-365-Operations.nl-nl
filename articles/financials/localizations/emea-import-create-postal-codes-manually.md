---
title: Postcodes importeren of handmatig maken
description: In dit onderwerp wordt beschreven hoe u postcodes in de juiste indeling importeert en handmatig maakt. Dit onderwerp omvat informatie over de functie die is toegevoegd voor Microsoft Dynamics 365 for Finance and Operations.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 10/31/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LogisticsAddressSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 29901
ms.search.region: Belgium, Netherlands, Sweden
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3a17deced4895c198f5649b4edb341d8c1b8ed88
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1538208"
---
# <a name="import-or-manually-create-postal-codes"></a>Postcodes importeren of handmatig maken

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u postcodes in de juiste indeling importeert en handmatig maakt. Dit onderwerp omvat informatie over de functie die is toegevoegd voor Microsoft Dynamics 365 for Finance and Operations. 

Met het importproces kunt u de postcodes voor een bepaald land of een bepaalde regio bijwerken. U kunt postcodes ook handmatig maken.

## <a name="import-zippostal-codes"></a>Postcodes importeren
U kunt de pagina **Postcodes importeren** gebruiken om nieuwe postcodes in Finance and Operations te importeren. Wanneer u de codes importeert, worden de bestaande postcodes door de nieuwe indeling vervangen en worden eventuele nieuwe codes toegevoegd.

Voor sommige landen moet u het Gegevensbeheer-raamwerk gebruiken om codes te importeren, terwijl voor andere landen alleen een uploadbestand vereist is. Voor België, Nederland en Zweden moet een bestand worden geüpload.

> [!NOTE]
> -   Voor België bevat de officiële webpagina van de Belgische Post een officiële lijst van de postcodes en de bijbehorende plaatsnamen. HTML-bestandsindeling wordt ondersteund voor het importeren.
> -   Voor Nederland levert een externe organisatie het bestand dat postcodes bevat. Nadat de import is voltooid, worden alle postcodes in de indeling (NNNN AA) weergegeven.
> -   Voor Zweden biedt Postnummerservice.se twee typen bestanden: Zweedse postcodes en Zweedse adressen. Tekstbestandsindeling wordt voor beide typen ondersteund voor het importeren.


## <a name="create-zippostal-codes-manually"></a>Handmatig postcodes maken
In plaats van codes te importeren kunt u de pagina **Adresinstelling** gebruiken om handmatig nieuwe postcodes toe te voegen.


