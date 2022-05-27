---
title: Financiële dimensies definiëren
description: Deze procedure toont hoe u een door een entiteit ondersteunde financiële dimensie en een aangepaste financiële dimensie toevoegt.
author: aprilolson
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10a991938f68c0ade19999e48a02f032c92a6779
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/05/2022
ms.locfileid: "8716938"
---
# <a name="define-financial-dimensions"></a>Financiële dimensies definiëren

[!include [banner](../../includes/banner.md)]

Deze procedure toont hoe u een door een entiteit ondersteunde financiële dimensie en een aangepaste financiële dimensie toevoegt. De taakbegeleiding gebruikt het demobedrijf USMF.

## <a name="create-an-entity-backed-financial-dimension"></a>Een door een entiteit ondersteunde financiële dimensie maken
1. Ga naar **Navigatievenster > Modules > Grootboek > Rekeningschema > Dimensies > Financiële dimensies**.
2. Klik op **Nieuw**.
3. Selecteer in het formulierveld **Gebruikerswaarden** een door het systeem gedefinieerde entiteit waarop de financiële dimensie moet worden gebaseerd. 
4. Typ in het veld **Dimensienaam** een waarde om de financiële dimensie te beschrijven. De naam kan anders zijn dan de door het systeem gedefinieerde entiteit maar kan geen spaties of speciale tekens bevatten.
5. Klik op **Activeren**. Bij het activeren van de financiële dimensie wordt de tabel met de financiële dimensienaam bijgewerkt en worden verwijderde dimensies gewist. U kunt dimensiewaarden invoeren voordat u een financiële dimensie activeert, maar u kunt een financiële dimensie niet gebruiken voordat deze is geactiveerd.  
6. Klik in het activeringbericht op **Sluiten**.
7. Klik op **Activeren**. U kunt de activering van een dimensie inplannen om op een specifieke datum en tijd in batch te worden uitgevoerd.  
8. Klik in het **actievenster** op **Dimensiewaarden**. Sommige dimensiewaarden zijn bedrijfsspecifiek. U kunt controleren of deze bedrijfsspecifiek zijn: als de bedrijfsnaam in de lijst van dimensiewaarden wordt weergeven.  

## <a name="create-a-custom-financial-dimension"></a>Een aangepaste financiële dimensie maken
1. Klik op **Nieuw**.
2. Selecteer **Aangepaste dimensie** in het veld **Waarden gebruiken van**.
3. Typ in het veld **Dimensienaam** een waarde om de financiële dimensie te beschrijven.
    - De naam mag geen spaties of speciale tekens bevatten.  
    - U kunt ook een opmaakmasker opgeven om de hoeveelheid en het type gegevens te beperken die u voor dimensiewaarden kunt invoeren.   
    - U kunt tekens zoals letters of een koppelteken invoeren die voor elke dimensiewaarde hetzelfde blijven. U kunt hekjes (#) en invoeren, evenals en-tekens (&) die dienen als tijdelijke aanduidingen voor letters en cijfers die elke keer worden gewijzigd als een dimensiewaarde wordt gemaakt. Gebruik een hekje (#) als tijdelijke aanduiding voor een cijfer en een en-teken (&) als tijdelijke aanduiding voor een letter.  Voorbeeld: om de waarde van de letters tot CC en drie nummers te beperken, voert u CC-### als opmaakmasker in.  
4. Klik op **Activeren**. Bij het activeren van de financiële dimensie wordt de tabel met de financiële dimensienaam bijgewerkt en worden verwijderde dimensies gewist. U kunt dimensiewaarden invoeren voordat u een financiële dimensie activeert, maar u kunt een financiële dimensie niet gebruiken voordat deze is geactiveerd.     
5. Klik op **Activeren**. U kunt de activering van een dimensie inplannen om op een specifieke datum en tijd in batch te worden uitgevoerd.      
6. Klik in het **actievenster** op **Dimensiewaarden**.
7. Klik op **Nieuw**.
8. Typ in het veld **Dimensiewaarde** een naam om uw waarde van financiële dimensie te beschrijven.
9. Typ in het veld **Beschrijving** een beschrijving die uw waarde van financiële dimensie beschrijft.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
