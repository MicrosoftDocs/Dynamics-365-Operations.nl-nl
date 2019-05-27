---
title: Valutawisselkoersen importeren
description: Als een rechtspersoon facturen in vreemde valuta's heeft ontvangen, is het nodig de vreemde valuta in de lokale valuta om te rekenen. Dit betekent dat de actuele wisselkoersen voor verschillende valuta's vereist zijn. Dit onderwerp biedt een overzicht van de vereiste instellingen en verwerking voor het importeren van deviezenreferentiekoersen die via internet zijn gepubliceerd door de wisselkoersproviders, zoals de Europese Centrale Bank en de Centrale Bank van Rusland.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: edd72b48a640126577dd7a2add3a4891ae505fdf
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557946"
---
# <a name="import-currency-exchange-rates"></a>Valutawisselkoersen importeren

[!include [banner](../includes/banner.md)]

Als een rechtspersoon facturen in vreemde valuta's heeft ontvangen, is het nodig de vreemde valuta in de lokale valuta om te rekenen. Dit betekent dat de actuele wisselkoersen voor verschillende valuta's vereist zijn. Dit onderwerp biedt een overzicht van de vereiste instellingen en verwerking voor het importeren van deviezenreferentiekoersen die via internet zijn gepubliceerd door de wisselkoersproviders, zoals de Europese Centrale Bank en de Centrale Bank van Rusland.

In de volgende gedeelten wordt de stroom informatie beschreven die wordt gebruikt voor het instellen en verwerken van de import van wisselkoersen in vreemde valuta.

## <a name="configure-an-exchange-rate-provider"></a>Een wisselkoersprovider configureren
Voordat u wisselkoersen kunt importeren, moet u de informatie instellen die wordt vereist door de providers die de wisselkoersen aanbieden. Gebruik de pagina **Wisselkoersproviders configureren** om de wisselkoersproviders te selecteren. Sommige wisselkoersproviders zijn opgenomen in de demonstratiegegevens in Microsoft Dynamics 365 for Finance and Operations. De volgende tabel bevat omschrijvingen voor de besturingselementen op deze pagina.

|           |                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Veld** | **Omschrijving**                                                                                                                                                                                                             |
| **Naam**  | De naam van de wisselkoersprovider.                                                                                                                                                                                     |
| **Sleutel**   | De unieke id voor alle configuratie-informatie die de provider vereist. Deze informatie wordt automatisch toegevoegd voor elke wisselkoersprovider die u toevoegt wanneer u op de knop **Toevoegen** klikt. |
| **Waarde** | Informatie voor elke sleutel. Deze informatie wordt toegevoegd voor elke wisselkoersprovider die u toevoegt wanneer u op de knop **Toevoegen** klikt.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Valutawisselkoersen importeren
U kunt wisselkoersen importeren vanuit de bron van wisselkoersproviders en ze instellen op de pagina **Valutawisselkoersen**. Gebruik de pagina **Valutawisselkoersen importeren** om de wisselkoersen te importeren. De volgende tabel bevat omschrijvingen van de velden die nodig zijn om het importproces met succes te voltooien.

|                                        |                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Veld**                              | **Omschrijving**                                                                                                                                                                                                                                                                                                                                                             |
| **Wisselkoerstype**                 | Een wisselkoerstype.                                                                                                                                                                                                                                                                                                                                                      |
| **Wisselkoersprovider**             | Een wisselkoersprovider.                                                                                                                                                                                                                                                                                                                                                  |
| **Importeren vanaf**                       | Met deze parameter wordt bepaald of vanaf de datum van vandaag of voor een datumbereik wordt geïmporteerd. Voer begin- en einddatums in, of selecteer deze, als u een datumbereik wilt gebruiken.                                                                                                                                                                                                                |
| **Benodigde valutaparen maken**    | Met dit selectievakje wordt het automatisch maken van valutaparen beheerd, als de valutaparen die worden geïmporteerd, niet aanwezig zijn. Deze optie is mogelijk niet beschikbaar voor sommige providers.                                                                                                                                                                                               |
| **Bestaande wisselkoersen overschrijven**   | Met dit selectievakje wordt het bijwerken van de bestaande wisselkoers voor een valutapaar beheerd als de wisselkoers voor een bepaalde datum al bestaat. Als u dit selectievakje niet inschakelt, wordt de wisselkoers voor de specifieke datums niet geïmporteerd als er al een andere wisselkoers bestaat.                                                                                       |
| **Importeren op nationale feestdag voorkomen** | Met dit selectievakje wordt de import van de wisselkoers beheerd voor een datum die een feestdag betreft. Bijvoorbeeld: als u dit selectievakje inschakelt en de Europese Centrale Bank als de wisselkoersprovider gebruikt, wordt de wisselkoers op een feestdag die is gerelateerd aan de huidige rechtspersoon niet bijgewerkt. Deze optie is mogelijk niet beschikbaar voor sommige providers. |





