---
title: Standaardomschrijvingen voor het grootboek
description: Standaardomschrijvingen kunnen worden gebruikt om het veld Omschrijving bij te werken in boekstukboekingen naar het grootboek.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: d5a38af57d614ae2c93b0af74ec4a1c085519d46
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841886"
---
# <a name="default-descriptions-for-the-general-ledger"></a>Standaardomschrijvingen voor het grootboek

[!include [banner](../../includes/banner.md)]

Standaardomschrijvingen kunnen worden gebruikt om het veld **Omschrijving** bij te werken in boekstukboekingen naar het grootboek. Deze functionaliteit is verbeterd om te werken met Francoprijzen.

Als u standaardomschrijvingen voor boekingen in het grootboek wilt instellen, gaat u naar **Organisatiebeheer \> Instellen \> Standaardomschrijvingen**.

In de volgende tabel worden de nieuwe waarden weergegeven die zijn toegevoegd aan het veld **Omschrijving** op de pagina **Standaardomschrijvingen** ter ondersteuning van de francoprijzen.

| Type omschrijving | Opmerkingen |
|---|---|
| Kostprijsberekening bij import - Kostentoerekening | Wanneer een inkooporderfactuur wordt geboekt, wordt een kostentoerekening verwerkt voor ramingskosten. Er kunnen standaardomschrijvingen worden opgegeven om het trajectnummer toe te voegen aan de omschrijving. Gebruik *%4* voor het zendingsnummer. |
| Kostprijsberekening bij import - Order voor goederen in transit | Als u verwerking in transit gebruikt, wordt de inkooporderfactuur geboekt en worden de goederen geboekt naar een rekening voor goederen in transit. Er kunnen standaardomschrijvingen worden opgegeven om het ordernummer in transit toe te voegen aan de omschrijving. Gebruik *%4* voor het ordernummer in transit. |
| Voorraad - afsluiten - correctie | Wanneer de factuur voor de leveranciers wordt verwerkt voor trajectkosten, wordt een voorraadcorrectie verwerkt om trajectkosten te ramen. Er kunnen standaardomschrijvingen worden opgegeven om het trajectnummer toe te voegen aan de omschrijving. Gebruik *%4* voor het zendingsnummer. |

Zie [Standaardomschrijvingen voor automatische boeking instellen](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md) voor meer informatie over het werken met de pagina **Standaardomschrijvingen**.
