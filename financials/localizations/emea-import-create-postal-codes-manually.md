---
title: Postcodes importeren of handmatig maken
description: In dit artikel wordt beschreven hoe u postcodes in de juiste indeling kunt importeren en handmatig maken. Dit onderwerp bevat informatie over de functie die is toegevoegd of gewijzigd voor Microsoft Dynamics 365 for Operations.
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 34ad4a2de437eac6508a7cd7525add11878fcf33
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2017


---

# <a name="import-or-manually-create-postal-codes"></a>Postcodes importeren of handmatig maken

[!include[banner](../includes/banner.md)]


In dit artikel wordt beschreven hoe u postcodes in de juiste indeling kunt importeren en handmatig maken. Dit onderwerp bevat informatie over de functie die is toegevoegd of gewijzigd voor Microsoft Dynamics 365 for Operations. 

Met het importproces kunt u de postcodes voor een bepaald land of een bepaalde regio bijwerken. U kunt postcodes ook handmatig maken.

## <a name="import-zippostal-codes"></a>Postcodes importeren
U kunt de pagina **Postcodes importeren** gebruiken om nieuwe postcodes in Microsoft Dynamics 365 for Operations te importeren. Wanneer u de codes importeert, worden de bestaande postcodes door de nieuwe indeling vervangen en worden eventuele nieuwe codes toegevoegd.

Voor sommige landen moet u het Gegevensbeheer-raamwerk gebruiken om codes te importeren, terwijl voor andere landen alleen een uploadbestand vereist is. Voor België, Nederland en Zweden moet een bestand worden geüpload.

> [!NOTE]
> -   Voor België bevat de officiële webpagina van de Belgische Post een officiële lijst van de postcodes en de bijbehorende plaatsnamen. HTML-bestandsindeling wordt ondersteund voor het importeren.
> -   Voor Nederland levert een externe organisatie het bestand dat postcodes bevat. Nadat de import is voltooid, worden alle postcodes in de indeling (NNNN AA) weergegeven.
> -   Voor Zweden biedt Postnummerservice.se twee typen bestanden: Zweedse postcodes en Zweedse adressen. Tekstbestandsindeling wordt voor beide typen ondersteund voor het importeren.


## <a name="create-zippostal-codes-manually"></a>Handmatig postcodes maken
In plaats van codes te importeren kunt u de pagina **Adresinstelling** gebruiken om handmatig nieuwe postcodes toe te voegen.



