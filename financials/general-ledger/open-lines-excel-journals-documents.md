---
title: Journaalregels en documenten publiceren vanuit Excel
description: In dit onderwerp wordt uitgelegd hoe u regels voor algemene journalen invoert en publiceert vanuit Microsoft Excel. U vindt er informatie over de verschillende sjablonen die u gebruiken kunt, afhankelijk van het type transactie dat u invoert.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62213
ms.assetid: 211874a7-4bf0-4a0c-96c2-fa05042777d3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 9726c61b69f79bdd56803ced4c06044dd517ac13
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2017


---

# <a name="publish-journal-lines-and-documents-from-excel"></a>Journaalregels en documenten publiceren vanuit Excel

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt uitgelegd hoe u regels voor algemene journalen invoert en publiceert vanuit Microsoft Excel. U vindt er informatie over de verschillende sjablonen die u gebruiken kunt, afhankelijk van het type transactie dat u invoert.

Gebruikers kunnen regels voor financiële journalen invoeren en publiceren vanuit Microsoft Excel. Nadat een gebruiker een journaal heeft gemaakt, kan hij met de knop **Regels openen in Excel** een lijst met beschikbare sjablonen laten weergeven. Sjablonen zijn ontworpen ter ondersteuning van specifieke scenario's, maar niet elke combinaties van rekeningtypes wordt ondersteund in het journaal. In de volgende tabel ziet u de sjablonen die beschikbaar zijn en de rekeningtypen die ze ondersteunen.
|                          |                                                                                                                         |                                                                                         |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **Sjabloon**             | **Ondersteunde rekeningtypen**                                                                                             | **Hoe de sjabloon te openen**                                                          |
| Grootboekjournaalregels     | Rekening: Grootboek, Klant, Leverancier, Bank Tegenrekening: Grootboek, Klant, Leverancier, Bank Intercompany wordt ondersteund.       | Algemeen journaal                                                                         |
| Facturenregister         | Rekening: Leverancier Tegenrekening: Grootboek Intercompany wordt niet ondersteund.                                                    | Register leveranciersfacturen                                                                     |
| Facturenjournaal          | Rekeningen: Leverancier Tegenrekening: Grootboek Intercompany wordt ondersteund.                                                      | Factuurjournaal leveranciers                                                                      |
| Leveranciersfactuur           |                                                                                                                         | Leveranciersfactuur                                                                          |
| Klantfacturenjournaal | Rekening: Klant Tegenrekening: Grootboek Intercompany wordt ondersteund.                                                     | Algemeen journaal                                                                         |
| Vrije-tekstfactuur        |                                                                                                                         | Klik op de pagina **Vrije-tekstfactuur** op **Openen in Excel** (het Microsoft Office-pictogram). |
| Vaste-activajournaal     | Activum naar grootboek, bank, klant of leverancier. Intercompany wordt niet ondersteund.                                               | Vaste-activajournaal                                                                     |
| Journaal met betalingen van leverancier   | Rekening: Leverancier Tegenrekening: Grootboek, Bank Intercompany wordt ondersteund.                                                 | Journaal met betalingen van leverancier                                                                  |
| Journaal met betalingen van klant | Rekening: Klant Tegenrekening: Grootboek, Bank Intercompany wordt ondersteund.                                               | Journaal met betalingen van klant                                                                |
| Projectonkostenjournaal  | Rekening: Project, Grootboek, Klant, Leverancier Tegenrekening: Project, Grootboek, Klant, Leverancier Intercompany wordt ondersteund. | Algemeen journaal Onkosten (onder Projectbeheer en boekhouding)                       |

Wanneer de regels worden gepubliceerd, worden ze gevalideerd om ervoor te zorgen dat ze voldoen aan de regels die zijn ingesteld in de financiële journalen. Nadat de regels zijn gepubliceerd, kunnen gebruikers de boekstukken bewerken of boeken vanuit Microsoft Dynamics 365 for Operations. 

Het toevoegen van financiële dimensies aan een sjabloon vereist meer wijzigingen. Zie voor meer informatie [Dimensies toevoegen aan de Microsoft Excel-sjabloon](/dynamics365/operations/dev-itpro/financial/add-dimensions-excel-templates). Nadat dimensies zijn toegevoegd aan de entiteit, zijn ze beschikbaar in de Excel-ontwerper en kunnen worden toegevoegd aan de sjabloon.






