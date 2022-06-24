---
title: Standaardomschrijvingen voor het grootboek
description: Standaardomschrijvingen kunnen worden gebruikt om het veld Omschrijving bij te werken in boekstukboekingen naar het grootboek.
author: Weijiesa
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 7020c39dd599be047e07caa391d6d4c69c426328
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889543"
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
