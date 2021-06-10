---
title: Sjablonen voor financiële journalen openen in Office
description: In dit onderwerp worden problemen beschreven die kunnen optreden wanneer u aangepaste financiële journalen maakt met behulp van een Microsoft Excel-sjabloon.
author: kweekley
ms.date: 05/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0773f47551b2460ec310b92b67c634b433147749
ms.sourcegitcommit: 8c5b3e872825953853ad57fc67ba6e5ae92b9afe
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/24/2021
ms.locfileid: "6089452"
---
# <a name="open-financial-journal-templates-in-office"></a>Sjablonen voor financiële journalen openen in Office

[!include [banner](../includes/banner.md)]

In dit onderwerp worden problemen beschreven die kunnen optreden wanneer u aangepaste financiële journalen maakt met behulp van een Microsoft Excel-sjabloon.

## <a name="symptom"></a>Symptoom

U hebt een aangepaste Excel-sjabloon voor financiële journalen gemaakt, maar deze sjabloon wordt niet weergegeven in het menu **Regels openen in Excel**. Anders wordt de sjabloon wel in het menu weergegeven, maar wordt er een andere sjabloon geopend wanneer u deze selecteert.

## <a name="resolution"></a>Oplossing

De standaardfunctionaliteit Openen in Excel gebruikt de hoofdgegevensbron (tabel) van de huidige pagina om te bepalen welke Office-sjablonen of gegevensentiteiten als opties worden weergegeven in het menu **Openen in Excel**. Dit gedrag is niet de ideale ervaring voor financiële journalen, omdat financiële journalen dezelfde tabellen (LedgerJournalTable en LedgerJournalTrans) gebruiken als de hoofdgegevensbron van veel andere journaaltypen.

Voor financiële journalen is de functie Regels openen in Excel bedoeld om sjablonen weer te geven die zijn ontworpen voor het journaal in de context waarvan u momenteel werkt, zoals het algemene journaal of een betalingsjournaal. Een sjabloon die moet worden gebruikt met een leverancierbetalingsjournaal wordt bijvoorbeeld zodanig ontworpen dat uw primaire rekening wordt afgedwongen als leverancierrekening.

Als u het niveau wilt verhogen van een sjabloon zodat deze beschikbaar is in de menu's **Regels openen in Excel** en **Openen in Excel**, is het voor ontwikkelaars eenvoudig om de interface **LedgerIJournalExcelTemplate** te implementeren en de klasse **DocuTemplateRegistrationBase** uit te breiden. Er zijn vele voorbeelden van deze benadering in het systeem geïmplementeerd. Een voorbeeld dat ter referentie kan worden gebruikt, is de interface **LedgerDailyJournalExcelTemplate** die voor het algemene journaal (of dagelijks journaal) is gemaakt.

Wanneer de interface **LedgerIJournalExcelTemplate** is geïmplementeerd voor uw sjabloon, worden in het menu **Regels openen in Excel** sjablonen gefilterd op het journaaltype van uw journaal. Met deze interface worden alleen de sjablonen weergegeven die beschikbaar zijn voor dat journaal. De interface biedt ook een validatiemethode die ervoor zorgt dat een sjabloon niet kan worden geopend voor een journaal als deze niet aan de vereisten van het rekeningtype voldoet. U kunt bijvoorbeeld opgeven dat het rekeningtype van het type **Leverancier** of **Grootboek** moet zijn.

Zie [Sjablonen toevoegen aan het menu Regels openen in Excel](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md) voor meer informatie over deze functionaliteit.
