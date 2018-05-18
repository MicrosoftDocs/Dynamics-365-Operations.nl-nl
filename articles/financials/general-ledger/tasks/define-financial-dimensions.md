--- 
title: "Financiële dimensies definiëren"
description: "Deze taakhandleiding toont het toevoegen van een door een entiteit ondersteunde financiële dimensie en een aangepaste financiële dimensie."
author: aprilolson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0b72acf763f0f6dbc64c3e00986bc9eb0e366bb5
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="define-financial-dimensions"></a>Financiële dimensies definiëren

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze taakhandleiding toont het toevoegen van een door een entiteit ondersteunde financiële dimensie en een aangepaste financiële dimensie.  De taakbegeleiding gebruikt het demobedrijf USMF.


## <a name="create-an-entity-backed-financial-dimension"></a>Een door een entiteit ondersteunde financiële dimensie maken
1. Ga naar Grootboek > Rekeningschema > Dimenies > Financiële dimensies.
2. Klik op Nieuw.
3. Selecteer in het veld Gebruikerswaarden van een door het systeem gedefinieerde entiteit waarop de financiële dimensie moet worden gebaseerd. 
4. Typ in het veld Dimensienaam een waarde om de financiële dimensie te beschrijven.
    * De naam kan anders zijn dan de door het systeem gedefinieerde entiteit maar kan geen spaties of speciale tekens bevatten.  
5. Klik op Activeren.
    * Bij het activeren van de financiële dimensie wordt de tabel met de financiële dimensienaam bijgewerkt en worden verwijderde dimensies gewist. U kunt dimensiewaarden invoeren voordat u een financiële dimensie activeert, maar u kunt een financiële dimensie niet gebruiken voordat deze is geactiveerd.  
6. Klik in het activeringbericht op Sluiten.
7. Klik op Activeren.
    * U kunt de activering van een dimensie inplannen om op een specifieke datum en tijd in batch te worden uitgevoerd.  
8. Klik op Dimensiewaarden.
    * Sommige dimensiewaarden zijn bedrijfsspecifiek. U kunt controleren of deze bedrijfsspecifiek zijn: als de bedrijfsnaam in de lijst van dimensiewaarden wordt weergeven.  

## <a name="create-a-custom-financial-dimension"></a>Een aangepaste financiële dimensie maken
1. Sluit de pagina.
2. Klik op Nieuw.
3. Selecteer <Custom dimension> in het veld Waarden gebruiken van.
4. Typ in het veld Dimensienaam een waarde om de financiële dimensie te beschrijven.
    * De naam mag geen spaties of speciale tekens bevatten.  
    * U kunt ook een opmaakmasker opgeven om de hoeveelheid en het type gegevens te beperken die u voor dimensiewaarden kunt invoeren.   
    * U kunt tekens zoals letters of een koppelteken invoeren die voor elke dimensiewaarde hetzelfde blijven. U kunt hekjes (#) en invoeren, evenals en-tekens (&) die dienen als tijdelijke aanduidingen voor letters en cijfers die elke keer worden gewijzigd als een dimensiewaarde wordt gemaakt. Gebruik een hekje (#) als tijdelijke aanduiding voor een cijfer en een en-teken (&) als tijdelijke aanduiding voor een letter.  Voorbeeld: om de waarde van de letters tot CC en drie nummers te beperken, voert u CC-### als opmaakmasker in.  
5. Klik op Activeren.
    * Bij het activeren van de financiële dimensie wordt de tabel met de financiële dimensienaam bijgewerkt en worden verwijderde dimensies gewist. U kunt dimensiewaarden invoeren voordat u een financiële dimensie activeert, maar u kunt een financiële dimensie niet gebruiken voordat deze is geactiveerd.  
6. Klik op Activeren.
    * U kunt de activering van een dimensie inplannen om op een specifieke datum en tijd in batch te worden uitgevoerd.  
7. Klik op Dimensiewaarden.
8. Klik op Nieuw.
9. Typ in het veld Dimensiewaarde een naam om uw waarde van financiële dimensie te beschrijven.
10. Typ in het veld Beschrijving een beschrijving die uw waarde van financiële dimensie beschrijft.


