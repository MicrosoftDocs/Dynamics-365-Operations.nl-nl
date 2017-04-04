---
title: Valutawisselkoersen importeren
description: Als een rechtspersoon heeft ontvangen van facturen in vreemde valuta&quot;s, is het nodig zijn om te zetten van de vreemde valuta in de lokale valuta. Dit betekent dat de actuele wisselkoersen voor verschillende valuta&quot;s vereist zijn. Dit onderwerp biedt een overzicht van de vereiste instellingen en verwerking voor het importeren van verwijzing wisselkoersen gepubliceerd via Internet door de wisselkoers leveranciers, zoals de europese Centrale Bank en de Centrale Bank van Rusland.
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: bf66a1b1c9314b454223274810a21913d54b702d
ms.lasthandoff: 03/31/2017


---

# <a name="import-currency-exchange-rates"></a>Valutawisselkoersen importeren

Als een rechtspersoon heeft ontvangen van facturen in vreemde valuta's, is het nodig zijn om te zetten van de vreemde valuta in de lokale valuta. Dit betekent dat de actuele wisselkoersen voor verschillende valuta's vereist zijn. Dit onderwerp biedt een overzicht van de vereiste instellingen en verwerking voor het importeren van verwijzing wisselkoersen gepubliceerd via Internet door de wisselkoers leveranciers, zoals de europese Centrale Bank en de Centrale Bank van Rusland.

De volgende secties beschrijven de informatiestroom die wordt gebruikt voor het instellen en verwerken van het importeren van wisselkoersen.

## <a name="configure-an-exchange-rate-provider"></a>Een wisselkoersprovider configureren
Voordat u wisselkoersen importeren kunt, moet u de informatie die wordt vereist door de leveranciers die de wisselkoersen aanbieden instellen. Gebruik de **Wisselkoersproviders configureren** pagina de Wisselkoersproviders selecteren. Sommige Wisselkoersproviders zijn opgenomen in de demonstratiegegevens in Microsoft Dynamics 365 voor bewerkingen. De volgende tabel bevat omschrijvingen voor de besturingselementen op deze pagina.

|           |                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field** | **Description**                                                                                                                                                                                                             |
| **Name**  | De naam van de wisselkoersprovider.                                                                                                                                                                                     |
| **Sleutel**   | De unieke id voor alle configuratie-informatie die de provider vereist. Deze informatie wordt automatisch toegevoegd voor elke provider wisselkoers toe te voegen wanneer u klikt op de **Add** knop. |
| **Value** | Informatie voor elke sleutel. Deze informatie wordt toegevoegd voor elke provider wisselkoers toe te voegen wanneer u klikt op de **Add** knop.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Valutawisselkoersen importeren
U kunt wisselkoersen importeren vanuit de bron wisselkoers aanbieders en ingesteld in de **Valutawisselkoersen** pagina. Gebruik de **Valutawisselkoersen importeren** pagina om de wisselkoersen te importeren. De volgende tabel bevat omschrijvingen van de velden die nodig zijn om het importproces met succes wordt voltooid.

|                                        |                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field**                              | **Description**                                                                                                                                                                                                                                                                                                                                                             |
| **Exchange rate type**                 | Een wisselkoerstype.                                                                                                                                                                                                                                                                                                                                                      |
| **Exchange rate provider**             | Een provider wisselkoers.                                                                                                                                                                                                                                                                                                                                                  |
| **Import as of**                       | Deze parameter beheert of u wilt importeren vanaf de datum van vandaag of een datumbereik. Als u gebruiken een datumbereik wilt, invoeren of selecteren van begin- en einddatum.                                                                                                                                                                                                                |
| **Create necessary currency pairs**    | Dit selectievakje beheert valutaparen, automatisch wordt gemaakt als de valutaparen die zijn geïmporteerd, niet bestaat. Deze optie is mogelijk niet beschikbaar voor sommige aanbieders.                                                                                                                                                                                               |
| **Override existing exchange rates**   | Dit selectievakje beheert het bijwerken van de bestaande wisselkoers voor een valutapaar als de wisselkoers voor een bepaalde datum al bestaat. Als u dit selectievakje niet inschakelt, wordt de wisselkoers voor de specifieke datums niet geïmporteerd als een andere wisselkoers al bestaat.                                                                                       |
| **Prevent import on national holiday** | Dit selectievakje in als beheert het importeren van de wisselkoers voor een datum die een feestdag. Bijvoorbeeld: als u dit selectievakje inschakelt en de europese Centrale Bank als de wisselkoersprovider gebruiken, het systeem wordt niet bijgewerkt de wisselkoers op een feestdag die is gerelateerd aan de huidige rechtspersoon. Deze optie is mogelijk niet beschikbaar voor sommige aanbieders. |




