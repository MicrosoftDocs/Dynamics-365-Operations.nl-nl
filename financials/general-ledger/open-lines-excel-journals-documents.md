---
title: Journaalregels en documenten uit Excel publiceren
description: In dit onderwerp wordt uitgelegd hoe invoeren en publiceren van regels voor algemene journalen vanuit Microsoft Excel. Deze bevat informatie over de verschillende sjablonen die u gebruiken kunt, afhankelijk van het type transacties die u invoert.
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
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
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 087339cb3002b42bcb985c2ccfc2d97c752a817c
ms.lasthandoff: 03/31/2017


---

# <a name="publish-journal-lines-and-documents-from-excel"></a>Journaalregels en documenten uit Excel publiceren

In dit onderwerp wordt uitgelegd hoe invoeren en publiceren van regels voor algemene journalen vanuit Microsoft Excel. Deze bevat informatie over de verschillende sjablonen die u gebruiken kunt, afhankelijk van het type transacties die u invoert.

Gebruikers kunnen invoeren en publiceren van regels voor financiële journalen vanuit Microsoft Excel. Nadat een gebruiker een journaal, maakt de **regels in Excel geopend** knop met de sjablonen die beschikbaar zijn weergegeven. Sjablonen zijn ontworpen ter ondersteuning van specifieke scenario's, maar niet alle mogelijke combinaties van rekeningtype in het journaal wordt ondersteund. De volgende tabel ziet u de sjablonen die beschikbaar zijn en de typen ter ondersteuning.
|                          |                                                                                                                         |                                                                                         |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **Template**             | **Ondersteunde typen**                                                                                             | **Het openen van de sjabloon**                                                          |
| Grootboekjournaalregels     | : Grootboek, klant, leverancier, Bank-tegenrekening: grootboek, klant, leverancier, Bank Intercompany wordt ondersteund.       | Algemeen journaal                                                                         |
| Facturenregister         | Rekening: Tegenrekening leverancier: Intercompany grootboek wordt niet ondersteund.                                                    | AP facturenregister                                                                     |
| Facturenjournaal          | Accounts: Leverancier tegenrekening: grootboek Intercompany wordt ondersteund.                                                      | Factuurjournaal leveranciers                                                                      |
| Leveranciersfactuur           |                                                                                                                         | Leveranciersfactuur                                                                          |
| Klantfacturenjournaal | Rekening: Tegenrekening klant: grootboek Intercompany wordt ondersteund.                                                     | Algemeen journaal                                                                         |
| Vrije-tekstfactuur        |                                                                                                                         | Op de **vrije-tekstfactuur** pagina, klikt u op **openen in Excel** (het pictogram van Microsoft Office). |
| Vaste-activajournaal     | Activa met grootboek, bank, klant of leverancier. Intercompany wordt niet ondersteund.                                               | Vaste-activajournaal                                                                     |
| Journaal met betalingen van leverancier   | Rekening: Tegenrekening leverancier: grootboek, Bank Intercompany wordt ondersteund.                                                 | Journaal met betalingen van leverancier                                                                  |
| Journaal met betalingen van klant | Rekening: Tegenrekening klant: grootboek, Bank Intercompany wordt ondersteund.                                               | Journaal met betalingen van klant                                                                |
| Projectonkostenjournaal  | Account: Project, grootboek, klant, leverancier-tegenrekening: Project, grootboek, klant, leverancier Intercompany wordt ondersteund. | Algemeen journaal onkosten (onder projectbeheer en boekhouding)                       |

Wanneer de regels worden gepubliceerd, worden ze gevalideerd om ervoor te zorgen dat ze voldoen aan de regels die zijn ingesteld in de financiële journalen. Nadat de regels worden gepubliceerd, kunnen gebruikers bewerken of de boekstukken boeken vanuit Microsoft Dynamics 365 voor bewerkingen. 

Financiële dimensies aan een sjabloon om toe te voegen zijn meer wijzigingen nodig. Zie voor meer informatie, [dimensies toevoegen aan de Microsoft Excel-sjabloon](\dev-itpro\financial-dimensions\add-dimensions-excel-templates). Nadat de dimensies worden toegevoegd aan de entiteit, worden ze beschikbaar zijn in de Excel-ontwerper en kunnen worden toegevoegd aan de sjabloon.




