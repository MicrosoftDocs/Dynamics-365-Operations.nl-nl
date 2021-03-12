---
title: Overzicht van positieve betalingen
description: Dit artikel bevat info over positieve betalingen die worden gebruikt om een elektronische lijst met cheques te genereren die aan de bank wordt gegeven.
author: panolte
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePaySummary
audience: Application User
ms.reviewer: roschlom
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: ffb2ded8c6f1e86657f298f3638da39ac4c63b66
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972101"
---
# <a name="positive-pay-overview"></a>Overzicht van positieve betalingen

[!include [banner](../includes/banner.md)]

Dit artikel bevat info over positieve betalingen die worden gebruikt om een elektronische lijst met cheques te genereren die aan de bank wordt gegeven. 

U kunt positieve betalingen gebruiken om een elektronische lijst met cheques te genereren die aan de bank wordt gegeven. Positieve betalingsbestanden kunnen banken helpen fraude te voorkomen. U kunt positief betalen gebruiken om een elektronische lijst met cheques te genereren telkens als cheques worden afgedrukt. Wanneer een cheque aan de bank wordt voorgelegd, vergelijkt de bank de cheques met een lijst van cheques die eerder werden ingediend. Als de cheque overeenkomt met wat de bank op de lijst heeft, keert de bank de cheque uit. Als de cheque niet overeenkomt met een cheque in de lijst, gaat de bank de cheque controleren.

Positief betalen staat ook bekend als SafePay. 

Positieve betalingsbestanden kunnen vertrouwelijke informatie over begunstigden bevatten en chequebedragen. Verzeker daarom dat u de juiste beveiligingsmaatregelen treft vanaf de tijd dat bestanden worden gegenereerd, totdat deze door de bank worden ontvangen. Positief betalen bestanden zijn gedownload volgens de downloadinstructies voor de webbrowser. 

Positieve betalingsbestanden worden gemaakt door gegevensentiteiten te gebruiken. Voordat u een positief betalingsbestand genereert, moet u de transformatie-indelingen instellen voor de XML die de gegevens vertaalt in een indeling die de bank kan gebruiken. 

Wijs voor elke bankrekening waarvoor u positieve betalingsinformatie wilt genereren, de positieve betalingsindeling toe. Nadat u betalingen genereert, kunt u een positief betalingsbestand genereren voor slechts één rechtspersoon en één bankrekening. U kunt ook positieve betalingsbestanden genereren voor meerdere rechtspersonen en bankrekeningen tegelijk. 

Nadat de cheques betaald zijn die in een positive pay-bestand staan geregistreerd, ontvangt u een bevestigingsnummer van uw bank. U kunt het positive pay-bestand dan bevestigen in het systeem. 

Als u een positief betalingsbestand moet wijzigen, kunt u het intrekken. Vervolgens wordt voor elke cheque in het positieve betalingsbestand het veld dat aangeeft of die cheque is opgenomen in een positief betalingsbestand opnieuw ingesteld.

Zie voor meer informatie [Positieve betalingsbestanden instellen en genereren](set-up-generate-positive-pay-files.md).



