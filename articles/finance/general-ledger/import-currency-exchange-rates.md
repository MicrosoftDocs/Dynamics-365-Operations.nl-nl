---
title: Valutawisselkoersen importeren
description: Dit onderwerp bevat informatie over de vereisten voor het importeren van deviezenreferentiekoersen die zijn gepubliceerd door wisselkoersproviders.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 74acfab28d45fc75c4ecd595aeba1fb1e13bbcff
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442045"
---
# <a name="import-currency-exchange-rates"></a>Valutawisselkoersen importeren

[!include [banner](../includes/banner.md)]

Als een rechtspersoon facturen in vreemde valuta's heeft ontvangen, moet de vreemde valuta in de lokale valuta worden omgerekend. Dit betekent dat de actuele wisselkoersen voor verschillende valuta's vereist zijn. Dit onderwerp biedt een overzicht van de instellingen en verwerking die zijn vereist voor het importeren van deviezenreferentiekoersen die zijn gepubliceerd door wisselkoersproviders, zoals de Europese Centrale Bank en de Centrale Bank van Rusland.

In de volgende gedeelten wordt de stroom informatie beschreven die wordt gebruikt voor het instellen en verwerken van de import van wisselkoersen in vreemde valuta.

## <a name="configure-an-exchange-rate-provider"></a>Een wisselkoersprovider configureren
Voordat u wisselkoersen kunt importeren, moet u de informatie instellen die wordt vereist door de providers die de wisselkoersen aanbieden. Gebruik de pagina **Wisselkoersproviders configureren** om de wisselkoersproviders te selecteren. Sommige wisselkoersproviders zijn opgenomen in de demonstratiegegevens in Dynamics 365 Finance. De volgende tabel bevat omschrijvingen voor de besturingselementen op deze pagina.

|           |                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Veld** | **Omschrijving**                                                                                                                                                                                                             |
| **Naam**  | De naam van de wisselkoersprovider.                                                                                                                                                                                     |
| **Sleutel**   | De unieke id voor alle configuratie-informatie die de provider vereist. Deze informatie wordt automatisch toegevoegd voor elke wisselkoersprovider die u toevoegt. |
| **Value** | Informatie voor elke sleutel. Deze informatie wordt toegevoegd voor elke wisselkoersprovider die u toevoegt.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Valutawisselkoersen importeren
U kunt wisselkoersen importeren vanuit de bron van wisselkoersproviders en ze toevoegen op de pagina **Valutawisselkoersen**. Gebruik de pagina **Valutawisselkoersen importeren** om de wisselkoersen te importeren. De volgende tabel bevat omschrijvingen van de velden die nodig zijn om het importproces met succes te voltooien.

|                                        |                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Veld**                              | **Omschrijving**                                                                                                                                                                                                                                                                                                                                                             |
| **Wisselkoerstype**                 | Een wisselkoerstype.                                                                                                                                                                                                                                                                                                                                                      |
| **Wisselkoersprovider**             | Een wisselkoersprovider.                                                                                                                                                                                                                                                                                                                                                  |
| **Importeren vanaf**                       | Met deze parameter wordt bepaald of vanaf de huidige datum of voor een specifiek datumbereik wordt geïmporteerd. Voer begin- en einddatums in of selecteer deze, als u een datumbereik wilt gebruiken.                                                                                                                                                                                                                |
| **Benodigde valutaparen maken**    | Met dit selectievakje wordt het automatisch maken van valutaparen beheerd, als de valutaparen die worden geïmporteerd, niet aanwezig zijn. Deze optie is mogelijk niet beschikbaar voor sommige providers.                                                                                                                                                                                               |
| **Bestaande wisselkoersen overschrijven**   | Met dit selectievakje wordt het bijwerken van de bestaande wisselkoers voor een valutapaar beheerd als de wisselkoers voor een bepaalde datum al bestaat. Als u dit selectievakje niet inschakelt, wordt de wisselkoers voor de specifieke datums niet geïmporteerd als er al een andere wisselkoers bestaat.                                                                                       |
| **Importeren op nationale feestdag voorkomen** | Met dit selectievakje wordt de import van de wisselkoers beheerd voor een datum die een feestdag betreft. Bijvoorbeeld: als u dit selectievakje inschakelt en de Europese Centrale Bank als de wisselkoersprovider gebruikt, wordt de wisselkoers op een feestdag die is gerelateerd aan de huidige rechtspersoon niet bijgewerkt. Deze optie is mogelijk niet beschikbaar voor sommige providers. |
| **Koers van de vorige dag** | Dit selectievakje is beschikbaar als u de functie **ECB-import op de huidige of vorige datum** inschakelt op de pagina **Functiebeheer**. Dit selectievakje is alleen beschikbaar voor de provider, *Europese Centrale Bank*. Schakel dit selectievakje in om de valutawisselkoers te importeren die door de Europese Centrale Bank op de vorige werkdag om ongeveer 16:00 CET is gepubliceerd. Het selectievakje is standaard ingeschakeld. Schakel dit selectievakje uit als u de valutawisselkoers wilt importeren die op dezelfde werkdag is gepubliceerd.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]