---
title: CODA-bankafschrift
description: In dit onderwerp bevat informatie over CODA, een rapportindeling die in het Belgische elektronische banksysteem wordt gebruikt.
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankAccountTable, BankCodaAccountStatement, BankCodaAccountStatementLines, BankCodaParameters, BankCodaTrans, BankCodaTransCategory, BankCodaTransDefTable, BankCodaTransFamily
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 262534
ms.assetid: 38a1f540-1488-4b63-b850-04e270622296
ms.search.region: Belgium
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 187a17ac4c1fb7b30447f7586b57497d7460c694
ms.lasthandoff: 03/31/2017


---

# <a name="coda-bank-statement"></a>CODA-bankafschrift

In dit onderwerp bevat informatie over CODA, een rapportindeling die in het Belgische elektronische banksysteem wordt gebruikt. 

Voor de invoer van Belgische bank-overzicht gebruikt u de CODA-bestandsindeling. Deze functie kunt u de bedrijfsbankrekening openen en eindsaldi controleren en afstemmen van geïmporteerde transacties op basis van afstemmingsregels.

## <a name="import-transactions-from-a-bank-statement"></a>Transacties importeren vanuit een bankafschrift
Voltooi de volgende stappen voor het importeren van een bankafschriftbestand voor een bankrekening. **opmerking**: voordat u een bankafschriftbestand importeert, u moet al hebt uitgevoerd de volgende:

-   De CODA-configuraties van Lifecycle Services (LCS) importeren. Zie voor meer informatie [elektronische downloaden rapportage configuraties vanuit Lifecycle Services](/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).
-   Selecteer het geïmporteerde CODA-configuratie op de **CODA-parameters** pagina.

1.  Ga naar de **bankrekeningen** pagina.
2.  Klik op **afstemmen**&gt;**CODA**.
3.  Klik op **CODA**&gt;**importeren uit bestand**, en selecteer vervolgens het pad naar het bankafschriftbestand.

Wanneer u transacties geïmporteerd, kunt u het volgende doen op de **bankafschrift** pagina.

-   Controleer de begin- en -saldi.
-   De geïmporteerde transacties weergeven als een rapport met bankafschrift die u kunt afdrukken.
-   Geïmporteerde transacties weergeven met extra regels, zoals regels met het rekeningtype 'Geen'. Klik op **CODA &gt;Details**.

## <a name="process-imported-bank-statement-transactions"></a>Proces bankafschrifttransacties geïmporteerd
Voer de volgende stappen uit om de banktransacties van de instructie te verwerken.

1.  Proces details regels (**CODA**&gt;**detailregels verwerken**). Start automatisch afstemmen op basis van **CODA-definities**. Deze regels bepalen welke account grootboek, klant of leverancier moet worden gebruikt voor deze transactie. Vergelijking is gebaseerd op welke transactiegroepscode, transactiecode en transactiecategoriecode zijn opgegeven in de CODA-bestand voor elke transactie.
2.  Transacties met een rekeningtype klanten en leveranciers kunnen worden vergeleken met de facturen. Indien nodig, kunnen de geïmporteerde transacties handmatig worden gewijzigd op elk gewenst moment na de verwerking, alvorens over te boeken naar het grootboek.
3.  Als er transacties met fouten zijn (in het algemeen als er geen regels instellen), deze kunnen worden verwezen naar de speciale grootboekrekening opgegeven op de **CODA-parameters **pagina (**CODA**&gt;**wissen fouten**).
4.  Nadat alle transacties in het bankafschrift worden vereffend, moeten worden overgeboekt naar het grootboekjournaal gereed zijn (**CODA**&gt;**overboeken naar grootboek**). Journaalinstellingen moeten worden opgegeven voor de bankrekening. Journalen kunnen worden geopend op de ** bankrekeningen ** pagina voor de geselecteerde record door te klikken op **instellen**&gt;**CODA-journaal**.

Nadat bankafschrifttransacties verwerken voltooid is, wordt een nieuwe grootboekjournaal gemaakt en geboekt.


